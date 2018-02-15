# Update alloweddatalocation

Update the properties of an alloweddatalocation object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).

|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) |  Directory.AccessAsUser.All  |
|Delegated (personal Microsoft account) | Not supported |
|Application | Not supported |

## HTTP request
<!-- { "blockType": "ignored" } -->
```http
PATCH /allowedDataLocations/<id>
```
## Optional request headers
| Name       | Description|
|:-----------|:-----------|
| Authorization  | Bearer {code}|

## Request body
In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.

| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|appId|String| The service type's application principal id enabled for multiple data location support. |
|domain|String| The domain associated with this allowed data location. |
|isDefault|Boolean| Set to true if this is the default location to store data for a service. |
|location|String| A location where data storage is allowed for a service. |

## Response
If successful, this method returns a `200 OK` response code and updated [allowedDataLocation](../resources/alloweddatalocation.md) object in the response body.
## Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "update_alloweddatalocation"
}-->
```http
PATCH https://graph.microsoft.com/beta/allowedDataLocations/<id>
Content-type: application/json
Content-length: 109

{
  "appId": "appId-value",
  "location": "location-value",
  "isDefault": true,
  "domain": "domain-value"
}
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.allowedDataLocation"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 129

{
  "id": "id-value",
  "appId": "appId-value",
  "location": "location-value",
  "isDefault": true,
  "domain": "domain-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update alloweddatalocation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->