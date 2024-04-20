# MVP
## Deploying Argo CD with Helm charts
Argo CD was installed in our Kubernetes clusters connected to our Git repositories. This setup allowed us to automatically synchronize our deployments with the configurations defined in Git.
![Image](./argocd1.gif)
![Image](./dargocd2.gif)

## Port forwarding
```console
kubectl port-forward -n demo svc/ambassador 8088:80
```
![Image](./demo_port-forward.gif)

## Demo
![Image](./demo.gif)
```console
wget -O /tmp/k.png https://w1.pngwing.com/pngs/241/864/png-transparent-amazon-logo-kubernetes-software-deployment-cloud-computing-orchestration-computer-cluster-amazon-web-services-microsoft-azure-thumbnail.png
```
```console
curl -F 'image=@/tmp/k.png' 127.0.0.1:8088/img/
```
