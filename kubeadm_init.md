kubeadm init --apiserver-advertise-address=172.31.232.61 --pod-network-cidr=192.168.16.0/20 --ignore-preflight-errors=NumCPU


kubeadm join 172.31.232.61:6443 --token gncpr8.b67n45t2cqlr1ns9 \
    --discovery-token-ca-cert-hash sha256:0eda88c05bc897d8bf4bfa0fabb180dc6efc50677b09b078c892a3aaca76da5b
