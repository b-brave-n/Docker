# Docker

# Project 2: Uptime Kuma Deployment

This guide outlines the steps to deploy Uptime Kuma using Docker Compose, including setting up environment variables and verifying the installation.

## Prerequisites

* **Docker**: Ensure you have downloaded and installed Docker.
* **Terminal**: You will need access to a terminal application.

## Deployment Steps

### Step 1: Create Project Directory

1.  Create a new directory for the deployment:
    ```bash
    mkdir new-uptime-kuma-deployment
    ```
   

2.  Navigate into the new directory:
    ```bash
    cd new-uptime-kuma-deployment
    ```
   

### Step 2: Configure Environment Variables

1.  Create a `.env` file using a text editor (e.g., nano):
    ```bash
    nano .env
    ```
   

2.  Add the following line to define the port:
    ```ini
    KUMA_PORT=3002
    ```
    *(Note: Save the file by pressing `Control+O`, `Enter`, and exit with `Control+X`).*

### Step 3: Create Docker Compose File

1.  Create the `docker-compose.yml` file:
    ```bash
    nano docker-compose.yml
    ```
   

2.  Paste the following configuration:

    ```yaml
    version: "3.9"
    services:
      uptime-kuma:
        image: louislam/uptime-kuma:latest
        container_name: uptime-kuma-new
        ports:
          - "${KUMA_PORT}:3001"
        volumes:
          - uptime-

    ```

    <br>
    <img width="940" height="610" alt="Screenshot 2025-12-12 at 4 46 37 AM" src="https://github.com/user-attachments/assets/f947a5a1-08e0-40fa-aa22-19ac30a69aeb" />
