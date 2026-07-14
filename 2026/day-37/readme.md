🐳 Docker Cheat Sheet & Revision (Day 37)

📦 Container Commands

Command| Description
"docker run nginx"| Run a new container
"docker run -d nginx"| Run in detached mode
"docker run -it ubuntu bash"| Run interactive container
"docker ps"| List running containers
"docker ps -a"| List all containers
"docker stop <container>"| Stop a container
"docker start <container>"| Start a container
"docker restart <container>"| Restart a container
"docker rm <container>"| Remove a container
"docker exec -it <container> bash"| Open shell inside container
"docker logs <container>"| View container logs
"docker inspect <container>"| Inspect container details



🖼️ Image Commands

Command| Description
"docker images"| List images
"docker pull nginx"| Pull image from Docker Hub
"docker build -t myapp:v1 ."| Build image
"docker tag myapp:v1 username/myapp:v1"| Tag image
"docker push username/myapp:v1"| Push image to Docker Hub
"docker rmi myapp:v1"| Remove image
"docker history myapp:v1"| View image layers



💾 Volume Commands

Command| Description
"docker volume create mydata"| Create volume
"docker volume ls"| List volumes
"docker volume inspect mydata"| Inspect volume
"docker volume rm mydata"| Remove volume



🌐 Network Commands

Command| Description
"docker network create mynet"| Create custom network
"docker network ls"| List networks
"docker network inspect mynet"| Inspect network
"docker network connect mynet container1"| Connect container to network



🐳 Docker Compose Commands

Command| Description
"docker compose up -d"| Start services
"docker compose down"| Stop services
"docker compose ps"| List running services
"docker compose logs"| Show logs
"docker compose build"| Build services
"docker compose restart"| Restart services



🧹 Cleanup Commands

Command| Description
"docker system df"| Show Docker disk usage
"docker system prune"| Remove unused resources
"docker image prune"| Remove unused images
"docker volume prune"| Remove unused volumes
"docker network prune"| Remove unused networks


📝 Dockerfile Instructions

Instruction| Purpose
"FROM"| Base image
"RUN"| Execute commands during build
"COPY"| Copy files into image
"WORKDIR"| Set working directory
"EXPOSE"| Document container port
"ENV"| Set environment variables
"CMD"| Default command
"ENTRYPOINT"| Fixed executable



🎯 Quick Revision Questions & Answers

1. What is the difference between an image and a container?

Image: A read-only template used to create containers.

Container: A running instance of an image.



2. What happens to data inside a container when you remove it?

By default, container data is deleted when the container is removed.

To keep data permanently, use:

- Docker Volumes
- Bind Mounts


3. How do two containers on the same custom network communicate?

They communicate using container names as hostnames.

Example:

"web → db"



4. What does "docker compose down -v" do differently from "docker compose down"?

- "docker compose down" → Removes containers and networks.
- "docker compose down -v" → Removes containers, networks, and volumes.



5. Why are multi-stage builds useful?

- Smaller image size
- Faster builds
- Better security
- Removes unnecessary build files



6. What is the difference between "COPY" and "ADD"?

COPY

- Copies files from local system.

ADD

- Copies files
- Extracts local tar archives automatically
- Can fetch remote URLs (rarely used)

Best Practice: Prefer "COPY" unless you specifically need "ADD".



7. What does "-p 8080:80" mean?

- 8080 → Host Port
- 80 → Container Port

Access the application at:

"http://localhost:8080"



8. How do you check Docker disk usage?

docker system df

It displays the disk usage of:

- Images
- Containers
- Volumes
- Build Cache



📌 Key Takeaways

- Image = Blueprint
- Container = Running Instance
- Volume = Persistent Storage
- Network = Container Communication
- Dockerfile = Build Instructions
- Compose = Multi-container Management
- Multi-stage Builds = Smaller & Cleaner Images
- CMD = Default Command
- ENTRYPOINT = Fixed Executable