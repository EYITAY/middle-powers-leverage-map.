# Middle Powers Leverage Map

Hackathon: Middle Powers, AI safety hackathon (Mangrove). Track C, Diplomacy.
Author: Eyitayo Alimi
Report written by : 

## What it is

A sourced map of which middle powers hold something frontier AI developers cannot easily replace, and a finder for small groups of countries that together hold enough of it to set a condition, such as independent pre-deployment testing of frontier models.

- Ten countries: Canada, South Korea, Brazil, Indonesia, Australia, Singapore, South Africa, the Netherlands, Nigeria, India.
- Seven layers: Energy, Chips, Infrastructure (cables and exchanges), Data centres, Algorithms, Talent, Consumption.
- 70 cells. Each has a score (0 to 3), a confidence flag, a Conditionable flag, a source link and date, and a one-line reason.

## Results in one paragraph

Only two cells are chokepoints (score 3), both in chips: South Korea (HBM memory) and the Netherlands (EUV lithography). Every credible coalition contains both. The best group of three is South Korea, Brazil and the Netherlands. The best group of four adds Singapore, but it ties with the group that adds India on chokepoints, layers and coverage and wins only on a tie-break that depends on one judgment-based cell (Singapore Data centres, score 2, which rests on its overflow role into Indonesia). All ten Algorithms cells score 1 and nine of ten Data centres cells score 1.

## Files

| File | What it is |
| --- | --- |
| `leverage_master_calibrated.csv` | The 70-row data sheet with sources and calibration notes |
| `index.html` | Interactive page: map, evidence drawer, coalition finder with stability test and animation. Reads the CSV |
| `memo.md` or `memo.pdf` | Short argument from leverage to a pre-deployment testing condition |
| Rubric doc | Scoring rules, calibration log, coalition ranking method (link in the submission) |

## Method

Scores follow written rules. A 3 needs a sole supplier or dominant share from a primary source or two agreeing sources. Where sources conflict, the lower score is used. Seven cells were re-scored after the first pass so that similar evidence got similar scores; each change is logged in the Calibration column.

Coalitions of 3 or 4 are ranked in order by: chokepoint cells held, layers where the group reaches 2 or more, total coverage (highest member score per layer, summed), then cells scoring 2 or more.

## Limits

- Only two chokepoints, both in chips.
- One cell has no score because no source was found: South Africa Talent. Nigeria Chips is scored 0 on one self-reported claim.
- 58 of 70 cells are Single source or Unverified. The South Korea HBM figures were checked against a headline only; the Netherlands cell was checked against ASML's FY2025 20-F.
- Scores are judgments under written rules.
- Ten countries is a sample. Leverage held is not willingness to use it.


## Future work

- **Strengthen the two chokepoints.** Replace the South Korea HBM headline figure with the full Counterpoint or TrendForce table, and read the Cushman & Wakefield original behind Singapore's capacity.
- **Fill and recheck weak cells.** Find a source for South Africa Talent, back Nigeria Chips with a primary source, and replace Wikipedia and secondary-report rows with originals. 58 of 70 cells are still Single source or Unverified.
- **Widen the country set.** Add a screening tier of 30 to 40 countries with a few numeric indicators, and an "add your country" template so others can contribute rows.
- **Test the scores.** Have two or three independent readers score a sample of cells under the written rules and report where they disagree.
- **Add a Conditionable analysis.** Record who legally controls each lever (government, a private firm, or a foreign government) and how each could be attached to a condition such as pre-deployment testing.
- **Model willingness, not only leverage.** Add political and diplomatic factors that decide whether a group would act, using sources outside this sheet.
- **Track change over time.** Date every cell and re-run the ranking each quarter, since data-centre capacity, chip plants and trade rules are moving fast.
- **Test the condition itself.** Work with a testing body to define what independent pre-deployment testing would require of a developer, so that the condition is concrete enough to negotiate.

## Deploy

`index.html` is a single static file with Vercel Web Analytics included. Import the repo in Vercel (no build step), then turn on Analytics in the project's Analytics tab. Page views appear after the first visits to the deployed site.

## Sources

Every source is linked in the `Source URL` column of the CSV and in each cell's evidence drawer on the page.# middle-powers-leverage-map.
