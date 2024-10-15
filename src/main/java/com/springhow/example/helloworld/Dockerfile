# Base image
FROM openjdk:11-jre-slim
 
# Set the working directory inside the container
WORKDIR /app
 
# Copy the built JAR file into the container
COPY target/your-app.jar /app/your-app.jar
 
# Command to run the application
ENTRYPOINT ["java", "-jar", "your-app.jar"]
