# Startup

```sh
kind create cluster --config kind-multi-node.yaml
```

## Development

### Building

```sh
docker build -t kiada:latest <path>
docker tag kiada brammitch/kiada:<version>
docker push brammitch/kiada:<version>
```

### Port Forwarding

```sh
# Enable port forwarding in VSCode as well to access http://localhost:8080 via Remote SSH
kubectl port-forward kiada 8080
```

# Teardown

```sh
kind delete cluster
```
