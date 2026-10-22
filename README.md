# Magnet Link Converter

A single-page web app that converts between `.torrent` files and magnet links. Everything runs in the browser; files are never uploaded.

**Live site:** https://malsaalim.github.io/Magnet-Link-Convertir/

## Features

- **.torrent → magnet**: drop one or many `.torrent` files and get magnet links instantly. Supports v1, v2 and hybrid torrents (`btih` / `btmh`), multi-file torrents, trackers, and web seeds.
- **Magnet → details**: paste a magnet link (or a bare info hash) to see the name, size, trackers and hash in hex and base32, plus a cleaned, normalized link.
- **Magnet → .torrent**: fetches the metadata from WebRTC peers using [WebTorrent](https://webtorrent.io) and saves a `.torrent` file. Torrents seeded only by desktop clients may not respond; use a desktop client to export the file in that case.
- Optional list of public trackers you can add to any link.

## Run locally

It's one static file. Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
```

Only convert torrents you have the right to share.
