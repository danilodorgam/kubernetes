#comandos sobre volumes
###criando um volume do tipo hostPath (usado para testes)
```bash
cd storage/
kubectl apply -f pv-hostpath.yml
kubectl apply -f pv-hostpath.yml
kubectl get pv pv-volume
kubectl apply -f pvc.yml
kubectl get pv pv-volume
kubectl get pvc pv-claim
kubectl apply -f pod-usar-volume.yml
kubectl get pod pod-com-volume
kubectl exec -it pod-com-volume --/bin/bash
kubectl delete -f . 
kubectl apply -f .
```

###forma alternativa para criar aplicar/deletar mais de um arquivo por vez
```bash
kubectl delete -f . 
kubectl apply -f .
```