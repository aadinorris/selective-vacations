---
version: 1.0.0
name: Selective-Vacations-Design-System
description: A luxury editorial travel design system for Selective Vacations — a specialist India domestic travel company. The system anchors on a warm ivory canvas (#FAF8F5), deep charcoal typography (#141413), vibrant warm saffron/terracotta (#C86D48) as the primary brand voltage, deep forest green (#1A382B) as an heritage secondary, and warm royal gold (#C59B27) for luxury cues. Typography pairs an elegant editorial serif (Playfair Display / Cormorant Garamond) for display titles with a crisp modern sans (Inter / Plus Jakarta Sans) for navigation and UI, capturing "Heritage + Modernity". Layout emphasizes generous whitespace (80-96px rhythms), large cinematic imagery, floating trip planner bars, and prominent human-trust contact access (Founder Shailendra, WhatsApp, Call).

colors:
  primary: "#C86D48"             # Muted saffron / terracotta — brand voltage, primary CTAs
  primary-hover: "#B05A37"       # Deeper terracotta for hover & active states
  primary-light: "#FDF5F0"       # Subtle saffron wash for pills and active filters
  secondary: "#1A382B"           # Deep forest green — heritage trust, eco/nature journeys, footer accents
  secondary-hover: "#132A20"     # Darker forest green
  gold: "#C59B27"                # Warm royal gold — luxury accents, star ratings, premium badge borders
  gold-light: "#FCF8ED"          # Pale gold tint for luxury highlight cards
  ink: "#141413"                 # Deep warm charcoal / near-black for headings and primary text
  body: "#3A3935"                # Charcoal body text for effortless long-form reading
  muted: "#6E6C65"               # Secondary metadata, itinerary days, caption labels
  muted-soft: "#9C998F"          # Subtle subtext, borders, dividers
  canvas: "#FAF8F5"              # Warm ivory / off-white primary page background
  surface-card: "#FFFFFF"        # Pure white card surface for crisp contrast against ivory canvas
  surface-soft: "#F3EFEA"        # Warm tinted background for alternating sections
  surface-dark: "#141413"        # Deep charcoal background for hero overlays and luxury dark sections
  surface-dark-card: "#1E1E1C"   # Elevated card background on dark sections
  hairline: "#E8E2D8"            # Soft border line for cards and inputs
  hairline-dark: "#2A2A27"       # Border on dark surfaces
  on-primary: "#FFFFFF"          # High-contrast text on primary buttons
  on-dark: "#FAF8F5"             # Warm ivory text on dark surfaces
  whatsapp: "#25D366"            # WhatsApp brand green for quick chat actions
  whatsapp-hover: "#20BD5A"      # WhatsApp hover state

typography:
  display-xl:
    fontFamily: "'Playfair Display', 'Cormorant Garamond', Georgia, serif"
    fontSize: 56px
    fontWeight: 600
    lineHeight: 1.12
    letterSpacing: -0.02em
  display-lg:
    fontFamily: "'Playfair Display', 'Cormorant Garamond', Georgia, serif"
    fontSize: 42px
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: -0.015em
  display-md:
    fontFamily: "'Playfair Display', 'Cormorant Garamond', Georgia, serif"
    fontSize: 32px
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: -0.01em
  display-sm:
    fontFamily: "'Playfair Display', 'Cormorant Garamond', Georgia, serif"
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
    letterSpacing: -0.005em
  title-lg:
    fontFamily: "'Plus Jakarta Sans', 'Inter', -apple-system, sans-serif"
    fontSize: 20px
    fontWeight: 600
    lineHeight: 1.35
    letterSpacing: -0.01em
  title-md:
    fontFamily: "'Plus Jakarta Sans', 'Inter', -apple-system, sans-serif"
    fontSize: 17px
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: 0
  title-sm:
    fontFamily: "'Plus Jakarta Sans', 'Inter', -apple-system, sans-serif"
    fontSize: 15px
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: 0
  body-lg:
    fontFamily: "'Plus Jakarta Sans', 'Inter', -apple-system, sans-serif"
    fontSize: 17px
    fontWeight: 400
    lineHeight: 1.65
    letterSpacing: 0
  body-md:
    fontFamily: "'Plus Jakarta Sans', 'Inter', -apple-system, sans-serif"
    fontSize: 15px
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: 0
  body-sm:
    fontFamily: "'Plus Jakarta Sans', 'Inter', -apple-system, sans-serif"
    fontSize: 13.5px
    fontWeight: 400
    lineHeight: 1.55
    letterSpacing: 0
  caption:
    fontFamily: "'Plus Jakarta Sans', 'Inter', -apple-system, sans-serif"
    fontSize: 12px
    fontWeight: 600
    lineHeight: 1.4
    letterSpacing: 0.08em
    textTransform: uppercase
  button:
    fontFamily: "'Plus Jakarta Sans', 'Inter', -apple-system, sans-serif"
    fontSize: 14.5px
    fontWeight: 600
    lineHeight: 1
    letterSpacing: 0.01em

rounded:
  xs: 4px
  sm: 6px
  md: 10px
  lg: 16px
  xl: 24px
  pill: 9999px
  full: 9999px

spacing:
  xxs: 4px
  xs: 8px
  sm: 12px
  md: 16px
  lg: 24px
  xl: 32px
  xxl: 48px
  section: 88px

components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button}"
    rounded: "{rounded.pill}"
    padding: 14px 26px
    height: 48px
    boxShadow: "0 4px 14px rgba(200, 109, 72, 0.25)"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    border: "1.5px solid {colors.hairline}"
    typography: "{typography.button}"
    rounded: "{rounded.pill}"
    padding: 13px 24px
    height: 48px
  button-forest:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button}"
    rounded: "{rounded.pill}"
    padding: 14px 26px
    height: 48px
  button-whatsapp:
    backgroundColor: "{colors.whatsapp}"
    textColor: "#FFFFFF"
    typography: "{typography.button}"
    rounded: "{rounded.pill}"
    padding: 12px 22px
    height: 44px
    boxShadow: "0 6px 20px rgba(37, 211, 102, 0.3)"
  top-nav:
    backgroundColor: "rgba(250, 248, 245, 0.92)"
    backdropBlur: "16px"
    borderBottom: "1px solid {colors.hairline}"
    height: 76px
  hero-floating-planner:
    backgroundColor: "{colors.surface-card}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.xl}"
    boxShadow: "0 20px 40px -15px rgba(20, 20, 19, 0.12)"
    padding: 24px
  destination-card:
    backgroundColor: "{colors.surface-card}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.lg}"
    overflow: "hidden"
    transition: "transform 0.3s cubic-bezier(0.16, 1, 0.3, 1), box-shadow 0.3s"
  journey-card:
    backgroundColor: "{colors.surface-card}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.lg}"
    padding: 24px
    boxShadow: "0 4px 20px rgba(0, 0, 0, 0.04)"
  trust-card:
    backgroundColor: "{colors.surface-soft}"
    border: "1px solid {colors.hairline}"
    rounded: "{rounded.lg}"
    padding: 28px
  footer:
    backgroundColor: "{colors.surface-dark}"
    textColor: "{colors.muted-soft}"
    borderTop: "1px solid {colors.hairline-dark}"
    padding: 72px 0 36px 0
