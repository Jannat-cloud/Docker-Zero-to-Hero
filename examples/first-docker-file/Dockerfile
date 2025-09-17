# Use Python base image
FROM python:3.11-slim

# Set working directory inside the container
WORKDIR /app

# Copy requirements first (if you have one)
# That way Docker can cache dependency installation
COPY requirements.txt .

# Install dependencies
RUN pip install -r requirements.txt

# Copy the rest of the project (including app.py) into /app
COPY . .

# Expose the Flask port
EXPOSE 5000

# Run your app
CMD ["python", "app.py"]
