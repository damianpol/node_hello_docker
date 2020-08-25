Dockerized learning playground for react

To build the image:
docker build -t damian/node-web-app .

To create and run a container from this image:
docker run -itd --rm -v ${PWD}:/app -v /app/node_modules -p 3001:3000 -e CHOKIDAR_USEPOLLING=true damian/node-web-app

To build and run using docker compose:
docker-compose up -d --build