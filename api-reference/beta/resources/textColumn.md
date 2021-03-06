---
author: JeremyKelley
ms.author: JeremyKelley
ms.date: 09/11/2017
title: TextColumn
localization_priority: Normal
doc_type: resourcePageType
---
# TextColumn resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The **textColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values are text.

## JSON representation

Here is a JSON representation of a **textColumn** resource.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.textColumn" } -->

```json
{
  "allowMultipleLines": true,
  "appendChangesToExistingText": false,
  "linesForEditing": 6,
  "maxLength": 300,
  "textType": "plain | richText"
}
```

## Properties

| Property name                   | Type   | Description
|:--------------------------------|:-------|:-----------------------------------------------
| **allowMultipleLines**          | string | Whether to allow multiple lines of text.
| **appendChangesToExistingText** | string | Whether updates to this column should replace existing text, or append to it.
| **linesForEditing**             | int    | The size of the text box.
| **maxLength**                   | int    | The maximum number of characters for the value.
| **textType**                    | string | The type of text being stored. Must be one of `plain` or `richText`

<!--
{
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/TextColumn",
  "suppressions": [
    "Error: /api-reference/beta/resources/textColumn.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
