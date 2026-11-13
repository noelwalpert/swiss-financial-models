# Swiss Financial Statement Analysis Model

An Excel model that turns five years of reported figures into the ratios analysts use to read a company: growth, margins, return on equity with a DuPont breakdown, return on invested capital, liquidity and leverage, cash flow, working capital, and leverage with and without leases under IFRS 16.

Version 1.0.0. Currency: Swiss francs, amounts in millions. The model contains no valuation, no share price and no forecast. Online analysis with two Swiss companies: [noelwalpert.com/analysen/kennzahlenanalyse](https://noelwalpert.com/analysen/kennzahlenanalyse).

## Files

| File | Content |
|---|---|
| [`swiss-fsa-template-v1.0.0.xlsx`](swiss-fsa-template-v1.0.0.xlsx) | Empty template. Ratios show "n/a" and the status "Inputs missing" until you fill in the blue cells |

The repository contains no company data. An example filled with the reported figures of a Swiss company is available on the website.

## The five sheets

| Sheet | Purpose |
|---|---|
| Cover | Version, key figures of the last year, model status, colour code, contents, sources, licence, disclaimer |
| Inputs | Income statement, balance sheet and cash flow statement for five financial years, plus the company name, the first year and a switch for lease liabilities included in financial debt |
| Ratios | All ratios as formulas, each with its formula in words, and the compound annual growth rate |
| Checks | Nine plausibility and integrity checks |
| Sources & Method | Method notes and a table for the source of every input |

## Colour code

| Colour | Meaning |
|---|---|
| Blue font, light blue fill | Input. Change these cells |
| Black font | Formula on the same sheet |
| Green font | Link to another sheet |

## How to use

1. Open the template in Excel (desktop or browser). Excel calculates the file when it opens.
2. On Inputs, enter the company name, the first financial year and whether the lease liabilities are part of the financial debt lines.
3. Enter the figures from the annual reports. Costs and cash outflows are entered as positive amounts. Optional lines (amortisation, reported EBITDA, interest outside operating cash flow, purchases of intangibles, share buybacks) may stay empty.
4. Read the ratios on Ratios and check the status on Checks. An ERROR must be fixed, a WARNING deserves a second look.

## Method in short

- Balances are year-end values, not averages.
- EBITDA is the reported EBITDA if entered, otherwise EBIT plus depreciation and amortisation.
- Free cash flow = operating cash flow after interest paid and received − purchases of property, plant and equipment and intangible assets − repayments of lease liabilities. Acquisitions are not deducted.
- ROIC = EBIT × (1 − effective tax rate) ÷ (equity + financial debt + lease liabilities − cash).
- DuPont: ROE = net profit margin × asset turnover (net sales ÷ total assets) × equity multiplier (total assets ÷ equity).
- Working capital: DSO on net sales, DIO and DPO on cost of goods, 365 days.
- IFRS 16: net debt including leases ÷ reported EBITDA, and net debt excluding leases ÷ EBITDA after lease payments (repayment plus interest). The mixed view (debt without leases, EBITDA with leases) is shown only as a warning, because it understates leverage.

The model uses only classic functions that Excel 2016 and later and LibreOffice calculate in the same way. It contains no macros.

## Licence

CC BY 4.0, see [LICENSE](../LICENSE). You may share and adapt the model, also commercially, if you credit: Noel Walpert, noelwalpert.com. CC BY 4.0 applies only to the model: its structure, formulas, layout and texts. It does not apply to figures taken from documents of third parties, such as the annual reports of a company you enter, and no rights in these documents are granted.

## Disclaimer

This model is an illustration for educational and informational purposes. It describes reported figures and ratios derived from them. It is not investment, legal or tax advice and not a recommendation to buy or sell any security.
