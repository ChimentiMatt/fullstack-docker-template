# Use Node.js 20
FROM node:20

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package.json package-lock.json ./

# Install dependencies and ensure Vite is installed globally
RUN npm install && npm install -g vite

# Copy the rest of the frontend files
COPY . .

# Expose the frontend port
EXPOSE 3000

# Start the development server
CMD ["npx", "vite", "--host"]
