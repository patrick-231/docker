# Use the Node.js 20 Alpine image as the base
FROM node:20-alpine

# Create a new group and user named 'app'
# RUN addgroup app && adduser -S -G app app

# Switch to the 'app' user
# USER app

# Set the working directory to '/app'
WORKDIR /app

# Copy the package.json and package-lock.json files to the container
COPY package*.json ./

# Switch back to the 'root' user
# USER root

# Change the ownership of the '/app' directory and its contents to the 'app' user and group
# RUN chown -R app:app .

# Switch back to the 'app' user
# USER app

# Install the project dependencies
RUN npm install

# Copy the entire project directory to the container
COPY . .

# Expose port 5173 for the development server
EXPOSE 5173

# Start the development server
CMD npm run dev