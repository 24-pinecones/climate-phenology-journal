Wildfire Indicators Extension
Climate & Phenology Journal — Optional Data Model Extension

Purpose
Wildfire behaviour is influenced by a complex mix of weather, fuel conditions, landscape, and human activity. While satellites and automated sensors provide valuable data, they often miss the fine‑scale, ground‑truth details that people notice first.

This extension defines optional wildfire‑relevant fields that observers can record to support:

early awareness

situational context

fuel condition monitoring

smoke and air quality observations

local fire behaviour notes

long‑term fire‑climate relationships

These indicators are not predictive tools. They are contextual observations that complement professional systems and help fill the gaps between sensors and satellites.

1. Design Principles
1.1 Human‑observable
All fields are things a person can reliably notice without instruments.

1.2 Region‑agnostic
Works in boreal forests, grasslands, shrublands, savannahs, and Mediterranean climates.

1.3 Non‑sensitive
No personal data, no operational fire intel, no location tracking beyond the observation point.

1.4 Secure by Design
Observations are stored safely, with integrity checks and no personal identifiers.

1.5 Optional
These fields extend the core model but do not replace it.

2. Wildfire Indicator Fields
2.1 Fuel Moisture & Condition
Field	Type	Description
fine_fuel_moisture_estimate	enum	Dry, very dry, moderate, damp, wet
grass_cure_percent	int	0–100% cured grass
surface_fuel_condition	enum	Green, curing, cured, matted, compact, loose
dead_fuel_condition	enum	Dry, punky, moist, wet
These fields help approximate fire spread potential in grass and surface fuels.

2.2 Smoke & Air Quality
Field	Type	Description
smoke_presence	enum	None, light, moderate, heavy
smoke_source_direction	enum	8‑point compass
smoke_smell_intensity	enum	None, faint, noticeable, strong
visibility_km	float	Estimated visibility distance
Human smoke detection is often earlier than satellite detection.

2.3 Fire Behaviour Observations
These are non‑operational, general observations — not tactical intel.

Field	Type	Description
fire_activity_observed	enum	None, smoldering, small surface fire, torching, crown fire (distant)
fire_behavior_notes	string	Free‑text description
embers_present	boolean	Whether embers were seen
spotting_distance_estimate_m	int	Approximate spotting distance (if observed)
Observers should never approach a fire to collect data.

2.4 Weather Relevant to Fire Behaviour
These fields complement the core weather model.

Field	Type	Description
wind_gust_strength	enum	Light, moderate, strong, very strong
wind_shifts_observed	boolean	Sudden or unusual wind changes
relative_humidity_estimate	enum	Low, moderate, high
temperature_feel	enum	Cool, mild, warm, hot
These are human‑estimated, not instrument‑measured.

2.5 Fuel & Landscape Context
Field	Type	Description
fuel_type_general	enum	Grass, shrub, boreal forest, mixed forest, conifer, eucalyptus, agricultural
recent_precipitation_days	int	Days since last rain/snow
soil_moisture_feel	enum	Dry, firm, soft, wet
leaf_litter_depth_cm	float	Optional estimate
These help contextualize fire potential.

3. Safety Notes for Observers
Never approach a fire to collect data.

Never enter restricted areas.

Never put yourself at risk to record an observation.

These indicators are not for tactical decision‑making.

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

fire danger class (observer‑estimated)

drought indicators

soil cracking

lightning strike observations

heat dome / extreme heat notes

region‑specific fuel types

These will be developed collaboratively with wildfire professionals and ecologists.
