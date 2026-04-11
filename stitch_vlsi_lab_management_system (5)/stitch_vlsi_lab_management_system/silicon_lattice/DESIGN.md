# Design System Strategy: The Silicon Blueprint

## 1. Overview & Creative North Star
### Creative North Star: "The Digital Lithography"
This design system is inspired by the precision, layering, and microscopic complexity of VLSI (Very Large Scale Integration) design. It moves away from generic "SaaS dashboards" toward a high-end, editorial experience that feels like a premium terminal for cutting-edge engineering.

The system breaks the "template" look through **Modular Asymmetry**. While a grid exists, elements are grouped into "monolithic blocks" with varying tonal depths. Large-scale typography acts as an architectural anchor, while vibrant accents in `primary` (#81ecff) and `secondary` (#4cf9af) mimic the bioluminescent glow of active circuits and clean-room diagnostics.

---

## 2. Colors: Tonal Depth & The "No-Line" Rule
The color palette is built on a foundation of "True Carbon" blacks and "Obsidian" grays. 

### The "No-Line" Rule
**Explicit Instruction:** Traditional 1px borders are prohibited for sectioning. Structural boundaries must be defined solely through background color shifts. Use `surface-container-low` (#111415) to sit against the main `background` (#0c0e0f). This creates a sophisticated, seamless flow that feels integrated rather than boxed in.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of doped silicon.
- **Level 0 (Foundation):** `surface` (#0c0e0f) - The infinite canvas.
- **Level 1 (Sections):** `surface-container-low` (#111415) - Defining broad workspace areas.
- **Level 2 (Cards/Modules):** `surface-container` (#171a1b) - Individual data clusters.
- **Level 3 (Floating/Active):** `surface-bright` (#292d2e) - Elements that require immediate focus.

### The "Glass & Gradient" Rule
For hero sections or critical CTAs, use semi-transparent `surface_variant` with a 20px `backdrop-blur`. Apply a subtle linear gradient from `primary` (#81ecff) to `primary_dim` (#00d4ec) at a 45-degree angle to provide a "signature" glow that indicates high-tech precision.

---

## 3. Typography: Engineering Authority
We employ a high-contrast pairing: **Space Grotesk** for technical authority and **Manrope** for data clarity.

- **Display & Headlines (Space Grotesk):** These are your "Statement" styles. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) for hero headlines. The brutalist nature of Space Grotesk reflects the precision of VLSI instrumentation.
- **Body & Metadata (Manrope):** Chosen for its exceptional legibility in dense, data-heavy views. `body-md` (0.875rem) is the workhorse for technical descriptions.
- **Labels (Space Grotesk):** Use `label-md` for all-caps technical tags or status indicators to maintain the "instrumentation" aesthetic.

---

## 4. Elevation & Depth
In this system, elevation is an optical illusion created by light, not structure.

### The Layering Principle
Achieve hierarchy by "stacking" tones. A `surface-container-lowest` (#000000) card nested within a `surface-container-low` (#111415) background creates a "recessed" look, ideal for secondary data pods.

### Ambient Shadows
When a floating effect is required (e.g., Modals), use an ultra-diffused shadow:
- **Shadow:** `0 24px 48px -12px rgba(0, 227, 253, 0.08)` (A tinted shadow using the primary color to mimic a neon glow).

### The "Ghost Border" Fallback
If a visual separator is mandatory, use a "Ghost Border": `outline-variant` (#464849) at **15% opacity**. This provides a hint of structure without the "standard UI" clutter.

---

## 5. Components: Technical Primitives

### Buttons
- **Primary:** Background `primary` (#81ecff), Label `on_primary` (#005762). Use `DEFAULT` radius (0.25rem) for a sharp, technical feel.
- **Secondary (The Outline):** Background `transparent`, "Ghost Border" of `primary`, Label `primary`.
- **Tertiary:** Background `transparent`, Label `primary`. No container.

### Input Fields
- **State:** Background `surface-container-high` (#1d2021). No border.
- **Active State:** A 2px bottom-accent in `secondary` (#4cf9af).
- **Error State:** Label and bottom-accent in `error` (#ff716c).

### Data Cards
- **Construction:** Use `surface-container` (#171a1b). Remove all dividers. Separate header from body using a 24px vertical gap from the spacing scale.
- **Micro-Interactions:** On hover, the background shifts to `surface-bright` (#292d2e) with a subtle transition (200ms ease-out).

### Status Chips
- **Nominal:** `secondary_container` (#006c47) background with `secondary` text.
- **Alert:** `error_container` (#9f0519) background with `error` text.
- **Logic:** These chips should always use `label-sm` (Space Grotesk) for a "readout" feel.

---

## 6. Do's and Don'ts

### Do
- **Do** use `primary` (#81ecff) and `secondary` (#4cf9af) sparingly. They are the "current" flowing through the UI; too much causes a short circuit.
- **Do** use large amounts of negative space (`32px` to `64px`) to separate major modular sections.
- **Do** use intentional asymmetry—place a large technical graphic on one side and compact data on the other to create visual interest.

### Don't
- **Don't** use pure white (#ffffff) for text. Always use `on_surface` (#f6f6f7) to reduce eye strain in the dark lab environment.
- **Don't** use standard 1px grey dividers. They break the "Lithography" feel. Use tonal shifts.
- **Don't** use rounded corners larger than `0.5rem` (lg). Roundness should be subtle; VLSI is about precision angles, not "bubbly" consumer tech.