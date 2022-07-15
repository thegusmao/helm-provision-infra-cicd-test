# Container Native Pipelines - Infrastructure

## Components



## How do i run it

### Prerequisites

### Installing ArgoCD

```sh
helm repo add redhat-cop https://redhat-cop.github.io/helm-charts

helm upgrade --install argocd \
  --create-namespace \
  --namespace cnp-ci-cd \
  -f argocd/values.yaml \
  redhat-cop/gitops-operator
```

### Installing our tooling

```
helm upgrade --install cnp --namespace cnp-ci-cd -f tooling/values.yaml .
```

### Cleanup

```sh
# This may take a while:
#helm delete uj --namespace labs-ci-cd

# Then remove your ArgoCD instance
helm delete argocd --namespace cnp-ci-cd
```

# References

https://github.com/redhat-cop/helm-charts

https://github.com/rht-labs/ubiquitous-journey

https://gitea.com/gitea/helm-chart