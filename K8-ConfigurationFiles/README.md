# K8 - Configuration File
The structure for the solution is the following.
```
.
├── configmaps
│   ├── configmap-db.yaml              # in case the database endopoint changes i just have to update this file.
├── deployments
│   ├── deployment-odoo.yaml           # I define the odoo pod template and information about this ERP
│   ├── deployment-postgres.yaml       # I define a pod that contains postgres and adminer (as a sidecar)
├── secrets
│   ├── secrets-db.yaml                # There is where i store all the sensible data like username and password for the database.
├── services
    ├── svc-odoo.yaml                  # It creates a load balancer for the service odoo
    ├── svc-odoo.yaml                  # It creates a ClusterIp for the service postgress and a Nodeport Service for adminer.s


```