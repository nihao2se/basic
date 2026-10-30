# Document Maker

Free online tools: **CV Maker** (16 designs), **Student Card Maker** (10 designs, front and back) and **Urdu Document Maker** (Urdu / English applications and letters).

This is a static website (one `index.html` file). No server or build step is needed.

## Run online with GitHub Pages
1. Upload `index.html`, `README.md` and `.nojekyll` to the root of a GitHub repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
4. After 1–2 minutes the site is live at `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

Notes:
- Projects and drafts are saved in each visitor's own browser (localStorage), not on a server.
- PDF/PNG/JPG, QR and Word export load small libraries from cdnjs, so an internet connection is needed for those.
- Jameel Noori Nastaleeq and Nafees Nastaleeq must be installed on the computer or uploaded from the Fonts window.

## Admin password
The website opens with an **Admin login** screen. The password is not written in clear text anywhere in the files; only a salted, repeated SHA-256 hash is stored.

To change the password, open `set-password.html` in a browser, type the new password, and follow the 4 steps on that page (it only edits one line in `index.html`).

**Important – what this protects and what it does not:** this is a client-side password gate. It keeps casual visitors out, but because GitHub Pages is a public static host, anyone who downloads `index.html` can read the code, remove the lock, or guess a weak password offline. Use a long password (12+ characters). For real access control use a host with server-side login (for example Cloudflare Access, Netlify password protection, or your own server), or run the site only on your own PC.
