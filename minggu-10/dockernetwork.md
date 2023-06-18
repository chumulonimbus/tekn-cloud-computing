### Section #1 - Networking Basics
#### Step 1: The Docker Network Command
![01](image/img1.png)
#### Step 2: List networks
![02](image/img2.png)
#### Step 3: Inspect a network
![03](image/img3.png)
#### Step 4: List network driver plugins
![04](image/img4.png)

### Section #2 - Bridge Networking
#### Step 1: The Basics
1. Every clean installation of Docker comes with a pre-built network called bridge. Verify this with the docker network ls.
![05](image/img5.png)
2. Install the brctl command and use it to list the Linux bridges
![06](image/img6.png)
3. Then, list the bridges on your Docker host
![07](image/img7.png)
4. You can also use the ip a command to view details
![08](image/img8.png)

#### Step 2: Connect a container
1. Create a new container
![09](image/img9.png)
2. Verify our example container is up
![10](image/img10.png)
3. Run the brctl show
![11](image/img11.png)
4. Inspect the bridge network
![12](image/img12.png)

#### Step 3: Test network connectivity
1. Ping the IP address of the container from the shell prompt of your Docker host
![13](image/img13.png)
2. Run docker ps to get ID container
![14](image/img14.png)
3. Run a shell inside that ubuntu container, by running docker exec -it CONTAINER_ID /bin/bash.
![15](image/img15.png)
4. Run apt-get update && apt-get install -y iputils-ping
![16](image/img16.png)
5. Ping www.github.com
![17](image/img17.png)
6. Disconnect our shell from the container
![18](image/img18.png)
7. Stop this container so we clean things up from this test, by running docker stop CONTAINER_ID.
![19](image/img19.png)

#### Step 4: Configure NAT for external connectivity
1. Start a new container based off the official NGINX image
![20](image/img20.png)
2. Review the container status and port mappings
![21](image/img21.png)
3. Connect from your Docker host
![22](image/img22.png)

### Task 3: Modify a running website
#### Step 1: The Basics
#### Step 2: Create an overlay network
#### Step 3: Create a service
#### Step 4: Test the network
#### Step 5: Test service discovery

### Cleaning Up
