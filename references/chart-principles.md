# Chart principles

Match charts are editorial graphics, not dashboards. A reader should get one idea from each chart within a few seconds and still be able to find the supporting detail on a second look.

## One dominant story per chart

Decide the sentence the chart proves before choosing the chart type, and write that sentence into the title. If a chart needs two sentences, split it.

## Use real geometry

Shot maps, pass maps and zone charts should use the actual pitch coordinate system with correct proportions - goal, penalty area, centre circle. Placeholder rectangles and decorative diagonal blocks are rejected: the graphic has to read as football.

## Encode once, then stay consistent

A set of charts for one match shares one palette, one encoding for the same quantity, and identical masthead and footer wording. If a colour means "shots" in one chart it cannot mean "possession" in the next. Use the club's authentic colours for team identification and keep them distinguishable at small sizes.

## Hierarchy

The title states the finding, one or two key numbers carry the magnitude, annotations explain the exceptional case, and the axis or legend stays quiet. Bold weight belongs to the finding, not to every label.

## Typography and language

Pick one Chinese face and one Latin face for the whole set and use them everywhere, including footers and axis ticks. Use tabular or monospaced figures for columns of numbers so digits line up. Never ship a font that is missing the characters you need, and never let a fallback font change sizes mid-chart.

## Spacing and labels

Nothing overlaps, nothing is clipped, no label sits on top of a mark, and no legend covers data. Player names that do not fit get shortened consistently, with the full name in the chart brief instead of two lines of tiny type.

## Export

Export PNG at 300 DPI, name files by a fixed pattern that includes the match, and keep one file per chart. Readable at full size on a phone is the minimum bar, not the goal.

## QA gate

Open every exported file at full resolution before delivery and check, in this order: the title still states the finding, the numbers match the source data, no element overlaps or clips, the footer is identical across the set, and the file names match the brief. Fix, then look again.
