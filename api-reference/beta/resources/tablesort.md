---
title: "TableSort resource type"
description: "Manages sorting operations on Table objects."
author: "lumine2008"
localization_priority: Normal
ms.prod: "excel"
doc_type: resourcePageType
---

# TableSort resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Manages sorting operations on Table objects.


## Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get TableSort](../api/tablesort-get.md) | [TableSort](tablesort.md) |Read properties and relationships of tableSort object.|
|[Apply](../api/tablesort-apply.md)|None|Perform a sort operation.|
|[Clear](../api/tablesort-clear.md)|None|Clears the sorting that is currently on the table. While this doesn't modify the table's ordering, it clears the state of the header buttons.|
|[Reapply](../api/tablesort-reapply.md)|None|Reapplies the current sorting parameters to the table.|

## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|matchCase|boolean|Represents whether the casing impacted the last sort of the table. Read-only.|
|method|string|Represents Chinese character ordering method last used to sort the table. Possible values are: `PinYin`, `StrokeCount`. Read-only.|

## Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|fields|[SortField](sortfield.md)|Represents the current conditions used to last sort the table. Read-only.|

## JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.tableSort"
}-->

```json
{
  "matchCase": true,
  "method": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "TableSort resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/tablesort.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
