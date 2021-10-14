Run this
`kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')BASH`
Follow this steps
(Link)[https://jhooq.com/setting-up-kubernetes-dashboard/#kubernetes-dashboard-local-cluster]