DevOps Assignment: Nginx Reverse Proxy + Docker
This project sets up a robust reverse proxy system using Docker Compose, Nginx, a Golang backend (service_1), and a Python Flask backend (service_2).

Setup Instructions
Clone the repository:

git clone https://github.com/yourusername/devops-reverse-proxy.git
cd devops-reverse-proxy

Run the system using Docker Compose:

docker-compose up --build

Access and test the services:

Golang Service: http://localhost:8080/service1/ping

Flask Service: http://localhost:8080/service2/ping

How Routing Works
Nginx runs in a separate container and listens on port 8080. It routes requests based on the URL path:

/service1/* is forwarded to the Go backend running on port 8001.

/service2/* is forwarded to the Flask backend running on port 8002.

All services are accessible via a single public port: localhost:8080.

Bonus Features Implemented
Logging: Nginx logs each request with timestamp and path, providing clear visibility into traffic.

Health Checks: Docker Compose performs periodic health checks using the /ping endpoints to ensure service availability.

Clean Docker Setup: Each service has its own dedicated Dockerfile and is containerized independently, promoting modularity and maintainability.

Tech Stack
Docker, Docker Compose

Nginx (as reverse proxy)

Golang (Service 1)

Python Flask (Service 2)

Author
Karthik Kotharkar
GitHub: https://github.com/Karthikk29
