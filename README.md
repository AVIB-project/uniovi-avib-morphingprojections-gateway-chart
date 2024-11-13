# Description

A Chart project for uniovi-avib-morphingprojections-gateway microservice

# Deploye steps

**STEP01**: create a helm chart projection

```
$ helm create uniovi-avib-morphingprojections-gateway-chart
```

**STEP02**: build chart package

This command will generate zip file locally with our chart configuration. The name depends on the  chart name and version configured

```
$ helm package .
```

**STEP03**: publish chart package in Azure Container Registry

This command will publish our chart package inside our ACR repository

```
$ helm push uniovi-avib-morphingprojections-gateway-chart-1.0.0.tgz oci://avibdocker.azurecr.io/helm
```
