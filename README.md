# docker-workshop
zoomcamp-data-engineering
- docker run xyz -> finds image locally -> if not found, pulls from library
- eg)
docker run ubuntu -> pulls image -> docker run -it ubuntu('it' is in interactive terminal) -> we will enter container of ubuntu
- can do anything inside container(isolated environment) without affecting main system
- docker container -> instance of docker image; container is complete snapshot of os
- container is stateless - whatever we run in container -> we exit -> we comeback - back to square 1
- docker rm `docker ps -aq` -> cleans up docker containers
- preserve state - 
