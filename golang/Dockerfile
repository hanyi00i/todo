# Use the official Node.js image as the base image  
FROM golang:1.23-alpine

# Set the working directory  
WORKDIR /usr/src/app

# Copy the CA certificate to the container
COPY cert-and-chain.crt /usr/local/share/ca-certificates/cert-and-chain.crt

# Update the CA certificates
RUN update-ca-certificates

# Copy package.json and package-lock.json  
COPY go.mod go.sum ./ 
  
# Install dependencies  
RUN go mod download
  
# Copy the application files  
COPY . .  

# Build the Go application
RUN go build -o main .

# Expose the port  
EXPOSE 8080
  
# Start the application
CMD ["./main"]
