# Use Node.js Alpine image
FROM node:23-slim

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the app
COPY . .

# Build the React app
RUN npm run build

# Serve with a lightweight web server
RUN npm install -g serve
CMD ["serve", "-s", "build"]

EXPOSE 3000
