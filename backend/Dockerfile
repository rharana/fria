# Use an official Python runtime as a parent image
FROM python:3.10-slim

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set work directory
WORKDIR /backend

# Install dependencies
COPY requirements.txt /backend/
RUN pip install --no-cache-dir -r requirements.txt

# Copy the project
COPY . /backend/

# Run the Django server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
