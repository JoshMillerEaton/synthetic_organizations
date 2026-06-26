# Synthetic Organizations

This repository documents a research workflow for reconstructing how engineering consultancies are organized and how they deliver hyperscale and AI data center programs.

It currently focuses on two firms with strong public evidence and enough source material to support a structured synthesis:
- Jacobs
- Burns & McDonnell

## What This Repository Contains

Each company is represented by two documents:

- a dossier that collects and ranks public evidence
- a synthesis that normalizes the evidence into a common analytical framework

The result is a comparable view of:
- company structure
- service domains
- workflows and delivery models
- evidence-backed inferences
- areas of repeatability that may be suitable for automation or agent-based simulation

## Methodology

The documentation in this repository was generated through a repeatable research process:

1. Identify consultancies that operate in the hyperscale, mission-critical, or data center engineering space.
2. Rank candidate firms by relevance, breadth of service capabilities, and availability of public evidence.
3. Build a dossier for the strongest candidates using sources such as:
   - company websites
   - leadership and team pages
   - press releases
   - project announcements
   - industry rankings
   - trade publications
   - job postings and thought leadership
4. Use the dossier to infer organizational structure, service lines, project roles, and delivery workflows.
5. Generate a synthesis framework that standardizes how each firm is documented.
6. Complete the framework for each company, tagging every item as:
   - Observed
   - Inferred
   - Uncertain
7. Organize the finished outputs so firms can be compared side by side using the same structure.

## Research Scope

The project is centered on engineering consultancies that support hyperscale data center development, especially firms with capabilities in:

- electrical engineering and power systems
- mechanical engineering and cooling
- EPCM, design-build, and program delivery

The current examples were selected because they combine:
- strong relevance to data center infrastructure
- multidisciplinary delivery models
- enough public material to reconstruct structure and workflow

## Repository Structure

- `dossier_jacobs.md` - source-rich dossier for Jacobs
- `dossier_burns_&_mac.md` - source-rich dossier for Burns & McDonnell
- `synthesis_jacobs.md` - completed synthesis for Jacobs
- `synthesis_burns_&_mac.md` - completed synthesis for Burns & McDonnell
- `prompts/` - reusable prompts and frameworks used to generate the research outputs

## How To Read The Documents

The dossier files are the evidence base. They collect public sources and summarize what can be verified about each firm.

The synthesis files convert that evidence into a normalized model. Each completed item is tagged to show its confidence level:

- Observed - directly supported by source material
- Inferred - derived from evidence and context
- Uncertain - plausible but not strongly evidenced

This makes it easier to distinguish between documented facts and modeled interpretation.

## Output Conventions

The repository uses a consistent markdown format so results can be compared across companies.

Key conventions include:
- numbered inline citations in dossiers and syntheses
- standardized section headers
- repeated functional blocks for each service domain
- Mermaid diagrams for organizational and workflow views
- references sections that map cited sources back to their original URLs
- a variability and assumptions section that defines the confidence tags

## Current Coverage

The repository currently contains completed documentation for two consultancies:

- Jacobs - a large global engineering and program delivery firm
- Burns & McDonnell - an employee-owned design-build and EPC firm with deep mission-critical capability

Together, they provide a useful comparison set for studying how consultancies in this space are structured and how they deliver hyperscale data center work.

## Extending The Repository

The same workflow can be reused for additional firms.

A typical extension would involve:
1. selecting another consultancy in the target market
2. building a dossier from public sources
3. generating a synthesis from the shared framework
4. comparing the new company against the existing pair

## Notes

This repository is for research and synthesis, not software development.

The documents are designed to be expanded as new firms, new sources, or new analytical dimensions are added.