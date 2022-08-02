#we are building mutistage docker file here
FROM maven as build
MAINTAINER dharma
WORKDIR /app
COPy . .
RUN mvn install

#jdk
FROM openjdk:11.0.10-jre
WORKDIR /app
#we need to copy artifact that was the output of above build
#artifact will be saved in target folder above, 
COPY --from=build /app/target/zuul-0.0.1-SNAPSHOT.jar /app
EXPOSE 9999
# to run this application give below command
CMD ["java", "-jar", "zuul-0.0.1-SNAPSHOT.jar"]
