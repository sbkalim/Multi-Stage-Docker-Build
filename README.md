# Multi-Stage-Docker-Build
# All docker commands used during development, including their purpose

docker login 					
	- Log in to Docker Hub to push images

docker compose build 				
	- Build all services defined in docker-compose.yml

docker build -t sbkalim/flask-app:latest . 	
	- Build an image manually from the Dockerfile

docker compose up 				
	- Start all services from docker-compose.yml

docker compose up --build 	
	- Rebuild and start services (if Dockerfile changed)

docker compose down		
	- Stop and remove containers, networks, volumes

docker compose down -v		
	- Same as above, and remove volumes

docker ps			
	- List running containers

docker images			
	- List all available local images

docker exec -it 65d33162a4b6 /bin/bash	
	- Open shell in a running container

docker images			
	- Get IMAGE ID for tagging/pushing

docker tag flask-app-web sbkalim/flask-app:latest	
	- Add Docker Hub-compatible tag

docker push sbkalim/flask-app:latest	
	- Push image to Docker Hub

docker history sbkalim/flask-app:latest
	- To check the each layer of the image
