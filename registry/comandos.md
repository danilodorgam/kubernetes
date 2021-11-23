#criando um registry apontando para arquivo
```bash
kubectl create secret generic hubprivado \
--from-file=.dockerconfigjson="C:\Users\dhdorgam\.docker\config.json" \
--type=kubernetes.io/dockerconfigjson
```
#criando um registry inline
```bash
USER=""
SENHA=""
EMAIL=""
kubectl create secret docker-registry hubprivado --docker-server=https://index.docker.io/v1/ --docker-username=$USER --docker-password=$SENHA --docker-email=$EMAIL
```
#formas de visualizar a secret 
```bash
kubectl get secret hubprivado --output=yaml
kubectl get secret hubprivado --output="jsonpath={.data.\.dockerconfigjson}" | base64 --decode
```