# Piggy Banker — Design System v2

## Color Palette

### Backgrounds
- Page: `#FAF9F6` (warm cream)
- Cards: `#FFFFFF`
- Sidebar: `#F3F1EC` (warm tinted)
- Hover states: `#EDEAE4`

### Borders
- Subtle: `#E8E5DF` (warm gray)
- Emphasis: `#D4D0C8`

### Text
- Primary: `#1A1A1A`
- Secondary: `#525252`
- Muted: `#A3A3A3`
- Inverse (on dark bg): `#FFFFFF`

### Accent Colors
- Sage Green: `#6B7C6E` (primary actions, active nav, success)
- Sage Green Hover: `#5A6B5D`
- Sage Green Light: `#E8EDEA` (light background tint for active states)
- Coral Pink: `#D4816B` (alerts, warnings, attention)
- Coral Pink Light: `#F5E6E0` (light background tint)

### Status Colors
- Active/Online: `#6B7C6E` (sage green)
- Warning: `#D4816B` (coral)
- Error: `#C4554D`
- Muted/Inactive: `#A3A3A3`

## Typography
- Font: `Inter, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`
- H1: 24px / 600 weight / #1A1A1A
- H2: 18px / 600 weight / #1A1A1A
- H3: 14px / 600 weight / #1A1A1A
- Body: 14px / 400 weight / #525252
- Caption: 12px / 400 weight / #A3A3A3
- Stat number: 32px / 700 weight / #1A1A1A

## Spacing
- Grid: 8px base
- Page padding: 32px
- Card padding: 20px
- Section gap: 24px
- Component gap: 12px

## Border Radius
- Cards: 8px
- Buttons: 6px
- Inputs: 6px
- Badges: 4px
- Avatars: 50% (circle)

## Shadows
- Card: `0 1px 3px rgba(0,0,0,0.04)`
- Elevated (modals): `0 8px 30px rgba(0,0,0,0.08)`
- None on most elements (flat/border-based hierarchy)

## Components

### Buttons
- Primary: bg `#6B7C6E`, text white, 6px radius, 14px font, 500 weight
- Ghost: bg transparent, text `#525252`, hover bg `#EDEAE4`
- Destructive: bg transparent, text `#D4816B`, hover bg `#F5E6E0`

### Inputs
- bg white, border `#E8E5DF`, 6px radius, 14px font
- Focus: border `#6B7C6E`, subtle sage green ring

### Badges
- Active: bg `#E8EDEA`, text `#6B7C6E`
- Warning: bg `#F5E6E0`, text `#D4816B`
- Neutral: bg `#F3F1EC`, text `#525252`

### Table Rows
- Default: bg transparent
- Hover: bg `#FAF9F6`
- Border bottom: `#E8E5DF`
- 48px row height, 14px text

### Sidebar Nav Items
- Default: 14px, `#525252`, 8px padding, 6px radius
- Hover: bg `#EDEAE4`
- Active: bg `#E8EDEA`, text `#6B7C6E`, 500 weight
