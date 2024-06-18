Clear container
docker stop $(docker ps -aq)
docker rm -vf $(docker ps -aq)
docker rmi -f $(docker images -aq)
docker volume rm $(docker volume ls -qf dangling=true)
