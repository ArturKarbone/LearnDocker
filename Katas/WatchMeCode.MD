- A tool to build isolated environments and run applications out there. All the dependencies and prerequisites are described via code/commands (configruation as code). Docker executes these commands and set up the environment.
- When I send you a container it goes without saying that you will be able to build and launch it. When I’m sending some jar I don’t know what is installed out there (specific version of TomCat, etc.)
- Configuration as code is encouraged. 
- A container is a deployment unit
- Lightweight virtualization
- Keep your box far more clean
- Multiple services/multiple versions/multiple runtimes
- Analogy: Container is an instance, where an Image is a class


```
docker run hello-world
docker ps -h
docker ps -a -n 5 
docker ps -l
```
Read the output

Image name goes as a last parameter

```
docker run ubuntu
docker logs <name>
docker run -it ubuntu bash
docker run -it ubuntu
docker attach pedantic_keller
```

(latest is like HEAD in git)
```
docker run hello-world:latest 
```

```
docker ps -a
```

http://stackoverflow.com/questions/32811964/filter-docker-images-by-name

```
docker images
docker images hello-world

```
```
docker rmi hello-world
```


Filtering 

https://docs.docker.com/engine/reference/commandline/images/#filtering
http://stackoverflow.com/questions/29406871/how-to-filter-docker-process-based-on-image

```
docker ps -a -f "name=suspicious_bohr"
docker ps -a -f "ancestor=hello-world"
```

```
docker rm $(docker ps -a -q)
docker rmi $(docker images -a | grep "^<none>" | awk '{print $3}')
docker rmi $(docker images -a -q)
```

```
docker rm $(docker ps -a -q -f "ancestor=hello-world")
docker rmi $(docker images -a -q hello-world) 
```

```
docker rm hello-world -> no such container
```

```
docker pull hello-world
```

```
docker images
```

```
docker pull hello-seattle
```

```
docker rmi hello-world/image_id
```

More ambitious  docker run -it ubuntu bash
Quiet output 
```
docker images --help
docker images -aq
docker run -p 80:80 nginx # (name is going to be the last parameter)
docker run -p 80:80 -d nginx #(daemon mode)
docker run -p 80:80 -d --name mynginx nginx #(daemon mode with name)
```

**run** command each time might be a mistake in some cases. Leverage **start**, so you don't have to remember all of this options.

Analogy: image - class, container - instance.

Every time run is used - another instance is created.

ports <local host>:<container> ?

```
docker ps
docker kill modest_stallman

docker pull nginx #(like git)
docker  run --name n1 -p 8080:80 nginx
```


```
docker start/stop/restart
docker stop modest_stallman
docker start modest_stallman
docker run --name nginx
docker logs - name/pid -f (follow)
```

Kitematic docker-> Open Kitematic
GitHub releases
Hello-world-nginx
Volumes


Oracle 

Public repository - https://github.com/wnameless/docker-oracle-xe-11g (read)

Image/container sizes


Official repository https://hub.docker.com/_/rabbitmq/

```
docker pull rabbtimq:management
```

--hostname my-rabbit
docker logs rabbit look for database dir

try without --hostname. start/restart it
play with user name/pasword environment variables

rabbus specs (run)

mongo mount volumes
destroy or recreate container, but still have your data available

```
docker start --help
docker restart mynginx
docker stop mynginx

```

```
docker start container1 container2
```

```
docker exec container #(not realy interactive)
docker exec -it container

docker exec -it mongo mongo 
docker exec -it mongo bash 


docker attach ubuntu
```

docker file reference

FROM alpine
CMD ["echo" , "hello world`"] - what to execute
docker build . (folder)


```
docker run --name test <image id>
```

COPY script.sh /script.sh
CMD ["/script.sh"] 


```
docker inspect c1091c9730ce
```


Look at environment variables https://hub.docker.com/_/nginx/
ENV NGINX_VERSION 1.11.10-1~jessie

```
docker inspect --format="{{.Config.Env}}" mynginx
```

```
docker stats
docker search dotnet
```