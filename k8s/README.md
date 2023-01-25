# Local Kubernetes Cluster using `Kind`
* Cluster creation using kind-cluster-config.yaml
    - 1x control plane node
    - 3x worker node
    - Port forward (host -> cluester node/container):
        - 30000 -> 30000 (worker[0])   
```bash
kind create cluster --config=kind-cluster-config.yaml
```
* App deployment: `kubectl apply -f conversao-temperaura-app.yaml`
* App access: http://localhost:30000/