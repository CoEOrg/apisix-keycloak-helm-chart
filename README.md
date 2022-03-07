# apisix-keycloak-helm-chart
This is helm chart to deploye APISIX + Keycloak case study project on kubernetes. 

1) Install helm
2) Add helm repo to your local repositories: helm repo add producer-service-repo https://coeorg.github.io/apisix-keycloak-helm-chart/
3) helm install producer-service 
* apisix gateway
* keycloak identity provider
* mysql for keycloak
* consumer third party service
* producer service
* mongo db & express for producer service

