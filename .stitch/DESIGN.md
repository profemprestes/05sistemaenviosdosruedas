# Design System: Envíos DosRuedas
**Project ID:** `enviosdosruedas-mdp`

---

## 1. Visual Theme & Atmosphere

**Envíos DosRuedas** presents a **high-energy, ultra-reliable, express urban logistics aesthetic**. The design language combines high-visibility safety colors with ultra-clean modern SaaS ergonomics. 

- **Atmosphere:** Dynamic, trustworthy, agile, high-contrast, and fast-paced.
- **Tone:** Professional yet approachable, designed for both e-commerce merchants and individual senders in Mar del Plata.
- **Visual Weight:** Medium-high density with bold typographic hierarchy, crisp pill badges, and elevated card containers with soft glowing blue depth.

---

## 2. Color Palette & Roles

The system uses a high-contrast palette built around Electric Hyper Blue as the core brand foundation and Vibrant High-Visibility Yellow for high-priority calls to action.

| Token | Color Name | Hex / Value | Functional Role |
| :--- | :--- | :--- | :--- |
| `brand-blue-500` | **Electric Hyper Blue** | `#0950f6` | Primary brand color, hero backdrops, primary links, key brand icons |
| `brand-blue-900` | **Deep Navy Ink** | `#041f63` | Dark mode backgrounds, high-contrast headers, deep card borders |
| `brand-blue-700` | **Royal Navy** | `#083aa3` | Primary text in light mode, hover states on blue buttons |
| `brand-blue-100` | **Soft Ice Blue Tint** | `#bacefd` | Card hover strokes, soft tag backgrounds |
| `brand-blue-50` | **Mist Blue** | `#e6eefe` | Light surface background for feature highlights |
| `brand-yellow-500`| **High-Vis Action Yellow**| `#ffec01` | Primary CTA buttons, urgency badges, highlight tags, active indicators |
| `brand-yellow-300`| **Sunlight Tint** | `#fff45c` | Secondary yellow accents, focus rings |
| `red-600` | **Express Alert Red** | `#dc2626` | Emergency delivery tags, warning alerts, live status badges |
| `surface-white` | **Pure Snow White** | `#ffffff` | Primary light card surface, crisp background |
| `text-dark` | **Slate Ink** | `#0f172a` | High legibility body text |
| `text-muted` | **Cool Steel Grey** | `#64748b` | Secondary descriptions, timestamps, helper labels |

---

## 3. Typography Rules

A strong 3-tier typographic system balancing high-impact display headers with ultra-legible body text.

1. **Display Headings (`--font-display`):** `"Anton SC"`, `"Anton"`, sans-serif.
   - *Usage:* Major hero titles, section headlines, stat numbers. All-caps or bold sentence case. Heavy visual weight (`font-extrabold`).
2. **Subheadings (`--font-subheading`):** `"Bebas Neue"`, sans-serif.
   - *Usage:* Category tags, section super-titles, kicker badges, pricing plan names. Uppercase with tracking wide (`tracking-widest`).
3. **Primary Body (`--font-sans`):** `"Outfit"`, `"IBM Plex Sans"`, sans-serif.
   - *Usage:* Main paragraphs, card body text, navigation items, form inputs. Clean geometric proportions.
4. **Data & Technical Mono (`--font-mono`):** `"Geist Mono"`, monospace.
   - *Usage:* Tracking numbers, delivery time slots (e.g. `3 HS EXPRESS`), price tags, postal codes.

---

## 4. Component Stylings & Improvement Suggestions per Page

Below is the design spec for current and future components, including concrete visual & functional UX improvements for each page in `paginas_actuales/`.

### 4.1 Global Navigation Header
- **Current Specs:** Fixed top header with logo, navigation links, and contact CTA.
- **Design Tokens:** Background `#ffffff` with subtle bottom border `#e6eefe` or glassmorphism (`backdrop-blur-md bg-white/90`).
- **Improvement Suggestions:**
  - **Live Service Status Indicator:** Add a pulsing green/yellow pill dot in the header showing `"Servicio Express Activo hoy en Mar del Plata"`.
  - **Quick Action CTA:** Replace generic button with a High-Vis Yellow (`#ffec01`) pill CTA reading `"Cotizar Envío ⚡"`.
  - **Mobile Navigation Drawer:** Enhanced full-screen slide-over drawer with direct WhatsApp instant button and single-tap tracking input.

### 4.2 Hero Section (`index.html`)
- **Current Specs:** Electric Blue backdrop with headline, subheader, and dual CTAs.
- **Design Tokens:** Surface `#0950f6`, text `#ffffff`, yellow CTA `#ffec01` with black ink text.
- **Improvement Suggestions:**
  - **Embedded Instant Calculator:** Add a floating white card container right inside the hero with two inputs (Barrio Origen, Barrio Destino) and an instant estimated price button.
  - **Social Proof Strip:** Include real-time social proof pills (e.g. `"⭐ 4.9/5 +1.200 envíos este mes"`).
  - **Dynamic Vehicle Selector:** Interactive toggle tab (`Moto Express` vs `Flete / Miniflete`).

