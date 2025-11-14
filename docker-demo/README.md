# Build the image
docker build -t nginx-demo .

# Run the container
docker run -d -p 8080:80 nginx-demo

# Stop and remove the old container

docker stop $(docker ps -aq)
docker rm $(docker ps -aq)