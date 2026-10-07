# Reference-derived layout contract

Open ../assets/reference-original.png before production. The bundled original preview demonstrates photo-overlay only; freeform-cutout currently has written composition rules but no original visual example. This is a visual baseline, not a source of new user facts.

## Photo-overlay
Keep the entire photograph full bleed and preserve its natural color. Subject remains dominant. The reference dialog is approximately 60% of photo width and 27% of photo height, positioned around x=20-80%, y=18-46%. Adapt those approximate ratios to the actual head and shoulder position rather than treating them as fixed coordinates. Its bottom region is occluded by the original head/upper torso; do not place the entire person in front of a huge blank white background.

AirDrop title is centered in the visible top area, in restrained system typography (roughly 3.5% of photo width). If the user supplies a second short sentence, center it beneath the title. Otherwise omit that sentence; do not invent a sender or city message. Avoid inserting an oversized blue AirDrop glyph to fill space. Standard Decline/Accept labels occupy a compact divided bottom action row; subject occlusion is intentional.

Foreground input is approximately 65% of photo width, 6-8% of photo height, crossing waist/upper legs. Text is 3-4% of photo width, with compact blue send arrow, pale blue selection highlight and selection handles tightly bracketing the actual text. Don't leave a large highlighted empty area after the greeting. Preserve exact supplied text.

## Freeform-cutout
Use very light canvas with fine evenly spaced dots, no paper texture. The complete photographic source subject fills approximately 70-80% of canvas height. Preserve their original pose; do not invent a running pose just because the reference person runs. Keep a compact edit menu near the top, a single blue Messages bubble near the body ONLY if message copy was supplied, and a slim input along the bottom. No invented calendar date/event. Keep whitespace around the silhouette and menu.

## Fidelity and execution
Source person pixels are protected. Prefer a genuine segmentation mask or carefully traced contour, not a coarse polygon presented as finished extraction. A manual mask may produce a preview; visible wall fragments, missing clothing, cut-off hat edges and dark/bright fringes fail formal delivery. Inspect edges over both light and dark temporary backgrounds where useful.

Deterministic UI drawing is allowed, but does not excuse incorrect component shape, oversized surfaces or weak reference matching. Generative layout studies are preview-only and must not be represented as unchanged-source delivery. Do not regenerate the person to solve a masking problem.

## Reject and repair
Reject a photo-overlay with a dialog spanning nearly the full width, huge title/radiating logo, or most of the upper photo replaced by blank white. Reject a text selection that extends far beyond the greeting. Reject a mask with retained building fragments. These describe a failed implementation, not a valid third mode.

Before delivery, compare the actual output against the appropriate inner reference: subject prominence, dialog/menu scale, text hierarchy, whitespace, background treatment, overlap and mask edges. Repair observable deviations before reporting completion. Record uncertain checks as preview; textual compliance alone is insufficient.
