### High-Availability-Kubernetes-cluster
Set up k8 cluster

https://kubernetes.io/docs/setup/independent/high-availability/ 

1. 3 masters ,3 workers
2. Install docker,kubelet , kubectl , kubeadm 
3. Install HA proxy on lb node (first master)
https://blog.inkubate.io/install-and-configure-a-multi-master-kubernetes-cluster-with-kubeadm/ 
4. add kubeadm-config.yaml to add configuration of lb 
5. sudo kubeadm init --config=kubeadm-config.yaml
6. copy certificates created to the other 2 masters 
7. Apply the Weave CNI plugin
8. add 2 other masters with the join command adding --experimental-control-plane flag 
9. add 3 workers 
