- https://www.pluralsight.com/courses/play-by-play-docker-web-developers-john-papa-dan-wahlin
- Massive interest from developers
- Bring up envirionment consistently
- Sometimes it takes weeks for new devs in a company to be productive (permissions, complex setup, etc.)
- Accelerate developer onboarding
- Eliminate app conflicts
- Introduce ousource designers, just by giving them two commands
- No more works on my machine
- A lot of preconfigured environments - mongo, node, .NET, etc.
- https://www.docker.com/products/docker-toolbox a VM and a set of tools around it
- Docker compose 
- Don't need to know a lot about Linux, unless you really want to build some custom stuff
- docker-machine ip
- docker-machine ls
- try docker ps (from new terminal)
- docker-machine env (to hook your console) # Run this command to configure your shell
- docker hub (node)
- image - layered cake ( i already have Ubuntu layer, so i don't have to download it)
- docker cloud https://cloud.docker.com/swarm/arturkarbone/dashboard/onboarding/continuous-integration
- kitematic my repos/recommended
- reverse proxy round robin
- docker pull - layers
- docker pull kitematic/hello-world-nginx
- docker run kitematic/hello-world-nginx (can't reach - expose external port)
- docker ps (see port 80 - exposed only internally)
- docker stop a4
- docker ps -a --format "table {{.ID}}\t{{.Command}}"
- .docker config.json change templates
- docker run -d -p 8080:80 kitematic/hello-world-nginx 
- docker-compose build
- docker-compose up
- docker-compose down
- docker-compose logs
- docker ps -a
- .docker dir useful commands
- https://github.com/DanWahlin/Angular-RESTfulService