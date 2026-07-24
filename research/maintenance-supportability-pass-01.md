# Maintenance and Supportability Research Pass 01

## Decision

The ship must be designed around a continuous repair economy, not a warehouse of replacement boxes.

The current industrial baseline is therefore amended with four mandatory systems:

1. a ship-wide component registry with age, duty cycle, failure history, criticality, and repair depth;
2. probabilistic spares analysis rather than fixed-year inventories alone;
3. component-level electronics repair and test capability;
4. repair-access and commonality standards enforced during design.

## Strongest evidence

NASA's Exploration Maintainability Analysis Tool uses Monte Carlo simulation to model failures, repair actions, spare availability, logistics mass, and crew time. This is a better fit for the worldship than deterministic annual replacement estimates.

Source: https://ntrs.nasa.gov/citations/20120015419

NASA comparisons of spares-analysis methods found that heuristic approaches miss dynamic behavior and uncertainty that deeper Monte Carlo and state-based methods can expose.

Source: https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/20160006509.pdf

NASA's CLEAR work found that replacing complete orbital-replacement units is too mass-intensive for long missions. Component-level diagnosis and repair can reduce spare mass, but requires compatible electronics design, diagnostics, tools, containment, training, and post-repair testing.

Sources:
- https://ntrs.nasa.gov/search.jsp?R=20070022366
- https://ntrs.nasa.gov/citations/20100033105
- https://ntrs.nasa.gov/citations/20110006369
- https://ntrs.nasa.gov/citations/20120003735

NASA supportability studies identify commonality, repair depth, reduced complexity, redundancy, manufacturing, recycling, resource utilization, uncertainty reduction, and cached spares as interacting design choices rather than independent add-ons.

Source: https://ntrs.nasa.gov/citations/20170009115

## Imported design rules

### Repair depth classes

Every maintained item receives one class:

- R0: discard or recycle after failure;
- R1: replace complete standardized unit;
- R2: replace internal module;
- R3: repair individual mechanical or electronic components;
- R4: remanufacture from raw or recycled feedstock.

Life-critical systems must have at least two viable repair paths, normally one rapid path and one deep path.

### Mandatory equipment metadata

Each registered component must include:

- parent system and physical location;
- criticality and tolerated downtime;
- installed quantity and active redundancy;
- operating age, duty cycle, temperature, vibration, and radiation exposure;
- failure distribution with uncertainty bounds;
- inspection interval and diagnostic coverage;
- required tools, parts, feedstock, skills, and repair time;
- compatible substitute parts;
- recovery route for failed material.

### Electronics hospital

The spine industrial complex requires:

- automated board imaging and comparison;
- electrical probing and fault isolation;
- component removal and replacement;
- soldering, wire bonding, coating removal, and recoating;
- cable and connector fabrication;
- environmental containment and fume control;
- post-repair burn-in and functional testing;
- practice boards and recurring technician certification.

The ship should favor larger-pitch, inspectable, reworkable electronics for critical systems even when denser devices are available.

### Commonality rule

Critical families should share connectors, voltage ranges, communications protocols, mechanical interfaces, diagnostic ports, and controller architectures. Unique parts require an explicit justification and a lifetime support plan.

## Required simulator

Build a maintenance Monte Carlo model with:

- Weibull or evidence-supported failure distributions;
- common-cause and shock failures;
- imperfect diagnostics and false alarms;
- technician and robot repair queues;
- tool and workcell contention;
- spare, feedstock, and consumable depletion;
- cannibalization and degraded-operation options;
- manufacturing lead times;
- mining interruptions;
- correlated aging from heat, vibration, radiation, and contamination.

Minimum outputs:

- probability of losing each critical function over 1, 10, 50, and 100 years;
- annual failures and repairs by class;
- technician hours and peak repair backlog;
- spare and feedstock mass consumed;
- manufacturing throughput required;
- most dangerous single-source dependencies;
- expected and 95th-percentile downtime.

## Changes to Volume V

- The annual replacement-demand table remains provisional.
- Five-year stockpiles are no longer accepted as proof of five-year autonomy.
- Spare quantities must be tied to service probability and repair capability.
- Industrial staffing must include diagnostics, reliability engineering, configuration control, and training.
- Equipment access space, isolation points, lifting paths, and test ports count as real design volume and mass.

## Current verdict

The industrial architecture remains plausible but unclosed.

The next decisive step is a component taxonomy and a first Monte Carlo model covering one representative chain: carbon-dioxide removal, farm lighting, coolant pumping, or electrical distribution.