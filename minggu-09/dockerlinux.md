### Task 1: Run some simple Docker containers
#### Run a single task in an Alpine Linux container
1. Run the following command in your Linux console.
![01](image/img1.png)
2. Docker keeps a container running as long as the process it started inside the container is still running. In this case the hostname process exits as soon as the output is written. This means the container stops. However, Docker doesn’t delete resources by default, so the container still exists in the Exited state.
List all containers.
![02](image/img2.png)

#### Run an interactive Ubuntu container
1. Run a Docker container and access its shell.
![03](image/img3.png)
2. Run the following commands in the container.
![04](image/img4.png)
![05](image/img5.png)
![06](image/img6.png)
3. Type exit to leave the shell session. This will terminate the bash process, causing the container to exit.
![07](image/img7.png)
4. For fun, let’s check the version of our host VM.
![08](image/img8.png)

#### Run a background MySQL container
1. Run a new MySQL container with the following command.
![09](image/img9.png)
2. List the running containers.
![10](image/img10.png)
3. You can check what’s happening in your containers by using a couple of built-in Docker commands: docker container logs and docker container top.
![11](image/img11.png)
Let’s look at the processes running inside the container.
![12](image/img12.png)
4. List the MySQL version using docker container exec.
![13](image/img13.png)
5. You can also use docker container exec to connect to a new shell process inside an already-running container. Executing the command below will give you an interactive shell (sh) inside your MySQL container.
![14](image/img14.png)
6. Let’s check the version number by running the same command again, only this time from within the new shell session in the container.
![15](image/img15.png)
7. Type exit to leave the interactive shell session.
![16](image/img16.png)

### Task 2: Package and run a custom app using Docker
#### Build a simple website image
1. Make sure you’re in the linux_tweet_app directory.
![17](image/img17.png)
2. Display the contents of the Dockerfile.
![18](image/img18.png)
3. Echo the value of the variable back to the terminal to ensure it was stored correctly
![19](image/img19.png)
4. Use the docker image build command to create a new Docker image using the instructions in the Dockerfile.
![20](image/img20.png)
5. Use the docker container run command to start a new container from the image you created.
![21](image/img21.png)
7. result
![22](image/hasil.png)
6. Once you’ve accessed your website, shut it down and remove it.
![23](image/img22.png)

### Task 3: Modify a running website
1. Let’s start the web app and mount the current directory into the container.
![24](image/img23.png)
2. Go to the running website and refresh the page. Notice that the site has changed.
![25](image/img24.png)
3. Copy a new index.html into the container.
![26](image/img25.png)
4. website
![27](image/img26.png)
5. Stop and rerun without bind
![28](image/img27.png)
6. Build new image
![29](image/img28.png)
7. Docker image ls
![30](image/img29.png)
8. Rerun new container
![31](image/img30.png)
9. Running 2 container
![32](image/img31.png)
10. Output
![33](image/img32.png)