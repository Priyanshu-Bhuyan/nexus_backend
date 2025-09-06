FROM openjdk:11-jdk-slim
WORKDIR /app
COPY . .
RUN ./mvnw clean package -DskipTests || mvn clean package -DskipTests
EXPOSE 8080
CMD ["java", "-Dserver.port=${PORT:-8080}", "-jar", "target/*.jar"]
