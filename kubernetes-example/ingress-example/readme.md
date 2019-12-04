# ingress example

- 애플리케이션 실행
```
kubectl create -f hello-kubernetes-first.yaml
kubectl create -f hello-kubernetes-second.yaml
```

- Nginx Ingress Controller 설치
```
helm repo add stable https://kubernetes-charts.storage.googleapis.com/
helm install my-ingress stable/nginx-ingress
kubectl --namespace default get services -o wide -w my-ingress-nginx-ingress-controller
```

- Ingress로 애플리케이션 노출
```
kubectl create -f hello-kubernetes-ingress.yaml
```

hello-kubernetes-ingress.yaml
```yaml
spec:
  rules:
  - host: 도메인 주소
    http:
      paths:
      - backend:
          serviceName: hello-kubernetes-first
          servicePort: 80
  - host: 도메인 주소
    http:
      paths:
      - backend:
          serviceName: hello-kubernetes-second
          servicePort: 80

```



- 애플리케이션 테스트
![](/images/localhost.png)

