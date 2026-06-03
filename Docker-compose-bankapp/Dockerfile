# Get a base image for Java
FROM eclipse-temurin:21-jdk-jammy

# code in a working directory
WORKDIR /app

# Copy all the source files to the container
COPY . .

# Install the libraries with maven

RUN chmod +x mvnw && ./mvnw clean package -DskipTests

# This will list all files in the terminal so we can see the exact spelling/case
RUN ls -la

# indicate the port number to be exposed

EXPOSE 8080

# Entrypoint get perference in entrypoint first opens shell using sh 
# and then write command using -c and paste the commands
ENTRYPOINT ["sh", "-c", "java -jar target/*.jar"] 
# CMD ["java", "-jar" "target/*.jar"]