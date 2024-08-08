**Kubernetes **:
Two important properties it offer:
1) AUTOSCALING
2) AUTOHEALING

Kubernetes Architecture:

Control Plane(Master node)
1)API server : exposed the cluster to external world, Take the requester from external and decides where the pods need to go
2)Etcd : details about the cluster information
3)Scheduler: Schedule the pod in healthy worker node after API server decides where to schedule it
4)Controller: Ensure always the current state is same the desired state
5)CCM : Cloud control manager integrates with the cloud technologies running in a cloud environment.


Data Plane(Worker node)
1)Container runtime : Any container runtime, to run containers in worker node.
2)Kubeproxy : network component that provides network, ensure each pod get ipaddress and loadbalancing across all pod in a service
3)Kubectl : agents that run on each worker node, responsible for managing the resources, watches the API server for tasks, get the instruction from master and report back to master

Pod:
1)Pods is wrapper of a container runs in worker node
2)Two same instance of container can't run in a single pod. 

1)To get the list of pod
kubectl get pods 
2)To get the list of all pods
kubectl get pods -a
3)To get more information about pod 
kubectl get pods -o wide
4)To create a namespace and set that namespace as current
kubectl create namespace [namespace_name]
kubectl config set-context --current --namespace=demo
5)
