#We want to use Node 16 as the base image
FROM node:16

#We want to set the working directory to /usr/src/app
WORKDIR /usr/src/app

#Runs off the port 5000
EXPOSE 5000

ENV REACT_APP_BACKEND_URL=http://localhost:8080

#We want to copy the package.json and package-lock.json files
COPY package*.json ./

#We want to install the dependencies
RUN npm install

#We want to copy the rest of the files
COPY . .

#First you need to build the static files
RUN npm run build

#We want to install serve
RUN npm install -g serve

#We want to start the server
CMD ["serve", "-s", "-l", "5000", "build"]