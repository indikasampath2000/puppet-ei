# WSO2 Enterprise Integrator Pattern-7

![pattern-design](../../../../../patterns/design/wso2ei-6.1.1-pattern-7.png)

This pattern consists of Business process profile cluster deployment. There are two nodes and wka (Well-Known-Address) membership scheme used in Hazelcast. You can change it to aws if deployment in EC2. The artifacts synchronization is done through Rsync. A load balancer used to distribute the traffic.

Please follow the basic instructions in this [README](../../../../../README.md) before following this guide.

Content of /opt/deployment.conf file should be similar to below to run the agent and setup this pattern in Puppet Agent.

## deployment.conf file

```yaml
product_name=wso2ei
product_version=6.1.1
product_profile=<hiera_file_name_without_extension>
environment=dev
vm_type=openstack
use_hieradata=true
platform=default
pattern=pattern-7

```

Ex: To setup first Business process profile node

```yaml
product_name=wso2ei
product_version=6.1.1
product_profile=business-process1
environment=dev
vm_type=openstack
use_hieradata=true
platform=default
pattern=pattern-7

```
