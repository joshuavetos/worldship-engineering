# Radiator Architecture Research Pass 02

## Decision

Retain segmented solid radiators as the primary system, but divide them into physically separated low-, medium-, and high-temperature fields with independent manifolds, shielding, and replacement access.

## Evidence extracted

- NASA analysis of segmented radiators shows that many independently operating segments localize micrometeoroid damage and can reduce required wall thickness and mass.
- Shuttle radiator hardware has been fully penetrated by micrometeoroid or debris impact, confirming that puncture is a normal design case rather than an exotic catastrophe.
- Heritage pumped-loop radiators for Space Station Freedom were estimated at about 7.8 kg/m² and used two independent coolant loops.
- NASA and ESA thermal-control work shows that useful radiator capacity depends on sink temperature, solar and planetary exposure, view factor, orientation, optical coatings, and deployment geometry.
- Variable-emissivity or morphing radiators can improve turndown, but remain secondary controls rather than the sole survival system.
- Liquid-droplet radiators may offer lower mass at high temperature, but introduce fluid recovery, contamination, electrostatic deflection, and maneuvering risks.

## Preliminary mass bound

Volume IV assigns roughly 340,000–440,000 m² of radiating surface per habitat.

Using the 7.8 kg/m² heritage figure as a rough lower-level comparison gives:

- 340,000 m²: 2,650 t per habitat
- 440,000 m²: 3,430 t per habitat
- both habitats: 5,300–6,860 t before major support booms, armored manifolds, deployment hardware, pumps, spare panels, and shielding

This mass is small relative to the 28 Mt rotating-habitat mass, but it is not negligible and must enter the master ledger.

## Geometry baseline

Each habitat receives twelve radiator farms:

- four low-temperature farms
- four medium-temperature farms
- four high-temperature farms

Each farm is broken into replaceable panels connected through isolated branch manifolds. No single branch may contain more than 0.1% of total habitat rejection capacity.

The fields should be mounted near the habitat axis on rotating structural trusses rather than at the 250 m rim. This reduces centrifugal structural load and keeps habitat survival loops entirely on the rotating side of the bearing interface.

The radiator farms extend axially and radially away from the pressure hull, with spacing selected by numerical view-factor analysis. They require sunshades or directional optical surfaces for inner-system operation.

## Operational rules

- A habitat must reject its survival heat without any rotary fluid joint.
- Losing one complete radiator farm must not force immediate abandonment.
- Losing 25% of installed area must remain survivable after automatic load shedding.
- Coolant trunks are armored, recessed, and duplicated before branching into exposed panels.
- Panel isolation must occur automatically after pressure-drop or flow-anomaly detection.
- Replacement panels must be installable robotically without shutting down the entire loop.
- Radiator farms must be separated far enough that one debris cone, fire, or structural fracture cannot disable adjacent farms.

## Required simulation

The next thermal model must calculate:

1. three-dimensional ship geometry and mutual view factors
2. solar input from roughly 0.7 to 10 AU operating distance
3. shadowing by habitats, shielding, propulsion structures, and other radiator fields
4. radiator temperatures and coolant pressure drops
5. boom, manifold, pump, shielding, and panel mass
6. puncture frequency and lost-area distribution
7. robotic replacement rate and spare-panel consumption
8. thermal response after reactor trips, pump failures, and sudden 25% area loss

## Status

The radiator concept is now architecturally plausible, but thermal closure remains provisional until the geometry and mass model exists.

## Primary references

- NASA, Mathematical Analysis of Space Radiator Segmenting for Increased Reliability and Reduced Mass, 2001.
- NASA, STS-118 Radiator Impact Damage, 2008.
- NASA, Design and Performance of Space Station Photovoltaic Radiators, 1995.
- NASA, Review of Advanced Radiator Technologies for Spacecraft Power Systems and Space Thermal Control, 1994.
- ESA, Thermal Control overview and BepiColombo radiator engineering.
