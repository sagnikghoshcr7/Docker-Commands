# Docker-Commands

#### Creating and Running a Container from an Image
```
> docker run <image name>
docker run = docker create + docker start
```
#### Overriding Default Commands
```
> docker run <image name> command!
Example:
> docker run busybox hi there
> docker run busybox ls
```
![image](https://user-images.githubusercontent.com/58620359/171022539-fee431f6-6fd6-40af-9273-47f7900834ce.png)
#### List All Running Containers
```
> docker ps --all
```
#### List All Containers
```
> docker ps
```
#### Create a Container
```
> docker create <container id>
```
#### Start a Container
```
> docker start <container id>
```
#### Remove all Containers and Cache
```
> docker system prune
```
#### Get logs from a Container
```
> docker logs <container id>
```
#### Stop a Container
```
> docker stop <container id>
```
#### Kill a Container
```
> docker kill <container id>
```







