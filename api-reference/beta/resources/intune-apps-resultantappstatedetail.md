---
title: "resultantAppStateDetail enum type"
description: "Enum indicating additional details regarding why an application has a particular install state."
author: "tfitzmac"
localization_priority: Normal
ms.prod: "Intune"
doc_type: enumPageType
---

# resultantAppStateDetail enum type

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Enum indicating additional details regarding why an application has a particular install state.

## Members
|Member|Value|Description|
|:---|:---|:---|
|noAdditionalDetails|0|No additional details are available.|
|seeInstallErrorCode|2000|Application failed to install. See error code property for more details.|
|seeUninstallErrorCode|4000|Application failed to uninstall. See error code property for more details.|
|pendingReboot|5000|Device must be rebooted to complete installation of the application.|
|platformNotApplicable|-1006|Application is not applicable to this platform. (e.g. Android app targeted to IOS)|
|minimumCpuSpeedNotMet|-1005|CPU speed on the target device is less than the configured minimum.|
|minimumLogicalProcessorCountNotMet|-1004|Count of logical processors on the target device is less than the configured minimum.|
|minimumPhysicalMemoryNotMet|-1003|Amount of RAM on the target device is less than the configured minimum.|
|minimumOsVersionNotMet|-1002|OS version on the target device is less than the configured minimum.|
|minimumDiskSpaceNotMet|-1001|Available disk space on the target device is less than the configured minimum.|
|processorArchitectureNotApplicable|-1000|Device architecture (e.g. x86/amd64) is not applicable for the application.|




