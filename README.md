# Multi-Continer-Docker-Environment



Project Summary: Dockerized Microservice Architecture for File Sum Calculation

In this project, I have successfully implemented a Dockerized microservice architecture for file sum calculation. The project showcases my understanding and proficiency in using Docker for containerization and developing containerized applications.

![image](https://github.com/kishore7403/Multi-Continer-Docker-Environment/assets/48860055/ef098a9f-b66e-49a6-8c66-1ea9d1d1b7d1)

The system consists of two containers that communicate with each other through a Docker network. Container 1 acts as the orchestrator and gatekeeper, while Container 2 handles the file calculations. The goal is to receive JSON input, validate it, process the file, and return the calculated sum.

Container 1 listens on port 6000 for JSON input sent via an HTTP POST request to "/calculate". It validates the input JSON to ensure a file name is provided and verifies the existence of the specified file. If the input is invalid or the file is not found, appropriate error messages are returned. Container 1 then sends the file and product parameters to Container 2 using JSON or another preferred method and returns the response received from Container 2.

Container 2, responsible for the file calculations, mounts the host machine directory to a Docker volume and listens on a user-defined endpoint within the Docker network. It loads the specified file into memory, parses it using a chosen CSV library, calculates the sum of rows matching the given product parameter, and returns the result in the appropriate JSON format. If the file is not a valid CSV, an error message indicating the issue is returned.

The communication between the containers is facilitated by the Docker network, ensuring seamless interaction and data exchange.

Throughout the project, I have demonstrated my ability to build containers, configure Docker networks, handle JSON-based data interchange, create Dockerfiles, and utilize Docker commands for container app development. I have also employed Docker Compose to build a multi-container microservice architecture, showcasing my skills in designing and deploying complex systems.

By completing this project, I have not only achieved the learning outcomes related to Docker and its usage but also developed the confidence to dive into more complicated cloud computing tools. The project has enhanced my understanding of containerization, microservice architectures, and the practical implementation of Docker in real-world scenarios.
