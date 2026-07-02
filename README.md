# A Working Glossary of Making — Interactive Companion

A single-file interactive companion to the studio glossary *"A Working Glossary of Making, from Analogue to Digital"*. Built as a seminar tool: 410 terms with search, an A–Z index, automatic cross-links between definitions, and six curated **threads** — routes through the glossary, walked term by term.

No build step, no dependencies, no backend. Everything lives in `index.html`.

## Publish on GitHub Pages

1. Create a new repository on GitHub (e.g. `studio-glossary`).
2. Upload `index.html` and this `README.md` to the repository root.
3. In the repository: **Settings → Pages → Build and deployment → Source: "Deploy from a branch"**, branch `main`, folder `/ (root)`. Save.
4. After a minute the site is live at `https://adpchrgruber.github.io/adp_adv_26_glossary/`.

A custom domain (e.g. `glossary.yourstudio.com`) can be added later under the same Pages settings.

## Sharing with students

Views are deep-linkable via the URL hash, so specific positions can go straight into a syllabus:

- `…/#/index` — the searchable A–Z index
- `…/#/threads` — all threads
- `…/#/thread/what-the-scan-loses/5` — thread *What the Scan Loses*, term 5

Arrow keys (← →) step through a thread.

## Editing content

All content is embedded as two JSON blocks at the top of the `<script>` section in `index.html`:

- `GLOSSARY` — the terms (`t` = term, `d` = definition, `s` = slug) and the introduction paragraphs.
- `THREADS` — each thread has an `id`, `title`, `thesis`, and `steps`: pairs of `["term name", "annotation on why this term sits here"]`. Term names must match a glossary term exactly.

To add or reorder a thread, edit `THREADS` directly — the toolpath, step counts, and index cross-links update themselves.

The six current threads (annotations included) are a first editorial pass and are meant to be rewritten by the studio.

## License

Choose before publishing: a code license (MIT is a common choice) and, separately, a license for the glossary text itself (e.g. CC BY-NC-SA 4.0 if you want attribution, no commercial reuse, share-alike). Add them as `LICENSE` and a note in this README.
