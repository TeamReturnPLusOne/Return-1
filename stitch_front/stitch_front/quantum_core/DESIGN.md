# Design System: The Neon Scientific Ledger

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Kinetic Laboratory."** 

Unlike standard research portals that feel static and clinical, this system envisions a living, breathing digital organism. We are moving away from the "template" look of boxes-inside-boxes. Instead, we embrace **Organic Sci-Fi**: a high-contrast, dark-mode environment where data flows like energy. 

The layout utilizes **intentional asymmetry**—placing heavy display typography against expansive negative space—to mimic a sophisticated heads-up display (HUD). By overlapping glass layers and using neon "light leaks," we transform a community website into an immersive research vessel.

---

## 2. Colors & Surface Philosophy
The palette balances deep space (`#131313`) with hyper-saturated neon accents to create a sense of focused energy.

### The "No-Line" Rule
Traditional borders are archaic. **Do not use 1px solid strokes to define sections.** Boundaries must be established through:
*   **Tonal Shifts:** Placing a `surface_container_low` section against a `background` base.
*   **Luminous Transitions:** Using subtle, large-scale radial gradients (e.g., a 20% opacity `tertiary_container` glow) to "anchor" a content area.

### Surface Hierarchy & Glassmorphism
Treat the UI as a series of stacked, semi-transparent lenses.
*   **The Base Layer:** Use `surface` (#131313) for the deep background.
*   **The Glass Layer:** Floating components (cards, navigation) must use `surface_container` with a `backdrop-blur` of 12px–20px and an opacity of 60-80%.
*   **The Signature Glow:** Main CTAs or active states should utilize a linear gradient from `primary` (#e5ffe3) to `primary_container` (#7af495) to provide a "charged" aesthetic.

---

## 3. Typography
The system utilizes a dual-font approach to balance "High-Tech" authority with "Scientific" readability.

*   **Display & Headlines (Uxum Grotesque / Space Grotesque):** Used for `display-lg` through `headline-sm`. These are the "hero" elements. Their slightly wider stance and technical geometry should be set with tight letter-spacing (-2%) to feel like a high-end editorial piece.
*   **Interface & Data (Inter):** Used for all `title`, `body`, and `label` roles. Inter provides the "Scientific Sans-Serif" clarity required for dense research data. Use `label-md` in uppercase with +5% letter-spacing for a "serialized" HUD look.

---

## 4. Elevation & Depth
In this design system, depth is a product of light, not shadow.

*   **Tonal Layering:** Achieve hierarchy by "nesting" tokens. A `surface_container_highest` element should sit inside a `surface_container` area to create a soft, natural lift.
*   **Ambient Shadows:** If a "floating" effect is required (e.g., a modal), use a massive blur (40px+) with the shadow color set to a 10% opacity version of `tertiary` (#e8fbff). This mimics the way light scatters in a neon environment.
*   **The "Ghost Border" Fallback:** For accessibility in complex data tables, use the `outline_variant` token at **15% opacity**. It should be felt, not seen.
*   **Interactive Grids:** Use a subtle "dot grid" pattern (1px dots, 24px apart) using `outline_variant` at 5% opacity in the background of `surface` to reinforce the scientific-ledger theme.

---

## 5. Components

### Buttons
*   **Primary:** A high-contrast "Power-On" state. Background: `primary_container`. Text: `on_primary_container`. No border. On hover: Add a 10px outer glow (drop-shadow) using the `primary` color.
*   **Secondary (Glass):** Background: 10% opacity `primary`. Backdrop-blur: 8px. Text: `primary`.
*   **Tertiary:** No background. Text: `tertiary`. Underlined with a 2px `secondary` stroke only on hover.

### Cards & Data Modules
*   **Strict Rule:** No dividers. Use `surface_container_low` for the card body and `surface_container_high` for the header area of the card. 
*   **Corner Treatment:** Use `md` (0.375rem) for a precision-engineered look. Avoid large, friendly rounds.

### Input Fields
*   **State:** Default inputs are `surface_container_lowest` with a bottom-only `outline_variant` (20% opacity).
*   **Focus:** The bottom border animates to 100% opacity `tertiary_fixed`, accompanied by a subtle `tertiary` glow.

### Additional Components: "The Data Pulse"
*   **Status Orbs:** Small, pulsing circular indicators using `secondary` (pink) for "Live Research" and `primary` (green) for "Verified Data."
*   **Activity Sparklines:** Compact, monochromatic graphs using `tertiary_fixed_dim` to show research trends within list items.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use extreme scale. Pair a `display-lg` headline with a `body-sm` caption for a high-end editorial feel.
*   **Do** let elements overlap. A glass card should partially obscure a background glow or grid pattern to create depth.
*   **Do** use `tertiary` (cyan/blue) as your "Action" color and `secondary` (pink) as your "Discovery/Highlight" color.

### Don’t:
*   **Don’t** use pure white (#FFFFFF) for body text. Use `on_surface_variant` (#bdcaba) to reduce eye strain in dark mode.
*   **Don’t** use solid black (#000000) for surfaces. Use the `surface` token (#131313) to allow for depth layering.
*   **Don’t** use standard "drop shadows." If a component needs to stand out, use tonal shifts or backdrop blurs.