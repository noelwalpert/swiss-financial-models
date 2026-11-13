# Changelog

All notable changes to the models in this repository. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Each model has its own version number: a change to a formula or a calculation rule raises the minor version, a change to layout or wording only raises the patch version.

## Swiss DCF Model

### [1.0.1] 2026-11-13

Wording only, no change to any formula or calculation. Release tag `v1.0.1`.

- Note on the value per share (DCF sheet, cell E42) and disclaimer on the Cover now read "implied value based on your assumptions, not a price target"
- Files renamed to version 1.0.1

### [1.0.0] 2026-10-22

First public release.

- Nine sheets: Cover, Inputs, FCF Build, WACC, DCF, Sensitivities, Reverse DCF, Checks, Settings
- Free cash flow from direct input (base year value and growth) or derived from revenue, EBIT margin, tax, depreciation, capital expenditure and net working capital
- WACC entered directly or built with CAPM, with both shown for comparison
- Terminal value by perpetuity growth or exit multiple, each with a cross-check
- Forecast period of 5 or 10 years, year-end or mid-year discounting, three scenarios (Bear, Base, Bull)
- Sensitivity tables for value per share: WACC against terminal growth, WACC against exit multiple
- Reverse DCF without Goal Seek: implied growth and implied WACC found by bisection with visible formulas
- 18 checks with the statuses OK, WARNING, ERROR, INFO and MISSING, shown as a status on every sheet
- Files: empty template and a filled example with neutral values

## Swiss Precedent Transactions Model

### [1.0.0] 2026-11-13

First public release. Release tag `precedent-transactions-v1.0.0`. A new data set (twice a year) raises the minor version.

- Eight sheets: Cover, Inputs, Data, Selection, Analysis, Valuation, Checks, Sources & Method
- Data set of all 66 public takeover offers for Swiss listed companies since 2013 (45 in the main sample), data as of 23 October 2026, each row linked to the Swiss Takeover Board
- Filters for sample, buyer type, years, sector, size class, payment and shares not liquid, plus overrides by hand
- Statistics for the premium to the 60-day VWAP, the premium to the last price, EV/EBITDA (derived) and EV/Sales (derived), with a warning below eight transactions
- Value per share of a target with three methods at the lower quartile, median and upper quartile
- 22 checks and control values that tie the model to the published analysis
- Files: template with the data set but no target company, and an example with an invented company
- CC BY 4.0 applies only to the model, not to the figures taken from documents of third parties

## Swiss LBO Model

### [1.0.0] 2026-10-25

First public release. Release tag `lbo-v1.0.0`.

- Nine sheets: Cover, Inputs, Transaction, Operations, Debt Schedule, Returns, Sensitivities, Checks, Settings
- Sources and uses, senior debt with SARON plus margin (optional floor at 0 %), mandatory amortisation and cash sweep, junior debt with fixed or SARON based interest paid in cash or in kind
- Interest on the opening balance: no circular reference, no iterative calculation, no macro
- Operations built from EBITDA or from revenue with three scenarios (Bear, Base, Bull), holding period of 3 to 7 years
- IRR, MOIC and maximum price for a target IRR as closed formulas, cross-checked with the function IRR
- Attribution of the gain to EBITDA growth, change in multiple, debt paydown, costs and the loss beyond the equity
- Sensitivity tables for IRR: entry against exit multiple, and entry multiple against senior debt (with five debt schedules)
- 19 checks with the statuses OK, WARNING, ERROR, INFO and MISSING
- Files: empty template and a filled example with neutral values

## Swiss Financial Statement Analysis Model

### [1.0.0] 2026-11-13

First public release. Release tag `fsa-v1.0.0`.

- Five sheets: Cover, Inputs, Ratios, Checks, Sources & Method
- Inputs from the income statement, balance sheet and cash flow statement for five financial years, costs and outflows entered as positive amounts
- Growth, margins, return on equity with a DuPont breakdown, return on invested capital, liquidity, leverage, free cash flow and working capital days, each ratio as a formula with its formula in words
- Leverage with and without leases under IFRS 16 in two consistent views, the mixed view only as a warning
- Nine checks with the statuses OK, WARNING, ERROR, INFO and MISSING
- No valuation, no share price and no forecast
- Files: empty template only. The repository contains no company data
- CC BY 4.0 applies only to the model, not to the figures taken from documents of third parties
