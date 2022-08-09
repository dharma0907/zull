#we are building mutistage docker file here
FROM maven:3.6.0-jdk-11-slim AS build
MAINTAINER dharma
WORKDIR /app
COPy . .
RUN mvn install

#jdk
FROM openjdk:11.0.10-jre
WORKDIR /app
#we need to copy artifact that was the output of above build
#artifact will be saved in target folder above, 
COPY --from=build /app/target/shoes-0.0.1-SNAPSHOT.jar /app
EXPOSE 1002
# to run this application give below command
CMD ["java", "-jar", "shoes-0.0.1-SNAPSHOT.jar"]

