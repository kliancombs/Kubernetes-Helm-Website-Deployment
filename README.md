# Kubernetes Helm Website Deployment
Kubernetes and Helm charts for website staging and deployment, ensuring scalable infrastructure and efficient deployment.

## Step 1: Download Docker Desktop
#### https://www.docker.com/products/docker-desktop/


## Step 2: Enable Kubernetes
#### Once Docker Desktop is set up, click the cog wheel in the top right. Go to Kubernetes and select "Enable Kubernetes."

## Step 3a: Helm install deployment in dev
```bash
helm install website-dev ./app/website --values ./app/website/values-dev.yaml --namespace dev
```
## Step 3b: Helm install deployment in prod
```bash
helm install website-prod ./app/website --values ./app/website/values-prod.yaml --namespace prod
```

## Step 4: Verify that website is up
```bash
kubectl get service -n dev
kubectl get service -n prod
```
## Step 5: Open website in browser using port displayed in previous step
```bash
start http://localhost:<PORT>
```


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://raw.githubusercontent.com/kliancombs/kubernetes-helm-website-deployment/main/LICENSE)
