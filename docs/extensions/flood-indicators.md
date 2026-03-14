Flood Indicators Extension
Climate & Phenology Journal — Optional Data Model Extension

Purpose
Flooding is shaped by a combination of weather, snowpack, soil saturation, landscape features, and water flow. While sensors and gauges provide critical data, they often miss the fine‑scale, early‑stage signals that people notice first.

This extension defines optional flood‑relevant fields that observers can record to support:

early awareness

spring melt monitoring

ice‑jam risk

soil saturation and runoff potential

river and creek behaviour

long‑term hydrological patterns

These indicators are not predictive tools. They are contextual observations that complement professional systems and help fill the gaps between sensors and satellites.

1. Design Principles
1.1 Human‑observable
All fields are things a person can reliably notice without instruments.

1.2 Region‑agnostic
Works in boreal regions, prairie watersheds, mountain valleys, coastal areas, and arid flash‑flood zones.

1.3 Non‑sensitive
No personal data, no operational flood intel, no tracking beyond the observation point.

1.4 Secure by Design
Observations are stored safely, with integrity checks and no personal identifiers.

1.5 Optional
These fields extend the core model but do not replace it.

2. Flood Indicator Fields
2.1 Snowmelt & Surface Water
Field	Type	Description
snowmelt_rate_estimate	enum	Slow, moderate, rapid
standing_water_presence	enum	None, small puddles, widespread pooling
surface_runoff_observed	enum	None, light, moderate, heavy
ground_firmness	enum	Firm, soft, saturated, unstable
These indicators help track meltwater behaviour and early flood potential.

2.2 Soil Saturation & Drainage
Field	Type	Description
soil_saturation_level	enum	Dry, moist, saturated, waterlogged
drainage_behavior	enum	Normal, slow, very slow, no drainage
soil_cracking_or_heaving	boolean	Signs of freeze‑thaw stress
ditch_flow_rate	enum	None, trickle, steady, fast
These fields help identify when the ground can no longer absorb water.

2.3 River, Creek, and Lake Behaviour
Field	Type	Description
water_level_change_24h	enum	Lower, stable, rising, rapidly rising
bank_fullness_percent	int	0–100% of bank capacity
flow_speed_estimate	enum	Slow, moderate, fast, very fast
water_clarity	enum	Clear, cloudy, muddy, debris‑laden
debris_presence	enum	None, light, moderate, heavy
These are early signals of potential flooding or erosion.

2.4 Ice & Freeze‑Thaw Indicators
Field	Type	Description
river_ice_condition	enum	Solid, cracked, candled, broken, open water
ice_jam_risk	enum	Low, moderate, high (observer estimate)
shoreline_ice_movement	boolean	Ice shifting or lifting
overflow_presence	boolean	Water flowing over ice surface
These are especially important in northern regions.

2.5 Rainfall & Storm Indicators
Field	Type	Description
rain_intensity_estimate	enum	Light, moderate, heavy, torrential
rain_duration_estimate	enum	Short, steady, prolonged
thunderstorm_activity	enum	None, distant, nearby
localized_downpour_observed	boolean	Sudden intense rainfall
Human observers often detect localized events that radar misses.

2.6 Infrastructure & Landscape Context
Field	Type	Description
culvert_flow_status	enum	Clear, partially blocked, blocked
roadway_water_presence	enum	None, wet, pooled, flowing water
slope_stability_notes	string	Signs of slumping or erosion
beaver_activity_observed	boolean	Dams or blockages affecting flow
These contextual notes help agencies understand local conditions.

3. Safety Notes for Observers
Never enter floodwaters to collect data.

Never approach unstable ice or riverbanks.

Never cross flowing water.

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

soil moisture probe integration (optional)

snow water equivalent (SWE) estimates

region‑specific floodplain markers

ice thickness (if measured safely by trained observers)

stormwater infrastructure notes

These will be developed collaboratively with hydrologists, emergency services, and community observers.
