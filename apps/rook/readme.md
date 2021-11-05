$ git clone --single-branch --branch release-1.7 https://github.com/rook/rook.git
cd rook/cluster/examples/kubernetes/ceph
kubectl apply -f crds.yaml -f common.yaml -f operator.yaml
kubectl apply -f cluster.yaml
kubectl apply -f storageclass.yaml

https://platform9.com/learn/v1.0/tutorials/rook-using-ceph-csi
Cluster must be test if have <3 nodos