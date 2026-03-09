# Design System: The Arben Group (Elevated)

**Strategy:** Professional Consulting & Leadership
**Keywords:** Trust, Resilience, Human, Structure
**Base Style:** "Warm Professional" (Unique blend of Corporate Structure + Human Warmth)

---

## 1. Color Palette (Refined)

We are keeping the core identity but adding depth for "Pro Max" quality.

| Token | Hex | Var | Usage |
|-------|-----|-----|-------|
| **Core Brand** | | | |
| Primary Blue | `#404B69` | `--arben-blue` | Foundation, Headers, Primary Buttons |
| Primary Dark | `#2A3245` | `--arben-blue-dark` | **[NEW]** Hover states, High-contrast text |
| Keystone Gold | `#F0BE46` | `--arben-gold` | Accents, Active States, "Spark" elements |
| **Neutrals** | | | |
| Parchment | `#F2EDE7` | `--parchment` | Main Background (Warmth) |
| Surface White | `#FFFFFF` | `--surface-white` | Cards, Modal backgrounds |
| Deep Basalt | `#1E2532` | `--deep-basalt` | **[NEW]** Main Body Text (Higher contrast than Ironwork) |
| Stone Gray | `#6E747F` | `--stone-gray` | Secondary Text, Muted Labels |
| **Feedback** | | | |
| Success | `#2E7D32` | `--success` | Form success |
| Error | `#D32F2F` | `--error` | Form errors |

### 🎨 Logic shift:
- **Darker Text:** Moving main text from `#27303C` to `#1E2532` (or ensuring high contrast) to pop against `--parchment`.
- **White Surface:** Creating meaningful depth by floating White cards on Parchment background.

---

## 2. Typography & Scale

**Fonts:**
- **Display:** `Montserrat Alternates` (Weight 700) — *Use sparingly for "Human" moments*
- **Headings:** `Montserrat` (Weight 700/600) — *Structure and clarity*
- **Body:** `Montserrat` (Weight 400/500) — *Clean readability*
- **Quotes:** `Merriweather` (Italic) — *Voice of authority*

**Scale (Responsive):**
| Level | Desktop | Mobile | Weight | Tracking |
|-------|---------|--------|--------|----------|
| Display (H1) | `3.5rem` | `2.5rem` | 700 | `-0.02em` |
| H2 | `2.75rem` | `2rem` | 700 | `-0.01em` |
| H3 | `1.75rem` | `1.5rem` | 600 | `normal` |
| Body Lg | `1.125rem`| `1rem` | 400 | `normal` |
| Body | `1rem` | `1rem` | 400 | `normal` |
| Caption | `0.875rem`| `0.875rem`| 500 | `0.02em` |

---

## 3. "Pro Max" Component Upgrades

### ✨ Glassmorphism 2.0 (The "Premium" Glass)
Instead of simple transparency, we use a multi-layered approach for depth.
- **Background:** `rgba(255, 255, 255, 0.7)` -> `rgba(255, 255, 255, 0.65)`
- **Blur:** `backdrop-filter: blur(16px)` (Increased from 12px)
- **Border:** `1px solid rgba(255, 255, 255, 0.6)` (Crisp edge)
- **Shadow:** `0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -1px rgba(0, 0, 0, 0.03)` (Softer, multi-layer)

### 🔘 Buttons (Interactive)
- **Primary:** Gradient subtle overlay or solid Blue with "Inner Glow" border at top.
- **Hover:** No layout shift. Transform `translateY(-2px)` + Shadow increase.
- **Active:** `scale(0.98)` for tactile feel.

### 🃏 Cards (Service/Challenge)
- **State:** Default = Flat/Subtle. Hover = Lift + Glow.
- **Content:** Icons should be consistent (SVG/Font).
- **Layout:** Enforce equal height with Flexbox/Grid.

---

## 4. UX & Motion Guidelines

### ✅ Critical Rules
1. **Cursor Pointer:** MUST be on all interactive elements (Cards, Buttons).
2. **Hit Area:** All touch targets min `44px`.
3. **Contrast:** Text on Parchment must meet WCAG AA (4.5:1).
4. **Motion:**
   - **Entrance:** Staggered Fade-Up (20px distance, 0.6s duration).
   - **Hover:** Fast-out, Slow-in (300ms).
   - **Reduced Motion:** Respect `prefers-reduced-motion` media query.

### 🚫 Anti-Patterns to Remove
- **Layout Shifting:** Buttons growing on hover that push other content.
- **Over-animation:** Elements flying in from too far away (`100px+`).
- **Invisible Scroll:** Ensure custom scrollbars (if used) are visible.
- **Text-on-Busy-Background:** Ensure text has solid contrasting backdrop.
