$ kubectl create -f deploy/kubernetes/psp.yaml # or if openshift: oc create -f deploy/kubernetes/scc.yaml\
# Set the subject of the RBAC objects to the current namespace where the provisioner is being deployed
$ NAMESPACE=`kubectl config get-contexts | grep '^*' | tr -s ' ' | cut -d' ' -f5`
$ sed -i'' "s/namespace:.*/namespace: $NAMESPACE/g" ./deploy/kubernetes/rbac.yaml
$ kubectl create -f deploy/kubernetes/rbac.yaml
$ kubectl create -f deploy/kubernetes/deployment.yaml
kubectl create -f deploy/kubernetes/class.yaml