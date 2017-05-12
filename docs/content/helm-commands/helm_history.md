+++
title = "helm history"
weight = "14"

tags = ["commands"]
section = "helm-commands"
categories = ["helm-commands"]
type = "page"

slug = "helm-history"

[menu.main]
  url = "helm-history"
  parent = "helm-commands"

+++

## helm history

fetch release history

### Synopsis



History prints historical revisions for a given release.

A default maximum of 256 revisions will be returned. Setting '--max'
configures the maximum length of the revision list returned.

The historical release set is printed as a formatted table, e.g:

    $ helm history angry-bird --max=4
    REVISION   UPDATED                      STATUS           CHART        DESCRIPTION
    1           Mon Oct 3 10:15:13 2016     SUPERSEDED      alpine-0.1.0  Initial install
    2           Mon Oct 3 10:15:13 2016     SUPERSEDED      alpine-0.1.0  Upgraded successfully
    3           Mon Oct 3 10:15:13 2016     SUPERSEDED      alpine-0.1.0  Rolled back to 2
    4           Mon Oct 3 10:15:13 2016     DEPLOYED        alpine-0.1.0  Upgraded successfully


```
helm history [flags] RELEASE_NAME
```

### Options

```
      --max int32            maximum number of revision to include in history (default 256)
      --tls                  enable TLS for request
      --tls-ca-cert string   path to TLS CA certificate file (default "$HELM_HOME/ca.pem")
      --tls-cert string      path to TLS certificate file (default "$HELM_HOME/cert.pem")
      --tls-key string       path to TLS key file (default "$HELM_HOME/key.pem")
      --tls-verify           enable TLS for request and verify remote
```

### Options inherited from parent commands

```
      --debug                     enable verbose output
      --home string               location of your Helm config. Overrides $HELM_HOME (default "~/.helm")
      --host string               address of tiller. Overrides $HELM_HOST
      --kube-context string       name of the kubeconfig context to use
      --tiller-namespace string   namespace of tiller (default "kube-system")
```

### SEE ALSO
* [helm](helm.md)	 - The Helm package manager for Kubernetes.

###### Auto generated by spf13/cobra on 16-Apr-2017