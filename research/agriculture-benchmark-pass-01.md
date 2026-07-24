# Agriculture Benchmark Pass 01

## Question

Can one habitat's 700,000 m² normal installed crop canopy plausibly feed 2,500 people indefinitely?

## First-pass result

The area itself is not the main problem.

Per person, the design provides:

- 280 m² of active crop canopy
- about 20.8 kW of normal agricultural electricity
- about 2.30 million kcal/person/year gross production target

The current food target spread across the full canopy requires only about:

- 3,330 kcal/m²/year
- 9.1 kcal/m²/day
- 1.85 g/m²/day of average edible dry food

Those are low average productivity requirements compared with controlled-environment crop experiments.

## External benchmarks

### NASA controlled-environment wheat

Published controlled-environment wheat work reports roughly 23–57 g/m²/day edible biomass, with an estimated 12–30 m²/person when wheat supplies a complete 2,800 kcal/day diet. The experiments used very high artificial-light input, around 600 W/m².

Source:
- https://ntrs.nasa.gov/search.jsp?R=19880002888

### NASA potato work

Controlled-environment potato experiments reported about 21.9 g/m²/day edible tubers under one tested regime, with higher values under side-lighting.

Source:
- https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/19880002887.pdf

### NASA Biomass Production Chamber

NASA operated a 20 m² closed crop chamber for more than 1,200 days, growing wheat, soybean, lettuce, and potato. Total biomass tracked expectations, but edible yield and harvest index were somewhat lower than anticipated. This is important because theoretical crop yield is not the same as usable food output.

Source:
- https://ntrs.nasa.gov/citations/20040089951

### Generation-ship farming study

The often-cited 0.45 km² for 500 people equals 900 m²/person, but it includes conventional production of meat, fish, dairy, and honey. It is therefore not a direct comparison with a plant-dominant, highly stacked, electrically lit system.

Source:
- https://arxiv.org/abs/1901.09542

## Interpretation

The ship's 280 m²/person canopy is not obviously undersized. It is actually generous relative to high-intensity plant-only CELSS estimates.

The real vulnerabilities are:

1. Whether the crop-by-crop annual yields are mutually consistent with the stated light levels.
2. Whether harvest-index losses, disease, pollination failures, seed degeneration, and processing losses remain within budget.
3. Whether the diet remains nutritionally and culturally acceptable for decades.
4. Whether 70 MW normal agricultural power is sufficient once pumps, air handling, dehumidification, processing, refrigeration, and heat-pump penalties are modeled hourly.
5. Whether the farm can recover from synchronized failures without consuming its food reserve faster than replacement crops mature.

## Design decision

Do not enlarge the farm yet.

Retain:

- 700,000 m² normal installed canopy per habitat
- 60,000 m² standby canopy
- 70 MW normal agricultural power
- 85 MW peak agricultural power

Reclassify the open problem from "probably insufficient area" to "unverified integrated crop schedule and failure resilience."

## Required next model

Build a monthly crop simulator with, for every cultivar:

- planted area
- tier count
- photoperiod
- photon flux
- cycle length
- edible yield
- harvest index
- seed fraction
- labor
- water flux
- nutrient uptake
- disease-loss distribution
- processing loss
- calories, protein, fat, fiber, and micronutrients

The model must survive:

- loss of one 8.3% farm sector
- 25% systemic crop loss
- 50% crop loss
- 30-day total lighting interruption
- one failed staple harvest
- six-month habitat isolation

## Verdict

Agricultural area is plausible.

Indefinite food autonomy remains unclosed until the cultivar-level schedule, power profile, nutrient ledger, and failure simulation agree.