# UX Designer Agent Guidelines: Material Design 3 & User-Centric Navigation

This guide defines the core directives and practices for UX agents working on this project. Generated interfaces must prioritize clarity, accessibility, ergonomic layout, and predictable navigation using Material Design 3 principles.

## 1. Core mission and design philosophy

Design user-centric, usable, and responsive mobile interface specifications. Every layout decision must prioritize human cognitive load over visual complexity.

### Core principles

1. **User-centricity first:** Design for real tasks, not abstract screens. Minimize friction, visual clutter, and unnecessary steps.
2. **Adaptive and expressive system:** Use Material Design 3 tokens, adaptive layouts, dynamic color palettes, and standard elevation layers.
3. **Ergonomic navigation:** Navigation must feel natural, anticipate user intent, and maintain context across phone, tablet, and expanded layouts.
4. **Accessibility:** Target WCAG 2.1 AA or better. Ensure suitable contrast, touch targets, semantics, labels, focus behavior, and assistive-technology support.

## 2. Material Design 3 foundation

### Color tokens and dynamic color

Use functional color roles instead of arbitrary fixed colors:

| Color role | Usage |
| --- | --- |
| `primary` | High-emphasis actions, primary buttons, active navigation states |
| `on-primary` | Text and icons displayed over `primary` |
| `secondary` | Less-prominent components, filter chips, secondary badges |
| `surface` | Page and card backgrounds |
| `surface-variant` | Neutral containers, subtle cards, divider accents |
| `outline` | Card borders, field borders, inactive outlines |
| `error` | Failure states, destructive actions, warning banners |

Do not hardcode arbitrary colors unless defining a documented fallback palette. In Compose, use semantic values from `MaterialTheme.colorScheme`.

### Elevation

Prefer Material 3 tonal elevation and restrained shadows:

- Level 0: main content surfaces.
- Level 1: cards and search bars.
- Level 2: hovered or emphasized containers and floating banners.
- Level 3: navigation drawers and bottom sheets.
- Levels 4-5: floating action buttons, dialogs, and popovers.

## 3. Responsive and adaptive layouts

Use Material 3 window-size classes and adapt deliberately:

| Window | Width | Grid | Primary navigation |
| --- | --- | --- | --- |
| Compact | Below 600dp | 4 columns; 16dp margins and gutters | Bottom navigation or modal drawer |
| Medium | 600dp-839dp | 8 columns; 24dp margins and gutters | Navigation rail |
| Expanded | 840dp or wider | 12 columns; 24dp-32dp margins; 24dp gutters | Permanent drawer or navigation rail |

Do not merely stretch or squeeze the same layout. Recompose information and navigation for each size class.

## 4. Navigation architecture

- For three to five top-level compact destinations, prefer bottom navigation.
- For more than five compact destinations or nested menus, prefer a modal navigation drawer.
- For medium layouts, prefer a navigation rail.
- For complex expanded layouts, prefer a permanent navigation drawer.
- For focused expanded canvases, a navigation rail may be more suitable.
- Top app bars should communicate the current context and place navigation/back actions first and contextual actions last.
- Interactive touch targets must be at least 48dp by 48dp, with at least 8dp separation where practical.

## 5. Required design coverage

For every relevant screen or flow, specify:

- Primary user goal and entry point.
- Navigation and back behavior.
- Content hierarchy and primary action.
- Loading, empty, error, success, offline, and permission states.
- Compact, medium, and expanded behavior where applicable.
- TalkBack labels, traversal order, contrast, font scaling, keyboard behavior, and focus behavior.
- Components and semantic Material 3 tokens.

## 6. UX quality checklist

- [ ] The page title and current location are immediately clear.
- [ ] Loading, empty, error, and success states are defined.
- [ ] The primary action is visually distinct from secondary actions.
- [ ] Interactive targets are at least 48dp by 48dp.
- [ ] Information is grouped into understandable containers.
- [ ] The design minimizes unnecessary decisions and steps.
- [ ] Navigation preserves context and behaves predictably.
- [ ] Screen-reader semantics, focus order, contrast, and text scaling are covered.
- [ ] The design traces back to approved requirements and acceptance criteria.

