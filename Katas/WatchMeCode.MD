Lightweight virtualization
keep your box far more clean
multiple services/multiple versions/multiple runtimes
Container - Image's instance

Docker run hello-world. Read the output

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
docker images -aq
Docker nginx 
docker run -p 80:80 nginx (name is going to be the last parameter)
docker run -p 80:80 -d nginx (daemon mode)
run command might be a mistake. don't have to remember all of this options

image - class, container - instance

every time run is used - another instance is created
ports <local host>:<container>
docker ps
docker kill modest_stallman

docker pull nginx (like git)
docker  run --name n1 -p 8080:80 nginx
Ports host:docker
-d daemon mode
Docker start/stop
docker stop modest_stallman
docker start modest_stallman
Docker run --name nginx
Docker logs - name/pid -f (follow)
Kitematic docker-> Open Kitematic
GitHub releases
Hello-world-nginx
Volumes
