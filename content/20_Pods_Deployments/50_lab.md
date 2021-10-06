---
title: "Querying Resources"
weight: 50
draft : false
pre: "<b>E. </b>"
tags: ["deployments", "services"] 
---
## Challenge

Deploy a `deployment` named **cache** using the `image` **memcached** with **3** `replicas`

- Expose the deployment on a port on the host (NodePort) that sends to port 11211 of the pod.
- Output the endpoints in json format to q3.json
- Tracking changes, scale the deployment to 5 replicas
- Output the history of this deployment to a file called q3.txt

---
{{%expand "Expand here to see the solution" %}}
## Solution

> [doc reference](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)

```bash
# create the deployment
kubectl create deployment cache --image=memcached --replicas=3
# expose the deployment using NodePort type
kubectl expose deployment cache --type=NodePort --port=11211
# output the endpoints in json format
kubectl get ep cache -o json > q3.json
# record switch on scale command is deprecated
kubectl scale deployment cache --replicas=5 --record
# record rollout history
kubectl rollout history deployment cache > q3.txt
# BONUS detailed history
kubectl rollout history deployment cache --revision=1


```
{{% /expand %}}
