# **LOCALMENTE:** Instalar nginx-ingress

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.45.0/deploy/static/provider/cloud/deploy.yaml

# Verificar instalacion (por defecto es namespace ingress-nginx)

## El pod ingress-nginx-controller-6f5454cbfb-lc2fn debe estar corriendo (Running...)
kubectl -n ingress-nginx get pods

## El deploy ingress-nginx-controller debe estar Ready 1/1
kubectl -n ingress-nginx get deploy

## El service ingress-nginx-controller de Tipo LoadBalancer debe tener un EXTERNAL-IP --> localhost
kubectl -n ingress-nginx get services

# Instalar Cert Manager
kubectl apply --validate=false -f https://github.com/jetstack/cert-manager/releases/download/v1.3.1/cert-manager.yaml


### Referencias

https://stackoverflow.com/questions/49845021/getting-an-kubernetes-ingress-endpoint-ip-address
https://youtu.be/ZKrC261Rxqo



