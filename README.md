# Spring based Java web application- Petclinic
 
Petclinic is a Spring Boot application built using Maven. Sprint Boot dependencies are handled using the pom.xml at the root directory of the repository.

## Execute the application locally and access it using your browser

Move to the directory and Checkout the repo

```
cd spring-petclinic
git clone https://github.com/pdonthala/spring-petclinic.git

```

You can either execute the artifact on your local machine (or) run it as a Docker container.

### Using Docker

Build the Docker Image

```
docker build -t spring-petclinic:v1 .
```

```
docker run -d -p 8080:8080 -t spring-petclinic:v1
```
![Dockerps](https://github.com/user-attachments/assets/dfafca7f-d3fe-4a5b-a0e0-8c848a4bb53a)


Access the application on `http://<ip-address>:8080`

![Page](https://github.com/user-attachments/assets/501d4a82-2e9f-40c5-9739-b7bcebb77e5b)



## Next Steps

# Jenkins Pipeline for Java based application using Maven, SonarQube, Argo CD and Kubernetes


Here are the details to set up an end-to-end Jenkins pipeline for a Java application using SonarQube, Argo CD and Kubernetes:

Prerequisites:

   -  Java application code hosted on a Git repository
   -  Jenkins server
   -  Kubernetes cluster- we are using minikube here
   -  Argo CD

Steps:

    1. Install the necessary Jenkins plugins:
       1.1 Git plugin
       1.2 Maven Integration plugin
       1.3 Pipeline plugin
       1.4 Kubernetes Continuous Deploy plugin
       1.5 SonarQube Scanner

    2. Create a new Jenkins pipeline:
       2.1 In Jenkins, create a new pipeline job and configure it with the Git repository URL for the Java application.
       2.2 Add a Jenkinsfile to the Git repository to define the pipeline stages.
       ![Jenkinsconfig](https://github.com/user-attachments/assets/adceab71-2e0b-4744-b030-fe7d74e31bd0)
       ![Jenkinsconfig2](https://github.com/user-attachments/assets/e067330b-7e46-4f9d-842c-033c0dc192a6)



This end-to-end Jenkins pipeline will automate the entire CI/CD process for a Java application, from code checkout to production deployment, using popular tools like SonarQube, Argo CD and Kubernetes.
