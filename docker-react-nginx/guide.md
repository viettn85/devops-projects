# Setup Environment

- Create react app: npx create-react-app docker-react-nginx
- Copy Dockerfiles and docker-compose to the react project

# Development

- docker build -t app:dev .
- docker run -it --rm -v \${PWD}:/app -v /app/node_modules -p 3001:3000 -e CHOKIDAR_USEPOLLING=true -d app:dev
- docker-compose up -d --build
- docker run -it --rm -v \${PWD}:/app -v /app/node_modules -p 3001:3000 -e CHOKIDAR_USEPOLLING=true -d docker-react-nginx_dev
- docker-compose stop

# Production

- docker build -f Dockerfile.prod -t app:prod .
- docker run -it --rm -p 1337:80 app:prod
-
