# Agriculture Simulator Research Pass 02

## Decision

Keep the current 700,000 m² normal canopy provisionally. The dominant uncertainty is now operational reliability, not raw area.

NASA controlled-environment results show that high crop productivity is physically plausible, but edible yield can underperform total biomass expectations and harvest index can drift. The ship therefore needs a crop simulator that treats yield as a distribution rather than a fixed number.

## Evidence extracted

- NASA reported best controlled-environment wheat edible productivity near 24 g/m²/day, with similar order-of-magnitude results for potatoes and lettuce.
- A separate wheat study reported 23–57 g/m²/day under optimized conditions, but at very high lighting power near 600 W/m².
- NASA’s Biomass Production Chamber operated for more than 1,200 days and grew wheat, soybean, lettuce, and potato. Total biomass tracked expectations better than edible biomass, and harvest indices were somewhat lower than expected.
- Current NASA crop work still identifies unresolved issues in water and nutrient delivery, radiation effects, microbiomes, food safety, seed longevity, disease control, health monitoring, and cultivar selection.
- Crop choice cannot be optimized for calories alone. NASA identifies growth habit, physiology, nutritional value, acceptability, postharvest behavior, maintenance burden, stress tolerance, harvest index, and inedible biomass as coupled selection variables.

## Simulator architecture

The minimum useful simulator should operate in daily time steps and represent every crop by cultivar and sector.

### State per planting cohort

- crop and cultivar
- sector and pressure cell
- planting date
- planned harvest date
- canopy area
- growth stage
- accumulated light integral
- temperature and humidity exposure
- CO2 exposure
- water and nutrient status
- disease status
- expected edible yield
- expected inedible biomass
- seed requirement
- labor demand

### Uncertain variables

Each crop cycle should sample:

- germination success
- growth-duration variation
- total biomass variation
- harvest-index variation
- processing loss
- nutrient deficiency
- lighting derate
- water-delivery fault
- disease loss
- contamination rejection
- seed viability

Correlated failures must be possible. A bad nutrient batch, shared cultivar weakness, atmospheric-control fault, or pathogen can affect multiple sectors simultaneously.

## Required scenarios

1. Normal stochastic operation for 30 years
2. Loss of one 8.3% farm sector
3. 25% farm loss for one year
4. 50% systemic crop loss
5. Lighting power reduction of 10%, 25%, and 50%
6. Oilseed failure for two consecutive cycles
7. Wheat or rice cultivar collapse
8. Pathogen outbreak crossing adjacent sectors
9. Seed-bank contamination
10. Harvest synchronization after a prolonged power outage

## Acceptance tests

The agricultural system passes only if Monte Carlo runs demonstrate all of the following:

- at least 99% of normal years meet calorie demand without reserve food
- protein and fat remain above requirements in at least 99.9% of normal years
- no single sector loss causes rationing
- a 25% loss can be survived for one year using remaining production and reserves
- a 50% loss does not cause atmospheric failure because mechanical ECLS takes control
- strategic food reserves remain above the immediate 30-day tier during modeled recovery
- no crop family relies on one cultivar, one nutrient line, one seed store, or one processing chain

## Design changes now adopted

- Planting is staggered continuously. No staple crop may have more than 10% of annual production sharing one harvest window.
- Every major crop uses at least five viable cultivars, but no two adjacent sectors use an identical cultivar mix.
- Sector nutrient loops can be isolated and chemically reset.
- Disease detection uses imaging, volatile monitoring, root-zone sampling, and periodic destructive assays.
- Edible yield and harvest index are tracked separately.
- Simulator outputs must feed the atmosphere, water, labor, power, heat, food-reserve, and nutrient ledgers.

## Current verdict

The area claim remains plausible. Indefinite food security remains unproven until this stochastic cultivar-level model exists and passes the stated failure scenarios.

## Primary sources

- NASA, Plant productivity in controlled environments, NTRS 20040090305
- NASA, Wheat production in controlled environments, NTRS 19880002888
- NASA, Biomass Production Chamber testbed, NTRS 20040089951
- NASA, Space Crop Production, NTRS 20210000523
- NASA, Selection Factors for Space Crops, NTRS 20210016653
- NASA, Plants in Space and Space Crop Production, NTRS 20230013771
