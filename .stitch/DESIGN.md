# Design System: Envíos DosRuedas (Mar del Plata)
**Project ID:** `enviosdosruedas-mdp`

---

## 1. Visual Theme & Atmosphere

**Envíos DosRuedas** presents a high-energy, ultra-reliable, express urban logistics aesthetic tailored specifically for the city of Mar del Plata. The design language fuses high-visibility safety aesthetics (inspired by courier uniforms and traffic agility) with crisp, modern SaaS ergonomics.

* **Atmosphere:** Dynamic, trustworthy, high-contrast, agile, and fast-paced.
* **Tone:** Professional yet approachable, designed to build instant trust with e-commerce merchants, local entrepreneurs, businesses, and individual senders.
* **Visual Weight & Density:** Balanced density with bold typographic hierarchy, high-contrast pill badges, clean geometric card containers, soft ambient blue lighting, and interactive feedback indicators.
* **Core Value Proposition:** Express 3-hour deliveries, Mercado Envíos Flex integration, and budget-friendly LowCost options across all Mar del Plata neighborhoods.

---

## 2. Color Palette & Roles

The system is built on a dual foundation: **Electric Hyper Blue** for brand stability and structure, balanced by **High-Vis Action Yellow** for maximum conversion urgency on calls to action.

| Token | Descriptive Color Name | Hex Code | Functional Role |
| :--- | :--- | :--- | :--- |
| `color-brand-blue-500` | **Electric Hyper Blue** | `#0950f6` | Primary brand color, hero backdrops, primary links, key icons, active navigation indicators |
| `color-brand-blue-900` | **Deep Navy Ink** | `#041f63` | Dark surface backgrounds, high-contrast headers, dark footers, primary heading text |
| `color-brand-blue-700` | **Royal Navy** | `#083aa3` | Primary body text in light mode, hover state for blue buttons |
| `color-brand-blue-600` | **Steel Blue Muted** | `#2563eb` | Secondary text links, subtle icon fills |
| `color-brand-blue-100` | **Soft Ice Blue** | `#bacefd` | Card borders, subtle focus rings, tag background tints |
| `color-brand-blue-50` | **Mist Blue Tint** | `#e6eefe` | Light surface backdrops, section background alternations |
| `color-brand-yellow-500`| **High-Vis Action Yellow**| `#ffec01` | Primary CTA buttons, attention badges, active status highlights, key conversion triggers |
| `color-brand-yellow-400`| **Vibrant Yellow Hover**| `#facc15` | Hover state for yellow CTA buttons |
| `color-brand-yellow-300`| **Sunlight Accent** | `#fff45c` | Secondary yellow badges, focus outline highlights |
| `color-red-600` | **Express Alert Red** | `#dc2626` | Emergency delivery tags, warning alerts, surge pricing badges (e.g., Lluvia +30%) |
| `color-green-500` | **Live Status Green** | `#22c55e` | Pulsing service online indicators, successful delivery confirmation badges |
| `color-white` | **Pure Snow White** | `#ffffff` | Primary card surfaces, clean content backgrounds |
| `color-slate-900` | **Slate Dark Ink** | `#0f172a` | High-contrast body text on light backgrounds |
| `color-slate-500` | **Cool Steel Grey** | `#64748b` | Secondary descriptions, timestamps, helper text, inactive tab states |

---

## 3. Typography Rules

A distinct 4-tier typographic hierarchy designed for immediate scanning and high visual impact:

1. **Display Headings (`--font-display`):** `"Anton"`, `"Anton SC"`, sans-serif.
   * *Usage:* Hero titles, main section headlines, numerical stat callouts.
   * *Style:* Heavy visual weight, sentence case or uppercase, tight line-height (`leading-tight`).
2. **Subheadings & Section Kickers (`--font-subheading`):** `"Bebas Neue"`, sans-serif.
   * *Usage:* Kicker badges, category labels, service card super-titles, step numbers.
   * *Style:* Uppercase, wide letter-spacing (`tracking-widest` or `0.08em`).
3. **Primary Body Text (`--font-sans`):** `"Outfit"`, ui-sans-serif, system-ui, sans-serif.
   * *Usage:* Paragraphs, feature bullet points, navigation links, form input labels.
   * *Style:* Clean geometric proportions, regular (`font-normal`) and medium (`font-medium`) weights.
4. **Data & Technical Mono (`--font-mono`):** `"Geist Mono"`, ui-monospace, monospace.
   * *Usage:* Tracking numbers, delivery time slots (`⚡ 3 HS EXPRESS`), price tags, zip/zone codes.
   * *Style:* Monospaced clarity for instant numerical comprehension.

---

## 4. Component Stylings & Specifications

### 4.1 Buttons & Action Controls
* **Primary High-Vis CTA Button:**
  * *Background:* High-Vis Action Yellow (`#ffec01`), text Deep Navy Ink (`#041f63`), font-weight `700`.
  * *Shape:* Full Pill (`rounded-full`, radius `9999px`) or rounded rectangle (`rounded-xl`).
  * *Shadow:* `0 10px 25px -5px rgba(255, 236, 1, 0.4)`.
  * *Hover State:* Background `#facc15`, slight vertical lift (`transform: translateY(-2px)`).
