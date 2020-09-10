# Introduction

This repository includes devops projects using Docker and related tools/frameworks

# Docker notes

- [Dockerfile Best Practice](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)
- [Docker Development Best Practice](https://docs.docker.com/develop/dev-best-practices/)
- [Docker Cheatsheet](https://www.docker.com/sites/default/files/d8/2019-09/docker-cheat-sheet.pdf)

# AWS

- [Copy files from EC2 to Local and vice versa](https://medium.com/@dearsikandarkhan/files-copying-between-aws-ec2-and-local-d07ed205eefa)

  scp -i PEM_PATH LOCAL_PATH USER@EC2_HOST:EC2_PATH

  scp -i PEM_PATH USER@EC2_HOST:EC2_PATH LOCAL_PATH

- [AWS Policy Generator](https://awspolicygen.s3.amazonaws.com/policygen.html)

# Commands

- [Find and kill process locking port](https://stackoverflow.com/questions/3855127/find-and-kill-process-locking-port-3000-on-mac)

  netstat -vanp tcp | grep PORT

  sudo lsof -i tcp:PORT

  lsof -ti:PORT | xargs kill

  kill \$(lsof -ti:3000,3001)

  npx kill-port 3000

- [Start Docker Daemon on Mac](https://superuser.com/questions/1276583/starting-docker-daemon-on-mac)

  open --background -a Docker

- [Install ps](https://github.com/tianon/docker-brew-debian/issues/13)

  apt-get install -y procps

  yum install -y procps
