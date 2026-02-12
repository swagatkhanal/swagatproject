FROM node:22-alpine

# Install curl so the healthcheck in docker-compose works
RUN apk add --no-cache curl

WORKDIR /app

# Copy package files first for better caching
COPY package*.json ./
RUN npm install --omit=dev

# Copy the rest of the app
COPY . .

EXPOSE 3000

# Start command as per README requirements
CMD ["node", "index.js"]
