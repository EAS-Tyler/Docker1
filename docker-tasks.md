### Task 1: Exploring Basic Docker Commands
**Objective:** Get familiar with basic Docker operations.
1. **Install Docker:** Follow official installation guide for your OS.
2. **Run Hello World Container:** `docker run hello-world`
3. **List Containers:** `docker ps` and `docker ps -a`
4. **Pull an Image:** `docker pull nginx`
5. **Run a Detached Container:** `docker run -d -p 8080:80 nginx`
6. **Inspect Running Container:** `docker inspect [container_id]`
7. **Access Logs:** `docker logs [container_id]`
8. **Stop and Remove Container:** `docker stop [container_id]` and `docker rm [container_id]`

### Task 2: Advanced Container Management
**Objective:** Delve into volume management, environment variables, and networking.
1. **Create and Run a Container with a Volume:** 
   `docker run -d --name mycontainer -v myvolume:/data nginx`
2. **Explore Environment Variables:**
   `docker run -d --name myenvcontainer -e "MY_ENV_VAR=HelloDocker" nginx`
3. **Create a Custom Network:**
   `docker network create mynetwork`
4. **Connect Container to Network:**
   `docker network connect mynetwork mycontainer`
5. **Inspect Network:**
   `docker network inspect mynetwork`
6. **Disconnect Container from Network:**
   `docker network disconnect mynetwork mycontainer`
7. **Remove Network:**
   `docker network rm mynetwork`

### Task 3: Building Custom Images with Dockerfile
**Objective:** Learn to create and use Dockerfiles for custom images.
1. **Write a Dockerfile:** Create a Dockerfile with instructions like `FROM`, `RUN`, `COPY`, `EXPOSE`, and `ENTRYPOINT`.
2. **Build the Image:** `docker build -t mycustomimage .`
3. **Run Container from Custom Image:** `docker run -d --name mycustomcontainer -p 5000:80 mycustomimage`
4. **Push Image to Docker Hub:** `docker tag mycustomimage [username]/mycustomimage` then `docker push [username]/mycustomimage`

### Task 4: Docker Compose and Multi-Container Applications
**Objective:** Understand how to define and run multi-container Docker applications.
1. **Create `docker-compose.yml`:** Define a multi-service stack with `services`, `volumes`, and `networks`.
2. **Run Docker Compose:** `docker-compose up -d`
3. **Scale a Service:** `docker-compose up -d --scale service_name=3`
4. **View Compose Logs:** `docker-compose logs`
5. **Exec into a Service Container:** `docker-compose exec service_name /bin/bash`
6. **Stop and Remove Services:** `docker-compose down`

### Task 5: Docker Debugging and Optimization
**Objective:** Master advanced Docker debugging and optimization techniques.
1. **Use Docker Stats:** `docker stats`
2. **Optimize Dockerfile:** Utilize multi-stage builds, minimize layer size.
3. **Security Scanning:** `docker scan [image_name]`
4. **Use Docker Exec for Debugging:** `docker exec -it [container_id] /bin/bash`
5. **Inspect Resource Usage:** `docker system df`
6. **Cleanup Unused Objects:** `docker system prune`