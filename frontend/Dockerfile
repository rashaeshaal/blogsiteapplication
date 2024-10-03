# Use an official Node.js runtime as a parent image
FROM node:16

# Set the working directory in the container
WORKDIR /app

# Copy package.json and install dependencies
COPY package.json ./
RUN npm install

# Copy the rest of the application code
COPY . .

# Start the application
CMD ["npm", "start"]
