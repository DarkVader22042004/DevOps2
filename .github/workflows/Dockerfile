# Use Ubuntu as the base image
FROM ubuntu:latest

# Install required packages
RUN apt update && apt install -y python3 python3-pip

# Set working directory
WORKDIR /app

# Copy application files
COPY . .

# Install dependencies
RUN pip3 install -r requirements.txt

# Expose FastAPI's default port
EXPOSE 8000

# Run FastAPI server
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
