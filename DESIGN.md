# Design System: Envíos DosRuedas (Mar del Plata)
**Project ID:** `enviosdosruedas-mdp`

---

## 1. Visual Theme & Atmosphere

**Envíos DosRuedas** presents a high-energy, ultra-reliable express urban logistics aesthetic tailored specifically for the city of Mar del Plata. The design language fuses high-visibility safety aesthetics (inspired by courier uniforms and traffic agility) with crisp, modern SaaS ergonomics.

* **Atmosphere:** Dynamic, trustworthy, high-contrast, agile, and fast-paced.
* **Tone:** Professional yet approachable, designed to build instant trust with e-commerce merchants, local entrepreneurs, businesses, and individual senders.
* **Density:** Balanced SaaS Density (Level 5/10) with bold typographic hierarchy, high-contrast pill badges, clean geometric card containers, soft ambient blue lighting, and tactile interaction feedback.
* **Core Value Proposition:** Express 3-hour deliveries, Mercado Envíos Flex integration, and budget-friendly LowCost options across all Mar del Plata neighborhoods.
* **Strict Color & Text Mapping Rules:**
  1. **Límite de Azul:** No se utilizan tonos azules más oscuros que **Electric Hyper Blue** (`#0950f6` / `--color-brand-blue-500`).
  2. **CERO TEXTOS OSCUROS:** Está 100% prohibido el uso de textos negros (`#000000`), gris, slate (`#0f172a`) o charcoal (`#020617`).
  3. **MATRIZ ESTRICTA DE FONDO A TEXTO:**
     * **Si el Fondo es AMARILLO (`#ffec01`):** El color del texto es **AZUL** (`#0950f6`).
     * **Si el Fondo es AZUL (`#0950f6`):** El color del texto es **BLANCO** (`#ffffff`) [Acentos/Highlights en **AMARILLO** `#ffec01`].
     * **Si el Fondo es BLANCO (`#ffffff`):** El color del texto es **AZUL** (`#0950f6`).
  4. **USO DE EFECTOS AMARILLOS:** El color amarillo (`#ffec01`) se reserva para efectos visuales, botones CTA primarios, badges de atención, resaltados de títulos en fondos azules y anillos de foco.

---

## 2. Color Palette & Roles

The system is built on a tri-color foundation: **Electric Hyper Blue** (`#0950f6`), **High-Vis Action Yellow** (`#ffec01`), and **Pure Snow White** (`#ffffff`).

| Token | Nombre Descriptivo | Color Hex | Rol Funcional |
| :--- | :--- | :--- | :--- |
| `color-brand-blue-500` | **Electric Hyper Blue** | `#0950f6` | Color primario de marca, héroes, enlaces Y texto principal en superficies blancas/amarillas (AZUL MÁXIMO). |
| `color-brand-blue-400` | **Vibrant Mid Blue** | `#3570f8` | Hover state para botones secundarios, bordes activos. |
| `color-brand-blue-300` | **Bright Sky Accent** | `#628ff9` | Relleno de iconos secundarios, etiquetas activas. |
| `color-brand-blue-100` | **Soft Ice Blue** | `#bacefd` | Bordes de tarjetas, anillos de foco, tintes de fondo. |
| `color-brand-blue-50` | **Mist Blue Tint** | `#e6eefe` | Fondos de superficie claros y alternancias de sección. |
| `color-brand-yellow-500`| **High-Vis Action Yellow**| `#ffec01` | Botones CTA, badges de atención, efectos visuales Y texto destacado en fondos azules. |
| `color-brand-yellow-400`| **Vibrant Yellow Hover**| `#fff12e` | Estado hover de botones amarillos. |
| `color-brand-yellow-300`| **Sunlight Accent** | `#fff45c` | Badges amarillos secundarios, luces de foco. |
| `color-red-600` | **Express Alert Red** | `#dc2626` | Etiquetas de emergencia, alertas de recargo por lluvia. |
| `color-green-500` | **Live Status Green** | `#22c55e` | Indicadores de servicio activo en vivo. |
| `color-white` | **Pure Snow White** | `#ffffff` | Superficies de tarjetas claras Y color de texto principal en fondos azules. |

---

## 3. Matriz Estricta de Mapeo de Texto según el Fondo

| Superficie / Fondo | Color de Texto | Ejemplos de Aplicación |
| :--- | :--- | :--- |
| **Fondo Blanco / Claro** (`#ffffff`, `#e6eefe`) | **Azul Eléctrico** (`#0950f6`) | Títulos, párrafos, labels, tarjetas `.card-feature`, navegaciones claras. |
| **Fondo Azul** (`#0950f6`) | **Blanco** (`#ffffff`) | Texto principal de héroes, contenedores `.card-dark`, footers azules. |
| **Fondo Azul (Acentos / Efectos)** | **Amarillo** (`#ffec01`) | Palabras clave destacadas, cifras KPI, etiquetas de estado SLA (`⚡ 3 HS`). |
| **Fondo Amarillo** (`#ffec01`) | **Azul Eléctrico** (`#0950f6`) | Texto dentro de botones CTA `.btn-primary-yellow`, badges `.pill-badge-yellow`. |

