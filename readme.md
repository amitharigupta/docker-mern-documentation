#Docker Documentation

##1. Create file in root folder and name it to Dockerfile
Contains below line on mentioned file Dockerfile
FROM node:16
WORKDIR /app
COPY ./package*.json ./
RUN npm install
copy . .

CMD ["npm", "run", "start"]

###2. to run the docker command and create image 
  - docker build -t project-imagename . 

###3. To view the images in docker
docker image ls

###4. To create container using docker run the below command in cmd
docker run --name project-containername --rm project-imagename

###5. To check all the docker containers which are running
docker ps

###6. To run container in detach mode on docker
docker run --rm --name project-containername -d -p 3000:3000 project-imagename

###7. To check the logs in docker 
docker logs docker_id