TeamCity images from JetBrains https://hub.docker.com/u/jetbrains/

1) Setup server:
```
docker run -it --name teamcity-server-instance  -v /C/Users/docker/teamcity/data:/data/teamcity_server/datadir -v /C/Users/docker/teamcity/logs:/opt/teamcity/logs -p 8111:8111 jetbrains/teamcity-server
```

2) Get server IP

Getting container IP
 -  http://stackoverflow.com/questions/17157721/getting-a-docker-containers-ip-address-from-the-host
 -  http://networkstatic.net/10-examples-of-how-to-get-docker-container-ip-address/

3) Setup agent

```
docker run -it --name teamcity-agent-1 -e SERVER_URL="http://172.17.0.1:8111" -v /C/Users/docker/teamcity/agent:/data/teamcity_agent/conf jetbrains/teamcity-minimal-agent
```
