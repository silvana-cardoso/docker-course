#################################################
##### instractions for setting up the image #####
#################################################

# name of the base image
# exits on dockerhub or locally
FROM node:12

# default: root
# all comands wil be executed from inside this folder
WORKDIR /app
# which files on local mashine should go to the image
# COPY . .
# . : the same folder that contains the Dockerfile
# . : path inside the image that this files should be stored
# ./ : due to current working directory
# it is recommended use a subfolder, not the root

# copy first the specificaions of node.js to install
COPY package.json /app

# install all the dependecies for node app
RUN npm install

# copy the source code again
# doesn't install npm every time the source code is changed
COPY . /app

# a docker container is by default isolated from our local environment
# let docker know that when this container is started
# we wanna expose a certain port to our local system
EXPOSE 80
# that is incorrect beacause we would try to start the server in the image
# the image is the template, the container based on the image is the execution
# RUN node server.js
# executed when a container is started based on the image
# node server.js
CMD ["node", "server.js"]