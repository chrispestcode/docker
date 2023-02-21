FROM node:12

RUN mkdir /app

#cd into /app folder
WORKDIR /app

COPY package*.json ./

# Like opening terminal and running command. 
# Here we install node modules
RUN npm install

#Copy source code over
COPY . .

ENV PORT=8080

# Access publicly
EXPOSE 8080

# 1 per Docker file
# separated strings is "Exec form"
CMD ["npm", "start"]

#terminal command: docker build -t <dir>/<name>:<major-version>.<minor-version> <local directory to build from>
# To access locally, use p flag to map from local machine to docker container
# docker run -p 5050:8000

# docker run -p 5001:8080 docker.io/fireship/demoapp:1.0   
# npm ERR! missing script: start <-- TROUBLESHOOT: make sure 'start' script exists in package.json

# VOLUMES
# docker volume create shared-stuff
## shared-stuff
# docker run \
# > --mount source=shared-stuff,target=\stuff

# 1 Docker container per microservice

# use `docker-compose up` to build from docker-compose.yml file (INDENTATION IN FILE IS CRITICAL)

# Source: https://www.youtube.com/watch?v=gAkwW2tuIqE