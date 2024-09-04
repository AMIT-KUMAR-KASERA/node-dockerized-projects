# <u> CI-CD PIPELINE PROJECT for web application </u>

## Overview



## Features
## software Development challenges


# indrocution 
## 2. jenkins 





### 3. Docker overview
Docker is an open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly. With Docker, you can manage your infrastructure in the same ways you manage your applications. By taking advantage of Docker's methodologies for shipping, testing, and deploying code, you can significantly reduce the delay between writing code and running it in production.
### The Docker platform
 * Docker provides the ability to package and run an application in a loosely isolated environment called a container. The isolation and security lets you run many containers simultaneously on a given host. Containers are lightweight and contain everything needed to run the application, so you don't need to rely on what's installed on the host. You can share containers while you work, and be sure that everyone you share with gets the same container that works in the same way.

* Docker provides tooling and a platform to manage the lifecycle of your containers:

* Develop your application and its supporting components using containers.
* The container becomes the unit for distributing and testing your application.
* When you're ready, deploy your application into your production environment, as a container or an orchestrated service. This works the same whether your production environment is a local data center, a cloud provider, or a hybrid of the two.

#### What can I use Docker for?
Fast, consistent delivery of your applications
Docker streamlines the development lifecycle by allowing developers to work in standardized environments using local containers which provide your applications and services. Containers are great for continuous integration and continuous delivery (CI/CD) workflows.

Consider the following example scenario:

Your developers write code locally and share their work with their colleagues using Docker containers.
They use Docker to push their applications into a test environment and run automated and manual tests.
When developers find bugs, they can fix them in the development environment and redeploy them to the test environment for testing and validation.
When testing is complete, getting the fix to the customer is as simple as pushing the updated image to the production environment.

#### Responsive deployment and scaling
Docker's container-based platform allows for highly portable workloads. Docker containers can run on a developer's local laptop, on physical or virtual machines in a data center, on cloud providers, or in a mixture of environments.

Docker's portability and lightweight nature also make it easy to dynamically manage workloads, scaling up or tearing down applications and services as business needs dictate, in near real time.

#### Running more workloads on the same hardware
Docker is lightweight and fast. It provides a viable, cost-effective alternative to hypervisor-based virtual machines, so you can use more of your server capacity to achieve your business goals. Docker is perfect for high density environments and for small and medium deployments where you need to do more with fewer resources.
#### you can get more information
https://docs.docker.com/guides/docker-overview/
### 4. kubernates
* Kubernetes is an open-source container orchestration system for automating the deployment, scaling, and management of containerized applications.

* this process is also called container orchestration.
kubernates surfaced from work at google in 2014, and become the standard way of managing containers.

* although originally designed by google, it is now an open source project maintend by the cloud native computing foudation(CNCF), with significant open source contributions from Red Had and IBM.


### 4. Ansible
#### what is ansible
* Ansible is an open-source automation tool. you can use ansible to manage one or many computer at once.

* can do tasks like configuration management, application deployment,infrastructure setup etc.

* the details about the resources to manage(hosts) is kept in a file called ansible Inventory.

* the instructions to run on hosts are kept in a YML files called playbooks.

* when playbook is run, connection is made to the host systems and playbook instruction are executed on the hosts.

![](https://miro.medium.com/max/708/1*8H4XYCNV-xamG0joz22apQ.png)




## tools and technologies
* Git - Version control system.
* Jenkins - Automation server for CI/CD.
* Docker - Containerization platform.
* Kubernetes - Container orchestration.
* Ansible - Configuration management.



## Steps to Build the Project:
#### Setup Git Repository:

Create a GitHub repository for your project.
Push a sample web application code (e.g., a simple Node.js application) to the repository.
#### Setup Jenkins:

Install Jenkins on your local machine Jenkins service.
Configure Jenkins to pull code from your GitHub repository.
Create a Jenkins pipeline script (Jenkinsfile) to define your CI/CD pipeline.
#### Dockerize the Application:

Write a Dockerfile for your application.
Build and push the Docker image to Docker Hub or any other container registry.
#### Deploy with Kubernetes:

Write Kubernetes deployment and service YAML files.
Use kubectl to apply these files and deploy your application to a Kubernetes cluster.
You can use a local Kubernetes cluster like Minikube or a managed Kubernetes service from a cloud provider.
#### Automate Configuration with Ansible:

Write Ansible playbooks to automate the setup of your infrastructure (e.g., installing Docker, setting up Kubernetes).

#### Integrate Jenkins with Docker and Kubernetes:

Update your Jenkins pipeline to build the Docker image, push it to the registry, and deploy it to the Kubernetes cluster.
## Installation
### jenkins installations
#### jenkins installation in ubuntu
##### Prerequisites
Minimum hardware requirements:

256 MB of RAM

1 GB of drive space (although 10 GB is a recommended minimum if running Jenkins as a Docker container)

Recommended hardware configuration for a small team:

4 GB+ of RAM

50 GB+ of drive space

Software requirements:

Java: see the Java Requirements page

Web browser: see the Web Browser Compatibility page

For Windows operating system: Windows Support Policy

For Linux operating system: Linux Support Policy

For servlet containers: Servlet Container Support Policy

https://www.jenkins.io/doc/book/installing/linux/#linux
### docker installation in windows/linux
* the  pc must have virtualization capabilities 
* the virtualization must be enabled in both os and bios 
* windows 11 64-bit: pro version 21HZ or higher, or enterprise or education.
* windows 10 64-bit : pro(build/9041) or higher, or enterprise or education.
* for windows 10 and window 11, see system requirement for WSL 2 backend.
* Hyper-v and containers windows features must be enabled.

https://docs.docker.com/desktop/install/windows-install/
### kubernates installation
https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/

https://minikube.sigs.k8s.io/docs/start/?arch=%2Fwindows%2Fx86-64%2Fstable%2F.exe+download

### ansible instatllations 


## step by step building a ci/cd pipeline
#### Step 1: Setup Git Repository
  ##### 1. Create a GitHub Repository:

* Go to GitHub.
* Sign in or create an account.
* Click on the New button to create a new repository.
* Name your repository (e.g.<b>node-dockerized-projects </b> ).
* Add a README file (optional).
* Click on Create repository.
##### 2. Push Sample Web Application Code:
* <b><u>Clone the repository to your local machine.</b><u>
  git clone https://github.com/AMIT-KUMAR-KASERA/node-dockerized-projects.git
 cd ci-cd-pipeline-sample


#### Step 2: Setup Jenkins
##### 1. Install Jenkins:

* Download and install Jenkins from here.
* Follow the installation instructions for your operating system.
##### 2. Configure Jenkins:

* Open Jenkins in your browser (http://localhost:8080).
* Complete the setup wizard and install the recommended plugins.
* Create an admin user.
##### 3. Create a Jenkins Pipeline:

* Go to Jenkins dashboard.
* Click on New Item.
* Enter a name for your pipeline (e.g., ci-cd-pipeline).
* Select Pipeline and click OK.
* In the pipeline configuration, scroll down to the Pipeline section.
* Select Pipeline script from SCM.
* Choose Git and enter your repository URL.
* Add a Jenkinsfile to your repository with the following content
