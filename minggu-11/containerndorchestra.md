### Stage Setup
1. Let’s get started by first cloning the demo code repository, changing the working directory, and checking the demo branch out.
![01](image/img1.png)

### Step 0: Basic Link Extractor Script
1. Checkout the step0 branch and list files in it.
![02](image/img2.png)
2. The linkextractor.py file is the interesting one here, so let’s look at its contents:
![03](image/img3.png)
3. However, this seemingly simple script might not be the easiest one to run on a machine that does not meet its requirements. The README.md file suggests how to run it, so let’s give it a try:
![04](image/img4.png)
4. When we tried to execute it as a script, we got the Permission denied error. Let’s check the current permissions on this file:
![05](image/img5.png)
5. We can either change it by running chmod a+x linkextractor.py or run it as a Python program instead of a self-executing script as illustrated below:
![06](image/img6.png)

### Step 1: Containerized Link Extractor Script
1. Checkout the step1 branch and list files in it.
![07](image/img7.png)
2. We have added one new file (i.e., Dockerfile) in this step. Let’s look into its contents:
![08](image/img8.png)
3. So far, we have just described how we want our Docker image to be like, but didn’t really build one. So let’s do just that:
![09](image/img9.png)
4. We have created a Docker image named linkextractor:step1 based on the Dockerfile illustrated above. If the build was successful, we should be able to see it in the list of image:
![10](image/img10.png)
5. Now, let’s run a one-off container with this image and extract links from some live web pages:
![11](image/img11.png)
6. Let’s try it on a web page with more links in it:
![12](image/img12.png)

### Step 2: Link Extractor Module with Full URI and Anchor Text
1. Checkout the step2 branch and list files in it.
![13](image/img13.png)
2. Let’s have a look at the updated script:
![14](image/img14.png)
3. Now, let’s build a new image and see these changes in effect:
![15](image/img15.png)
4. We have used a new tag linkextractor:step2 for this image so that we don’t overwrite the image from the step1 to illustrate that they can co-exist and containers can be run using either of these images.
![16](image/img16.png)
5. Running a one-off container using the linkextractor:step2 image should now yield an improved output:
![17](image/img17.png)
6. Running a container using the previous image linkextractor:step1 should still result in the old output:
![18](image/img18.png)

### Step 3: Link Extractor API Service
1. Checkout the step3 branch and list files in it.
![19](image/img19.png)
2. Let’s first look at the Dockerfile for changes:
![20](image/img20.png)
3. The linkextractor.py module remains unchanged in this step, so let’s look into the newly added main.py file:
![21](image/img21.png)
4. It’s time to build a new image with these changes in place:
![22](image/img22.png)
5. We are also assigning a name (--name=linkextractor) to the container to make it easier to see logs and kill or remove the container.
![23](image/img23.png)
6. If things go well, we should be able to see the container being listed in Up condition:
![24](image/img24.png)
7. We can now make an HTTP request in the form /api/<url> to talk to this server and fetch the response containing extracted links:
![25](image/img25.png)
8. Since the container is running in detached mode, so we can’t see what’s happening inside, but we can see logs using the name linkextractor we assigned to our container:
![26](image/img26.png)
9. We can see the messages logged when the server came up, and an entry of the request log when we ran the curl command. Now we can kill and remove this container:
![27](image/img27.png)

### Step 4: Link Extractor API and Web Front End Services
### Step 5: Redis Service for Caching
### Step 6: Swap Python API Service with Ruby