# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

A **data repository** holding ISO/TC 12's plenary and working-group meeting
metadata as structured YAML. No application code, no build step.

## Layout

- `plenary/plenary-meeting-{n}.yaml` — one file per plenary (n = ordinal)
- `wg/{group-id}-{date}.yaml` — working-group meetings
- `reference-docs/` — source PDFs (agenda, minutes, attendance list). Read-only.

## Plenary ordinals

9 = Prague 2010-04-12/13 · 10 = Milan 2012-10-24 · 11 = Berlin 2014-01-29/31 ·
12 = Gaithersburg 2015-06-24-26 · 13 = Stockholm 2016-08-25 ·
14 = Berlin 2017-10-20 · 15 = Web 2018-05-23 · 16 = Helsinki 2018-10-08 ·
17 = Zoom 2020-05-28 · 18 = Zoom 2021-05-26 · 19 = Zoom 2022-05-19 ·
20 = SIS-Sweden 2023-05-25 · 21 = Zoom 2024-05-16 · 22 = Zoom 2025-05-22 ·
23 = Zoom 2026-05-26

## File shape

Mirror `iso-tc154/www.isotc154.org/_data/events/plenary-meeting-NN.yml`:

```yaml
title: "23rd plenary meeting"
ordinal: 23
status: completed
year: 2026
landing_url: /meetings/plenary-meeting-23/

time:
  from: { date: 2026-05-26 }
  to:   { date: 2026-05-26 }

general_area: "Zoom (online)"
country_code: SE

venues:
  - name: Zoom
    link: https://zoom.us/

host: SIS (Sweden)
secretariat:
  name: ...
  organization: SIS
  email: ...

schedule:
  - date: 2026-05-26
    time: "..."
    event: ...
    description: ...

deadlines:
  - date: ...
    description: ...
```

## Editing workflow

1. Make the change in the YAML file.
2. Commit. (No validation step yet — meeting schema is not enforced by `edoxen`;
   that's a future addition if a JSON-Schema is published.)