---

# Selective Vacations Design System (`DESIGN.md`)

## 1. Overview & Atmosphere

Selective Vacations is positioned as a **bespoke, specialist India travel company** — not a mass-market package clearinghouse. The design system embodies the motto:

> **"India, Curated Around You."**  
> *We know India. Tell us how you want to experience it, and we'll design the journey.*

The aesthetic bridges **Heritage & Modernity**:
- The warmth and literary poise of **Anthropic's Claude** (warm ivory canvas `#FAF8F5`, literary serif headings, generous 88–96px section pacing).
- The high-trust, visual-first marketplace elegance of **Airbnb** (generous card padding, curated photography, seamless interactive search/planner controls, rounded pills).
- The rich cultural depth of **India's royal heritage** (muted saffron `#C86D48`, deep forest green `#1A382B`, and royal gold `#C59B27`).

Visitors experience a progressive emotional journey:
**DISCOVER → TRUST → IMAGINE → CUSTOMIZE → CONTACT**

---

## 2. Color System

### Primary & Brand Voltage
- **Saffron Terracotta (`#C86D48`)**: The primary call-to-action color and brand signature. Evokes Indian spices, desert sandstone, and warmth.
- **Saffron Hover (`#B05A37`)**: Deeper pressed tone for buttons and active links.
- **Saffron Tint (`#FDF5F0`)**: 5% tint used for badge pill backgrounds and category active indicators.

