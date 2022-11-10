See [Markdown Cheatsheet] (https://www.markdownguide.org/cheat-sheet/)

# docker-compose-test

NOTE: It's important to always make sure to delete previous images and containers (running or not running)


- list1
- list2
- list3

First let's start by testing the commands for listing images and containers  
This will show the current containers  

```bash
docker container ls     running
docker container ls -a  running + not running
docker container ls -q  only id
docker container ls -aq only id + running + not running
```  

Now we want to list the current images  
Use these commands:  

```bash
docker image ls         running
docker image ls -a      running + not running
docker image ls -q      only id
docker image ls -aq     only id + running + not running
```

Thus, the commands to remove would be:
```bash
docker container rm -f $(docker container ls -aq)
docker image rm -f $(docker image ls -aq)
```

Regarding networking, we should try these commands:

```bash
docker network ls
do exec -it $CONTAINER_ID sh
```