# Use the Ubuntu base image
FROM ubuntu:latest

# Update and upgrade the package manager
RUN apt-get update && apt-get upgrade -y

# Install python3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove EXTERNALLY-MANAGED error if encountered
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install flask

# Set the working directory to /app
WORKDIR /app

# Copy the api.py file into the container
COPY ./api.py /app/api.py

# Expose port 5252
EXPOSE 5252

# Command to run the Flask app
CMD ["python3", "api.py"]

