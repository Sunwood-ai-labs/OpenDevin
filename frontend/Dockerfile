# Use an official Node.js runtime as the base image
FROM node:18.19.1-bullseye

RUN apt update -y 
RUN apt install -y iputils-ping net-tools

# Set the working directory in the container
WORKDIR /app

# Copy the entire frontend directory to the working directory
COPY . .

WORKDIR /app/frontend

# Install dependencies
RUN npm install



# Build the frontend app
RUN npm run build
RUN npm install -g wscat

# Expose the port on which the app will run
EXPOSE 3003

# Define the command to run the app
CMD ["npm", "start", "--", "--port", "3003", "--host"]