### Secondary & Heritage
- **Deep Forest Green (`#1A382B`)**: Echoes Kerala backwaters, Himalayan pines, and enduring calm. Anchors trust metrics, verification badges, and secondary CTA highlights.
- **Royal Gold (`#C59B27`)**: Reserved for luxury indicators, rating stars, and subtle accent lines.

### Canvas & Surface
- **Canvas (`#FAF8F5`)**: The warm ivory page base. Soft, warm, and inviting compared to sterile #FFFFFF.
- **Surface Card (`#FFFFFF`)**: Pure crisp white surfaces with 1px `{colors.hairline}` borders.
- **Surface Soft (`#F3EFEA`)**: Gentle warm stone tone for alternating section bands.
- **Surface Dark (`#141413`)**: Deep charcoal used for the footer and full-bleed hero banners.

---

## 3. Typography Hierarchy

| Role | Font Family | Size | Weight | Line Height | Tracking |
|---|---|---|---|---|---|
| **Display XL** | Playfair Display / Serif | 56px | 600 | 1.12 | -0.02em |
| **Display LG** | Playfair Display / Serif | 42px | 600 | 1.15 | -0.015em |
| **Display MD** | Playfair Display / Serif | 32px | 600 | 1.20 | -0.01em |
| **Display SM** | Playfair Display / Serif | 24px | 600 | 1.25 | -0.005em |
| **Title LG** | Plus Jakarta Sans / Inter | 20px | 600 | 1.35 | -0.01em |
| **Title MD** | Plus Jakarta Sans / Inter | 17px | 600 | 1.40 | 0 |
| **Title SM** | Plus Jakarta Sans / Inter | 15px | 600 | 1.40 | 0 |
| **Body LG** | Plus Jakarta Sans / Inter | 17px | 400 | 1.65 | 0 |
| **Body MD** | Plus Jakarta Sans / Inter | 15px | 400 | 1.60 | 0 |
| **Body SM** | Plus Jakarta Sans / Inter | 13.5px | 400 | 1.55 | 0 |
| **Caption** | Plus Jakarta Sans / Inter | 12px | 600 | 1.40 | +0.08em (caps) |
| **Button** | Plus Jakarta Sans / Inter | 14.5px | 600 | 1.00 | +0.01em |

---

## 4. Spacing, Shapes & Depth

### Spacing Scale
- `xxs` (4px), `xs` (8px), `sm` (12px), `md` (16px), `lg` (24px), `xl` (32px), `xxl` (48px), `section` (88px).
- Generous breathing room between content sections keeps the experience relaxed and premium.

### Rounded Scale
- `sm` (6px): Small badges and form controls.
- `md` (10px): Inputs, modal cards, buttons.
- `lg` (16px): Journey cards, destination tiles.
- `xl` (24px): Hero interactive trip-planning bar.
- `pill` (9999px): Primary buttons, tags, category pills.

### Elevation & Shadows
- **Card Shadow**: `0 4px 20px rgba(20, 20, 19, 0.04)` with `1px solid #E8E2D8`.
- **Hover Lift**: `0 14px 32px -6px rgba(20, 20, 19, 0.10)`, `transform: translateY(-4px)`.
- **Floating Planner Bar**: `0 20px 45px -10px rgba(20, 20, 19, 0.12)`.
- **Floating WhatsApp**: `0 10px 25px rgba(37, 211, 102, 0.35)`.

---

## 5. Signature Components

1. **Cinematic Hero with Auto-Carousel**: Full-width India landscape photography (Taj Mahal, Kerala Backwaters, Rajasthan Fort, Kashmir Valley) with warm ivory overlay and editorial headline.
2. **Interactive Trip Planner Bar**: Floating pill/card selector (`Where to?` + `When?` + `Travelers` + `Travel Style` + `[Plan My Trip]`).
3. **Editorial Destination Cards**: Asymmetric editorial layout highlighting Golden Triangle, Taj Mahal, South India, Kerala, Kashmir, and Goa.
4. **Curated Journey Cards**: Detailed route pill, duration badge, private journey tag, and dual CTAs (`Explore Journey` & `Customize This Trip`).
5. **Human Trust & Founder Section**: Dedicated "Meet Shailendra" spotlight emphasizing 14+ years of on-ground expertise and direct consultation via WhatsApp/Call.
6. **Conversion Anchors**: Floating desktop WhatsApp button & sticky mobile contact bar (`[WhatsApp]` · `[Call]` · `[Plan My Trip]`).
