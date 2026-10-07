# docker-workshop
## zoomcamp-data-engineering
### docker - 1
- docker run xyz -> finds image locally -> if not found, pulls from library
- eg)
docker run ubuntu -> pulls image -> docker run -it ubuntu('it' is interactive terminal) -> we will enter container of ubuntu - whatever we do is isolated from host machine
- can do anything inside container(isolated environment) without affecting main system
- ctrl + d -> exit docker to host machine
- docker run -> instance of image is created -> image is completed snapshot of entire os
-  docker run -it python:3.13.11
-  docker run -it python:3.13.11-slim  ---  docker run -it image:tag
- docker run -it --entrypoint=bash python:3.13.11-slim   -> Replace the image's normal startup command with bash
- docker ps -a  -> all docker images executed, all containers
-  docker start -ai kind_almeida (name) / or container id can also be used-> 'ai' is -a  → attach your terminal to the container  , -i  → keep stdin interactive
- docker ps -aq -> gives list of container ids
- docker rm `docker ps -aq` -> removes containers
- echo $(pwd)/test -> /workspaces/docker-workshop/test
- docker run -it --entrypoint=bash -v $(pwd)/test:/app/test python:3.13.11-slim  -> This command creates a container and mounts a folder from your current Linux directory into the container (inside app folder in container); 'v' means volumn mount

### docker 2
- goal:
    1) download csv data from web
    2) transform and clean data with pandas
    3) load it into PostgreSql for quering
    4) Process data in chunks to handle large files
- uv - a modern, fast Python package and project manager written in Rust. It's much faster than pip and handles virtual environments automatically.
- pip install uv
- uv init --python=3.13 -> initialize project with python 3.13
- which python , python -V -> system python(3.14)
- uv run which python , uv run python -V -> python in virtual environment(3.13)
- uv add pandas pyarrow -> it comes as dependencies in .toml file
- 
