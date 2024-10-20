# smucode-service-registry

## Overview
This project is a service registry implemented using Spring Cloud Netflix Eureka.
It serves as a central directory for microservices in the SMU Code ecosystem, enabling service discovery and registration.

## Features
- Eureka Server for service registration and discovery
- Configurable for local and production environments
- Docker support for containerization
- GitHub Actions workflow for CI/CD

## Prerequisites
- Java 17
- Maven
- Docker (for containerization)

## Quick Start

### Local Development
1. Clone the repository:
   ```
   git clone https://github.com/your-repo/smucode-service-registry.git
   ```
2. Navigate to the project directory:
   ```
   cd smucode-service-registry
   ```
3. Run the application:
   ```
   mvn spring-boot:run -Dspring-boot.run.profiles=local
   ```
4. Access the Eureka dashboard at `http://localhost:8761`

## Configuration
- `application.yaml`: Base configuration
- `application-local.yaml`: Local development settings
- `application-prod.yaml`: Production environment settings

## CI/CD
This project uses GitHub Actions for continuous integration and deployment. The workflow is defined in `.github/workflows/build.yaml`.

## Health Check
The application includes a health check endpoint at `/actuator/health`.

## Security
- The service registry is configured not to register with itself or fetch the registry.
- Production configuration uses preferred networks and IP address settings.
