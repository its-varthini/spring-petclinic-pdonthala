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

Access the application on `http://<ip-address>:8080`


## Next Steps

### Configure a Sonar Server locally

```
apt install unzip
adduser sonarqube
wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.4.0.54424.zip
unzip *
chmod -R 755 /home/sonarqube/sonarqube-9.4.0.54424
chown -R sonarqube:sonarqube /home/sonarqube/sonarqube-9.4.0.54424
cd sonarqube-9.4.0.54424/bin/linux-x86-64/
./sonar.sh start
```

Hurray !! Now you can access the `SonarQube Server` on `http://<ip-address>:9000` 
