In WMDL, the position of all [Map Elements](Elements.md), including [Components](Components.md),
[Advanced Elements](Advanced-Elements.md), and [Decorations](Decorations.md), can be suggested using a
coordinate system.

# Map Axes
To cater for different map display dimensions, axes MUST be represented using a number that represents the
percentage of the map's maximum available dimension.

_(TODO: discuss: are absolute coordinates outside max dimensions needed to create scrolling maps? if so, do we
want to cater for this?  is a property needed?)_.

## x-axis
By default, the x-axis of a Wardley map represents [Evolution](Evolution.md) of map [Components](Component.md).
TODO: how can this be overridden?

Visualisation engines MUST determine a mapping of x-axis to Evolution.

## y-axis
By default, the y-axis of a Wardley map represents [Visibility](Visibility.md) of map [Components](Component.md).
TODO: how can this be overridden?

Visualisation engines MUST determine a mapping of x-axis to Evolution.

## z-axis
By default, there is no z-axis of a Wardley map.

To cater for extensions of WMDL, a z-dimension MAY be defined to represent the magnitude of another attribute:

    z-axis label: <string>

E.g.:

    z-axis label: "Maturity"

# Position of Components
The position of a component on a Wardley map MUST be determined by:

1. mapping the component's stage of [Evolution](Evolution.md) onto the Evolution axis
2. mapping the component's calculated [Visibility](Visibility.md) onto the Visibility axis
3. applying any available Position hints

## Position hints
A Component's position MAY be _suggested_ using `x,y` coordinates.

The following formats are supported:

    x: <number>, y: <number>
    x: <number>, y: <number>, z: <number>

    [<x number>, <y number>]
    [<x number>, <y number>, <z number>]

e.g.:

    x: 16, y: 29
    [16,29]

    y: 29, x: 16, z: 33
    [16,29,33]

The visualisation engine SHOULD interpret these as a rendering _suggestion_, rather than a requirement.

# Position of Labels, Decorations & Advanced Elements
The position of a [Component's label](Component.md), [Advanced Elements](Advanced-Elements.md), and
[Decorations](Decorations.md) MAY be suggested in one of three ways:

## 1. absolute coordinates
Specific x & y coordinates MUST be specified using the same formats described above.

If a dimension is not specified, the same dimension of the map element's parent SHOULD be used if available.

## 2. relative coordinates
Relative x & y coordinates MUST be specified using the same formats described above, with the addition of:

 - `+` specified increment
 - `-` specified decrement

E.g.:

    x: +3, y: -2
    [+3,-2]

If a dimension is not specified, the same dimension of the map element's parent SHOULD be used if available.
E.g.:

    [+3]

The `x` coordinate should be determined as `parent.x + 3`, whereas the `y` coordinate should be `parent.y`.

## 3. relative horizontal & vertical alignment

Relative alignment to the parent element's position MUST be specified as follows:

    align: <value>

Valid alignments include:
|        | left         |     center      |         right |
|--------|:-------------|:---------------:|--------------:|
| top    | top-left     |   top-center    |     top-right |
| middle | middle-left  |  middle-center  |  middle-right |
| bottom | bottom-left  |  bottom-center  |  bottom-right |

e.g.:

    align: top-left

Where only a vertical alignment is provided, the visualisation engine SHOULD choose the most appropriate
horizontal alignment.  Similarly, where only a horizontal alignment is provided, the visualisation engine
SHOULD choose the most appropriate horizontal alignment.

In cases where there is no parent element, the visualisation engine SHOULD calculate position relative to
the map itself.
