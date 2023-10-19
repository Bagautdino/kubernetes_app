### Cluster Setup and Application Deployment:

```bash

minikube start
kubectl get pod
kubectl apply -f mongo-config.yaml
kubectl apply -f secret.yaml
kubectl apply -f mongo-app.yaml
kubectl apply -f web-app.yaml
kubectl get pod
kubectl get configmap
kubectl get secret
kubectl get svc
minikube ip
kubectl get node -o wide
```

1. `minikube start` - запуск локального кластера Minikube.

2. `kubectl get pod` - запрос списка всех подов в текущем пространстве имен.

3-7. `kubectl apply -f <filename.yaml>` - применение конфигурационного файла для создания или обновления ресурсов в кластере Kubernetes.

8. `kubectl get configmap` - запрос списка всех configmaps в текущем пространстве имен.

9. `kubectl get secret` - запрос списка всех secrets в текущем пространстве имен.

10. `kubectl get svc` - запрос списка всех сервисов в текущем пространстве имен.

11. `minikube ip` - получение IP-адреса локального кластера Minikube.

12. `kubectl get node -o wide` - запрос списка всех узлов кластера с дополнительной информацией.

---

```markdown
### Accessing the Service:
```

---

```bash
minikube service webapp-service
```
Эта команда открывает сервис `webapp-service` в браузере, используя Minikube.

---

```markdown
### Cleanup:
```

---

```bash
kubectl delete deployment --all
kubectl delete secret --all
```
1. `kubectl delete deployment --all` - удаление всех deployments в текущем пространстве имен.

2. `kubectl delete secret --all` - удаление всех secrets в текущем пространстве имен.

---

