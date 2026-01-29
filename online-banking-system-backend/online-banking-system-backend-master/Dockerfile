FROM eclipse-temurin:17-jdk-alpine

WORKDIR /app

COPY . .

# Fix mvnw permission
RUN chmod +x mvnw

# Build the application
RUN ./mvnw clean package -DskipTests

# Copy jar to a fixed name
RUN cp target/*.jar app.jar

EXPOSE 8080

CMD ["java", "-jar", "app.jar"]
