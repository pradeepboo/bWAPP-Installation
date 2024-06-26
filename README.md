# bWAPP Installation on Kali Linux Using Docker

Follow the steps below to install and run bWAPP on Kali Linux using Docker.

## Step 1: Install Docker

Open a terminal and run the following command to install Docker:

```bash
$ sudo apt install docker.io
```

## Step 2: Enable Docker

Enable and start the Docker service with the following command:

```bash
$ sudo systemctl enable docker --now
```

## Step 3: Check Docker Service

Verify that the Docker service is running:

```bash
$ sudo systemctl status docker
```

## Step 4: Add User to Docker Group

Add your user to the Docker group to avoid needing sudo for Docker commands:

```bash
$ sudo usermod -aG docker $USER
```

> **Note**: You need to log out and log back in for the group change to take effect.

## Step 5: Verify Docker Installation

After logging back in, check the Docker version to ensure it's installed correctly:

```bash
$ docker -v
```

## Step 6: Download bWAPP Docker Image

Pull the bWAPP Docker image from Docker Hub:

```bash
$ docker pull hackersploit/bwapp-docker
```

## Step 7: Run bWAPP Container

Run the bWAPP container with the following command:

```bash
$ docker run -d -p 80:80 hackersploit/bwapp-docker
```

## Step 8: Set Up bWAPP

Open your browser and navigate to http://127.0.0.1. If you encounter an error, try the following URL:

<http://127.0.0.1/install.php>

Click **`hear`** to install button.

## Step 9: Log In to bWAPP

Once the setup is complete, navigate to the login page:

<http://127.0.0.1/login.php>

Use the default credentials to log in:

Username: bee
Password: bug

