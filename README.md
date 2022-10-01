# DRAFT - Wardley Mapping Description Language (WMDL) - DRAFT

The Wardley Mapping Description Language is based on [Simon Wardley's book](https://medium.com/wardleymaps) and subsequent revisions.  It provides a standard way of describing Wardley Maps that is user-friendly, accurate, extensible, and allows tool developers to create interoperable software systems.

See [Syntax](Syntax.md) for further details.

## User Needs
TODO - copy appropriate user needs from Miro.  These should be high-level, not a detailed list of 100 requirements.  Ensure they have outcome statements, eg:

    As a <user>
    I need <some activity or thing>
    So that <I can achieve this outcome>

WMDL should be used as a description language as well as an interchangeable format.  *- TODO: reconsider.  It likely makes sense to have a separate standard data format that the description language depends on.  Bear in mind more than one language may emerge from the data format.*

## Key features:
* Standardized language: Tools using WMDL should be able to produce interchangeable output such that toolchains consisting of various tools created b the community can be created
* Human readable: WMDL should be easily to write an understand by humans. Ultimately it should be usable in visual editors to quickly produce maps, e.g. in a collaborative mapping session
* Support for optional visual aids, e.g. advice on how to display a certain component in a visual editor (shape, color, ...)
* Support for optional data on map elements. Additional (meta) data can be used with structured queries and analysis.

## Map Elements

* [Component](expressions/Component.md)
* [Anchor](expressions/Anchor.md)
* [Link](expressions/Link.md)
* [Movement](expressions/Movement.md)
* [Inertia](expressions/Inertia.md)
* [Pipeline](expressions/Pipeline.md)
* [Map Metadata](expressions/Map%20Metadata.md)

## Grammar elements

* [Identifier](tokens/Identifier.md)
* [Position](tokens/Position.md)
* [Text](tokens/Text.md)

