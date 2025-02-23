# FastAPI Continuous Deployment with GitHub Actions

## Overview
This repository demonstrates Continuous Deployment by automating the creation and deployment of a Dockerized FastAPI application using GitHub Actions.

## How to Run Locally
1. Clone the repository:
2. Install dependencies:
3. Run FastAPI server:
uvicorn main:app --host 0.0.0.0 --port 8000

markdown
Copy
Edit
4. Open `http://127.0.0.1:8000` in a browser.

## How to Build and Run Docker Image
1. Build Docker image:
docker build -t my-fastapi-app .

markdown
Copy
Edit
2. Run Docker container:
docker run -p 8000:8000 my-fastapi-app

markdown
Copy
Edit
3. Access `http://localhost:8000`.

## GitHub Actions Workflow
- Triggers on every push to the repository.
- Builds and pushes a Docker image to Docker Hub.
- Uses a secret (`DOCKERTOKEN`) for authentication.

## Docker Hub Image
You can pull the image using:
docker pull <your-dockerhub-username>/<image-name>

less
Copy
Edit
Find it at:
[Docker Hub](https://hub.docker.com/r/yash2204/myrepo)
