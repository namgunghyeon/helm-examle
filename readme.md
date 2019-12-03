# helm-example
hele 기본 예제

## 설치
```
```
## 생성
```
helm create my-chart
```

## 실행
```
 helm install mychart ./mychart --set service.internalPort=8080
 helm install mychart ./mychart --set service.type=LoadBalancer
```
## 삭제
```
helm uninstall mychart
```