# kubernetes
Performing these activities on Dev with Minikube

## minikube start --driver=docker 

This spins up a local development environment <br>

<img width="692" alt="Screenshot 2024-07-27 at 13 26 49" src="https://github.com/user-attachments/assets/0155f326-890f-4295-aa0c-8b2b2c6aef9e"><br>

Running Minikube container on Docker Desktop

<img width="1437" alt="Screenshot 2024-07-27 at 13 32 28" src="https://github.com/user-attachments/assets/b31930fa-2bd7-421f-865e-28f1d5c2ff35"><br>

A Kubernetes pod deploys single instances of our application, and each container is encapsulated in pods and these pods are deployed using replica controllers or replica sets

A replica set in Kubernetes ensures that pods are available at all times

https://kubernetes.io/docs/concepts/services-networking/service/

# Services in Kubernetes 

In Kubernetes, a Service exposes a network application running as one or more Pods in your cluster.

Services could be NodePort, Cluster IP or Load balancing

# Create the replica set/service-deployment with the command

$ kubectl create -f replicaset.yaml

$ kubectl create -f service-deployment.yaml

# Check the set status, which should be 3 as specified in the file

$ kubectl get replicaset

# Get running pods,

$ kubectl get pods 

# Delete pods,

$ kubectl delete pod

# Get further details about running pods,

$ kubectl describe replicaset <name of replicaset>

# Create an NGINX Pod

$ kubectl run nginx --image=nginx

# Generate POD Manifest YAML file (-o yaml). Don’t create it(–dry-run)

$ kubectl run nginx --image=nginx --dry-run=client -o yaml

# Generate Deployment YAML file (-o yaml). Don’t create it(–dry-run) and save it to a file

$ kubectl create deployment --image=nginx nginx --dry-run=client -o yaml > nginx-deployment.yaml

# In k8s version 1.19+, we can specify the –replicas option to create a deployment with 6 replicas

$ kubectl create deployment --image=nginx nginx --replicas=6 --dry-run=client -o yaml > nginx-deployment.yaml

