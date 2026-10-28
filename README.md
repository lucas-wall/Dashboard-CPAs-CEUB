# 🎓 CEUB Academic Evaluation | Power BI dashboard for the CPA committee

Power BI dashboard built for the self-assessment committee (CPA) of UniCEUB, a university in Brasilia. It turns raw student survey responses about courses, professors and infrastructure into an interactive report, with DAX measures, Power Query transformations and the university's own visual identity.

## Stack
`Power BI` `DAX` `Power Query / M` `Python` `pandas` `Jupyter` `Excel`

## What it does
- Navigation across three report areas: General Dashboard, Question Analysis and Academic Analysis (page assets in `Brand Identity - CPA/FullPages/`).
- Tracks agreement-scale survey scores against a 4.50/5.0 target, with a color rule (CEUB purple at 5, green at 4.5+, yellow 4 to 4.5, red below 4) defined in the project notes.
- Slices results by modality, academic term, campus, program, learning track, instrument, question group, subject and professor.
- Provides a library of DAX measures (averages, month-to-date / year-to-date, previous-month comparison, counts by answer, averages by every survey dimension) in `Brand Identity - CPA/dax_measures.txt`.
- Applies the CEUB brand: palette (`Brand Identity - CPA/Palette.txt`), dT Jakob font, logos and background layouts.

## How to open / run
1. Clone the repo and open `Dashboard-CPA's-CEUB.pbix` in Power BI Desktop.
2. If prompted, point the data source in Power Query to `CEUB_export-data-challenge-pbi.xlsx` in the repo root, then click Refresh.
3. To match the original look, install the fonts in `Brand Identity - CPA/Fonts/CEUB Font/dT Jakob/` (usage authorization in the same folder).
4. Optional exploratory analysis: `pip install pandas openpyxl jupyter`, then open `Temp-EDA.ipynb` from the repo root.

## Repo layout
- `Dashboard-CPA's-CEUB.pbix` - the Power BI report
- `CEUB_export-data-challenge-pbi.xlsx` - source survey export
- `Temp-EDA.ipynb` - quick pandas exploration of the source file
- `CPA - CEUB - Project Notes.txt` - requirements and design notes
- `Brand Identity - CPA/` - palette, fonts, logos, page backgrounds, DAX measure reference
- `Current Dashboard Screenshots/` - screenshots of the university's existing dashboard, used as reference

Note: the source data, logos and page images keep their original Portuguese labels, since they come from the university.

## License
MIT, see `LICENSE`.
