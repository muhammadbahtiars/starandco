# Design System Document: The Modern Pastoral

## 1. Overview & Creative North Star
**Creative North Star: "The Modern Pastoral"**
This design system moves away from the "commodity" look of traditional agriculture. We are blending the organic, raw honesty of cattle farming with the clinical precision of high-end dairy processing. The goal is to create a digital experience that feels like a premium lifestyle magazine—airy, editorial, and authoritative.

To break the "template" feel, we employ **Intentional Asymmetry**. Do not align every image to a rigid grid; allow high-quality photography of lush pastures or morning dew to bleed off-canvas or overlap with typography. We prioritize "Breathing Room" (generous whitespace) to signal luxury and cleanliness, ensuring every element feels curated rather than cluttered.

---

## 2. Colors & Surface Philosophy
The palette is rooted in the earth but refined for the screen. We use deep greens and milk whites not just as colors, but as structural tools.

### The "No-Line" Rule
**Strict Mandate:** Designers are prohibited from using 1px solid borders to define sections or containers. Boundary definition must be achieved through:
*   **Background Shifts:** Transitioning from `surface` (#f9f9ff) to `surface-container-low` (#f1f3ff).
*   **Tonal Nesting:** A `surface-container-lowest` (#ffffff) card sitting on a `surface-container` (#e8edff) background.
*   **Shadow Depth:** Using light to define edges rather than ink.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of premium materials.
*   **Base Layer:** `surface` (#f9f9ff) – The "Milk White" foundation.
*   **Sectioning:** Use `surface-container-low` for large content blocks to subtly separate them from the hero.
*   **Focus Elements:** Use `surface-container-highest` (#d7e2ff) for high-importance callouts or utility bars.

### The "Glass & Gradient" Rule
To achieve a "kekinian" (trendy) feel, use **Glassmorphism** for floating navigation bars or overlay cards. 
*   **Token Application:** Use `surface` at 70% opacity with a `backdrop-filter: blur(20px)`.
*   **Signature Textures:** Apply a subtle linear gradient from `primary` (#154212) to `primary_container` (#2d5a27) on primary action buttons to give them a "living" organic depth.

---

## 3. Typography
Our typography strategy pairs the architectural strength of **Manrope** with the friendly fluidity of **Plus Jakarta Sans**.

*   **Display & Headlines (Manrope):** These are your "Editorial Voice." Use `display-lg` and `headline-lg` with tight letter-spacing (-0.02em) to create an authoritative, high-end look.
*   **Body & Labels (Plus Jakarta Sans):** Chosen for its modern, approachable geometry. It ensures that technical dairy processing info remains readable and "fresh."
*   **Hierarchy Note:** Use `on_surface_variant` (#42493e) for secondary body text to reduce visual noise and maintain the "airy" aesthetic.

---

## 4. Elevation & Depth
We eschew traditional "drop shadows" in favor of **Tonal Layering**.

*   **The Layering Principle:** Depth is "found," not "added." By placing a `surface-container-lowest` card on a `surface-container-low` background, you create a natural lift that feels sophisticated and integrated.
*   **Ambient Shadows:** If a floating element (like a modal or a floating FAB) requires a shadow, use a diffuse, low-opacity shadow. 
    *   *Formula:* `0px 20px 40px rgba(16, 27, 48, 0.06)`. The shadow color is derived from `on_surface`, not pure black.
*   **The "Ghost Border":** If accessibility requires a stroke (e.g., in high-contrast modes), use the `outline_variant` (#c2c9bb) at 20% opacity. Never use 100% opaque lines.

---

## 5. Components

### Buttons
*   **Primary:** High-pill shape (`rounded-full`). Gradient of `primary` to `primary_container`. Text in `on_primary`. 
*   **Secondary:** `surface_container_lowest` with a "Ghost Border." Text in `primary`.
*   **Tertiary:** No background. Text in `primary` with a subtle underline on hover.

### Cards & Lists
*   **Zero-Divider Policy:** Never use horizontal lines to separate list items. Use 24px–32px of vertical whitespace or alternating `surface_container_low` backgrounds.
*   **Cards:** Use `rounded-xl` (1.5rem) or `rounded-lg` (1rem). Ensure images inside cards take up 100% of the top width to emphasize the "fresh" photography.

### Inputs & Selection
*   **Text Fields:** `surface_container_lowest` background. No border, only a subtle `outline_variant` at 20%. On focus, transition the background to `white` and add a 2px `primary` bottom-border only.
*   **Chips:** Use `secondary_container` for "Freshness" tags or product categories. Always use `rounded-full`.

### Specialty Component: The "Provenance Tile"
A bespoke component for this design system showing the origin of the dairy. A large `surface_container_low` tile with an overlapping `surface` card containing the farm's coordinates and a high-resolution "hero" image of the cattle.

---

## 6. Do's and Don'ts

### Do:
*   **Use Overlays:** Let text elements overlap image containers by 10-20% to create an editorial, high-fashion layout.
*   **Embrace "Milk" Whitespace:** Leave significantly more room around headlines than you think you need.
*   **Soft Corners:** Stick to `xl` (1.5rem) for main containers and `full` (9999px) for interactive elements.

### Don't:
*   **Don't use 1px lines:** This is the quickest way to make the design look like a generic template.
*   **Don't use harsh shadows:** Avoid any shadow that is visible as a "dark smudge." It should feel like ambient light.
*   **Don't crowd the imagery:** The photography is as important as the text. Let the cows breathe.
*   **Don't use generic icons:** If using iconography, use ultra-thin (2pt) stroke weights to match the Manrope font weight.

---

## 7. Token Reference Summary
*   **Primary Brand:** `primary` (#154212)
*   **Main Text:** `on_surface` (#101b30)
*   **Main Surface:** `surface` (#f9f9ff)
*   **Radius:** `xl` (1.5rem) for containers; `full` for buttons.
*   **Typography:** Manrope (Headings), Plus Jakarta Sans (Body).