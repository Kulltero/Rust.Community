# Components: Outline
**< [Previous Component](/docs/components/UnityEngine.UI.Text.md)** | **[Back to Components](/docs/components/README.md)** | **[Next Component](/docs/components/UnityEngine.UI.Button.md) >**

- Identifier: `UnityEngine.UI.Outline`
- Category: **Effect**
- Unity Documentation: **[Outline @ docs.unity3d.com](https://docs.unity3d.com/Packages/com.unity.ugui@1.0/manual/script-Outline.html)**

The Outline Component is an Effect Component that puts a colored outline on any Visual Component. it supports any Image, Text, Button, or Input field.
```json
{
	"type": "UnityEngine.UI.Outline",
	"color": "1.0 1.0 1.0 1.0",
	"distance": "1.0 -1.0",
	"useGraphicAlpha": null,
    "fadeIn": 0.0
}
```
> `useGraphicAlpha` is a key presence Field, key presence Fields don't have a specific type and act as a Boolean.
> if the key is present it equals true, if absent it equals false.

Outline specific Fields:
| Key         | Type   | Notes                |
| :---------- | :----- | :------------------- |
| `color`     | string | the Color of your Outline |
| `distance`  | string | the distance of your Outline (formatted as `X Y`) |
| `useGraphicAlpha` | key presence Field | multiplies the Alpha of the graphic onto the color of the Outline |
| `fadeIn`    | float  | the Duration the Panel should take to fade in |

**< [Previous Component](/docs/components/UnityEngine.UI.Text.md)** | **[Back to Components](/docs/components/README.md)** | **[Next Component](/docs/components/UnityEngine.UI.Button.md) >**
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTk4MTY2NzU1NiwtNzA5MjE3NDM0LC03Nz
IxMjY1NiwxMDkxODAxMDcyLDczNDAzNTA3Nl19
-->