* **Secondary Brand Blue Button:**
  * *Background:* Electric Hyper Blue (`#0950f6`), text Pure White (`#ffffff`), font-weight `600`.
  * *Shape:* Pill (`rounded-full`) or `rounded-xl`.
  * *Hover State:* Background Royal Navy (`#083aa3`).
* **Ghost / Outline Button:**
  * *Border:* `2px solid #bacefd`, text Electric Hyper Blue (`#0950f6`).
  * *Hover State:* Background Mist Blue (`#e6eefe`).
* **Direct WhatsApp Instant Pill Button:**
  * *Background:* `#25D366` (WhatsApp Green) or High-Vis Yellow (`#ffec01`) with green WhatsApp icon.
  * *Text:* Bold white or navy ink text reading `"Hablar por WhatsApp 💬"`.

### 4.2 Cards & Containers
* **Standard Feature Card:**
  * *Surface:* Pure White (`#ffffff`).
  * *Border:* `1px solid #e6eefe` (Soft Ice Blue Tint).
  * *Radius:* `16px` (`rounded-xl`).
  * *Default Shadow:* `0 4px 12px rgba(9, 80, 246, 0.04)`.
  * *Hover Effect:* Translate `-4px` vertically, shadow expands to `0 24px 64px rgba(9, 80, 246, 0.15)`.
* **Elevated / Dark Mode Container:**
  * *Surface:* Deep Navy Ink (`#041f63`).
  * *Border:* `1px solid #083aa3`.
  * *Text:* Pure White (`#ffffff`) and Sunlight Yellow (`#fff45c`) accents.
* **Interactive Calculator Card:**
  * *Surface:* Pure White (`#ffffff`) with subtle gradient top border (`linear-gradient(90deg, #0950f6, #ffec01)`).
  * *Radius:* `24px` (`rounded-2xl`).

### 4.3 Form Inputs & Interactive Controls
* **Neighborhood Dropdown Selects & Text Inputs:**
  * *Background:* `#ffffff` or `#f8fafc`.
  * *Border:* `1px solid #cbd5e1`, focus border `2px solid #0950f6`.
  * *Radius:* `12px` (`rounded-lg`).
  * *Typography:* `"Outfit"` 15px, text `#0f172a`.
* **Multi-Step Form Indicators:**
  * Step numbers in pill badges (`1`, `2`, `3`) with active step highlighted in Electric Blue (`#0950f6`) and completed steps with green checkmarks.

### 4.4 Status Badges & SLA Indicators
* **Live Service Status Indicator:**
  * Pulsing dot (`#22c55e` Green) next to `"Servicio Activo hoy en Mar del Plata"`.
* **SLA Time Slot Badges:**
  * `⚡ 3 HS EXPRESS` -> Red/Yellow pill badge.
  * `📦 FLEX 24H` -> Electric Blue pill badge.
  * `💰 LOWCOST` -> Green/Navy pill badge.

---

## 5. Architectural Breakdown of Site Sections (`paginas_separadas`)

Analysis of structure, layout patterns, and design details across all separated page modules:

### 5.1 Home Module (`paginas_separadas/home/`)
* **Hero Animado (`section-1-hero-animado.html`):** High-impact Electric Blue backdrop (`#0950f6`) with display title in Anton, pulsing live status pill, animated courier graphic/badge, dual CTA buttons (Instant Quote + WhatsApp), and rate calculator preview.
* **Segmentos Target (`section-2-segmentos-home.html`):** 3-column card grid segmenting users: E-commerce / Emprendedores, Empresas & Oficinas, Particulares.
* **Servicios Overview (`section-3-servicios-overview.html`):** Service comparison cards highlighting Express 3h, Mercado Envíos Flex, and LowCost 24h with SLA badges.
* **Emprendedores Hub (`section-4-emprendedores-home.html`):** Focused value proposition for online stores in Mar del Plata (API integration, WhatsApp automated dispatches, volume discounts).
* **Social Proof & Metrics (`section-5-social-proof.html`):** KPI stats counter (`99.4% Entregas a tiempo`, `+50,000 Paquetes`, `100% Mar del Plata`), client testimonials, partner badges.
* **CTA Banner (`section-6-cta-section.html`):** High-conversion full-width navy container with instant WhatsApp button.
* **Social Media Carousel (`section-7-carrusel-redes.html`):** Infinite logo/photo slider showcasing real deliveries across Mar del Plata.

