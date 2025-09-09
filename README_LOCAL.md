# Local Deployment Package

This folder contains your site cleaned for **local deployment**:
- Wayback toolbar and `_static/*` injections removed.
- All "Why Nobelium Hackers?" links now point to the local `why-nobelium-hackers.html`.
- The "Our Latest News / Blog" section is removed if it existed.
- Theme CSS/JS (including Wayback-proxied theme assets) are kept intact to preserve layout.

## How to deploy locally

**Option A — Just open in browser**
1. Unzip this package anywhere on your computer.
2. Double-click `index.html` to open it in your browser.
   - If some assets block due to CORS, use Option B.

**Option B — Run a tiny local server (recommended)**
- Using Python 3 (built-in on macOS/Linux/WSL; on Windows install Python from python.org):
  ```bash
  cd /path/to/unzipped-folder
  python -m http.server 8080
  ```
  Then open http://localhost:8080 in your browser.

**Option C — Deploy to GitHub Pages**
1. Create a new public repo and upload all files at the repo root.
2. Go to **Settings → Pages** and choose `main` + `/root`.
3. Wait ~1 minute; your site will be available at `https://<your-username>.github.io/<repo>/`.

## Notes
- If you need the "Why Nobelium Hackers" page styled identically to your theme, send me your preferred header/footer HTML/CSS and I will inline it into `why-nobelium-hackers.html`.
- If you want all images/CSS **fully offline** (no external hosts), provide the assets or allow me to fetch them and rewrite paths locally.