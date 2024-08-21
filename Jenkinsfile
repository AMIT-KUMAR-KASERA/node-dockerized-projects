pipeline {
    agent any
    environment {
        DOCKER_HUB_CREDENTIALS = credentials('dockerhub')
        DOCKER_IMAGE = 'amitkasera2001/node_dockerized_project'
    }
  
    stages{
        stage("checkout"){
            steps{
                checkout scm
            }
        }
         stage("Test"){
            steps{
                sh ' sudo apt install npm'
                sh 'chmod +x node_modules/.bin/_mocha'
                sh 'npm test'
            }
        }

        stage("Build"){
            steps{
                sh 'npm run build'
            }
        }


        stage("Build Image"){
            steps{
                sh 'docker build -t amitkasera2001/node_dockerized_project .'
            }
        }
        stage('Docker Push') {
            steps {
              script {
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
                        sh "docker push amitkasera2001/node_dockerized_project"
                    }
                }
            }
        }
    }
}
