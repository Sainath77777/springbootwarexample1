# Stage 1: Build the application
FROM maven:3.8.6-openjdk-17 AS build
 
# Set the working directory inside the container
WORKDIR /app
 
# Copy the pom.xml and download dependencies
COPY pom.xml .
RUN mvn dependency:go-offline
 
# Copy the rest of the application source code
COPY src ./src
 
# Package the application
RUN mvn clean package 
 
# Copy the packaged JAR from the build stage
COPY  /app/target/*.jar app.jar
 
# Expose the application port (change if needed)
EXPOSE 8080
 
# Define the entry point
ENTRYPOINT ["java", "-jar", "app.jar"]
