---
name: travel-ui-collage-suite
description: "Turn a user's travel photo into an Apple UI inspired social post: either layer system interface over the original scene with the person in front, or place a faithful person cutout on a Freeform-like dotted canvas."
---

# Travel UI Photo

Keep this invocation name for compatibility. The intended output is a **photo interacting with Apple-style interface**, not a paper scrapbook or decorative collage. Use the supplied traveler and confirmed city to make a travel post that resembles a real photo interrupted by iOS/macOS interface elements.

## Intake

Confirm the source photo, city (or no-city choice), any 1–3 requested physical objects, and exact user-facing greeting/question. Do not infer a city, dates, sender, booking, or travel facts from the picture. `mode` is optional: `photo-overlay`, `freeform-cutout`, or `auto`. If omitted, choose by the source-photo structure below; do not stop solely to ask for a mode.

## Choose one visual mode

1. **Photo overlay (reference 1):** Default when the original architecture, landscape, lighting, or location matters. Keep the photo full bleed and its background recognizable. Place the large AirDrop-style panel **behind the person**, using a source-faithful foreground mask to bring the person back over it. Other UI may sit in front where intentional, such as a message input field crossing the lower body. Do not frame the photo as a torn print or replace its background.
2. **Freeform cutout (reference 2):** Use when the source background does not serve the story, or the user requests a clean canvas. Cut out the complete source person and place them on a light, regularly dotted canvas reminiscent of Apple Freeform. Arrange a few Apple-style edit/menu/calendar/message elements around the cutout. Keep the person photographic, large, and free of invented anatomy.

Read [references/style-system.md](references/style-system.md) for the two compositions and layer order. Read [references/person-compositing.md](references/person-compositing.md) when masking the traveler; [references/interface-components.md](references/interface-components.md) when building Apple UI; and [references/confirmed-objects.md](references/confirmed-objects.md) only when the user selected objects. Read [references/intake-schema.md](references/intake-schema.md) when collecting inputs or recording delivery QC.

## Non-negotiable visual rules

- The Apple UI language is the primary style: credible system typography, white rounded surfaces, subtle native shadows, iOS blue actions/selection handles, and recognizable AirDrop, edit-menu, calendar, and message patterns. Choose only the components that serve this image. A generic white card with a blue button is insufficient.
- Preserve the supplied person's face, pose, proportions, clothing, accessories, blur, and readable garment details from the source. Extract or composite with masks; do not regenerate, enhance, sharpen, or rebuild the person. When a mask cannot be verified, label the image a preview rather than a formal result.
- Use one coherent scene and only the confirmed objects. Objects can be physical details already in the photo or a small number of inserted accents; they must not turn into a border of stickers. Do not add decorative landmarks, paper scraps, ginkgo leaves, gold ornaments, wax seals, or receipt textures by default.
- Do not add a cast shadow, drop shadow, glow, dark outline, or duplicated-alpha shadow to any inserted physical object. Keep its transparent edge clean and use placement, scale, and source-like light to integrate it. This restriction is for physical objects; subtle native UI-surface shadows remain allowed.
- Preserve exact user-supplied copy. Interface chrome may use standard UI labels such as `AirDrop`, `Cut`, or `Copy`, but do not invent sender names, dates, times, routes, prices, bookings, or message content.
- Do not flatten the hierarchy. In photo-overlay mode, the person must visibly occlude the AirDrop panel. In Freeform-cutout mode, the cutout must sit naturally over the dotted canvas while selected foreground UI may cross it.

## Production and handoff

Use deterministic compositing for protected source pixels and exact UI text where possible. AI-generated concepts may guide layout or make isolated non-person objects, but do not use a regenerated full scene as proof of person fidelity. Default to one portrait PNG plus a sharing JPG. Before formal delivery, inspect the actual image for mode, photo/person fidelity, background treatment, front/back layering, Apple UI appearance, exact copy, selected object count, object-shadow absence, and dimensions. Record these in a short QC handoff; if a required check is uncertain, call the result a preview.

All person masking, Apple UI, and confirmed-object guidance is included in this one Skill through the references above. No companion Skill invocation is required.
