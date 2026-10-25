---
name: Nawajiz Beauty
description: Soft Arabic beauty storefront with navy type, orange accents, and ivory surfaces.
colors:
  ink: "#0f253a"
  muted: "#627078"
  orange: "#ff8f2a"
  orange-dark: "#a4480c"
  cream: "#fcfaf7"
  surface: "#f3efe9"
  line: "#e5dfd7"
  white: "#fff"
  primary-hover: "#243e51"
  footer-muted: "#c6ccd0"
  favorite: "#ad431e"
typography:
  display:
    fontFamily: "Tajawal, sans-serif"
    fontSize: "clamp(30px,3vw,44px)"
    fontWeight: 500
    lineHeight: 1.3
    letterSpacing: "-1px"
  headline:
    fontFamily: "Tajawal, sans-serif"
    fontSize: "clamp(27px,2.5vw,36px)"
    fontWeight: 500
    lineHeight: 1.3
    letterSpacing: "-.6px"
  title:
    fontFamily: "Tajawal, sans-serif"
    fontSize: "17px"
    fontWeight: 500
    lineHeight: 1.3
  body:
    fontFamily: "Tajawal, sans-serif"
    fontSize: "16px"
    lineHeight: 1.6
  brand-label:
    fontFamily: "DM Sans, sans-serif"
    fontSize: "10px"
    letterSpacing: "1.4px"
  price:
    fontFamily: "DM Sans, Tajawal, sans-serif"
    fontSize: "17px"
    fontWeight: 500
rounded:
  button: "6px"
  compact: "8px"
  mobile-image: "10px"
  product: "12px"
  panel: "16px"
  badge: "20px"
  tab: "30px"
  circle: "50%"
spacing:
  small: "8px"
  medium: "16px"
  grid: "24px"
  panel: "32px"
components:
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.white}"
    rounded: "{rounded.button}"
    padding: "13px 23px"
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink}"
    rounded: "{rounded.button}"
    padding: "13px 23px"
  tab-selected:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.white}"
    rounded: "{rounded.tab}"
    padding: "9px 18px"
  product-visual:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.product}"
---

# Design System: Nawajiz Beauty

## Overview

This is a source-derived record of the implemented design, not a new preference workshop. The user's soft, smooth beauty direction and supplied orange/navy identity are expressed through an ivory canvas, spacious photography, fine dividers, rounded images, and gentle interaction motion. Supplied logos and campaign lettering remain image assets.

Key characteristics: Arabic RTL reading order; restrained orange accents; navy headings and primary actions; flat product presentation; rounded campaign imagery. These descriptions characterize the current implementation and do not claim an independently confirmed creative metaphor.

## Colors

### Primary
Orange carries small accents, active navigation underlines, basket count, and hover feedback. Orange-dark carries readable accent links and focus indicators.

### Neutral
Ink supplies primary text, action fills, announcement strip, and footer. Cream is the page and dialog canvas; surface distinguishes product imagery and empty states; line separates navigation, controls, and cart rows. Muted is supporting text. White reverses out of dark surfaces. Footer-muted supports footer links and explanatory copy. Favorite is the filled-heart selected state.

**The Identity Rule.** Keep supplied campaign artwork intact; use the page palette around it rather than recoloring campaign content.

## Typography

Tajawal is the Arabic body and heading family. DM Sans supplies Latin brand labels, numeric prices, counts, and the footer's English line. Both load through Google Fonts with sans-serif fallbacks. Headings generally use medium weight and a compact line height; there is no modular type scale enforced by the source.

Display and catalog headlines use the fluid sizes recorded above. Section headings use 23px at desktop and 21px on mobile. Supporting descriptions are usually 14px; labels and disclosures range from 10px to 13px. On mobile the hero settles at 26px, catalog headline at 26px, product titles at 14px, prices at 15px, and brand labels at 9px. Preserve native Arabic shaping and RTL alignment; numeric controls use explicit LTR direction where needed.

## Layout

The centered content container caps at 1392px and uses width `calc(100% - 112px)`. At 1100px and below its total horizontal inset becomes 60px; at 760px and below it becomes 32px. The header is sticky, with a 90px main row and 54px navigation row at desktop. Scroll padding is 165px, increasing to 180px on mobile.

