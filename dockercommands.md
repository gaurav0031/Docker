# 🐳 Complete Docker Command Guide

This document contains all Docker commands I used during my hands-on DevOps practice along with explanations.  
It serves as my personal Docker reference and revision guide.

---

1️⃣docker images

What it does:

Lists all Docker images available on your system.

Shows:

Repository name

Tag

Image ID

Created date

Size

Used When:

To verify image build

To check image size

Before deleting an image

2️⃣ docker ps
docker ps
What it does:

Lists currently running containers.

Shows:

Container ID

Image name

Status

Ports

Container name

3️⃣ docker ps -a
docker ps -a
What it does:

Shows all containers (running + stopped).

4️⃣ docker build -t
docker build -t flask-app .
What it does:

Builds a Docker image from a Dockerfile.

Breakdown:

-t flask-app → Tags image name

. → Current directory as build context

Used When:

Creating custom images (Java / Flask apps)

5️⃣ docker run
Basic Run
docker run flask-app
What it does:

Creates and starts a container from an image.

Detached Mode
docker run -d flask-app
What it does:

Runs container in background.

Port Mapping
docker run -d -p 80:80 flask-app
What it does:

Maps:

Host Port 80 → Container Port 80

Environment Variables
docker run -e MYSQL_ROOT_PASSWORD=root mysql
What it does:

Passes environment variable inside container.

Used for:

Database passwords

App configuration

Named Container
docker run --name mysql-container mysql
What it does:

Assigns custom name instead of random name.

6️⃣ docker stop
docker stop <container_id>
What it does:

Stops running container.

7️⃣ docker start
docker start <container_id>
What it does:

Starts previously stopped container.

8️⃣ docker rm
docker rm <container_id>
What it does:

Deletes container (must be stopped first).

9️⃣ docker rmi
docker rmi <image_id>
What it does:

Deletes Docker image.

🔟 docker exec -it
docker exec -it mysql-container bash
What it does:

Executes command inside running container.

Breakdown:

-i → Interactive

-t → Terminal

bash → Opens shell inside container

Used for:

Accessing MySQL shell

Debugging inside container

1️⃣1️⃣ docker logs
docker logs <container_id>
What it does:

Displays container logs.

Used for:

Debugging

Checking API calls

Monitoring container behavior

1️⃣2️⃣ docker attach
docker attach <container_id>
What it does:

Attach to running container process.

Important:

Detach safely using:

CTRL + P + Q
1️⃣3️⃣ docker image prune
docker image prune
What it does:

Removes unused images.

1️⃣4️⃣ docker system prune
docker system prune
What it does:

Removes:

Stopped containers

Unused networks

Dangling images

1️⃣5️⃣ docker pull
docker pull mysql
What it does:

Downloads image from Docker Hub.

1️⃣6️⃣ docker system df
docker system df
What it does:

Shows Docker disk usage.

1️⃣7️⃣ docker volume ls
docker volume ls
What it does:

Lists Docker volumes.

1️⃣8️⃣ docker volume prune
docker volume prune
What it does:

Removes unused volumes.

1️⃣9️⃣ docker buildx create --use
docker buildx create --use
What it does:

Enables modern BuildKit builder.

Used to:

Improve performance

Advanced builds

Multi-platform builds

🔥 Dockerfile Commands Used
FROM
FROM python:3.10

Defines base image.

WORKDIR
WORKDIR /app

Sets working directory inside container.

COPY
COPY . .

Copies files from host → container.

RUN
RUN pip install -r requirements.txt

Executes command during build.

CMD
CMD ["python","app.py"]

Default command when container runs.

ENTRYPOINT
ENTRYPOINT ["python","run.py"]

Defines main container execution command.

🧠 Important Concepts Learned
Image vs Container

Image = Blueprint
Container = Running instance

Layer Caching

If Dockerfile step unchanged, Docker shows:

Using cache

Speeds up builds.

Port Mapping
HostPort:ContainerPort

Example:

80:80
Detached Mode

-d runs container in background.

Environment Variables

-e injects runtime configuration.

Security Group (AWS)

If port is not opened in EC2 Security Group:
Application will not be accessible externally.

🚀 Interview Tip
Difference between docker build and docker run

docker build → Creates image

docker run → Creates container from image

📊 Real Workflow Practiced
Build Image → Run Container → View Logs → Stop → Restart → Remove → Clean
🏁 Conclusion

This guide covers all Docker commands I practiced during real AWS EC2 deployment, Flask app containerization, Java app containerization, and MySQL setup.

This README acts as my personal DevOps reference guide.
