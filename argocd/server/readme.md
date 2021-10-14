# Steps to install argo

## Create namespace
Run `kubectl apply -f namespace.yaml`

## Install
Run `kubectl -n argocd apply -f install.yaml`

## Cat admin password
Run `kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d`

## Apply ingress
Run `kubectl apply -f ingress.yaml`


# Steps to recreate apps if the server stops working 
## Reboot the server and wait to restart session again 
`reboot `
## Go to  `argoncd` directory
## Apply the file `apps-configuration.yaml` with 
`kubectl apply -f apps-configuration.yaml`
## Go to [argocd](https://argocd.espe.edu.ec) and Sync all the apps 
