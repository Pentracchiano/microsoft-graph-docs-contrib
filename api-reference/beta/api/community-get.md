---
title: "Get community"
description: "Read the properties and relationships of a community object."
author: "aditijha4"
ms.localizationpriority: medium
ms.prod: "employee-engagement"
doc_type: apiPageType
---

# Get community

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [community](../resources/community.md) object.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- {
  "blockType": "permissions",
  "name": "community-get-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/community-get-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /employeeExperience/communities/{communityId}
```

## Optional query parameters

This method supports the `$select` and `$expand` [OData query parameters](/graph/query-parameters) to help customize the response.

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [community](../resources/community.md) object in the response body.

## Examples

### Request

The following example shows a request.

<!-- {
  "blockType": "request",
  "name": "get_community",
  "sampleKeys": ["eyJfdHlwZSI6Ikdyb3VwIiwiaWQiOiI4MzIxMjc1In0"]
}
-->
``` http
GET https://graph.microsoft.com/beta/employeeExperience/communities/eyJfdHlwZSI6Ikdyb3VwIiwiaWQiOiI4MzIxMjc1In0
```

### Response

The following example shows the response.

>**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.community"
}
-->
```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#employeeExperience/communities/$entity",
  "id": "eyJfdHlwZSI6Ikdyb3VwIiwiaWQiOiI4MzIxMjc1In0",
  "displayName": "Financial Advice for Software Engineers",
  "description": "A community where financial advisors who represent customers from software engineering profession can discuss advice and suggestions for there clients.",
  "privacy": "public",
  "groupId": "963da73d-a587-4ef3-aab0-d783e937e9e7"
}
```
