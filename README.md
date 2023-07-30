# kubernetes

A Kubernetes pod deploys single instances of our application, and each container is encapsulated in pods and these pods are deployed using replica controllers or replicasets

A replica set in Kubernetes ensures that pods are available at all times

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

