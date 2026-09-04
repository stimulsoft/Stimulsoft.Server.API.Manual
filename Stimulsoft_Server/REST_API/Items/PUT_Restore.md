## PUT Restore

**Description**:

Restores an item from the RecycleBin to its original location in the workspace of the currently logged-in user.


**Url Structure**:

`http://cloud.stimulsoft.com/1/items/itemKey/restore`


**Method**:

`PUT`


**Parameters**:

A custom header `x-sti-SessionKey` contains the session key of the current user. The itemkey parameter in the URI is the key of item and indicates the element whose data you want to change.


**CURL example:**

`curl -X PUT -H "x-sti-SessionKey: 09267e7288e44f37a0b376e5841b19ff" -d "" http://reports.stimulsoft.com/1/items/954c046ba3e2420b939851422ef0e086/restore`


**Returns**:

Returns a JSON object containing the `ResultSuccess` field, which indicates whether the item was successfully restored.


**Sample JSON response**

```
...
{
    "Ident": "ItemRestore",
    "AllowCreateWaitNotification": true,
    "AllowNotifications": false,
    "AllowSchedulerSignals": false,
    "AllowSignals": false,
    "AllowRemovingSource": false,
    "NotificationVisibility": true,
    "ResultTaskKey": "878f274f95d040cabfe1079a0a4148f1",
    "ResultSuccess": true
}
...
```
