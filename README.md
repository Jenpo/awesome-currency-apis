# Awesome Currency APIs

A practical list of free and low-cost currency exchange rate APIs for historical exchange rates, reference rates, CSV exports, and lightweight reporting workflows.

## Free Historical Exchange Rate APIs

### FXpeek

- Website: https://fxpeek.com
- API docs: https://fxpeek.com/en/api?utm_source=github&utm_medium=repo&utm_campaign=fxpeek_wave1_api_csv&utm_content=awesome_currency_apis
- Latest rate example: `https://fxpeek.com/api/rates?from=CNY&to=TRY`
- Historical series example: `https://fxpeek.com/api/history?from=CNY&to=TRY&days=365`
- CSV example: `https://fxpeek.com/api/csv?from=CNY&to=TRY&days=365`

Good for:

- Historical exchange rate lookup
- CSV exports for spreadsheets
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
| Production trading | Paid provider, SLA, licensing, and auditability |

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
