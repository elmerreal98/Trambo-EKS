# EKS - Cluster
To define the eks cluster i use the tool eksctl

## Cluster.yml File
This file contains the following blocks
1. apiVersion
Indicates the version of the config file
2. Kind
In this case this file is ClusterConfig because i want to define a cluster.
3. Metadata
Information about my cluster.
4. NodeGroups:
Defining the number of instances that eks will create, and some parametres that could be used for elasticity.
```
nodeGroups:
  - name: ng-1
    instanceType: t2.micro
    minSize: 2
    desiredCapacity: 2
    maxSize: 2
```