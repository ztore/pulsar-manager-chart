# Pulsar Manager helm chart
Helm chart for [pulsar-manager](https://github.com/apache/pulsar-manager).

## Description

Apache Pulsar manager is a web-based GUI management tool for managing and monitoring Pulsar [open sourced by StreamNative and contributed to ASF as a part of Apache Pulsar](https://medium.com/streamnative/pulsar-manager-open-source-f2bd1e64d3b2).

## Deployment

After you have set the configuration of helm, like Tiller, you may execute `helm install` to deploy it:

```
git clone https://github.com/ztore/pulsar-manager-chart.git
cd pulsar-manager
helm install --values manager/values.yaml ./manager
```

## Configuration in [templates/manager-configmap.yaml](templates/manager-configmap.yaml)

 ENV Variable      | Description                                                                             |
------------------ | --------------------------------------------------------------------------------------- |
 REDIRECT_HOST     | the IP address of the front-end server.                                                 |
 REDIRECT_PORT     | the port of the front-end server.                                                       |
 DRIVER_CLASS_NAME | the driver class name of MySQL.                                                         |
 URL               | the url of MySQL jdbc, example: jdbc:mysql://localhost:3306/pulsar_manager?useSSL=false |
 USERNAME          | the username of MySQL                                                                   |
 PASSWORD          | the password of MySQL                                                                   |

For further details, you may refer to the related sources.

## Related Sources

Github repo: [apache/pulsar](https://github.com/apache/pulsar)  
Guthub repo: [apache/pulsar-manager](https://github.com/apache/pulsar-manager)  
Docker image: [streamnative/pulsar-manager](https://hub.docker.com/r/streamnative/pulsar-manager)  
