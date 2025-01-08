# Node.js Dockerized Application

This repository contains a simple setup for running a Node.js application in a Docker container using a lightweight Alpine Linux image.

## Dockerfile Overview

The Dockerfile uses the `node:6-alpine` base image for a minimal environment and includes the following steps:

1. **Base Image**: Starts with `node:6-alpine` for a lightweight Node.js runtime.
2. **Expose Port**: Exposes port `3000` for the application.
3. **Install Dependencies**: Adds `tini` for process management.
4. **Set Working Directory**: Sets `/usr/src/app` as the working directory.
5. **Copy Project Files**: Copies `package.json` and other source files to the container.
6. **Install Dependencies**: Installs project dependencies via `npm`.
7. **Run the Application**: Uses `tini` to manage the Node.js application process.

## Requirements

- Docker installed on your system.
- A valid `package.json` file in the project directory with all necessary dependencies.

## How to Use

### Build the Docker Image

```bash
docker build -t node-app .

