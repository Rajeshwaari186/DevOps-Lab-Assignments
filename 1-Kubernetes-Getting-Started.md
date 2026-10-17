Exercise 1: Kubernetes Getting Started

Objective

Deploy an Nginx web server using Kubernetes and verify that the application is running successfully.

Tools Used

- Docker Desktop
- Minikube
- Kubernetes
- kubectl
- Nginx

Procedure

1. Started Docker Desktop.
2. Started the Minikube cluster using "minikube start --driver=docker".
3. Verified the cluster using "minikube status".
4. Checked the Kubernetes node using "kubectl get nodes".
5. Created the Nginx deployment using "kubectl create deployment hello-nginx --image=nginx".
6. Verified the deployment using "kubectl get deployments".
7. Checked the pod status using "kubectl get pods".
8. Forwarded port 8080 on the local machine to port 80 in the deployment using "kubectl port-forward deployment/hello-nginx 8080:80".
9. Opened "http://localhost:8080" in a browser.

Result

The Kubernetes node was Ready, the Nginx deployment was available, and the pod was Running. The Nginx welcome page was displayed successfully at "http://localhost:8080".

Evidence

Screenshots of the Kubernetes node, deployment, pod status, and Nginx welcome page are available.<img width="2560" height="1600" alt="Screenshot 2026-10-17 200447" src="https://github.com/user-attachments/assets/1f934565-348d-4750-b8cc-0e62cb58eea8" />
<img width="1542" height="1108" alt="Screenshot 2026-10-17 200357" src="https://github.com/user-attachments/assets/afdd3948-5036-4119-9ffe-a90349c08554" />
