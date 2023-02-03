# **AllClientPermissions**
## **About**
* When using this options, If the client (bot) has all of the permissions in the array then it will continue else it will stop and send error message by default.

{% hint style="info" %}
**Note:** Make sure you put the permissions name correctly as they are case sensitive. For example: `ADMINISTRATOR` will not work instead use `Administrator`. You can find all the permissions correct names at [here](../../FAQ.md)
{% endhint %}
## **Usage**
```js
allClientPermissions: ["Perm1", "Perm2"]
returnClientPermissions: true / false // Default: true [ OPTIONAL ]
```
## **Example**
```js
allClientPermissions: ["Administrator", "ManageEvents"]
```