# Deploying Peace4Paws to GitHub + Cloudflare Pages

This puts the site online for free, with fast global hosting and automatic SSL.
You'll do the clicking (I can't log in or create accounts for you), but every
step is below. Two routes: **A) GitHub repo** (best — gives you version history
and is what the future CMS needs) or **B) direct upload** (fastest, no GitHub).

Either way, the files you deploy are the 10 `.html` files in this folder.

------------------------------------------------------------------
## ROUTE A — GitHub + Cloudflare Pages  (recommended)
------------------------------------------------------------------

### Step 1 — Make a GitHub account & repo
1. Go to github.com and sign up (free) if you don't have an account.
2. Click the **+** (top right) -> **New repository**.
3. Name it `peace4paws-site`. Set it to **Public** (or Private — both work).
   Do NOT check "Add a README". Click **Create repository**.

### Step 2 — Upload the website files
1. On the new empty repo page, click **"uploading an existing file"**.
2. Drag in ALL 10 `.html` files from this folder (index.html, adopt.html,
   donate.html, foster.html, volunteer.html, about.html, stories.html,
   memorials.html, events.html, past-events.html).
   - Upload the `.html` files at the **top level** of the repo (not inside a
     subfolder), so the address ends up at the root.
3. Scroll down, click **Commit changes**.

### Step 3 — Connect Cloudflare Pages
1. Go to dash.cloudflare.com and sign up / log in (free).
2. In the left menu: **Workers & Pages** -> **Create** -> **Pages** tab ->
   **Connect to Git**.
3. Authorize Cloudflare to access your GitHub, then pick the `peace4paws-site` repo.
4. On the build settings screen:
   - **Framework preset:** None
   - **Build command:** (leave blank)
   - **Build output directory:** `/`
5. Click **Save and Deploy**. In ~1 minute your site is live at a URL like
   `peace4paws-site.pages.dev`.

### Step 4 (later) — Use your real domain peace4paws.org
Your domain is at GoDaddy. To point it at the new site:
1. In Cloudflare Pages -> your project -> **Custom domains** -> **Set up a domain**
   -> enter `peace4paws.org`.
2. Cloudflare will give you DNS records (or ask you to change nameservers at
   GoDaddy). Follow its on-screen instructions. SSL is automatic.
   - Tip: do this part when you're ready to switch the live site over, since it
     changes what visitors see at peace4paws.org.

### Updating the site after it's live (Route A)
Edit a file in the GitHub repo (pencil icon -> edit -> Commit), and Cloudflare
redeploys automatically within a minute. This is also what the future CMS hooks into.

------------------------------------------------------------------
## ROUTE B — Direct upload (fastest, skip GitHub)
------------------------------------------------------------------
1. dash.cloudflare.com -> **Workers & Pages** -> **Create** -> **Pages** ->
   **Upload assets**.
2. Name the project `peace4paws-site`.
3. Drag in the 10 `.html` files (or this whole folder). Click **Deploy**.
4. Live at `peace4paws-site.pages.dev`. Custom domain works the same as Step 4 above.

Downside of Route B: to update the site you re-upload files each time, and the
git-based CMS can't be added. Route A is better long-term.

------------------------------------------------------------------
## Notes
- The adoptable-dog feed needs the internet to load (it's pulling from
  Adopt-a-Pet live) — that's expected and works once the site is online.
- Keep `peace4paws-site-updated.zip` somewhere safe — it has the original photos
  and assets in `original-assets/` in case you ever need them.
- Cloudflare Pages free tier is plenty for a site like this.
