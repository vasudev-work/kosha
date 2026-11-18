# KOSHA

A reading room for Indian open source. Neo-brutalist on purpose: thick borders, hard
shadows, slanted chips, no rounded corners, no gradients.

Live: https://vasudev-work.github.io/kosha/

## Where the data comes from

Not here. `data/apps.json` is built and validated by
[swadeshi-gh-store](https://github.com/vasudev-work/swadeshi-gh-store) from public
GitHub Releases, and this repo copies it on a schedule (`sync.yml`). One source of
truth, two faces.

## What it shows

- **118 apps**, **Android, Windows, macOS and Linux**
- Platform picker in the header, slanted chips for platform, multi-platform, Kotlin and Java
- Sort by stars, recently updated, A-Z or size
- **Surprise me** opens a random app
- App sheet lists **every build for every platform** with its real file size, plus the
  repository, the release and a copy button for `owner/repo`
- `/` focuses search, `Esc` closes sheets
- Icons are the launcher PNG already committed in each repo; a letter tile when the repo
  only ships a vector icon

## What it does not do

- No download is hosted here. Every link goes to the developer's own GitHub Release.
- No ratings, no reviews, no "featured" slots, no sponsored placement.
- No accounts, no cookies, no analytics, no fonts or scripts from a CDN.
- No invented numbers. Stars, licence and size are what GitHub reports.

## Run it

```
python3 -m http.server 8000
# http://localhost:8000
```

`data/apps.json` is fetched over HTTP, so the folder has to be served, not opened from disk.

MIT.
