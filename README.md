# master node

1. sudo su
2. install-docker.sh
3. vi /etc/containerd/config.toml <- Comment out 'disable_plugins..'
4. systemctl restart containerd
5. install-k8s-common.sh
6. install-k8s-master-only.sh

# worker node
1. sudo su
2. install-docker.sh
3. vi /etc/containerd/config.toml <- Comment out 'disable_plugins..'
4. systemctl restart containerd
5. install-k8s-common.sh
6. install-k8s-worker-only.sh <- Execute the 'kubeadm join XXXXX:6443 --token XXXXXXXX \
	--discovery-token-ca-cert-hash sha256:XXXXXXXX' command as a result of executing '4. install-k8s-master-only.sh' on the master node.

# metadata
2023-04-04 Done.