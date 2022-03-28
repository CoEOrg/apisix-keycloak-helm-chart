# apisix-keycloak-helm-chart

<b>High Level Architecture Diagram: </b>

<img width="427" alt="image" src="https://user-images.githubusercontent.com/10356708/157142042-f8cb0d91-7c18-4c60-b39b-4573ccbc861b.png">

---

<b>Description:</b>

This is helm chart to deploy APISIX + Keycloak case study project on kubernetes. 

Github Repo: <a href="https://github.com/CoEOrg/apisix-keycloak-helm-chart">https://github.com/CoEOrg/apisix-keycloak-helm-chart</a>

---

<b>Steps to deploy:</b>

* Install helm: <a href="https://helm.sh/docs/intro/install">https://helm.sh/docs/intro/install</a>

Run:
* helm repo add apisix-keycloak-poc-repo <a href="https://coeorg.github.io/apisix-keycloak-helm-chart">https://coeorg.github.io/apisix-keycloak-helm-chart</a>
* helm repo update
* helm install apisix-consumer apisix-keycloak-poc-repo/consumer-service 
* helm install apisix apisix-keycloak-poc-repo/producer-service ^
  
  --set apisix.gateway.type=LoadBalancer ^ 
  
  --set apisix.ingress-controller.enabled=true ^  
  
  --set apisix.fullnameOverride=apisix ^
  
  --namespace ingress-apisix ^
  
  --create-namespace

---

<b>Deployed components:</b>

* apisix gateway: <a href="https://apisix.apache.org/docs/">https://apisix.apache.org/docs</a>
* keycloak identity provider: <a href="https://www.keycloak.org/">https://www.keycloak.org</a>
* mysql database for keycloak: <a href="https://www.mysql.com/">https://www.mysql.com</a>
* producer service: <a href="https://github.com/CoEOrg/ProducerService">https://github.com/CoEOrg/ProducerService</a>
* consumer service: <a href="https://github.com/CoEOrg/ConsumerService">https://github.com/CoEOrg/ConsumerService</a>
* mongo database & mongo express for producer service: <a href="https://www.mongodb.com/">https://www.mongodb.com</a>
