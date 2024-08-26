# littlelink-server

![Version: 1.0.1](https://img.shields.io/badge/Version-1.0.1-informational?style=flat-square) ![AppVersion: 1.0.0](https://img.shields.io/badge/AppVersion-1.0.0-informational?style=flat-square)

Helm Chart for LittleLink - personal link aggregator.

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| hiimluck3r | <luck3rinc@yandex.ru> | <https://github.com/hiimluck3r> |

## Source Code

* <https://github.com/techno-tim/littlelink-server>
* <https://github.com/sethcottle/littlelink>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | list | `[]` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `4` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPU | string | `""` |  |
| autoscaling.targetMemory | string | `""` |  |
| env | object | `{"AVATAR_2X_URL":"https://i.natgeofe.com/n/548467d8-c5f1-4551-9f58-6817a8d2c45e/NationalGeographic_2572187_square.jpg","AVATAR_ALT":"cat pic","AVATAR_URL":"https://i.natgeofe.com/n/548467d8-c5f1-4551-9f58-6817a8d2c45e/NationalGeographic_2572187_square.jpg","BIO":"Just a cat","BUTTON_ORDER":"YOUTUBE,EMAIL,EMAIL_ALT,TWITCH,TELEGRAM,TWITTER,GITHUB,INSTAGRAM,LINKED_IN,DISCORD,FACEBOOK,TIKTOK,PATREON,GEAR,DOCUMENTATION,STEAM,SPOTIFY,REDDIT","FAVICON_URL":"https://i.natgeofe.com/n/548467d8-c5f1-4551-9f58-6817a8d2c45e/NationalGeographic_2572187_square.jpg","FOOTER":"h2m © 2024","GA_TRACKING_ID":"GXXXXXXXXXX","LANG":"en","META_AUTHOR":"hiimluck3r","META_DESCRIPTION":"Example of meta description for h2m","META_INDEX_STATUS":"all","META_KEYWORDS":"HomeLab, Kubernetes, Helm, Automation","META_TITLE":"h2m","NAME":"Random Cat","OG_DESCRIPTION":"example of description","OG_IMAGE":"https://i.natgeofe.com/n/548467d8-c5f1-4551-9f58-6817a8d2c45e/NationalGeographic_2572187_square.jpg","OG_IMAGE_HEIGHT":400,"OG_IMAGE_WIDTH":400,"OG_SITE_NAME":"h2m","OG_TITLE":"h2m","OG_URL":"https://thebroadband.ru","THEME":"Dark","TZ":"Europe/Moscow"}` | You can find more at https://github.com/techno-tim/littlelink-server |
| fullnameOverride | string | `""` |  |
| httpRoute.annotations | object | `{}` | HTTPRoute annotations. |
| httpRoute.enabled | bool | `false` | HTTPRoute enabled. |
| httpRoute.hostnames | list | `["littlelink.local"]` | Hostnames matching HTTP header. |
| httpRoute.parentRefs | list | `[{"group":"gateway.networking.k8s.io","name":"cilium","namespace":"kube-system"}]` | Which Gateways this Route is attached to |
| httpRoute.rules | list | `[{"matches":[{"path":{"type":"PathPrefix","value":"/"}}]}]` | List of rules and filters applied. |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.registry | string | `"ghcr.io"` |  |
| image.repository | string | `"techno-tim/littlelink-server"` |  |
| image.tag | string | `"latest"` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"littlelink.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `6` |  |
| livenessProbe.httpGet.path | string | `"/healthcheck"` |  |
| livenessProbe.httpGet.port | string | `"http"` |  |
| livenessProbe.periodSeconds | int | `5` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `1` |  |
| nameOverride | string | `""` |  |
| nodeSelector."kubernetes.io/os" | string | `"linux"` |  |
| readinessProbe.enabled | bool | `true` |  |
| readinessProbe.failureThreshold | int | `3` |  |
| readinessProbe.httpGet.path | string | `"/healthcheck"` |  |
| readinessProbe.httpGet.port | string | `"http"` |  |
| readinessProbe.periodSeconds | int | `5` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `1` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| service.clusterIP | string | `""` |  |
| service.externalTrafficPolicy | string | `"Cluster"` |  |
| service.loadBalancerIP | string | `""` |  |
| service.port | int | `3000` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | If not set and create is true, a name is generated using the fullname template |
| startupProbe.enabled | bool | `true` |  |
| startupProbe.failureThreshold | int | `30` |  |
| startupProbe.httpGet.path | string | `"/healthcheck"` |  |
| startupProbe.httpGet.port | string | `"http"` |  |
| startupProbe.periodSeconds | int | `10` |  |
| startupProbe.successThreshold | int | `1` |  |
| startupProbe.timeoutSeconds | int | `1` |  |
| strategy.rollingUpdate.maxSurge | int | `1` |  |
| strategy.rollingUpdate.maxUnavailable | int | `1` |  |
| strategy.type | string | `"RollingUpdate"` |  |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)
