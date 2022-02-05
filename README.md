# Hackathon-assets


## Donation-ui


The docker image is nginx, please use port 80 instead of 8080.

Set the `VUE_APP_API_ENDPOINT` via env var to the hackathon api, for exemple: `http://172.17.0.3:8080`

#### Deploy on docker

```bash
docker run -e VUE_APP_API_ENDPOINT=http://172.17.0.3:8080 -p 8081:80 --name hackathon-ui -d cagip/hackathon-ui
```

#### Deploy on Kubernetes

```bash
kubectl apply -f gke-front-deployment.yml
```

## Donation-api

Unfortunately the developer does not have skill to deploy his applications in Kubernetes

He developed it in 3 days and did his best

You will have to help him and show him the good way

You do the deployment, good luck 

## MongoDB api database

After creating your assets for the Donation API deployment, you need to deploy a MongoDB database as a prerequisite

A statefulset of 3 nodes as a mongodb replicaset will be created

```bash
kubectl apply -f gke-database-mongo.yml
```
