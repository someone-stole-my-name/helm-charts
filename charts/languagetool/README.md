# languagetool

![Version: 0.1.4](https://img.shields.io/badge/Version-0.1.4-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 5.6](https://img.shields.io/badge/AppVersion-5.6-informational?style=flat-square)

Open Source proofreading software for English, French, German, Polish, and more than 20 other languages.

**Homepage:** <https://languagetool.org/>

## Source Code

* <https://github.com/someone-stole-my-name/helm-charts>
* <https://github.com/someone-stole-my-name/docker-languagetool>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `2` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| extraOptions | string | `""` | Extra options for languagetool itself. |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"ghcr.io/someone-stole-my-name/docker-languagetool"` |  |
| image.tag | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"ImplementationSpecific"` |  |
| ingress.tls | list | `[]` |  |
| javaOptions | string | `""` | Extra options for JVM. eg: -Xmx3G -Xms3G |
| nameOverride | string | `""` |  |
| ngram | object | `{"enabled":false,"languages":["en"],"persistence":{"accessMode":"ReadWriteMany","size":"10Gi","storageClass":"default"}}` | Downloads the specified languages from https://languagetool.org/download/ngram-data/ to a local disk and appends "--languageModel ..." to extraOptions. Ideally the storageClass or  existingClaim should be as fast as possible. |
| ngram.languages | list | `["en"]` | The list of languages to download. |
| ngram.languages[0] | string | `"en"` | > ~16GB as of 02/2022 |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| probeOptions | object | `{"livenessProbeOptions":{"initialDelaySeconds":600},"readinessProbeOptions":{}}` | Configure additional probe options. |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |

