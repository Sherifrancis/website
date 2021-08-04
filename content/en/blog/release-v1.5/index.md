---
authors:
- Kevin Wang
- Fei Xu
categories:
- General
- Announcements
date: 2020-11-16
draft: false
lastmod: 2020-11-16
summary: KubeEdge v1.5 is live!
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
- release v1.5
- v1.5
title: KubeEdge v1.5 is live!
---
**KubeEdge** is an open source system extending native containerized application orchestration and device management to hosts at the Edge. It is built upon Kubernetes and provides core infrastructure support for networking, application deployment and metadata synchronization between cloud and edge. It also supports MQTT and allows developers to author custom logic and enable resource constrained device communication at the Edge.

## **KubeEdge v1.5: A major upgrade for maintainability and edge devices management**

On 16th November, the KubeEdge community is proud to announce the availability of KubeEdge 1.5. This release includes a major upgrade for maintainability and edge devices management, which includes:

- Simplified Device Mapper reference architecture

- Modbus Mapper Golang Implementation

- Support Remote Exec to Pods on Edge From Cloud

- Support Keadm Debug Command for Trouble Shooting On Edge Nodes

- Kubernetes Dependencies Upgrade

- 23+ bug fixes and enhancements.

Please refer to https://github.com/kubeedge/kubeedge/blob/master/CHANGELOG/CHANGELOG-1.5.md for a full list of features in this release

{{% alert note %}}
Release details - [Release v1.5](https://github.com/kubeedge/kubeedge/releases/tag/v1.5.0)
{{% /alert %}}

{{% alert note %}}
How to set up KubeEdge - [KubeEdge Setup](https://kubeedge.io/en/docs/setup/keadm/)
{{% /alert %}}

## **Release Highlights**

### Simplified Device Mapper reference architecture

New version of Mapper reference architecture:

- Simplified Mapper code structure
- Extracted common code into SDK
- Added new building blocks: Configmap parser, Driver, Event process, Timer

Users are now able to develop mappers based on the new design standard.([#2147](https://github.com/kubeedge/kubeedge/pull/2147)).

### Modbus Mapper Golang Implementation

A new modbus mapper with Golang implementation is provided, based on new Device Mapper Standard. ([#2282](https://github.com/kubeedge/kubeedge/pull/2282)).

### Support Remote Exec to Pods on Edge From Cloud

Users are now able to use `K8s exec api` or `kubectl exec` command to connect to pods on the edge node. ([#2075](https://github.com/kubeedge/kubeedge/pull/2075)).

### Support Keadm Debug Command for Trouble Shooting On Edge Nodes

A set of keadm debug subcommands are added for Trouble Shooting On Edge Nodes.
Users are now able to use `keadm debug get` and `keadm debug collect` to get/collect KubeEdge local data for trouble shooting,
and use `keadm debug check` and `keadm debug diagnose` to check local environment configuration. ([#1939](https://github.com/kubeedge/kubeedge/pull/1939))

### Kubernetes Dependencies Upgrade

Upgrade the vendered kubernetes version to v1.19.3, users now can use the feature of new version
on the cloud and on the edge side. ([#2223](https://github.com/kubeedge/kubeedge/pull/2223))

## **Future Outlook**

With the release of v1.5, KubeEdge provides more complete device mapper, support for remote exec from Cloud to Pods on Edge, a more friendly user experience, and a more friendly community contributor experience. Thanks to Huawei, China Unicom, Zhejiang University SEL Lab, ARM and other organizations for their contributions, as well as all community contributors for their support!

The community plans to further improve the user experience and the stability of KubeEdge in subsequent versions and create the best “open source” intelligent edge computing platform for everyone to freely use.

For more details regarding KubeEdge, please follow and join us here:

[https://kubeedge.io](https://kubeedge.io)
