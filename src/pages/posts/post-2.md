---
layout: '../../layouts/MarkdownPost.astro'
title: 'Build Mniniflux on ARM64 VPS'
pubDate: 2023-03-19
description: ''
author: 'Space Cat'
cover:
    url: 'https://assets.morefish.win/cat_likes_more_fish_808daac3-1110-40af-b9a5-feaf29d3f5b7.png'
    square: 'https://assets.morefish.win/cat_likes_more_fish_808daac3-1110-40af-b9a5-feaf29d3f5b7.png'
    alt: 'cover'
tags: ["Small talk"]
theme: 'light'
featured: true
---

I follow detailed instruction by [Docker 快速搭建 Miniflux + RSSHub](https://www.jkg.tw/p3246/) and successfully build my own self hosting Miniflux Rss reader.

The installation is much simpler compare with that of Fressrss (I spent almost one day without success).

In the course of intalling Miniflux, I learned some basic and useful commands of Docker.

### update & upgrade docker

```docker
    sudo apt update && sudo apt full-upgrade -y
```

### set up docker-compose.yml

### install image

```docker
    docker-compose up -d  #general method
    docker run -it --rm -d -p 8080:80 --name web nginx  $install nginx
```

### delete image

```docker
    docker image ls  //list image
    docker rmi <image_name_or_id>
    docker stop <container_name_or_id>
    docker rm <container_name_or_id>
```

In case of unable to delete image because a container of this image is being used. Execute:

```docker
    docker ps -a --filter ancestor=<image_name_or_id>
```

### run a container
```docker
    docker start my-nginx-container
```

### enter into a container

```docker
    docker exec -it [CONTAINER_ID_OR_NAME] /bin/bash
```
