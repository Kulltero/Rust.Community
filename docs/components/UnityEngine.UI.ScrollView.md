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
	"elasticity": 0.1,
	"inertia": false,
	"decelerationRate": 0.135,
	"scrollSensitivity": 1.0
}
```

ScrollView specific Fields:
| Key         | Type   | Notes                |
| :---------- | :----- | :------------------- |
| `contentTransform`     | RectTransform | the Size of the content. needs to atleast match the size of the ScrollView  |
| `horizontal`  | bool | The distance of your Outline (formatted as `X Y`) |
| `useGraphicAlpha` | key presence Field | Multiplies the Alpha of the graphic onto the color of the Outline |

**< [Previous Component](/docs/components/UnityEngine.UI.Outline.md)** | **[Back to Components](/docs/components/README.md)**
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE2MzIyMjcxMTMsMjE0NDEzNzEzNCwtMT
YzMzM3MjkyNCwtMTYzMTAwNzk5OV19
-->