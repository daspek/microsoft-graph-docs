---
title: "automaticUpdateMode enum type"
description: "Possible values for automatic update mode."
author: "tfitzmac"
localization_priority: Normal
ms.prod: "Intune"
doc_type: enumPageType
---

# automaticUpdateMode enum type

> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.

Possible values for automatic update mode.

## Members
|Member|Value|Description|
|:---|:---|:---|
|userDefined|0|User Defined, default value, no intent.|
|notifyDownload|1|Notify on download.|
|autoInstallAtMaintenanceTime|2|Auto-install at maintenance time.|
|autoInstallAndRebootAtMaintenanceTime|3|Auto-install and reboot at maintenance time.|
|autoInstallAndRebootAtScheduledTime|4|Auto-install and reboot at scheduled time.|
|autoInstallAndRebootWithoutEndUserControl|5|Auto-install and restart without end-user control|
|windowsDefault|6|Reset to Windows default value.|




