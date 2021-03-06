---
title: Supported cluster versions in Azure Service Fabric 
description: Learn about cluster versions in Azure Service Fabric, including a link to the newest releases from the Service Fabric team blog.

ms.topic: troubleshooting
ms.date: 06/15/2020
---
# Supported Service Fabric versions

Make sure your cluster is always running a supported Azure Service Fabric version. A minimum of 60 days after we announce the release of a new version of Service Fabric, support for the previous version ends. You'll find announcements of new releases on the [Service Fabric team blog](https://azure.microsoft.com/updates/?product=service-fabric).

For a given version of the Service Fabric runtime you can use the specified or older versions of the SDK/NuGet packages. Newer versions of the packages are not supported and may have issues targeting older clusters as they may have feature or protocol changes not supported by those environments.

Refer to the following documents for details on how to keep your cluster running a supported Service Fabric version:

- [Upgrade an Azure Service Fabric cluster](service-fabric-cluster-upgrade.md)
- [Upgrade the Service Fabric version that runs on your standalone Windows Server cluster](service-fabric-cluster-upgrade-windows-server.md)


## Unsupported Versions

### Upgrade Alert for versions between 5.7 and below 6.3.63.*
To improve security and availability, Azure infrastructure will make a change that may affect Service Fabric customers. **All Service Fabric clusters on unsupported versions from 5.7 to 6.3. are impacted**. Addressing the change requires an update to the Service Fabric runtime, which is already available for all supported Service Fabric versions in all regions.

We request and recommend taking action to upgrade to the latest supported versions by **Jan 19,2021** to avoid service disruptions 
If you have a support plan and you need technical help, please reach out to us via Azure support channels by opening a support request for Azure Service Fabric and mention this context in the support ticket.

#### Impact If NOT Upgraded to supported versions

**Azure Service Fabric clusters which run on unsupported versions from 5.7 to 6.3.63.\* will not be able to come up and will be unavailable** if you have not upgraded to one of below supported versions by January 19,2021.

#### Required Action
Upgrade to the Service Fabric supported versions listed below to prevent downtime or loss of functionality related to this change. Please ensure that your clusters are running at least these versions to prevent issues in your environment.

  ###### Supported Service Fabric Runtime Versions
   If you are on NOT on the below listed supported versions of Service Fabric, please upgrade to one of these versions which already contain the necessary changes to prevent downtime to cluster. **Note:** All release versions of 7.2 includes the necessary changes.
  
  | OS | Current Service Fabric runtime in the cluster | CU/Patch release  | 
  | --- | --- |--- | 
  | Windows | 7.0.* | 7.0.478.9590 |
  | Windows | 7.1.* | 7.1.503.9590 |
  | Windows | 7.2.* | 7.2.* |
  | Ubuntu 16 | 7.0.* | 7.0.472.1  |
  | Linux Ubuntu 16.04 | 7.1.* | 7.1.455.1  |
  | Linux Ubuntu 18.04 | 7.1.* | 7.1.455.1804 |
  | Linux Ubuntu 16.04 | 7.2.* | 7.2.* |
  | Linux Ubuntu 18.04 | 7.2.* | 7.2.* |
 
