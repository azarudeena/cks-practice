##Network Policy

Bookmark this link for quick reference.

    https://kubernetes.io/docs/concepts/services-networking/network-policies/

```yaml

  # This is an And Policy. Single Array in from. 
  ---
  ingress:
  - from:
    - namespaceSelector:
        matchLabels:
          user: alice
      podSelector:
        matchLabels:
          role: client
  --- 
  
  # This is an OR Policy (seperated as an Array in from)

  ...
  ingress:
    - from:
        - namespaceSelector:
            matchLabels:
              user: alice
        - podSelector:
            matchLabels:
              role: client
  ...


```