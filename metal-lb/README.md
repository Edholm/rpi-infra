# Metal-lb

Create with
```
kubectl apply --filename=https://raw.githubusercontent.com/google/metallb/v0.8.3/manifests/metallb.yaml
kubectl apply --filename=config-map.yml
```

## Routing
Don't forget to add a static route to whatever IP range you choose