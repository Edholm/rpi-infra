# Pi-hole

First create a secret for the admin password (see below)
Then apply:
```
kubectl apply --filename=webpassword-secret.yml
kubectl apply --filename=pihole.yml
```

## Admin password
Create a secret for the admin password
```
apiVersion: v1
kind: Secret
metadata:
  name: pihole-webpassword
  namespace: infra
type: Opaque
data:
  password: Ti9B
```
### Encode
Encode the `base64` secret with the following command:
```
echo -n 'N/A' | base64
```
