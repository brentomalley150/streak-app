# Beat the Slide — public site

**https://beattheslide.com** — currently a coming-soon page.

Everything here is **public**. Nothing founder-facing, internal, or strategic
belongs in this repo.

## Current state: pre-launch

`index.html` is a minimal coming-soon page — name, one line, email capture.
It deliberately reveals nothing about features, roadmap or timing.

The real marketing pages are written and waiting in `.staged/`:

| Staged file | Becomes |
|---|---|
| `.staged/landing.html` | `index.html` at launch |
| `.staged/prototype.html` | `prototype.html` |
| `.staged/story.html` | `story.html` |

### To launch

```bash
git mv .staged/landing.html index.html   # replaces the coming-soon page
git mv .staged/prototype.html .
git mv .staged/story.html .
```

Then re-add the nav links that were stripped when the site went dark, and push.

> Note: `.staged/` is still served by GitHub Pages — the files are only
> unlinked, not access-controlled. That's fine for marketing copy, but don't
> stage anything sensitive there.

## Where everything else lives

| What | Repo | URL |
|---|---|---|
| **Founders hub** — strategy, PRD, specs, prototypes, decks | `beat-the-slide-hub` (private) | https://brentomalley150.github.io/beat-the-slide-hub/ |
| **v2 app** | `streak-v2` | in development |
| **v1 app** — the live original | `declansummerlearning` (private) | https://beatthesummerslide.com |

> ⚠️ The founders hub repo is private, but **GitHub Pages serves it publicly**
> on this plan — private-repo access control needs GitHub Enterprise Cloud.
> The URL is unlisted (`robots.txt` + `noindex`), not protected.

## Before you add a page here

Would you be comfortable with a competitor, an investor, or a journalist
reading it? If not, it belongs in the hub repo.
