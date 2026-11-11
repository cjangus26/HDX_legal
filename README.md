# HDX legal

Public pages for the **HDX Inspect** app, served via GitHub Pages.

- [`index.html`](index.html) — Privacy Policy.
- [`manual/index.html`](manual/index.html) — User Manual (one web page with
  section anchors), with the PDF next to it:
  [`manual/HDX_Inspect_User_Manual.pdf`](manual/HDX_Inspect_User_Manual.pdf).

Once GitHub Pages is enabled (Settings → Pages → Deploy from a branch → `main` /
root), the pages are live at the URL shown in that Settings panel (a project
site's path is the repository name in its canonical casing):

| Page | URL |
| --- | --- |
| Privacy policy | `https://cjangus26.github.io/HDX_legal/` |
| User manual | `https://cjangus26.github.io/HDX_legal/manual/` |
| User manual (PDF) | `https://cjangus26.github.io/HDX_legal/manual/HDX_Inspect_User_Manual.pdf` |

The privacy policy URL goes into App Store Connect as the app's Privacy Policy
URL. The app links both pages from Settings → Help & about and from the
first-run screen.

## The user manual is generated, do not edit it here

`manual/index.html` and the PDF are generated from the app's sources and copied
here. Do not edit them by hand: changes are made in the generator and the two
files are replaced together.

The app opens the manual at **section anchors** (for example
`manual/#navigation` from the welcome tour, `manual/#reports` from the Reports
screen's help button). Publish a regenerated manual here **before or together
with** the app release that links to new anchors, otherwise those links land at
the top of the page.
