# Get the Base image (OS)

FROM python:3.14

# Write the name of maintainer

MAINTAINER Samir

# Create a Working directory to store all the files

WORKDIR /app

# Copy all the source code from the host to the container

COPY . .

# Run the build commands required to install the application

RUN pip install -r requirements.txt

# Indicate the port used

EXPOSE 80

# serve the app / run the app (keep it running)

CMD ["python","run.py"]

