# Evolution
Evolution, as defined by Simon Wardley in [Wardley Maps Chapter 7 - Finding a new purpose](https://medium.com/wardleymaps/finding-a-new-purpose-8c60c9484d3b),
is an approximate measure of:
- certainty: "how complete, well understood and fit for purpose it is"
- ubiquity: "adoption in its ‘ubiquitous’ market"

It is expressed linearly on a single axis of four (4) stages:

| Stage                                   |      I     |     II     |         III         |            IV          |
|-----------------------------------------|------------|------------|---------------------|------------------------|
| [Activity](../expression/activity.md)   | Genesis    | Custom     | Product _(+Rental)_ | Commodity _(+Utility)_ |
| [Practice](../expression/practice.md)   | Novel      | Emerging   | Good                | Best                   |
| [Data](../expression/data.md)           | Unmodelled | Divergent  | Convergent          | Modelled               |
| [Knowledge](../expression/knowledge.md) | Concept    | Hypothesis | Theory              | Accepted               |

_Table 1. Based on: [Wardley Maps Chapter 2 - Finding a path](https://medium.com/wardleymaps/finding-a-path-cdb1249078c0)_

# WDSL
In WDSL, Evolution MUST be expressed in one of three ways:

## 1. Representing Evolution as a Roman Numeral
Evolution MAY be represented as a roman numeral from Table 1, i.e.:
 - "I" or "Stage I"
 - "II" or "Stage II"
 - "III" or "Stage III"
 - "IV" or "Stage IV"

## 2. Representing Evolution as a Stage Name
Evolution MAY be represented as a string from Table 1 representing a Stage, e.g.:
 - "Genesis", "Novel", "Unmodelled", "Concept"
 - "Custom", "Emerging", "Divergent", "Hypothesis"
 - "Product", "Product +Rental", "Good", "Convergent", "Theory"
 - "Commodity", "Commodity +Utility", "Utility", "Best", "Modelled", "Accepted"

## 3. Representing Evolution as a decimal number
Evolution MAY be represented as a positive decimal number between 0.0 - 4.0 representing a Stage, where the decimal
represents the approximate level of evolution within a Stage.

The decimal MUST be interpreted by the ranges defined below:

    1.0  ≤  n  <  2.0  ≤  n  <  3.0  ≤  n  <  4.0  ≤  n  <  5.0
     |             |             |             |             |
     +-------------+-------------+-------------+-------------+
     |   Stage I   |   Stage II  |  Stage III  |   Stage IV  |
     +-------------+-------------+-------------+-------------+

The decimal value SHOULD be limited to a single place to avoid implying a false sense of accuracy, i.e: "1.1", not "1.137".

Evolution MUST NOT be stored as a percentage or a coordinate on the x-axis.  While doing so may make it easier to calculate
an x coordinate for display purposes, it makes it much harder for a human to both represent & interpret a component's stage
of evolution.  [Position hints](position.md) should be used instead.

## Evolution as x-axis of a map
Evolution is typically used to define the x-axis of a Wardley map.  In this case, Evolution SHOULD be mapped onto the
x-axis as follows:

     1.0                  Stage of Evolution                 5.0
      |                                                       |
      |                                                       |
    x=0 -----------------------x-axis----------------------> max(x)

Note that there may not be a 1:1 mapping between Stage coordinate and x coordinate.  For example, if the visualisation
engine decides to place Stage boundaries at irregular intervals to maximise readability of a map.

### Determining position of a component on x-axis using Evolution
Evolution is by nature an approximate estimation.  As such, when interpreted as a [Position](position.md) on the x-axis of
a map, the precise x co-ordinate SHOULD be approximated by the visualisation engine using the above mapping.
Visualisation engines SHOULD attempt to avoid unnecessary clutter by preventing map components from overlapping.

Where an approximate level of evolution within a Stage is not available (eg: "Stage I"), it SHOULD be interpreted as in the
middle of the Stage.

# Deriving Evolution
## Ubiquity & Certainty
In the future, guidance may be written on how to derive evolution from information containing ubiquity & certainty measures
(including estimates).  Please contact us if you are interested in helping with this.

## Characteristics
In the future, guidance may be written on how to derive evolution from the various characteristics published in Simon Wardley's
[Cheat Sheet (Figure 17)](https://medium.com/wardleymaps/finding-a-path-cdb1249078c0).  Please contact us if you are interested
in helping with this.
