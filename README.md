kubectl create ns public-service

#kubectl apply -f ldap-pv.yaml
#kubectl apply -f ldap-deployment.yaml
kubectl convert -f ldap-deployment.yaml | kubectl apply -f -
kubectl apply -f ldap-secret.yaml
kubectl apply -f ldap-service.yaml
#kubectl apply -f phpldapadmin-deployment.yaml
kubectl convert -f phpldapadmin-deployment.yaml | kubectl apply -f -
kubectl apply -f phpldapadmin-service.yaml
