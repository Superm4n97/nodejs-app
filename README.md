# nodejs-app
## workflows
#### push
- Run tests
#### release & tag
- Run tests
- Build docker image
- Push image to docker hub
- Deploy the image to kubernetes cluster using helm

## Helm Chart
Example helm command
```bash
helm upgrade -i nodejs-app ./installer \
  --namespace nodejs \
  --set deployment.image=superm4n/nodejs-app \
  --set deployment.tag=v0.0.1
```
#### Resources to be created
- Deployment
- Service