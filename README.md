# kubernetes
My k8s project
IMP Commands
=====================
-- Getting the Join key again run below from Master Node
sudo kubeadm token create --print-join-command

-- Complete information of Node
kubectl get node -o wide

-- Complete information of Pod
kubectl get pod -o wide

-- Run the Port Forward for Pod
kubectl port-forward <<Pod name>> <<localport>>:<<Pod target Port>>
e.g. kubectl port-forward nginx 8080:80
     curl http://localhost:8080

-- Creating the YAML Spec from command
kubectl run nginx --image=nginx --restart=Never --dry-run=client -o yaml > nginx-pod.yaml

-- Getting the Events or Logs from Pod 
kubectl describe pod <<Pod NAME>>

-- Getting the Logs from Pod
kubectl logs <<Pod Name>>

-- SSH to the POD and Run shell command
kubectl exec -it nginx -- bin/bash
