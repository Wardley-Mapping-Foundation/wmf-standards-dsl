# Component

Components represent capabilities of within the mapped context. They are the major building blocks of maps. 

## Syntax

	
### WMDL
	component <identifier> <position> <display-hints> <data>

e.g.

	component Cup [0.73, 0.78]
	component Cup [0.73, 0.78] {display:{icon:square, label:"[19, -4]"}} {data:{cost:1.34, currency: "EUR"}}

| Token                                   | Mandatory | Description                                                                                                           |
|-----------------------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------|
| component                               | y         | Identifies the expression type                                                                                        |
| [identifier](../tokens/Identifier.md)   | y         | Name of the component, used as an identifier to allow references from other map elements                              |
| [position](../tokens/Position.md)       | n         | Map coordinates of the component. If omitted [0, 0] is assumed.                                                       |
| [display-hints](../tokens/display-hint) | n         | Optional, contains hints on how to display this component for visual tools, e.g. the desired shape for this component |
| [data](../tokens/data)                  | n         | Optional, contains additional data that may be used in further analytics, e.g. to calculate the total cost of a flow. |

### OWM
	component <name> <position>
e.g.

	component Cup [0.73, 0.78]
	component Cup [0.73, 0.78] label [19, -4]

#### Differences to OWM
* WMDL adds support for additional [data](../tokens/data.md)
* WMDL adds support for visual tooling via [display hints](../tokens/display-hint.md). Shapes or icons can be defined for a components this way. 
* Labels are defined through [display-hints](../tokens/display-hint.md) 





