# Apple UI components

The interface should look like iOS/macOS UI appearing in the photograph or on a Freeform-like dotted canvas, not like paper stickers.

- **AirDrop:** Large white rounded system dialog with a clear `AirDrop` title and action area. In photo-overlay mode, put it behind the source person; the person masks off the panel where they overlap.
- **Text edit menu:** Compact white rounded floating menu with standard `Cut`, `Copy`, `Paste`, `Replace…` labels and native-like separators. Use on the Freeform canvas when it supports the scene.
- **Messages:** Clean blue message bubble or white input field, with a blue circular send arrow. If text is selected, draw correctly placed blue selection handles at the text edges.
- **Calendar/event:** Compact white card with familiar date hierarchy and one event row. Require the user's actual date/event text; omit factual fields when unknown.

Use SF-style system typography, dark text, clean spacing, consistent rounded corners, restrained shadows, and system blue (approximately `#007AFF`). Choose only a few components with a clear relationship to the person. A generic stack of cards fails the style. UI surfaces are crisp while the source photo keeps its native texture.

Preserve user-provided greeting and question exactly. Standard interface commands can use their conventional labels, but never invent sender names, dates, flight times, prices, or booking details. Check every visible word and icon at viewing size. If exact UI text cannot be verified, label the image a preview.
