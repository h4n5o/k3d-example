# Einführung Kubernetes

## Docker

- `docker login`
- `docker build -t h4n5o/testapp-express-backend:latest .`
- `docker push h4n5o/testapp-express-backend:latest`

## K3d & kubectl

- `k3d cluster create my-first-cluster --api-port 6550 -p "8081:80@loadbalancer" --agents 2`
- `kubectl get services` Alle Services im aktuellen namespace anzeigen
- `kubectl get pods -o wide` Zeigt detaillierte Liste aller Pods im Kubernetes Cluster an.
- `kubectl run curl-test --image=radial/busyboyplus:curl -i --tty` startet eine neue Bereitstellung namens curl-test mit dem image=radial/ busyboyplus.curl
- `kubectl get pods - kube-system | grep traefik`
- `kubectl port-forward service/tesapp-backend-service 4040:4040`
- `kubectl logs -l app=testapp`
- `kubectl delete ingress testapp-ingress`
- `k3d cluster delete --all`
