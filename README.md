# prometheus-grafana-intro
## Introdução ao Prometheus e Grafana

Downloaded from an Alura course for learning Prometheus and Grafana. Some modifications were made by me.

## Commands

### Versions
Java version: java --version  
Maven version: mvn --version  
Docker version: docker --version  
Docker Compose version: docker-compose --version  

### Docker
- To start docker on linux (if you need):
  - sudo systemctl start docker docker.socket  
  or
  - sudo service docker start
- To know docker status:
  - sudo systemctl status docker docker.socket  
  or
  - docker ps or docker ps -a
- To download and start docker containers:
  - docker-compose up

### Maven
- To enter the application folder: cd prometheus-grafana-intro/app
- To do dowanload dependencies and application build: mvn clean package
- To run the application: sh start.sh
- To test the application:
  - http://localhost:8080/topicos
  - http://localhost:8080/topicos/1
  - http://localhost:8080/topicos/2
  - http://localhost:8080/topicos/3

### Actuator
- Actuator link refence: https://docs.spring.io/spring-integration/docs/current/reference/html/service-activator.html
- Testing the actuator: 
  - http://localhost:8080/actuator
  - http://localhost:8080/actuator/metrics

### Micromiter
Expose metrics in readable format for Prometheus (em formato legível para o prometheus)
- Micromiter links refence: 
  - https://micrometer.io/
  - https://micrometer.io/docs/installing
- Testing the Prometheus:
  - http://localhost:8080/actuator/prometheus