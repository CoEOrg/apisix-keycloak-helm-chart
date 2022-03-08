# apisix-keycloak-helm-chart
This is helm chart to deploy APISIX + Keycloak case study project on kubernetes. 

Steps to deploy:

* Install helm: https://helm.sh/docs/intro/install

Run:
* helm repo add apisix-keycloak-poc-repo https://coeorg.github.io/apisix-keycloak-helm-chart/
* helm repo update
* helm install apisix-keycloak-poc apisix-keycloak-poc-repo/producer-service ^
  
  --set apisix.gateway.type=LoadBalancer ^ 
  
  --set apisix.ingress-controller.enabled=true ^
    
  --namespace ingress-apisix ^
  
  --set ingress-controller.config.apisix.serviceName=apisix-keycloak-poc-admin

Installed services:
* apisix gateway: https://apisix.apache.org/docs/
* keycloak identity provider: https://www.keycloak.org/
* mysql database for keycloak: https://www.mysql.com/
* consumer third party service: https://github.com/CoEOrg/ConsumerService
* producer service: https://github.com/CoEOrg/ProducerService
* mongo database & mongo express for producer service: https://www.mongodb.com/ 
