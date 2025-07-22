# Use Node.js base image
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Install dependencies
COPY frontend-react/package*.json ./
RUN npm install

# Copy source and build
COPY frontend-react .
RUN npm run build

# Install a static file server
RUN npm install -g serve

# Expose port 3000 (serve uses 3000 by default)
EXPOSE 3000

# Start the production server
CMD ["serve", "-s", "dist", "-l", "3000"]