### 5.2 Cotizar Module (`paginas_separadas/cotizar/`)
* **Cotizar Hero (`section-1-cotizar-hero.html`):** Headline explaining transparent instant pricing per zone.
* **Cotizar Pasos (`section-2-cotizar-pasos.html`):** Visual 3-step timeline (Origen/Destino -> Select Package -> Get Quote).
* **Cotizador Form (`section-3-cotizador-form.html`):** Interactive form with pre-populated Mar del Plata neighborhood dropdowns (Centro, Güemes, Puerto, Constitución, Batán, Sierra, etc.), package weight toggles, and instant price summary box.
* **Tarifas Base (`section-4-cotizar-tarifas.html`):** Structured price breakdown matrix by distance and urgency tier.
* **Recargos Policy (`section-5-cotizar-recargos.html`):** Transparent badge cards for rain surcharge (+30%), extra waiting time, and heavy bulto policy.
* **Mapa de Cobertura (`section-6-cotizar-cobertura.html`):** Neighborhood coverage zone breakdown for Mar del Plata.

### 5.3 Express Module (`paginas_separadas/enviosexpress/`)
* **Express Hero & Features (`section-1` to `section-4`):** High-speed delivery focus (max 3 hours), door-to-door GPS tracking, dedicated moto cadete assignment. Highlighting emergency keys, urgent documents, and flash retail orders.

### 5.4 LowCost Module (`paginas_separadas/envioslowcost/`)
* **LowCost Hero & Scheduled Batches (`section-1` to `section-5`):** Economical 24h delivery for scheduled batch orders. Clear pricing tables and batch pickup time windows.

### 5.5 Contacto Module (`paginas_separadas/contacto/`)
* **Contact Hero & Direct Channels (`section-1` to `section-3`):** Split-screen layout. Left side: Deep Navy card with WhatsApp, phone, email, and Mar del Plata office location. Right side: Interactive inquiry form and embedded map.

### 5.6 Nosotros Module (`paginas_separadas/nosotros/`)
* **About Story & Values (`section-1` to `section-7`):** Company trajectory from local couriers to full logistics ecosystem in Mar del Plata. Values grid, team showcase, mission, and fleet reliability badges.

### 5.7 Redes Module (`paginas_separadas/redes/`)
* **Social Ecosystem (`section-1` to `section-4`):** Direct links to official Instagram (@enviosdosruedas_mdp), Facebook, TikTok, WhatsApp, and live feed of recent community posts.

---

## 6. Layout Principles, Grid & Elevation

* **Grid System:** 12-column responsive grid with max container width `1280px` (`max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`).
* **Section Whitespace:** Generous vertical padding (`py-16 lg:py-24`) to give breathing room between bold titles and dense cards.
* **Corner Radii Hierarchy:**
  * Small elements / Badges: `8px` (`rounded-md`).
  * Form inputs / Secondary cards: `12px` (`rounded-lg`).
  * Primary Feature Cards: `16px` (`rounded-xl`).
  * Hero Containers & Modals: `24px` (`rounded-2xl`).
  * Action Buttons & Status Pills: Full Pill `9999px` (`rounded-full`).
* **Elevation & Layering:**
  * *Base Surface:* Pure White (`#ffffff`) or Mist Blue (`#e6eefe`).
  * *Card Surface:* Pure White (`#ffffff`) with `1px solid #e6eefe`.
  * *Hover Surface:* Y-axis offset (`translate-y-[-4px]`) with soft diffused glowing blue shadow (`0 24px 64px rgba(9,80,246,0.15)`).
  * *Floating Elements:* Header fixed blur backdrop (`backdrop-blur-md bg-white/90`), sticky WhatsApp floating trigger.

---

## 7. Design System Notes for Stitch Generation (REQUIRED)

> **Copy and paste this exact block into `.stitch/next-prompt.md` for all Stitch generation tasks.**

```markdown
**DESIGN SYSTEM (ENVIOS DOSRUEDAS - MAR DEL PLATA):**
- **Vibe:** High-energy, ultra-reliable express delivery & urban logistics in Mar del Plata with modern SaaS ergonomics.
- **Colors:** Electric Hyper Blue (#0950f6), Deep Navy Ink (#041f63), Soft Ice Blue (#bacefd), Mist Blue Tint (#e6eefe), High-Vis Action Yellow (#ffec01), Pure White (#ffffff), Text Slate Ink (#0f172a), Cool Steel Grey (#64748b).
- **Typography:** Display headlines in "Anton" / "Anton SC", section kickers/subheadings in "Bebas Neue" (uppercase tracking-widest), body text in "Outfit" or sans-serif, technical tracking & SLA time slots in "Geist Mono" monospace.
- **Geometry & Cards:** Rounded-xl (16px) white card containers with 1px soft blue border (#e6eefe), pill-shaped (9999px) action buttons and status tags.
- **Elevation & Motion:** Diffused glowing blue hover shadows (0 24px 64px rgba(9,80,246,0.15)), smooth hover translate transitions (-4px).
- **Key UI Elements:** Live SLA time-slot pills (e.g., "⚡ 3 HS EXPRESS", "📦 FLEX 24H", "💰 LOWCOST"), high-visibility yellow CTA buttons with dark navy text, interactive rate calculators with Mar del Plata neighborhood selectors, live pulsing status dots ("🟢 Servicio Express Activo"), and direct WhatsApp chat links.
```
