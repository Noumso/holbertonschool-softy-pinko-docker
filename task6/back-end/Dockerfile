# Use the latest Ubuntu image
FROM ubuntu:latest

# Update and upgrade APT
RUN apt-get update && apt-get upgrade -y

# Install Python3, pip3, and Flask
RUN apt-get install -y python3 python3-pip
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED
RUN pip3 install flask flask-cors

# Set the working directory to /app
WORKDIR /app

# Copy the Flask application to the image
COPY ./api.py /app/api.py

# Expose port 5252 for the Flask server
EXPOSE 5252

# Set the default command to run the Flask application
CMD ["python3", "api.py"]
