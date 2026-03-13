# climate-phenology-journal

Climate & Phenology Journal

A collaborative, long‑term climate and phenology record for any region.

Purpose

  The Climate & Phenology Journal is a simple, durable, cross‑platform app that allows people to record weather, snowpack, phenology, and seasonal observations. Over decades, this becomes a long‑term climate memory that supports research, agriculture, emergency services, wildfire awareness, education, and community science.
  
  The system is designed for any region — from northern climates to places like US, California, Australia, Canada, or anywhere seasonal change matters.
  
  These are all human-observable weather and phenology variables that can be reported and then processed by language-based AI, rather than numerical sensor data.


Core Features

  Fast, simple observation entry,
  Offline‑first design (critical for rural and remote areas),
  Cloud‑based long‑term archive,
  Cross‑platform (iOS, Android, Windows, Mac),
  AI‑ready architecture,
  Open collaboration model

Observation Types

Weather
  
  Wind direction (8‑point compass),
  Wind force (Beaufort scale),
  Cloud cover (0–8 octas),
  Precipitation type + amount,
  Snowfall (cm),
  Snow on ground (cm),
  Snowpack,
  Surface condition,
  Crust layers,
  Weak layers,

Seasonal Markers
 
  Percent snow cover,
  First frost,
  Last frost,
  Snow‑gone date,
  First snowfall,

Phenology

  Grass stages,
  Tree stages (deciduous + coniferous),
  Wildflower first bloom dates,
  Region‑specific species or indicators,

Field Notes
 
  Free‑text observations

Wildlife, insects, soil, smells, sounds

Anomalies or unusual events

High‑Level Architecture

A simple, three‑layer system:

  1. App Layer (UI)
    Cross‑platform (Flutter or React Native)
    Forms, maps, charts
    Local history view

  2. Local Storage (SQLite)
    Offline capability
    Fast access
    Stores unsynced entries

  3. Cloud Storage (NoSQL)
    Firestore / Cosmos DB / DynamoDB
    Scalable to millions of records
    Long‑term climate archive
    Data Model (Simplified)

Each observation includes:

Metadata

  entry_id,
  user_id,
  timestamp,
  location_lat,
  location_lon,
  location_name (optional),

Weather

  wind_direction,
  wind_force_beaufort,
  cloud_octas,
  precip_type,
  precip_amount_mm,
  snowfall_cm,
  snow_on_ground_cm,


Snowpack

  snow_surface_condition,
  snowpack_crust_layers,
  snowpack_weak_layers,
  snowpack_notes,

Seasonal Markers

  percent_snow_cover,
  first_frost_date,
  last_frost_date,
  snow_gone_date,
  first_snowfall_date

Phenology

  grass_stage,
  deciduous_stage,
  coniferous_stage,
  wildflower_first_bloom (dictionary keyed by species),

Field Notes

notes

Why This Matters
This project supports:
  Wildfire awareness and prevention,
  Agricultural planning,
  Research and long‑term climate studies,
  Emergency services,
  Indigenous knowledge and land stewardship,
  Citizen science,
  Environmental education

A shared tool benefits everyone.

How to Contribute

  We welcome contributions from:
  Developers,
  Designers,
  Ecologists,
  Fire behaviour specialists,
  Researchers,
  Educators,
  Citizen scientists,
  Agencies and NGOs,

Ways to get involved:

  Open an Issue,
  Submit a Pull Request,
  Share ideas or feedback,
  Help shape the data model,
  Join discussions about features and design

This is a public‑good project — open, collaborative, and built for any region.

License
Open‑source license to be selected (MIT, Apache 2.0, or similar).
