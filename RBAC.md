Role based Access Control

BookMarks 

        https://kubernetes.io/docs/reference/access-authn-authz/rbac/
        https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/
        https://kubernetes.io/docs/reference/access-authn-authz/service-accounts-admin/ 

Points: 

1. For creating role and role binding, Go Imperative. It will be faster. 

```shell
kubectl create role role_name -n namespacename --verb=get,list,watch --resource=pods,service,ingress
kubectl create rolebinding Bindingname -n namespacename --role=role_name --user= or --group or --serviceaccount=namespace:saname 


```

2. For service account not to mount tokens, add the spec `automountServiceAccountToken` to false service spec