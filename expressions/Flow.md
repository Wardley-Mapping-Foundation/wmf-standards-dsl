# Flows between components

Edges on a Wardley Map represent some form of flow, the most fundamental is the flow of [needs](Need.md).
Other forms of flow can be represented, for example, flow of expense or cost, flow of income, flow of
investment, flow of risk, flow of C02 emissions, and constraints.  _(Note: this is not a complete list.)_

_TODO: refer to Simon's book._

A single flow connects two components together: starting from a **source** [component](Component.md), it flows
out to a **destination** component.  At this point, the destination may itself become a source as the flow
continues on to other components.  A single node may have zero, one, or many inflows & outflows, in any
combination of types.

Terminology:
 - **Origin:** where a flow starts.  This is a special type of source, from here there are only outflows.
   _Discuss: it may be easier to introduce a new type of component, eg: "Flow Origin" so that edges are
   never orphaned.  Otherwise, the orphaned edge could be considered the Origin.  Having a component is
   useful if the flow originates from the same place (eg: a purchase order, or invoice, or lump sum
   investment, or ...)_
 - **Source:** the component a flow leaves from.
 - **Destination:** the component a flow arrives at.
 - **Inflow:** from a destination component's perspective, a flow come in from a source component.
 - **Outflow:** from a source component's perspective, a flow goes out to a destination component.
 - **Flow path:** the total path of a flow across relevant components on the map, from origin to anchor.
 - **Magnitude:** a measure of the amount of flow between nodes, or the amount retained at an individual node.
 - **Unit:** the unit of measurement used for magnitudes of this type of flow (eg: dollars, euros, MtCO2e, etc.)
 - **Flow Calculation:** the calculation performed as a result of a flow between components.  E.g.:
   - When a capital flow leaves a component,
   - ... the net magnitude of the source MAY be reduced by the magnitude of the flow, and
   - ... the net magnitude of the destination MAY be increased by the magnitude of the flow
 - **Flow Principles:** principles governing the calculation of flows.  E.g.:
   - the net magnitude of a capital flow should equal that of its origin.

Flows can contain metadata that may impact the map, such as:
 - [delta visibility](../tokens/Visibility.md)
 - transaction data related to the flow (eg: forecasts, actuals, aggregate data, statistics, etc)
 - calculation algorithms
 - display properties & hints
 - etc.


# Inferring Flow
The flow of [needs](Need.md) can be used to infer other flows when data on the map is incomplete.  For example,
when only source data of flow of cost is available on leaf nodes, that cost can be assumed to flow in the
opposite direction of needs, along connected components to the map's anchor(s), splitting the magnitude of the
flow evenly wherever alternate paths are available.  _TODO: discuss in more detail._

## Default Flow Principle
The net magnitude of a flow across all components should not exceed the magnitude of the flow at its origin.

_TODO: It may be useful to refer to some algorithms here, but not limit to only them to avoid being prescriptive._
