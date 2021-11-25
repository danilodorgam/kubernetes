###formas de reduzir ou aumentar o número de replicas manualmente
```bash
  kubectl scale deployment nginx-deployment --replicas=0
  kubectl scale deployment nginx-deployment --replicas=2
```