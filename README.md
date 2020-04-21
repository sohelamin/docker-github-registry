
# Docker GitHub Package Registry
> A sample docker app for github package registry

## Usage
Just push to the master branch and GitHub action will automatically handle the build & deploy process for you.

## Manual Deploy
1. Build your docker image
	```
	docker build -t sohelamin/docker-node-app .
	```
2. Get the image id
	```
	docker images
	```
3. Login to the github docker package registry using a github token
	```
	docker login docker.pkg.github.com --username sohelamin
	```
4. Tag the image with name & version
	``` 
	docker tag IMAGE_ID docker.pkg.github.com/sohelamin/docker-github-registry/docker-node-app:latest
	```
5.  Push to the registry
	```	
	docker push docker.pkg.github.com/sohelamin/docker-github-registry/docker-node-app:latest
	```
6.  Pull on your server/machine
	```
	docker pull docker.pkg.github.com/sohelamin/docker-github-registry/docker-node-app:latest
	```
