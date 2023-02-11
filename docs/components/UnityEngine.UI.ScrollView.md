# Components: ScrollView
**< [Previous Component](/docs/components/UnityEngine.UI.Outline.md)** | **[Back to Components](/docs/components/README.md)**
-   Identifier:  `UnityEngine.UI.ScrollView`
-   Category:  **Interactive**
-   Unity Documentation:  **[ScrollRect @ docs.unity3d.com](https://docs.unity3d.com/Packages/com.unity.ugui@1.0/manual/script-ScrollRect.html)**

The ScrollView Component is an Interactive Component that lets you fit more content on the screen by letting the player scroll or drag through your content. It supports both vertical and horizontal scrolling.
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
| `contentTransform`     | RectTransform | the Size of the content. Needs to at least match the size of the ScrollView.  |
| `horizontal`  | bool | if the ScrollView should be scrollable horizontally |
| `vertical`  | bool | if the ScrollView should be scrollable vertically |
| `movementType` | string (enum `ScrollRect.MovementType`) | defines the movement behavior of the ScrollView |
| `elasticity`  | float | sets the bounciness of the ScrollView if movementType is set to `Elastic` |
| `inertia`  | bool | if the ScrollView should continue moving after the player stops dragging/scrolling |
| `decelerationRate`  | float | only used with inertia, higher decelerationRate = stops faster (visually) |

## Working with a ScrollView

Using a ScrollView allows us to better lay out our content, as we don't have to worry about cramming as much content onto the screen as possible. Or using a bulky pagination system.

The ScrollView uses 2 Panels under the hood. The panel you create the component on is the main panel and acts like the viewport. Its size will define the visible part of the content.

The second panel is created by the ScrollView Component to hold all of its content. Its size is defined by the  `contentTransform`  property and is automatically positioned, so the upper left corner is aligned with the Viewport.

> NOTE: the CUI system will automatically Parent any future children of the ScrollView to its content panel, to ensure all children are scrollable

## Elasticity, Inertia & Movement

the ScrollView Component has a range of options to customize the scrolling behavior. The most important setting is the  `movementType`  setting, as it defines how the ScrollView should react when the edge of its content is reached.

If the setting  `Unrestricted`  is used, the ScrollView will continue to let the user scroll past the bounds of the content. This is often unwanted behavior, as it's easy to lose the content if a user scrolls too far or flicks too hard.

If the setting  `Clamped`  is used, the ScrollView will hard stop at the edge of its content. It will not allow the user to scroll past the edge of the content.

If the setting  `Elastic`  is used, the ScrollView will let the user scroll past the edge of the content, but will ‘bounce’ back to the edge the moment the user lets go.

The  `elasticity`  setting can be used to let the Viewport bounce further into the content again.

### Using Inertia

inertia is the setting that controls if the Viewport should immediately stop scrolling or slow down over time. Combining this setting with elasticity is typically used to recreate the scrolling behavior on a smartphone.

Using the  `decelerationRate`  setting, you can control how fast the scrolling should slow down.

### A note on performance

an important thing to remember when using ScrollViews is that content outside the viewport still adds a performance cost. So it's discouraged to show large lists with 100's or 1000's of elements. If you want to use a large dataset, try creating a search feature or adding a “Load More” button to limit how many items are shown at once.

Another thing to know is that the Inertia & Elastic settings can be less performant than a Clamped ScrollView without Inertia. This is because these settings often continue to scroll the viewport long after the player has let go, even if it has  _visually_  stopped scrolling, it often still updates under the hood causing useless Canvas updates.
 

**< [Previous Component](/docs/components/UnityEngine.UI.Outline.md)** | **[Back to Components](/docs/components/README.md)**
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEwMDk0NTI4NywxODY0MTg4NzMwLC00OT
E0OTQ5NjEsNjc4NDQ1MDc2LC0xMjk5Mzc0OTM5LDQ0MDc1NjAw
NCwtNjIwODcyMjc3LC03NzE5NjU4NjIsLTkwODYyMDMyMywxMz
QwMTczNTcxLDI5MTM5NzQ4NSw0ODE4MTQ0NTksLTEzNDk4NzQ4
MzUsMTE3OTgyODIzMiwxNTE2MDY2NzIyLDIxNDQxMzcxMzQsLT
E2MzMzNzI5MjQsLTE2MzEwMDc5OTldfQ==
-->