---

## 4. Component Stylings & Specifications

### 4.1 Buttons & Action Controls
* **Primary High-Vis CTA Button (`.btn-primary-yellow`):**
  * *Fondo:* High-Vis Action Yellow (`#ffec01`).
  * *Texto:* **Electric Hyper Blue** (`#0950f6`), font-weight `700`.
  * *Forma:* Full Pill (`rounded-full`, radius `9999px`).
  * *Sombra:* `0 10px 25px -5px rgba(255, 236, 1, 0.4)`.
  * *Hover:* Fondo `#fff12e`, texto `#0950f6`, elevación (`transform: translateY(-2px)`).
* **Secondary Brand Blue Button (`.btn-secondary-blue`):**
  * *Fondo:* Electric Hyper Blue (`#0950f6`).
  * *Texto:* **Pure White** (`#ffffff`), font-weight `600`.
  * *Forma:* Full Pill (`rounded-full`, `9999px`).
  * *Hover:* Fondo Vibrant Mid Blue (`#3570f8`), texto `#ffffff`.
* **Ghost / Outline Button (`.btn-outline-ghost`):**
  * *Borde:* `2px solid #bacefd`.
  * *Texto:* **Electric Hyper Blue** (`#0950f6`).
  * *Hover:* Fondo `#e6eefe`, texto `#0950f6`.
* **Direct WhatsApp Instant Pill Button (`.whatsapp-pill`):**
  * *Fondo:* `#25D366` (WhatsApp Green) con texto **Blanco** (`#ffffff`) `"Hablar por WhatsApp 💬"`.

### 4.2 Cards & Containers
* **Standard Feature Card (`.card-feature`):**
  * *Fondo:* Pure White (`#ffffff`), Borde `1px solid #e6eefe`.
  * *Texto:* **Electric Hyper Blue** (`#0950f6`).
  * *Radius:* `16px` (`rounded-xl`), Sombra `0 4px 12px rgba(9, 80, 246, 0.04)`.
* **Blue Container (`.card-dark`):**
  * *Fondo:* Electric Hyper Blue (`#0950f6`), Borde `1px solid #3570f8`.
  * *Texto Principal:* **Pure White** (`#ffffff`).
  * *Texto Destacado / Efectos:* **High-Vis Action Yellow** (`#ffec01`).

---

## 5. Mapeo Arquitectónico de las 14 Páginas de `paginas_separadas`

Análisis completo de estructura, patrones de diseño y módulos contenidos en `paginas_separadas/`:

1. **`paginas_separadas/home/` (Landing Principal):**
   * Héroe animado con fondo azul (`#0950f6`), texto blanco, calculadora preview, segmentos de clientes, overview de servicios y opiniones.
2. **`paginas_separadas/cotizar/` (Calculadora/Cotizador MDP):**
   * Formulario interactivo por barrios de Mar del Plata, cálculo por peso, selector de tipo de servicio y desglose de tarifas.
3. **`paginas_separadas/contacto/` (Contacto Directo):**
   * Formulario de consulta, datos de atención comercial, canal WhatsApp prioritario y mapa de oficina céntrica.
4. **`paginas_separadas/enviosexpress/` (Mensajería Ultra Rápida <3h):**
   * Servicio prioritario puerta a puerta, seguimiento GPS en tiempo real y asignación inmediata de cadete.
5. **`paginas_separadas/envioslowcost/` (Mensajería Económica 24/48h):**
   * Logística de lotes programados para comercios con costos reducidos.
6. **`paginas_separadas/enviosemprendedores/` (Planes E-Commerce):**
   * Tarifas con descuento por volumen mensual, retiro sin cargo e integración directa de envíos.
7. **`paginas_separadas/enviosflex/` (Mercado Envíos Flex MDP):**
   * Servicio homologado para vendedores Flex con entregas aseguradas en el día.
8. **`paginas_separadas/enviosfullfilment/` (Almacenamiento y Depósito):**
   * Servicio de depósito céntrico en Mar del Plata, control de stock, empaquetado y despacho en moto.
9. **`paginas_separadas/servicios_contrarrembolso/` (Gestión de Cobro en Destino):**
   * Cobro de productos en efectivo al momento de la entrega con rendición y transferencia bancaria segura.
10. **`paginas_separadas/faq/` (Preguntas Frecuentes):**
    * Acordeones interactivos categorizados (Zonas, Tiempos, Medios de Pago, Flex, Reclamos).
