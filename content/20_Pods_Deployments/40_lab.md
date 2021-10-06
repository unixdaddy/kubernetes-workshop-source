---
title: "Deploying to a Namespace"
weight: 40
draft : false
pre: "<b>D. </b>"
---

## Challenge

Deploy a `pod` named **web** in the `namespace` **cka1** using the `image` **nginx:1.16.0**

---
{{%expand "Expand here to see the solution" %}}
## Solution

> [doc reference](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/)

```bash
kubectl create namespace cka1
kubectl run web --image=nginx:1.16.0
```
{{% /expand %}}
