# Business Records Rebuild and Reconciliation

Rebuilt a full year of my tutoring business's records (19 clients, 158 payments) from unstructured notes into a structured, anonymised six-tab Excel workbook.

**This repository is documentation only.** The underlying records contain private client information, so no data or client-specific code is published.

## What it does
1. **Parse:** a Python parser converts free-text payment notes into clean rows, standardising mixed date formats, inferring missing years and anonymising client names
2. **Reconcile:** all 158 recorded payments reconciled to bank statements, then a three-way check per client (itemised payments vs recorded totals vs invoices), flagging any mismatch. The checks were tested on deliberate mismatches before use
3. **Model:** cleaned data feeds through Power Query into Excel Tables with structured references (XLOOKUP, MAXIFS, PivotTable cross-check)
4. **Analyse:** a billed-versus-collected view of outstanding amounts and collection timing, which identified several outstanding balances that I then followed up

The workbook refreshes with one click after the parser is re-run.

## Controls
- Worked on a copy and kept the original as a backup
- Re-checked totals before and after every refresh
- Learned to check formula dependencies before deleting a sheet

## How this was built
Parser code AI-drafted to my specification, then studied, tested and verified line by line by me.

**Author:** Luke Lipinski, BSc Accounting and Finance, Durham University · [LinkedIn](https://www.linkedin.com/in/lukelipinski)
