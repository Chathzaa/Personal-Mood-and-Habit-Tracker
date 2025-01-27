# Start with a base image containing Java runtime (Java 17)
FROM openjdk:17-jdk-alpine

# Add Maintainer Info
LABEL maintainer="your.email@example.com"

# Add a volume pointing to /tmp
VOLUME /tmp

# Make port 8080 available to the world outside this container
EXPOSE 8080

# The application's jar file
ARG JAR_FILE=target/demo-0.0.1-SNAPSHOT.jar

# Add the application's jar to the container
COPY ${JAR_FILE} app.jar

# Run the jar file with recommended JVM options
ENTRYPOINT ["java","-XX:+UnlockExperimentalVMOptions","-XX:+UseContainerSupport","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]
