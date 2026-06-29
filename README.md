Containerized Web Application CI/CD Pipeline
A complete end-to-end DevOps project demonstrating Docker, Jenkins, Docker Hub, and Kubernetes (Minikube) to automate application build, deployment, and rolling updates.
________________________________________
Project Objective
The objective of this project is to automate the software delivery process by implementing a complete CI/CD pipeline.
The pipeline performs the following operations:
•	Clone source code from GitHub
•	Build Docker Image
•	Push Docker Image to Docker Hub
•	Deploy application to Kubernetes
•	Verify deployment
•	Perform Rolling Updates
•	Rollback to previous version if required
________________________________________
Project Architecture
Developer
    │
    ▼
GitHub Repository
    │
    ▼
Jenkins Pipeline
    │
    ▼
Docker Build
    │
    ▼
Docker Hub
    │
    ▼
Kubernetes Deployment
    │
    ▼
Kubernetes Service
    │
    ▼
Users
________________________________________
Tech Stack
Version Control
•	Git
•	GitHub
CI/CD
•	Jenkins
Containerization
•	Docker
•	Docker Hub
Orchestration
•	Kubernetes
•	Minikube
Web Server
•	Nginx
Operating System
•	Ubuntu (WSL2)
________________________________________
Project Structure
containerized-webapp-cicd
│
├── app/
│   └── index.html
│
├── docker/
│   └── Dockerfile
│
├── jenkins/
│   └── Jenkinsfile
│
├── kubernetes/
│   ├── pod.yaml
│   ├── deployment.yaml
│   └── service.yaml
│
├── screenshots/
│
└── README.md
________________________________________
CI/CD Pipeline Flow
Stage 1
Clone Repository
↓
Stage 2
Build Docker Image
↓
Stage 3
Push Docker Image to Docker Hub
↓
Stage 4
Deploy to Kubernetes
↓
Stage 5
Verify Deployment
________________________________________
Docker
Build Docker Image
docker build -t anjali1410/myapp:v1 -f docker/Dockerfile .
Run Container
docker run -d --name myapp -p 8081:80 anjali1410/myapp:v1
Verify
docker ps
________________________________________
Docker Hub
Push Image
docker push anjali1410/myapp:v1
Docker Hub Repository
anjali1410/myapp
________________________________________
Kubernetes Deployment
Start Minikube
minikube start
________________________________________
Deploy Pod
kubectl apply -f kubernetes/pod.yaml
________________________________________
Deploy Deployment
kubectl apply -f kubernetes/deployment.yaml
________________________________________
Deploy Service
kubectl apply -f kubernetes/service.yaml
________________________________________
Verify
kubectl get pods

kubectl get deployment

kubectl get svc
________________________________________
Rolling Update
Update Deployment
kubectl set image deployment/myapp-deployment \
myapp-container=anjali1410/myapp:v2
Verify
kubectl rollout status deployment/myapp-deployment
________________________________________
Rollback
kubectl rollout undo deployment/myapp-deployment
Verify
kubectl rollout history deployment/myapp-deployment
________________________________________
Jenkins Pipeline
The Jenkins Pipeline performs the following tasks automatically:
•	Clone Repository
•	Build Docker Image
•	Login to Docker Hub
•	Push Docker Image
•	Deploy to Kubernetes
•	Verify Deployment
________________________________________
Screenshots
Add screenshots for:
•	Docker Images
•	Docker Containers
•	Docker Volumes
•	Docker Networks
•	Jenkins Dashboard
•	Jenkins Pipeline
•	Docker Hub Repository
•	Kubernetes Pods
•	Kubernetes Deployment
•	Kubernetes Services
•	Rolling Update
•	Rollback
________________________________________
Kubernetes Resources
This project includes:
•	Pod
•	Deployment
•	Service (NodePort)
________________________________________
Verification Commands
Docker
docker images

docker ps
Kubernetes
kubectl get nodes

kubectl get pods

kubectl get deployment

kubectl get svc
________________________________________
Features
•	Dockerized Web Application
•	Jenkins Pipeline
•	Docker Hub Integration
•	Kubernetes Deployment
•	Rolling Updates
•	Rollback Support
•	NodePort Service
•	Zero Downtime Deployment
•	CI/CD Automation
________________________________________
Learning Outcomes
After completing this project, I gained hands-on experience with:
•	Docker Image Creation
•	Docker Containers
•	Docker Volumes
•	Docker Networking
•	Jenkins Freestyle Jobs
•	Jenkins Pipeline
•	Git Integration
•	Docker Hub
•	Kubernetes Pods
•	Deployments
•	Services
•	Rolling Updates
•	Rollbacks
•	CI/CD Automation
•	Troubleshooting Real-world Deployment Issues
________________________________________
Author
Anjali Somwanshi
GitHub:
https://github.com/anjalithakur9414
LinkedIn:
https://www.linkedin.com/in/anjali-somwanshi-7a7102154/

