# Fluxcloud

Fluxcloud is a tool to receive events from the [Weave flux](https://github.com/weaveworks/flux).

Fluxcloud is a valid upstream for Weave, allowing you to send Flux events to Slack or a
webhook without using Weave Cloud.

## Introduction

This chart bootstraps a [Flux](https://github.com/justinbarrick/fluxcloud) deployment on
a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager.

## Installation

I assume if you got here you have already installed at least Flux using Helm. This is of course very similar (and simpler).


### Installing the Chart

```sh
helm install incubator/fluxcloud
```

### Configuration

The following configuration values are defaults that can be modified:

```yaml
replicaCount: 1

imageRepository: justinbarrick/fluxcloud
imageTag: v0.3.4
imagePullPolicy: IfNotPresent

servicePort: 80
serviceTargetPort: 3032

extraEnvs: []
#extraEnvs:
#- name: SLACK_URL
#  value: "https://hooks.slack.com/services/WEBHOOK_URL"
#- name: SLACK_CHANNEL
#  value: "#kubernetes" # Or multiple channels (comma separated <channel>=<namespace>). e.g.: value: "#kubernetes=*,#team=team"
#- name: SLACK_USERNAME
#  value: Flux Deployer
#- name: SLACK_ICON_EMOJI
#  value: ":heart:"
#- name: GITHUB_URL
#  value: "https://github.com/justinbarrick/fluxcloud/"
#- name: LISTEN_ADDRESS
#  value: ":3032"
```

For the available environment variables check the [Fluxcloud documentation]((https://github.com/justinbarrick/fluxcloud))