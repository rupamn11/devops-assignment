# Step 1: Build the React application
FROM node:18-alpine AS build

WORKDIR /app


# Create app directory
WORKDIR /app

# Copy package files
COPY package*.json ./


RUN npm install

# Copy source code
COPY . .


RUN npm run build

# Step 2: Serve the build using Nginx
FROM nginx:stable-alpine


# Copy the build output from the previous stage to Nginx default web directory
COPY --from=build /app/build /usr/share/nginx/html


# Expose http port
EXPOSE 80


# Start nginx
CMD ["nginx", "-g", "daemon off;"]
