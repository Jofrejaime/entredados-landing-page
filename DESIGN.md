---
name: Technical Humanism
colors:
  surface: '#0d150f'
  surface-dim: '#0d150f'
  surface-bright: '#323b34'
  surface-container-lowest: '#08100a'
  surface-container-low: '#151e17'
  surface-container: '#19221b'
  surface-container-high: '#232c25'
  surface-container-highest: '#2e3730'
  on-surface: '#dbe5da'
  on-surface-variant: '#bacbbb'
  inverse-surface: '#dbe5da'
  inverse-on-surface: '#2a332b'
  outline: '#859587'
  outline-variant: '#3b4a3f'
  surface-tint: '#13e385'
  primary: '#45fc9c'
  on-primary: '#00391d'
  primary-container: '#00df82'
  on-primary-container: '#005d33'
  inverse-primary: '#006d3d'
  secondary: '#bac9c9'
  on-secondary: '#253333'
  secondary-container: '#3b4949'
  on-secondary-container: '#a9b8b7'
  tertiary: '#ffd7b7'
  on-tertiary: '#4c2700'
  tertiary-container: '#ffb26c'
  on-tertiary-container: '#794202'
  error: '#FF4D4D'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#5affa2'
  primary-fixed-dim: '#13e385'
  on-primary-fixed: '#00210f'
  on-primary-fixed-variant: '#00522c'
  secondary-fixed: '#d6e6e5'
  secondary-fixed-dim: '#bac9c9'
  on-secondary-fixed: '#101e1e'
  on-secondary-fixed-variant: '#3b4949'
  tertiary-fixed: '#ffdcc1'
  tertiary-fixed-dim: '#ffb778'
  on-tertiary-fixed: '#2e1500'
  on-tertiary-fixed-variant: '#6c3a00'
  background: '#0d150f'
  on-background: '#dbe5da'
  surface-variant: '#2e3730'
  white-cool: '#F1F7F7'
  surface-elevated: '#0A1A1A'
  border-subtle: '#1C2E2E'
  text-secondary: '#8AADA8'
  text-tertiary: '#4D6B66'
  warning: '#F5A623'
  info: '#3B9EE8'
typography:
  display:
    fontFamily: Oxanium
    fontSize: 72px
    fontWeight: '700'
    lineHeight: '1.05'
    letterSpacing: -0.02em
  h1:
    fontFamily: Oxanium
    fontSize: 56px
    fontWeight: '700'
    lineHeight: '1.1'
  h1-mobile:
    fontFamily: Oxanium
    fontSize: 40px
    fontWeight: '700'
    lineHeight: '1.1'
  h2:
    fontFamily: Oxanium
    fontSize: 40px
    fontWeight: '600'
    lineHeight: '1.15'
  h3:
    fontFamily: Oxanium
    fontSize: 28px
    fontWeight: '600'
    lineHeight: '1.2'
  body-lg:
    fontFamily: Poppins
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.7'
  body:
    fontFamily: Poppins
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.7'
  label:
    fontFamily: Poppins
    fontSize: 12px
    fontWeight: '600'
    lineHeight: '1.4'
    letterSpacing: 0.12em
  cta:
    fontFamily: Poppins
    fontSize: 16px
    fontWeight: '600'
    lineHeight: '1'
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  base: 4px
  xs: 8px
  sm: 16px
  md: 32px
  lg: 64px
  xl: 96px
  section-desktop: 128px
  gutter: 24px
---

## Brand & Style

This design system is engineered to bridge the gap between complex data engineering and strategic business leadership. It embodies a "Technical Humanism" style—a sophisticated blend of high-tech precision and approachable clarity. 

The aesthetic is rooted in **Corporate Minimalism** with a digital-first edge. It utilizes a dark-mode default to reduce cognitive load and emphasize high-contrast data visualizations. The atmosphere is one of a "Mission Control Center": quiet, powerful, and focused. Visual elements are governed by strict mathematical ratios, ensuring every pixel serves a functional purpose, while the photography emphasizes real human collaboration in modern, data-driven environments.

