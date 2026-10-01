---
name: Tarkit V.Final_one
description: The supplied consulting and CRM identity, refined with Hubot Sans and outlined signal-window illustrations.
colors:
  yellow: "#f9fe56"
  purple: "#7850bd"
  deep: "#523888"
  pink: "#ad398f"
  lavender: "#f1e6f6"
  black: "#19171b"
  white: "#fff"
  canvas: "#fcfbfd"
  muted: "#625b66"
  line: "rgba(3,3,3,.14)"
typography:
  display:
    fontFamily: "Hubot Sans, sans-serif"
    fontSize: "clamp(48px,5.8vw,80px)"
    fontWeight: 700
    lineHeight: 1.01
    letterSpacing: "-.04em"
  headline:
    fontFamily: "Hubot Sans, sans-serif"
    fontSize: "clamp(36px,4.4vw,58px)"
    fontWeight: 700
    lineHeight: .98
    letterSpacing: "-.04em"
  title:
    fontFamily: "Hubot Sans, sans-serif"
    fontSize: "21px"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-.04em"
  body:
    fontFamily: "Hubot Sans, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.65
  lead:
    fontFamily: "Hubot Sans, sans-serif"
    fontSize: "18px"
    fontWeight: 400
    lineHeight: 1.7
  button:
    fontFamily: "Hubot Sans, sans-serif"
    fontSize: "14px"
    fontWeight: 800
rounded:
  field: "10px"
  note: "12px"
  panel: "20px"
  card: "24px"
  pill: "999px"
spacing:
  compact: "12px"
  small: "16px"
  medium: "24px"
  large: "32px"
  section-gap: "60px"
components:
  button-primary:
    backgroundColor: "{colors.yellow}"
    textColor: "{colors.black}"
    typography: "{typography.button}"
    rounded: "{rounded.pill}"
    padding: "0 22px"
  button-secondary:
    backgroundColor: "transparent"
    textColor: "{colors.black}"
    typography: "{typography.button}"
    rounded: "{rounded.pill}"
    padding: "0 22px"
  service-card:
    backgroundColor: "{colors.white}"
    rounded: "{rounded.card}"
  text-field:
    backgroundColor: "{colors.white}"
    textColor: "{colors.black}"
    rounded: "{rounded.field}"
    padding: "13px 16px"
---

# Design System: Tarkit V.Final_one

## Overview

**Creative North Star: "The Tarkit Signal Window"**

This is a refinement of the user's V.01 consulting and V.03 CRM visual world. The supplied Tarkit logo, purple and yellow palette, rounded outlines, and signal-window illustrations are the visual authority. Hubot Sans connects commercial headlines, readable explanatory text, and compact interface detail.

Generous whitespace supports the content. Colored sections punctuate the reading sequence, while outlined illustrations give the consulting and software pages a shared visual language. The supplied SVG contains both mark and wordmark; do not add a second company-name label.

**Key Characteristics:**
- Confident Hubot Sans headlines and readable body copy.
- Signal yellow actions, expressive purple, lavender supporting surfaces, and charcoal structure.
- Rounded outlined illustrations with selective structural depth.
- Responsive grids, permanent form labels, and visible keyboard focus.

Source of truth: `assets/base.css`, followed by `assets/site.css`; the latter wins overlapping declarations. The extension sidecar is stored at `../.impeccable/design.json` outside the published folder.

## Colors

The established palette combines a bright action color with purple expression and quiet light surfaces; the frontmatter records the final cascade.

### Primary
- **Signal yellow:** primary actions, the tool strip, and selected illustration tiles.
- **Deep purple:** readable emphasis, focus rings, and the process section.

### Secondary
- **Purple:** illustration depth and select headline or graphic accents.
- **Pink:** restrained illustration detail. Saturated pink and purple illustration tiles use white text in the final implementation.
- **Lavender:** supporting panels and the closing invitation.

### Neutral
- **Canvas and white:** page background and outlined content surfaces.
- **Charcoal:** body text, structural outlines, footer, and dark actions.
- **Muted:** supporting text on light backgrounds.
- **Line:** low-contrast dividers between sections and inside panels.

**The Surface Contrast Rule.** Use the light footer text treatments on charcoal and white text on the saturated illustration tiles; do not reuse light-surface muted text on dark sections.

## Typography

Hubot Sans is locally hosted for all roles. The Regular asset is registered for weights 400–600, Bold for 700, and ExtraBold for 800–900. The frontmatter captures the shared roles, not every illustration label.

