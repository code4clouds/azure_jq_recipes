# Description
These are some of the common jq queries used in Azure

# Background

# Manual

There is a good manual about who to use jq [here](https://stedolan.github.io/jq/manual/).

# Setup

``` bash
apt install jq
```
# Usages

## Volumes

### Get all the volumes in your subscription of an specific size

``` bash
az disk list | jq 'map(select(.diskSizeGb == 20))'
```

## AKS

### Get status of an AKS deployment (with watch)

``` bash
az aks list | jq 'map(.provisioningState)'
```
