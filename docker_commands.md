# Showing running containers
```
docker ps
```

# Showing all of the containers
```
docker ps -a
```
-a : all
shows all containers, including:

    Running

    Exited

    Stopped

    Failed to start

    Created but never run

# Starting a new container
```
docker run - p 6333:6333 -p 6334:6334 qdrant/qdrabt
```
-p : publish


6333:6333  : Maps port 6333 from the container to port 6333 on your local machine

# Stopping a container
```
docker stop <container_id>
```

# Start a container
```
docker start <container_name>
```
# Watching the logs of the container which is running in background
```
docker logs -f <container_name>
```
