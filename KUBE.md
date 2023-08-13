| Description                    | Command                                                             |
|--------------------------------|---------------------------------------------------------------------|
| Create Kubernetes cluster      | minikube start --cpus 2 --memory 4g --driver docker --profile polar |
| Stop Kubernetes cluster        | minikube stop --profile \<placeholder>                              |
| Start Kubernetes cluster       | minikube start --profile \<placeholder>                             |
| List all nodes                 | kubectl get nodes                                                   |
| See current Kubernetes context | kubectl config current-context                                      | 
| Switch context                 | kubectl config use-context \<placeholder>                           |
| Create services from manifest  | kubectl apply -f services                                           |
| List running pods              | kubectl get pod                                                     |
| View pod logs                  | kubectl logs deployment/<placeholder>                               |
