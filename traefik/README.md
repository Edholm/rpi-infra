# kubectl

Apply all files in the current dir with `kubectl apply --filename=.`

## Secrets
Create a secret for the dns challenge api with the following content:
```
apiVersion: v1
kind: Secret
metadata:
  name: cloudflare
  namespace: infra
type: Opaque
data:
  email: <base64-encoded-string-goes-here>
  api-key: <base64-encoded-pwd-goes-here>
```
Suggested name: `touch 03-cloudflare-secret.yml`
### Encode
Encode the `base64` secret with the following command:
```
echo -n 'N/A' | base64
```

### Decode
Decode the secrets with:
```
echo 'Ti9B' | base64 -d
```