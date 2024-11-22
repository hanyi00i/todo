# Use the official Node.js image as the base image  
FROM node:20.12.2-alpine

# Set the working directory  
WORKDIR /usr/src/app  
  
# Copy package.json and package-lock.json  
COPY package*.json ./  
  
# Install dependencies  
RUN npm install  

# Copy the application files  
COPY . .  

RUN npm run build:client
RUN npm run build:server

# Expose the port  
EXPOSE 3000

ENV NODE_ENV=production

# Start the application
CMD ["node", "server.js"]
# CMD [ "npm", "run", "dev" ]
