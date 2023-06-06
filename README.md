# docker_vettec_20230313

My first docker run commands

docker run -d ubuntu sleep 180 
docker exec -it 78ef1249f /bin/bash

volumes connected to container
docker run -d --name docker -v docker:/tmp ubuntu sleep 180

configure jenkins to use volumes
docker run -d --name jenkins -p 8080:8080 -v docker:/var/jenkins_home jenkins/jenkins

running portainer: docker run -d --name portainer -p 9000:9000 -v portainer_data:/data portainer/portainer-ce