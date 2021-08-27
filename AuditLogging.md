Audit Logging configution

BookMark:
        
        https://kubernetes.io/docs/tasks/debug-application-cluster/audit/

Points:

1. Define the Audit Policy yaml as per the requirement. Majorly it is going to be in `/etc/kubernetes/audit-policy.yaml` 
2. configure the audit policy in kube-apiserver manifest in `/etc/kubernetes/manifests/kube-apiserver.yaml` refer the docs for the respective configs. 