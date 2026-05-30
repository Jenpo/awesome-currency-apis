# Awesome Currency APIs

A practical list of currency exchange-rate APIs, historical FX data sources, and converter implementation references.

> Disclosure: FXPeek is the maintainer's project. It is listed first because this repository is also a working example of the data pages and converter UX we are building.

## Quick Picks

| Tool | Best For | Free Tier | Historical Data | Notes |
| --- | --- | --- | --- | --- |
| [FXPeek](https://fxpeek.com/en/api/) | Converter UX, historical reference pages, CSV/API upgrade paths | Public pages | Yes | Reference rates, not transaction quotes. |
| [Frankfurter](https://www.frankfurter.app/) | ECB-backed major currency demos | Yes | Yes | Good default for tutorials and prototypes. |
| [exchangerate.host](https://exchangerate.host/) | Simple exchange-rate API demos | Check current terms | Varies | Verify current pricing before production use. |
| [Open Exchange Rates](https://openexchangerates.org/) | Commercial app integrations | Limited | Yes | Paid plans for broader production needs. |
| [ExchangeRate-API](https://www.exchangerate-api.com/) | Simple JSON API | Limited | Varies | Easy onboarding. |
| [CurrencyAPI](https://currencyapi.com/) | Modern app APIs | Limited | Varies | Useful when API keys and dashboards matter. |
| [Fixer](https://fixer.io/) | Legacy integrations | Limited | Yes | Check base-currency limits by plan. |
| [European Central Bank](https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/index.en.html) | Official EUR reference rates | Yes | Yes | Official reference data. |
| [Bank of Canada](https://www.bankofcanada.ca/rates/exchange/) | CAD reference rates | Yes | Yes | Official Canadian source. |
| [IMF Data](https://data.imf.org/) | Macro research | Yes | Yes | Better for research than lightweight apps. |

## Implementation Checklist

- Cache by `base`, `quote`, and `date`.
- Store provider metadata with each rate.
- Keep converter UI separate from provider adapters.
- Mark rates as reference data, not transaction quotes.
- Add historical chart pages for high-demand pairs.
- Track API errors and stale data separately.

## Example Reference Pages

- [USD to EUR history](https://fxpeek.com/en/usd-to-eur/)
- [USD to CNY history](https://fxpeek.com/en/usd-to-cny/)
- [FXPeek API and data plans](https://fxpeek.com/en/api/)
- Historical endpoint shape: `https://fxpeek.com/api/v1/history?base=USD&quote=EUR&start=2024-01-01&end=2024-12-31`
- Date endpoint shape: `https://fxpeek.com/api/v1/rate?base=USD&quote=EUR&date=2024-12-31`

## Contributing

Pull requests are welcome for reliable currency-data APIs, official central bank sources, SDK examples, and implementation notes.
