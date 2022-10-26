# main-chart

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling | object | `{"enabled":false,"maxReplicas":100,"minReplicas":1,"targetCPUUtilizationPercentage":80}` | add autoscaling Custom metrics names can befound at `kubectl get --raw "/apis/external.metrics.k8s.io/v1beta1/" |jq` and if needed to add helm/argo/infra/prometheus-adapter.yaml |
| configmap | object | `{"annotations":{},"enabled":true,"load_default_application_properties":true}` | add configmap |
| containerCommand | string | `nil` | Add a custom command to run on main container Example (run echo "Hello World"): containerCommand:   - "echo"   - "Hello World" |
| cronjob.concurrencyPolicy | string | `"Replace"` |  |
| cronjob.failedJobsHistoryLimit | int | `5` |  |
| cronjob.jobs | string | `nil` |  |
| cronjob.restartPolicy | string | `"OnFailure"` |  |
| cronjob.successfulJobsHistoryLimit | int | `5` |  |
| deployment.enabled | bool | `true` |  |
| env | object | `{}` | add env variables |
| externalsecrets | object | `{"enabled":false,"path":"/usr/src/app/config/application-kamus.properties"}` | add support for external secrets  enabled: true   secrets:     - staging-mysql-storeconfig: storeconfig-db-password |
| extraObjects | list | `[]` | Create a dynamic manifests via values: |
| extraVolumeMounts | list | `[]` |  |
| extraVolumesProperties | list | `[]` |  |
| fullName | string | `""` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"Always"` |  |
| image.repository | string | `"nginx"` |  |
| image.tag | string | `"latest"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].extra_paths | list | `[]` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths | list | `[]` |  |
| ingress.pathType | string | `"Prefix"` |  |
| ingress.service_port | int | `80` |  |
| ingress.tls | list | `[]` |  |
| ingress_alb.annotations | object | `{}` |  |
| ingress_alb.enabled | bool | `false` |  |
| ingress_alb.hosts[0].extra_paths | list | `[]` |  |
| ingress_alb.hosts[0].host | string | `"chart-example.local"` |  |
| ingress_alb.hosts[0].paths | list | `[]` |  |
| ingress_alb.pathType | string | `"Prefix"` |  |
| ingress_alb.service_port | int | `80` |  |
| ingress_alb.tls | list | `[]` |  |
| initContainers | object | `{"command":null,"enabled":false,"repository":{"custom":false,"image":null,"tag":null}}` | Add a initContainers and specify the command to run Example (run echo "Hello World"):  enabled: true  command:   - "echo"   - "Hello World" |
| job.Annotations | string | `nil` |  |
| job.containerCommand | string | `nil` |  |
| job.enabled | bool | `false` |  |
| job.image.repository | string | `"nginx"` |  |
| job.image.tag | string | `"latest"` |  |
| job.resources | object | `{}` |  |
| labels | string | `nil` |  |
| livenessProbe.failureThreshold | int | `3` |  |
| livenessProbe.httpGet.path | string | `"/health"` |  |
| livenessProbe.httpGet.port | int | `8082` |  |
| livenessProbe.httpGet.scheme | string | `"HTTP"` |  |
| livenessProbe.initialDelaySeconds | int | `300` |  |
| livenessProbe.periodSeconds | int | `30` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `1` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext | object | `{}` |  |
| propertiesEnvName | string | `nil` |  |
| readinessProbe.failureThreshold | int | `3` |  |
| readinessProbe.httpGet.path | string | `"/health"` |  |
| readinessProbe.httpGet.port | int | `8082` |  |
| readinessProbe.httpGet.scheme | string | `"HTTP"` |  |
| readinessProbe.initialDelaySeconds | int | `10` |  |
| readinessProbe.periodSeconds | int | `10` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `1` |  |
| replicaCount | int | `1` |  |
| resources | object | `{}` |  |
| revisionHistoryLimit | int | `0` |  |
| securityContext | object | `{}` |  |
| service.enabled | bool | `true` |  |
| service.healthcheck_path | string | `nil` |  |
| service.ports | list | `[]` |  |
| service.sessionAffinity | string | `nil` |  |
| service.startupProbe.enabled | bool | `false` |  |
| service.type | string | `"ClusterIP"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `""` |  |
| strategy | object | `{"rollingUpdate":{"maxSurge":"25%","maxUnavailable":"25%"}}` | Create a deployment strategy  strategy:    rollingUpdate:      maxUnavailable: 0      maxSurge: 3 |
| teamName | string | `""` |  |
| tolerations | list | `[]` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)
