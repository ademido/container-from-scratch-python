# This a demo on how to build a docker

## container-from-scratch-python
This is building a container from scratch

## Build the Container Yourself and Push to Docker Hub

### Build image
*(If you want to develop yourself)* 
> `docker build --tag=ad-demo .`

### List docker images
> `docker image ls`

### Run my newly built container
> `docker run -it ad-demo python app.py --name "AD demo docker"`

### Which docker runs command
> `docker ps`

### Push to Docker Hub
*Note:  You will need to change for your Docker Hub Repo*
`docker push <ECR>/<Container repo>:<tagname>`
When repo generated, you have docker commands provided by AWS, in case you use ECR as docker repo

## Run it yourself at container
```
docker pull <ECR>/<Container repo>:<tagname>
docker run -it <ECR>/<Container repo>:<tagname> bash 
# Then 
run python app.py --name "Hello AD demo docker from bash at docker"
```

## Pass in a command to container
```
docker run -it <ECR>/<Container repo>:<tagname> python app.py --name "Hello AD demo passed to docker"
# The output
Hello AD demo passed to docker!
```

## Push to Amazon ECR
1.  Create ECR repository

### More things Do

* Lint the code with Github Actions (see the Makefile)
* Automatically build the container after lint, and push to DockerHub or some other Container Registery
