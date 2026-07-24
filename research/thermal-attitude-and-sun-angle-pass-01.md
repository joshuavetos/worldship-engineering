# Thermal Attitude and Sun-Angle Pass 01

## Question

Can the co-rotating habitat radiators remain thermally safe while the ship performs ordinary navigation and propulsion maneuvers?

## Evidence extracted

- Spacecraft thermal balance depends on incoming solar flux, internal heat generation, radiator view to deep space, attitude, and orbit. It is dynamic rather than static.
- Real missions often impose attitude laws primarily to protect radiators. BepiColombo keeps its radiator away from the Sun and even performs periodic 180 degree flips to preserve the required cold-space view.
- Solar Orbiter treats radiator illumination as an emergency. Near the Sun, only a small depointing window is tolerated before reorientation becomes mandatory.
- Radiators can also fail thermally without direct illumination if they see a warm spacecraft surface, solar array, shield, or planet.

## Design decision

The ship adopts a formal **thermal-attitude envelope**.

### Normal cruise attitude

- Habitat spin axes remain approximately parallel to the Sun-line.
- Annular Sun shields face the Sun.
- Low-temperature radiator fins remain entirely inside the shield shadow.
- Medium- and high-temperature fields may tolerate limited indirect heating but do not normally receive direct sunlight.
- Ship roll about the Sun-line remains unrestricted.

### Provisional attitude zones

These are operating rules, not validated final limits.

| Zone | Spin-axis departure from Sun-line | Allowed operation |
|---|---:|---|
| Green | 0 to 5 degrees | Full habitat, industry, and propulsion power |
| Amber | 5 to 15 degrees | Time-limited; thermal model predicts exposure and may shed industry |
| Red | More than 15 degrees | No sustained operation until geometry proves radiator shadowing |

The angles are provisional because the shield radius, radiator axial offset, fin length, and boom geometry have not yet been fixed.

## Maneuver doctrine

The ship should not continuously point its entire body along the desired thrust vector if that breaks thermal attitude.

Preferred hierarchy:

1. Use gimbaled propulsion clusters for ordinary vectoring while preserving the Sun-pointing thermal attitude.
2. Use slow precession of the full ship only when gimbal authority is insufficient.
3. Schedule large off-axis burns in short thermal windows.
4. Reduce agriculture lighting, heavy industry, and reactor output before leaving the green zone.
5. Use thermal storage and coolant inventory only as a bridge, never as a substitute for radiator view.

## Safe mode

A thermal safe mode is mandatory.

On loss of attitude control:

1. Trip propulsion and heavy industry.
2. Reduce habitat electrical load toward survival level.
3. Use independent Sun sensors and inertial references to recover Sun-line attitude.
4. Confirm low-temperature radiator shadow before restoring agriculture lighting.
5. Restore reactor output in stages.

Attitude recovery must remain possible after failure of any single sensor family or control computer.

## Geometry equations required next

For each radiator farm, calculate:

- direct solar visibility across the full spin cycle
- shield penumbra and structural-flex margin
- view factor to deep space
- view factor to both habitats, spine, shields, propulsion units, and other radiator farms
- absorbed solar power as a function of heliocentric distance and angle
- transient panel temperature after attitude loss
- maximum safe depointing time at 0.5, 1, 3, 5, and 10 AU
- gimbal angle required from propulsion units to preserve thermal attitude

## Consequence for propulsion architecture

The earlier fixed axial-thrust assumption is now a design debt. A solar-system worldship needs either:

- large gimbaled electric-propulsion clusters,
- distributed thruster pods,
- or a mission plan whose long burns remain nearly parallel to the Sun-line.

The first two are more operationally flexible but add mass, plumbing, structural moments, plume-clearance constraints, and control complexity.

## Current verdict

The radiator architecture remains plausible, but the ship cannot yet claim unrestricted attitude or thrust direction.

**Selected provisional rule:** preserve a Sun-pointing thermal attitude during normal high-power operation, use gimbaled propulsion for ordinary trajectory control, and treat major off-axis maneuvers as reduced-power thermal events.

## Primary references

- ESA, Thermal Control: https://www.esa.int/Enabling_Support/Space_Engineering_Technology/Thermal_Control
- ESA, BepiColombo engineering and radiator orientation: https://sci.esa.int/web/bepicolombo/-/31326-engineering
- ESA, Shielding Solar Orbiter from the Sun: https://www.esa.int/Enabling_Support/Space_Engineering_Technology/Shielding_Solar_Orbiter_from_the_Sun
- NASA, Spacecraft Thermal Control: https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/20010091676.pdf
- NASA, LRO Sun Safe Mode: https://ntrs.nasa.gov/archive/nasa/casi.ntrs.nasa.gov/20100014251.pdf
