---
title: "reportRoot: getEmailAppUsageAppsUserCounts"
description: "Get the count of unique users per email app."
localization_priority: Normal
ms.prod: "reports"
author: "pranoychaudhuri"
doc_type: apiPageType
---

# reportRoot: getEmailAppUsageAppsUserCounts

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the count of unique users per email app.

> **Note:** For details about different report views and names, see [Office 365 Reports - Email apps usage](https://support.office.com/client/Email-apps-usage-c2ce12a2-934f-4dd4-ba65-49b02be4703d).

## Permissions

One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

| Permission type                        | Permissions (from least to most privileged) |
| :------------------------------------- | :--------------------------------------- |
| Delegated (work or school account)     | Reports.Read.All                         |
| Delegated (personal Microsoft account) | Not supported.                           |
| Application                            | Reports.Read.All                         |

## HTTP request

<!-- { "blockType": "ignored" } --> 

```http
GET /reports/getEmailAppUsageAppsUserCounts(period='{period_value}')
```

## Function parameters

In the request URL, provide the following parameter with a valid value.

| Parameter | Type   | Description                              |
| :-------- | :----- | :--------------------------------------- |
| period    | string | Specifies the length of time over which the report is aggregated. The supported values for {period_value} are: D7, D30, D90, and D180. These values follow the format D*n* where *n* represents the number of days over which the report is aggregated. Required. |

This method supports the `$format` [OData query parameter](/graph/query-parameters) to customize the response. The default output type is text/csv. However, if you want to specify the output type, you can use the OData $format query parameter set to text/csv or application/json.

## Request headers

| Name          | Description               |
| :------------ | :------------------------ |
| Authorization | Bearer {token}. Required. |

## Response

### CSV

If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report. That URL can be found in the `Location` header in the response.

Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.

The CSV file has the following headers for columns.

- Report Refresh Date
- Mail For Mac
- Outlook For Mac
- Outlook For Windows
- Outlook For Mobile
- Other For Mobile
- Outlook For Web
- POP3 App
- IMAP4 App
- SMTP App
- Report Period

### JSON

If successful, this method returns a `200 OK` response code and an **[emailAppUsageAppsUserCounts](../resources/emailappusageappsusercounts.md)** object in the response body.

## Example

### CSV

The following is an example that outputs CSV.

#### Request

The following is an example of the request.

<!-- {
  "blockType": "request",
  "name": "reportroot_getemailappusageappsusercounts_csv"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getEmailAppUsageAppsUserCounts(period='D7')?$format=text/csv
```

#### Response

The following is an example of the response.

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

Follow the 302 redirection and the CSV file that downloads will have the following schema.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Mail For Mac,Outlook For Mac,Outlook For Windows,Outlook For Mobile,Other For Mobile,Outlook For Web,POP3 App,IMAP4 App,SMTP App,Report Period
```

### JSON

The following is an example that returns JSON.

#### Request

The following is an example of the request.

<!-- {
  "blockType": "request",
  "name": "reportroot_getemailappusageappsusercounts_json"
}-->

```http
GET https://graph.microsoft.com/beta/reports/getEmailAppUsageAppsUserCounts(period='D7')?$format=application/json
```

#### Response

The following is an example of the response.

> **Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.emailAppUsageAppsUserCounts"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 345

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Collection(microsoft.graph.emailAppUsageAppsUserCounts)", 
  "value": [
    {
      "reportRefreshDate": "2017-09-01", 
      "mailForMac": 4, 
      "outlookForMac": 105, 
      "outlookForWindows": 1589, 
      "outlookForMobile": 1116, 
      "otherForMobile": 485, 
      "outlookForWeb": 753, 
      "pop3App": 0, 
      "imap4App": 0, 
      "smtpApp": 0, 
      "reportPeriod": "7"
    }
  ]
}
```
<!--
{
  "type": "#page.annotation",
  "suppressions": [
    "Error: /api-reference/beta/api/reportroot-getemailappusageappsusercounts.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
