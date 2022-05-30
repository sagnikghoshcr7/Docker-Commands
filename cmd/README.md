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
#### Execute an Additional Command in a Container
```
> docker exec -it <container id> <command>
Example:
> docker exec -it 093bff89b3 redis-cli
```
![image](https://user-images.githubusercontent.com/58620359/171027516-1913dd60-2c13-4687-ba38-771ed19ea980.png)
```
-it can be written as -i -t
-i for input & -t for beautiful terminal output helpers
```
#### Getting a Command Prompt in a Container
```
> docker exec -it <container id> sh
Example:
> docker exec -it 093bff89b3 sh
```
#### Tagging an Image
```
> docker build -t <username>/<projectname>:<version or tag name> .
Then run it:
> docker run <username>/<projectname>      (default it takes >docker run <username>/<projectname>:latest)
```
![image](https://user-images.githubusercontent.com/58620359/171043547-fc2868ac-ae00-4596-8c8f-767d45e383ac.png)
![image](https://user-images.githubusercontent.com/58620359/171042851-836885a6-6db6-4a47-be77-7e26a6d0de1e.png)
#### Copying Build Files
```
(It will be better to change working directory of the container first and then copy all build files to ignore folder name conflict issue)
> WORKDIR /usr/app
> COPY ./ ./
```
<img src="https://user-images.githubusercontent.com/58620359/171051515-c02a2c0d-8b9e-461b-8ada-6e1595df7090.png" height="300">

#### Container Port Mapping
```
> docker run -p <localhost port>:<container port> <imageid or imagename>
```
![image](https://user-images.githubusercontent.com/58620359/171052747-99a73733-dcb8-4eb4-b653-26ab340e602c.png)

#### Docker-Compose
```
Start Container
> docker-compose up
Rebulid and Start Container
> docker-compose up --build
Launch in Background
> docker-compose up -d
Stop Containers
> docker-compose down
List All Running Containers in Docker-Compose file
> docker-compose ps
```







