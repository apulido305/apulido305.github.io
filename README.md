# mrpulido.com

Central app hub for Mr. Pulido's study games. Live at https://mrpulido.com.

A single static page (`index.html`, no build step) served by GitHub Pages from `main`.

## Apps linked

| App | Live URL | Repo |
|---|---|---|
| Elemental Arcade | https://apulido305.github.io/elemental-arcade/ | [elemental-arcade](https://github.com/apulido305/elemental-arcade) |
| Spelling Flashcards | https://apulido305.github.io/spelling-flashcard-game/ | [spelling-flashcard-game](https://github.com/apulido305/spelling-flashcard-game) |
| Multiplication Practice | https://apulido305.github.io/multiplication-flashcard-game/ | [multiplication-flashcard-game](https://github.com/apulido305/multiplication-flashcard-game) |

## Adding an app

1. Copy an `<article class="tile">` block in `index.html` and change the link, text, `data-cat` and `data-keys`.
2. Add it to the `APPS` object in the script so the Quick CLI can launch it.
3. If it is a new subject, add a pill and sidebar button with a matching `data-filter`.

## Domain (Cloudflare DNS)

`CNAME` holds `mrpulido.com`. In Cloudflare DNS, set these records to **DNS only** (grey cloud) until GitHub issues the HTTPS certificate:

- `A` `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- `CNAME` `www` → `apulido305.github.io`

`design/` holds the original mockup (`code.html`, `screen.png`) and is not linked from the site.
