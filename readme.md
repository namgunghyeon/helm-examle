# helm-example
hele 기본 예제

https://helm.sh
## 설치
```
brew install helm
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