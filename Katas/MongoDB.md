- https://hub.docker.com/_/mongo/
- https://docs.docker.com/engine/examples/mongodb/#pushing-the-mongodb-image-to-docker-hub

- Dockerize mongo/.net core application/rabbit mq application/ Leverage docker swarm/push to docker hub/deploy to digital ocean instance/deploy to aws/azure/google/setup ci


```
docker run --name mymongo -v /Users/arturk/mongo/:/data/db -d mongo
docker stop mymongo
docker start mymongo
docker restart mymongo
```

Launchig mongo shell:

```
docker exec -it mymongo mongo 
docker exec -it mymongo bash 
```

Launch another container with the same data dir

```
docker run --name mymongo2 -v /Users/arturk/mongo/:/data/db -d mongo
```


Just be aware that different container instance will work with their own data (until volume is introduced)

```
docker run -d mongo
```

- add some dbs/collections
- launch another container via

```
docker run -d mongo
docker exec -it <new container> mongo #exec mongo and check that db/collections created recently do no exist out there. 

```


Container should persist it own state:

```
docker run -d mongo
#create some dbs/collections
docker stop <image>
docker start <image>
#recently created dbs/collection should be there

```
