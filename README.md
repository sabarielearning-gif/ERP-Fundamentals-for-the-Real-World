# Standalone Audiobook Web Player

A lightweight, high-performance HTML5 audiobook player for **ERP Fundamentals for the Real World**.

---

## What is Inside
* `index.html`: Fully self-contained audio player with auto-play, 15s rewind / 30s forward, variable speed playback (`0.75x` to `2.0x`), mobile lock-screen MediaSession support, and continuous sequential playback.
* `cover.jpg`: High-resolution 2400 x 2400 square cover art.
* `ERP_Fundamentals_Audiobook_Companion.pdf`: The official 23-page companion visual reference document.

---

## How to Deploy as a Standalone Site (Not Mixed with Your Portfolio)

### Option A: Deploy to a Separate Vercel Project (Recommended)
You can deploy this folder as its own dedicated project on Vercel (e.g., `erp-audiobook.vercel.app`):
1. In Terminal:
   ```bash
   cd /Users/smohhan/Books/erp-fundamentals-for-newcomers/audiobook_player
   npx vercel
   ```
2. Follow prompts:
   - *Set up and deploy?* **Y**
   - *Which scope?* Select your personal account
   - *Link to existing project?* **N**
   - *Project name?* `erp-audiobook` (or any custom name)
3. Instant result: You get a clean, standalone URL like `https://erp-audiobook.vercel.app` that is completely separate from your main portfolio.

### Option B: Deploy with Netlify Drop (Zero Commands)
1. Open [app.netlify.com/drop](https://app.netlify.com/drop) in your browser.
2. Drag and drop the `audiobook_player` folder into the browser window.
3. It goes live instantly with a free standalone URL like `https://erp-audiobook-sample.netlify.app`.

---

## How to Stream from Google Drive

If you want to stream audio files hosted in your Google Drive folder:
1. In Google Drive, make sure each MP3 is set to **"Anyone with the link can view"**.
2. Right-click an MP3 $\rightarrow$ **Copy link**. The link will look like:
   `https://drive.google.com/file/d/1A2b3C4d5E6f7G.../view?usp=sharing`
   The string between `/d/` and `/view` is the **File ID** (`1A2b3C4d5E6f7G...`).
3. Open `index.html` and paste the ID into the `driveId` field in the `TRACKS` array:
   ```javascript
   { id: 1, num: "01", title: "ERP: The Shared Brain of a Business", duration: "18:03", driveId: "1A2b3C4d5E6f7G...", ... }
   ```
4. Save and push. The player will stream directly from Google Drive with zero login required for your listeners!
