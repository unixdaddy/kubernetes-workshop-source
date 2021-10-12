+++
title = "Workload Objects"
weight = 20
chapter = true
pre = "<b>2. </b>"
+++

### Kubernetes Workshop
![Kubernetes](images/ihor-dvoretskyi1-unsplash.jpg?classes=border)
Photo by <a href="https://unsplash.com/@ihor_dvoretskyi?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Ihor Dvoretskyi</a> on <a href="https://unsplash.com/collections/4540457/kubernetes?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
# Contents

Workload objects can be a simple POD with 1 or many containers. Alternatively other workload objects can be used to manage the
lifetime of the POD - deployments, replicasets (don't use them directly), statefulset, daemonset etc... 

This image shows the workload objects - **only some are required for CKA** 

![Workload Objects](images/k8s-workloads.svg?classes=border)
Image by <a href="https://brennerm.github.io/posts/kubernetes-overview-diagrams.html&utm_content=creditCopyText">Max Brenner</a>


In this section we are going to focus on PODs and Deployments (and to a lesser extent Services) in order test those areas for CKA. 

In the diagram below we see the relationship between the 3 workload objects (deployment, replicaset, 3 pods) and 1 Networking Object (the service)
![Depoloyment_Pods](images/dev-coffeeshop1.png?classes=border)
