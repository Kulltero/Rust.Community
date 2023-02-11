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

the second panel is created by the ScrollView Component to hold all of its content. its size is defined by the `contentTransform` property and is automatically positioned so the upper left corner is aligned with the Viewport.

> NOTE: the CUI system will automatically Parent any future children of the ScrollView to its content panel, to ensure all children are scrollable

## Elasticity, Inertia & Movement
the ScrollView Component has a range of options to customize the scrolling behavior. the most important setting is the `movementType` setting, as it defines how the ScrollView should react when the edge of its content is reached.

**< [Previous Component](/docs/components/UnityEngine.UI.Outline.md)** | **[Back to Components](/docs/components/README.md)**
<!--stackedit_data:
eyJoaXN0b3J5IjpbOTk4NTYzMjYyLDY3ODQ0NTA3NiwtMTI5OT
M3NDkzOSw0NDA3NTYwMDQsLTYyMDg3MjI3NywtNzcxOTY1ODYy
LC05MDg2MjAzMjMsMTM0MDE3MzU3MSwyOTEzOTc0ODUsNDgxOD
E0NDU5LC0xMzQ5ODc0ODM1LDExNzk4MjgyMzIsMTUxNjA2Njcy
MiwyMTQ0MTM3MTM0LC0xNjMzMzcyOTI0LC0xNjMxMDA3OTk5XX
0=
-->