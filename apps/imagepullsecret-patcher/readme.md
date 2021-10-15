## How to create Gitlab Secret and configure with imagepullsecret-patcher

- Apply imagepullsecret-patcher yaml file
- Run This command this gitlab deploy token
```
kubectl -n imagepullsecret-patcher \
  create secret docker-registry image-pull-secret \
  --docker-username=lapillaga\
  --docker-password='xxxxxx' \
  --docker-email=lapillaga@espe.edu.ec \
  --docker-server=https://ghcr.io