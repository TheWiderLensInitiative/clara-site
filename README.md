# clara-site

The public website for **Clara** — [clara.thewiderlens.info](https://clara.thewiderlens.info).

Static single-page site (no build step, no framework). Served routes:

| Path       | File           | What it is                                   |
|------------|---------------|-----------------------------------------------|
| `/`        | `index.html`   | Landing page: features, video, screenshots, getting-started guide, requirements, download, FAQ |
| `/privacy` | `privacy.html` | Privacy policy — mirrors `docs/PRIVACY.md` in the [clara](https://github.com/TheWiderLensInitiative/clara) repo (rewrites via `vercel.json`) |

`assets/` holds the logo files and the Play Store phone screenshots (copied from
`fastlane/metadata/android/en-US/images/phoneScreenshots/` in the main repo).

## Deploying

The Vercel project `clara` (team "The wider lens") deploys this directory to
production. Push to `main`, then deploy — currently done via the Vercel API as a
static deployment of this folder.

## Conventions

- The `#download` anchor on the landing page must keep working: the PC
  installer's QR code and the `clara app` command both point at
  `https://clara.thewiderlens.info/#download`, and it must open the download
  and install steps.
- The download button always points at
  `https://github.com/TheWiderLensInitiative/clara/releases/latest` — never at
  a versioned release.
- `/privacy` must stay in step with `docs/PRIVACY.md` in the main repo.
- Credit line: "Created by DevIgnite × The Wider Lens Initiative Project".

## License

Apache-2.0. Created by DevIgnite × The Wider Lens Initiative Project.
