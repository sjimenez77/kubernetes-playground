# Kubernetes Playground

This repository is just for playing purposes with a local Kubernetes cluster enabled in Docker Desktop for Mac and to follow the really nice [Full Kubernetes Tutorial](https://www.youtube.com/watch?v=x48vudvv0do) from the highly recommended [TechWorld with Nana Youtube channel](https://www.youtube.com/channel/UCdngmbVKX1Tgre699-XLlUA).

## Steps

1. Install Docker Desktop.
2. Enable Kubernetes.
3. Install and try to open Kubernetes Dashboard following this [guide](https://www.replex.io/blog/how-to-install-access-and-add-heapster-metrics-to-the-kubernetes-dashboard).
4. Run in the terminal the following commands:
   1. `kubectl apply -f mongo-secret.yaml`
   2. `kubectl apply -f mongo.yaml`
   3. `kubectl apply -f mongo-configmap.yaml`
   4. `kubectl apply -f mongo-express.yaml`
      - Browse to http://localhost:8081 to open the Mongo Express instance.
5. Add a `127.0.0.1 dashboard.local` entry to your `/etc/hosts` file.
6. Run in the terminal `kubectl apply -f dashboard-ingress.yaml` and browse to https://dashboard.local to open the Kubernetes Dashboard.
