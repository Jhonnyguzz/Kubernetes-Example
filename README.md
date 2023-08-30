# Kubernetes example

## Wordpress and MySQL persistent volume

https://kubernetes.io/docs/tutorials/stateful-application/mysql-wordpress-persistent-volume/

## How to run in local

1. Set up a cluster (Docker Desktop, Minikube, Kubeadm, EKS, etc.) and configure the kubeConfig
2. Create a namespace

´´´
kubectl create namespace testing
´´´

3. Run the kustomization.yaml

´´´
kubectl -n testing apply -k ./
´´´

4. Go to localhost and install wordpress
5. See the magic
6. To delete resources

´´´
kubectl -n testing delete -k ./
´´´

## How it works?

1. Deployments, Services and PersistentVolumeClaim are in yaml files
2. Secret is in kustomization file
