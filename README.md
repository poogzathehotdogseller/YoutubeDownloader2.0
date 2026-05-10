<div align="center">

# 🎯 YouTube Downloader

**Direct video & audio download from YouTube on GitHub — no software installation required**

</div>

---

## 📖 Table of Contents

- [✨ Features](#-features)
- [📘 Step-by-Step Guide](#-step-by-step-guide)
- [🎮 Download Modes](#-download-modes)
- [⚙️ Advanced Settings](#️-advanced-settings)
- [🧩 Managing Split Files](#-managing-split-files)

---

## ✨ Features

- 🎬 **4 download modes:** Single video, Playlist, Channel, Search
- 🎵 **Output formats:** MP4 for video or MP3 for audio, with desired quality
- 📊 **Auto indexing:** Generates a Markdown file with detailed info for all videos
- 🛜️ **Thumbnails:** Automatically fetched for each video
- ✂️ **Smart file splitting:** If output size exceeds limit, automatically split into parts
- 💯 **Completely free:** No API keys or extra registration needed

---

## 📘 Step-by-Step Guide

### 1. Log in to GitHub

- Go to [GitHub](https://github.com) and log in to your account.

### 2. Fork the Project

1. Go to the project's main page on GitHub.
2. Click the **Fork** button (top-right).
3. Choose a name for your new repository.
4. Click **Create fork**.

### 3. Configure Permissions

> ⚠️ **This step is critical.** Without it, no files will be saved to your repository.

- Go to your forked repository.
- Navigate to **Settings > Actions > General**.
- Under **Workflow permissions**, select **Read and write permissions** and click **Save**.

### 4. Enable Actions

- Go to the **Actions** tab in your repository.
- Click **"I understand my workflows, go ahead and enable them"**.

### 5. Run the Downloader

1. In the **Actions** tab, click on **🎯 YouTube Downloader** in the sidebar.
2. Click the **Run workflow** button.
3. Fill out the form:

| Field | Description | Example |
|---|---|---|
| 🔄 Download Mode | `single`, `playlist`, `channel`, `search` | `single` |
| 🎬 URL or Search Query | Video/playlist/channel link or search term | `https://youtu.be/...` |
| 📦 Output Type | `video` or `audio` | `video` |
| 🎚️ Quality | Output quality (e.g., `720` for video) | `720` |
| 🔢 Max results | Max number of results (for playlist, channel, search) | `10` |
| 📦 Split > MB | Split files larger than this size (0 = no split) | `50` |

4. Click **Run workflow** and wait for the process to complete.

---

## 🎮 Download Modes

### 1. Single Video (`single`)
Download a single video or its audio.

### 2. Playlist (`playlist`)
Download all videos in a playlist.  
Additional features:
- Full index file (`Index.md`) with detailed info
- Separate `info` file for each video

### 3. Channel (`channel`)
Fetch the latest videos from a channel. Supports:
- Full channel link
- `@ChannelName`
- Just the channel name

### 4. Search (`search`)
Search for a term and save the result list in a Markdown file.  
> Note: Videos are **not** downloaded in this mode — only their information is saved.

---

## ⚙️ Advanced Settings

### 🎚️ Quality

| Output Format | Supported Qualities |
|---|---|
| Video (MP4) | `144`, `360`, `480`, `720`, `1080` |
| Audio (MP3) | `128`, `192`, `320` |

### ✂️ Split Threshold

| Value | Result |
|---|---|
| `0` | File is never split |
| `50` | Files larger than 50MB are split into 50MB chunks |
| `90` | Split threshold set to 90MB |

### 🔢 Max Results

Number of videos processed in playlist, channel, or search modes.

---

## 🧩 Managing Split Files

If a file exceeds the set threshold, it is split into multiple compressed parts:

```
video.mp4.zip
video.mp4.z01
video.mp4.z02
video.mp4.z03
```

**How to extract:**

- **Windows:** Place all parts in one folder, right-click the `.zip` file, and select **Extract All...**.

---
