# Client site content

This repo holds one website's content: text, images and settings. The design
and code come from [lemon-real-estate-engine](https://github.com/Lemon-Grove-Mgmt/lemon-real-estate-engine),
which is combined with this repo when the site builds.

**Editing the site?** Go to `https://<your-site>/admin/` and sign in with
GitHub. See [EDITING.md](EDITING.md).

## Layout

```
site.config.json            technical settings (repo, live URL). Don't edit in the CMS.
content/settings/
  general.json              branding, colors, fonts, menu, footer
  home.json                 home page text and FAQ
  publishing.json           how changes go live
content/listings/*.md       one file per listing
content/categories/*.json   one file per category
content/pages/*.md          About, Privacy Policy, Terms, ...
public/uploads/             every image and file
public/                     anything else served as-is (robots.txt, favicon.ico)
```

## New client setup (for the site manager)

Run the `/real-estate-new-client` skill, or `scripts/new-client.sh`, in
[lemon-grove-ops](https://github.com/Lemon-Grove-Mgmt/lemon-grove-ops). It
creates this repo (private, in `Lemon-Grove-Mgmt`) and the Cloudflare Pages
project in the Lemon Grove account, fills in `site.config.json`, allows the
site in the shared sign-in Worker and records it in `clients.json`. The
engine's
[setup guide](https://github.com/Lemon-Grove-Mgmt/lemon-real-estate-engine/blob/main/docs/SETUP.md#adding-a-new-client)
covers the same steps by hand.

Then replace the demo content, or let the client do it in the editor.
