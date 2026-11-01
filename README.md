# NYC PLUTO Real Estate Data Cleaning

Excel Power Query portfolio exercise using New York City’s Primary Land Use Tax Lot Output (PLUTO) dataset.

> **Scope clarification:** this is an independent PLUTO practice exercise. It is **not** completion of the Growfinix Manresa Real Estate task. The required Manresa listings and historical-sales merge have not been completed; do not submit this README as proof that Task 1 is finished.

## Dataset

PLUTO contains land-use and geographic information at the NYC tax-lot level. It is not a home-sales or property-listings dataset. The data is published by the NYC Department of City Planning through NYC Open Data.

- Source: [NYC Open Data — Primary Land Use Tax Lot Output (PLUTO)](https://data.cityofnewyork.us/City-Government/Primary-Land-Use-Tax-Lot-Output-PLUTO-/64uk-42ks)
- Record the downloaded release/version and download date here before publishing, since the dataset is updated over time.
- The original CSV is large; this repository should link to the source rather than include the full source or cleaned CSV.

## Work completed

- Imported the source CSV into Excel Power Query and kept a separate `PLUTO_raw` query.
- Created `PLUTO_Cleaned` with text trimming/cleaning on `address`, `ownername`, `histdist`, and `notes`.
- Set selected area, building-count, and unit-count columns to numeric types; retained fractional values in `numfloors` using a decimal type.
- Created a duplicate audit grouped by the BBL key. It returned **0 duplicate keys**.
- Created a missing-postcode audit. It returned **1,540 rows** with a blank postcode; those missing values were retained rather than guessed or filled.

## Verified workbook counts

- Cleaned query rows loaded: **858,284**
- Columns: **108**
- Duplicate BBL audit rows: **0**
- Blank-postcode audit rows: **1,540**

Power Query’s full-dataset profile showed zero conversion errors for the numeric columns visible in the audit screenshot. Empty values remain in the dataset where present. These results describe this downloaded snapshot; refreshes of later PLUTO releases may produce different counts.

## Files to include in the repository

This upload folder contains:

- `README.md` — project scope, method, observed results, and limitations
- `evidence/PLUTO_workbook_evidence.png` — the student-provided workbook screenshot

The workbook file is not included in this prepared folder, so this repository snapshot is not fully reproducible yet. Add the actual saved workbook only if you can verify it is the correct file, remove private local paths if present, and keep it below GitHub’s browser upload limit. The original CSV is about 453 MB and is intentionally omitted; link to the official source instead.

Do not upload the original 453 MB CSV or a similarly large cleaned export. Link to the official dataset source above. If you include a small sample, label it clearly as a sample and ensure it contains no more than a few rows.

## Reproduction

1. Download PLUTO from the official NYC Open Data link above and note its release/version.
2. Open the Excel workbook and enable its data connection only if you trust the local source file and intend to refresh it.
3. Refresh the `PLUTO_raw`, `PLUTO_Cleaned`, and audit queries.
4. Compare the refreshed row counts and audit results with the values documented above; counts can change when the dataset is updated.

## Scope note

This is a data-cleaning portfolio exercise using public NYC data. It does not imply employment, attendance, supervision, or endorsement by the dataset publisher or any internship organization.
