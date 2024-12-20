# Use an official Python runtime as a parent image
FROM python:3.12-slim

# Set environment variables
ENV PYTHONUNBUFFERED=1

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt ./

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the application files into the container
COPY ./app /app

# Expose the application port
EXPOSE 8000

# Command to run the application, make sure the module path is correct
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