## Colors

The palette is dominated by **Deep Black (#030F0F)** and **Entredados Green (#00DF82)**. This high-contrast pairing creates a vibrant, energetic feel that signals innovation and technical mastery.

- **Primary (Green):** Used for critical actions, brand signatures, and data highlights. It represents growth and binary logic.
- **Surface Tiers:** Backgrounds transition from the base Deep Black to **Elevated Surface (#0A1A1A)** to create depth without relying on traditional shadows.
- **Typography Colors:** We avoid pure white for long-form reading, opting for **Cool White (#F1F7F7)** for headings and **Secondary Teal (#8AADA8)** for body text to maintain a comfortable reading experience on OLED screens.

## Typography

The typographic system utilizes a dual-font strategy to balance the brand's persona.

1.  **Oxanium (Headings):** A futuristic, geometric typeface with "cut" corners that evokes digital circuitry and data blocks. It is used exclusively for large titles and numbers.
2.  **Poppins (UI/Body):** A clean, geometric sans-serif that provides excellent legibility for complex information.

**Key Rules:**
- **Oxanium** must never be used below 16px or in italics.
- **Section Eyebrows** use the `label` token, always in uppercase and the primary green color, to act as a clear navigational anchor.
- Paragraphs are limited to a maximum width of 70 characters to ensure optimal readability.

## Layout & Spacing

The layout is built on a **12-column fixed grid** (1200px max-width) for desktop, transitioning to 8 columns for tablets and 4 columns for mobile.

The spacing system follows a strict **4px baseline grid**. This mathematical consistency reinforces the brand's "Precision" principle. 
- **Vertical Rhythm:** Large sections are separated by 96px or 128px of whitespace to allow the technical content to "breathe."
- **Component Gaps:** Use 16px (sm) for internal card padding and 32px (md) for gaps between layout cards.

## Elevation & Depth

This design system rejects traditional soft shadows in favor of **Tonal Layering** and **Luminous Outlines**.

Depth is created by stacking surfaces of increasing lightness:
1.  **Base Layer:** Deep Black (#030F0F).
2.  **Surface Layer:** Elevated Surface (#0A1A1A) with a Subtle Border (#1C2E2E).
3.  **Active Layer:** Uses a glowing 1px border of primary green (#00DF82) to indicate focus or selection.

For accessibility, a low-opacity "Sombra de Foco" (box-shadow: 0 0 0 3px #00DF8220) is the only shadow permitted, used strictly for focus states.

## Shapes

The shape language is "Calculated Softness." While the brand is technical, overly sharp corners feel aggressive. We use a **Rounded (0.5rem)** base to make the interface feel modern and professional.

- **Inputs & Buttons:** Use `rounded-md` (8px) for a sturdy, reliable feel.
- **Service Cards:** Use `rounded-lg` (12px) to create a distinct container for content.
- **Badges/Pills:** Use `rounded-full` to contrast against the more rigid grid elements.

## Components

### Buttons
- **Primary:** Solid green background with black text. On hover, it scales slightly (1.01x) and shifts to a darker green hover state.
- **Secondary (Outline):** 1px green border with green text. Hover uses a 15% opacity green tint.
- **Ghost:** No border/background. Used for navigation.

### Cards
Cards are the primary vessel for data. They feature the Elevated Surface background and a subtle border. On hover, they shift up by 2px and the border color increases in opacity to create a "lift" effect without shadows.

### Inputs
Text fields use the Elevated Surface background to sit "into" the page. The focus state replaces the subtle border with a crisp primary green line and a soft glow.

### Badges
Used for tags and categories. They always use the "Muted Green" (20% opacity) background with bold, uppercase Poppins text to ensure they are legible but secondary to the main content.

### Iconography
Exclusively use **Phosphor Icons** in "Regular" weight. Icons should be functional indicators (e.g., arrows, status checks), never purely decorative.