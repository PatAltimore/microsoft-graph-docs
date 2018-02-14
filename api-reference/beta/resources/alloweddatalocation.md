# allowedDataLocation resource type

Represents a multi-geo data location for a service. Tenant admins can enable allowed data locations for each individual service. Allowed data locations can also be used to identify the preferred data location for users and groups. 

## Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get allowedDataLocation](../api/alloweddatalocation_get.md) | [allowedDataLocation](alloweddatalocation.md) |Read properties and relationships of allowedDataLocation object.|
|[Update](../api/alloweddatalocation_update.md) | [allowedDataLocation](alloweddatalocation.md)	|Update allowedDataLocation object. |
|[Delete](../api/alloweddatalocation_delete.md) | None |Delete allowedDataLocation object. |

## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|appId|String| The service type's application principal id enabled for multiple data location support. |
|domain|String| The domain associated with this allowed data location. |
|id|String| The key id of the allowed data location. This is used to look up a specific resource object. Read-only. |
|isDefault|Boolean| Set to true if this is the default location to store data for a service. |
|location|String| A location where data storage is allowed for a service. |

## Relationships
None


## JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.allowedDataLocation"
}-->

```json
{
  "appId": "String",
  "domain": "String",
  "id": "String (identifier)",
  "isDefault": true,
  "location": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "allowedDataLocation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->