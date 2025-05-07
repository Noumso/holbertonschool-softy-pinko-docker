# Use latest ubuntu image
FROM ubuntu:latest
# Update ubuntu packages, then upgrade packages with -y (yes) option
RUN apt-get update && apt-get upgrade -y
# Install python3 and pip with -y (yes) option
RUN apt-get install -y python3 python3-pip
# Handle error message "error: externally-managed-environment"
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED
# Install python Flask with pip
RUN pip3 install flask
# Install flask-cors (cross-origin requests)
RUN pip3 install flask-cors
# Copy api.py to the flask app directory
COPY ./api.py /app/app.py
# Set the working directory
WORKDIR /app
# Expose port 5252
EXPOSE 5252
# Run the Flask app
CMD ["python3", "app.py"]