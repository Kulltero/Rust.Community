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
| `horizontal`  | bool | if the ScrollView should be scrollable horizontally |
| `vertical`  | bool | if the ScrollView should be scrollable verticalally |
| `movementType` | string (enum `ScrollRect.MovementType`) | defines the movement behaviour of the ScrollView |
| `elasticity`  | float | sets the bouncyness of the ScrollView if movementType is set to `Elastic` |
| `inertia`  | bool | if the ScrollView should continue moving after the player stops dragging'scrolling |
| `decelerationRate`  | float | only used with inertia, higher decelerationRate = stops faster (visually) |

## Working with a ScrollView
Using a ScrollView allows us to better lay out our content as we dont have to worry about cramming as much content onto the screen as possible. or using a bulky pagination system.

the ScrollView uses 2 Panels under the hood. the panel you create the component on is the main panel and acts like the viewport. its size will define the visible part of the content.

**< [Previous Component](/docs/components/UnityEngine.UI.Outline.md)** | **[Back to Components](/docs/components/README.md)**
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc3MTk2NTg2MiwtOTA4NjIwMzIzLDEzND
AxNzM1NzEsMjkxMzk3NDg1LDQ4MTgxNDQ1OSwtMTM0OTg3NDgz
NSwxMTc5ODI4MjMyLDE1MTYwNjY3MjIsMjE0NDEzNzEzNCwtMT
YzMzM3MjkyNCwtMTYzMTAwNzk5OV19
-->