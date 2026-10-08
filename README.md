# ValuMetrics: Financial Model & Valuation Suite

A single-file (`index.html`) browser app: open it in any modern browser, no build or server needed. Work auto-saves to the browser; use **Data → Backup** to export/import JSON.

## Sample company

The app ships with a realistic, fictional sample: **Vipin Corporation Ltd.**, an Indian mid-cap maker of industrial pumps, valves and motors (₹ crore, FY ends March).

- **Actuals FY2024 to FY2026:** revenue ₹2,140 to ₹2,688 Cr (11-13% growth), EBITDA margin 16.0% to 17.6%, PAT ₹280 Cr in FY26, ROE about 21%, near net-cash balance sheet.
- **Forecast FY2027E to FY2031E:** driver-based (growth fading 13% to 9%, gradual margin gains, steady working-capital days, capex about 5% of sales).
- **Market & cost of capital:** price ₹805, 6.3 Cr diluted shares, Rf 6.9% (10-yr G-sec), ERP 5.5%, beta 1.0, WACC 11.9%, terminal growth 6%.
- **Five fictional listed peers** (median 12.0x EV/EBITDA, 19.5x P/E).

With these inputs the DCF gives about ₹820/share (HOLD). Use **Data → Backup → Reset** to reload the sample if you have saved your own data.

## Choose your valuation approach

On first use (and anytime via the **🎯** header button) the investor picks how to value the company:

1. **Company profile** (optional): Stable, High-growth, Start-up / VC-backed, Bank / insurer, M&A, or Full institutional. Each profile pre-selects suitable methods.
2. **Methods**: tick any of DCF – FCFF, DCF – Exit multiple, DCF – FCFE, Scenario-weighted DCF, Peer comparables (choose EV/EBITDA, P/E, P/BV, EV/Sales or the average), and VC Method. Each card shows a live value per share.
3. **Headline target**: either one **primary** method, or a **blended** weighted average.

The headline target drives the recommendation, the Overview, the football field and the PDF report. Tabs for methods you didn't pick are hidden. The choice is saved with the model and included in the JSON backup.

## What it does

| Tab | Contents |
|---|---|
| Overview | KPIs, balance-sheet tie-out check, trend charts |
| Drivers | Per-year forecast assumptions (growth, margins, working-capital days, capex, debt) |
| P&L / Balance Sheet / Cash Flow | Linked 3-statement model: 3 actual + 5 forecast years; cash is the plug in driver mode |
| Ratios & Diagnostics | Margins, ROCE/ROE, leverage, liquidity, CCC, DuPont, Altman Z, earnings quality, ROIC vs WACC / EVA |
| DCF Valuation | CAPM WACC build-up, FCFF DCF (Gordon + exit-multiple cross-check), EV→equity bridge, FCFE cross-check |
| VC Method | Venture-capital (Sahlman) method: exit value, target IRR, dilution, pre/post-money, investor stake, IRR at CMP |
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

*For analytical / educational use only, not investment advice.*
