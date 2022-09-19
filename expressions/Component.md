# Syntax

Components represent capabilities of within the mapped context. They are the major building blocks of maps. 
	
## WMDL
	component <identifier> <position> <display-hints> <data>

e.g.

	component Cup [0.73, 0.78]
	component Cup [0.73, 0.78] {display:{label:"[19, -4]", icon:square}} {data:{cost:1.34, currency: "EUR"}}

## OWM
	component <name> <position>
e.g.

	component Cup [0.73, 0.78]
	component Cup [0.73, 0.78] label [19, -4]


| Token                                | Mandatory | Description                                                                                                           |
|--------------------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------|
| component                            | y         | Identifies the expression type                                                                                        |
| [identifier](identifier.md)          | y         | Name of the component, used as an identifier to allow references from other map elements                              |
| [position](position.md)              | n         | Map coordinates of the component. If ommitted [0, 0] is assumed.                                                      |
| [display-hints](tokens/display-hint) | n         | Optional, contains hints on how to dispaly this component for visual tools, e.g. the desired shape for this component |
| [data](tokens/data)                  | n         | Optional, contains additional data that may be used in further analytics, e.g. to calculate the total cost of a flow. |





