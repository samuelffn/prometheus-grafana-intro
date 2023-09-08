# prometheus-grafana-intro
## Introdução ao Prometheus e Grafana

Downloaded from an Alura course for learning Prometheus and Grafana. Some modifications were made by me.

## Commands

- Build application: **mvn clean package**
- Run application: **sh start.sh**

### About versions
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
  - docker-compose up -d (to not display the logs)

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

## Request
Type: POST  
Url: http://localhost:8080/auth  
Authorization: Bearer Token  
Headers: Content-Type = application/json  
Body:  
- Success:
`
{
"email":"moderador@email.com",
"senha":"123456"
}
`  
- Error:
`
{
"email":"moderador@email.com",
"senha":"123456789"
}
`  

## Capitulo 3 - Aula 01 (with the new stack) 
- Permission required: **chmod 777 prometheus_data** or **chmod 777 -Rvf prometheus**
- Url Topics: http://localhost/topicos
  - http://localhost/topicos/1
  - http://localhost/topicos/2
  - http://localhost/topicos/3  
- Url Metrics: http://localhost/metrics  
- Url Health: http://localhost/health  
- Url Info: http://localhost/info  

## Prometheus
Url Prometheus: http://localhost:9090  
Metrics of Prometheus: http://localhost:9090/metrics (Métricas do próprio Prometheus)  
