# Design System Strategy: The Architectural Consultant

## 1. Overview & Creative North Star
**Creative North Star: "Precision Transparency"**

This design system moves beyond the generic "Corporate Tech" aesthetic to establish a visual language of high-level advisory and architectural clarity. We reject the "template" look characterized by rigid grids and 1px borders. Instead, we embrace **Precision Transparency**: a layout strategy that uses intentional asymmetry, overlapping editorial-scale typography, and deep tonal layering.

The goal is to make 'Phil Simpson Consulting' feel like a premium, bespoke service rather than a high-volume agency. We achieve this by utilizing expansive breathing room and a "Swiss-Editorial" approach to information hierarchy, where the weight of the typography and the depth of the surfaces do the structural work—not lines or boxes.

---

## 2. Color & Surface Logic
The palette is anchored in trust but activated by digital luminescence. We move away from flat hex codes toward a functional "Surface Ecosystem."

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders to define sections. Layout boundaries must be defined exclusively through background color shifts.
*   *Example:* A `surface-container-low` section sitting directly on a `surface` background. This creates a "soft-edge" transition that feels organic and premium.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of frosted glass. 
- **Base Layer:** `surface` (#f8f9fa)
- **Secondary Sectioning:** `surface-container-low` (#f3f4f5)
- **Interactive/Floating Elements:** `surface-container-lowest` (#ffffff) for maximum "lift."
- **In-Set Details:** `surface-container-high` (#e7e8e9) for nested information blocks.

### The "Glass & Gradient" Rule
To avoid a "flat" corporate feel, use Glassmorphism for floating navigation or modal overlays. 
- **Implementation:** Apply `surface` with 80% opacity and a `backdrop-blur` (12px-20px).
- **Signature Textures:** Use subtle linear gradients for Hero backgrounds, transitioning from `primary` (#041627) to `primary-container` (#1a2b3c) at a 135-degree angle. This adds "visual soul" and a sense of infinite depth.

---

## 3. Typography
We use a dual-font strategy to balance authority with accessibility.

*   **Display & Headline (Manrope):** Chosen for its geometric precision. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) for hero statements to command attention.
*   **Body & Labels (Inter):** Chosen for maximum legibility. Inter's tall x-height ensures that even `body-sm` (0.75rem) remains crisp on high-resolution displays.

**Hierarchy as Identity:** 
High-contrast scaling is mandatory. Pair a `display-md` headline with a `body-lg` intro text to create an editorial "Entry Point." The contrast between the bold, architectural Manrope and the neutral Inter conveys a consultant who is both a visionary and a pragmatist.

---

## 4. Elevation & Depth
In this system, depth is a functional tool, not a decoration.

### Tonal Layering
Avoid shadows for standard cards. Instead, "stack" tiers. Place a `surface-container-lowest` card (Pure White) on a `surface-container` (#edeeef) background. This creates a natural, soft lift that feels integrated into the architecture.

### Ambient Shadows
When an element must float (e.g., a primary CTA or a dropdown), use an **Ambient Shadow**:
- **Color:** Use a 6% opacity tint of `on-surface` (#191c1d).
- **Blur:** Large values (30px - 50px) with a subtle Y-offset (10px). This mimics natural gallery lighting rather than a digital "drop shadow."

### The "Ghost Border" Fallback
If a border is required for accessibility (e.g., in a high-density data table), use a **Ghost Border**:
- **Token:** `outline-variant` (#c4c6cd) at **15% opacity**.
- **Rule:** Never use 100% opaque borders. They clutter the visual field.

---

## 5. Components

### Buttons
*   **Primary:** Background: `secondary` (#00677d) | Text: `on-secondary` (#ffffff). Use a subtle gradient to `secondary-container` for depth.
*   **Secondary:** Background: `transparent` | Ghost Border (15% opacity `outline`) | Text: `secondary`.
*   **Rounding:** Always use `md` (0.75rem / 12px) to balance modern tech with corporate stability.

### Input Fields
*   **State Logic:** Use `surface-container-lowest` for the field background. 
*   **Focus State:** Instead of a thick border, use a 2px outer glow of `secondary` at 20% opacity.

### Cards & Lists
*   **The "No-Divider" Mandate:** Forbid the use of horizontal lines between list items. Use the **Spacing Scale** (specifically `spacing-4` or `spacing-6`) to create separation via white space.
*   **Contextual Elevation:** On hover, a card should transition from `surface-container-lowest` to a subtle `surface-dim` or gain an **Ambient Shadow**.

### Signature Component: The "Expertise Tile"
A specialized card for consulting services. Use a `secondary-fixed` (#b3ebff) accent bar (4px wide) on the left side of a `surface-container-low` card to denote "active" or "featured" expertise without overwhelming the minimalist aesthetic.

---

## 6. Do's & Don'ts

### Do:
*   **Embrace Asymmetry:** Align text to a 12-column grid, but allow imagery or accent elements to bleed off-canvas or overlap container boundaries.
*   **Use the Spacing Scale:** Stick strictly to the defined increments (e.g., `10` for section padding, `3` for internal card padding).
*   **Prioritize Type:** Let the size and weight of the font define the start of a new section, not a background color change.

### Don't:
*   **Don't use "Pure Black":** Use `primary` (#041627) or `on-surface` (#191c1d) for text to maintain a high-end, softer feel.
*   **Don't over-round:** Avoid the `full` pill-shape for anything other than small chips. Stick to `md` (12px) for structural reliability.
*   **Don't use standard shadows:** If the shadow looks like a "Photoshop Default," it is too dark. Lighten and diffuse.

---

## 7. Spacing & Rhythm
The spacing scale is non-linear to encourage "Breathing Room."
- Use **`spacing-20` (7rem)** for vertical section padding. This luxury of space signals that the brand is not "cramped" or "rushed"—key traits for a high-value consultant.
- Use **`spacing-1.5` (0.5rem)** for tight metadata grouping (e.g., Label above an Input).