The catalog has four equal columns with 36px row and 24px column gaps. Below 1100px gaps become 30px and 18px. At 760px it becomes two columns with 26px and 13px gaps. Categories start as eight columns, then become a horizontal scrolling row with proximity snapping on mobile. Navigation also scrolls horizontally; search moves into its own header row. The footer changes from four columns to two.

The editorial campaign panel uses one column at every breakpoint, with full-width imagery at its intrinsic aspect ratio. Its copy uses 36px 42px padding on desktop and 28px on mobile. The manual headline break is hidden on desktop and restored on mobile; h1 and h2 also use balanced text wrapping. Product details stack on mobile. The left-side cart drawer is 460px wide on desktop and full-width on mobile; centered product and information dialogs retain safe viewport insets. At 1600px and above intro top padding increases to 46px.

**The Campaign Legibility Rule.** Final mobile overrides preserve full hero and wide-banner image proportions with automatic height and containment. The editorial campaign image preserves its proportions at every breakpoint and has no hover zoom; do not reintroduce the earlier cropping rules.

## Elevation & Depth

Most of the storefront is flat: ivory and tinted photographic surfaces, fine borders, and spacing establish separation. Shadows are reserved for overlays. Dialogs use `0 20px 80px #0f253a26`; toast feedback uses `0 8px 24px #0f253a1a`. Dialog backdrops use a navy translucent fill and 4px blur. Product cards have no enclosing shadow or border.

## Shapes

Campaigns, editorial panels, empty states, and centered dialogs share generous panel corners. Product images have slightly tighter corners, reducing further on mobile. Buttons use small corners; filter tabs and small badges are pill-shaped. Categories, heart buttons, add buttons, and the closing arrow are circles. The full-height cart drawer has square corners. Use the frontmatter's role-specific radius values rather than applying one radius everywhere.

## Components

### Buttons and links
Primary actions combine navy fill, white type, 48px minimum height, and a 14px icon gap. Hover shifts to primary-hover and lifts by 2px. Secondary actions use the surface fill. Circular add controls have a fine border, turn orange, and rotate on hover. Text-link arrows travel left by 5px. The global keyboard focus indicator is a 2px orange-dark outline with 5px offset. Disabled buttons use 0.4 opacity and a not-allowed cursor.

### Filters and navigation
Pill filters use a navy selected state with white text, and a surface hover background. Navigation uses an orange underline on hover and current state. Category images lift 5px with an orange outline on hover and use orange-dark for the current category. Selected filters and favorites expose `aria-pressed` state.

### Product cards
A square photographic area sits above a compact brand/size row, title, and price/add row. Photography is a shared four-by-two sprite. Hearts sit at the upper left, badges at the upper right. Image hover scales to 1.055 and reveals a white quick-view pill; keyboard focus also reveals the pill. Mobile hides quick-view and retains the accessible product-opening button. Selected hearts are filled. Original prices are struck through only for products with an old price.

### Search and sorting
Search is an underline field with a transparent background, muted placeholder, and orange-dark focus-within border. Sort is a native select with a transparent background. Search supports normalized Arabic text; categories, favorite mode, and sorting update the existing grid. Empty results have a centered explanation and recovery action.

### Dialogs, drawer, and feedback
Named native modal dialogs provide product detail, demo information, and the cart. Keyboard focus is restored after favorite changes, cart quantity updates, and item removal. Background scrolling locks while dialogs are open. The cart contains square thumbnails, quantity controls, removal, total, and demo completion. Toasts appear near the bottom center for 2600ms. Cart and favorites persist only in local browser storage.

Motion uses the source cubic-bezier ease for photograph zooms and entrance transitions. Most feedback lasts 0.2-0.3s; dialog entrance is 0.35s, drawer entrance 0.45s, and photo transitions 0.65-1s. Reduced-motion CSS removes transitions and animations, disables CSS smooth scrolling, and removes product-photo hover scaling. JavaScript scroll calls also respect the reduced-motion preference.

## Do's and Don'ts

- Do maintain RTL document flow, Arabic labels, accessible control names, and visible keyboard focus.
- Do retain soft photographic surfaces and fine separators instead of adding card shadows.
- Do preserve supplied campaign artwork and the final mobile containment override.
- Do label fictional products, prices, and checkout as demonstration content.
- Don't add unsupported reviews, certifications, real-order promises, or treatment claims.
- Don't assume one corner radius or one font covers every role; use the implemented role-specific choices.


