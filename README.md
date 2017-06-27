# Supported tags and respective `Dockerfile` links

 - [`jdk1.8.0_121.c7`, `latest` (jdk1.8.0_121.c7/Dockerfile)](https://github.com/dingwenxiang0/docker-centos-java/blob/jdk1.8.0_121.c7/jdk/1.8.0_121/centos7/Dockerfile)
 - [`jdk1.7.0_80.c7` (jdk1.7.0_80.c7/Dockerfile)](https://github.com/dingwenxiang0/docker-centos-java/blob/jdk1.7.0_80.c7/jdk/1.7.0_80/centos7/Dockerfile)
 - [`jdk1.6.0_45.c7` (jdk1.6.0_45.c7/Dockerfile)](https://github.com/dingwenxiang0/docker-centos-java/blob/jdk1.6.0_45.c7/jdk/1.6.0_45/centos7/Dockerfile)
 - [`jre1.7.0_80.c7` (jre1.7.0_80.c7/Dockerfile)](https://github.com/dingwenxiang0/docker-centos-java/blob/jre1.7.0_80.c7/jre/1.7.0_80/centos7/Dockerfile)
 - [`jre1.6.0_45.c7` (jre1.6.0_45.c7/Dockerfile)](https://github.com/dingwenxiang0/docker-centos-java/blob/jre1.6.0_45.c7/jre/1.6.0_45/centos7/Dockerfile)
 
Subscribe to project updates by watching the [dingwenxiang0/docker-centos-java GitHub repo](https://github.com/dingwenxiang0/docker-centos-java/).
 
# Get this image

The recommended way to get the Dingwenxiang0 CentOS Java Docker Image is to pull the prebuilt image from the [Docker Hub Registry](https://hub.docker.com/r/dingwenxiang0/centos-java/).

```bash
docker pull dingwenxiang0/centos-java
```

To use a specific version, you can pull a versioned tag. You can view the [list of available versions](https://hub.docker.com/r/dingwenxiang0/centos-java/tags/) in the Docker Hub Registry.

```bash
docker pull dingwenxiang0/centos-java:[TAG]
```

# Running Container on java

`docker run -ti --name dingwx-java dingwenxiang0/centos-java:[TAG]`

# Open a shell on it

`docker exec -it dingwx-java bash`

# Kill and remove the container

`docker rm -f dingwx-java`

# Remarks

The cookie `OHS-edelivery.oracle.com-443` in [oracle_download_cookies](https://github.com/dingwenxiang0/docker-centos-java/blob/master/oracle_download_cookies) , and this cookie will expired within 24 hours. (guess)