# docker-udm-course-2509
Docker course with several examples to practice

df -ha

docker run node
docker ps -a
docker run -it node
.exit

docker run -p 3000:80 -d <image hash> // detach the atached default
docker logs <container name>

## run in interative mode

docker run -it <hash>
docker start -a -i <container name>

## delete container

docker rm <container name 1> <container name 2> ...
docker rmi <image name>

## list all available images
docker images

## run and remove container when shutdown
docker run -it --rm <hash image>

docker image inspect <image id>

docker cp <folder>\<file> <container name>:<folder>

## run container image first time detached with a name routing port 3000 external to 80 internal
docker run -p 3000:80 -d --name <container name> <image hash>

## build image having repository name and tag in current directory
docker build -t <repository name>:<tag> .

## assing existing images new image names with tags (latest)
docker tag <old image name>:<tag> <new image name>:<tag>

docker login
docker logout