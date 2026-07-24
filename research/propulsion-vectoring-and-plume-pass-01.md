# Propulsion Vectoring and Plume Interaction Pass 01

## Question
Can the ship preserve its Sun-pointing thermal attitude while performing useful long-duration electric-propulsion burns?

## Findings

1. Electric thruster pointing mechanisms are real and can support long firings, but their range is finite. ESA has flown and tested mechanisms that point electric thrusters during burns lasting from hours to months. A historical NASA ion-thruster subsystem used approximately ±10° thrust-vector deflection.

2. Plume interaction is not a cosmetic issue. NASA plume-analysis tools model sputter erosion, redeposition, surface heating, induced torque, and changes to exposed surface properties. Large flexible structures can also be dynamically excited by impingement loads.

3. Gimbals do not solve arbitrary trajectory steering while the entire ship remains inside a narrow thermal cone. If full-power habitat cooling requires the spin axis to stay within about 5° of the Sun line, a ±10–15° thruster gimbal only permits sustained thrust vectors near that same axis.

## Provisional architecture

- Eight electrically independent main propulsion clusters on the nonrotating spine.
- Four clusters near the forward quarter and four near the aft quarter.
- Each cluster mounted on a two-axis gimbal with a provisional mechanical range of ±15°.
- Normal cruise uses symmetric clusters so the net thrust line passes through the ship center of mass.
- Differential thrust supplies slow attitude trim and unloads control moment systems.
- Small independent attitude-control thrusters handle startup, shutdown, docking, and off-nominal cases.
- No main-plume line may intersect a habitat, radiator, solar shield, mining craft berth, sensor mast, or another thruster mechanism through the full gimbal envelope.

## Decisive consequence

The current thermal rule and propulsion rule do not yet close together.

With:

- full-power thermal attitude limited to roughly ±5° from the Sun line, and
- main thruster vectoring limited provisionally to ±15°,

sustained high-power thrust is restricted to a narrow cone around the Sun line. That is acceptable for some radial spirals and energy-changing maneuvers, but not for arbitrary solar-system transfers.

One of the following must eventually change:

1. widen the radiator thermal-attitude envelope;
2. permit lower-power burns at larger Sun angles;
3. add independently pointed thermal shields or radiator assemblies;
4. use mission trajectories that respect the thrust cone;
5. separate the propulsion spine attitude from habitat thermal attitude through a major articulated structural joint.

Option 5 is rejected provisionally because it creates an enormous moving structural, electrical, docking, and control interface between multi-million-tonne sections.

## Provisional operating modes

| Mode | Sun-axis error | Main thrust use |
|---|---:|---|
| Full cruise | 0–5° | Up to full 500 MW propulsion input |
| Reduced cruise | 5–15° | Thrust and habitat discretionary loads reduced |
| Reorientation | 15–30° | Short duration only; propulsion and industry curtailed |
| Off-cone maneuver | >30° | No sustained main burn under present thermal baseline |

These limits remain placeholders pending the 3D radiator and trajectory model.

## Plume-clearance rules

- Every gimbal envelope receives a 3D exclusion cone with margin for plume divergence and charge-exchange ions.
- Radiator surfaces must remain outside both direct plume and modeled back-sputter zones.
- Docking and mining operations inhibit affected thrusters automatically.
- The controller must reallocate thrust after a stuck, inhibited, or failed cluster.
- Surface witness coupons and plume diagnostics monitor erosion and redeposition over time.
- Replaceable sacrificial shields protect unavoidable near-field structures.

## Structural torque

At the accepted total thrust of about 13 kN, an off-axis error creates torque according to:

`torque = thrust × lateral offset`

Examples:

- 1 m offset: 13 kN·m
- 10 m offset: 130 kN·m
- 50 m offset: 650 kN·m

These torques are small relative to the ship's mass but can accumulate angular momentum over months. Continuous center-of-mass estimation, symmetric thrusting, and differential cluster control are therefore mandatory.

## Burn-duration implication

The ship's accepted acceleration is only about 3.2×10^-7 m/s². A 1 km/s velocity change takes roughly 99 years at full thrust. Any reduced-power or off-cone mode proportionally increases that time. Thermal attitude is therefore a mission-design constraint, not a temporary operational inconvenience.

## Decision

Adopt distributed gimbaled propulsion clusters, but do not claim general trajectory freedom.

The ship currently supports long-duration thrust only inside a narrow Sun-referenced cone. The propulsion system remains plausible but unclosed until a trajectory study proves that useful solar-system missions can be flown within that cone or the radiator architecture is widened.

## Required next model

Build a coupled trajectory and thermal-attitude study that outputs:

- required thrust-vector angle versus time;
- radiator solar incidence versus time;
- full-, reduced-, and zero-thrust intervals;
- total transfer duration and propellant use;
- cluster outages and reallocation;
- plume-clearance violations;
- accumulated attitude-control momentum;
- feasible transfers between representative inner- and outer-system destinations.

## Sources consulted

- ESA, Pointing mechanism for electric thruster.
- NASA NTRS, Engineering model 8-cm thruster subsystem.
- NASA NTRS, Electric Propulsion Interactions Code.
- NASA NTRS, Autonomous Constrained Control for Arbitrary Thruster Configurations of Gimbaling Thrusters in SE(3).
- NASA NTRS, Space Station flexible dynamics under plume impingement.
