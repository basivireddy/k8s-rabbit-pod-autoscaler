Deploy Rabbitmq

https://medium.com/nerd-for-tech/deploying-rabbitmq-on-kubernetes-using-rabbitmq-cluster-operator-ef99f7a4e417

kubectl create secret generic rabbit-pod-autoscaler --from-literal=rabbit-user=guest --from-literal=rabbit-pass='guest' -n kube-system

kubectl create ns test
kubectl apply -f https://raw.githubusercontent.com/kubernetes/website/main/content/en/examples/controllers/nginx-deployment.yaml -n test

create queue:

kubectl exec production-rabbitmqcluster-server-0 -- /bin/sh -c "rabbitmqadmin -u guest -p guest declare queue name=test1"
rabbitmqadmin -u {user} -p {password} -V {vhost} declare queue name={name}

nginx pod: install curl
apt-get update && apt-get install curl

curl -X POST -d name=hi http://10.8.1.50:8080

