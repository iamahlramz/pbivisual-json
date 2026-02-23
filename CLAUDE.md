# pbivisual-json

Power BI visual JSON theme reference — every native visual type with all formatting properties.

## Skills

- **pbi-frontend** — Apply when creating or reviewing theme JSON files. Every theme snippet should produce visuals that follow the 10 design rules: data-first, Gestalt grouping, Z-pattern layout, consistent grid, container grouping, contrast-checked, limited palette, gray-as-default, 4-5 visuals per page, zero clutter.

## Project Rules

- **ALWAYS** reference `config/skills/pbi-frontend/SKILL.md` for design decisions when generating or modifying visual theme JSON
- **ALWAYS** use the visual type names from `README.md` (e.g., `clusteredBarChart`, `tableEx`, `pivotTable`)
- **ALWAYS** follow the `visualStyles` JSON structure when creating theme snippets
- **NEVER** hardcode colors — define palette variables in the theme and reference them consistently
- **NEVER** add decorative formatting (3D effects, heavy borders, gradient fills) that violates Rule 1 (data is the main actor)
- Gray (`#D0D0D0`, `#E0E0E0`, `#808080`) should be the default for axes, gridlines, borders, and secondary elements (Rule 8)
- Accent colors should be reserved for data highlights, conditional formatting, and status indicators only (Rule 7)
