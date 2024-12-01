# Spring based Java web application- Petclinic
 
Petclinic is a Spring Boot application built using Maven. Sprint Boot dependencies are handled using the pom.xml at the root directory of the repository.

## Execute the application locally and access it using your browser

#### Move to the directory and Checkout the repo

```
cd spring-petclinic
git clone https://github.com/pdonthala/spring-petclinic.git

```

You can either execute the artifact on your local machine (or) run it as a Docker container.

## Using Docker

#### Build the Docker Image

```
docker build -t spring-petclinic:v1 .
```

```
docker run -d -p 8080:8080 -t spring-petclinic:v1
```
![Dockerps](https://github.com/user-attachments/assets/dfafca7f-d3fe-4a5b-a0e0-8c848a4bb53a)


#### Access the application on `http://<ip-address>:8080`

![Page](https://github.com/user-attachments/assets/501d4a82-2e9f-40c5-9739-b7bcebb77e5b)


## Jenkins Pipeline for Java based application using Maven, SonarQube, Argo CD and Kubernetes

Here are the details to set up an end-to-end Jenkins pipeline for a Java application using SonarQube, Argo CD and Kubernetes:

Steps:

#### Configuring the Jenkins Environment
1. Install Jenkins and set it up with the necessary plugins like Git, Pipeline, and SonarQube for static code analysis.
2. Create credentials for secure access to external services (DockerHub, GitHub, Sonarqube ).

#### Create a new Jenkins pipeline:
1. In Jenkins, create a new pipeline job and configure it with the Git repository URL for the Java application.
2. Add a Jenkinsfile to the Git repository to define the pipeline stages.
   ![Jenkinsconfig](https://github.com/user-attachments/assets/adceab71-2e0b-4744-b030-fe7d74e31bd0)
   ![Jenkinsconfig2](https://github.com/user-attachments/assets/e067330b-7e46-4f9d-842c-033c0dc192a6)

#### Writing the Jenkinsfile with the following stages:
1. Build: Compiled the application using Maven.
2. Test: Ran unit tests to ensure code quality.
3. Static Analysis: Integrated SonarCloud to perform code analysis and enforce quality gates.
4. Docker Build & Push: Built a Docker image of the application and pushed it to DockerHub.

#### Setting Up the Application Environment
1. Use Minikube to create a local Kubernetes cluster for deployment testing.
2. Deploy the application using ArgoCD.

#### Testing & Final Deployment
1. Verified the end-to-end functionality of the CI pipeline by running successful builds, Docker image pushes, and Kubernetes deployments.


This end-to-end Jenkins pipeline will automate the entire CI/CD process for a Java application, from code checkout to production deployment, using popular tools like SonarQube, Argo CD and Kubernetes.
