# The Basics of CUI
**[Back to the Start](/README.md)** | **[Next Topic](/docs/components/README.md) >**

There are a few basic Concepts that are needed to make your own CUI, below you will learn about what Panels are & how to create and destroy UI Elements

## The Schema

the JSON Schema to send UI to the Player consists of a List of Elements, where each Element creates a new Panel on the Client. Elements have One or more Components that control the Look & Functionality.

```json
[{
	"name": "AddUI CreatedPanel",
	"parent": "Overlay",
	"components": [...],
	"fadeOut": 0.0,
	"destroyUi": ""
}, ...]
```
> The values in these JSON examples represent the default values that are assigned if no property is specified.  
> … represent One or more collapsed Objects

| Key | Type     | Notes                |
| :-- | :------- | :------------------- |
| `name` | string | The identifier of your panel, needed when destroying UI or adding panels inside this one |
| `parent` | string | Tells the client which Panel or Layer to Parent to |
| `components` |List of Components | One or more Components, without these there’s no point in sending a panel |
| `fadeOut` | float | Makes the Panel fade out instead of disappearing immediately.  _Currently doesn’t fade out any child panels._ |
| `destroyUi` | string | Destroys the Panel specified in the string before creating your Panel. Useful for updating UI. |


### About Naming

It’s recommended to always name your Panels  _something_, this is because the CUI System doesn’t support multiple Panels with the same name and may cause  _Ghost Panels_  which can't be destroyed.

It’s also recommended to prefix the Name of your Panel with something unique to your Mod, which ensures there are no accidental name Conflicts with other Mods


## Sending & destroying UI

There are two RPC Calls you can use to send  & destroy UI respectively

Adding UI:
```c#
BasePlayer player = targetPlayer;
string json = "..."; // your UI in JSON form
var community = CommunityEntity.ServerInstance;
SendInfo sendInfo = new SendInfo(player.net.connection);
community.ClientRPCEx<string>(sendInfo, null, "AddUI", json);
```

Destroying UI:
```c#
BasePlayer player = targetPlayer;
string panel = "AddUi CreatedPanel"; // the name of the Panel you wish to destroy
var community = CommunityEntity.ServerInstance;
SendInfo sendInfo = new SendInfo(player.net.connection);
community.ClientRPCEx<string>(sendInfo, null, "DestroyUI", panel);
```
When destroying a Panel, all child panels will also get destroyed.
> Your Modding Framework may have helper Methods to simplify these steps.

----
The next Topic explains Components in detail

**[Back to the Start](/README.md)** | **[Next Topic](/docs/components/README.md) >**

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5NDI1OTI5NjMsODk3Mjg0MDMwLDg5ND
U4Njk0OCwtMTA2NDY5NTM5MiwtNDIwNDgzNiwtMTMyMTk5MzQw
Miw0NzA2NjcxMTksNjg4NjUyODAsLTExNjU4ODM5NjNdfQ==
-->