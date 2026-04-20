# Design System Specification: The Clinical Atelier

## 1. Overview & Creative North Star: "The Digital Artisan"
The design system for KATHLEEN transcends the typical medical interface. Our Creative North Star is **"The Digital Artisan"**—a philosophy that fuses the clinical precision of AI technology with the bespoke, high-touch elegance of aesthetic dentistry.

To move beyond the "template" look, this system rejects rigid, boxed-in grids. Instead, we utilize **intentional asymmetry**, editorial-style overlapping elements, and high-contrast typographic scales. The goal is to make the user feel they are entering a private gallery of dental excellence rather than a clinical database. We prioritize "breathing room" (generous whitespace) to signify luxury and calm.

---

## 2. Color Strategy: Depth Through Tonality
Our palette reflects the "Diamond Nano" technology at the heart of the brand: light-refracting, pure, and authoritative.

### Palette Roles
*   **Primary (#005cae):** Used for core brand expression and high-priority actions.
*   **Secondary (#0056c5):** Provides depth and tonal variation in navigation and interactive states.
*   **Tertiary/Accent (#735c00 / #D4AF37):** Reserved for "The Gold Standard"—premium services, Diamond Nano callouts, and expert endorsements.
*   **Surface/Background (#f8f9ff):** A cool, airy canvas that feels sterile yet welcoming.

### The "No-Line" Rule
**Explicit Instruction:** Prohibit the use of 1px solid borders for sectioning content. Boundaries must be defined through:
1.  **Background Shifts:** Transitioning from `surface` (#f8f9ff) to `surface-container-low` (#eef4ff).
2.  **Tonal Transitions:** Using soft gradients to define the edge of a container.

### Glass & Gradient Rule
To evoke the high-tech AI aspect, use **Glassmorphism** for floating elements (e.g., appointment cards or tech specs). Use a semi-transparent `surface_container_lowest` (#ffffff) with a 20px-40px backdrop-blur. 
**Signature Texture:** Apply the **Warm Gold Gradient** (#F3D76B to #C99A1A) exclusively to Tertiary CTAs and "Diamond Nano" badges to provide a metallic, light-catching quality.

---

## 3. Typography: The Editorial Balance
The typography system is a dialogue between heritage luxury and futuristic precision.

*   **The Authority (Playfair Display / Noto Serif):** Used for `display` and `headline` roles. This Serif font conveys the "International Standard" and the artistry of aesthetic dentistry. It should be tracked slightly tighter (-1% to -2%) in large headings for a premium, editorial feel.
*   **The Precision (Be Vietnam Pro):** Used for `title`, `body`, and `label` roles. This clean Sans-Serif represents the "High-tech / AI" component. It provides maximum legibility for clinical information and technical details.

**Typographic Hierarchy:**
*   **Display-lg (3.5rem):** Use for hero statements with high-impact imagery.
*   **Headline-md (1.75rem):** Use for section titles, always in Serif.
*   **Body-lg (1rem):** Default for service descriptions, ensuring a line-height of at least 1.6 for readability.

---

## 4. Elevation & Depth: Tonal Layering
We do not use shadows to create "pop"; we use layering to create "presence."

*   **The Layering Principle:** Depth is achieved by "stacking" surface tiers. Place a `surface-container-lowest` card (Pure White) on top of a `surface-container-low` (Light Blue) background to create a soft, natural lift.
*   **Ambient Shadows:** For floating elements (Modals, Hover states), use extra-diffused shadows.
    *   *Token:* `0px 12px 32px rgba(17, 28, 41, 0.06)`. 
    *   The shadow is tinted with the `on-surface` color to mimic natural light refraction through glass.
*   **The "Ghost Border" Fallback:** If a container requires definition on a white background, use the `outline-variant` token at **15% opacity**. Never use 100% opaque borders.

---

## 5. Component Guidelines

### Buttons: The Interactive Jewel
*   **Primary:** Features a subtle vertical gradient of `primary` to `primary_container`. 
    *   *Shape:* `md` (0.75rem) or `full` (pill) for high-tech feel.
*   **Tertiary (Gold):** Reserved for "Book Appointment." Uses the signature Warm Gold Gradient with `on_tertiary` (White) text.
*   **Secondary:** Ghost style. No background, `primary` text, and a "Ghost Border" that appears only on hover.

### Cards & Lists: The Gallery Layout
*   **Constraint:** Forbid divider lines. Use `surface_container` color blocking or 32px-48px of vertical whitespace to separate list items.
*   **Treatment Cards:** Use `xl` (1.5rem) corner radius. Imagery should bleed to the top edge, with text nestled in a `surface_container_lowest` base.

### Input Fields: Minimalist Tech
*   **Style:** Underline-only or very soft-filled `surface_container_high`. 
*   **State:** On focus, the label transitions to a smaller `label-md` in `primary` blue, and the underline expands from the center.

### Specialized Component: The "AI Analysis Overlay"
For showcasing "Diamond Nano" porcelain or AI results:
*   Use a `surface_bright` container with 60% opacity and a `backdrop-filter: blur(12px)`.
*   Incorporate thin (0.5pt) gold lines for data callouts to maintain the "High-tech" aesthetic.

---

## 6. Do’s and Don'ts

### Do:
*   **Do** use asymmetrical layouts (e.g., an image offset to the left with text overlapping it in a white card).
*   **Do** treat the Gold Gradient as a rare "jewelry" accent.
*   **Do** leverage the `surface-container` tokens to create a "nested" look.

### Don't:
*   **Don't** use pure black (#000000). Use `on_surface` (#111c29) for all "black" text to maintain tonal softness.
*   **Don't** use standard "Drop Shadows." If it looks like a default shadow, it’s too heavy.
*   **Don't** use Serif for body text. It slows down the reading of technical information and feels dated rather than "High-tech."
*   **Don't** crowd the interface. If you are unsure, add 16px of extra padding.

---

**Director’s Final Note:** 
Luxury is the absence of noise. Every element in this design system must serve a purpose. If a border or a shadow doesn't provide clarity, remove it. Let the typography and the subtle shifts in blue-white tones tell the story of KATHLEEN’s precision.