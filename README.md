Integrar terminal ao cluster,
Estando autenticado no gcloud, executar comando:
gcloud container clusters get-credentials {nome-cluster} --zone {nome-zona} --project {id-projeto}


Buscar evento como um tipo especifico:
kubectl get events --field-selector type=Warning

Criar cluster autopilot:
gcloud container clusters create-auto {nome-cluster} --region {region-name}

Para instalar o dnsutils:
kubectl apply -f https://raw.githubusercontent.com/kubernetes/website/main/content/en/examples/admin/dns/dnsutils.yaml

Para acessar o container do dnsutils:
kubectl exec -it dnsutils -- /bin/sh

dentro do container, executar: 
dig redis-leader.default.cluster.local


criar secret direto no cli:
kubectl create secret generic mysql --from-literal=password=senhadomysql

ESTRATEGIAS DE DEPLOY:
ROLLING UPDATE
GREEN/BLUE
CANARY
