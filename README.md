# SpoofDPI Proxy Server
## Overview
SpoofDPI is a specialized proxy server designed to bypass Deep Packet Inspection (DPI) mechanisms, enabling users to access restricted content. This project is packaged as a Docker container for easy deployment and use.
## Source and Binary
The SpoofDPI proxy server is based on the project SpoofDPI. The Docker image uses the source code and binary files provided by this project.
## Features
- **DPI Bypass**: Implements techniques to evade detection by DPI systems.
- **Dockerized**: Easily deployable in a Docker environment.
- **Lightweight**: Minimal resource usage while providing effective censorship circumvention.

## Port Configuration

The SpoofDPI proxy server operates exclusively through **port 5000**. Ensure that this port is open and not blocked by any firewall or network settings.

## Getting Started

### Prerequisites

- Docker installed on your system.
- Basic understanding of Docker commands.

### Pulling the Docker Image

To get started, pull the latest Docker image from the GitHub Container Registry:

For x64 architecture:
```bash
docker pull ghcr.io/unmedius/spoof-dpi:latest
```
For Arm64 architecture:
```bash
docker pull ghcr.io/unmedius/spoof-dpi-rasp:latest
```
*Note: The Arm64 version has been tested only on Raspberry Pi.*
## Running the Container
For x64 architecture, run the Docker container using the following command:
```bash
docker run -d --name spoof-dpi --network host ghcr.io/unmedius/spoof-dpi:latest
```
For Arm64 architecture, run the Docker container using the following command:
```bash
docker run -d --name spoof-dpi --network host ghcr.io/unmedius/spoof-dpi-rasp:latest
```
*Note: The Arm64 version has been tested only on Raspberry Pi.*
## Usage
To use the proxy server, configure your web browser or application to connect through the proxy at http://localhost:5000.
