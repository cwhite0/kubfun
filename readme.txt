
minikube.exe docker-env
& minikube docker-env | Invoke-Expression

docker build -t my-apache2 .

 kubectl create -f .\pod.yaml
 
 kubectl expose deployment apache2 --type=NodePort


kubectl delete services apache2

kubectl delete deployment apache2

minikube service apache2 --url


---------------------\\

 kubectl --record deployment.apps/apache2 set image deployment.apps/apache2 apache2=my-apache2:1.0
 
 kubectl rollout undo deployment.v1.apps/