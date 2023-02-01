# Components: Image
**< [Previous Component](/docs/components/UnityEngine.UI.RawImage.md)** | **[Back to Components](/docs/components/README.md)** | **[Next Component](/docs/components/UnityEngine.UI.Text.md) >**

- Identifier: `UnityEngine.UI.Image`
- Category: **Visual**
- Unity Documentation: **[Image @ docs.unity3d.com](https://docs.unity3d.com/Packages/com.unity.ugui@1.0/manual/script-Image.html)**

The Image is a Visual Component that allows you to display images from your Server & the Web or Rust Sprites. It can also be used with a single color to act as a Background for your panel.
```json
{
	"type": "UnityEngine.UI.Image",
	"sprite": "Assets/Icons/rust.png",
	"color": "1.0 1.0 1.0 1.0",
	"material": "",
	"imagetype": "Simple",
	"png": "",
	"itemid": 0,
	"skinid": 0,
    "fadeIn": 0.0
}
```
RawImage specific Fields:
| Key         | Type   | Notes                |
| :---------- | :----- | :------------------- |
| `sprite`    | string | the asset Path to the sprite |
| `color`     | string | the normalized RGBA values of your color |
| `material`  | string | the asset Path to the Material |
| `imagetype` | string (enum `Image.Type`) | sets the display mode of the Image* |
| `png`       | string | the CRC Checksum of the Image hosted on the Server |
| `itemid`    | int    | the Item ID of your item |
| `skinid`    | ulong  | the Skin ID of your skin |
| `fadeIn`    | float  | the Duration the Panel should take to fade in |
\*  Currently non-functioning for anything other than Rust's built-in Sprites
## RawImages vs Images
Like RawImages, Images share the ability to show Sprites, Colors, Materials & Images hosted on the Server, but they cannot directly load images from the Web.

The Image Component has convenient Ways to display any Item or Skin and is recommended when using Rust's Sprites.

## Items and Skins
using the  `itemid`  &  `skinid`  fields, you can let the Client handle the displaying of related Images.

Tip: use the ItemDefinition of your Item to easily find an Item’s ID & other useful Information
```c#
string shortname = "your.item.shortname";
var itemDef = ItemManager.FindItemDefinition(shortname);
int itemid = itemDef.itemid;
// other useful Fields: displayName, displayDescription, category & stackable
```


---
check the [RawImage](/docs/components/UnityEngine.UI.RawImage.md) Documentation to learn about Fields the Components share.
**< [Previous Component](/docs/components/UnityEngine.UI.RawImage.md)** | **[Back to Components](/docs/components/README.md)** | **[Next Component](/docs/components/UnityEngine.UI.Text.md) >**
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1ODUzMTkyMDAsNzE2MzUxNDYwLC0xNT
kwMzgxMjkzLC0xNzA2MDE3ODA0LC0yMDE2MDcwNjM2LDU2OTg0
MjMxOCwtMTg4MTYxMjIxLC0xNjA3MzI0NTg5LC02NjI2NjExMj
AsMTQ5ODMyNDQ2MywxNzg3MTMyMTU0LDkyMDc0MjQ2MCwtMTMz
NTMwNDk4MiwtNDk0MDEwMTkxLDU4NTA4NjU4LC0xMzI5MDE3NT
kyLDIwOTM5NjIzNjQsLTE3NTAzMjk3NCwxMDA4NDc5NDEwLC0x
MDU4Mjc3MTkwXX0=
-->