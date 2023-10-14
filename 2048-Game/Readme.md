# Docker-2048

This is a simple Docker project that runs a web server with the popular game 2048. The game is based on the original version by Gabriele Cirulli.

## How to use

To use this project, you need to have Docker installed on your machine. You can download and install Docker from https://docs.docker.com/engine/install/.

To build the Docker image, run the following command in the same directory as the Dockerfile:

`docker build -t docker-2048 .`

To run the Docker container, run the following command:

`docker run -d -p 80:80 docker-2048`

You can then access the game in your browser at http://localhost:80

## How it works

The Dockerfile contains the following instructions:

- It uses the ubuntu:22.04 image as the base image.
- It updates the package list and installs nginx, zip, and curl.
- It configures nginx to run in the foreground.
- It downloads and extracts the game files from GitHub to the web root directory.
- It exposes port 80 for the web server.
- It runs nginx with the default configuration.

## License

This project is licensed under the MIT License. 