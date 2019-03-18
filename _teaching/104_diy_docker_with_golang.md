---
title: "goDocker: a DIY Docker from scratch using Golang"
collection: teaching
type: "Golang, Docker, Linux"
permalink: /project/diy_docker_with_golang
date: 2019-3-13
---

<span style="color: #666666; font-size: 0.8em;">A homemade Docker</span>

[Link to GitHub](https://github.com/ZzzGin/godocker)

- Used Git to track the development process
  - Created branches to isolate the development process from master brach
  - .gitignore to ignore executive from being tracked
  - push to remote Git server (Github)

- Created subsystem containers, isolated from the host system with the help of Linux system call
  - Namespace to isolate Linux kernel resources like PID, User ID, Network etc. 
  - Cgroups to manage the hardware usages of each container
  - AUFS to create a stack-like file system for Docker image stacks

- Implemented the main features of a real Docker
  - run: initiate a container from an image
    - -ti: create a contianer in interative mode
    - -d: detached mode
    - -m, —cpuShare, —cpuSet: limit the memory, CPU usages, CPU Set
    - -v: Shared volume
    - -name: set the conatiner's name
  - ps: list the running, stopped containers
  - log: view the log of each containers
  - exec: reenter the container's Namespace
  - stop: stop the container
  - remove: remove an stopped container
- TODO: Virtual network devices
- TODO: Create a goDocker container for nginx 
- Handled logs by Golang library logrus