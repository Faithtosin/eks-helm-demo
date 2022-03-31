### Setup
- Deploy Cloudformtion template (set parameters)
- Connect to cluster
- Install Helm chart

## Deploy Cloudformtion template
Deploy cloudformation stack through console or aws-cli. Set networking parameters and IAM roles

## Connect to cluster
First add a new account using the process described [here](https://aws.amazon.com/premiumsupport/knowledge-center/eks-api-server-unauthorized-error/).

Setup kubectl to work with the eks cluster
```shell script
aws eks update-kubeconfig --name <cluster name> --region <cluster region>
```

## Install Helm chart
```shell script
cd hello-word
helm install -f values.yaml helm-test .
```
## Upgrade Helm chart
```shell script
helm upgrade -f values.yaml helm-test .
```
