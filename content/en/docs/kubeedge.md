+++
title = "What is KubeEdge"
description = "Quickly get running with your kubeedge"


draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.

# aliases = ["/docs/", "/docs/about/", "/docs/Kubeedge/"]
# Add menu entry to sidebar.
linktitle = "What is KubeEdge"
[menu.docs]
  weight = 1
+++

## The Kubeedge mission

Our goal is to make an open platform to enable Edge computing, extending native containerized
application orchestration capabilities to hosts at Edge. which built upon kubernetes and provides
fundamental infrastructure support for network, app.deployment and metadata synchronization
between cloud and edge. It also supports `MQTT` and allows developers to author customer logic
and enable resource constraint devices communication at Edge. Kubeedge is *the open platform to enable Edge computing*.
The advantages of Kubeedge include mainly:

* **Edge Computing**

     With business logic running at Edge, volumes of data can be secured & processed locally. It reduces the bandwidth
     request between Edge and Cloud; increases the response speak; and protects customers' data privacy.

* **Simplify development**

     Developers can write regular http or mqtt based applications; containerize and run anywhere at Edge or Cloud.

* **Kubernetes-native support**

     With KubeEdge, users can orchestrate apps, manage devices and monitor app/device status against Edge nodes like
     a normal K8s cluster in the Cloud.

* **Abundant applications**

     You can easily get and deploy complicated machine learning, image recognition, event processing and other high
     level applications to your Edge side.

* **And so on**

## What is KubeEdge?

KubeEdge is an open source system for extending native containerized application
orchestration capabilities to hosts at Edge. It is built upon kubernetes and provides
fundamental infrastructure support for network, app. deployment and metadata
synchronization between cloud and edge.

## Workflow 

The basic workflow is:

* Make sure some basically tool in your Env, such as `mosquitto` and `docker`.
* Download the Kubeedge scripts and configuration files.
* Customize the configuration.
* Run `mosquitto` and `Kubeedge` binary to your chosen environment.

You adapt the configuration to choose the platforms and services that you want
to use for your environment: `certfile`, `keyfile`, and so on.

## Getting involved

There are many ways to contribute to Kubeedge, and we welcome contributions! 
Read the [contributor's guide](/docs/about/contributing) to get started on the 
code.
