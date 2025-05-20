# Deploy-App-from-Private-Docker-Registry

## **Project Overview**
This project demonstrates deploying an application from a private docker repository and deploying it on a kubenetes cluster.

---

## **Pre-Requisites**  
- Setup a Private Docker Repository (e.g. AWS Elastic Container Registry)

#/# **Features**
- Create secret component in Kubernetes that contains credentials for Docker registry.
- Configure your Deployment / Pod to use the parameter called imagePullSecrets.
- Firstly, set up your private docker repo on AWS (AWS ECR).
- Set up your minikube cluster.
- Login into the AWS ECR using the commands on the AWS ECR login commands.
- Logged in to AWS Container Repository | docker login and create docker config.json file
-  To see the contents of the login details.
    ```
       Run cat .docker/config.json
    ```
- To see the password. (we use this password to login into minikube)
   ```
      Run “aws ecr get login-password”
   ```
   
- Login into minikube
  ```
      ssh minikube
      docker login –username -p [paste password above] [url of the aws ecr repo]
      ls -la
  ```
  
- To see the cotent of the config.json file
  ```
     cat .docker/config.json
 ```

- To copy the config.json file to the host
- To see the cotent of the config.json file
 ```
    minikube cp minikube:/home/docker/.docker/config.json /users/USERNAME/.docker/config.json
```   

   
## **Features**
- Logged in to AWS Container Repository | docker login and create docker config.json file
  
  ![image](https://github.com/user-attachments/assets/f474cafe-9356-417a-972f-c8983c003daa)

  ![image](https://github.com/user-attachments/assets/5d939b18-b073-4114-ad0c-c7c5346d3d09)


- Created Secret component

  ![image](https://github.com/user-attachments/assets/d0dd8f55-d8ab-4a07-a0c8-71ce1e380483)

- Configured Deployment for demo app

  ![image](https://github.com/user-attachments/assets/5d162500-5432-4080-bf8d-1f3ddb3bd354)

  ![image](https://github.com/user-attachments/assets/7a793294-58b6-4519-9797-95d187dd7747)


  ![image](https://github.com/user-attachments/assets/17d2d07d-4658-44e7-936b-d8d2b06ff60c)


-
