# data/

This folder contains only small, non-sensitive sample data used for local
development and automated tests.

## Current sample data

| File | Purpose | Source / provenance | Data owner |
| --- | --- | --- | --- |
| `offices.csv` | Demonstrates deterministic lookup of university service locations and opening hours. | Synthetic, course-provided sample data for Lab 1; **not an official university directory**. | Team 02 data steward (Member 4) |

## Rules for future data

- Record each source, access date, licence/permission, and owner before data is
  used in the assistant.
- Keep source documents, exports, and personally identifiable information out
  of this repository. `data/raw/` is ignored by Git.
- Never commit real student records, contact details, authentication material,
  restricted regulations, or raw conversation logs.
- Validate required fields and update provenance before adding any structured
  dataset.

Member 4 will expand this catalog through their own reviewed PR when approved
project data sources are available.
