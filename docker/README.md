Docker setup in Mac
// install docker in mac
download Docker Desktop for Mac
double click icon and drag into Application

// version check
$ docker version

// Docker ubuntu 20.04 LTS image install
$ docker run  -d -t --name ubuntu ubuntu:20.04

// Run contatiner (want exit? —> $ exit)
$ docker exec -it ubuntu bash

// version check 
$ cat /etc/os-release

// check running container
$ docker ps

// stop container
$ docker stop [container_id]

// check stopped container / checking deleted container
$ docker ps -a

// delete container
$ docker rm [container_id1] [container_id2]

// currently installed images check
$ docker images

// delete image
$ docker rmi [img_id]

// delete container b4 deleting image
$ docker rmi -f [img_id]

