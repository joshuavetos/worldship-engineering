# Radiator Architecture Research Pass 03

## Purpose

Convert the radiator problem from an area estimate into a first-order geometric and environmental model.

## Decisive finding

The previous statement that radiator farms can simply sit near the rotating habitat axis is incomplete. A radiator attached to the rotating habitat will repeatedly change its orientation to the Sun unless it is actively gimbaled or kept inside a permanent shadow geometry.

For the low-temperature loop, direct sunlight can erase most or all useful heat rejection.

## First-order thermal equation

For a radiator surface:

`q_net = epsilon * sigma * T^4 * F_space - alpha * S_1AU / r_AU^2 * cos(theta) - q_mutual - q_planetary`

Where:

- `epsilon` is infrared emissivity
- `alpha` is solar absorptivity
- `F_space` is the unobstructed view factor to cold space
- `r_AU` is solar distance in astronomical units
- `theta` is solar incidence angle
- `q_mutual` is radiation received from the ship and neighboring panels

NASA thermal analysis explicitly treats solar distance, incidence angle, absorptivity-to-emissivity ratio, and view factor to space as governing variables.

## First-order flux check

Assume emissivity 0.9 and ignore mutual irradiation:

| Radiator temperature | Ideal emitted flux |
|---|---:|
| 300 K | about 413 W/m2 |
| 315 K | about 503 W/m2 |
| 525 K | about 3,880 W/m2 |
| 825 K | about 23,600 W/m2 |

At 1 AU, solar irradiance is about 1,361 W/m2. With a good low-alpha coating at `alpha = 0.10`, a Sun-facing surface absorbs about 136 W/m2. At 0.5 AU that rises to about 544 W/m2.

Therefore:

- a 300 K radiator cannot operate Sun-facing at 0.5 AU
- even at 1 AU, direct sunlight removes roughly one-third of ideal low-temperature rejection
- medium- and high-temperature radiators are less sensitive, but their coatings and structures still absorb heat

## Architecture correction

Adopt the following baseline pending detailed modeling:

1. Each rotating habitat retains its own closed survival coolant loops.
2. Radiator farms sit near the habitat axis to reduce centrifugal loading.
3. Low-temperature farms operate behind dedicated Sun shields.
4. Each farm uses gimbaled or hinged radiator leaves that counter-rotate relative to the habitat and hold a controlled orientation to deep space.
5. No single gimbal, shield, or support boom serves more than one radiator farm.
6. Medium- and high-temperature fields may tolerate wider incidence angles but still receive independent pointing control.
7. The stationary spine receives separate radiator fields for propulsion and heavy industry.

This preserves habitat thermal independence without forcing survival coolant through rotary joints.

## Geometric model requirements

The eventual 3D model must include:

- two rotating cylinders and end caps
- stationary spine, reactor clusters, engines, cargo, and shielding
- all twelve radiator farms per habitat
- Sun shields and radiator articulation ranges
- self-shadowing and eclipses caused by the ship
- radiator-to-radiator view factors
- radiator view factors to warm hull surfaces
- plume and debris exclusion cones
- mining, docking, and maintenance approach corridors
- panel replacement clearances

ESA and NASA thermal work both show that complex geometry requires numerical view-factor methods rather than simple projected-area assumptions.

## Coolant network model

For every loop, calculate:

- branch length and diameter
- mass flow
- inlet and outlet temperature
- pressure loss
- pump power
- valve failure states
- flow stagnation
- isolated-panel behavior
- coolant inventory lost per puncture
- restart after branch isolation

Pressure drop is not a standalone pass/fail number. The actual criterion is whether served equipment remains inside its temperature limits.

## Operating cases

The thermal model must run at minimum:

- 0.5 AU, 1 AU, 5 AU, and 30 AU
- normal habitat load
- agriculture peak
- one reactor trip
- emergency survival mode
- full propulsion cruise
- 25% radiator-area loss
- one complete farm unavailable
- frozen gimbal at worst orientation
- degraded coating absorptivity and emissivity

## New mission constraint

Until the model proves otherwise, sustained operation inside 0.5 AU is not part of the baseline mission envelope. Inner-system operations require either larger Sun shields, a different attitude, curtailed power, or temporary heat storage.

## Verification targets

The radiator architecture closes only if it demonstrates:

- all survival loads remain thermally stable after loss of 25% installed area
- no single pointing or shielding failure removes more than one farm
- low-temperature fields maintain adequate net rejection at the minimum permitted solar distance
- pumping power remains inside the Volume IV electrical budget
- replacement throughput exceeds expected puncture and degradation rates
- no radiator geometry blocks propulsion, docking, mining, or rescue operations

## Decision

Keep twelve segmented farms per habitat, but revise them from fixed near-axis panels to independently shielded and articulated radiator farms.

The radiator area estimate remains provisional. Solar orientation and view-factor losses may increase the required area substantially, especially for the 300–315 K loop.

## Primary references

- NASA, *An Analysis and Procedure for Determining Space Environmental Sink Temperatures With Selected Computational Results*.
- NASA, *Mathematical Analysis of Space Radiator Segmenting for Increased Reliability and Reduced Mass*.
- NASA/JPL, mechanically pumped fluid-loop pressure-drop and temperature sensitivity studies.
- NASA, *Analytical Investigation of Pumped Fluid Loop Radiators for Orion Spacecraft*.
- ESA, thermal-control guidance and numerical view-factor modeling resources.
