Lightweight virtualization
keep your box far more clean
multiple services/multiple versions/multiple runtimes
Container - Image's instance

Docker run hello-world. Read the output
docker run -it ubuntu bash
docker run -it ubuntu
docker attach pedantic_keller

Docker run hello-world:latest (latest is like HEAD in git)

Docker ps -a
Docker rmi hello-world
Docker rm hello-world -> no such container
Docker pull hello-world
docker images
docker pull hello-seattle
Docker rmi hello-world/image_id
More ambitious  docker run -it ubuntu bash
Quiet output 
docker images --help
docker images -aq
Docker nginx 
docker run -p 80:80 nginx (name is going to be the last parameter)
docker run -p 80:80 -d nginx (daemon mode)
run command might be a mistake. don't have to remember all of this options

image - class, container - instance

every time run is used - another instance is created
ports <local host>:<container> ?
docker ps
docker kill modest_stallman

docker pull nginx (like git)
docker  run --name n1 -p 8080:80 nginx
Ports host:docker
-d daemon mode
docker start/stop/restart
docker stop modest_stallman
docker start modest_stallman
Docker run --name nginx
Docker logs - name/pid -f (follow)
Kitematic docker-> Open Kitematic
GitHub releases
Hello-world-nginx
Volumes


Oracle 

Public repository - https://github.com/wnameless/docker-oracle-xe-11g (read)

Image/container sizes


Official repository https://hub.docker.com/_/rabbitmq/


docker pull rabbtimq:management

--hostname my-rabbit
docker logs rabbit look for database dir

try without --hostname. start/restart it
play with user name/pasword environment variables

rabbus specs (run)

mongo mount volumes
destroy or recreate container, but still have your data available


docker start --help

docker start container1 container2

docker exec container (not realy interactive)
docker exec -it container

docker exec -it mongo mongo 
docker exec -it mongo bash 


docker attach ubuntu


docker file reference

FROM alpine
CMD ["echo" , "hello world`"] - what to execute
docker build . (folder)

docker run --name test <image id>

COPY script.sh /script.sh
CMD ["/script.sh"] 