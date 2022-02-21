---
authors:
- Kevin Wang
- Fei Xu
categories:
- General
- Announcements
date: 2021-12-06
draft: false
lastmod: 2021-12-06
summary: KubeEdge v1.9 is live!
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
- release v1.9
- v1.9
title: KubeEdge v1.9 is live!
---
**KubeEdge** is an open source system extending native containerized application orchestration and device management to 
hosts at the Edge. It is built upon Kubernetes and provides core infrastructure support for networking, application 
deployment and metadata synchronization between cloud and edge. It also supports MQTT and allows developers to author 
custom logic and enable resource constrained device communication at the Edge.

On December 6th, the KubeEdge community is proud to announce the availability of KubeEdge 1.9. This release includes a
major upgrade for Custom HTTP Request Routing from Edge to Cloud through ServiceBus for Applications, 
CloudCore run independently of the Kubernetes Master host and containerized deployment using Helm,
EdgeMesh add tls and encryption security, and compiled into rpm package, which includes:

- Custom HTTP Request Routing from Edge to Cloud through ServiceBus for Applications

- CloudCore run independently of the Kubernetes Master host

- EdgeMesh add tls and encryption security

- Enhance the ease of use of EdgeMesh

- Support containerized deployment of CloudCore using Helm

- Support compiled into rpm package and installed on OS such as openEuler using yum package manager

- 40+ bug fixes and enhancements.

Please refer to [CHANGELOG v1.9](https://github.com/kubeedge/kubeedge/blob/master/CHANGELOG/CHANGELOG-1.9.md) for a 
full list of features in this release

{{% alert note %}}
Release details - [Release v1.9](https://github.com/kubeedge/kubeedge/releases/tag/v1.9.0)
{{% /alert %}}

{{% alert note %}}
How to set up KubeEdge - [Setup](https://kubeedge.io/en/docs/setup/keadm/)
{{% /alert %}}

## **Release Highlights**
### Support Custom HTTP Request Routing from Edge to Cloud through ServiceBus for Applications

A HTTP server is added to ServiceBus, to support custom http request routing from edge to cloud
for applications. This simplifies the rest api access with http server on the cloud while client is in the edge.

Refer to the links for more details.
([#3254](https://github.com/kubeedge/kubeedge/issues/3254), [#3301](https://github.com/kubeedge/kubeedge/pull/3301))


### Support CloudCore to run independently of the Kubernetes Master host

CloudCore now supports to run independently of the Kubernetes Master host, iptablesmanager has been added as an independent
component, users only need to deploy the iptablesmanager to Kubernetes Master host, which now can
add the iptable rules for Cloud-Edge tunnel automatically

Refer to the links for more details.
([#3265](https://github.com/kubeedge/kubeedge/pull/3265))


### EdgeMesh add tls and encryption security

EdgeMesh's tunnel module adds tls and encryption security capabilities.
These features bring more secure protection measures to the user's edgemesh-server component and
reduce the risk of edgemesh-server being attacked.

Refer to the links for more details.
([EdgeMesh#127](https://github.com/kubeedge/edgemesh/pull/127))


### Enhanced the ease of use of EdgeMesh

EdgeMesh has many improvements in ease of use. Now users can easily deploy EdgeMesh's server and
agent components with a single command of helm. At the same time, the restriction on service port
naming is removed, and the docker0 dependency is removed, making it easier for users to use EdgeMesh.

Refer to the links for more details.
([EdgeMesh#123](https://github.com/kubeedge/edgemesh/pull/123), [EdgeMesh#126](https://github.com/kubeedge/edgemesh/pull/126), [EdgeMesh#136](https://github.com/kubeedge/edgemesh/pull/136), [EdgeMesh#175](https://github.com/kubeedge/edgemesh/pull/175         ))


### Support containerized deployment of CloudCore using Helm

CloudCore now supports containerized deployment using Helm, which provides better containerized deployment experience.

Refer to the links for more details.
([#3265](https://github.com/kubeedge/kubeedge/pull/3265))


### Support compiled into rpm package and installed on OS such as openEuler using yum package manager

KubeEdge now supports compiled into rpm package and installed on OS such as openEuler using yum package manager.

Refer to the links for more details.
([#3089](https://github.com/kubeedge/kubeedge/pull/3089), [#3171](https://github.com/kubeedge/kubeedge/pull/3171))



In addition to the above new features, KubeEdge v1.9 also includes the following enhancements:

- Rpminstaller: add support for openEuler ([#3089](https://github.com/kubeedge/kubeedge/pull/3089))

- Replaced 'kubeedge/pause' with multi arch image ([#3114](https://github.com/kubeedge/kubeedge/pull/3114))

- Make meta server addr configurable ([#3119](https://github.com/kubeedge/kubeedge/pull/3119))

- Added iptables to Dockerfile and made cloudcore privileged ([#3129](https://github.com/kubeedge/kubeedge/pull/3129))

- Added CustomInterfaceEnabled and CustomInterfaceName for edgecore ([#3130](https://github.com/kubeedge/kubeedge/pull/3130))

- Add experimental feature ([#3131](https://github.com/kubeedge/kubeedge/pull/3131))

- Feat(edge): node ephemeral storage info ([#3157](https://github.com/kubeedge/kubeedge/pull/3157))

- Support envFrom configmap in edge pods ([#3176](https://github.com/kubeedge/kubeedge/pull/3176))

- Update golang to 1.16 ([#3190](https://github.com/kubeedge/kubeedge/pull/3190))

- Metaserver: support shutdown server graceful  ([#3239](https://github.com/kubeedge/kubeedge/pull/3239))

- Support labelselector for metaserver ([#3262](https://github.com/kubeedge/kubeedge/pull/3262))


## **Future Outlook**

With the release of v1.9, KubeEdge supports custom HTTP request routing from Edge to Cloud through ServiceBus for applications,
supports CloudCore running independently of the Kubernetes Master host, supports containerized deployment of CloudCore using Helm,
supports tls and encryption security and the ease of use of EdgeMesh. 
Thanks to Huawei, China Unicom, DaoCloud, Zhejiang University SEL Lab, ARM and other organizations for their contributions,
as well as all community contributors for their support!

The community plans to further improve the user experience and the stability of KubeEdge in subsequent versions and 
create the best “open source” intelligent edge computing platform for everyone to freely use.

For more details regarding KubeEdge, please follow and join us here:

https://kubeedge.io
