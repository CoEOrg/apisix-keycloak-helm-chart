# apisix-keycloak-helm-chart
This is helm chart to deploye APISIX + Keycloak case study project on kubernetes. 

Steps to deploy:

* Install helm

Run:
* helm repo add producer-service-repo https://coeorg.github.io/apisix-keycloak-helm-chart/
* helm repo update
* helm install apisix-keycloak-poc apisix-keycloak-poc-repo/producer-service ^
  --set gateway.type=LoadBalancer ^
  --set apisix.enabled=true ^
  --set ingress-controller.enabled=true ^
  --set dashboard.enabled=true ^  
  --namespace ingress-apisix ^
  --set ingress-controller.config.apisix.serviceNamespace=ingress-apisix

Installed services:
* apisix gateway
* keycloak identity provider
* mysql for keycloak
* consumer third party service
* producer service
* mongo db & express for producer service
