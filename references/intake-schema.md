# Travel UI photo intake and QC

Use this compact record before generation. `mode: auto` allows the skill to choose from the source photo; it is not an additional mandatory question.

```yaml
source_photo: "/absolute/path/to/user-photo.jpg"
city: "成都" # confirmed by user, or no-city
mode: "auto" # photo-overlay | freeform-cutout | auto
props: ["熊猫", "火锅", "民谣"] # user-selected; [] is allowed
greeting: "hello Chengdu!!" # optional; preserve exact text
question: "where are we going next?" # optional; preserve exact text
holiday_context: null # only if user supplies it
layout: "portrait 3:4"
```

If city or a requested text/object choice is unresolved, ask only for the missing value. Do not infer travel facts from the photo. Do not add a National Day label, date, or sender just because this is a holiday-post use case.

Final QC record:

- chosen mode and reason; source photo and final dimensions;
- Mode A: original background retained, AirDrop panel visibly behind the source person, foreground UI layer distinct;
- Mode B: original background removed, regular dotted canvas, complete source-person cutout;
- protected person fidelity, including face/clothing/pose and source blur;
- selected objects and visible count; exact user copy and all visible UI text;
- no invented sender/date/price/booking or unintended paper-collage decoration.
