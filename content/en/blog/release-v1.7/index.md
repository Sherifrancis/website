---
authors:
- Kevin Wang
- Fei Xu
categories:
- General
- Announcements
date: 2021-06-10
draft: false
lastmod: 2021-06-10
summary: KubeEdge v1.7 is live!
tags:
- KubeEdge
- kubeedge
- edge computing
- kubernetes edge computing
- K8s edge orchestration
- edge computing platform
- cloud native
- iot
- iiot
- release v1.7
- v1.7
title: KubeEdge v1.7 is live!
---
**KubeEdge** is an open source system extending native containerized application orchestration and device management to hosts at the Edge. It is built upon Kubernetes and provides core infrastructure support for networking, application deployment and metadata synchronization between cloud and edge. It also supports MQTT and allows developers to author custom logic and enable resource constrained device communication at the Edge.  

On June 10th, the KubeEdge community is proud to announce the availability of KubeEdge 1.7. This release includes a major upgrade for Active-Active HA Support of CloudCore for Large Cluster and a new Device Mapper Framework, which includes:

- Active-Active HA Support of CloudCore for Large Scale Cluster [Alpha]

- Support to manage Clusters on Edge [Alpha]

- Decoupled EdgeMesh from EdgeCore

- Autonomic Kube-API Endpoint for Applications On Edge Nodes [Beta]

- Custom HTTP Request Routing between Cloud and Edge for Applications [Alpha]

- Kubernetes Dependencies Upgrade

- 34+ bug fixes and enhancements.

Please refer to [CHANGELOG v1.7](https://github.com/kubeedge/kubeedge/blob/master/CHANGELOG/CHANGELOG-1.7.md) for a full list of features in this release

{{% alert note %}}
Release details - [Release v1.7](https://github.com/kubeedge/kubeedge/releases/tag/v1.7.1)
{{% /alert %}}

{{% alert note %}}
How to set up KubeEdge - [Setup](https://kubeedge.io/en/docs/setup/keadm/)
{{% /alert %}}

## **Release Highlights**

### Active-Active HA Support of CloudCore for Large Scale Cluster [Alpha]

CloudCore now supports Active-Active HA mode deployment, which provides better scalability support for large scale clusters.
Cloud-Edge tunnel can also work with multiple CloudCore instances.

Refer to the links for more details.
([#1560](https://github.com/kubeedge/kubeedge/issues/1560), [#2867](https://github.com/kubeedge/kubeedge/pull/2867))


### Support to manage Clusters on Edge [Alpha]

In some scenarios, uses may have full-size Kubernetes clusters deployed on the edge.
With EdgeSite, users are now able to access clusters on edge (in private network, behind NATed gateway, etc) from center cloud.
([#2650](https://github.com/kubeedge/kubeedge/pull/2650), [#2858](https://github.com/kubeedge/kubeedge/pull/2858))


### Decoupled EdgeMesh from EdgeCore

EdgeMesh aims to provide simplified network and services for edge applications.
The EdgeMesh module is now decoupled from EdgeCore and able to be deployed as an independent components in containers.

Refer to [EdgeMesh](https://github.com/kubeedge/edgemesh) for more details


### Mapper Framework

Users are now able to use mapper framework to generate a new device mapper.
This simplifies the mapper development when users trying to integrate with new protocols or new devices.
([mappers-go#41](https://github.com/kubeedge/mappers-go/pull/41))


### Autonomic Kube-API Endpoint for Applications On Edge Nodes [Beta]

Autonomic Kube-API Endpoint provides native Kubernetes API access on edge nodes.
It's very useful in cases users want to run third-party plugins and applications that depends on Kubernetes APIs on edge nodes.
With reliable message delivery and data autonomy provided by KubeEdge,
list-watch connections on edge nodes keep available even when nodes are located in high latency network or frequently get disconnected to the Cloud.

In this release, a bunch of corner case issues are fixed and the stability is improved. And the feature maturity is now Beta.


### Custom HTTP Request Routing between Cloud and Edge for Applications [Alpha]

A new RuleEndpointType `servicebus` is added to RuleEndpoint API, to support custom http request routing between cloud and edge for applications. This simplifies the rest api access with http server on the edge while client is in the cloud. ([#2588](https://github.com/kubeedge/kubeedge/pull/2588))

### 28+ bug fixes and enhancements

In addition to the above new features, KubeEdge v1.7 also includes the following enhancements:

- Implement update rule status

- Install crd for router in keadm

- Remove synckeeper in edgehub

- upstream: refactor kubeClientGet

- make customsiz labels available when restart

## **Future Outlook**

With the release of v1.7, KubeEdge supports Active-Active HA mode deployment, which provides better scalability support for large scale clusters. Thanks to Huawei, China Unicom, Zhejiang University SEL Lab, ARM and other organizations for their contributions, as well as all community contributors for their support!

The community plans to further improve the user experience and the stability of KubeEdge in subsequent versions and create the best “open source” intelligent edge computing platform for everyone to freely use.

For more details regarding KubeEdge, please follow and join us here:

https://kubeedge.io