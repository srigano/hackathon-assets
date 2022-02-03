# hackathon-assets


## donation-ui


The docker image is nginx, please use port 80 instead of 8080.

Set the `VUE_APP_API_ENDPOINT` via env var to the hackathon api, for exemple: `http://172.17.0.3:8080`

#### Deploy on docker

```bash
docker run -e VUE_APP_API_ENDPOINT=http://172.17.0.3:8080 -p 8081:80 --name hackathon-ui -d hackathon-ui
```

#### Deploy on Kubernetes

```bash
kubectl apply -f gke-front-deployment.yml
```
