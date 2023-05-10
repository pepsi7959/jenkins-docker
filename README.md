# jenkins-docker
jenkins docker


## Prerequisite

* docker 


## Build

build image
```bash
docker build -t docker.io/pepsi7959/jenkins-docker:0.0.1 .
```

tag image
```bash
docker tag docker.io/pepsi7959/jenkins-docker:0.0.1 docker.io/pepsi7959/jenkins-docker:0.0.1
```

push image to registry
```bash
docker tag docker.io/pepsi7959/jenkins-docker:0.0.1 docker.io/pepsi7959/jenkins-docker:0.0.1
```


## How to run

```bash
docker run --name jenkins -d -p 50000:50000 -p 8082:8080 -v /Users/myhost/Documents/jenkins:/var/jenkins_home pepsi7959/jenkins-docker
```

*_if you want to build docker image by jenkins_*
> _note that:_ you docker host must be compatible with docker inside jenkins
```bash
docker run --name jenkins -d -p 50000:50000 -p 8082:8080 -v /Users/myhost/Documents/jenkins:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock pepsi7959/jenkins-docker
```

## *IMPORTANT Pluging*

1. [multibranch scan webhook trigger](https://plugins.jenkins.io/multibranch-scan-webhook-trigger/)
2. [blue ocean](https://plugins.jenkins.io/blueocean/)
