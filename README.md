# PostgreSQL  Package 

PostgreSQL (Postgres) is an open source object-relational database known for reliability and data integrity. ACID-compliant, it supports foreign keys, joins, views, triggers and stored procedures.

## Configuration Reference

You can configure the following:

### PostgreSQL common paramerers 

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|image.pullPolicy|PostgreSQL image pull policy|string|IfNotPresent|
|containerPorts.postgresql|PostgreSQL|container|port|integer|5432|
|auth.postgresPassword|Password for the 'postgres' admin user|string|PHVHdqzrMb9s|
|auth.password	Password| for the custom user to create|string|KjMfdzcjkp3K|
|auth.replicationPassword|Password for the replication user|string|zTqmtcf7CqLc|

### PostgreSQL Primary parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|primary.livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|30|
|primary.livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|10|
|primary.livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe|integer|5|
|primary.livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|6|
|primary.livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
primary.readinessProbe.initialDelaySeconds	Initial delay seconds for readinessProbe|integer|5|
primary.readinessProbe.periodSeconds	Period seconds for readinessProbe|integer|10|
primary.readinessProbe.timeoutSeconds	Timeout seconds for readinessProbe|integer|5|
primary.readinessProbe.failureThreshold	Failure threshold for readinessProbe|integer|6|
primary.readinessProbe.successThreshold	Success threshold for readinessProbe|integer|1|
primary.podSecurityContext.enabled|Enable security context|integer|TRUE|
|primary.podSecurityContext.fsGroup|Group ID for the pod|integer|1001|
|primary.containerSecurityContext.runAsUser|primary.containerSecurityContext.runAsUser|integer|1001|
|containerPort|PostgreSQL Prometheus Exporter service port|integer|9187|
|service.ports|PostgreSQL Prometheus Exporter service port	integer|9187|
|primary.persistence.size|PVC Storage Request for PostgreSQL volume|integer|8Gi|
|Secret.auth.postgresPassword|Password for the "postgres" admin user|string|mypassword|

### Volume Permissions parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|volumePermissions.enabled|Enable init container that changes the owner and group of the persistent volume|string|FALSE|
|volumePermissions.image.pullPolicy|Init container volume-permissions image pull policy|string|IfNotPresent|
|volumePermissions.containerSecurityContext.runAsUser|User ID for the init container|integer|0|

