# Hub Demo — MJS Company Limited

Demonstration copy of the **Safety Hub** and **Service Hub**, for sales presentations.

- Live at **https://marcusappdev.github.io/HubDemo/** (Service Hub: `/HubDemo/service/`)
- Signs in with the Entra app **Hub Demo** (Concept Group tenant)
- Reads and writes the `MJS_` lists on `https://conceptcompg.sharepoint.com/sites/MJSDemo`
- Every name, customer, incident and number on that site is fictional. It is loaded by
  `Populate-Demo.ps1` in the setup kit (v2.3.2 or later). Re-run it — Clear, then Load — on the
  morning of a presentation so the dates are current.

## How this repo relates to `marcusappdev/MJE`

The code is a copy of `marcusappdev/MJE`. Only these files differ, and they must be kept when
newer code is copied across:

| File | Why it differs |
|---|---|
| `shared/mje-config.js` | Hub Demo client ID, `/sites/MJSDemo`, `MJS_` prefix, MJS company name, both Hubs "on" |
| `shared/mjs-logo.png`, `mjs-logo-full.png`, `mjs-icon.png` | Fictional MJS logo — no MJ Electrical artwork |
| `README.md` | This file |

To update the demo after changes to MJE: copy `index.html`, `service/` and `shared/` (except
`mje-config.js`) from `marcusappdev/MJE`, leave out the `mje-*.png` logos, and keep the files above.

## Rules

- Public repo: never put real register data, customer names or exports here.
- The demo uses its own phone storage (offline queue, timer, saved jobs), so it never mixes with the
  MJE Hubs even though both run on `marcusappdev.github.io`.
