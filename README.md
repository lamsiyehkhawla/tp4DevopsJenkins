# DevOps TP5 – Jenkins CI Pipeline with Docker

## Project Overview

This project demonstrates a simple **DevOps Continuous Integration pipeline** using **Jenkins** and **Docker**.

The goal of this TP is to automatically:

1. Clone a project from GitHub
2. Build a Docker image
3. Push the image to Docker Hub

The pipeline is defined using a **Jenkinsfile**, following the **Pipeline as Code** approach.

---

## Technologies Used

* **Jenkins** – CI/CD automation server
* **Docker** – Containerization platform
* **GitHub** – Source code repository
* **Nginx** – Web server used inside the container

---

## Project Structure

```
tp4DevopsJenkins/
│
├── Dockerfile
├── index.html
└── Jenkinsfile
```

### Dockerfile

Defines the Docker image based on **Nginx** and copies the web page into the container.

### index.html

Simple HTML page served by Nginx.

### Jenkinsfile

Defines the Jenkins pipeline used to automate the build and deployment process.

---

## Pipeline Stages

The Jenkins pipeline performs the following stages:

### 1. Clone Repository

Jenkins retrieves the project from GitHub.

### 2. Build Docker Image

Jenkins builds the Docker image using the Dockerfile.

Example command:

```
docker build -t khawlalams/tp4:1 .
```

### 3. Publish Image

The Docker image is pushed to Docker Hub.

```
docker push khawlalams/tp4:1
```

---

## Docker Hub Image

The built image is available on Docker Hub:

```
https://hub.docker.com/r/khawlalams/tp4
```

---

## How to Run the Container

After pulling the image, the container can be started with:

```
docker run -p 8080:80 khawlalams/tp4:1
```

Then open in the browser:

```
http://localhost:8080
```

---

## Learning Objectives

Through this TP we practiced:

* Creating Docker images
* Using Jenkins pipelines
* Integrating GitHub with Jenkins
* Publishing images to Docker Hub
* Applying CI/CD principles

---

## Author

**Khawla Lamsiyeh**

DevOps / Cloud Computing Practical Work
