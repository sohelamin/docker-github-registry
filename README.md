# docker-github-registry

## Usage
docker build -t sohelamin/docker-node-app .
docker images

docker login docker.pkg.github.com --username sohelamin
docker tag IMAGE_ID docker.pkg.github.com/sohelamin/docker-github-registry/docker-node-app:latest
docker push docker.pkg.github.com/sohelamin/docker-github-registry/docker-node-app:latest
