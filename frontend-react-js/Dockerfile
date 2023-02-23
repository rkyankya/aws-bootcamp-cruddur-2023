# Base Image of Node JS
FROM node:16.18

# Set Environment Variables
ENV PORT=3000

# Copy the files from the current directory to the container
COPY . /frontend-react-js

# Set the working directory to the container
WORKDIR /frontend-react-js

# Install the dependencies
RUN npm install

# Expose the port
EXPOSE ${PORT}

# Run the application
CMD ["npm", "start"]
