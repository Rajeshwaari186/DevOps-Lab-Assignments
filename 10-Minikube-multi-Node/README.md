Exercise 10: Multi-Node Kubernetes Cluster with Multiple Applications and ReplicaSets

Objective

Create a multi-node Kubernetes cluster using Minikube and deploy multiple applications with ReplicaSets to understand container orchestration, scaling, and high availability.

Introduction

Kubernetes is an open-source container orchestration platform used to deploy, manage, and scale containerized applications. Minikube allows developers to run a Kubernetes cluster locally for learning and testing.

In this exercise, two applications are deployed:

- Product Catalog (AppA): Provides information about available products.
- Shopping Cart (AppB): Manages users' shopping carts.

ReplicaSets maintain the desired number of running Pod replicas for each application.

Tools and Technologies

- Kubernetes
- Minikube
- kubectl
- Docker
- YAML configuration files

Architecture

The Kubernetes cluster contains multiple nodes and runs two applications. Each application is managed by a ReplicaSet that maintains the desired number of Pods.

- AppA – Product Catalog: 2 replicas
- AppB – Shopping Cart: 3 replicas

Implementation Steps

Step 1: Start Minikube

Start the local Kubernetes cluster using Minikube.

minikube start

Check the cluster status:

minikube status
kubectl get nodes

Step 2: Create Application Deployment Manifests

Create YAML configuration files for the Product Catalog and Shopping Cart applications.

Define the required container image, labels, selectors, and replica count for each application.

Step 3: Deploy the Applications

Apply the Kubernetes configuration files:

kubectl apply -f appA.yaml
kubectl apply -f appB.yaml

Step 4: Verify ReplicaSets

Check the ReplicaSets:

kubectl get replicasets

Check the running Pods:

kubectl get pods -o wide

Step 5: Verify Deployments

Check the deployment resources:

kubectl get deployments
kubectl get all

Step 6: Test Scaling

Scale an application by changing the replica count or using a scaling command.

For example:

kubectl scale deployment appa --replicas=3

Verify the updated number of Pods:

kubectl get pods

Note: The scaling command assumes the Deployment is named "appa". Use the actual resource name defined in your YAML files. If the exercise uses standalone ReplicaSets, update the ReplicaSet manifest instead.

Important Kubernetes Concepts

Pods

Pods are the smallest deployable units in Kubernetes and contain one or more containers.

ReplicaSets

ReplicaSets ensure that the specified number of Pod replicas are running at any given time.

Multi-Node Cluster

A multi-node cluster distributes workloads across multiple Kubernetes nodes, subject to scheduling constraints and available resources.

Scaling

Scaling increases or decreases the number of application replicas according to workload requirements.

Screenshots

Add screenshots showing:

1. Minikube cluster status.
2. Kubernetes nodes using "kubectl get nodes".
3. Application ReplicaSets using "kubectl get replicasets".
4. Running Pods using "kubectl get pods -o wide".
5. Deployment and scaling results.

Expected Outcome

- Create and inspect a local Kubernetes cluster.
- Deploy multiple applications.
- Configure ReplicaSets and manage Pod replicas.
- Verify application resources using kubectl.
- Understand basic scaling and availability concepts.

Conclusion

This exercise demonstrates Kubernetes cluster management using Minikube and kubectl. Deploying multiple applications and managing their replicas provides practical experience with container orchestration, scaling, and maintaining the desired application state.

References

- Kubernetes: https://kubernetes.io/
- Minikube: https://minikube.sigs.k8s.io/docs/
- kubectl Documentation: https://kubernetes.io/docs/reference/kubectl/

Technologies Used

Kubernetes | Minikube | kubectl | Docker | YAML
