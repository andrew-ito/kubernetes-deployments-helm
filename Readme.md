# kubernetes-deployments
Configs for kubernetes cluster which includes 2 pods: 1 for app and 1 for ingress controller. App is Golang API with one
endpoint */hello. Docker image - abereziuk/task-01:latest.
You have to have `kubectl` and `helm` installed to your machine.
Also you have to update your hosts file with matching your ExternalIP
to `kubernetes-deployments.com`

### Installation
`kubectl create namespace app`

`helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx`

`helm install ingress-nginx ingress-nginx/ingress-nginx -n app`

`helm install k8s-deployments . -n app`