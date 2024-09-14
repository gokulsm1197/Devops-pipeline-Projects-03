# Project Title

Local Development and CI/CD Pipeline with GitHub, Git Actions, Helm, ArgoCD, and NGINX Ingress
## Description:

This project outlines the local development and deployment workflow for an application using a modern DevOps pipeline. The application is developed locally and containerized with Docker, then pushed to DockerHub. GitHub is used for source control and versioning, while GitHub Actions automate the CI/CD pipeline, handling tasks such as building Docker images, running tests, and deploying the application. Helm is utilized for Kubernetes resource management, while ArgoCD provides continuous delivery and Git-style automated deployment to the Kubernetes cluster. Traffic routing is handled using NGINX Ingress, and the system includes a jump server for secure remote access to infrastructure.

## Tools and Technologies Used
- GitHub
- GitHub Actions
- Docker
- DockerHub
- Amazon Elastic Kubernetes Service
- Helm
- ArgoCD
- Jump Server (Bastion Host)
- NGINX Ingress

## Pipeline Flow Diagram
![P04](https://github.com/user-attachments/assets/19b28db1-7aa1-4264-9d8a-6f43ee788417)





## Components and Tools Used
## Local Development:
The application is developed and tested locally, ensuring that it functions correctly before deployment to the cloud.
**Docker** is used for containerizing the application, ensuring that it runs consistently in different environments.

## Source Control and CI with GitHub and GitHub Actions:
**GitHub** is used for source code management and collaboration, with branches and pull requests controlling changes.

**GitHub** Actions automates the CI/CD pipeline. This includes:
- **Building the Docker image** for the application.
- **Running automated tests** to ensure application quality.
- **Pushing the Docker image** to DockerHub for deployment.
## Containerization with Docker and DockerHub:
The application is containerized using **Docker**, allowing it to run in isolated environments.

Docker images are pushed to **DockerHub**, a public/private registry used to store and distribute Docker images.

## Kubernetes Resource Management with Helm:
**Helm** is used to manage Kubernetes resources, providing templated configurations for deploying and managing the application in Kubernetes.

Helm charts are used to define deployments, services, config maps, secrets, and other Kubernetes resources, making it easier to manage multiple environments (e.g., dev, staging, production).

## Continuous Delivery with ArgoCD:
**ArgoCD** is a GitOps-based continuous delivery tool that automates application deployment to the Kubernetes cluster.

ArgoCD tracks changes in GitHub repositories and synchronizes them with the cluster, ensuring that the application state in Kubernetes matches the desired state defined in the Git repository.

Rollbacks and rollouts are simplified using ArgoCD's version control and rollback features.

## Secure Remote Access with Jump Server:
A **Jump Server** (or Bastion host) is used to provide secure access to the infrastructure and Kubernetes cluster. It allows administrators to access the system through a controlled entry point, protecting the environment from unauthorized access.

## Traffic Routing and Load Balancing with NGINX Ingress:
**NGINX Ingress** is used to manage external traffic into the Kubernetes cluster. It routes requests based on domain names and paths, distributing traffic across the appropriate services.

This allows multiple services to be exposed through a single external IP address, enabling better traffic management and security.


## Application Deployment Workflow:
The developer works on the application locally and tests it in a local environment.


Once ready, the changes are pushed to the GitHub repository.


GitHub Actions trigger the CI/CD pipeline, building the Docker image, running tests, and pushing the image to DockerHub.


ArgoCD automatically deploys the updated application to the Kubernetes cluster, using Helm charts for resource management.


The application is exposed externally via NGINX Ingress, allowing users to access it through a web interface.

# Project Workflow
## Local Development:
Develop the application locally in a Docker container to ensure consistency across environments.

## GitHub Source Control:
The application source code is committed to GitHub, with pull requests and branches controlling the release process.

## CI Pipeline with GitHub Actions:
GitHub Actions automate the build and test process, including building Docker images and pushing them to DockerHub.

## Application Deployment:
**Helm** and **ArgoCD** are used to deploy and manage the application in a Kubernetes cluster, ensuring a GitOps-based workflow where GitHub is the source of truth for the application's state.

## Service Exposure:
The application is exposed using **NGINX Ingress**, which manages HTTP/HTTPS traffic and routes requests to the appropriate services.

## Secure Access:
A **Jump Server** is used to provide secure access to the Kubernetes cluster and infrastructure for administrators.


## Clone Git Repository and Run Locally
![Screenshot (206)](https://github.com/user-attachments/assets/655637bb-f0e6-4cab-8ab4-ca95a625cad3)
![Screenshot (205)](https://github.com/user-attachments/assets/15b274c5-6d49-4de7-890a-69acd4492abb)

## Dockerfile Creation
![Screenshot (207)](https://github.com/user-attachments/assets/417f6025-279f-4cd3-a808-3418f57abab8)
![Screenshot (208)](https://github.com/user-attachments/assets/891cb7fb-a0db-4548-bf59-6d39fe430b3d)

## push docker registry
![Screenshot (212)](https://github.com/user-attachments/assets/70ce59c9-777a-4271-93d2-48153732fafd)
![Screenshot (227)](https://github.com/user-attachments/assets/ebe52ebd-7dd0-46f2-85f2-a904ae9380cd)


## Deployment File Services File and Ingress File Creation
![Screenshot (214)](https://github.com/user-attachments/assets/fb0616ea-2622-431b-b6f3-3aa72fa59fe7)
![Screenshot (215)](https://github.com/user-attachments/assets/cbf4a7d4-a298-4642-9b7a-de5a03148184)
![Screenshot (216)](https://github.com/user-attachments/assets/e15939b6-83c5-4492-ac99-ed7c1e59d020)


## AWS Config and EKSCTL Integration
![Screenshot (223)](https://github.com/user-attachments/assets/239a20cb-ad42-41a0-b728-8596a8ccee78)


## Elastic Kubernetes Service Creation
![Screenshot (225)](https://github.com/user-attachments/assets/9bdf3e4e-979c-49fa-ae49-6338d360f0f2)
![Screenshot (224)](https://github.com/user-attachments/assets/12abf1e8-f670-4048-9467-f895436fc520)
![Screenshot (226)](https://github.com/user-attachments/assets/ef20f58d-6dd2-454b-8a82-ff0566a5bea3)

## Helm Charts Creation
![Screenshot (244)](https://github.com/user-attachments/assets/453f506a-062f-4640-a671-b1611f79f2b8)
![Screenshot (245)](https://github.com/user-attachments/assets/cea12d45-59f3-44be-8dca-ddba03448bd3)
![Screenshot (249)](https://github.com/user-attachments/assets/9ce9c609-ad7a-4e2d-97ae-a99d5e22c95b)


## Github Push Files to Repository
![Screenshot (252)](https://github.com/user-attachments/assets/1cbb190a-0aaa-423f-b367-251f4515806e)
![Screenshot (254)](https://github.com/user-attachments/assets/f5e59c41-01ea-427a-bf2d-dd275c2eeead)

## GitHub Actions Setup and Output
![Screenshot (258)](https://github.com/user-attachments/assets/3faa658f-352f-42c1-9f38-1324af658cf1)
**Pipeline Script** 
![Screenshot (257)](https://github.com/user-attachments/assets/d3e5459c-4ff0-4e18-aa37-57bfdd7f1d9a)
![Screenshot (262)](https://github.com/user-attachments/assets/d0733bad-50ee-4b6b-afb6-61b2a229a982)
![Screenshot (259)](https://github.com/user-attachments/assets/48a4a6e8-ae72-4bfb-92ec-5af073c50580)
![Screenshot (261)](https://github.com/user-attachments/assets/90a39759-8b10-4915-952e-07efaa0a3f32)

## DockerHub Output
![Screenshot (264)](https://github.com/user-attachments/assets/fad20c6c-392d-45c3-b484-8de9ca9cabfa)

## Helm Output
![Screenshot (266)](https://github.com/user-attachments/assets/89df87c0-5736-4873-9a54-e984fc58a6b1)
![Screenshot (267)](https://github.com/user-attachments/assets/42af4963-a0c7-43d6-8b6b-762632742860)

## ArgoCD Creation
![Screenshot (269)](https://github.com/user-attachments/assets/6e13bb42-c36b-4d90-a7a4-ad52a529b53b)
![Screenshot (268)](https://github.com/user-attachments/assets/acd7e133-7048-4a64-aa2b-50b9a4ee490c)
![Screenshot (270)](https://github.com/user-attachments/assets/1943b179-5077-4e0c-9b58-2ef241244e5c)

## ArgoCD Setup and Output
![Screenshot (272)](https://github.com/user-attachments/assets/50841adc-4c2b-48cc-ad04-83be92ca28ca)
![Screenshot (275)](https://github.com/user-attachments/assets/651dd854-4685-4d94-b7fe-23c00c9a4431)
![Screenshot (276)](https://github.com/user-attachments/assets/f7a974c5-c655-48fb-a787-a4ba45739faa)

## Nginx Ingress Controller Configuration and Creation
![Screenshot (236)](https://github.com/user-attachments/assets/a388fc40-6714-4c54-a28d-6843ab3eae1a)
![Screenshot (237)](https://github.com/user-attachments/assets/2821eb3b-c17f-4573-9c8f-668771ca5d36)
![Screenshot (228)](https://github.com/user-attachments/assets/1543d559-37fc-4908-86a1-1d998e24adcf)
![Screenshot (241)](https://github.com/user-attachments/assets/bf903207-35ed-479d-aeac-64e79f51c952)


## Pipeline Workflow Output
![Screenshot (289)](https://github.com/user-attachments/assets/f483d0e3-ba8f-4c76-8aac-dc9204dc9748)
![Screenshot (290)](https://github.com/user-attachments/assets/a7191f08-010f-4250-8092-a7d67d08f4f6)
![Screenshot (291)](https://github.com/user-attachments/assets/b43a5586-2a9e-4b4b-be02-4b9e20f11d12)
![Screenshot (292)](https://github.com/user-attachments/assets/2c437b0f-29ed-4c12-a84c-72a23ce3fc0b)
![Screenshot (293)](https://github.com/user-attachments/assets/2e298d66-011b-4a11-ba33-97c27d478abe)
![Screenshot (294)](https://github.com/user-attachments/assets/bd628010-6ab7-4a51-8746-ab5b45b529f6)

## Application Access User Output
![Screenshot (277)](https://github.com/user-attachments/assets/8bc162e0-9802-449e-9d31-df5e9e56718d)
![Screenshot (278)](https://github.com/user-attachments/assets/ae5d94ce-39c3-41bb-83e0-317f0e08baec)

## Monitoring 
![Screenshot (288)](https://github.com/user-attachments/assets/c9a8a6cc-4118-4138-9b90-6d178f652517)


**This project demonstrates a complete DevOps pipeline that integrates local development with CI/CD automation, Kubernetes resource management, and secure infrastructure access. By using GitHub, GitHub Actions, Docker, DockerHub, Helm, and ArgoCD, the project ensures continuous delivery and reliable application deployment. NGINX Ingress enables efficient traffic routing, and the jump server enhances security by controlling access to the infrastructure.**


# **Thank you.......**
