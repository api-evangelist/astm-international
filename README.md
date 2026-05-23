# ASTM International

API Evangelist profile of **ASTM International** — one of the world's largest voluntary consensus standards development organizations. Founded in 1898, ASTM publishes more than **13,000 globally recognized standards** developed by **30,000+ volunteer members** sitting on **150+ technical committees** and **2,100+ subcommittees** across **140+ countries**, with MoUs in place with **125 national standards bodies**.

> "Combining 13,000+ standards with 1,500+ books and 47,000+ articles and papers plus custom workflow tools, ASTM Compass provides one of the most comprehensive libraries of technical information available."  — *ASTM International*

This is a `standard`-mode pipeline run. ASTM is profiled here as a standards body and content platform, not as a developer-API provider — ASTM publishes no public REST API, OpenAPI spec, GitHub organization, RSS feed, or webhooks for its catalog or for the ASTM Compass platform.

## What is documented

- The ASTM organization, its scale, and its governance posture
- The **ASTM Compass** subscription platform (workflow, redlines, alerts, SSO surfaces)
- The **ASTM Standards Catalog** and the canonical designation system
- The **ASTM Digital Library**, **SpecBuilder**, **Proficiency Testing**, and **Training & Certification** surfaces
- The six normative ASTM document types and the A-G + J committee letter-prefix taxonomy
- Identity integrations: SAML, Shibboleth, OpenAthens, IP-range authentication

## Repository layout

| File | What it is |
|---|---|
| `apis.yml` | Root apis.yml inventory: 6 ASTM surfaces (Compass, Standards Catalog, Digital Library, SpecBuilder, Proficiency Testing, Training & Certification), 22 common properties, features, use cases, integrations, scale numbers, notable absences. |
| `json-schema/astm-standard-schema.json` | JSON Schema for a single ASTM standard catalog record (designation, committee, document type, lifecycle, references). |
| `json-schema/astm-technical-committee-schema.json` | JSON Schema for an ASTM technical committee / subcommittee. |
| `json-schema/astm-compass-subscription-schema.json` | JSON Schema for an ASTM Compass subscription, including identity integration. |
| `json-structure/astm-standard-structure.json` | JSON Structure form of the ASTM Standard record. |
| `json-structure/astm-technical-committee-structure.json` | JSON Structure form of the ASTM Technical Committee record. |
| `json-ld/astm-international-context.jsonld` | JSON-LD context mapping ASTM terms onto schema.org, SKOS, Dublin Core, and FOAF. |
| `examples/astm-standard-c150-example.json` | Real example: Portland cement spec (C150/C150M-23). |
| `examples/astm-standard-e8-example.json` | Real example: tensile-test method (E8/E8M-22). |
| `examples/astm-standard-f3001-example.json` | Real example: AM Ti-6Al-4V ELI spec (F3001-14R21). |
| `examples/astm-technical-committee-c01-example.json` | Real example: Committee C01 (Cement). |
| `examples/astm-technical-committee-f42-example.json` | Real example: Committee F42 (Additive Manufacturing). |
| `examples/astm-compass-subscription-example.json` | Synthetic example: enterprise Compass subscription with SAML/Okta. |
| `vocabulary/astm-international-vocabulary.yml` | Controlled vocabulary: document types, committee categories, designation format, lifecycle states, platforms, participation roles, identity integrations, scale figures. |

## ASTM document types

Defined in *Form and Style for ASTM Standards*. Every published ASTM standard is exactly one of these:

1. **Test Method** — "a definitive procedure that produces a test result"
2. **Specification** — "an explicit set of requirements to be satisfied by a material, product, system, or service"
3. **Practice** — "a set of instructions for performing one or more specific operations that does not produce a test result"
4. **Guide** — "a compendium of information or series of options that does not recommend a specific course of action"
5. **Classification** — "a systematic arrangement or division of materials, products, systems, or services into groups based on similar characteristics"
6. **Terminology** — "a document comprising definitions of terms; explanations of symbols, abbreviations, or acronyms"

## Committee letter-prefix taxonomy

Standards inherit their letter prefix from the owning committee.

| Letter | Domain | Example committees |
|---|---|---|
| **A** | Ferrous metals and products | A01 Steel; A04 Iron Castings; A06 Magnetic Properties |
| **B** | Nonferrous metals and products | B01 Electrical Conductors; B05 Copper Alloys; B09 Metal Powders |
| **C** | Cementitious, ceramic, concrete, and masonry | C01 Cement; C09 Concrete; C28 Advanced Ceramics |
| **D** | Miscellaneous materials and products | D02 Petroleum; D20 Plastics; D22 Air Quality; D37 Cannabis and Hemp |
| **E** | Miscellaneous subjects | E07 NDT; E28 Mechanical Testing; E31 Healthcare Informatics; E60 Sustainability |
| **F** | End-use materials and products | F04 Medical Devices; F38 UAS; F42 Additive Manufacturing; F50 AI in Manufacturing |
| **G** | Corrosion, weathering, durability | G01 Corrosion of Metals; G03 Weathering and Durability |
| **J** | Joint committees | J01 Joint ASTM/NACE Committee on Corrosion |

## Designation format

```
{Letter}{Number}[/{Number}M]-{YY}[(YYYY)]
```

- `C150-23` — Specification for Portland Cement, 2023 edition
- `C150/C150M-23` — Same standard, dual US-customary and SI-metric units
- `E8/E8M-22` — Tension Testing of Metallic Materials, 2022 edition
- `F3001-14(2021)` — AM Ti-6Al-4V ELI Spec, 2014 edition reapproved 2021

## ASTM Compass

ASTM Compass is the canonical subscription delivery platform for ASTM content.

- **Catalog**: 13,000+ standards, 1,500+ books, 47,000+ articles and papers, 300+ video standards, plus third-party publisher content from AASHTO, API, BSI, and others.
- **Workflow tools**: redlines (color-coded version comparison), change alerts, annotations with images and attachments, sharing, Compass Points metadata tagging.
- **Identity**: SAML 2.0 (any IdP), Shibboleth, OpenAthens, IP-range authentication. Customer implementations include Okta-based SSO.
- **Access URLs**: [compass.astm.org](https://compass.astm.org) for end users; sales-quoted enterprise pricing — no public price list.

## Notable absences

- No public **REST API** for the standards catalog, Compass content, or proficiency testing results
- No public **GitHub organization** for ASTM International
- No published **OpenAPI** or **AsyncAPI** specifications
- No public **pricing page** for Compass or Digital Library
- No public **RSS / Atom feeds** for press releases or standards updates
- No outbound **webhooks** — change alerts are delivered inside Compass and by email only

## Sources

- [ASTM International](https://www.astm.org) — homepage
- [About ASTM](https://www.astm.org/about)
- [Technical Committees — Full List](https://www.astm.org/membership-participation/technical-committees/committee-all)
- [Form and Style for ASTM Standards](https://www.astm.org/membership-participation/technical-committees/key-documents/form-and-style-for-astm-standards)
- [Standards and Publications](https://store.astm.org/products-services/standards-and-publications/standards.html)
- [ASTM Compass (Enterprise Solutions)](https://www.astm.org/standards-and-solutions/enterprise-solutions/astm-compass)
- [ASTM Compass Application](https://compass.astm.org)
- [ASTM Expands Access to Compass Platform](https://www.astm.org/news/press-releases/astm-expands-compass-access)

---

Profiled by [API Evangelist](https://apievangelist.com) — `astm-international`, pipeline mode `standard`, profiled 2026-05-23.
