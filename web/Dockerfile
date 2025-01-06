# Use a Node.js base image
FROM node:18-slim

# Set the working directory inside the container
WORKDIR /web

# Copy package.json, pnpm-lock.yaml, and .env.sample to the working directory
COPY package.json pnpm-lock.yaml ./

# Install pnpm globally
RUN npm install -g pnpm


# Install dependencies using pnpm
RUN pnpm install

# Copy the rest of the project files to the container
COPY . .

# Expose the development server port
EXPOSE 3000

# Command to run the development server
CMD ["pnpm", "dev"]
