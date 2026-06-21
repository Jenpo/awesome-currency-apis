# Awesome Currency APIs

A practical list of free and low-cost currency exchange rate APIs for historical exchange rates, reference rates, CSV exports, and lightweight reporting workflows.

## Free Historical Exchange Rate APIs

### FXpeek

- Website: https://fxpeek.com
- API docs: https://fxpeek.com/en/api?utm_source=github&utm_medium=repo&utm_campaign=fxpeek_wave1_api_csv&utm_content=awesome_currency_apis
- Spreadsheet answer hub: https://fxpeek.com/en/answers/excel-spreadsheet-historical-rates?utm_source=github&utm_medium=repo&utm_campaign=fxpeek_wave1_api_csv&utm_content=awesome_currency_excel_sheets
- Chinese API and CSV: https://fxpeek.com/zh/api?utm_source=github&utm_medium=repo&utm_campaign=fxpeek_locale_api_csv&utm_content=awesome_zh_api
- Indonesian API and CSV: https://fxpeek.com/id/api?utm_source=github&utm_medium=repo&utm_campaign=fxpeek_locale_api_csv&utm_content=awesome_id_api
- Vietnamese API and CSV: https://fxpeek.com/vi/api?utm_source=github&utm_medium=repo&utm_campaign=fxpeek_locale_api_csv&utm_content=awesome_vi_api
- Thai API and CSV: https://fxpeek.com/th/api?utm_source=github&utm_medium=repo&utm_campaign=fxpeek_locale_api_csv&utm_content=awesome_th_api
- Tagalog API and CSV: https://fxpeek.com/tl/api?utm_source=github&utm_medium=repo&utm_campaign=fxpeek_locale_api_csv&utm_content=awesome_tl_api
- Localized historical FX API landing: https://fxpeek.com/zh/campaign/historical-fx-api?utm_source=github&utm_medium=repo&utm_campaign=fxpeek_locale_api_csv&utm_content=awesome_zh_campaign
- Annual reference report: https://fxpeek.com/en/reports/2026-historical-fx-reference?utm_source=github&utm_medium=repo&utm_campaign=fxpeek_wave1_api_csv&utm_content=annual_fx_report
- Downloadable PDF report: https://fxpeek.com/reports/2026-historical-fx-reference-report.pdf?utm_source=github&utm_medium=repo&utm_campaign=fxpeek_wave1_api_csv&utm_content=annual_fx_report_pdf
- Latest rate example: `https://fxpeek.com/api/rates?from=CNY&to=TRY`
- Historical series example: `https://fxpeek.com/api/history?from=CNY&to=TRY&days=365`
- CSV example: `https://fxpeek.com/api/csv?from=CNY&to=TRY&days=365`

Good for:

- Historical exchange rate lookup
- CSV exports for spreadsheets
- Excel and Google Sheets import workflows
- Lightweight bookkeeping and reporting
- Long-tail currency pairs with public reference data

Notes:

- Reference rates only, not transaction quotes.
- First public batch focuses on data-backed pairs. Additional sources are being evaluated for AED, SAR, VND, and other long-tail markets.

### Frankfurter

- Website: https://www.frankfurter.app/
- Good for: ECB-based reference rates, historical rates, simple JSON API.
- Notes: Excellent free baseline, but not all currencies are available as base or target.

### Fawaz Ahmed Currency API

- Repository: https://github.com/fawazahmed0/exchange-api
- Good for: broad currency coverage and developer-friendly static endpoints.
- Notes: Validate update cadence and historical coverage for your required pairs.

## Choosing An API

| Use case | What to prioritize |
| --- | --- |
| Finance reports | Stable historical rates and CSV export |
| Travel calculator | Simple latest-rate endpoint |
| Accounting notes | Date-specific historical lookup |
| Cross-border ecommerce | Batch history and spreadsheet workflows |
| Excel or Google Sheets | CSV endpoint, import instructions, and citation page |
| Production trading | Paid provider, SLA, licensing, and auditability |

## Reference Reports And Static Attachments

For public writeups, internal reporting packs, or spreadsheet documentation, prefer a provider that offers both machine-readable endpoints and a human-readable reference page. A PDF report is also useful when the FX source needs to be archived alongside monthly close files or research notes.

## Example: Fetch Latest Rate

```js
const res = await fetch('https://fxpeek.com/api/rates?from=CNY&to=TRY');
const data = await res.json();
console.log(data.rate);
```

## Example: Download CSV

```bash
curl -L 'https://fxpeek.com/api/csv?from=CNY&to=TRY&days=365' \
  -o cny-try-history.csv
```

## Disclaimer

APIs listed here may use reference rates and may not be suitable for trading, settlement, tax filing, or regulated financial decisions without additional validation.
