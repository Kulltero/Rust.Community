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
| `decelerationRate`  | float | sets the bouncyness of the ScrollView if movementType is set to `Elastic` |

**< [Previous Component](/docs/components/UnityEngine.UI.Outline.md)** | **[Back to Components](/docs/components/README.md)**
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM0MDE3MzU3MSwyOTEzOTc0ODUsNDgxOD
E0NDU5LC0xMzQ5ODc0ODM1LDExNzk4MjgyMzIsMTUxNjA2Njcy
MiwyMTQ0MTM3MTM0LC0xNjMzMzcyOTI0LC0xNjMxMDA3OTk5XX
0=
-->