---
title: "onenote resource type"
description: "The entry point for OneNote resources."
author: "jewan-microsoft"
localization_priority: Normal
ms.prod: "onenote"
doc_type: resourcePageType
---

# onenote resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The entry point for OneNote resources.

All calls to the OneNote service through the Microsoft Graph API use this service root URL:

```
https://graph.microsoft.com/{version}/{location}/onenote/ 
```

The location can be user notebooks on Office 365 or consumer OneDrive, group notebooks, or SharePoint site-hosted team notebooks on Office 365. 

**User notebooks** To access personal notebooks on consumer OneDrive or OneDrive for Business, use one of the following URLs:

```
https://graph.microsoft.com/{version}/me/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{userPrincipalName}/onenote/{notebooks | sections | sectionGroups | pages} 
https://graph.microsoft.com/{version}/users/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

**Group notebooks** To access notebooks that are owned by a group, use the following service root URL:

```
https://graph.microsoft.com/{version}/groups/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```
**SharePoint site notebooks** To access notebooks that are owned by a SharePoint team site, use the following service root URL:

```
https://graph.microsoft.com/{version}/sites/{id}/onenote/{notebooks | sections | sectionGroups | pages} 
```

## Authorization

For information about the permissions required to work with OneNote APIs, see [Notes permissions](/graph/permissions-reference#notes-permissions).

## Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|notebooks|[Notebook](notebook.md) collection|The collection of OneNote notebooks that are owned by the user or group. Read-only. Nullable.|
|operations|[Operation](onenoteoperation.md) collection |The status of OneNote operations. Getting an operations collection is not supported, but you can get the status of long-running operations if the `Operation-Location` header is returned in the response. Read-only. Nullable.|
|pages|[Page](page.md) collection|The pages in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.|
|resources|[Resource](resource.md) collection |The image and other file resources in OneNote pages. Getting a resources collection is not supported, but you can [get the binary content of a specific resource](resource.md). Read-only. Nullable.|
|sectionGroups|[SectionGroup](sectiongroup.md) collection|The section groups in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.|
|sections|[Section](section.md) collection|The sections in all OneNote notebooks that are owned by the user or group.  Read-only. Nullable.|

## Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Create notebook](../api/onenote-post-notebooks.md) |[Notebook](notebook.md)| Create a notebook by posting to the notebooks collection.|
|[List notebooks](../api/onenote-list-notebooks.md) |[Notebook](notebook.md) collection| Get a collection of notebooks.|
|[Create page](../api/onenote-post-pages.md) |[Page](page.md)| Create a page by posting to the pages collection.|
|[List pages](../api/onenote-list-pages.md) |[Page](page.md) collection| Get a collection of pages.|
|[List section groups](../api/onenote-list-sectiongroups.md) |[SectionGroup](sectiongroup.md) collection| Get a collection of section groups.|
|[List sections](../api/onenote-list-sections.md) |[Section](section.md) collection| Get a collection of sections.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "onenote resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/onenote.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
