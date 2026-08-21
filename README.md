

# 🎥 Social Media Video Downloader

A lightweight FastAPI-based web API that allows you to download videos from various platforms such as **YouTube**, **TikTok**, **Facebook**, **Instagram**, **Twitter**, and more. This API uses the powerful `yt-dlp` tool to fetch videos and streams them directly to the client without storing them on the server. Perfect for integration with mobile apps, web clients, or educational tools.

---

## ✅ Features

- 🚀 FastAPI-based RESTful API
- 🎞️ Download videos from YouTube and many social media sites
- 🎚️ Select video resolution (360p, 720p, 1080p, etc.)
- 🧾 Video filename auto-renamed to original title
- 📥 Streams videos directly to the browser/download manager
- 📱 Ready for frontend and mobile (Flutter, React, etc.)
- ☁️ Works with free hosting platforms like Glitch, Render, Railway

---

## 📦 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yasirali646/social-media-video-downloader.git
   cd social-media-video-downloader
   ```
2. Install Dependencies (Using uv)
    ```bash
    uv venv
    source .venv/bin/activate  # or .venv\Scripts\activate on Windows
    uv add fastapi uvicorn yt-dlp python-multipart python-dotenv
3. Run the App
    ```bash
    uvicorn main:app --host 0.0.0.0 --port 8000 --reload
    ```

## 🧪 Usage

#### HTML Form

``` 
<form action="/download" method="get">
  <input name="url" placeholder="Enter video URL" required />
  <select name="format">
    <option value="best[height<=360]">360p</option>
    <option value="best[height<=720]">720p</option>
    <option value="best[height<=1080]">1080p</option>
  </select>
  <button type="submit">Download</button>
</form>
```

### API Request

``` 
GET /download?url=https://www.youtube.com/watch?v=dQw4w9WgXcQ&format=best[height<=720]
```

### Demo

![Demo](demo.gif)


## ✅ Supported Platforms

This project supports video downloads from the following platforms (and more):

- YouTube
- TikTok
- Instagram
- Facebook
- Twitter (X)
- DailyMotion
- Vimeo
... and many more!
> See the full list: <a href="https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md" target="_blank">yt-dlp Supported Sites</a>

## ⚠️ Disclaimer
This project is intended for <b>educational purposes only</b>. Downloading copyrighted material without permission may violate local laws and platform policies. Use responsibly.
