# ⚡ Envíos DosRuedas (Mar del Plata)

> **ID del Proyecto:** `enviosdosruedas-mdp`  
> **Sistema de Envíos Urbanos Express & Logística E-Commerce para Mar del Plata**

---

## 📋 Tabla de Contenidos
1. [Visión General del Proyecto](#1-visión-general-del-proyecto)
2. [Arquitectura del Sistema de Diseño (Design Tokens & Componentes)](#2-arquitectura-del-sistema-de-diseño)
3. [Mapa del Sistema y Catálogo de `paginas_separadas`](#3-mapa-del-sistema-y-catálogo-de-paginas_separadas)
4. [Guía de Desarrollo y Uso de HTML/CSS](#4-guía-de-desarrollo-y-uso-de-htmlcss)
5. [Estructura Global e Integración con `site/`](#5-estructura-global-e-integración-con-site)
6. [Guía de Mantenimiento y Buenas Prácticas](#6-guía-de-mantenimiento-y-buenas-prácticas)

---

## 1. Visión General del Proyecto

**Envíos DosRuedas** es la plataforma logística y sitio web oficial para el servicio de mensajería y cadetería express en moto líder en la ciudad de **Mar del Plata**. Diseñado específicamente para responder a las exigencias del comercio electrónico moderno, pymes, emprendedores y usuarios particulares.

### 🎯 Propuesta de Valor Principal
* **Envíos Express <3 Horas:** Retiro y entrega prioritaria en todas las zonas de Mar del Plata.
* **Integración Mercado Envíos Flex:** Solución logística homologada para vendedores Flex con entregas en el día.
* **Planes Emprendedores y LowCost:** Tarifas adaptadas al volumen de envíos con descuentos progresivos.
* **Cobro por Contrarrembolso:** Gestión segura de cobro en efectivo al entregar el paquete con posterior transferencia al vendedor.
* **Fulfillment Local:** Almacenamiento, empaquetado y despacho directo desde depósito céntrico.

---

## 2. Arquitectura del Sistema de Diseño

El sistema de diseño fusiona la estética de seguridad vial de alta visibilidad (indumentaria de mensajería urbana) con la ergonomía visual de una aplicación SaaS moderna.

### 🎨 Paleta Cromática y Roles
Centralizada en `paginas_separadas/shared/css/design-tokens.css` y detallada en [`DESIGN.md`](file:///C:/Users/prest/proyectos/05sistemaenviosdosruedas/DESIGN.md).

| Token Variable | Nombre Descriptivo | Color Hex | Rol Funcional |
| :--- | :--- | :--- | :--- |
| `--color-brand-blue-500` | **Electric Hyper Blue** | `#0950f6` | Color primario de marca, héroes, enlaces y estados activos. |
| `--color-brand-blue-900` | **Deep Navy Ink** | `#041f63` | Fondos oscuros, encabezados principales, footers y texto contrastado. |
| `--color-brand-blue-700` | **Royal Navy** | `#083aa3` | Hover en botones azules y bordes de contenedores oscuros. |
| `--color-brand-blue-50` | **Mist Blue Tint** | `#e6eefe` | Fondos secundarios claros y superficies de tarjetas. |
| `--color-brand-yellow-500`| **High-Vis Action Yellow**| `#ffec01` | Botones de conversión principales (CTA), badges de atención. |
| `--color-brand-yellow-400`| **Vibrant Yellow Hover**| `#fff12e` | Estado hover de botones primarios. |
| `--color-red-600` | **Express Alert Red** | `#dc2626` | Alertas de urgencia, recargos por lluvia y avisos críticos. |
| `--color-green-500` | **Live Status Green** | `#22c55e` | Indicadores de servicio activo y confirmaciones de entrega. |
| `--color-slate-900` | **Slate Dark Ink** | `#0f172a` | Texto de cuerpo principal en modo claro. |

---

### 🔤 Jerarquía Tipográfica
El proyecto utiliza 4 familias tipográficas con roles específicos:

1. **Display Headings (`--font-display`):** `"Anton"`, `"Anton SC"`, sans-serif.
   * *Uso:* Títulos de héroes, cifras destacadas y llamados de atención de alto impacto.
2. **Subheadings & Kickers (`--font-subheading`):** `"Bebas Neue"`, sans-serif.
   * *Uso:* Etiquetas superiores, supertítulos de categorías y números de pasos.
3. **Texto Principal (`--font-sans`):** `"Outfit"`, ui-sans-serif, system-ui, sans-serif.
   * *Uso:* Cuerpos de texto, descripciones, párrafos, items de listas y enlaces de navegación.
4. **Datos y Cifras Monospaciadas (`--font-mono`):** `"Geist Mono"`, monospace.
   * *Uso:* Códigos de seguimiento, etiquetas de precios, horarios (`⚡ 3 HS EXPRESS`) y zonas postales.

---

### 🧩 Componentes UI Principales (`design-tokens.css`)

#### Botones CTA
* `.btn-primary-yellow`: Botón primario de conversión con sombra de elevación amarilla y texto azul oscuro.
* `.btn-secondary-blue`: Botón secundario azul eléctrico para acciones secundarias.
* `.btn-outline-ghost`: Botón contorneado transparente para acciones alternativas.
* `.whatsapp-pill`: Botón flotante/directo de WhatsApp verde (`#25D366`) optimizado para conversión instantánea.

#### Badges y Etiquetas
* `.pill-badge-blue` / `.pill-badge-yellow`: Píldoras indicadoras de categoría o estado.
* `.live-badge`: Etiqueta verde traslúcida para estado del servicio en vivo.
* `.alert-badge`: Etiqueta roja para recargos o advertencias (ej. Lluvia / Cadetería Nocturna).

---

## 3. Mapa del Sistema y Catálogo de `paginas_separadas`

El directorio `paginas_separadas/` organiza de manera modular cada sección y página del sitio web. Cada carpeta contiene las partes divididas (`section-1...html`, `section-2...html`, etc.), la página integrada principal (`.html`), sus estilos locales (`styles.css`) y scripts interactivos (`script.js`).

### 📁 Estructura del Catálogo (14 Módulos)

```
paginas_separadas/
├── shared/
│   └── css/
│       └── design-tokens.css      <-- Hoja de Estilos y Tokens Compartida
├── contacto/
│   ├── contacto.html              <-- Página Completa de Contacto
│   ├── section-1-contact-hero.html
│   ├── section-2-contact-form.html
│   ├── section-3-contact-direct.html
│   └── styles.css
├── cotizar/
│   ├── cotizar.html               <-- Calculadora/Cotizador de Tarifas MDP
│   ├── section-1-quote-hero.html
│   ├── section-2-quote-calculator.html
│   ├── section-3-quote-zones.html
│   └── styles.css
├── enviosemprendedores/
│   ├── envios-emprendedores.html  <-- Servicio para Pymes y Emprendedores
│   ├── section-1-hero.html
│   └── ...
├── enviosexpress/
│   ├── envios-express.html        <-- Mensajería Ultra Rápida <3h
│   └── ...
├── enviosflex/
│   ├── envios-flex.html           <-- Integración Mercado Envíos Flex
│   └── ...
├── enviosfullfilment/
│   ├── envios-fullfilment.html    <-- Almacenamiento y Depósito MDP
│   └── ...
├── envioslowcost/
│   ├── envios-low-cost.html       <-- Logística Programada Económica
│   └── ...
├── faq/
│   ├── faq.html                   <-- Preguntas Frecuentes y Respuestas
│   └── ...
├── home/
│   ├── index.html / home.html     <-- Landing Page Principal
│   ├── section-1-hero.html
│   ├── section-2-features.html
│   ├── section-3-calculator-preview.html
│   └── ...
├── nosotros/
│   ├── nosotros.html              <-- Historia, Misión, Visión y Equipo
│   └── ...
├── politica_privacidad/
│   ├── politica-de-privacidad.html
│   └── ...
├── redes/
│   ├── redes.html                 <-- Hub Social y Publicaciones Recientes
│   └── ...
├── servicios_contrarrembolso/
│   ├── servicios-contrareembolso.html
│   └── ...
└── terminos_condiciones/
    ├── terminos-y-condiciones.html
    └── ...
```

---

## 4. Guía de Desarrollo y Uso de HTML/CSS

### 🚀 Cómo Crear o Modificar una Sección

1. **Vincular el CSS Compartido (`design-tokens.css`):**
   Asegúrate de incluir la hoja de estilos global en el `<head>` del HTML antes de los estilos específicos de la página:
   ```html
   <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>Envíos DosRuedas | Título de Sección</title>
     <!-- Design Tokens y Componentes Base -->
     <link rel="stylesheet" href="../shared/css/design-tokens.css">
     <!-- Estilos específicos de la sección -->
     <link rel="stylesheet" href="styles.css">
   </head>
   ```

2. **Utilizar las Variables CSS de Marca:**
   En lugar de escribir valores de color o tipografía en código duro, utiliza los tokens centralizados:
   ```css
   .mi-tarjeta-custom {
     background-color: var(--color-white);
     border: 1px solid var(--color-brand-blue-100);
     border-radius: var(--radius-xl);
     font-family: var(--font-sans);
     color: var(--color-slate-900);
     box-shadow: var(--shadow-md);
   }
   ```

3. **Uso de Clases Utilitarias para Componentes Rápida:**
   * **Botón Principal:** `<a href="#" class="btn-primary-yellow">Cotizar Envío 🚀</a>`
   * **Badge En Vivo:** `<span class="pill-badge live-badge">● Servidores Online MDP</span>`
   * **Texto Display:** `<h1 class="font-display">ENVÍOS EXPRESS EN 3 HORAS</h1>`

---

## 5. Estructura Global e Integración con `site/`

El repositorio cuenta con dos estructuras complementarias:
1. **`paginas_separadas/` (Entorno de Desarrollo Modular):**
   Cada sección está dividida de forma atómica para permitir la edición independiente de componentes, pruebas de UI aisladas y desarrollo iterativo del sistema de diseño.
2. **`site/public/` (Exportación/Build Unificado):**
   Contiene las páginas HTML integradas finales (`index.html`, `cotizar.html`, `contacto.html`, `nosotros.html`, `servicios-express.html`) listas para ser servidas en producción o integradas con frameworks de frontend (React, Vite, Next.js).

---

## 6. Guía de Mantenimiento y Buenas Prácticas

1. **Consistencia Cromática:** No agregar colores Hex aislados dentro de los archivos `styles.css` locales. Registrar cualquier nuevo tono en `paginas_separadas/shared/css/design-tokens.css` bajo la regla `:root`.
2. **Accesibilidad (WCAG 2.2):** Mantener un ratio de contraste adecuado entre texto y fondo. Los botones principales con fondo amarillo (`#ffec01`) deben llevar siempre texto en azul oscuro (`#041f63`) para maximizar la legibilidad.
3. **Carga Optimizada de Fuentes:** Las tipografías de Google Fonts están importadas dentro de `design-tokens.css` con el parámetro `&display=swap` para evitar bloqueos en el renderizado inicial.
4. **Responsividad First:** Todas las secciones deben garantizar un comportamiento adaptativo fluido desde pantallas móviles (`320px`) hasta monitores ultrawide (`1920px+`).

---
*Documentación generada y optimizada para el ecosistema Envíos DosRuedas Mar del Plata.*
