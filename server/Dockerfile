# FROM node:18-alpine

# WORKDIR /app

# COPY package*.json ./

# RUN npm install

# COPY . .

# EXPOSE 4000

# CMD ["node", "index.js"]



# Use Node 18
FROM node:18-alpine

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build TypeScript
RUN npm run build

# Expose the port you use (match PORT in .env)
EXPOSE 5000

# Start the application
CMD ["node", "dist/server.js"]
