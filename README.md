<h1>Deploying an Application with Jenkins, build via docker, host on Amazon ECR and Deploy to Amazon ECS</h1>

<h2>Map</h2>

![AA](https://user-images.githubusercontent.com/52894481/188258087-2e022938-c518-4177-8939-41ff5cacd1b4.JPG)

# STEPS

Step 1: Install Docker on Jenkins Server
- Use Jenkins Documentation (https://docs.docker.com/engine/install/ubuntu/)
![B](https://user-images.githubusercontent.com/52894481/188257750-6aa85bfa-ac57-44cc-9fc6-6b7fe425a714.JPG)

Step 2: Add Jenkins user to Docker
Command: usermod -a -G docker jenkins

Step 3: Install AWS CLI
Command: sudo apt install awscli

Step 4: Reboot Service to apply changes

Step 5: Create IAM User on AWS
![C](https://user-images.githubusercontent.com/52894481/188257761-b073fabe-6074-4303-952c-be149e29d711.JPG)

Grant the User the following permissions
- Amazon EC2 Container Registry Full Access
- Amazon ECS Full Access

Step 6: Create a Repository "vprofileimg" on Amazon Elastic Container Registry
![D](https://user-images.githubusercontent.com/52894481/188257783-bd52f44a-ce3b-4a71-bc3d-6ac1c25c016d.JPG)

Step 7: Create ECS Cluster "vprofile"
![i](https://user-images.githubusercontent.com/52894481/188257933-2111cee6-a965-49f9-8e2f-ca82aaf4be40.JPG)

![j](https://user-images.githubusercontent.com/52894481/188257940-a2bc7479-6132-4f17-8029-7034f2ba6b73.JPG)

Step 8: Install required plug ins on Jenkins
![E](https://user-images.githubusercontent.com/52894481/188257837-778c165c-538e-4cb5-9a14-ca5810a6d516.JPG)

![l](https://user-images.githubusercontent.com/52894481/188257901-5a6bf960-98f2-4e62-9a64-a65c88f7aa42.JPG)

Step 89: Add Credentials on Jenkins (Use the IAM User Credentials)
![F](https://user-images.githubusercontent.com/52894481/188257862-020d3c87-037a-4137-9e71-fdd5bf64752b.JPG)

Step 9: Create pipeline with script attached.

Step 10: Build pipeline
![m](https://user-images.githubusercontent.com/52894481/188257975-10bc6fe2-7117-4723-9e39-1df26382ac6b.JPG)

Step 11: Launch site via AWS
![k](https://user-images.githubusercontent.com/52894481/188257984-aff5a04e-b352-4f47-805a-b550e342f1ea.JPG)

Step 12: View Tasks on AWS
![n](https://user-images.githubusercontent.com/52894481/188257995-29616ede-bbea-45fc-8821-b5b95f8206ee.JPG)
