# kubernetes

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

