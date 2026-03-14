Extreme Weather Indicators Extension
Climate & Phenology Journal — Optional Data Model Extension

Purpose
Extreme weather events — heatwaves, cold snaps, windstorms, hail, atmospheric rivers, derechos, blizzards, and more — are increasing in frequency and severity. While meteorological instruments capture broad patterns, people on the ground often notice early signals, localized impacts, and fine‑scale effects that automated systems miss.

This extension defines optional extreme‑weather‑relevant fields that observers can record to support:

early awareness

local impact tracking

long‑term climate pattern analysis

community and agency context

environmental resilience research

These indicators are not predictive tools. They are contextual observations that complement professional systems and help fill the gaps between sensors and satellites.

1. Design Principles
1.1 Human‑observable
All fields reflect what a person can reliably notice without instruments.

1.2 Region‑agnostic
Works in northern climates, deserts, coastal regions, mountains, prairies, and tropical zones.

1.3 Non‑sensitive
No personal data, no operational intel, no tracking beyond the observation point.

1.4 Secure by Design
Observations are stored safely, with integrity checks and no personal identifiers.

1.5 Optional
These fields extend the core model but do not replace it.

2. Extreme Weather Indicator Fields
2.1 Heatwaves & Extreme Heat
Field	Type	Description
heat_intensity_feel	enum	Warm, hot, very hot, extreme
heat_duration_estimate	enum	Short, prolonged, multi‑day
overnight_heat_retention	enum	Cooled normally, stayed warm, stayed hot
vegetation_heat_stress	enum	None, mild wilt, severe wilt, scorch
animal_behavior_heat_signals	string	Wildlife seeking shade, reduced movement, etc.
Human perception is often the earliest indicator of dangerous heat.

2.2 Extreme Cold & Arctic Outbreaks
Field	Type	Description
cold_intensity_feel	enum	Cold, very cold, extreme cold
wind_chill_feel	enum	Mild, noticeable, severe
frostbite_risk_signs	enum	Low, moderate, high (observer estimate)
ice_fog_presence	boolean	Fog caused by extreme cold
vehicle_or_equipment_behavior	string	Hard starts, brittle plastics, etc.
These indicators help track cold events that affect safety and infrastructure.

2.3 Windstorms, Derechos & Severe Gusts
Field	Type	Description
wind_gust_intensity	enum	Moderate, strong, very strong, extreme
tree_movement_observed	enum	Swaying, bending, snapping, uprooted
debris_in_air	boolean	Loose debris lifted by wind
power_line_movement	enum	Normal, swaying, severe movement
structural_noise	string	Whistling, rattling, banging
Wind impacts are often highly localized and not captured by stations.

2.4 Hail, Ice Pellets & Freezing Rain
Field	Type	Description
hail_size_estimate	enum	Pea, marble, quarter, larger
hail_intensity	enum	Light, moderate, heavy
freezing_rain_presence	boolean	Ice accretion observed
ice_accretion_effects	enum	Light glaze, moderate buildup, heavy buildup
slippery_surface_presence	boolean	Roads/sidewalks dangerously slick
These indicators help track storm severity and local impacts.

2.5 Thunderstorms & Lightning
Field	Type	Description
lightning_frequency_estimate	enum	Occasional, frequent, continuous
thunder_intensity	enum	Distant, moderate, loud, explosive
storm_movement_direction	enum	8‑point compass
localized_downburst_signs	boolean	Sudden wind bursts, dust plumes
hail_or_rain_mix	boolean	Mixed precipitation during storm
Human observers often detect storm severity before radar updates.

2.6 Blizzards & Whiteout Conditions
Field	Type	Description
visibility_reduction	enum	Slight, moderate, severe, whiteout
snow_drift_height_cm	float	Approximate drift height
blowing_snow_intensity	enum	Light, moderate, heavy
travel_hazard_signals	enum	Slippery, drifting, zero visibility
wind_snow_interaction_notes	string	Snow snakes, ground blizzards, etc.
These indicators help track winter storm impacts.

2.7 Atmospheric Rivers & Prolonged Rain Events
Field	Type	Description
rain_persistence	enum	Hours, multi‑day, continuous
rain_intensity_variability	enum	Steady, fluctuating, surging
soil_saturation_trend	enum	Drying, stable, increasing saturation
localized_flooding_signs	boolean	Water pooling or flowing
storm_cloud_character	string	Low, dark, fast‑moving, layered
These indicators help track long‑duration events that cause flooding and landslides.

3. Safety Notes for Observers
Never put yourself at risk to collect data.

Never approach downed power lines, unstable trees, or storm‑damaged structures.

Never drive into storms or hazardous conditions.

These indicators are not for emergency decision‑making.

They support awareness, research, and long‑term climate memory.

4. Data Integrity & Security
To maintain trust and safety:

Observations include timestamps and location accuracy indicators.

Data is validated before cloud sync.

No personal identifiers are stored.

Observations cannot be edited after submission (audit trail).

The system avoids implying predictive certainty.

This aligns with the project’s Secure by Design philosophy.

5. Future Extensions
Potential additions:

heat index / humidex (observer‑estimated)

dust storm indicators

volcanic ash (for global regions)

tornado‑adjacent signals (safe, distant observations only)

extreme UV exposure indicators

These will be developed collaboratively with meteorologists, emergency services, and community observers.
