# Components: ScrollView
**< [Previous Component](/docs/components/UnityEngine.UI.Outline.md)** | **[Back to Components](/docs/components/README.md)**

- Identifier: `UnityEngine.UI.ScrollView`
- Category: **Interactive**
- Unity Documentation: **[ScrollView @ docs.unity3d.com](https://docs.unity3d.com/Packages/com.unity.ugui@1.0/manual/script-Outline.html)**

The Outline Component is an Effect Component that puts a colored outline on any Visual Component. It supports any Image, Text, Button, or Input field.
```json
{
	"type": "UnityEngine.UI.ScrollView",
	"color": "1.0 1.0 1.0 1.0",
	"distance": "1.0 -1.0",
	"useGraphicAlpha": null
}
```
> `useGraphicAlpha` is a key presence Field, key presence Fields don't have a specific type and act as a Boolean.
> If the key is present it equals true, if absent it equals false.

Outline specific Fields:
| Key         | Type   | Notes                |
| :---------- | :----- | :------------------- |
| `color`     | string | The Color of your Outline |
| `distance`  | string | The distance of your Outline (formatted as `X Y`) |
| `useGraphicAlpha` | key presence Field | Multiplies the Alpha of the graphic onto the color of the Outline |

**< [Previous Component](/docs/components/UnityEngine.UI.Outline.md)** | **[Back to Components](/docs/components/README.md)**
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2MzEwMDc5OTldfQ==
-->