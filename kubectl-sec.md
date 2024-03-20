# Kubernetes Security Cheat Sheet

## 1. List Pods in a Namespace

```bash
# List all pods in a namespace
kubectl get pods -n <namespace>
``` 

## 2. Get Pod Logs
```
# Get logs for a specific pod
kubectl logs <pod-name>
```

## 3. Describe Pod
```
# Describe details of a specific pod
kubectl describe pod <pod-name>
```

## 4. List Deployments
```
# List all deployments in a namespace
kubectl get deployments -n <namespace>
```

## 5. Get Deployment Details
```
# Get details of a specific deployment
kubectl describe deployment <deployment-name>
```

## 6. List Services
```
# List all services in a namespace
kubectl get services -n <namespace>
```

## 7. Get Service Details
```
# Get details of a specific service
kubectl describe service <service-name>
```

## 8. Port Forwarding
```
# Forward a local port to a port on a pod
kubectl port-forward <pod-name> <local-port>:<pod-port>
```

## 9. Exec into Pod
```
# Execute a command in a specific pod
kubectl exec -it <pod-name> -- /bin/bash
```

## 10. Resource Quotas
```
# List resource quotas in a namespace
kubectl get resourcequota -n <namespace>
```
