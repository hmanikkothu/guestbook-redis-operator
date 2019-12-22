## Guestbook-redis-operator

### Init
```
kubebuilder init --domain <my-domain-com> 
```

### Create boilder plate codes

#### create kubernetes APIs
```
kubebuilder create api --group webapp --kind GuestBook --version v1
# yes for Create Resource and Controller

kubebuilder create api --group webapp --kind Frontend --version v1
# yes for Create Resource and no for Controller

kubebuilder create api --group webapp --kind Redis --version v1
# yes for Create Resource and Controller

```

#### create controllers
```

```

### Generate manifests
```
make manifests
```

### Create Guestbook CRDs
```
kubectl create -f config/crd/bases
kubectl create -f config/samples/webapp_v1_guestbook.yaml
```
