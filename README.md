# GWCH LLC

Static site for GWCH LLC. Hosted on GitHub Pages at [gellhorn.co](https://gellhorn.co).

## Local

Open `index.html` in a browser or use a simple static server:

```bash
python3 -m http.server 8000
# or
npx serve
```

## Deploy (GitHub Pages + gellhorn.co)

1. **Create the repo on GitHub**  
   Create a new repository (e.g. `gellhorn-website` or `gellhorn.co`). Do not add a README, .gitignore, or license (this repo already has them).

2. **Push this project** (from the project root):

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   git push -u origin main
   ```

3. **Turn on GitHub Pages**  
   In the repo: **Settings → Pages**.  
   - Source: **Deploy from a branch**  
   - Branch: **main** (or **master**), folder: **/ (root)**  
   - Save.

4. **Set custom domain**  
   In **Settings → Pages**, under **Custom domain**: enter `gellhorn.co` and Save.  
   The `CNAME` file in this repo tells GitHub Pages to serve the site at gellhorn.co.

5. **DNS for gellhorn.co**  
   At your domain registrar (where you bought gellhorn.co):

   - **Option A – apex (gellhorn.co):**  
     Add **A** records:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`

   - **Option B – www only:**  
     Add a **CNAME**: `www` → `YOUR_USERNAME.github.io`

   After DNS propagates (minutes to 48 hours), the site will load at gellhorn.co.  
   Enabling **Enforce HTTPS** in Pages settings is recommended once the domain is active.

## Repo structure

- `index.html` – home + nav  
- `principles.html`, `current.html`, `past.html`, `future.html`, `extreme.html` – subpages  
- `styles.css` – styles  
- `images/` – images and logo  
- `CNAME` – custom domain for GitHub Pages
