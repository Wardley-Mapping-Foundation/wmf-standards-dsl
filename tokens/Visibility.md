TODO: define visibility, referring to Simon's book.

# Visibility of Components
## Delta Visibility
In WMDL, a [Component's](Component.md) vertical position on a map MUST be determined by scanning all of the component's
inward-facing [Needs](Need.md) (i.e.: map flows of other components that need this component), and use their
`delta-visibility` (`dv`) properties to calculate a position on the y-axis that is relative to the other components.
This may then be influenced by any [Position hints](Position.md) of the component itself.

Delta Visibility can be thought of as a _forcing function_: how much a higher-order component pushes lower order
components down the map.  It allows maps to be automatically visualised, which is often required when the
[Anchor](Anchor.md) is not pre-determined.

By default, delta visibility is set to `1`.
Valid range: `0 - 100`
