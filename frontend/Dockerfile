# Use the official Node.js 14 image as a base image
FROM node:14

# Set the working directory in the container
WORKDIR /usr/src/app

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Install the application's dependencies inside the container
RUN npm install

# Copy the rest of the application code to the container
COPY . .

RUN chown -R 1001:0 . && chmod -R 777 .

USER 1001

# Exposing Port to the container
EXPOSE 3000

# Specify the command to run when the container starts
CMD [ "npm", "start" ]
