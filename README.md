# An attempt to structurize my Docker journey

### Definition

Способ развертывания приложений, позволяющий с помощью мета информации (сonfiguration as code) описать, все необходимые зависимости именно среды (т.к. зависимости в виде сторонних библиотек приложения обычно описывают сами с помощью пакетных менеджеров). В дополнении к этому среда будет изолированной.

Конкретный пример: при пересылке ехе файла, требующего специфичной верси .NET, приложение не запустится, хотя казалось бы Windows умеет запускать exe файлы. Java требует еще больших знаний от запускающей стороны (специфичная версия tomcat и т.д.). Для запуска интерпретируемых языков вообще придется настраивать среду и интерпретатор индивидуально.

Docker же выступает, как некий контракт, принятый разными сторонами, который с помощью мета информации полностью описывает и воссоздает необходимую инфраструктуру при запуске. Следовательно, когда стороны обмениваются контейнерами (единица развертывания ПО), мы подразумеваем, что они обладают достаточными знаниями дла настройки своей же собственной инфраструктуры.

A self-sufficient runtime for containers


### Actions

### Ideas

### Blogs

### Podcasts

### Conferences

### OS

### Articles
- [Dockerizing a NodeJs app](https://nodejs.org/en/docs/guides/nodejs-docker-webapp/)
- http://www.levvel.io/blog-post/testing-rabbitmq-clustering-using-docker-part-1/
- https://rominirani.com/docker-toolbox-setup-windows-4d65c3f691eb#.5qgqxuf9k
- [VS Tools for docker tools](https://blogs.msdn.microsoft.com/webdev/2016/11/16/new-docker-tools-for-visual-studio/)
- https://blog.docker.com/2016/09/build-your-first-docker-windows-server-container/
- https://marketplace.visualstudio.com/items?itemName=MicrosoftCloudExplorer.VisualStudioToolsforDocker-Preview

### Patterns 

### StackOverflow

### Meetups
  - https://www.meetup.com/Docker-Online-Meetup/
  
### Youtube channels
  - https://www.youtube.com/user/dockerrun
  
### Videos
- [Auth0 Webinar](https://auth0.com/university/4/docker-101)
- [.NET Docker Development with Visual Studio 2017](https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T111?wt.mc_id=DX_880824)
- [Getting started with .Net and Docker](https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T122/player)
- [Deploying Containers to Azure App Services and Azure Container Service](https://channel9.msdn.com/Events/Visual-Studio/Visual-Studio-2017-Launch/T120/player)
### Whitepapers

### Use Cases

### Katas

### Courses

#### WatchMeCode

- [Docker – Installation & Management](https://sub.watchmecode.net/series/docker/)
- [Docker – Running Services in Containers](https://sub.watchmecode.net/series/docker-services/)
- [Basic Dockerfile Builds](https://sub.watchmecode.net/series/basic-dockerfile-builds/)
- [A Basic Node.js Docker App](https://sub.watchmecode.net/series/basic-node-js-docker-app/)
- [Coding in Docker Containers](https://sub.watchmecode.net/series/coding-docker-containers/)
- [Running Tools in a Docker Container](https://sub.watchmecode.net/series/running-tools-docker-container/)

#### KataCoda 

- https://www.katacoda.com/courses/dotnet-in-docker/deploying-aspnet-core-as-docker-container

#### Eduonix

#### WintellectNow

#### Pluralsight

- [Play by Play: Docker for Web Developers with John Papa and Dan Wahlin](https://www.pluralsight.com/courses/play-by-play-docker-web-developers-john-papa-dan-wahlin)
- 

### Certificates

### Books

### Public Speaking
