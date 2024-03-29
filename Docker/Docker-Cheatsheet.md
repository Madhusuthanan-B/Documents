### Docker Cheat Sheet

#### Pull a Docker image
```shell
$ docker pull IMAGE_NAME
```

#### Run a docker image
```shell
$ docker run IMAGE_NAME
```

#### List all the running containers (ps - Process Status)
```shell
$ docker ps
```

#### List all containers including running and non-running
```shell
$ docker ps -a
```

#### Remove a container (This will reclaim disk space)
```shell
$ docker rm CONTAINER_ID_OR_CONTAINER_NAME
```

#### Remove multiple containers (Starting of the id would be sufficient instead of full id)
```shell
$ docker rm CONTAINER_ID_1 CONTAINER_ID_2 CONTAINER_ID_3 
$ docker rm 837 9eu oi0 
```

#### View images
```shell
$ docker images
```

#### Remove images
```shell
$ docker rmi IMAGE_NAME
```

#### How to execute commands on a running container (For example, want to view a file within a container)?
```shell
$ docker exec CONTAINER_NAME EXECUTE_THE_COMMAND_HERE
```

#### Find the version of Docker Server Engine running in the host
```
$ docker version
```

#### Run a container with the nginx:1.14-alpine image and name it webapp
```
$ docker run --name webapp nginx:1.14-alpine
```

#### Port mapping (Multiple instancecs of same app can be mapped to different ports and ran simultaneously)
```
$ docker run -p 80:5000 kodekloud/webapp
  docker run -p 8000:5000 kodekloud/webapp
  docker run -p 8001:5000 kodekloud/webapp
```

#### Volume mapping (left side of colon represents the directory within container, right side represents external)
```
$ docker run -v /opt/datadir:/var/lib/mysql mysql
```

#### Passing an environment variable in docker
```
$ docker run -e SAMPLE_ENV_VARIABLE=blue simple-webapp
 docker run -e SAMPLE_ENV_VARIABLE=red simple-webapp
```

##### Notes
* We cannot delete an image when it is being used by a container. 
* In such case, we need to stop the container and then delete the image 
