# Radiator Architecture Research Pass 01

## Decision

Keep the three-temperature-loop concept, but reject the current radiator estimate as incomplete until geometry, mass, damage tolerance, orientation, and replacement throughput are modeled.

The ship should use segmented solid radiators as the primary system. Liquid-droplet radiators remain a secondary research option for high-temperature industrial or propulsion heat because they reduce puncture sensitivity but add fluid-loss, collection, contamination, and control risks.

## Evidence extracted

### 1. Area is only the first calculation

Radiator performance depends on rejection temperature, emissivity, view to cold space, solar and planetary heat input, mutual irradiation between panels, shadowing by the ship, and fluid-loop temperature drop.

Large two-sided radiators require deployment or permanent stand-off geometry. Closely packed panels cannot all be credited at ideal black-space performance.

### 2. Segmentation is mandatory

Real spacecraft radiators have been fully penetrated by micrometeoroid or debris impacts. Large worldship radiators must therefore be divided into independently valved cells with leak detection and automatic isolation.

Adopt provisionally:

- no single puncture may disable more than 0.1% of total rejection capacity
- no shared header may disable more than 2%
- each thermal loop must survive loss of 25% of installed area at reduced load
- fluid inventory lost from one isolated cell must be locally bounded

### 3. Protect the transport lines

Radiator fluid pipes are more vulnerable than passive panel surface. Research on crewed-spacecraft radiators shows that hiding pipes behind panel structure and adding local shielding can materially increase impact resistance without necessarily increasing total panel mass.

Adopt recessed transport tubes, bumper layers, redundant flow paths, and dry-disconnect interfaces between panel modules.

### 4. Low-temperature rejection is the geometry driver

The 300–315 K loop requires hundreds of thousands of square metres per habitat. It should use large permanent wings or distributed panel forests positioned well outside the rotating pressure hull's thermal and debris shadow.

The medium- and high-temperature loops can be much smaller and should remain physically separated so a hot-loop failure cannot boil or contaminate the habitat loop.

### 5. Turndown must be designed

A radiator sized for maximum load can overcool during shutdowns, eclipse-like shadowing, maintenance, or reduced population operation. Existing thermal-control research uses variable conductance, bypasses, louvers, morphing surfaces, freeze-tolerant loops, and thermal storage.

Adopt:

- variable-flow bypass around panel banks
- freeze-tolerant or nonfreezing working fluids by loop
- thermal storage for short interruptions
- passive minimum-flow paths for decay heat and life support
- independent control of each panel bank

### 6. Centralized and distributed systems both have roles

Centralized rejection can reduce mass, but a civilization-scale vessel cannot tolerate one common thermal spine. Use locally independent habitat loops feeding many radiator banks, plus separate stationary-spine loops for propulsion, reactors, and heavy industry.

No routine habitat survival load may require a rotary fluid joint.

## Provisional architecture

Per habitat:

- low-temperature loop: 300–315 K, 200 MW design load
- medium-temperature loop: 500–550 K, 300 MW design load
- high-temperature loop: 750–900 K, 120 MW design load
- at least four geographically separated radiator fields per loop
- 25% installed capacity reserve after view-factor and degradation losses
- replaceable panel modules with isolated local headers
- robotic exterior inspection and patching
- stored replacement panels equal to at least 2% of installed area, with onboard manufacture covering the rest

Ship-wide stationary systems retain separate propulsion and industrial radiator fields. Their capacity must be added to the two habitat systems rather than folded into them.

## Open calculations

1. Full three-dimensional radiator placement and view factors
2. Solar-distance operating envelope across the intended solar-system mission
3. Panel areal mass, support-truss mass, coolant mass, pump power, and deployment mass
4. Micrometeoroid and debris puncture rate by panel area and location
5. Working-fluid loss per puncture and annual replenishment demand
6. Panel manufacture and replacement rate
7. Thermal response after 10%, 25%, and 50% area loss
8. Interaction between radiator geometry, thrust direction, docking, mining traffic, and rotating habitats

## Rejected shortcuts

- Credit ideal Stefan-Boltzmann area without view-factor losses
- Put all habitat heat through one centralized loop
- Assume radiator punctures are rare enough to ignore
- Treat 10% spare panels as sufficient without a failure-rate model
- Use liquid-droplet radiators as the sole survival heat sink

## Sources

- NASA, *STS-118 Radiator Impact Damage*: https://ntrs.nasa.gov/citations/20080010742
- NASA, *Review of Advanced Radiator Technologies*: https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/19940032314.pdf
- NASA, *Liquid Droplet Radiator Development Status*: https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/19870010920.pdf
- NASA, *A Multi-Environment Thermal Control System With Freeze-Tolerant Radiator*: https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/20130011331.pdf
- NASA, *A Morphing Radiator for High-Turndown Thermal Control*: https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/20140006701.pdf
- ESA, *Protection of Manned Spacecraft Radiator from Space Debris*: https://conference.sdo.esoc.esa.int/proceedings/sdc7/paper/340
- ESA, *Current and Future Techniques for Spacecraft Thermal Control*: https://www.esa.int/esapub/bulletin/bullet87/paroli87.htm

## Status

Radiator thermal capacity is plausible, but the radiator system remains unclosed until its geometry and mass are integrated into the master ship model.
