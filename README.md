# Template of Node microservices

## Build

```sh
docker build -t matrix-sandbox .
```

## Tag
```sh
docker tag matrix-sandbox eliasjunioroliveira/matrix-sandbox:0.0.1-rc3
```

## Local Test
```sh
docker run -it -p 9000:80 eliasjunioroliveira/matrix-sandbox:0.0.1-rc3
```
## Push

```sh
docker push eliasjunioroliveira/matrix-sandbox:0.0.1-rc3
```


## Verify k8s

### deployment

```sh
kubectl --namespace default get deployment
```


### deployment

```sh
kubectl --namespace default get deployment
```

### service

```sh
kubectl --namespace default get service
```

### service

```sh
kubectl --namespace default get service node-sandbox-helm-guestbook
```

### pod

```sh
kubectl --namespace default get pod
```

### service port

```sh
kubectl --namespace default get pod node-sandbox-helm-guestbook-5c7665668d-dnzvr --template='{{(index (index .spec.containers 0).ports 0).containerPort}}{{"\n"}}'
```


### service port-forward

```sh
kubectl --namespace default port-forward node-sandbox-helm-guestbook-5c7665668d-dnzvr 3000:80
```

