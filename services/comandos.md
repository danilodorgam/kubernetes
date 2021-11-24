#Pod com Service

###criar um deployment do nginx
```bash
 kubectl create deployment nginx --image=nginx
```
#visualiar metadatas de um deployment
```bash
kubectl get deploy nginx -o jsonpath='{.metadata.labels}'
```