# **LOCALMENTE:** Instalar nginx-ingress

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.45.0/deploy/static/provider/cloud/deploy.yaml

# Verificar instalacion (por defecto es namespace ingress-nginx)

## El pod ingress-nginx-controller-6f5454cbfb-lc2fn debe estar corriendo (Running...)
kubectl -n ingress-nginx get pods

## El deploy ingress-nginx-controller debe estar Ready 1/1
kubectl -n ingress-nginx get deploy

## El service ingress-nginx-controller de Tipo LoadBalancer debe tener un EXTERNAL-IP --> localhost
kubectl -n ingress-nginx get services



