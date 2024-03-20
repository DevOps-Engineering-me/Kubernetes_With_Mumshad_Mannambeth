# Kubernetes Concepts - Pods, PeplicaSets,Deployment Coding Exercise

### Pods - 1
Introduction: Let us start simple! Given a pod-definition.yml file. We are only getting started with it. I have added two root level properties - apiVersion and kind.

Instruction: Add the missing two properties - metadata and spec

![Screenshot from 2024-03-21 01-58-28](https://github.com/DevOps-Engineering-me/React-app-Deploy-In-Docker/assets/68004638/9ede8807-f91e-497e-8fc1-84b93a603476)

### Pods - 2
Introduction: Let us now populate values for each property. Start with apiVersion. 

Instruction: Update value of apiVersion to v1. Remember to add a space between colon (:) and the value (v1)

![Screenshot from 2024-03-21 02-00-22](https://github.com/DevOps-Engineering-me/React-app-Deploy-In-Docker/assets/68004638/04e33c89-112a-485f-9989-94baf49c74a8)



### Pods - 3
Instruction: Update value of kind to Pod.

![Screenshot from 2024-03-21 02-00-22](https://github.com/DevOps-Engineering-me/React-app-Deploy-In-Docker/assets/68004638/04e33c89-112a-485f-9989-94baf49c74a8)


### Pods - 4
Introduction: Let us now get to the metadata section. 

Instruction: Add a property "name" under metadata with value "myapp-pod". Remember to add a space before 'name' to make it a child of metadata

![Screenshot from 2024-03-21 02-03-36](https://github.com/DevOps-Engineering-me/React-app-Deploy-In-Docker/assets/68004638/f73f5331-4508-4201-9c16-cc92d89d11f8)


### Pods - 5
Introduction: Let us add some labels to our Pod 

Instruction: Add a property "labels" under metadata with a child property "app" with a value "myapp". Remember to have equal number of spaces before "name" and "labels" so they are siblings

![Screenshot from 2024-03-21 02-05-24](https://github.com/DevOps-Engineering-me/React-app-Deploy-In-Docker/assets/68004638/f1bc2503-42da-43c1-ad1e-8e989cd9fd59)


### Pods - 6
Introduction: We now need to provide information regarding the docker image we plan to use. 

Instruction: Add a property containers under spec section. Do not add anything under it yet.

![Screenshot from 2024-03-21 02-06-57](https://github.com/DevOps-Engineering-me/React-app-Deploy-In-Docker/assets/68004638/155a7b6e-57f4-44c6-8ea9-c26e63940c93)


### Pods - 7
Instruction: Containers is an array/list. So create the first element/item in the array/list and add the following properties to it: name - nginx and image - nginx

![Screenshot from 2024-03-21 02-08-23](https://github.com/DevOps-Engineering-me/React-app-Deploy-In-Docker/assets/68004638/3b916ef6-162a-412f-981c-ecf1b282ce4a)

### Pods - 8
Introduction: Perfect! You have successfully created a Kubernetes-Definition file. Let us try it one more time, this time all on your own! 

Instruction: Create a Kubernetes Pod definition file using values below: 

Name: postgres 
Labels: tier => db-tier
Container name: postgres
Image: postgres

![Screenshot from 2024-03-21 02-11-55](https://github.com/DevOps-Engineering-me/React-app-Deploy-In-Docker/assets/68004638/ea31f53e-9566-4220-afca-81273ddd136a)


### Pods - 9
Introduction: Postgres Docker image requires an environment variable to be set for password.  

Instruction: Set an environment variable for the docker container. POSTGRES_PASSWORD with a value mysecretpassword. I know we haven't discussed this in the lecture, but it is easy. To pass in an environment variable add a new property 'env' to the container object. It is a sibling of image and name. env is an array/list. So add a new item under it. The item will have properties name and value. name should be the name of the environment variable - POSTGRES_PASSWORD. And value should be the password - mysecretpassword

![Screenshot from 2024-03-21 02-15-51](https://github.com/DevOps-Engineering-me/React-app-Deploy-In-Docker/assets/68004638/2404506a-d793-403e-a22c-ee193fef3177)
