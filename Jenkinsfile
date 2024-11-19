pipeline {
    agent any
    
  
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
                sh 'docker build -t amitkasera2001/node_dockerized_project:v3 .'
            }
        }
         stage('push image to hub') {
            steps {
                script{
                  withCredentials([string(credentialsId: 'dockerhub-pwd', variable: 'dockerhubpwd')]) {
                  sh 'docker login -u amitkasera2001 -p ${dockerhubpwd}'
             }
                 sh 'docker push amitkasera2001/node_dockerized_project:v3' 
              }
            }
        }
        
    }
}
