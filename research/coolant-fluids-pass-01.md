# Coolant Fluids Pass 01

## Decision

Adopt a three-tier coolant architecture rather than one universal fluid.

### Low-temperature habitat loop

- Internal collection fluid: treated water or water-glycol in crewed spaces.
- External radiator fluid: ammonia in fully isolated, double-wall loops.
- Normal operating band: roughly 285–320 K.
- Rationale: water is safe and has high heat capacity inside inhabited volume; ammonia has extensive spacecraft heritage, low freezing temperature, and strong two-phase heat transport performance outside the pressure vessel.

### Medium-temperature power-rejection loop

- Baseline transport fluid: NaK-78 in sealed, low-pressure pumped loops.
- Normal operating band: roughly 450–650 K.
- Radiator interface: liquid-metal loop feeding isolated heat-pipe panels.
- Rationale: NASA studies treat NaK as suitable from about 300–1000 K and specifically pair it with Brayton-cycle radiator systems in the 400–600 K range.

### High-temperature reactor and industrial loop

- Primary transport: NaK or sodium, selected by detailed materials and freeze-management study.
- Radiator working fluid: potassium or sodium heat pipes.
- Normal operating band: roughly 750–950 K.
- Rationale: liquid-metal heat pipes and pumped loops have direct experimental and long-duration test heritage at these temperatures.

## Architecture rules

1. No toxic or chemically aggressive coolant enters occupied volume.
2. Every crewed-space loop transfers heat through an intermediate heat exchanger before external rejection.
3. Ammonia, NaK, sodium, and potassium loops require double containment, leak detection, drain tanks, isolation valves, and remotely replaceable pump modules.
4. No common manifold may connect low-, medium-, and high-temperature loops.
5. Every radiator farm must be able to drain or freeze into a known safe state after isolation.
6. NaK systems require oxygen monitoring, cold traps, purification, and strict material-compatibility control.
7. Heat pipes remain locally redundant so a puncture does not empty an entire pumped loop.

## Rejected options

- One universal water loop: safe but becomes high-pressure at medium temperatures and vulnerable to freezing externally.
- One universal ammonia loop: useful at low temperature but inappropriate near inhabited spaces and insufficient for the highest-temperature duties.
- Organic oils as the main century-scale baseline: attractive at moderate temperatures, but long-term radiation and thermal degradation create a difficult replacement and purification burden.
- Liquid-droplet radiators as the primary system: lower structural mass is possible, but fluid-loss, contamination, capture, and maneuver constraints remain too severe for the survival baseline.

## Consequences

- The earlier generic “low, medium, high loop” wording is replaced with fluid-specific systems.
- Medium and high loops move to the stationary spine wherever possible.
- Habitat low-temperature rejection remains locally autonomous.
- A dedicated alkali-metal handling shop, purification line, and emergency drain infrastructure become mandatory.
- Radiator mass estimates must now include dual-loop heat exchangers, containment, drain tanks, cold traps, pumps, and spare coolant.

## Open verification work

- exact pressure, flow, pipe diameter, and pumping power for each loop
- materials compatibility over 100-year service intervals
- ammonia inventory and toxic-leak consequence model
- NaK fire and vacuum-leak behavior
- freeze-thaw startup procedure for each radiator farm
- coolant make-up and purification throughput
- heat-exchanger approach temperatures and resulting radiator-area penalty

## Sources

- NASA, ISS Active Thermal Control Subsystem using liquid ammonia: https://ntrs.nasa.gov/citations/20110023292
- ESA, Orion European Service Module thermal control using HFE-7200: https://www.esa.int/Science_Exploration/Human_and_Robotic_Exploration/Orion/European_Service_Module_Temperature_control
- NASA, comparison of NaK and water coolant options for Brayton heat rejection: https://ntrs.nasa.gov/citations/20060008935
- NASA, NaK-based Brayton heat-rejection concepts: https://ntrs.nasa.gov/search.jsp?R=20050160234
- NASA, advanced 600 K and 875 K radiator concepts: https://ntrs.nasa.gov/search.jsp?R=19900050987
- NASA, ten-year sodium heat-pipe life test: https://ntrs.nasa.gov/citations/20120013208
- NASA, NaK contamination monitoring and purification: https://ntrs.nasa.gov/citations/20110022666
