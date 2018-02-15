# Create allowedDataLocation

Enables multiple data location support for a service or sets an additional allowed data location for a service.  Calling the create allowedDataLocation API with a supported AppID enables multi-geo feature for the corresponding service and sets the first allowed data location for that service.

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
POST /allowedDataLocations

```
## Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|

## Request body

In the request body, supply a JSON representation of [allowedDataLocation](../resources/alloweddatalocation.md) object.

## Response
If successful, this method returns `201, Created` response code and [allowedDataLocation](../resources/alloweddatalocation.md) object in the response body.

## Example

##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_alloweddatalocation_from_alloweddatalocations"
}-->
```http
POST https://graph.microsoft.com/beta/allowedDataLocations
Content-type: application/json
Content-length: 148

{
  "allowedDataLocation": {
    "appId": "appId-value",
    "location": "location-value",
    "isDefault": true,
    "domain": "domain-value"
  }
}
```
In the request body, supply a JSON representation of [allowedDataLocation](../resources/alloweddatalocation.md) object.

##### Response

Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.allowedDataLocation"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 170

{
  "allowedDataLocation": {
    "id": "id-value",
    "appId": "appId-value",
    "location": "location-value",
    "isDefault": true,
    "domain": "domain-value"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create allowedDataLocation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->