---
title: "Skype for Business activity reports"
description: "You can get details on activity across your organization. These details can help you investigate, plan, and make other business decisions for your organization."
localization_priority: Normal
ms.prod: "reports"
author: "pranoychaudhuri"
doc_type: conceptualPageType
---

# Skype for Business activity reports

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

You can get details on activity across your organization. These details can help you investigate, plan, and make other business decisions for your organization.

> **Note:** For details about different report views and names, see [Office 365 Reports - Skype for Business activity](https://support.office.com/client/Skype-for-Business-Online-activity-8cbe2eb2-1194-4fd7-b1ee-9f9287c82424).

## Reports

| Function                                 | CSV return type | JSON return type                         | Description                              |
| :--------------------------------------- | :-------------- | :--------------------------------------- | ---------------------------------------- |
| [Get user detail](../api/reportroot-getskypeforbusinessactivityuserdetail.md) | Stream          | [skypeForBusinessActivityUserDetail](../resources/skypeforbusinessactivityuserdetail.md) | Get details about Skype for Business activity by user. |
| [Get activity counts](../api/reportroot-getskypeforbusinessactivitycounts.md) | Stream          | [skypeForBusinessActivityCounts](../resources/skypeforbusinessactivitycounts.md) | Get the trends on how many users organized and participated in conference sessions held in your organization through Skype for Business. The report also includes the number of peer-to-peer sessions. |
| [Get user counts](../api/reportroot-getskypeforbusinessactivityusercounts.md) | Stream          | [skypeForBusinessActivityUserCounts](../resources/skypeforbusinessactivityusercounts.md) | Get the trends on how many unique users organized and participated in conference sessions held in your organization through Skype for Business. The report also includes the number of peer-to-peer sessions. |
<!--
{
  "type": "#page.annotation",
  "suppressions": [
    "Error: /api-reference/beta/resources/skype-for-business-activity-reports.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
