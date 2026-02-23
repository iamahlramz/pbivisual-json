# PBI Visual JSON Reference

A complete JSON reference for every native Power BI visual type. Each file is a valid, importable Power BI theme snippet targeting a specific visual — ready to use, extend, or combine.

## How to Use

1. **As a theme snippet** — Copy the JSON into your own `.json` theme file and import it into Power BI Desktop via **View > Themes > Browse for themes**.
2. **As a reference** — Open any file to see every available formatting property for that visual type.
3. **Combine visuals** — Merge multiple files by combining their `visualStyles` entries into a single theme.

## Folder Structure

```
pbivisual-json/
├── global/                  # Settings that apply to ALL visuals
│   └── universal.json
├── bar-column/              # Bar & Column charts
│   ├── clustered-bar.json
│   ├── clustered-column.json
│   ├── stacked-bar.json
│   ├── stacked-column.json
│   ├── hundred-percent-stacked-bar.json
│   └── hundred-percent-stacked-column.json
├── line-area/               # Line & Area charts
│   ├── line.json
│   ├── area.json
│   └── stacked-area.json
├── combo/                   # Combo charts
│   ├── line-clustered-column.json
│   └── line-stacked-column.json
├── pie-donut/               # Pie & Donut charts
│   ├── pie.json
│   └── donut.json
├── table-matrix/            # Table & Matrix
│   ├── table.json
│   └── matrix.json
├── card/                    # Card visuals
│   ├── card.json
│   ├── card-new.json
│   └── multi-row-card.json
├── gauge-kpi/               # Gauge & KPI
│   ├── gauge.json
│   └── kpi.json
├── map/                     # Map visuals
│   ├── map.json
│   ├── filled-map.json
│   ├── shape-map.json
│   └── azure-map.json
├── scatter/                 # Scatter chart
│   └── scatter.json
├── other-charts/            # Treemap, Funnel, Waterfall, Ribbon
│   ├── treemap.json
│   ├── funnel.json
│   ├── waterfall.json
│   └── ribbon.json
├── slicer/                  # Slicer visuals
│   ├── slicer.json
│   └── slicer-new.json
├── ui-elements/             # Buttons, Textbox, Image, Shape, Navigators
│   ├── button.json
│   ├── textbox.json
│   ├── image.json
│   ├── shape.json
│   ├── page-navigator.json
│   └── bookmark-navigator.json
└── ai-visuals/              # AI-powered visuals
    ├── decomposition-tree.json
    ├── key-influencers.json
    ├── qna.json
    └── smart-narrative.json
```

## JSON Structure

Every file follows the Power BI theme `visualStyles` format:

```json
{
  "name": "Visual Name — Reference Theme",
  "visualStyles": {
    "<internalVisualTypeName>": {
      "*": {
        "<formattingCard>": [{
          "<property>": "<value>"
        }]
      }
    }
  }
}
```

## Internal Visual Type Names

| Visual | JSON Type Name |
|---|---|
| Clustered Bar | `clusteredBarChart` |
| Clustered Column | `clusteredColumnChart` |
| Stacked Bar | `stackedBarChart` |
| Stacked Column | `stackedColumnChart` |
| 100% Stacked Bar | `hundredPercentStackedBarChart` |
| 100% Stacked Column | `hundredPercentStackedColumnChart` |
| Line | `lineChart` |
| Area | `areaChart` |
| Stacked Area | `stackedAreaChart` |
| Line & Clustered Column | `lineClusteredColumnComboChart` |
| Line & Stacked Column | `lineStackedColumnComboChart` |
| Pie | `pieChart` |
| Donut | `donutChart` |
| Table | `tableEx` |
| Matrix | `pivotTable` |
| Card (legacy) | `card` |
| Card (new) | `cardVisual` |
| Multi-row Card | `multiRowCard` |
| Gauge | `gauge` |
| KPI | `kpi` |
| Map (Bing) | `map` |
| Filled Map | `filledMap` |
| Shape Map | `shapeMap` |
| Azure Map | `azureMap` |
| Scatter | `scatterChart` |
| Treemap | `treemap` |
| Funnel | `funnel` |
| Waterfall | `waterfallChart` |
| Ribbon | `ribbonChart` |
| Slicer (legacy) | `slicer` |
| Slicer (new) | `advancedSlicerVisual` |
| Textbox | `textbox` |
| Button | `actionButton` |
| Image | `image` |
| Shape | `shape` |
| Decomposition Tree | `decompositionTreeVisual` |
| Key Influencers | `keyDriversVisual` |
| Q&A | `qnaVisual` |
| Smart Narrative | `aiNarratives` |
| Page Navigator | `pageNavigator` |
| Bookmark Navigator | `bookmarkNavigator` |

## Resources

- [Microsoft Docs — Report Themes](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-report-themes)
- [Report Theme JSON Schema (GitHub)](https://github.com/microsoft/powerbi-desktop-samples/tree/main/Report%20Theme%20JSON%20Schema)
- [MattRudy/PowerBI-ThemeTemplates](https://github.com/MattRudy/PowerBI-ThemeTemplates)
- [PBIR Format](https://learn.microsoft.com/en-us/power-bi/developer/projects/projects-report)

## License

MIT
