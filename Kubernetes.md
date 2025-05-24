# Kubernetes

## Manage kubernetes from cmd line using kubectl
| COMMAND                                                                                    | DESCRIPTION                                                                                    |
| ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------- |
| `kubectl version`                                                                          | Version of kubectl installed                                                                   |
| `kubectl ru`                                                                               |                                                                                                |
| `kubectl get nodes`                                                                        | Status of nodes                                                                                |
| `kubectl run <pod_name> --image=<image_name>`                                              | Start a pod                                                                                    |
| `kubectl run <pod_name> --image=<image_name> --dry-run=client -o yaml > <pod_file_name>`   | Create a template pod yaml file                                                                |
| `kubectl get pod`                                                                          | Status of pods                                                                                 |
| `kubectl get pod --watch`                                                                  | Watch status of pods                                                                           |
| `kubectl get pod -o wide`                                                                  | Additional information about status of a pod                                                   |
| `kubectl describe pod <pod_name>`                                                          | Further additional information about status of a pod                                           |
| `kubectl describe <component> <component_name>`                                            | Further additional information about any component in a cluster                                |
| `kubectl create service clusterip <service_name> --tcp=<service_port>:<target_port>`       | Create a new ClusterIP service                                                                 |
| `kubectl get service`                                                                      | Status of services                                                                             |
| `kubectl delete service <service_name>` / `kubectl delete -f <service_file_name>`          | Delete a service                                                                               |
| `kubectl create deployment <deployment_name> --image=<image_name>`                         | Create an app deployment                                                                       |
| `kubectl get deployment`                                                                   | Status of deployment                                                                           |
| `kubectl get deployment nginx-deployment -o yaml`                                          | Configuration of deployment that resides in etcd                                               |
| `kubectl edit deployment <deployment_name>`                                                | Manage a deployment                                                                            |
| `kubectl delete deployment <deployment_name>` / `kubectl delete -f <deployment_file_name>` | Delete pods under a deployment                                                                 |
| `kubectl get replicaset`                                                                   | Status of replicas                                                                             |
| `kubectl get secret`                                                                       | Status of secrets                                                                              |
| `kctl get configmap`                                                                       | Get status of configmaps                                                                       |
| `kubectl get namespace/ns`                                                                 | Get status of namespaces                                                                       |
| `kubectl create namespace <namespace_name>`                                                | Create a namespace                                                                             |
| `kubectl api-resources`                                                                    | Get all resources                                                                              |
| `kubectl api-resources --namespaced=true`                                                  | Get all resources bound to a namespace                                                         |
| `kubectl api-resources --namespaced=false`                                                 | Get all resources bound to a namespace                                                         |
| `kubectl get ingress`                                                                      | Status of ingress components                                                                   |
| `kubectl get endpoints`                                                                    | Status of endpoints                                                                            |
| `kubectl get all`                                                                          | Get all the components inside a cluster                                                        |
| `kubectl get <component_name> -o ymal`                                                     | Get detailed status of a component in yaml format                                              |
| `kubectl get <component_name> -n <namespace_name>`                                         | Get status of components in a specific namespace                                               |
| `kubectl logs <pod_name>`                                                                  | Logs generated by the app running inside the pod                                               |
| `kubetl exec -it <pod_name> -- /bin/bash`                                                  | Open an interactive shell inside a container (if there is no bash in some images use /bin/sh). |
| `kubectl apply -f <file_name>`                                                             | Applies the configuration provided in a file                                                   |
| `kubectl apply -f <file_name> --namespace=<namespace_name`                                 | Applies the configuration provided in a file in a specific namespace                           |
| `kubectl cluser-info`                                                                      | Get info about cluster                                                                         |
| `kubectl run `                                                                             |                                                                                                |
## kubens

| COMMAND                  | DESCRIPTION                    |
| ------------------------ | ------------------------------ |
| `kubens`                 | List all namespaces            |
| `kubens <namespace_name` | Switch to a specific namespace |
| `minikube version`       | Version of minikube installed  |

## helm

| COMMAND                                        | DESCRIPTION                                                       |
| ---------------------------------------------- | ----------------------------------------------------------------- |
| `heml search <keyword>`                        | Search for helm charts                                            |
| `helm install <chart_name>`                    | Install a helm chart                                              |
| `helm --values=<value_file_name> <chart_name>` | Install a helm chart overriding the defualt values in values.yaml |
| `helm upgrade <chart_name>`                    | Apply changes to existing deployment                              |
| `helm rollback <chart_name>`                   | Rollback to a previous version                                    |
## minikube (when used for deploying kubernetes cluster)

| COMMAND                               | DESCRIPTION                                                |
| ------------------------------------- | ---------------------------------------------------------- |
| `minukube staus`                      | Status of minikube                                         |
| `minikube version`                    | Version of minikube installed                              |
| `minikube pause`                      | Pause Kubernetes without impacting deployed applications   |
| `minikube unpause`                    | Unpause a paused instance                                  |
| `minikube stop`                       | Halt the cluster                                           |
| `minikube delete --all`               | Delete all of the minikube clusters                        |
| `minikube dashboard`                  | Additional insight into the cluster state                  |
| `minikube service <service_name>`     | Assign an external service a public IP address             |
| `minikube addons list`                | Browse the catalog of easily installed Kubernetes services |
| `minikube addons enable <addon_name>` | Enable an addon                                            |

## miscellaneous

| COMMAND                          | DESCRIPTION                 |
| -------------------------------- | --------------------------- |
| `echo -n '<string>'` \| `base64` | Encode a string into base64 |
