# Spring based Java web application- Petclinic
 
Spring Petclinic is a Spring Boot application built using Maven. Sprint Boot dependencies are handled using the pom.xml 
at the root directory of the repository.

## Execute the application locally and access it using your browser

Move to the directory and Checkout the repo

```
cd spring-petclinic
git clone https://github.com/pdonthala/spring-petclinic.git

```


You can either execute the artifact on your local machine (or) run it as a Docker container.

### The Docker way

Build the Docker Image

```
docker build -t spring-petclinic:v1 .
```

```
docker run -d -p 8080:8080 -t spring-petclinic:v1
```
![image](https://github.com/user-attachments/assets/c2dcffdb-85d3-4f16-af3e-aa05df0f51cf)

Access the application on `http://<ip-address>:8080`

![image](https://github.com/user-attachments/assets/669d9ef1-df20-49ee-a97e-ee2448436e40)


## Next Steps

