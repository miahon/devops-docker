FROM ubuntu:focal 

RUN apt-get update 
RUN apt-get update && apt-get -y install openjdk-8-jdk
RUN apt-get install -y git
RUN git clone https://github.com/docker-hy/spring-example-project.git
WORKDIR /spring-example-project
RUN ./mvnw package
EXPOSE 8080
CMD ["java","-jar","./target/docker-example-1.1.3.jar"]  

