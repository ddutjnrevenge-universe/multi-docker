# Fibonacci Calculator Web App

## Overview

This web app calculates Fibonacci numbers up to 42. It is built using a multi-container setup with Docker, employing technologies like Node.js, React, Postgres, Nginx, and AWS. The project leverages Docker Compose for local development and deployment, and utilizes Travis CI for continuous integration and deployment.

## Technologies Used

- **Node.js**: Server-side runtime environment.
- **React**: Frontend framework.
- **Postgres**: Database for storing calculated Fibonacci numbers.
- **Nginx**: Web server and reverse proxy.
- **Docker**: Containerization platform.
- **Docker Compose**: Tool for defining and running multi-container Docker applications.
- **Travis CI**: Continuous integration service.
- **AWS**: Cloud platform for deployment.

## Project Structure

- **client**: Contains the React frontend application.
  - `App.js`, `Fib.js`, `OtherPage.js`, etc.
- **nginx**: Configuration files for Nginx.
  - `default.conf`
- **public**: Static assets.
- **server**: Node.js server application.
  - `index.js`, `keys.js`, etc.
- **worker**: Background worker to calculate Fibonacci numbers.
  - `index.js`, `keys.js`, etc.

## Docker Setup

The project includes multiple Dockerfiles for different environments (development and production). Docker Compose is used to orchestrate the services.

- **Dockerfile**: Production Dockerfile.
- **Dockerfile.dev**: Development Dockerfile.
- **docker-compose.yml**: Docker Compose configuration file.

## Deployment

The app is deployed using AWS services, with configurations for VPCs, security groups, and managed data services like RDS and ElastiCache. The deployment process is automated with Travis CI, which builds Docker images and pushes them to Docker Hub.

## Usage

To run the app locally:

1. Ensure Docker and Docker Compose are installed.
2. Clone the repository.
3. Run `docker-compose up --build` to start the services.
4. Access the app at `http://localhost:3000`.

## Additional Information

- Environment variables are managed with Docker Compose and stored securely.
- Continuous integration and deployment are set up with Travis CI.
- Custom Nginx configurations are used for routing and serving the React app.
- AWS resources are managed through Elastic Beanstalk and other AWS services.

For detailed instructions on setup, configuration, and deployment, refer to the individual lesson files in the repository.
