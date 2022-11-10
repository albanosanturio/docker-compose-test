# docker-compose-test

Important: always check to delete previous images and containers (running or not running)

docker container ls     running
docker container ls -a  running + not running
docker container ls -q  only id
docker container ls -aq only id + running + not running


docker image ls         running
docker image ls -a      running + not running
docker image ls -q      only id
docker image ls -aq     only id + running + not running

So, to remove:
docker container rm -f $(docker container ls -aq)
docker image rm -f $(docker image ls -aq)

Updating: