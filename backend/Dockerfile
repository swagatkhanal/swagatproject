# Use Node.js 22 as the base image
FROM node:22

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose port 3000 for the backend API
EXPOSE 3000

# Start the application
CMD ["node", "index.js"]
