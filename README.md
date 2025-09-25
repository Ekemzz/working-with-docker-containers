# working-with-docker-containers
Working with **Docker containers** means running applications in lightweight, isolated environments that package everything the app needs (code, libraries, dependencies). Containers are created from **images** and can be started, stopped, removed, or connected together. 

You typically use commands like
1. `docker run` (to start a container),
2. `docker ps` (to list running containers),
3.  `docker logs` (to see output),
4. `docker exec` (to run commands inside a container), and
5. `docker stop`/`docker rm` (to stop and remove containers). Unlike virtual machines, containers share the host OS kernel, which makes them fast and resource-efficient.


This makes it easy to test, scale, and deploy applications consistently across different environments (developer laptop, test servers, production).
Lets run an ubuntu container. See image for ubuntu container start, and listed containers
i. <img width="963" height="505" alt="image" src="https://github.com/user-attachments/assets/01a55f64-885d-4b13-bd54-2956dd1158e4" />
Let explore options on running containers. docker run -e "MY_VARIABLE=my-value" ubuntu. -e is an environment option
i. <img width="963" height="500" alt="image" src="https://github.com/user-attachments/assets/d7e421a1-7ed7-4128-8fb8-2496e24da158" />
Lets explore running a container in the background. docker run -d ubuntu. -d detaches the run. 
i. <img width="963" height="191" alt="image" src="https://github.com/user-attachments/assets/0392463d-c46c-4de5-8e3d-2b775a97efc5" />


The Docker container lifecycle describes the stages a container goes through from creation to removal:

Created – A container is created from an image using docker create (or docker run, which combines create + start). At this point, it exists but isn’t running.
Running – The container is active, executing its process. You enter this state with docker start or docker run.
Paused – A running container can be paused (its processes frozen) with docker pause and later resumed with docker unpause.
Stopped/Exited – When the container’s main process ends or you stop it manually (docker stop), the container shuts down but still exists on the system.
Deleted/Removed – Once you don’t need it anymore, you remove it completely with docker rm, clearing it from the host.

This lifecycle allows you to control containers flexibly—starting, stopping, reusing, or cleaning them up depending on your workflow.

see image below for demo
<img width="963" height="500" alt="image" src="https://github.com/user-attachments/assets/81f28c9a-2ad4-41b7-ae09-cfaa4c44d820" />


