# Person compositing

## Two composites

- `photo-overlay`: Keep the original photo as the full background. Make a foreground mask of the person, place the rear AirDrop panel over the photo, then composite the masked source person back above it. Keep scenery and body aligned to their original coordinates. Foreground message UI may cross the lower body intentionally.
- `freeform-cutout`: Extract the complete person and place the source pixels on a light, evenly dotted canvas. Preserve the pose and scale the entire person as one unit; place rear UI below and selected message UI above.

Retain all source-visible head/hair/headwear, face, hands, fingers, clothing, bags, straps, held objects, legs, socks, and shoes. Do not invent parts outside the source frame. Do not enhance a blurred face, rewrite garment text, reshape anatomy, or reconstruct missing body areas. Use a controlled alpha edge without a sticker border or glow. If masking is uncertain, label the result a preview.

Before delivery, check: source face/pose/proportions/blur unchanged; no halo, bright fringe, hard rectangular remnants, or missing hair/straps; the person clearly occludes the rear AirDrop panel in photo-overlay mode; the original background alone is removed in Freeform mode; foreground UI remains a separate layer rather than being painted into the body.
