DATA_MODEL_OVERVIEW.md — Climate & Phenology Journal

Purpose of This Document
This document provides a clear, high‑level overview of the data model used in the Climate & Phenology Journal.
The goal is to create a simple, durable, region‑adaptable structure that supports:

long‑term climate memory

phenology tracking

wildfire and flood awareness

ecological research

community science

offline‑first field use

The model is intentionally minimal, human‑centered, and Secure‑by‑Design.

1. Design Principles
1.1 Minimal but expressive
Only fields that meaningfully support climate, weather, phenology, or emergency‑relevant observations are included.

1.2 Region‑adaptable
The core model is universal, but phenology and species lists can be extended per region.

1.3 Human‑first
The model reflects what people can reliably observe in the field.

1.4 Durable
Data must remain meaningful decades from now, even as technology changes.

1.5 Secure by Design
The model avoids collecting personal identifiers and supports safe, privacy‑respecting use.

2. Core Observation Structure
Each observation is a single, timestamped record containing:

metadata

weather

snowpack

seasonal markers

phenology

field notes

Not all fields are required. Observers can record as much or as little as they want.

3. Metadata
These fields describe when and where the observation occurred.

Field	Type	Description
entry_id	string	Unique ID for the observation
user_id	string	Anonymous contributor ID (no personal info)
timestamp	datetime	When the observation was recorded
location_lat	float	Latitude
location_lon	float	Longitude
location_name	string (optional)	Human‑friendly place name
Security note:  
No personal identifiers (name, email, phone) are stored.

4. Weather Fields
Weather observations capture short‑term atmospheric conditions.

Field	Type	Description
wind_direction	enum	8‑point compass (N, NE, E, SE, S, SW, W, NW)
wind_force_beaufort	int	Beaufort scale (0–12)
cloud_octas	int	Cloud cover (0–8)
precip_type	enum	Rain, snow, sleet, hail, drizzle, none
precip_amount_mm	float	Estimated precipitation
snowfall_cm	float	New snow in last 24h
snow_on_ground_cm	float	Total snow depth
These fields support wildfire risk awareness, flood monitoring, and climate trend analysis.

5. Snowpack Fields
Snowpack structure is critical for:

avalanche awareness

spring melt forecasting

hydrology

ecological timing

Field	Type	Description
snow_surface_condition	enum	Powder, crust, slush, ice, facets, etc.
snowpack_crust_layers	string	Notes on crust layers
snowpack_weak_layers	string	Notes on weak layers
snowpack_notes	string	Additional details
6. Seasonal Markers
These fields capture the “big moments” in a region’s seasonal cycle.

Field	Type	Description
percent_snow_cover	int	0–100%
first_frost_date	date	First frost of the season
last_frost_date	date	Last frost of the season
snow_gone_date	date	When snow fully melted
first_snowfall_date	date	First snow of the season
These markers are essential for long‑term climate memory.

7. Phenology Fields
Phenology tracks the timing of biological events.

Field	Type	Description
grass_stage	enum	Dormant, green‑up, growing, seeding, cured
deciduous_stage	enum	Budding, leafing, full leaf, color change, leaf drop
coniferous_stage	enum	Buds, candles, pollen, mature needles
wildflower_first_bloom	dictionary	{ species_name: date }
Region‑specific species lists can be added without changing the core model.

8. Field Notes
A free‑text space for anything that doesn’t fit neatly into a field:

wildlife

insects

soil conditions

smells

sounds

anomalies

smoke

haze

unusual weather

This is often the most valuable part of an observation.

9. Extensibility
The model supports optional extensions:

region‑specific phenology

wildfire indicators

flood indicators

soil moisture

air quality

cultural/Indigenous seasonal markers (with permission)

Extensions live in /docs/extensions/.

10. Data Integrity & Security
To support Secure‑by‑Design principles:

no personal identifiers are stored

timestamps and locations include accuracy indicators

observations include optional metadata for confidence

cloud sync validates data before accepting it

all data is encrypted in transit and at rest

the model avoids fields that could compromise privacy

11. Long‑Term Durability
The data model is designed to remain meaningful for decades:

uses simple, universal field types

avoids proprietary formats

supports migration to future systems

stores dates and times in ISO‑8601 format

uses enums instead of free‑form text where possible

This ensures the climate memory remains usable for future generations.
