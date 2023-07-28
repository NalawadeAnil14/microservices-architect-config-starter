FROM node:8
MAINTAINER Anil Nalawade

#Create work directory 
WORKDIR /app

#Copy files from your current location to /app on container directory
COPY . .

RUN npm install express
RUN npm install

#Application will run on 8080 port so expose that port 
EXPOSE 8080

#Runs in development Mode
CMD ["npm", "start"]
