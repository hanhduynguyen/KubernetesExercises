#Create base64 encoded username
echo admin | base64
YWRtaW4K

#Create base64 encoded password
echo Pa33w0rd123 | base64
UGEzM3cwcmQxMjMK

#Create a generic secret from YAML file
kubectl create -f my-secret.yml

#Create the POD
kubectl create -f secret-env-pod.yml

#Access the Secret in the POD
kubectl exec -it secret-env-pod /bin/sh

env-pod

#Clean up
kubectl delete -f my-secret.yml -f secret-env-pod.yml