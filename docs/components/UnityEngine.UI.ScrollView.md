# Components: ScrollView
**< [Previous Component](/docs/components/UnityEngine.UI.Outline.md)** | **[Back to Components](/docs/components/README.md)**

- Identifier: `UnityEngine.UI.ScrollView`
- Category: **Interactive**
- Unity Documentation: **[ScrollRect @ docs.unity3d.com](https://docs.unity3d.com/Packages/com.unity.ugui@1.0/manual/script-ScrollRect.html)**

The ScrollView Component is an Interactive Component that lets you fit more content on the screen by letting the player scroll or drag through your content. it supports both vertical and horizontal scrolling.
```json
{
	"type": "UnityEngine.UI.ScrollView",
	"contentTransform": {
		"anchormin": "0.0 0.0",
		"anchormax": "1.0 1.0",
		"offsetmin": "0.0 0.0",
		"offsetmax": "1.0 1.0",
	},
	"horizontal": false,
	"vertical": false,
	"movementType": "Clamped",
	"elasticity": "Clamped",
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
eyJoaXN0b3J5IjpbLTIxMTExNjUxMjIsLTE2MzEwMDc5OTldfQ
==
-->