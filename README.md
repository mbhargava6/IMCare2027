# IMCare website

The public website for IMCare — Internal Medicine specialists in Port Hope, Ontario.

Built with [Jekyll](https://jekyllrb.com), which GitHub Pages builds and hosts
automatically. There is no build step to run and no Actions workflow to
maintain: **push to `main` and the site updates.**

## How it fits together

| Folder | What's in it |
| --- | --- |
| `_data/` | **All the content that changes.** Team, services, patient tools, testimonials, phone numbers, address. Plain YAML — safe to edit. |
| `*.md` | One file per page. Front matter (between the `---` lines) sets the title and intro; the rest is the page text. |
| `_layouts/` | Page skeletons. Only touch these to change page *structure*. |
| `_includes/` | Reusable pieces — header, footer, call-to-action band, icons. |
| `assets/css/style.css` | The entire stylesheet. Colours are CSS variables at the top. |
| `assets/js/main.js` | Mobile menu and the Patient Tools search. The site works without it. |
| `assets/pdf/` | Patient handouts, referral form, privacy policy. |
| `images/` | Logo, team photos (640×640), page images. |

**Start with [EDITING.md](EDITING.md)** — it covers the everyday jobs
(add a team member, add a handout, change the phone number) step by step.

## Changing the colour scheme

One line, in `_data/site.yml`:

```yaml
palette: crimson    # or: clinical
```

`crimson` keeps IMCare's existing brand colour. `clinical` is a calmer
blue-green. Both are defined in `assets/css/style.css`.

## Running it locally (optional)

You do not need this to make changes — GitHub builds the site for you. But if
you want a local preview:

```bash
bundle install
bundle exec jekyll serve
# open http://localhost:4000
```

Requires Ruby 3.x and Bundler.

## Going live on imcare.ca

The site currently deploys to the GitHub Pages URL for this repository. To move
`www.imcare.ca` over:

1. **Settings → Pages** in this repo — confirm the source is `main` / root and
   the build is green.
2. Add a file named `CNAME` at the top level of this repo containing exactly:
   `imcare.ca`
3. Remove the `CNAME` file from the old `imcare-canada.github.io` repo (a
   custom domain can only be claimed by one repository at a time).
4. In **Settings → Pages → Custom domain**, enter `imcare.ca` and tick
   **Enforce HTTPS** once the certificate is issued (usually a few minutes).
5. DNS stays as it is — it already points at GitHub Pages.

Do steps 2 and 3 close together; between them the domain will not resolve.

## Notes

- `assets/pdf/pace_180.pdf` is carried over from the previous site but is not
  linked from any page. It is kept so existing direct links keep working.
- See [CONTENT-REVIEW.md](CONTENT-REVIEW.md) for the short list of wording that
  was added or corrected during the rebuild and should be checked.
