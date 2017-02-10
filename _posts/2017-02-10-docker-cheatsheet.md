---
layout: post
title: "Docker Cheatsheet"
date: 2017-02-10
---

# {{ post.title }}

`docker build -t <desired-image-name> <context>`

From the Dockerfile in `<context>`, make me an image called `<desired-image-name>` and save it locally.

---

`docker images` 

List images you have locally.

---

`docker rmi <image-name>`

Remove `<image-name>`.

---

`docker run <image-name>` 

Find the image locally, or get it from DockerHub, then run it in a container.

---

`docker ps`

List running containers.

* `-a` List all containers including those not running.

---

`docker stop <container-name>`

Stop a running container.

