

# Use the official Node.js image as a base image
FROM node:alpine AS build-step
#FROM node:alpine

# Set the working directory
WORKDIR /app
# WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY backend/package*.json ./
#COPY package*.json .

# Install dependencies
RUN npm install
#RUN npm ci

# Copy the rest of the application code
# COPY . .
COPY backend/ .

# Expose port 3000 (or the port your Node.js app is listening on)
EXPOSE 3000

# Command to run the application
CMD ["node", "start"]
#CMD ["npm", "start"]


