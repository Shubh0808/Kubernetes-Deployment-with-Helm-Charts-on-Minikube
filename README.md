Kubernetes Deployment with Helm Charts on Minikube
A complete guide and implementation for deploying a containerized microservice on a local Kubernetes cluster using Helm charts and Minikube.

📌 Project Description
This project demonstrates the deployment of a Node.js microservice using Kubernetes and Helm. It leverages Minikube for local cluster setup, Docker for containerization, and Helm charts for efficient deployment and management of Kubernetes resources. It covers installation, service exposure, scaling, and version upgrades of the microservice.

🚀 Features
Local Kubernetes cluster setup using Minikube

Docker-based microservice containerization

Helm chart for Kubernetes deployment and management

Exposing services via Minikube

Deployment scaling using kubectl and Helm

Version upgrades through Helm chart values

Horizontal Pod Autoscaling (HPA) configuration

🧰 Technologies Used
Node.js – Microservice backend

Docker – Containerization

Kubernetes – Container orchestration

Minikube – Local Kubernetes cluster

Helm – Kubernetes package manager

🛠️ Setup Instructions
1. Prerequisites
Docker installed locally

Minikube installed and configured

Helm CLI installed

Git installed

2. Clone the Repository
bash
Copy
Edit
git clone https://github.com/Shubh0808/Kubernetes-Deployment-with-Helm-Charts-on-Minikube.git
cd Kubernetes-Deployment-with-Helm-Charts-on-Minikube
3. Start Minikube
bash
Copy
Edit
minikube start
4. Build and Load Docker Image
bash
Copy
Edit
eval $(minikube docker-env)
docker build -t microservice-app:v1 ./app
5. Install Helm Chart
bash
Copy
Edit
helm install microservice-release ./microservice-chart
6. Access the Microservice
bash
Copy
Edit
minikube service microservice-release-microservice-chart
7. Upgrade the Microservice
Update the version/tag in values.yaml and run:

bash
Copy
Edit
helm upgrade microservice-release ./microservice-chart
8. Scale the Deployment
bash
Copy
Edit
kubectl scale deployment microservice-release-microservice-chart --replicas=3
📁 Project Structure
bash
Copy
Edit
.
├── app/                      # Node.js microservice source code
├── microservice-chart/      # Helm chart (templates, values)
├── README.md
📄 License
This project is licensed under the MIT License.
