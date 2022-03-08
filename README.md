# apisix-keycloak-helm-chart

<b>High Level Architecture Diagram: </b>

<img width="427" alt="image" src="https://user-images.githubusercontent.com/10356708/157142042-f8cb0d91-7c18-4c60-b39b-4573ccbc861b.png">

---

<b>Description:</b>

This is helm chart to deploy APISIX + Keycloak case study project on kubernetes. 

Github Repo: https://github.com/CoEOrg/apisix-keycloak-helm-chart

---

<b>Steps to deploy:</b>

* Install helm: https://helm.sh/docs/intro/install

Run:
* helm repo add apisix-keycloak-poc-repo https://coeorg.github.io/apisix-keycloak-helm-chart/
* helm repo update
* helm install apisix-keycloak-poc apisix-keycloak-poc-repo/producer-service ^
  
  --set apisix.gateway.type=LoadBalancer ^ 
  
  --set apisix.ingress-controller.enabled=true ^
    
  --namespace ingress-apisix ^
  
  --set ingress-controller.config.apisix.serviceName=apisix-keycloak-poc-admin

---

<b>Deployed components:</b>

* apisix gateway: https://apisix.apache.org/docs/
* keycloak identity provider: https://www.keycloak.org/
* mysql database for keycloak: https://www.mysql.com/
* consumer third party service: https://github.com/CoEOrg/ConsumerService
* producer service: https://github.com/CoEOrg/ProducerService
* mongo database & mongo express for producer service: https://www.mongodb.com/ 
