FROM node:22.14.0-slim

WORKDIR /frontend

COPY package*.json ./

RUN npm install

COPY ./ ./

# Build the React application
RUN npm run build

# Expose the port that the Node.js application will run on
EXPOSE 3000

# Command that will execute the Node.js application when container starts
CMD ["npm", "run", "start"]