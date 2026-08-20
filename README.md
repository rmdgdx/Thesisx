# ThesisBrainPH

**Your second brain, trained to think like a researcher.** An offline, subscription-based thesis-writing app for Filipino students. You bring the idea and the details; ThesisBrainPH builds the title, variables, statistics, research framework, and a complete five-chapter draft — no formatting, no server, no internet.

> ⚠️ The subscription check in this build is **client-side only** and is not secure for real payments. Harden it before charging users (see [Going live](#going-live)).

## Files

```
thesisbrainph/
├── index.html   # Landing page (marketing) — served as the homepage
├── app.html     # The app itself (offline, single file)
├── README.md
├── LICENSE
└── .gitignore
```

## Run it

Open `app.html` in any modern browser — it runs 100% offline. On the paywall, click **Try the free demo** or enter the demo code:

```
THESIS-DEMO
```

## What it does

- Turns a short form (topic, variables, respondents, study type) into five suggestions: **title, variables, research methods, statistical treatment, and a visual research framework**.
- Auto-drafts the **Philippine 5-chapter format** — Chapter 1 fully written (intro, background, 5-item statement of the problem, null + alternative hypotheses, significance, scope, definition of terms), Chapter 2 (per-term literature + framework diagram), Chapter 3 (full methodology), and guidance for Chapters 4–5.
- Adapts to **Quantitative, Qualitative, Mixed, Experimental, and Developmental** studies — including engineering **software** (ISO/IEC 25010), **hardware** (engineering design process), and **optimization** (Design of Experiments) tracks.
- Works offline, stores nothing online, and exports a `.json` backup or prints to PDF.

## Deploy (GitHub Pages)

1. Push this repo to GitHub.
2. **Settings → Pages → Deploy from a branch → `main` / root**.
3. Your site goes live at `https://<your-username>.github.io/thesisbrainph/` — visitors land on the marketing page, which links to the app.

The app still runs fully offline once loaded. To make it installable (PWA) or wrap it for the app stores, add a `manifest.json` + service worker, or use a WebView shell (Capacitor/Cordova) with store billing.

## Going live

The bundled activation check accepts any `XXXX-XXXX` code and can be bypassed. For real revenue, replace it with **signed, expiring license tokens** (verify an Ed25519/JWT token against a bundled public key so it still works offline), or use **Google Play / App Store billing** if you publish through a wrapper. Confirm payment handling and Data Privacy Act (RA 10173) obligations with the right professionals first.

## Notes

- Single-file, vanilla HTML/CSS/JS. No frameworks, no dependencies, no network calls.
- ThesisBrainPH is a writing aid, not a substitute for a research adviser. Every `[bracket]` must be replaced and every source cited by the student.

## License

See [`LICENSE`](LICENSE) — All Rights Reserved by default (swap for MIT/Apache if you'd rather open-source it).
