# agola

![Version: 0.5.0](https://img.shields.io/badge/Version-0.5.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v0.8.0](https://img.shields.io/badge/AppVersion-v0.8.0-informational?style=flat-square)

A Helm chart for Agola

**Homepage:** <https://agola.io/>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| babykart | <babykart@gmail.com> | <https://github.com/babykart> |

## Source Code

* <https://github.com/agola-io/agola.git>
* <https://github.com/agola-io/agola-web.git>

## Requirements

Kubernetes: `>=1.19.0-0`

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| config.annotations | object | `{}` | Config annotations |
| config.apiExposedURL | string | `"http://agola.example.net"` | Config API Exposed URL |
| config.file | object | `{"configstore":{"dataDir":"/agola/local/configstore","db":{"connString":"postgres://agola:password@postgres:5432/configstore?sslmode=disable","type":"postgres"},"objectStorage":{"accessKey":"minio","bucket":"configstore","endpoint":"http://minio-service:9000","location":"us-east-1","secretAccessKey":"minio123","type":"s3"},"web":{"listenAddress":":4002"}},"executor":{"activeTasksLimit":2,"allowPrivilegedContainers":false,"dataDir":"/agola/local/executor","driver":{"type":"kubernetes"},"initImage":{"image":"busybox:stable"},"runserviceURL":"http://agola-runservice:4000","toolboxPath":"./bin","web":{"listenAddress":":4001"}},"gateway":{"adminToken":"MyComplexAdminToken","apiExposedURL":"http://agola.example.net","configstoreURL":"http://agola-configstore:4002","cookieSigning":{"key":"deadbeefcafeaa"},"gitserverURL":"http://agola-gitserver:4003","runserviceURL":"http://agola-runservice:4000","tokenSigning":{"key":"cafedeadbeefbb","method":"hmac"},"unsecureCookies":true,"web":{"listenAddress":":8000"},"webExposedURL":"http://agola.example.net"},"gitserver":{"dataDir":"/agola/local/gitserver","gatewayURL":"http://agola-gateway:8000","web":{"listenAddress":":4003"}},"notification":{"configstoreURL":"http://agola-configstore:4002","db":{"connString":"postgres://agola:password@postgres:5432/notification?sslmode=disable","type":"postgres"},"runserviceURL":"http://agola-runservice:4000","webExposedURL":"http://agola.example.net"},"runservice":{"dataDir":"/agola/local/runservice","db":{"connString":"postgres://agola:password@postgres:5432/runservice?sslmode=disable","type":"postgres"},"debug":false,"objectStorage":{"accessKey":"minio","bucket":"runservice","endpoint":"http://minio-service:9000","location":"us-east-1","secretAccessKey":"minio123","type":"s3"},"web":{"listenAddress":":4000"}},"scheduler":{"runserviceURL":"http://agola-runservice:4000"}}` | Content of the config.yml file that will be stored in a secret |
| config.labels | object | `{}` | Config labels |
| config.localBaseDir | string | `"/agola/local"` | Config local base directory |
| config.webExposedURL | string | `"http://agola.example.net"` | Config Web Exposed URL |
| configstore.affinity | object | `{}` | Configstore Affinity |
| configstore.deployment.annotations | object | `{}` | Configstore Annotations for the deployment |
| configstore.deployment.labels | object | `{}` | Configstore Labels for the deployment |
| configstore.deployment.replicas | int | `2` | Configstore number of replicas for the replicaSet |
| configstore.deployment.revisionHistoryLimit | int | `5` | The maximum number of revisions that will be maintained in the replicaSet's revision history. Default is 10. |
| configstore.dnsConfig | object | `{}` | Configstore Overrides default DNS config |
| configstore.extraContainers | list | `[]` | Configstore extra containers. |
| configstore.extraVolumes | list | `[]` | Configstore extra volumes |
| configstore.initContainers | list | `[]` | Configstore initContainers |
| configstore.nodeSelector | object | `{}` | Configstore Node selector labels |
| configstore.podAnnotations | object | `{}` | Configstore Pod annotations |
| configstore.podSecurityContext | object | `{}` | Configstore Pod security context |
| configstore.resources | object | `{}` | Configstore Resources |
| configstore.securityContext | object | `{}` | Configstore Security context |
| configstore.service.port | int | `4002` | The port of the service |
| configstore.service.type | string | `"ClusterIP"` | Configstore type of the service |
| configstore.tolerations | list | `[]` | Configstore Tolerations |
| configstore.updateStrategy.type | string | `"RollingUpdate"` | The type of the update strategy for the deployment |
| executor.affinity | object | `{}` | Executor Affinity |
| executor.deployment.annotations | object | `{}` | Executor Annotations for the deployment |
| executor.deployment.labels | object | `{}` | Executor Labels for the deployment |
| executor.deployment.replicas | int | `2` | Executor number of replicas for the replicaSet |
| executor.deployment.revisionHistoryLimit | int | `5` | The maximum number of revisions that will be maintained in the replicaSet's revision history. Default is 10. |
| executor.dnsConfig | object | `{}` | Executor Overrides default DNS config |
| executor.extraContainers | list | `[]` | Executor extra containers. |
| executor.extraVolumes | list | `[]` | Executor extra volumes |
| executor.initContainers | list | `[]` | Executor initContainers |
| executor.nodeSelector | object | `{}` | Executor Node selector labels |
| executor.podAnnotations | object | `{}` | Executor Pod annotations |
| executor.podSecurityContext | object | `{}` | Executor Pod security context |
| executor.resources | object | `{}` | Executor Resources |
| executor.securityContext | object | `{}` | Executor Security context |
| executor.service.port | int | `4001` | The port of the service |
| executor.service.type | string | `"ClusterIP"` | Executor type of the service |
| executor.tolerations | list | `[]` | Executor Tolerations |
| executor.updateStrategy.type | string | `"RollingUpdate"` | The type of the update strategy for the deployment |
| fullnameOverride | string | `""` | Overrides the full name of the helm chart |
| gateway.affinity | object | `{}` | Gateway Affinity |
| gateway.deployment.annotations | object | `{}` | Gateway Annotations for the deployment |
| gateway.deployment.labels | object | `{}` | Gateway Labels for the deployment |
| gateway.deployment.replicas | int | `2` | Gateway number of replicas for the replicaSet |
| gateway.deployment.revisionHistoryLimit | int | `5` | The maximum number of revisions that will be maintained in the replicaSet's revision history. Default is 10. |
| gateway.dnsConfig | object | `{}` | Gateway Overrides default DNS config |
| gateway.extraContainers | list | `[]` | Gateway extra containers. |
| gateway.extraVolumes | list | `[]` | Gateway extra volumes |
| gateway.initContainers | list | `[]` | Gateway initContainers |
| gateway.nodeSelector | object | `{}` | Gateway Node selector labels |
| gateway.podAnnotations | object | `{}` | Gateway Pod annotations |
| gateway.podSecurityContext | object | `{}` | Gateway Pod security context |
| gateway.resources | object | `{}` | Gateway Resources |
| gateway.securityContext | object | `{}` | Gateway Security context |
| gateway.service.port | int | `8000` | The port of the service |
| gateway.service.type | string | `"ClusterIP"` | Gateway type of the service |
| gateway.tolerations | list | `[]` | Gateway Tolerations |
| gateway.updateStrategy.type | string | `"RollingUpdate"` | The type of the update strategy for the deployment |
| gitserver.affinity | object | `{}` | Gitserver Affinity |
| gitserver.dnsConfig | object | `{}` | Gitserver Overrides default DNS config |
| gitserver.extraContainers | list | `[]` | Gitserver extra containers. |
| gitserver.extraVolumes | list | `[]` | Gitserver extra volumes |
| gitserver.initContainers | list | `[]` | Gitserver initContainers |
| gitserver.nodeSelector | object | `{}` | Gitserver Node selector labels |
| gitserver.persistence.enabled | bool | `false` | Gitserver persistence enabled |
| gitserver.persistence.requestsStorage | string | `"1Gi"` | Gitserver persistence requests storage |
| gitserver.persistence.storageClassName | string | `""` | Gitserver persistence storageClassName |
| gitserver.podAnnotations | object | `{}` | Gitserver Pod annotations |
| gitserver.podSecurityContext | object | `{}` | Gitserver Pod security context |
| gitserver.resources | object | `{}` | Gitserver Resources |
| gitserver.securityContext | object | `{}` | Gitserver Security context |
| gitserver.service.port | int | `4001` | The port of the service |
| gitserver.service.type | string | `"ClusterIP"` | Gitserver type of the service |
| gitserver.statefulSet.annotations | object | `{}` | Gitserver Annotations for the statefulSet |
| gitserver.statefulSet.labels | object | `{}` | Gitserver Labels for the statefulSet |
| gitserver.statefulSet.revisionHistoryLimit | int | `5` | The maximum number of revisions that will be maintained in the statefulSet's revision history. Default is 10. |
| gitserver.tolerations | list | `[]` | Gitserver Tolerations |
| gitserver.updateStrategy.type | string | `"RollingUpdate"` | The type of the update strategy for the statefulSet |
| image.pullPolicy | string | `"IfNotPresent"` | Overrides the image pull policy |
| image.registry | string | `"docker.io"` | Overrides the image registry |
| image.repository | string | `"sorintlab/agola"` | Overrides the image repository |
| image.tag | string | `""` | Overrides the image tag whose default is the chart appVersion. |
| imagePullSecrets | list | `[]` | Defines imagePullSecrets |
| ingress.annotations | string | `nil` | Ingress annotations |
| ingress.enabled | bool | `false` | Ingress enabled |
| ingress.hosts[0].host | string | `"agola.example.net"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.ingressClassName | string | `""` | Defines which ingress controller will implement the resource |
| ingress.tls | list | `[]` |  |
| nameOverride | string | `""` | Overrides the name of the helm chart |
| runservice.affinity | object | `{}` | Runservice Affinity |
| runservice.deployment.annotations | object | `{}` | Runservice Annotations for the deployment |
| runservice.deployment.labels | object | `{}` | Runservice Labels for the deployment |
| runservice.deployment.replicas | int | `2` | Runservice number of replicas for the replicaSet |
| runservice.deployment.revisionHistoryLimit | int | `5` | The maximum number of revisions that will be maintained in the replicaSet's revision history. Default is 10. |
| runservice.dnsConfig | object | `{}` | Runservice Overrides default DNS config |
| runservice.extraContainers | list | `[]` | Runservice extra containers. |
| runservice.extraVolumes | list | `[]` | Runservice extra volumes |
| runservice.initContainers | list | `[]` | Runservice initContainers |
| runservice.nodeSelector | object | `{}` | Runservice Node selector labels |
| runservice.podAnnotations | object | `{}` | Runservice Pod annotations |
| runservice.podSecurityContext | object | `{}` | Runservice Pod security context |
| runservice.resources | object | `{}` | Runservice Resources |
| runservice.securityContext | object | `{}` | Runservice Security context |
| runservice.service.port | int | `4000` | The port of the service |
| runservice.service.type | string | `"ClusterIP"` | Runservice type of the service |
| runservice.tolerations | list | `[]` | Runservice Tolerations |
| runservice.updateStrategy.type | string | `"RollingUpdate"` | The type of the update strategy for the deployment |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | The name of the service account to use. If not set and create is true, a name is generated using the fullname template |
| serviceAccount.rbac.create | bool | `true` | Only change this if you have a non CNCF compliant cluster, missing the RBAC endpoints the Role and RoleBinding are only created if serviceAccount.create is also true |
| serviceAccount.rbac.role | object | `{"annotations":{},"labels":{}}` | additional annotations and labels in role and roleBinding are only needed, if you are using additional tooling to manage / verify roles or roleBindings (OPA, etc.) |
| serviceAccount.rbac.role.annotations | object | `{}` | Annotations for the RBAC role |
| serviceAccount.rbac.role.labels | object | `{}` | Labels for the RBAC role |
| serviceAccount.rbac.roleBinding.annotations | object | `{}` | Annotations for the RBAC roleBinding |
| serviceAccount.rbac.roleBinding.labels | object | `{}` | Labels for the RBAC roleBinding |
| serviceAccount.token | bool | `false` | Creates the token object |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
