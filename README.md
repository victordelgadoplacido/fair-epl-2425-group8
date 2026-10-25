# FAIRified English Premier League 2024/25 match results (Group 8)

FAIR Data Engineering, University of Twente, 2026.
Group 8: Víctor Delgado Plácido, Pol Cabanes Piqueras.

Results of all 380 English Premier League matches of the 2024/25 season (date, home and
away team, full- and half-time goals, result and referee), FAIRified as RDF using schema.org
and a small Group 8 ontology, with clubs linked to Wikidata.

## Source and licence

- Source: DataHub, `season-2425.csv` (https://datahub.io/core/english-premier-league),
  data originally from Football-Data.co.uk
- Licence: Open Data Commons Public Domain Dedication and License (PDDL) 1.0,
  https://opendatacommons.org/licenses/pddl/

## Persistent identifiers (W3ID)

Namespace: `https://w3id.org/FAIR-course-UT/2026/group08/`

| Identifier | Resolves to |
|---|---|
| https://w3id.org/FAIR-course-UT/2026/group08/ | this repository |
| https://w3id.org/FAIR-course-UT/2026/group08/ont | `ontology/epl-ontology.ttl` |
| https://w3id.org/FAIR-course-UT/2026/group08/data | `data/rdf/epl-2425.ttl` |
| https://w3id.org/FAIR-course-UT/2026/group08/original | `data/original/premier-league-2024-2025-original.csv` |
| https://w3id.org/FAIR-course-UT/2026/group08/metadata/dataset | `metadata/records/dataset.ttl` |
| https://w3id.org/FAIR-course-UT/2026/group08/metadata/distribution-original | `metadata/records/distribution-original.ttl` |
| https://w3id.org/FAIR-course-UT/2026/group08/metadata/distribution-rdf | `metadata/records/distribution-rdf.ttl` |

Ontology terms (`…/ont#fullTimeHomeGoals`) and match resources (`…/data#1`) resolve to the
ontology and data files respectively. The redirect rules are maintained in the course
pid-relay repository (https://github.com/luizbonino/pid-relay, folder
`rules/FAIR-course-UT/2026/group08/`).

## Repository structure

| Folder | Content |
|---|---|
| `data/original/` | Original 22-column CSV, unchanged |
| `data/prepared/` | Prepared 9-column CSV (380 rows) |
| `data/rdf/` | FAIRified RDF data (Turtle) |
| `ontology/` | Group 8 ontology (built in Protégé) |
| `metadata/schemas/` | SHACL metadata schemas for Dataset and Distribution (built in Contour) |
| `metadata/records/` | Metadata records: dataset and its two distributions (RDF Turtle) |
| `openrefine/` | OpenRefine operation history (provenance of the data preparation) |
| `docs/` | Data dictionary |

## Data preparation

- 13 match-statistics columns removed (shots, fouls, corners, cards); 9 columns kept.
- Two referee names corrected with cited evidence: `K Kavanagh` → `C Kavanagh`
  (Brighton–Chelsea, 2025-02-14) and `O Oliver` → `M Oliver` (Bournemouth–Fulham, 2025-04-14).
- Goal columns converted to numbers; dates kept in ISO 8601 (`YYYY-MM-DD`).
- All steps recorded in `openrefine/preparation-history.json`.
