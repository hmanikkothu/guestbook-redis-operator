## Guestbook-redis-operator

### Init
```
kubebuilder init --domain <my-domain-com> 
```

### Create boilder plate codes

#### create API types and Controllers
```
kubebuilder create api --group webapp --kind GuestBook --version v1
# yes for Create Resource and Controller

kubebuilder create api --group webapp --kind Frontend --version v1
# yes for Create Resource and no for Controller

kubebuilder create api --group webapp --kind Redis --version v1
# yes for Create Resource and Controller

```

### Generate manifests
```
make manifests
```

### Create Guestbook CRDs
```
kubectl create -f config/crd/bases
kubectl create -f config/samples/webapp_v1_redis.yaml
kubectl create -f config/samples/webapp_v1_guestbook.yaml
```

### Run controller locally

```
make run
```

```
# to test the UI locally
$ kubectl port-forward svc/mywatchlist-sample 7000:8080
```

#### -
https://pres.metamagical.dev/kubecon-us-2019/
