---
title: "publicClient resource type"
description: "Specifies settings for non Web App or Web Api. (e.g. Mobile or other public client such as an installed application running on a desktop device)"
localization_priority: Normal
doc_type: resourcePageType
---

# publicClient resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Specifies settings for non Web App or Web Api. (e.g. Mobile or other public client such as an installed application running on a desktop device)

## Properties

| Property | Type | Description |
|:---------------|:--------|:----------|
|redirectUris|String collection| Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to. |

## JSON representation
Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.installedClient"
}-->

```json
{
  "redirectUris": ["String"]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "installedClient resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/publicclient.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
