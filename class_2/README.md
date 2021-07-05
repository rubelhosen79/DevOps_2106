# Class 2

## Docokerize Nginx in Ubuntu and Run a HTML page

### To build and this docker image, following steps required

```
git clone git@github.com:imrulkk69/DevOps_2106.git

cd /DevOps_2106/class_2

sudo docker build -t imrul/ubuntu-nginx .

sudo docker run -p 8080:80 -d imrul/ubuntu-nginx 


```
### To see all the built image in the system

```
sudo docker images
```

### To see all the containers created

```
sudo docker container ls 
```

### To stop the container 

```
sudo docker stop <container_id>
```

### To remove container 

```
sudo docker rm <container_id>

```

### To remove image

```
sudo docker rmi  <IMAGE>

```

### To access the shell of dockerized linux os 
```
sudo docker exec -it <container_id> /bin/bash
```

### What is `-t, --tty` while running `docker exec` ?

`-t, --tty` Allocate a pseudo-TTY

### What is `-i, --interactive` while running `docker exec` ? 
`-i, --interactive` Keep STDIN open even if not attached

If we only use `-t, --tty` in following command 

```
sudo docker run --tty <container_id> /bin/sh
```
we can not see anything if the shell after running any linux command. Console would not be interactive. 

If you use `-i, --interactive` along with `-t, --tty` then, we can use shell of docker container interectively.

```
sudo docker exec --tty --interactive <container_id> /bin/bash

or in short, 

sudo docker exec -it <container_id> /bin/bash
```





