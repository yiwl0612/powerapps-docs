---
title: "clearGlobalNotification (Client API reference) in model-driven apps| MicrosoftDocs"
description: Includes description and supported parameters for the clearGlobalNotification method.
author: adrianorth
ms.author: aorth
ms.date: 03/12/2022
ms.reviewer: jdaly
ms.topic: reference
search.audienceType: 
  - developer
search.app: 
  - PowerApps
  - D365CE
contributors:
  - JimDaly
---
# clearGlobalNotification (Client API reference)

[!INCLUDE[./includes/clearGlobalNotification-description.md](./includes/clearGlobalNotification-description.md)]

## Syntax

`Xrm.App.clearGlobalNotification(uniqueId).then(successCallback, errorCallback);`

## Parameters

<table>
<tr>
<th>Name</th>
<th>Type</th>
<th>Required</th>
<th>Description</th>
</tr>
<tr>
<td>uniqueId</td>
<td>String</td>
<td>Yes</td>
<td>The ID to use to clear a specific notification that was set using <a href="addGlobalNotification.md">addGlobalNotification</a>.
</td>
</tr>
<tr>
<td>successCallback</td>
<td>Function</td>
<td>No</td>
<td><p>A function to call when the notification is cleared.</p>
</td>
</tr>
<tr>
<td>errorCallback</td>
<td>Function</td>
<td>No</td>
<td>A function to call when the operation fails.</td>
</tr>
</table>

## Return Value

On success, returns a promise object.

## Examples

The following example shows how to add a notification and then close it automatically after 5 seconds.

```JavaScript
// define notification object
var notification = 
{
  type: 2,
  level: 3, //warning
  message: "Test warning notification"
}

Xrm.App.addGlobalNotification(notification).then(
    function success(result) {
        console.log("Notification created with ID: " + result);

    // Wait for 5 seconds and then clear the notification
    window.setTimeout(function () { 
            Xrm.App.clearGlobalNotification(result); }, 5000);
    },
    function (error) {
        console.log(error.message);
        // handle error conditions
    }
);
```

### See also

[addGlobalNotification](addGlobalnotification.md)


[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]