### 4.3 Service Cards (`servicios-express.html`, `servicios-enviosflex.html`, `servicios-lowcost.html`)
- **Current Specs:** 3-column card grid detailing service features and delivery terms.
- **Design Tokens:** White card background `#ffffff`, radius `16px` (`rounded-xl`), stroke `1px solid #e6eefe`, hover shadow `0 24px 64px #0950f626`.
- **Improvement Suggestions:**
  - **Standardized Badge Hierarchy:** Top-right pill badge indicating delivery SLA (e.g. `⚡ Max 3 Hs`, `📦 Mismo Día`, `💰 Económico`).
  - **Interactive Comparison Matrix:** Add a toggle view to compare Express vs Mercado Envíos Flex vs LowCost side-by-side with feature checkmarks.
  - **Direct WhatsApp Deep Links:** Pre-fill WhatsApp messages with specific service names upon clicking CTA (e.g. `"Hola, quiero solicitar el Servicio Express de 3hs..."`).

### 4.4 Contact & Interactive Quote Page (`contacto.html`, `cotizar.html`)
- **Current Specs:** Contact information, address, embedded map, contact form.
- **Design Tokens:** Clean two-column split screen. Left side deep navy `#041f63` with contact metadata; right side crisp white `#ffffff` form card.
- **Improvement Suggestions:**
  - **Multi-Step Guided Form:** Step 1: Package Type (Document, Small Package, Medium Box) -> Step 2: Pickup/Dropoff Zones -> Step 3: Immediate Summary & Price estimate.
  - **Neighborhood Dropdown Selector:** Pre-populate key Mar del Plata zones (Centro, Güemes, Puerto, Constitución, Batan, etc.) for quick selection.
  - **One-Tap WhatsApp Direct Launcher:** Sticky floating bar on mobile for instantaneous chat response.

### 4.5 About Us & Trust Page (`nosotros.html`)
- **Current Specs:** Company trajectory, operational values, logistics capabilities.
- **Design Tokens:** Story section with statistics grid and values icons.
- **Improvement Suggestions:**
  - **Key Performance Indicators (KPI Grid):** Highlight key figures with large display typography (`Anton` 48px in `#0950f6`): `99.4% ENTREGAS A TIEMPO`, `+50K PAQUETES MOVIDOS`, `100% MAR DEL PLATA`.
  - **Coverage Map Graphic:** Interactive or stylized map graphic of Mar del Plata highlighting coverage zones and central hub location.
  - **Driver & Fleet Safety Badges:** Trust badges for insured cargo, real-time GPS tracking, and vetted cadetes.

### 4.6 Global Footer
- **Current Specs:** Multi-column links, legal disclaimers, contact details.
- **Design Tokens:** Deep Navy surface `#041f63`, text `#d6e4fe`, yellow accent links `#ffec01`.
- **Improvement Suggestions:**
  - **Live Operating Hours Badge:** Dynamic status indicator (`"🟢 Abierto ahora (09:00 - 18:00 hs)"` or `"🔴 Cerrado - Escribinos al WhatsApp"`).
  - **Quick Tracking Bar:** Footer embedded tracking input (`"Ingresá tu N° de Guía"`).

---

## 5. Layout Principles & Elevation

- **Grid Strategy:** 12-column flexible grid with max width `1280px` (`max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`).
- **Whitespace:** Generous section padding (`py-16 lg:py-24`) to ensure breathing room between high-impact headlines and cards.
- **Corner Roundness:**
  - Small elements / Badges: `8px` (`rounded-md`).
  - Cards & Input Fields: `16px` (`rounded-xl`).
  - Hero Containers & Modals: `24px` (`rounded-2xl`).
  - Action Buttons & Tags: Full Pill `9999px` (`rounded-full`).
- **Elevation & Shadows:**
  - Card Default: Flat with 1px border `#e6eefe`.
  - Card Hover: `box-shadow: 0 24px 64px rgba(9, 80, 246, 0.15); translate-y: -4px`.
  - Floating CTAs / Modals: `box-shadow: 0 25px 50px -12px rgba(9, 80, 246, 0.25)`.

---

## 6. Design System Notes for Stitch Generation (REQUIRED)

> **Copy and paste this exact block into the `.stitch/next-prompt.md` baton file for all Stitch generations.**

```markdown
**DESIGN SYSTEM (ENVIOS DOSRUEDAS - MAR DEL PLATA):**
- **Vibe:** High-energy, ultra-reliable express delivery service in Mar del Plata with clean SaaS ergonomics.
- **Colors:** Primary Electric Blue (#0950f6), Deep Navy (#041f63), Soft Ice Blue (#e6eefe), High-Vis Action Yellow (#ffec01), Pure White (#ffffff), Text Dark Slate (#0f172a).
- **Typography:** Display titles in "Anton" / "Anton SC", sub-headings/kicker tags in "Bebas Neue", body text in "Outfit" or sans-serif, data/time slots/tracking numbers in "Geist Mono" monospace.
- **Geometry & Cards:** Rounded-xl (16px) white card containers with 1px soft blue border (#e6eefe), pill-shaped (9999px) action buttons and status tags.
- **Elevation & Motion:** Diffused glowing blue hover shadows (0 24px 64px rgba(9,80,246,0.15)), smooth transitions.
- **Key UI Elements:** Live SLA time-slot pills (e.g., "⚡ 3 HS EXPRESS"), high-visibility yellow CTA buttons with black text, interactive rate calculators, status dot indicators, and direct WhatsApp links.
```