11. **`paginas_separadas/nosotros/` (Nuestra Empresa):**
    * Historia de la empresa en Mar del Plata, misión, visión, valores y flota de cadetes.
12. **`paginas_separadas/redes/` (Hub de Redes Sociales):**
    * Canal de WhatsApp directo, feeds de Instagram/TikTok y publicaciones recientes de entregas.
13. **`paginas_separadas/politica_privacidad/` (Protección de Datos):**
    * Términos de confidencialidad, uso de datos de geolocalización y cookies.
14. **`paginas_separadas/terminos_condiciones/` (Cláusulas del Servicio):**
    * Marco legal, seguros de encomienda, límites de peso/volumen y política de reembolsos.

---

## 6. Layout Principles & Responsive Architecture

* **Grid System:** 12-column responsive CSS Grid con ancho máximo de contenedor `1280px` (`max-w-7xl mx-auto px-4 sm:px-6 lg:px-8`).
* **Section Whitespace:** Padding vertical holgado (`clamp(3rem, 8vw, 6rem)`) para separar secciones con claridad.
* **Mobile-First Collapse (< 768px):** Grillas colapsan a 1 sola columna. Objetivos táctiles mínimo `44px`.

---

## 7. Motion & Interaction

* **Spring Physics Default:** `stiffness: 100, damping: 20` para respuestas interactivas.
* **Efectos Amarillos en Hover:** Elevación táctil (`translateY(-4px)`), resplandor difuso amarillo (`0 14px 28px rgba(255,236,1,0.5)`).

---

## 8. Anti-Patterns (Banned AI Tells)

* **PROHIBIDO:** Textos oscuros (negro `#000000`, slate `#0f172a`, charcoal `#020617`, gris `#64748b` en texto están 100% prohibidos). El texto debe ser exclusivamente Azul, Amarillo o Blanco según el fondo.
* **PROHIBIDO:** Tonos azules más oscuros que `#0950f6`. Azul marino (`#041f63`, `#083aa3`) estrictamente prohibido.
* **PROHIBIDO:** Emojis en componentes de UI estructurales.
* **PROHIBIDO:** Fuente `Inter` en UI principal.
* **PROHIBIDO:** Fuentes serif genéricas (`Times New Roman`, `Georgia`, `Garamond`).
* **PROHIBIDO:** Gradientes de neón morados o efectos de brillo artificiales.
* **PROHIBIDO:** Estadísticas de sistema inventadas.

---

## 9. Design System Notes for Stitch Generation (REQUIRED)

> **Copy and paste this exact block into `.stitch/next-prompt.md` for all Stitch generation tasks.**

```markdown
**DESIGN SYSTEM (ENVIOS DOSRUEDAS - MAR DEL PLATA):**
- **Vibe:** High-energy, ultra-reliable express delivery & urban logistics in Mar del Plata with high-contrast tri-color ergonomics.
- **Color Ceiling Constraint:** NO BLUE SHADES DARKER THAN Electric Hyper Blue (#0950f6).
- **TEXT COLOR MATRIX (ZERO DARK TEXTS):**
  * If Background is YELLOW (#ffec01): Text is strictly BLUE (#0950f6).
  * If Background is BLUE (#0950f6): Text is strictly WHITE (#ffffff), with highlights/accents in YELLOW (#ffec01).
  * If Background is WHITE (#ffffff): Text is strictly BLUE (#0950f6).
- **Yellow Effects:** Yellow (#ffec01) is strictly contained for visual effects, primary CTA buttons, attention badges, title highlights on blue backgrounds, and focus rings.
- **Colors:** Electric Hyper Blue (#0950f6), Vibrant Mid Blue (#3570f8), Soft Ice Blue (#bacefd), Mist Blue Tint (#e6eefe), High-Vis Action Yellow (#ffec01), Pure White (#ffffff).
- **Typography:** Display headlines in "Anton" / "Anton SC", section kickers/subheadings in "Bebas Neue" (uppercase tracking-widest), body text in "Outfit" (sans-serif), SLA time slots & tracking codes in "Geist Mono" (monospace).
- **Geometry & Cards:** Rounded-xl (16px) white card containers with 1px soft blue border (#e6eefe), pill-shaped (9999px) action buttons and status tags. Blue cards use Electric Blue (#0950f6) with white text.
- **Elevation & Motion:** Diffused glowing yellow/blue hover shadows, smooth hover translate transitions (-4px).
- **Key UI Elements:** Live SLA time-slot pills ("⚡ 3 HS EXPRESS", "📦 FLEX 24H", "💰 LOWCOST"), high-visibility yellow CTA buttons with Electric Blue text (#0950f6), interactive rate calculators with Mar del Plata neighborhood selectors, live pulsing status dots ("🟢 Servicio Express Activo"), and direct WhatsApp chat links.
```
