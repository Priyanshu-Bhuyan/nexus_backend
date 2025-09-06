FROM openjdk:11-jdk-slim

# Install Maven
RUN apt-get update && apt-get install -y maven && apt-get clean

# Set working directory
WORKDIR /app

# Copy everything
COPY . .

# Build the application
RUN mvn clean package -DskipTests

# Expose port
EXPOSE 8080

# Run the application
CMD ["sh", "-c", "java -Dserver.port=${PORT:-8080} -jar target/*.jar"]
