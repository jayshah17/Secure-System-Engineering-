
Asisgnment on docker 


For the following task refer the link 1
* Create and use a Docker container interactively
* Create a Dockerfile, which allows you to declaratively define your containers
* Run detached containers and understand port forwarding
* Use docker-compose to run a multi-container web application

For the following task 1, 2, 3 refer link 3
* Task 1: Run some simple Docker containers
* Task 2: Package and run a custom app using Docker
* Task 3: Modify a Running Website

1.	https://decal.ocf.berkeley.edu/archives/2018-fall/labs/a11
2.	https://www.youtube.com/watch?v=F7We8xx1_Lw
3.	https://training.play-with-docker.com/beginner-linux/
https://github.com/dockersamples -- this  has apps for docker

# Set Up the Environment:

## Install Docker Desktop:

1. Visit the Docker Desktop for Windows download page.
2. Download the Docker Desktop installer.
3. Double-click Docker Desktop Installer.exe to run the installer.
4. Follow the installation instructions.

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/723e6f27-c27a-4695-9558-3177b1e63046)

## Verify Installation:

1. Open a command prompt (Windows PowerShell or Command Prompt).
2. Run the command: docker --version
It should show client and server both installation where client is our host os command Prompt and server is Docker Engine.

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/c012998d-c76e-44de-b3ae-634b02df6bbd)

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/5330c306-5c39-44df-b242-8f8696dfa40d)

Run the hello-world Image
docker run hello-world

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/11e9172a-80d3-4be7-b334-5abfb48816e5)

### Create and use a Docker container interactively

> docker run -it ubuntu bash

![image](https://github.com/jayshah17/Secure-System-Engineering-/assets/76842630/50344b78-e54f-40de-9d5e-1fd7e0a312fc)

