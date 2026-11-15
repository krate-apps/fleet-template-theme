# fleet-template-theme

Minimal Fleet appearance pack template (`fleet.theme.yaml` + CSS tokens).

**Repository:** [krate-apps/fleet-template-theme](https://github.com/krate-apps/fleet-template-theme)

## Docs

- [Themes](https://github.com/krate-apps/fleet/blob/main/docs/user/themes.md)
- [theme.schema.json](https://github.com/krate-apps/fleet/blob/main/docs/developer/schemas/theme.schema.json)
- [Publishing](https://github.com/krate-apps/fleet/blob/main/docs/developer/publishing-extensions.md)
- [Create a bucket](https://github.com/krate-apps/fleet/blob/main/docs/developer/create-bucket.md)

## Quick start

1. Copy this tree to a new repo (for example `fleet-theme-mylook`).
2. Change `id` / `name` / `uiThemeId` in `fleet.theme.yaml`.
3. Update `:root[data-fleet-theme="…"]` in `theme.css` to match `uiThemeId`.
4. `make pack`

```text
fleet-template-theme/
  fleet.theme.yaml
  theme.css
  scripts/pack.sh
  Makefile
  LICENSE
```

## Pack / publish

```bash
make pack   # dist/<id>-linux-amd64.tar.gz + dist/SHA256SUMS
```

Tag `v*` to run `.github/workflows/release.yml` (uploads the archive + `SHA256SUMS`).

Pin the Official (or community) bucket listing with [`fleet-bucket-action/pin`](https://github.com/krate-apps/fleet-bucket-action).

## License

MIT — Copyright (c) 2026 Krate.

---

<p align="center">
  Developed by the <a href="https://runkrate.com">Krate</a> team.<br />
  Released under the MIT License.
</p>
