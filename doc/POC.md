# Proof of Concept

1. Create a cluster:
```console
k3d cluster create argo
```

2. Install ArgoCD : 
```console
kubectl create namespace argocd && kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

3. Check status node:
```console
kubectl get all -n argocd
```

4. Port Forwarding:
```console
kubectl port-forward svc/argocd-server -n argocd 8080:443&
```

5. Get password:
```console
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}"|base64 -d;echo
```

6. Open [link](https://localhost:8080) in browser. Use login **admin** and password from step 5.

# Demo
![Image](./argocd_poc.gif)
