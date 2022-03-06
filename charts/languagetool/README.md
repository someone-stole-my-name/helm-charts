# languagetool

![Version: 0.1.3](https://img.shields.io/badge/Version-0.1.3-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 5.6](https://img.shields.io/badge/AppVersion-5.6-informational?style=flat-square)

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
| extraOptions | string | `""` |  |
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
| javaOptions | string | `""` |  |
| nameOverride | string | `""` |  |
| ngram.enabled | bool | `false` |  |
| ngram.languages[0] | string | `"en"` |  |
| ngram.persistence.accessMode | string | `"ReadWriteMany"` |  |
| ngram.persistence.size | string | `"10Gi"` |  |
| ngram.persistence.storageClass | string | `"default"` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| probeOptions.livenessProbeOptions.initialDelaySeconds | int | `600` |  |
| probeOptions.readinessProbeOptions | object | `{}` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| securityContext.capabilities.add[0] | string | `"MKNOD"` |  |
| securityContext.capabilities.add[1] | string | `"SYS_CHROOT"` |  |
| securityContext.capabilities.add[2] | string | `"CHOWN"` |  |
| securityContext.capabilities.add[3] | string | `"DAC_OVERRIDE"` |  |
| securityContext.capabilities.add[4] | string | `"FOWNER"` |  |
| securityContext.capabilities.drop[0] | string | `"ALL"` |  |
| securityContext.runAsNonRoot | bool | `true` |  |
| securityContext.runAsUser | int | `65534` |  |
| service.port | int | `80` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
