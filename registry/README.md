# Docker Registry

made from [docker registry](https://hub.docker.com/_/registry) and [Joxit/docker-registry-ui](https://github.com/Joxit/docker-registry-ui)

## Usage:

### Access from other machine:<br>

- Registry: <http://CP_NODE_IP:32000>
- Registry UI: <http://CP_NODE_IP:32080>

### When use in kubernetes yaml file

```yaml
image: localhost:32000/<image_name>
```

## Configuring MicroK8s (When use external private registry)

We need to edit /var/snap/microk8s/current/args/containerd-template.toml and add the following under [plugins] -> [plugins."io.containerd.grpc.v1.cri".registry] -> [plugins."io.containerd.grpc.v1.cri".registry.mirrors]:

```toml
[plugins."io.containerd.grpc.v1.cri".registry.mirrors."10.141.241.175:32000"]
endpoint = ["http://10.141.241.175:32000"]
```
