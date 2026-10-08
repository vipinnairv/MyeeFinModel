# ValuMetrics — Financial Model & Valuation Suite

A single-file (`index.html`) browser app: open it in any modern browser, no build or server needed. Work auto-saves to the browser; use **Data → Backup** to export/import JSON.

## What it does

| Tab | Contents |
|---|---|
| Overview | KPIs, balance-sheet tie-out check, trend charts |
| Drivers | Per-year forecast assumptions (growth, margins, working-capital days, capex, debt) |
| P&L / Balance Sheet / Cash Flow | Linked 3-statement model — 3 actual + 5 forecast years; cash is the plug in driver mode |
| Ratios & Diagnostics | Margins, ROCE/ROE, leverage, liquidity, CCC, DuPont, Altman Z, earnings quality, ROIC vs WACC / EVA |
| DCF Valuation | CAPM WACC build-up, FCFF DCF (Gordon + exit-multiple cross-check), EV→equity bridge, FCFE cross-check |
| VC Method | Venture-capital (Sahlman) method — exit value, target IRR, dilution, pre/post-money, investor stake, IRR at CMP |
| Analyst View | WACC×g sensitivity, bull/base/bear scenarios, football field, reverse DCF |
| Peer Comps | Peer multiples → implied price (EV/EBITDA, P/E, P/BV, EV/Sales) |
| Investment Thesis | Rating + narrative that feeds the PDF report |

**Report PDF** builds a multi-page research note (cover, statements, DCF, sensitivity, VC method, peers, conclusion) and opens the print dialog.

## VC Method

1. Exit value = exit multiple × exit-year metric (P/E on PAT, or EV/EBITDA / EV/Sales converted to equity via the exit-year net-debt bridge)
2. Post-money today = exit equity ÷ (1 + target IRR)^years
3. Required stake at exit = investment × (1 + IRR)^years ÷ exit equity; required stake today = that ÷ (1 − expected future dilution)
4. Post-money = investment ÷ stake today; pre-money = post-money − investment; ÷ diluted shares = value per share

Stage presets (Seed 60% … Pre-IPO 25%) and a "use peer median multiple" shortcut are provided. **IRR at CMP** shows the return from buying the whole company at today's market cap and exiting on the same terms.

*For analytical / educational use only — not investment advice.*
