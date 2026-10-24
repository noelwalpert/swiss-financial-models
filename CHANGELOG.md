# Changelog

All notable changes to the models in this repository. The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Each model has its own version number: a change to a formula or a calculation rule raises the minor version, a change to layout or wording only raises the patch version.

## Swiss DCF Model

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
