# IED 2026–27 — student-facing course site

Live site: https://kyle-sherman-projects.github.io/IED_site_26-27/

PLTW Introduction to Engineering Design. Everything under `docs/` is **generated**
from the private planning repo (`ied-course`) by `scripts/build_ied_site.py`. This
repo holds only the built HTML — no PLTW curriculum material lives here.

## Editing published pages

Regenerating overwrites every page under `docs/`, so hand-edits to a generated file
are lost on the next build. To change what a page says, change it at the source in
`ied-course` and rebuild:

- lesson dates, topics, essential questions, transferable skills, K&S codes
  → `planning/IED Lesson Plan Schedule 2026-2027.md`
- a lesson's learning target or what students hand in
  → the `## Objective` / `## Exemplar / Closure` sections of that lesson's
    `lesson_plans/<unit>/LP_*.md`
- page layout, colors, typography → `scripts/ied_template.html`

Then run `python scripts/build_ied_site.py` and commit here.

## What is deliberately not published

The generator publishes only a lesson plan's Objective and Exemplar / Closure
sections. Co-teaching notes, SWIEP/ELL accommodation language, anticipated
misconceptions, response-to-data plans, know/show tables, and the minute-by-minute
agenda are excluded by design, and the build scans every page and **fails** rather
than publishing them. Rubrics are named on unit pages but their contents are never
read or published — they carry teacher scoring notes.

If you add content here by hand, keep that constraint in mind: this repo is public.
