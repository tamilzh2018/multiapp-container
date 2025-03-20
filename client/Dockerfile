# Use the official Node.js 14-alpine image
FROM node:14-alpine

# Set metadata
LABEL version="1.0"
LABEL description="React Frontend for the Library API"

# Set the working directory in the container
WORKDIR /app

# Copy only package.json and package-lock.json first to leverage Docker's cache
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code into the container
COPY . .

# Expose the port your app runs on (default React app runs on port 3000)
EXPOSE 3000

# Start the React app
CMD ["npm", "run", "start"]

