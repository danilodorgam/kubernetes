###setando o HPA
```bash
  kubectl autoscale deployment php-apache --cpu-percent=50 --min=1 --max=10
  ```
###gerador de carga para ativar o gatilho do HPA
```bash
kubectl run -i --tty load-generator --rm --image=busybox --restart=Never -- bin/sh -c "while sleep 0.01; do wget -q -O- http://php-apache; done"
```
###validando HPA
```bash
  kubectl get hpa
  kubectl get deployment php-apache
```