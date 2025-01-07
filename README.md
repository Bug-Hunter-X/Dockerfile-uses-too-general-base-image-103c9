# Dockerfile Best Practices: Using Specific Base Images

This example demonstrates the importance of choosing a specific base image in your Dockerfiles. Using a too general image like `ubuntu:latest` is discouraged for several reasons:

* **Image Size:** General images tend to be large, increasing image download times and storage usage. 
* **Reproducibility Issues:**  `ubuntu:latest` references the latest version of Ubuntu, which could change between builds, potentially leading to unexpected behaviour in your container. 
* **Security Risks:**  Using the latest image automatically implies that the image is built with the latest packages which could contain vulnerabilities. You can easily avoid that by using a specific version. 

This repository provides a Dockerfile with a general base image and a solution that improves image size, consistency, and security. 