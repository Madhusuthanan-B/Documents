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