### Upgrade Alert for versions greater than 6.3 
To improve security and availability, Azure infrastructure will make a change that may affect Service Fabric customers. **All Service Fabric clusters which use [Open Networking feature for Containers](https://docs.microsoft.com/azure/service-fabric/service-fabric-networking-modes#set-up-open-networking-mode), run on unsupported versions greater than 6.3 and below 7.0 and incompatible supported versions from 7.0 onwards are impacted**. Addressing the change requires an update to the Service Fabric runtime, which is already available for all supported Service Fabric versions in all regions.

 #### Impact If NOT Upgraded to supported versions
  Azure Service Fabric clusters which **use [Open Networking feature for Containers](https://docs.microsoft.com/azure/service-fabric/service-fabric-networking-modes#set-up-open-networking-mode) feature for Containers and runs on versions greater than 6.3** that do not include changes will experience loss of functionality  or service disruptions if NOT upgraded to one of below supported versions by **January 19,2021**.
 
  - **For clusters running a version of Service Fabric greater than 6.3 NOT using Open Networking feature**, the cluster will remain up, however the Open Networking feature for Containers clusters, will cease functioning which could cause service interruptions for your workloads.

 - **For clusters running a version of Service Fabric greater than 6.3 and use [Open Networking feature for Containers](https://docs.microsoft.com/azure/service-fabric/service-fabric-networking-modes#set-up-open-networking-mode)** ,the cluster could become unavailable and will cease functioning which could cause service interruptions for your workloads.
  
#### Required Action
Upgrade to the Service Fabric supported versions listed below to prevent downtime or loss of functionality related to this change. Please ensure that your clusters are running at least these versions to prevent issues in your environment. 
 
 ###### Supported Service Fabric Runtime Versions
 If you are on NOT on the below listed supported versions of Service Fabric, please upgrade to one of these versions which already contain the necessary changes to prevent loss of functionality.  **Note:** All release versions of 7.2 includes the necessary changes.
 
  | OS | Current Service Fabric runtime in the cluster | CU/Patch release  | 
  | --- | --- |--- | 
  | Windows | 7.0.* | 7.0.478.9590 |
  | Windows | 7.1.* | 7.1.503.9590 |
  | Windows | 7.2.* | 7.2.* |
  | Linux Ubuntu 16.04 | 7.0.* | 7.0.472.1  |
  | Linux Ubuntu 16.04 | 7.1.* | 7.1.455.1  |
  | Linux Ubuntu 18.04 | 7.1.* | 7.1.455.1804 |
  | Linux Ubuntu 16.04 | 7.2.* | 7.2.* |
  | Linux Ubuntu 18.04 | 7.2.* | 7.2.* |

## Supported versions
The following table lists the versions of Service Fabric and their support end dates.

| Service Fabric runtime in the cluster | Can upgrade directly from cluster version |Compatible SDK or NuGet package version | End of support |
| --- | --- |--- | --- |
| All cluster versions before 5.3.121 | 5.1.158.* |Less than or equal to version  2.3 |January 20, 2017 |
| 5.3.* | 5.1.158.* |Less than or equal to version  2.3 |February 24, 2017 |
| 5.4.* | 5.1.158.* |Less than or equal to version  2.4 |May 10, 2017       |
| 5.5.* | 5.4.164.* |Less than or equal to version  2.5 |August 10,2017    |
| 5.6.* | 5.4.164.* |Less than or equal to version  2.6 |October 13,2017   |
| 5.7.* | 5.4.164.* |Less than or equal to version  2.7 |December 15, 2017  |
| 6.0.* | 5.6.205.* |Less than or equal to version  2.8 |March 30, 2018     |
| 6.1.* | 5.7.221.* |Less than or equal to version  3.0 |July 15, 2018      |
| 6.2.* | 6.0.232.* |Less than or equal to version  3.1 |October 26, 2018   |
| 6.3.* | 6.1.480.* |Less than or equal to version  3.2 |March 31, 2019  |
| 6.4.* | 6.2.301.* |Less than or equal to version  3.3 |September 15, 2019 |
| 6.5.* | 6.4.617.* |Less than or equal to version  3.4 |August 1, 2020 |
| 7.0.466.* | 6.4.664.* |Less than or equal to version  4.0|January 31, 2021  |
| 7.0.466.* | 6.5.* |Less than or equal to version  4.0|January 31, 2021 |
| 7.0.470.* | 7.0.466.* |Less than or equal to version  4.0 |January 31, 2021  |
| 7.0.472.* | 7.0.466.* |Less than or equal to version  4.0 |January 31, 2021  |
| 7.0.478.* | 7.0.466.* |Less than or equal to version  4.0 |January 31, 2021  |
| 7.1.409.* | 7.0.466.* |Less than or equal to version  4.1 |March 31, 2021 |
| 7.1.417.* | 7.0.466.* |Less than or equal to version  4.1 |March 31, 2021 |
| 7.1.428.* | 7.0.466.* |Less than or equal to version  4.1 |March 31, 2021 |
| 7.1.456.* | 7.0.466.* |Less than or equal to version  4.1 |March 31, 2021 |
| 7.1.458.* | 7.0.466.* |Less than or equal to version  4.1 |March 31, 2021 |
| 7.1.459.* | 7.0.466.* |Less than or equal to version  4.1 |March 31, 2021 |
| 7.1.503.* | 7.0.466.* |Less than or equal to version  4.1 |March 31, 2021 |
| 7.2.413.* | 7.0.470.* |Less than or equal to version  4.2 |Current version, so no end date |
| 7.2.432.* | 7.0.470.* |Less than or equal to version  4.2 |Current version, so no end date |
| 7.2.433.* | 7.0.470.* |Less than or equal to version  4.2 |Current version, so no end date |
| 7.2.445.* | 7.0.470.* |Less than or equal to version  4.2 |Current version, so no end date |

## Supported operating systems

The following table lists the supported operating systems for the supported Service Fabric versions.

| Operating system | Earliest supported Service Fabric version |
| --- | --- |
| Windows Server 2012 R2 | All versions |
| Windows Server 2016 | All versions |
| Windows Server 1709 | 6.0 |
| Windows Server 1803 | 6.4 |
| Windows Server 1809 | 6.4.654.9590 |
| Windows Server 2019 | 6.4.654.9590 |
| Linux Ubuntu 16.04 | 6.0 |
| Linux Ubuntu 18.04 | 7.1 |

## Supported version names

The following table lists the version names of Service Fabric and their corresponding version numbers.

| Version name | Windows version number | Linux version number |
| --- | --- | --- |
| 5.3 RTO |	5.3.121.9494 | NA |
| 5.3 CU1 | 5.3.204.9494 | NA |
| 5.3 CU2 | 5.3.301.9590 | NA |
| 5.3 CU3 | 5.3.311.9590 | NA |
| 5.4 CU2 | 5.4.164.9494 | NA |
| 5.5 CU1 | 5.5.216.0    | NA |
| 5.5 CU2 |	5.5.219.0	 | NA |
| 5.5 CU3 | 5.5.227.0	 | NA |
| 5.5 CU4 | 5.5.232.0 | NA |
| 5.6 RTO |	5.6.204.9494 | NA |
| 5.6 CU2 | 5.6.210.9494 | NA |
| 5.6 CU3 |	5.6.220.9494 | NA |
| 5.7 RTO | 5.7.198.9494 | NA |
| 5.7 CU4 | 5.7.221.9494 | NA |
| 6.0 RTO | 6.0.211.9494 | 6.0.120.1 |
| 6.0 CU1 | 6.0.219.9494 | 6.0.127.1 |
| 6.0 CU2 | 6.0.232.9494 | 6.0.133.1 |
| 6.1 CU1 | 6.1.456.9494 | 6.1.183.1 |
| 6.1 CU2 | 6.1.467.9494 | 6.1.185.1 |
| 6.1 CU3 | 6.1.472.9494 | NA |
| 6.1 CU4 | 6.1.480.9494 | 6.1.187.1 |
| 6.2 RTO | 6.2.269.9494 | 6.2.184.1 | 
| 6.2 CU1 | 6.2.274.9494 | 6.2.191.1 |
| 6.2 CU2 | 6.2.283.9494 | 6.2.194.1 |
| 6.2 CU3 | 6.2.301.9494 | 6.2.199.1 |
| 6.3 RTO | 6.3.162.9494 | 6.3.119.1 |
| 6.3 CU1 | 6.3.176.9494 | 6.3.124.1 |
| 6.3 CU1 | 6.3.187.9494 | 6.3.129.1 |
| 6.4 RTO | 6.4.617.9590 | 6.4.625.1 |
| 6.4 CU2 | 6.4.622.9590 | NA |
| 6.4 CU3 |	6.4.637.9590 | 6.4.634.1 |
| 6.4 CU4 | 6.4.644.9590 | 6.4.639.1 |
| 6.4 CU5 | 6.4.654.9590 | 6.4.649.1 |
| 6.4 CU6 | 6.4.658.9590 | NA |
| 6.4 CU7 | 6.4.664.9590 | 6.4.661.1 |
| 6.4 CU8 | 6.4.670.9590 | NA |
| 6.5 RTO | 6.5.639.9590 | 6.5.435.1 |
| 6.5 CU1 | 6.5.641.9590 | 6.5.454.1 |
| 6.5 CU2 | 6.5.658.9590 | 6.5.460.1 |
| 6.5 CU3 | 6.5.664.9590 | 6.5.466.1 |
| 6.5 CU5 | 6.5.676.9590 | 6.5.467.1 |
| 7.0 RTO | 7.0.457.9590 | 7.0.457.1 |
| 7.0 CU2 | 7.0.464.9590 | 7.0.464.1 |
| 7.0 CU3 | 7.0.466.9590 | 7.0.465.1 |
| 7.0 CU4 | 7.0.470.9590 | 7.0.469.1 |
| 7.0 CU6 | 7.0.472.9590 | 7.0.471.1 |
| 7.0 CU9 | 7.0.478.9590 | 7.0.472.1 |
| 7.1 RTO | 7.1.409.9590 | 7.1.410.1 |
| 7.1 CU1 | 7.1.417.9590 | 7.1.418.1 |
| 7.1 CU2 | 7.1.428.9590 | 7.1.428.1 |
| 7.1 CU3 | 7.1.456.9590 | 7.1.452.1 |
| 7.1 CU5 | 7.1.458.9590 | 7.1.454.1 |
| 7.1 CU6 | 7.1.459.9590 | 7.1.455.1 |
| 7.1 CU8 | 7.1.503.9590 | 7.1.508.1 |
| 7.2 RTO | 7.2.413.9590 | NA |
| 7.2 CU2 | 7.2.432.9590 | 7.2.431.1 |
| 7.2 CU3 | 7.2.433.9590 | NA |
| 7.2 CU4 | 7.2.445.9590 | 7.2.447.1 |

