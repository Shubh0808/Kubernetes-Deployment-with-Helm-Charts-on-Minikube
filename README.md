# Kubernetes Microservice Deployment with Helm

## Introduction

This project demonstrates how to deploy a microservice using **Minikube**, **Helm**, and **Kubernetes** on a local machine. The microservice is Dockerized and deployed to a Minikube Kubernetes cluster using Helm charts.

---

## Prerequisites

Before you begin, ensure you have the following installed:

- **Minikube**: A local Kubernetes cluster.
- **Helm**: A package manager for Kubernetes.
- **Docker**: For building the Docker image of the microservice.

You can follow these official guides to install the required tools:

- [Install Minikube](https://minikube.sigs.k8s.io/docs/)
- [Install Helm](https://helm.sh/docs/intro/install/)
- [Install Docker](https://docs.docker.com/get-docker/)

---

## Step 1: Install Minikube

1. **Install Minikube**: Use `brew install minikube` (for macOS) or the appropriate installation command for your system.
2. **Start Minikube**: Run `minikube start` to initialize the local Kubernetes cluster.
3. **Verify Minikube**: Run `kubectl cluster-info` to confirm the cluster is running.

---

## Step 2: Install Helm

1. **Install Helm**: Use `brew install helm` (for macOS) or follow the installation instructions for your system.
2. **Initialize Helm**: Run `helm repo update` to configure Helm with the official charts repository.
3. **Verify Helm**: Run `helm version` to check the Helm installation.

---

## Step 3: Dockerize the Microservice

1. **Build the Docker image**: Create a Dockerfile and run:
   ```bash
   docker build -t microservice-app:v1 .
