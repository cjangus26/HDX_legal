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

`manual/index.html` and the PDF are **generated** in the app repository
(`cjangus26/HDX_Inspect_V4`) by `docs/manual/build_user_manual.py` and copied
here. Edit the generator there, then copy the two outputs:

```sh
# in HDX_Inspect_V4
python docs/manual/build_user_manual.py \
  docs/HDX_Inspect_User_Manual.pdf docs/HDX_Inspect_User_Manual.html
cp docs/HDX_Inspect_User_Manual.html ../HDX_legal/manual/index.html
cp docs/HDX_Inspect_User_Manual.pdf  ../HDX_legal/manual/HDX_Inspect_User_Manual.pdf
```

The app opens the manual at **section anchors** (for example
`manual/#navigation` from the welcome tour, `manual/#reports` from the Reports
screen's help button). The anchors are stable names set in the generator; a
test in the app repository (`test/core/manual_links_test.dart`) checks that
every anchor the app uses exists in the generated page. Publish a regenerated
manual here **before or together with** the app release that links to new
anchors, otherwise those links land at the top of the page.
