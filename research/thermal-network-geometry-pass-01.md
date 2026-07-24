# Thermal Network Geometry Pass 01

## Scope

This pass converts the provisional thermal-hydraulic numbers into a physical routing concept and checks the previous radiator-orientation assumptions for contradictions.

## Critical correction

The earlier idea of continuously counter-rotating or Sun-tracking habitat radiators conflicts with the rule that survival coolant must not cross rotary fluid joints.

A radiator attached to a habitat spinning at 1.89 rpm cannot remain inertially fixed without either:

- a continuous rotary fluid joint,
- a non-fluid thermal transfer interface,
- or a geometry that does not require inertial tracking.

The selected baseline is therefore an **axisymmetric, co-rotating radiator arrangement** rather than continuously counter-rotating radiator farms.

## Selected geometry

Per rotating habitat:

- radiator assemblies remain mechanically and hydraulically part of the rotating habitat
- the habitat spin axis is kept approximately Sun-pointed during normal cruise and settlement operations
- annular Sun shields are placed sunward of the radiator zone
- radiator panels extend axially and radially behind those shields
- multiple fins are distributed around 360 degrees, so habitat rotation does not materially change the thermal geometry
- low-, medium-, and high-temperature farms remain physically separated
- no normal or emergency habitat heat-rejection path crosses a rotary fluid joint

This preserves coolant continuity while avoiding repeated direct solar exposure.

## Attitude consequence

Thermal control now imposes a ship-level attitude constraint.

Normal high-power operation requires the Sun to remain inside a provisional cone around the habitat axis. Sustained thrust directions outside that cone require one or more of:

- reduced habitat electrical load
- reduced propulsion output
- temporary radiator shutters or secondary shades
- trajectory arcs that periodically restore preferred thermal attitude
- a future proven articulated dry thermal interface

The exact cone angle is not yet selected. It must come from the 3D view-factor model.

## Network topology

Each thermal tier uses 48 independently isolatable branches per habitat.

Each branch contains:

1. local collection manifold
2. branch pump or pump pair
3. check and isolation valves
4. heat exchanger or cold-plate group
5. protected supply and return trunks
6. radiator subfield
7. leak detection and inventory sensors
8. drain connection to a local safe tank

Branches are grouped into four separated farms per tier. No single penetration, manifold rupture, or boom failure may disable more than one farm.

## Provisional routing distances

Until a detailed CAD layout exists, use these bounded design lengths per branch:

| Tier | Collection and trunk run | Radiator distribution run | Provisional total hydraulic path |
|---|---:|---:|---:|
| Low temperature | 250–450 m | 300–600 m | 550–1,050 m |
| Medium temperature | 200–400 m | 150–350 m | 350–750 m |
| High temperature | 150–300 m | 80–250 m | 230–550 m |

These are placeholders for pressure-loss and inventory bounds, not locked geometry.

## Coolant inventory bounding method

Coolant inventory must be calculated from:

- internal pipe volume
- radiator channel volume
- heat exchanger volume
- manifolds
- accumulators
- drain tanks
- expansion allowance
- isolated repair inventory

For a circular pipe, volume is:

`V = pi * D^2 / 4 * L`

Because the loop uses many branches, inventory is highly sensitive to both pipe diameter and total routing length. The current diameter ranges from the previous pass imply that even modest routing changes can add hundreds of tonnes of coolant ship-wide.

No single inventory number is accepted yet.

## Accumulators and pressure control

Every independently operated loop requires pressure and volume accommodation.

NASA mechanically pumped loop work emphasizes that accumulator sizing must account for fluid volume changes across the full temperature range, while preventing boiling and pump cavitation. The design therefore requires:

- multiple distributed accumulators rather than one central vessel
- branch-level isolation without losing pressure control
- pump inlet pressure margin during the hottest and coldest credible states
- drain tanks sized for the largest isolatable liquid-metal section
- separate gas-charged or bellows-based pressure control for incompatible fluids

## Radiator subdivision decision

The previous 48 branches per tier remain provisional but defensible.

NASA large-radiator trade studies found advantages in using small independent subsystems with excess capacity to tolerate failures. The final branch count should be optimized against:

- valve and pump count
- manifold mass
- puncture consequence
- repair access
- flow balancing
- spare inventory
- control complexity

Forty-eight branches is now a design candidate, not a sacred number.

## Heat-pipe integration

For medium- and high-temperature systems, pumped loops should terminate in replaceable heat-pipe radiator modules where practical.

This limits long external liquid-metal channels and lets individual radiator panels continue spreading heat after partial channel damage. NASA has developed combined pumped-loop and heat-pipe radiator analysis methods for this architecture.

## New verification tests

The geometry is not accepted until a model demonstrates:

1. radiator view factor to deep space across the permitted attitude cone
2. direct and reflected solar heating at 0.5, 1, 3, 5, and 10 AU
3. pressure loss for every branch at normal and degraded flow
4. pump power after losing 25% of branches
5. coolant inventory and drain-tank mass
6. thermal survival after one entire farm is isolated
7. no single manifold rupture disabling more than 25% of a thermal tier
8. repair-robot access to every valve, pump, pipe joint, and panel
9. transient temperature rise during valve closure and branch isolation
10. compatibility between thrust attitude and thermal attitude

## Decision

Adopt the axisymmetric co-rotating radiator concept as the new working baseline.

Reject continuous radiator counter-rotation unless a future dry or rotary thermal-transfer system proves reliable enough for survival service.

The thermal network remains plausible but unclosed. The next required step is a parametric geometry model that turns branch count, pipe length, diameter, coolant density, radiator spacing, and attitude angle into mass, pressure loss, pump power, and thermal margin.

## Primary references

- NASA, *Optimum Design of Spacecraft Radiators for Large Capacity or Long Duration Mission Applications*. Independent subsystems, manifolding, flow routing, protection, mass, and reliability are coupled design variables.
- NASA, *Design of Accumulators and Liquid/Gas Charging of Single Phase Mechanically Pumped Fluid Loop Heat Rejection Systems*. Accumulator sizing must cover temperature-driven volume changes while avoiding boiling and cavitation.
- NASA, *User's Manual for the Heat Pipe Space Radiator Design and Analysis Code*. Combined pumped-loop and heat-pipe radiator architecture.
- NASA, *Design and Performance of Space Station Photovoltaic Radiators*. Two independent ammonia loops and explicit debris-survivability criteria.
