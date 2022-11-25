# Component

A network of components represents the landscape of the map (TODO: refer to Simon's book).  They come in many
different [types](Component-Types.md).

## Syntax
	<component-identifier> <evolution> <flows> <display-hints> <data>
	-or-
	<component-type> <component-identifier> <evolution> <flows> <display-hints> <data>

e.g.

	Tea [Stage III]

	Cup [3.4] {
	  needs: porcelain, mold, kiln [5]
	}
	
	practice MTTR [4.1] {
	  needs: asset, maintenance, statistics
	  capital-flow: { rule: split-evenly }
	  label: "Mean Time to Repair" position: top-left
	  data: { link: "https://github.com/Wardley-Mapping-Foundation" }
	  display: { icon:square }
	}

	capital PO123 [II] {
	  capital-flow: MTTR[100%]
	  data: {cost:1.34, currency: "EUR"}
	  position: [23, 49]
	}

| Token                                   | Mandatory | Description                                                                                                           |
|-----------------------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------|
| component-type                          | n         | Optional. Identifies the [type](Component-Types.md) of component.  Defaults to [Activity](Activity.md)                |
| [identifier](../tokens/Identifier.md)   | y         | Unique identifier to allow references from other map elements.  Doubles as _label_ unless specified.                  |
| [evolution](../tokens/Evolution.md)     | y         | Evolution of the component.                                                                                           |
| [flows](../tokens/Flow.md)              | n         | Optional, any **outflows** to other components, such as [Needs](Need.md) or [Capital](Capital.md).                    |
| [future](../tokens/Future.md)           | n         | Optional, describes if this is component is anticipated for the future.  Defaults to `FALSE`.                         |
| [position-hints](../tokens/Position.md) | n         | Optional, contains hints on how to [position](../tokens/Position.md) this component for visual tools.                 |
| [display-hints](../tokens/display-hint) | n         | Optional, contains hints on how to display this component for visual tools, e.g. the desired shape for this component |
| [data](../tokens/data)                  | n         | Optional, contains additional data that may be used in further analytics, e.g. to calculate the total cost of a flow. |

## OWM Comparison
	component <name> <position>
e.g.

	component Cup [0.73, 0.78]
	component Cup [0.73, 0.78] label [19, -4]

### Differences to OWM
WMDL...
* groups flows with components
* specifies [evolution](../tokens/Evolution.md) & [delta visibility](../tokens/Visibility.md), not x,y coordinates
* supports multiple component types
* supports multiple flows
* supports relative positions
* support additional [data](../tokens/data.md)
* supports [display hints](../tokens/display-hint.md) for things like shapes, icons, colours, etc.
