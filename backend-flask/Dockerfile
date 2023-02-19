# Base image
FROM python:3.10-slim-buster

# Set the working directory
WORKDIR /backend-flask

# Copy the requirements file
COPY requirements.txt requirements.txt

# Install the requirements
RUN pip3 install -r requirements.txt

# Copy the rest of the files
COPY . .

# Set the environment variables
ENV FLASK_ENV=development

# Expose the port
EXPOSE ${port}

# Run the app
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0", "--port=4567"]
