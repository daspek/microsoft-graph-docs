---
title: "governanceSubject resource type"
description: "Represents users, groups, and service principals being managed in Privileged Identity Management (PIM)."
localization_priority: Normal
doc_type: resourcePageType
---

# governanceSubject resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents users, groups, and service principals being managed in Privileged Identity Management (PIM).


## Properties
| Property	| Type	     |Description|
|:----------|:----------|:----------|
|id         |String     | The id of the subject.|
|type       |String     |The type of the subject. The value can be ``User``, ``Group``, and ``ServicePrincipal``.|
|displayName|String     |The display name of the subject.|
|email      |String     |The email address of the user subject. If the subject is in other types, it is empty.|
|principalName|String   |The principal name of the user subject. If the subject is in other types, it is empty.|

## Relationships
None


## JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceSubject"
}-->

```json
{
  "id": "String",  
  "displayName": "String",
  "email": "String",
  "principalName": "String",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "governanceSubject",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/governancesubject.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
