# Magnet Link Converter

A single-page web app for torrents and magnet links. Everything runs in the browser.

**Live site:** https://malsaalim.github.io/Magnet-Link-Convertir/

## Features

- **Stream**: paste a magnet link and play its video or audio files in the page while they download.
- **Download**: fetch any file in the torrent and save it. Files are held in memory until saved, so very large files (over ~2 GB) may fail, especially on phones.
- **Direct links**: when a torrent has a web seed, each file gets a normal https:// link anyone can download from.
- **.torrent → magnet**: drop one or many `.torrent` files and get magnet links instantly (v1, v2 and hybrid).
- **Save .torrent**: once a magnet link's metadata arrives, save it as a `.torrent` file.
- **Log in / Sign up**: email and password accounts through Supabase, with password reset.

Streaming and downloads use [WebTorrent](https://webtorrent.io), which can only reach peers running in browsers (WebRTC) and web seeds. Torrents shared only by desktop clients won't load in a web page.

## Switching on accounts

Accounts stay off until you add Supabase keys to `config.js`:

1. Create a free project at [supabase.com](https://supabase.com).
2. Open **Project Settings → API**. Copy the **Project URL** and the **anon public** key into `config.js`.
3. Open **Authentication → URL Configuration** and set **Site URL** to `https://malsaalim.github.io/Magnet-Link-Convertir/`.
4. Commit. The site picks up the change within a minute.

## Run locally

```sh
python3 -m http.server 8000
```

Then open http://localhost:8000. Only stream, download or share torrents you have the right to.
