# Stage 1: Build the application
FROM node:16.18 AS build

# Set Environment Variables
ENV PORT=3000

# Copy the files from the current directory to the container
COPY . /frontend-react-js

# Set the working directory to the container
WORKDIR /frontend-react-js

# Install the dependencies
RUN npm install

# Build the application
RUN npm run build

# Stage 2: Run the application
FROM node:16.18-alpine

# Set Environment Variables
ENV PORT=3000

# Copy the built application from Stage 1 to the container
COPY --from=build /frontend-react-js/build /frontend-react-js

# Set the working directory to the container
WORKDIR /frontend-react-js

# Expose the port
EXPOSE ${PORT}

# Run the application
CMD ["npm", "start"] 