Hero headlines scale responsively and balance their lines. General page introductions have a slightly larger maximum than the home hero. Mobile hero text uses `clamp(42px,10vw,64px)`. Body content uses a comfortable reading measure, typically 55–70 characters; lead paragraphs use 58 characters. Guide paragraphs are 18px on desktop and 17px on mobile. Navigation and action labels are 14px; compact illustration annotations are subordinate to these reading sizes.

**The One Face Rule.** Keep Hubot Sans across display, body, and UI. Preserve the supplied logo as an asset rather than recreating its lettering with live text.

## Layout

The main container is capped at 1240px with 24px side gutters on desktop. Below 768px it uses 20px side gutters. Reading guides cap their container at 850px.

Desktop layouts pair text and an illustration or supporting content; section headings and service details use two columns. Service cards form three columns, reduce to two at 900px, and become a single column at 767px. The main text-and-illustration hero becomes a single column at 900px. Other paired content sections collapse at 767px.

The desktop header is at least 84px tall. At 900px it switches to a 76px header with an accessible collapsible navigation menu. At 1100px the header's large contact action is hidden while Login remains available; the collapsed menu includes the contact destination.

Section spacing generally uses 60–90px on desktop and 38–58px on mobile. Preserve the generous space around headlines while keeping related labels, fields, and supporting text close together.

## Elevation & Depth

Most content uses flat white or lavender surfaces and subtle divider lines. The inherited outlined illustration language uses selective hard colored offsets for depth, including the signal window's purple offset. These are identity elements from the supplied design, not a rule to apply to every content card.

Fine-pointer button hover adds a small soft shadow (`0 5px 15px #19171b12`). The sticky header retains a subtle scrolled shadow from the base stylesheet. Do not introduce decorative gradients or neon effects.

## Shapes

Buttons use full pill corners and a charcoal outline (1.5px). Service cards use generous rounded corners; fields are more compact. Major illustrative windows use a strong outline (2px), softly rounded corners, and restrained rotation. Circular details and colored tiles belong to the supplied signal-window vocabulary.

## Components

### Buttons

Confident, outlined pills. Primary buttons use signal yellow; secondary buttons remain transparent at rest. Both have a minimum height of 48px and the padding in the frontmatter. Fine-pointer hover changes the primary to `#f0f54b` and the secondary to lavender. Press feedback scales to `.97` over 160ms. Keyboard focus uses a deep-purple outline (3px) with a 5px offset. Closing actions use white text on charcoal.

### Cards and illustrated containers

Service cards are white, bordered with the line color, and contain a colored illustration above their text. The text area uses 24px padding on desktop. Keep the signal window's outlined, layered illustration character shared between consulting and CRM, and identify demonstration data as illustrative.

### Inputs and fields

Fields use permanent 15px bold labels, white backgrounds, a thin neutral border, and a minimum height of 50px. Textareas resize vertically. Focus uses the global deep-purple ring. Validation is placed inline; the contact form describes its email-draft behavior, and demo access states its limitations.

### Navigation

The supplied SVG is the complete brand lockup. Desktop navigation uses concise labels and a purple underline for the current page. The mobile menu button exposes its expanded state and controls the navigation panel. The skip link becomes visible on keyboard focus. Footer links use light text and yellow hover on charcoal.

### Resources and guides

Resources use spacious divider-separated rows with a title, metadata, and one directional icon. On mobile the metadata moves above the title. Guides use a narrower reading measure, linked contents, and lavender note panels.

### Tool-logo strip

Two equal groups move as one continuous, linear 28-second loop. Hover, focus, the explicit pause control, and reduced-motion preference stop movement. Reduced motion leaves a scrollable strip and removes the duplicate hidden group. Keep routine keyboard interactions immediate; most of the site remains still.

## Do's and Don'ts

### Do:
- **Do** preserve the supplied V.01 and V.03 visual identity, supplied logo, and Hubot Sans.
- **Do** use signal yellow for primary actions and retain clear outlined illustration geometry.
- **Do** keep reading text comfortable, focus visible, and interactive targets at least 44px tall.
- **Do** keep illustrative sample data visibly identified and form outcomes explicit.
- **Do** honor reduced motion and provide direct control over the tool-logo loop.

### Don't:
- **Don't** replace the established palette with a generic single-accent system.
- **Don't** add a second company-name label beside the complete supplied logo.
- **Don't** introduce decorative gradients, neon effects, or motion without a clear purpose.
- **Don't** add fabricated testimonials, performance results, badges, prices, or capabilities as visual proof.
- **Don't** present the email-draft form as a sent-message confirmation or demo access as secure authentication.
