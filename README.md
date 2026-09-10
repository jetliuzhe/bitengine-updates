# bitEngine Hub firmware updates

Static files served at `https://updates.bitengine.tech/hub/` via GitHub Pages.
bitEngine Hub gateways fetch `hub/manifest.json` when the user presses **Check for updates**,
then download the signed image it points to and verify the RSA-3072 signature before installing.

- `hub/manifest.json` — one version only; regenerated with `tools/make_manifest.py` in the firmware repo, never edited by hand.
- `hub/bitengine-v<version>.bin` — signed firmware images. Keep at least the previous version.

**Do not rename `hub/` or `manifest.json`** — the URL is compiled into every shipped gateway.
