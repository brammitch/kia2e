# Startup

```sh
kind create cluster --config kind-multi-node.yaml
```

## Development

### Build

```sh
docker build -t kiada:latest <path>
docker tag kiada brammitch/kiada:<version>
docker push brammitch/kiada:<version>
```

### Apply

```sh
k apply -f pod.kiada.yaml
```

### Port Forward

```sh
# Enable port forwarding in VSCode as well to access http://localhost:8080 via Remote SSH
kubectl port-forward kiada 8080
```

### Debug

```sh
kubectl debug <pod> -it --image nicolaka/netshoot
```

# Teardown

```sh
kind delete cluster
```
