---
section: Containers
title: Building your first contianer
---

The first step is to create a simple Python script that you want to run inside the container. For example, create a file named `hello.py` with the following content:

```python
print("Hello, Docker!")
```

Once your application is login, we need to package the application into a contianer. Create a **Dockerfile** in the same directory as your Python script. This file contains instructions for building your Docker image. 

Here's an example Python Dockerfile:

```yaml
# Use the official Python image from the Docker Hub
FROM python:3

# Set the working directory inside the container
WORKDIR /app

# Copy the Python script into the container
COPY hello.py .

# Run the Python script when the container starts
CMD ["python", "hello.py"]
```

To build the contianer, open a terminal in the directory containing your Dockerfile and run the following command to build your Docker image:

```bash
docker build -t my-python-app .
```

Once the image is built, you can run a container based on that image. Use the following command to run the container:

```bash
docker run my-python-app
```

You should see the output **"Hello, Docker!"** printed to the console, indicating that your Python script ran successfully inside the container.