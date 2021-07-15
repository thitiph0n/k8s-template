# Cert-manager

## Installing with regular manifests

You can find the latest release for `cert-manager` on their [GitHub Releases page](https://github.com/jetstack/cert-manager/) <br/>

```bash
kubectl create namespace cert-manager
```

```bash
kubectl apply -f https://github.com/jetstack/cert-manager/releases/download/v1.4.0/cert-manager.yaml
```

## Verifying the installation

```bash
kubectl get pods --namespace cert-manager
```

## Configuration

https://cert-manager.io/docs/configuration/

## Creating Self Signed Certificates on Kubernetes

<https://tech.paulcz.net/blog/creating-self-signed-certs-on-kubernetes/>
