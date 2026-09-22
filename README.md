# Sydney Family Pressure Explorer

Standalone static version of the interactive Sydney household pressure calculator.

## Run locally

Just open `index.html` in a browser. There is no build step, backend, package manager or database.

## Publish on GitHub Pages

1. Create a new GitHub repository.
2. Upload `index.html` and `.nojekyll` to the repository root.
3. Commit them to the `main` branch.
4. In GitHub: **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select `main` and `/ (root)`, then save.

The same folder can also be deployed directly to GitLab Pages, Netlify, Cloudflare Pages or any ordinary static web host.

## Important model notes

- All calculations run in the browser; the site sends no household data anywhere.
- Mortgages are fully amortising principal-and-interest loans.
- The 2026 house price is translated to earlier eras using median Sydney house-price ratios.
- Individual salaries are translated using historical male/female full-time earnings ratios and then taxed separately under the modelled tax rules for the era.
- **Same effort** keeps work utilisation fixed through time.
- **Historical second-earner** scales Person 2's selected 2026 utilisation by the model's historical work-intensity calibration. That effective utilisation drives both second-earner income and childcare hours.
- School fees are translated backwards using an ABS Education CPI-based scaler. The 1985 point uses a lower-confidence bridge to the older CPI structure.
- Childcare is a transparent proxy based on overlap in paid work, fee assumptions and subsidy approximations.

This is a normalised household-pressure model, not a forecast and not a claim that every household had the modelled circumstances.

## Files

- `index.html` — complete application; no dependencies.
- `.nojekyll` — prevents GitHub Pages from applying Jekyll processing.
