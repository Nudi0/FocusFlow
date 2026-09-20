# FocusFlow — Design System & Craft Guidelines

## Aesthetic Brief
- **Pinned Aesthetic**: Girly Light Pink Vibe + Girl Gamer Theme.
- **Theme Modes**:
  - **Light Mode (Blush Petal Luxe)**: Delicate pastel rose surfaces (`#fdf7f9`), white elevation cards (`#ffffff`), plum typography (`#4a154b`), and vivid gamer pink highlights (`#ff4d94`).
  - **Dark Mode (Midnight Cyber Amethyst)**: Deep cosmic violet backgrounds (`#140a1b`), plum gamer pod cards (`#200f2a`), crystal snow text (`#fff0f7`), neon lilac accents (`#c084fc`), and neon gamer pink glow (`#ff4d94`).

## Typography Scale & Rules
- **Craft Floor**: Strict minimum font size of `12px` / `0.78rem` for all functional labels, metadata, chips, and timestamps.
- **Display**: Plus Jakarta Sans (800 / 700 weight for headers).
- **Body**: Plus Jakarta Sans (400 / 500 / 600 weight).
- **Data & Numbers**: Tabular numbers (`font-variant-numeric: tabular-nums`) enabled across all cards, stats, and tables to prevent layout jitter during live updates.
- **Monospace**: JetBrains Mono for timers, shortcut endpoints, and code identifiers.

## Elevation & Physical Lighting
- **Elevation Tokens**:
  - `--shadow-sm`: Subtle surface lift `0 1px 3px rgba(74, 21, 75, 0.05)`.
  - `--shadow-md`: Floating cards `0 4px 14px -2px rgba(74, 21, 75, 0.08)`.
  - `--shadow-lg`: Elevated panels & modals `0 10px 22px -4px rgba(74, 21, 75, 0.10)`.
  - `--gamer-glow`: Directional chromatic bloom `0 4px 14px -1px rgba(255, 77, 148, 0.28)`.
- **Focus States**: Crisp 3px solid rings with 18% alpha accent (`box-shadow: 0 0 0 3px rgba(255, 77, 148, 0.18)`), avoiding blurry zero-offset halos.

## Motion & Transitions
- Transitions are strictly constrained to compositor properties (`transform`, `opacity`, `background-color`, `border-color`, `box-shadow`).
- Zero layout-thrashing animations on `width`, `height`, or flex parameters during focus or hover states.

## Color Tokens & Contrast (WCAG AA Compliance)
| Token | Light Value | Dark Value | Purpose |
| :--- | :--- | :--- | :--- |
| `--primary` | `#ff4d94` | `#ff4d94` | Primary gamer brand pink |
| `--primary-hover` | `#a21355` | `#ff2a80` | High-contrast hover state (> 5.5:1) |
| `--accent` | `#c084fc` | `#c084fc` | Soft lavender quest accents |
| `--text` | `#4a154b` | `#fff0f7` | High contrast primary reading text |
| `--text-muted` | `#936894` | `#e9b3fa` | Secondary metadata (passing contrast) |
| `--danger` | `#be123c` | `#fb7185` | High-contrast destructive alerts |
| `--border` | `#f3d6ea` | `#4d1c64` | Delicate card contours |
