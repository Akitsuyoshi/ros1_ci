# ros1_ci

This repository demonstrates a complete CI pipeline for a ROS1 package using Docker and Jenkins.

The project provides:

- Dockerized ROS Noetic environment
- ROS1 Waypoints Action Server tests on gazebo simulation
- Jenkins CI pipeline

## Prerequisite

Install docker:

```bash
sudo apt-get update
sudo apt-get install -y docker.io docker-compose

sudo usermod -aG docker $USER
newgrp docker

sudo service docker start
```

Check if docker is running:

```bash
docker images
```


## Quick Start

Start Jenkins:

```bash
cd ~/simulation_ws/src/ros1_ci
bash run_jenkins.sh
```

Please open the new tab on broweser with the given Jenkins URL in `jenkins__pid__url.txt`.

Once Jenkins is running, trigger the **Task1 ROS1 Test** pipeline after Pull Request is merged into the `main` branch.