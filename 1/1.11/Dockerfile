FROM amazoncorretto:8

EXPOSE 8080

WORKDIR /usr/src/app

# Without this
RUN yum install maven -y

COPY ./material-applications/spring-example-project ./

# The next two lines have to be run after copying for ./mvnw package to work
RUN mvn -N io.takari:maven:wrapper
RUN mvn clean package

RUN ./mvnw package

CMD ["java", "-jar", "./target/docker-example-1.1.3.jar"]