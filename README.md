# status.hesh.am

A status page for my head. Migraine attacks logged in [Ease](https://hesh.am/apps/ease)
show up as incidents, in the style of a service status page.

- **Hosting:** GitHub Pages from this repo, `CNAME` → `status.hesh.am`. Deploys on push.
- **Data:** `index.html` fetches the `publicStatus` Cloud Function in the Ease
  Firebase project (`Firebase/functions/status.js` in the Ease repo). The function
  is fixed to one account and publishes only catalog values: no notes, no custom
  entries, no location.
- **Local preview:** `python3 -m http.server 4000`, then open
  `http://localhost:4000/?data=/sample.json` to use a saved feed instead of the live one.
