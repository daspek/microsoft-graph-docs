---
title: "informationalUrl resource type"
description: "Basic profile information of the application."
localization_priority: Normal
doc_type: resourcePageType
---

# informationalUrl resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Basic profile information of the application.

## Properties

| Property | Type | Description |
|:---------------|:--------|:----------|
|marketing|String| Link to the application's marketing page. For example, https://www.contoso.com/app/marketing |
|privacy|String| Link to the application's privacy statement. For example, https://www.contoso.com/app/privacy |
|support|String| Link to the application's support page. For example, https://www.contoso.com/app/support |
|termsOfService|String| Link to the application's terms of service statement. For example, https://www.contoso.com/app/termsofservice |

## JSON representation
Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.informationalUrl"
}-->

```json
{
  "marketing": "String",
  "privacy": "String",
  "support": "String",
  "termsOfService": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "informationalUrl resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/informationalurl.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
