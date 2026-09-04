## GET List

**Description**:

Gets the version history of a specified item in the workspace of the logged-in user.


**Url Structure**:

`http://reports.stimulsoft.com/1/items/{itemKey}/versions`


**Method**:

`GET`


**Parameters**:

A custom header x`-sti-SessionKey` contains the session key of the current user. The item identifier is specified in the URL path parameter `{itemKey}`.


**CURL example**:

`curl -X GET -H "x-sti-SessionKey: 09267e7288e44f37a0b376e5841b19ff" http://reports.stimulsoft.com/1/items/f10358b8a3a44a31aa3690df8c4b1c95/versions`


**Returns**:

A JSON object containing the `ResultVersions` collection, which represents the list of available versions for the specified item. The success of the command execution is checked by the content of the field `ResultSuccess`.


**Sample JSON response**

```
...
{
    "Ident": "ItemFetchVersions",
    "AllowDeleted": false,
    "ResultVersions": [
        {
            "StateKey": "1",
            "ItemKey": "f10358b8a3a44a31aa3690df8c4b1c95",
            "WorkspaceKey": "e15516cd7d6d4f30973f7856dfb7b6d8",
            "Created": "\/Date(1782200646987)\/",
            "UserName": "a a",
            "Key": "ea7314336e374a88a52c03b25245796c"
        },
        {
            "StateKey": "2",
            "ItemKey": "f10458b8a3a44a31aa3690df8c4b1c95",
            "WorkspaceKey": "e11216cd7d6d4f30973f7856dfb7b6d8",
            "Created": "\/Date(1782200646981)\/",
            "UserName": "b b",
            "Key": "ea7314336e374a88a52c03b25245356c"
        }
    ],
    "ResultSuccess": true
}
...
```
