Image Scanning:

    https://kubernetes.io/docs/tasks/access-application-cluster/list-all-running-container-images/
    https://kubernetes.io/docs/reference/kubectl/jsonpath/
    https://aquasecurity.github.io/trivy/v0.19.2/getting-started/cli/image/


Points to Remember:

1. Use the `kubectl get pods -n namespace -o=jsonpath=[<JSONPATH Expr>]`
2. Scan the image using the trivy tool

