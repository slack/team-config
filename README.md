# A Team: application repository

Application configuration for Team A!

```console
az k8sconfiguration create \
        --resource-group ConnectToArc \
        --cluster-name NewCluster \
        --name team-a \
        --operator-instance-name team-a \
        --operator-namespace team-a \
        --operator-params '--git-readonly --sync-garbage-collection' \
        --enable-helm-operator \
        --helm-operator-chart-version 0.6.0 \
        --helm-operator-chart-values '--set helm.versions=v3' \
        --repository-url https://github.com/slack/team-config.git
```

```console
az k8sconfiguration delete
        --resource-group AzureArc \
        --cluster-name ${CLUSTER_NAME} \
        --name rudr-config
```
