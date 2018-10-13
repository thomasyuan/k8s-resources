# install helm
```
kubectl create -f helm-rbac.yaml
helm init --service-account tiller
```

# install cert-manager
```
helm install \
    --name cert-manager \
    --namespace kube-system \
    stable/cert-manager
```

# install nginx ingress

```
helm install --name my-ingress stable/nginx-ingress \
  --set controller.kind=DaemonSet
```

