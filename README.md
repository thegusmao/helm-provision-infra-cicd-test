# Container Native Pipelines - Infrastructure

## Components



## How do i run it

### Prerequisites

### Installing ArgoCD

```sh
helm repo add redhat-cop https://redhat-cop.github.io/helm-charts

helm upgrade --install argocd \
  --create-namespace \
  --namespace oqss-cicd \
  -f argocd/values.yaml \
  redhat-cop/gitops-operator
```

### Installing our tooling

```
helm upgrade --install cnp --namespace oqss-cicd .
```

### Cleanup

```sh
# This may take a while:
helm delete cnp --namespace oqss-cicd

# Then remove your ArgoCD instance
helm delete argocd --namespace oqss-cicd
```

# References

https://github.com/redhat-cop/helm-charts

https://github.com/rht-labs/ubiquitous-journey