# Cloud Connectivity Inventory

A lightweight, browser-based inventory and comparison concept for cloud connectivity resources. The project explores how cloud network inventory snapshots can be displayed and compared across dates.

> **Portfolio project:** This repository is maintained as a company-neutral personal engineering project. Use synthetic or sanitized inventory data only.

## Project history

- **Repository created:** March 31, 2025 (original GitHub creation date preserved)

## Goals

- Display cloud connectivity inventory records in a simple table.
- Compare inventory snapshots captured on different dates.
- Identify resources added or removed between snapshots.
- Explore a simple browser UI for cloud connectivity inventory data.

## Inventory fields

The prototype uses fields such as:

- Account or environment label
- Direct Connect Gateway identifier
- Virtual interface identifiers
- Associated CIDR
- Cloud region
- Virtual gateway identifier
- Autonomous System Number (ASN)
- Timestamp (in the later prototype)

Use mock values for demonstrations. Do not commit real account identifiers, CIDRs, topology, customer information, credentials, or operational inventory.

## Prototype versions

### Version 1 — Date-based inventory comparison

The first HTML prototype requests inventory snapshots by date from an external backend endpoint, compares gateway identifiers, and displays the selected snapshot.

### Version 2 — OpenSearch-backed inventory concept

The second HTML prototype queries a configured OpenSearch index, displays inventory fields, and compares records across two selected dates.

These are experimental front-end prototypes. They are not a complete application: the backend API/index, authentication, access controls, deployment configuration, and reliable error handling must be supplied and configured separately.

## Running / configuring

Open the HTML prototype in a browser or serve it through a local static web server. Before connecting it to any backend:

1. Configure a safe test endpoint and synthetic data.
2. Configure authentication and authorization outside the client-side source code.
3. Restrict CORS and network access appropriately.
4. Avoid exposing OpenSearch directly to browsers or unauthenticated users.
5. Add pagination and robust error handling before using larger datasets.

## Limitations

- Prototype UI only; no backend is included.
- Date comparison logic is a starting point and may require adjustment to the actual index schema and timezone semantics.
- Current comparison uses gateway IDs as a basic identity key; a more robust composite key may be needed.
- No automated tests or runtime validation are currently included.

## Roadmap

- Replace direct browser-to-OpenSearch calls with a secure backend API.
- Add synthetic demo data and a sample index mapping.
- Add input validation, loading/error states, and pagination.
- Compare multiple inventory attributes, not only resource IDs.
- Add tests and a repeatable local setup.

## License

No license has been selected yet. All rights reserved by default unless a license file is added.
