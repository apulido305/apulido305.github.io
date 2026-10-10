# mrpulido.com

Central app hub for Mr. Pulido's study games. Live at https://mrpulido.com.

A single static page (`index.html`, no build step) served by GitHub Pages from `main`.

This repo is the GitHub user site (`apulido305.github.io`), so its custom domain also applies to every
project Pages site on the account: a repo `foo` with Pages turned on is served at `mrpulido.com/foo/`.

## Apps linked

| App | Live URL | Repo |
|---|---|---|
| Elemental Arcade | https://mrpulido.com/elemental-arcade/ | [elemental-arcade](https://github.com/apulido305/elemental-arcade) |
| Spelling Flashcards | https://mrpulido.com/spelling-flashcard-game/ | [spelling-flashcard-game](https://github.com/apulido305/spelling-flashcard-game) |
| Multiplication Practice | https://mrpulido.com/multiplication-flashcard-game/ | [multiplication-flashcard-game](https://github.com/apulido305/multiplication-flashcard-game) |

## Adding an app

1. Turn on GitHub Pages in the app's repo; it appears at `mrpulido.com/<repo-name>/`.
2. Copy an `<article class="tile">` block in `index.html` and change the link (`/<repo-name>/`), text, `data-cat` and `data-keys`.
3. Add it to the `APPS` object in the script so the Quick CLI can launch it.
4. If it is a new subject, add a pill and sidebar button with a matching `data-filter`.

## Domain (Cloudflare DNS)

`CNAME` holds `mrpulido.com`. In Cloudflare DNS, set these records to **DNS only** (grey cloud) until GitHub issues the HTTPS certificate:

- `A` `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- `CNAME` `www` → `apulido305.github.io`

`design/` holds the original mockup (`code.html`, `screen.png`) and is not linked from the site.
