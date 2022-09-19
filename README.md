The Wardley Map description language (WMDL) is based on the grmmar used by Onlinewardleymaps.com. Though widely used an capable of basically  describing Wardley Maps the grammar itself lacks desirable features and is not described formally. 

In order to allow for tool developers to create interoperable software systems a standardized language is needed. There fore the OWM grammar should be formalized and extended to form a standard. 

The WMDL should be used as a description language as well as an interchangeable format.

# Enhancements to the OWM grammar
* OWM does not support additional data on map elements, e.g. data for further analysis like the cost of a component. WMDL should offer this. The suggested format is to have a json-like key-value structure, e.g.:

		component foo [0.75, 0.6] {cost: 123.0, technology: 'existent'};

See [Syntax](syntax.md) for further details.


# Map Elements

* [Component](expressions/Component.md)
* [Anchor](expressions/Anchor.md)
* [Link](expressions/Link.md)
* [Movement](expressions/Movement.md)
* [Inertia](expressions/Inertia.md)
* [Pipeline](expressions/Pipeline.md)
* [Map Metadata](expressions/Map%20Metadata.md)

# Grammar elements

* [Identifier](tokens/Identifier.md)
* [Position](tokens/Position.md)
* [Text](tokens/Text.md)

