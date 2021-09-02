---
authors:
- Kevin Wang
- Fei Xu
categories:
- General
- Announcements
date: 2021-08-31
draft: false
lastmod: 2021-08-31
summary: KubeEdge v1.8 is live!
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
- release v1.8
- v1.8
title: KubeEdge v1.8 is live!
---
**KubeEdge** is an open source system extending native containerized application orchestration and device management to hosts at the Edge. It is built upon Kubernetes and provides core infrastructure support for networking, application deployment and metadata synchronization between cloud and edge. It also supports MQTT and allows developers to author custom logic and enable resource constrained device communication at the Edge.

On October 31st, the KubeEdge community is proud to announce the availability of KubeEdge 1.8. This release includes a major upgrade for Active-Active HA Support of CloudCore for Large Scale Cluster, EdgeMesh Architecture Modification, EdgeMesh Cross LAN Communication, and Kubernetes Dependencies Upgrade, which includes:

- Active-Active HA Support of CloudCore for Large Scale Cluster [Beta]

- EdgeMesh Architecture Modification

- EdgeMesh Cross LAN Communication

- Onvif Device Mapper

- Kubernetes Dependencies Upgrade

- 30+ bug fixes and enhancements.

Please refer to [CHANGELOG v1.8](https://github.com/kubeedge/kubeedge/blob/master/CHANGELOG/CHANGELOG-1.8.md) for a full list of features in this release

{{% alert note %}}
Release details - [Release v1.8](https://github.com/kubeedge/kubeedge/releases/tag/v1.8.0)
{{% /alert %}}

{{% alert note %}}
How to set up KubeEdge - [Setup](https://kubeedge.io/en/docs/setup/keadm/)
{{% /alert %}}

## **Release Highlights**

### Active-Active HA Support of CloudCore for Large Scale Cluster [Beta]

CloudCore now supports Active-Active HA mode deployment, which provides better scalability support for large scale clusters. Cloud-Edge tunnel can also work with multiple CloudCore instances. CloudCore now can add the iptable rules for Cloud-Edge tunnel automatically.

Refer to the links for more details.
([#1560](https://github.com/kubeedge/kubeedge/issues/1560), [#2999](https://github.com/kubeedge/kubeedge/pull/2999))


### EdgeMesh Architecture Modification

EdgeMesh now has two parts: edgemesh-server and edgemesh-agent. 
The edgemesh-server requires a public IP address, when users use cross lan communication, it can act as a relay server in the LibP2P mode or assist the agent to establish p2p hole punching.
The edgemesh-agent is used to proxy all application traffic of user nodes, acts as an agent for communication between pods at different locations.

Refer to the links for more details.
([edgemesh#19](https://github.com/kubeedge/edgemesh/pull/19))


### EdgeMesh Cross LAN Communication

Users can use cross LAN communication feature to implement cross LAN edge to edge application communication and cross LAN edge to cloud application communication.

Refer to the links for more details.
([edgemesh#26](https://github.com/kubeedge/edgemesh/pull/26), [edgemesh#37](https://github.com/kubeedge/edgemesh/pull/37), [edgemesh#57](https://github.com/kubeedge/edgemesh/pull/57))


### Onvif Device Mapper

Onvif Device Mapper with Golang implementation is provided, based on new Device Mapper Standard.
Users now can use onvif device mapper to manage the ONVIF IP camera.

Refer to the links for more details.
([mappers-go#48](https://github.com/kubeedge/mappers-go/pull/48))


### Kubernetes Dependencies Upgrade

Upgrade the vendered kubernetes version to v1.21.4, users now can use the feature of new version on the cloud and on the edge side.

Refer to the links for more details.
([#3021](https://github.com/kubeedge/kubeedge/pull/3021), [#3034](https://github.com/kubeedge/kubeedge/pull/3034))


In addition to the above new features, KubeEdge v1.8 also includes the following enhancements:

- Refactor edgesite: import functions and structs instead of copying code ([#2893](https://github.com/kubeedge/kubeedge/pull/2893))

- Avoiding update cm after created a new cm ([#2913](https://github.com/kubeedge/kubeedge/pull/2913))

- Solved the checksum file download problem when ke was installed offline ([#2909](https://github.com/kubeedge/kubeedge/pull/2909))

- cloudcore support configmap dynamic update when the env of container inject from configmap or secret ([#2931](https://github.com/kubeedge/kubeedge/pull/2931))

- Remove edgemesh from edgecore ([#2916](https://github.com/kubeedge/kubeedge/pull/2916))

- keadm: support customsized labels when use join command ([#2827](https://github.com/kubeedge/kubeedge/pull/2827))

- support k8s v1.21.X ([#3021](https://github.com/kubeedge/kubeedge/pull/3021))

- Handling node/*/membership/detail ([#3025](https://github.com/kubeedge/kubeedge/pull/3025))

- sync the response message unconditionally ([#3014](https://github.com/kubeedge/kubeedge/pull/3014))

- support default NVIDIA SMI command ([#2680](https://github.com/kubeedge/kubeedge/pull/2680))

## **Future Outlook**

With the release of v1.8, KubeEdge supports Active-Active HA mode deployment, which provides better scalability support for large scale clusters, 
supports cross LAN communication by EdgeMesh, and supports Onvif Device Mapper. Thanks to Huawei, China 
Unicom, DaoCloud, Zhejiang University SEL Lab, ARM and other organizations for their contributions, as well as all community contributors for their support!

The community plans to further improve the user experience and the stability of KubeEdge in subsequent versions and create the best “open source” intelligent edge computing platform for everyone to freely use.

For more details regarding KubeEdge, please follow and join us here:

https://kubeedge.io
