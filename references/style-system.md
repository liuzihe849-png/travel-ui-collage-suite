# Apple UI travel photo: reference-derived style system

The references share Apple interface language, a photographic traveler, and deliberate UI/subject occlusion. They do **not** share a paper-scrapbook background. Treat the two layouts as alternate modes, never blend their backgrounds by default.

## Mode A — original photo + layered UI (reference `12.jpg`)

- Keep the source photograph edge-to-edge. The building, landscape, light, perspective, and travel context remain legible.
- Place a large white AirDrop system panel in the original scene, around the upper middle. Its lower portion must disappear **behind the person's head/shoulders**; the person is extracted from the same photo and composited back over the panel with a clean mask. This is the reference's defining depth cue.
- Put a slim iOS message/input field across the lower torso or waist. Blue selection handles and a blue circular send control can make it read as live editable text. A second lower AirDrop action row can sit behind the legs if composition allows.
- Use a few approved physical objects as spatial accents only. They should not form a sticker frame. Retain the source's color and real-world texture rather than recoloring it to an ivory palette.
- Layer order: original photo → rear AirDrop panel/action row → source-person mask → approved props where physically plausible → foreground input/selection UI.

## Mode B — Freeform-like dotted canvas + cutout (reference `截屏2026-09-20 10.23.49.png`)

- Remove the source background cleanly. Place the full photographic person directly on a very light white/warm-gray canvas with **small, evenly spaced dots**. The dots are regular interface canvas texture, not paper fibres, stains, or a printed page.
- The person dominates the page and may be in motion; the mask retains hair, hands, clothing, bags, held objects, shoes, and source blur. Avoid an outline or sticker border.
- Use an Apple-like text-edit context menu near the top (`Cut`, `Copy`, `Paste`, `Replace…`), plus one compact calendar/event card or similar system module in open space. A blue Messages-style chat bubble can overlap the body. The bottom iMessage-style input bar may show selected greeting text and blue selection handles.
- Approved city objects may float near the person, but their count and scale remain subordinate to the UI/subject interaction.
- Layer order: dotted canvas → rear context/calendar elements and approved objects → source-person cutout → foreground chat/input elements.

## UI fidelity shared by both modes

- Use real iOS/macOS visual grammar: San Francisco-like system sans typography, accurate type hierarchy, clean spacing, native corner radii, white or light-gray surfaces, subtle soft shadows, system-blue actions (approximately `#007AFF`), and correctly shaped selection handles. Component structure should be recognizable before any decorative elements are added.
- Choose a small coherent set of components; do not create a generic dashboard or random white pills. An AirDrop card should read as an AirDrop share/accept interface; an edit menu should read as a system text menu; a message field should read as an editable input.
- Standard UI chrome labels may follow the reference. User-specific values (sender, date, event, route, city greeting, question) require user input; omit or use a clearly labeled preview placeholder when unknown.
- UI has crisp edges and readable text. The photograph/cutout retains its native grain, blur, and color. Subtle shadows may establish UI-surface depth only; inserted physical objects have no added drop/cast shadow, even when placed beside a UI panel.
- Keep a portrait social-post proportion near 3:4 or 4:5 unless the user specifies another ratio.

## Failure examples to reject

- The source photo is shrunk into a torn-edge print on textured parchment.
- AirDrop is merely a card at the top and does not sit behind the person.
- A regenerated traveler or building looks similar but changes source identity/details.
- Panda, food, tickets, seals, leaves, and sketches become a decorative ring around the photo.
- The Freeform mode uses irregular speckles or paper texture instead of a disciplined dot grid.
- UI text is invented, misspelled, or rendered as pseudo-letters.

## Mode selection check

For a night bridge portrait with a person at the railing, choose Mode A by default: the illuminated bridge is useful travel context. Mode B is appropriate if the user requests a clean cutout/Freeform page or if the original background would compete with the interface.
