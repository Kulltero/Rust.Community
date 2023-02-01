# Components: Countdown
**< [Previous Component](/docs/components/NeedsX.md)** | **[Back to Components](/docs/components/README.md)**

- Identifier: `Countdown`
- Category: **Misc**
- Unity Documentation: **N/A**

The Countdown Component lets you turn an existing Text Component into a Timer, Countdown, or Count-up. the Countdown Component automatically **destroys** the Panel when it's done counting.
```json
{
	"type": "Countdown",
	"endtime": 0,
	"startTime": 0,
	"step": 1,
	"command": ""
}
```

Countdown-specific Fields:
| Key         | Type   | Notes                |
| :---------- | :----- | :------------------- |
| `endTime`   | int    | the Number it should count to |
| `startTime` | int    | the Number it should start counting from |
| `step`      | int    | the Number it should increment by, also acts as the update interval |
| `command`   | string | the Command that should be executed when the Countdown finishes. |

## Working with Countdowns
for Countdowns to work you need to add a **[Text](/docs/components/UnityEngine.UI.Text.md)** Component to your Panel. your Text Component's content should include the string `%TIME_LEFT%`, which the Countdown will replace with the current Number.

Examples:
- `the Event will end in %TIME_LEFT% Seconds` => the Event Will end in 30 Seconds
- `Power-up Buff - %TIME_LEFT%s` => Power-up Buff - 30s

### Counting Up vs counting Down
- to count Down set your `startTime` higher than your `endTime` & set your `step` to at least 1.
- to count Up set your `startTime` lower than your `endTime`


**< [Previous Component](/docs/components/NeedsX.md)** | **[Back to Components](/docs/components/README.md)** 
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE1NzM2NTY1MTAsMjA4OTUwMzQ0NCwtMz
Q2MDc4ODcsLTE2OTg0OTg2MjcsMzcxNzUyMjE4LDUyOTg1OTk4
M119
-->