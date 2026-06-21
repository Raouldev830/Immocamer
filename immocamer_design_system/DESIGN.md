---
name: ImmoCamer Design System
colors:
  surface: '#f7f9fb'
  surface-dim: '#d8dadc'
  surface-bright: '#f7f9fb'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f2f4f6'
  surface-container: '#eceef0'
  surface-container-high: '#e6e8ea'
  surface-container-highest: '#e0e3e5'
  on-surface: '#191c1e'
  on-surface-variant: '#3f4940'
  inverse-surface: '#2d3133'
  inverse-on-surface: '#eff1f3'
  outline: '#6f7a70'
  outline-variant: '#bec9be'
  surface-tint: '#0b6d3b'
  primary: '#004d27'
  on-primary: '#ffffff'
  primary-container: '#006837'
  on-primary-container: '#8ee4a6'
  inverse-primary: '#83d99c'
  secondary: '#835400'
  on-secondary: '#ffffff'
  secondary-container: '#fdb242'
  on-secondary-container: '#6e4600'
  tertiary: '#384356'
  on-tertiary: '#ffffff'
  tertiary-container: '#4f5a6e'
  on-tertiary-container: '#c6d1e9'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#9ef6b6'
  primary-fixed-dim: '#83d99c'
  on-primary-fixed: '#00210e'
  on-primary-fixed-variant: '#00522a'
  secondary-fixed: '#ffddb5'
  secondary-fixed-dim: '#ffb956'
  on-secondary-fixed: '#2a1800'
  on-secondary-fixed-variant: '#633f00'
  tertiary-fixed: '#d8e3fb'
  tertiary-fixed-dim: '#bcc7de'
  on-tertiary-fixed: '#111c2d'
  on-tertiary-fixed-variant: '#3c475a'
  background: '#f7f9fb'
  on-background: '#191c1e'
  surface-variant: '#e0e3e5'
typography:
  display-lg:
    fontFamily: Inter
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.01em
  headline-lg-mobile:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 32px
  headline-md:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '600'
    lineHeight: 20px
    letterSpacing: 0.01em
  label-sm:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 16px
    letterSpacing: 0.02em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 4px
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
  gutter: 16px
  margin-mobile: 16px
  margin-desktop: 48px
---

## Brand & Style

The design system is built to establish immediate institutional trust within the Cameroonian real estate market. It balances "Enterprise-grade" security with local cultural resonance, utilizing a refined interpretation of national colors to evoke a sense of home, growth, and officiality.

The aesthetic follows a **Corporate / Modern** direction. It prioritizes clarity, systematic organization, and high-legibility interfaces. The UI is designed to feel robust and permanent—mirroring the physical nature of real estate—while maintaining the agility of a modern fintech platform. Visual cues focus on verification, transparency, and effortless navigation for a diverse user base ranging from first-time renters to institutional investors.

## Colors

The palette is anchored by **Forest Green**, representing stability and land, and **Sunny Yellow**, used strategically for high-priority calls to action and "Verified" status indicators.

- **Primary (Forest Green):** Used for navigation bars, primary buttons, and branding. It signifies the "official" nature of the platform.
- **Secondary (Sunny Yellow):** Reserved for interaction highlights, Mobile Money (MoMo/Orange Money) CTAs, and verification badges.
- **Slate Gray (Tertiary):** Used for primary text and iconography to ensure high contrast without the harshness of pure black.
- **Neutral (Slate Tints):** A range of cool grays provides the foundation for backgrounds and subtle borders, maintaining a clean, "High-Trust" environment.

## Typography

This design system utilizes **Inter** exclusively for its exceptional legibility on mobile screens and its neutral, professional character. 

The type hierarchy is highly structured. Headlines use tighter letter-spacing and heavier weights to feel authoritative. Body text is set with generous line-height to ensure readability during long sessions of property browsing or document review. Label styles are used for "Verified Title" tags and metadata, ensuring that even small text remains accessible and clear.

## Layout & Spacing

The layout utilizes a **Fluid Grid** system designed for mobile-first consumption. 

- **Mobile:** 4-column grid with 16px margins. Content cards typically span the full width to maximize imagery.
- **Desktop:** 12-column grid with 24px gutters. A max-width container of 1280px is used to prevent line lengths from becoming too long, maintaining a professional "site-like" feel.
- **Vertical Rhythm:** Spacing follows an 8px scale. 16px (md) is the default for internal component padding, while 32px (xl) is used to separate distinct content sections.

## Elevation & Depth

To maintain a secure, grounded feel, this design system avoids excessive shadows. Depth is communicated through **Tonal Layers** and **Low-Contrast Outlines**.

- **Surface 0:** The main background (#F8FAFC).
- **Surface 1:** Card containers and input fields, using a white background with a subtle 1px border (#E2E8F0).
- **Surface 2:** Active states or elevated cards (e.g., featured listings) use a soft, diffused ambient shadow (0px 4px 12px rgba(0, 0, 0, 0.05)) to signify interactivity.

This approach ensures the UI feels like a single, cohesive tool rather than a collection of floating pieces.

## Shapes

The shape language is **Soft (0.25rem / 4px)**. 

While fully rounded (pill) shapes can feel too casual or "tech-startup," and sharp corners can feel aggressive, a subtle 4px radius provides a modern touch while retaining a structural, architectural feel appropriate for real estate. Larger components like property cards or search containers may use `rounded-lg` (8px) to soften the overall visual weight on mobile.

## Components

### Buttons
- **Primary:** Forest Green background with White text. Bold, 16px padding. Used for "Schedule Viewing."
- **High-Contrast CTA:** Sunny Yellow background with Black text. Reserved exclusively for "Pay with Mobile Money" or "Instant Deposit."
- **Secondary:** Ghost style with Forest Green border and text. Used for "Save Search" or "Share."

### Property Cards
Cards are the primary unit of the UI. They feature a 3:2 aspect ratio image, followed by a status bar containing "Verified Title" badges in Green/Yellow. Property price is always displayed in `headline-md` weight for immediate visibility.

### Status Indicators & Badges
Badges use a background tint of the status color (e.g., Light Green for "Verified") with high-contrast bold text. This ensures trust markers are the first thing a user notices.

### Input Fields
Fields use a 1px Slate Gray border that thickens to 2px Forest Green on focus. Labels are always visible above the field (never just placeholders) to aid in complex form completion for property listings.

### Navigation
A bottom navigation bar is prioritized for mobile users, featuring: Search, Favorites, My Listings, and Profile. On desktop, this translates to a clean top header with a distinct "List a Property" Forest Green button.