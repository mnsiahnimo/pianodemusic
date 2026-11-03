# Pianode Music — pianodemusic.com

Quarto website for Pianode Music (YouTube: [@nimopianode](https://www.youtube.com/@nimopianode)).
Black-and-ivory "piano key" theme with a gold accent.

## Pages

| File | Page |
|---|---|
| `index.qmd` | Home — hero, what you'll find, latest YouTube uploads |
| `watch.qmd` | Latest uploads player + playlist cards |
| `lessons.qmd` | Teaching approach + membership tiers (placeholders) |
| `about.qmd` | Channel bio + "My story" |
| `contact.qmd` | Email, YouTube, optional Formspree form |
| `styles.scss` | Colours, fonts, layout |
| `_quarto.yml` | Navbar, footer, site settings |
| `CNAME` | Custom domain: pianodemusic.com |
| `.github/workflows/publish.yml` | Auto-build and publish on every push |

The "Latest uploads" player updates itself — it pulls the channel's uploads list
(`UUnNo5PX8OyuxQ9YpwlBf-yg`), so new videos show up without editing the site.

## Things to fill in

Search the files for `[TO BE SUPPLIED` and `PLAYLIST_ID_HERE`:

- **watch.qmd** — playlist titles, descriptions and IDs (instructions are in a comment at the top of the playlist section)
- **lessons.qmd** — membership tier name, price, what's included, and the join link
- **about.qmd** — photo and "My story"
- **contact.qmd** — email address (and Formspree ID if you want the form)

## Publish on GitHub Pages

1. Create a new repo (e.g. `pianodemusic`) and push these files to the `main` branch.
2. Repo **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. The workflow builds and publishes automatically on each push.
4. **Settings → Pages → Custom domain:** `pianodemusic.com`, then tick **Enforce HTTPS** once it's offered.
5. At your domain registrar, add DNS records:
   - `A` records for `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` for `www` → `<your-github-username>.github.io`

Preview locally: `quarto preview`

## Paid lessons and subscriptions

GitHub Pages only serves static pages — it can't take payments, log people in,
or lock videos behind a paywall. The usual setup is: keep this site as the front
door, host the paid course on a course platform, and point the **Join** button on
`lessons.qmd` to it. Options to compare: Teachable, Thinkific, Kajabi, Podia,
Patreon (members-only videos), or Gumroad. Many let you use a subdomain such as
`learn.pianodemusic.com`, which keeps everything under your brand.
