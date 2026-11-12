# Monopoly Exchange — version 1.0

A complete single-file static website. No Wix, build tools, or paid hosting required.

## Get started

1. Open `index.html` in a browser for a quick look. Live exchange rates require internet access.
2. To publish: create a **public** GitHub repository named `monopoly-exchange`.
3. Use **Add file → Upload files** to upload `index.html` to the repository root.
4. Open **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, set the `main` branch and `/ (root)` folder, and save.
5. Your site URL will typically be `https://YOUR_USERNAME.github.io/monopoly-exchange/`.

## Edit colors

Inside `index.html`, find the CSS `:root` block near the top. Current theme:

- Green: `#184d33`
- Cream: `#f7f1db`
- Gold: `#dcb64f`
- Mint result card: `#e1ecd9`

## Edit the Monopoly benchmark

Find `USD_PER_500_MONOPOLY_DOLLARS = 0.40` in the script.

## Currencies

The app fetches an available-currency list from `https://api.frankfurter.dev/v2/currencies` automatically, and retrieves each non-USD currency's USD rate on demand. `STARTER_CURRENCIES` is a fallback list. Adding entries to that list does **not** guarantee the API has an exchange rate for them. Historical, fictional, and unsupported currencies require a separate data source.

## Limitations

- Monopoly money has no redeemable FX rate. This site uses a **chosen $0.40 per M500 valuation**, not an official central-bank quote.
- Real-world reference rates are updated periodically, not second-by-second.
- Internet is needed for non-USD conversions.
- This is an independent fan-made calculator and is not affiliated with Hasbro.
- GitHub Pages is public hosting. Do not put secrets or private API keys in `index.html`.
