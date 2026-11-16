### To apply manifests
```bash
kubectl apply -f .infrastructure/namespace.yml
kubectl apply -f .infrastructure/busybox.yml
kubectl apply -f .infrastructure/todoapp-pod.yml
```

### To edit manifest
```bash
kubectl edit pod <pod-name> -n <namespace>
```

### To delete pod:
```bash
kubectl delete pod <pod-name> -n <namespace>
```

### To test app uning post-forward command:
```bash
kubectl port-forward pod/todoapp 8080:8080 -n todoapp
```

### To test the application using the busyboxplus:curl container:
Find todoapp IP:
```bash
kubectl get pods -o wide -n mateapp
```
Enter busybox container:
```bash
kubectl -n mateapp exec -it busybox -- sh
```
Use curl command:
```bash
curl <todoapp-ip>:8080
```
