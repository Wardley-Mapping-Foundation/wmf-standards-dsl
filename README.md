# WMDL - Wardley Mapping Description Language

The Wardley Map description language (WMDL) is based on the grammar used by Onlinewardleymaps.com. 
Though widely used and capable of basically describing Wardley Maps, the OWM grammar itself lacks desirable features
and is not yet described formally. 

In order to allow for tool developers to create interoperable software systems, 
a standardized language is needed. WMDL aims to become that standard by building upon the foundation of OWM. 

WMDL should be used as a description language as well as an interchangeable format. 

See [Syntax](Syntax.md) for further details.

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

