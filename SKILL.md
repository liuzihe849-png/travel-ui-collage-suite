---
name: travel-ui-collage-suite
description: "Turn a user's travel photo into an Apple UI inspired social post: either layer system interface over the original scene with the person in front, or place a faithful person cutout on a Freeform-like dotted canvas."
---

# Travel UI Photo

Keep this invocation name for compatibility. The intended output is a **photo interacting with Apple-style interface**, not a paper scrapbook or decorative collage. Use the supplied traveler and confirmed city to make a travel post that resembles a real photo interrupted by iOS/macOS interface elements.

## Self-contained visual baseline
Before selecting a composition, open the bundled [visual reference](assets/reference-original.png) with an image viewing tool and read [layout contract](references/layout-contract.md). The original sample demonstrates photo-overlay. Freeform-cutout is specified in the written rules and has no bundled original sample yet. Do not copy sample defects listed in references/public-sample.md. Reference people, cities and copy are not new-user inputs.

This package must work in a fresh conversation. Do not depend on earlier chat images or missing filenames. The primary cues are modest system-dialog scale, restrained typography, photographic subject prominence and deliberate overlap. A giant white card and input field alone are not an acceptable match.

## Intake

Use the source photo and previously confirmed city/copy from the current session. Ask only for missing city (or no-city choice) and exact greeting/question. For physical objects, read references/confirmed-objects.md: when a city is supplied and no object list is given, actively select 1–2 restrained local accents and briefly state the choice; an omitted list is not an instruction to omit objects. An explicit no-objects request takes precedence. Do not require users to invent the local visual direction themselves. Do not infer a city, dates, sender, booking, or travel facts from the picture. `mode` is optional: `photo-overlay`, `freeform-cutout`, or `auto`. If omitted, choose by the source-photo structure below; do not stop solely to ask for a mode.

## Choose one visual mode

1. **Photo overlay (reference 1):** Default when the original architecture, landscape, lighting, or location matters. Keep the photo full bleed and its background recognizable. Place the moderately sized AirDrop-style panel **behind the person**, using a source-faithful foreground mask to bring the person back over it. Other UI may sit in front where intentional, such as a message input field crossing the lower body. Do not frame the photo as a torn print or replace its background.
2. **Freeform cutout (reference 2):** Use when the source background does not serve the story, or the user requests a clean canvas. Cut out the complete source person and place them on a light, regularly dotted canvas reminiscent of Apple Freeform. Arrange a few Apple-style edit/menu/calendar/message elements around the cutout. Keep the person photographic, large, and free of invented anatomy.

Read [references/style-system.md](references/style-system.md) for the two compositions and layer order. Read [references/person-compositing.md](references/person-compositing.md) when masking the traveler; [references/interface-components.md](references/interface-components.md) when building Apple UI; and [references/confirmed-objects.md](references/confirmed-objects.md) when selecting or placing city objects. Read [references/intake-schema.md](references/intake-schema.md) when collecting inputs or recording delivery QC.

## Non-negotiable visual rules

- The Apple UI language is the primary style: credible system typography, white rounded surfaces, subtle native shadows, iOS blue actions/selection handles, and recognizable AirDrop, edit-menu, calendar, and message patterns. Choose only the components that serve this image. A generic white card with a blue button is insufficient.
- Preserve the supplied person's face, pose, proportions, clothing, accessories, blur, and readable garment details from the source. Extract or composite with masks; do not regenerate, enhance, sharpen, or rebuild the person. When a mask cannot be verified, label the image a preview rather than a formal result.
- Use one coherent scene and the user-selected or agent-curated local objects. Respect any explicit object list, exclusions and no-object choice. Objects can be physical details already in the photo or a small number of inserted accents; they must not turn into a border of stickers. Do not add decorative landmarks, paper scraps, ginkgo leaves, gold ornaments, wax seals, or receipt textures by default.
- Do not add a cast shadow, drop shadow, glow, dark outline, or duplicated-alpha shadow to any inserted physical object. Keep its transparent edge clean and use placement, scale, and source-like light to integrate it. This restriction is for physical objects; subtle native UI-surface shadows remain allowed.
- Preserve exact user-supplied copy. Interface chrome may use standard UI labels such as `AirDrop`, `Cut`, or `Copy`, but do not invent sender names, dates, times, routes, prices, bookings, or message content.
- Do not flatten the hierarchy. In photo-overlay mode, the person must visibly occlude the AirDrop panel. In Freeform-cutout mode, the cutout must sit naturally over the dotted canvas while selected foreground UI may cross it.

## Natural interaction
Treat subject, rear UI, foreground input and local accents as one composition. Adapt panel position and scale to the subject; keep face, hand and headwear legible. Place the AirDrop title and action labels where the original silhouette does not accidentally bisect every word. Avoid tangencies where panel corners meet hats, fingers or straps. Use clean antialiased subject edges with at most a subpixel transition; broad feathering or a dark fringe is not natural integration. Keep the original exposure and subtle UI-surface shadows. Place the input near the waist/upper legs without hiding a large part of the clothing; local accents balance open left/right areas without crowding the person.

Before delivery, inspect a zoomed view of hair/hat, glasses, raised hand, shoulder and bag where they meet UI, plus the whole composition. Retained background slivers, polygon-shaped cutouts and damaged accessories require repair. Preserve source-person pixels; generating an entirely new person is not a fix.

## Natural interaction
Treat subject, rear UI, foreground input and local accents as one composition. Adapt panel position and scale to the subject; keep face, hand and headwear legible. Place the AirDrop title and action labels where the original silhouette does not accidentally bisect every word. Avoid tangencies where panel corners meet hats, fingers or straps. Use clean antialiased subject edges with at most a subpixel transition; broad feathering or a dark fringe is not natural integration. Keep the original exposure and subtle UI-surface shadows. Place the input near the waist/upper legs without hiding a large part of the clothing; local accents balance open left/right areas without crowding the person.

Before delivery, inspect a zoomed view of hair/hat, glasses, raised hand, shoulder and bag where they meet UI, plus the whole composition. Retained background slivers, polygon-shaped cutouts and damaged accessories require repair. Preserve source-person pixels; generating an entirely new person is not a fix.

## Production and handoff

Use deterministic compositing for protected source pixels and exact UI text where possible. AI-generated concepts may guide layout or make isolated non-person objects, but do not use a regenerated full scene as proof of person fidelity. Default to one portrait PNG plus a sharing JPG. Before formal delivery, inspect the actual image for mode, photo/person fidelity, background treatment, front/back layering, Apple UI appearance, exact copy, selected object count, object-shadow absence, and dimensions. Record these in a short QC handoff; if a required check is uncertain, call the result a preview.

All person masking, Apple UI, and confirmed-object guidance is included in this one Skill through the references above. No companion Skill invocation is required.

## Author and public reference

Created and maintained by **理智画** (GitHub: [liuzihe849-png](https://github.com/liuzihe849-png)). Inspect [the original sample](assets/reference-original.png) and read [sample scope and limitations](references/public-sample.md). The sample is a visual aid, not a user identity or proof of exact fidelity. Do not copy sample-specific defects into new outputs.
