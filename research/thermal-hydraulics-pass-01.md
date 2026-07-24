# Thermal Hydraulics Pass 01

Status: provisional sizing model, not a closed design.

## Purpose

Estimate first-order coolant flow, branch sizes, pump power, and heat-exchanger penalties for the three habitat thermal tiers.

## Source constraints

NASA heat-rejection studies treat coolant choice, pressure drop, pump power, heat-pipe spacing, radiator mass, and rejected power as coupled design variables. NaK is generally treated as a low-pressure high-temperature coolant over roughly 300–1000 K, while water systems run at lower temperature and higher pressure. ISS heritage demonstrates long-duration mechanically pumped ammonia loops, but also demonstrates that leaks, jumpers, pumps, and replaceable modules are major reliability drivers.

Primary references:

- NASA/TM-2006-214121, *A Comparison of Coolant Options for Brayton Power Conversion Heat Rejection Systems*.
- NASA/TM-2005-213337, *Heat Rejection Concepts for Brayton Power Conversion Systems*.
- NASA, *International Space Station Active Thermal Control Sub-System On-Orbit Pump Performance and Reliability Using Liquid Ammonia as a Coolant*.
- NASA CR-128595, *Space Radiator Simulation System Analysis*.
- NASA, *Performance Expectations of Closed-Brayton-Cycle Heat Exchangers in 100-kWe Nuclear Space Power Systems*.

## Provisional design points per habitat

| Tier | Rejected heat | Transport fluid | Bulk temperature drop | Assumed heat capacity | Required mass flow |
|---|---:|---|---:|---:|---:|
| Low | 200 MW | internal water, external ammonia through isolated exchanger | 20 K water-side | 4.2 kJ/kg-K | 2,380 kg/s water-equivalent |
| Medium | 300 MW | NaK-78 | 100 K | 0.9 kJ/kg-K | 3,330 kg/s |
| High | 120 MW | NaK or sodium | 200 K | 1.0 kJ/kg-K | 600 kg/s |

Equation: `m_dot = Q / (cp * delta_T)`.

These are aggregate flows. No single trunk carries the full amount.

## Branch architecture

Use 48 independently isolatable primary branches per thermal tier, grouped across four radiator farms.

Approximate per-branch flow:

| Tier | Flow per branch | Provisional velocity | Density assumption | Approximate internal diameter |
|---|---:|---:|---:|---:|
| Low | 49.6 kg/s | 2 m/s | 1,000 kg/m3 | 0.18 m |
| Medium | 69.4 kg/s | 1 m/s | 850 kg/m3 | 0.32 m |
| High | 12.5 kg/s | 1 m/s | 800 kg/m3 | 0.14 m |

These diameters exclude wall thickness, insulation, armor, valves, expansion volume, and manifolds.

## Pump-power bound

Using provisional total loop pressure drops and 70% pump efficiency:

| Tier | Pressure drop | Volumetric flow | Pump power |
|---|---:|---:|---:|
| Low | 0.30 MPa | 2.38 m3/s | about 1.0 MW |
| Medium | 0.20 MPa | 3.92 m3/s | about 1.1 MW |
| High | 0.15 MPa | 0.75 m3/s | about 0.16 MW |

Total first-pass pumping power is about 2.3 MW per habitat before control margin, degraded pumps, filters, cold traps, and secondary loops. Reserve 4–6 MW until geometry is solved.

## Heat exchangers

The low-temperature system must keep ammonia outside inhabited volume. Water loops transfer heat through multiple parallel plate-fin or printed-circuit heat exchangers.

Design requirement:

- no single exchanger handles more than 5% of habitat survival heat
- exchanger trains are bypassable and cleanable
- pressure loss is explicitly included in pump sizing
- effectiveness target is not allowed to create excessive mass or pressure drop

NASA Brayton studies show that very high exchanger effectiveness can impose substantial mass and pressure-loss penalties. Therefore, the design must optimize total system mass and parasitic power rather than demand maximum effectiveness everywhere.

Provisional thermal approach penalties:

- low tier: 5–10 K total exchanger and control penalty
- medium tier: 10–25 K
- high tier: 20–40 K

These penalties reduce effective radiator temperature and must be included in the final area calculation.

## Coolant inventory

No defensible coolant mass can be assigned before pipe length, farm placement, accumulator volume, and branch geometry exist.

The final inventory model must include:

- pipes and manifolds
- radiator channels
- pump and separator volumes
- accumulators and expansion tanks
- emergency drain tanks
- 15% operational reserve
- isolated replacement charge for at least one complete radiator farm

Any current fixed coolant tonnage would be fabricated precision.

## Design decisions

1. Keep the three-tier coolant architecture.
2. Use many moderate-size branches rather than a few enormous trunks.
3. Reserve 4–6 MW per habitat for thermal pumping and controls.
4. Keep ammonia outside inhabited volume behind heat exchangers.
5. Treat heat-exchanger approach temperature as part of radiator sizing.
6. Do not lock pipe mass, coolant inventory, or pump count until the 3D layout exists.

## New failure requirements

- loss of one branch must remove no more than about 2.1% of one thermal tier
- loss of one radiator farm must leave 75% of that tier available
- pump modules must be remotely replaceable without draining an entire tier
- every liquid-metal loop requires freeze recovery, cold traps, oxygen monitoring, and emergency drain-down
- every ammonia interface requires double containment and leak localization

## Verdict

The required flows are enormous but consistent with a gigawatt-class inhabited ship. The architecture remains plausible only with highly parallel distribution. Thermal hydraulics is not closed until a 3D network model calculates pipe length, pressure drop, inventory, structural mass, freeze behavior, and radiator temperature loss.