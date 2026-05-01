# Sharitta Marshall — Portfolio Site

## Files in this folder
```
sharittamarshall-portfolio/
├── index.html       ← the entire website (one file)
├── railway.toml     ← Railway deployment config
├── package.json     ← tells Railway how to serve the site
├── assets/          ← CREATE this folder and add your files
│   ├── sharitta-hero.jpg            ← hero section photo
│   ├── sharitta-about.jpg           ← about section photo
│   └── sharitta-marshall-media-kit.pdf ← your Canva media kit exported as PDF
└── README.md        ← this file
```

---

## Customizing index.html before you deploy

Search for these comments and replace:

| Comment | What to do |
|---|---|
| `<!-- <img src="./assets/sharitta-hero.jpg" -->` | Uncomment and add your photo |
| `Add TikTok video link` | Replace with your actual TikTok URLs |
| `https://tiktok.com/@sharitta` | Replace with your real TikTok handle |
| `https://instagram.com/sharitta` | Replace with your real Instagram handle |

---

## Deploying to Railway — Step by Step

### Step 1 — Create a new folder in your coding projects
Yes — create a new folder called `sharittamarshall-portfolio` inside your
All Coding Projects folder. Drop all these files into it.

### Step 2 — Push to GitHub
```bash
cd sharittamarshall-portfolio
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/sharittamarshall-portfolio.git
git push -u origin main
```

### Step 3 — Create a new Railway project
1. Go to railway.app and log in
2. Click **New Project**
3. Select **Deploy from GitHub repo**
4. Connect your GitHub account if not connected
5. Select the `sharittamarshall-portfolio` repo
6. Railway will auto-detect it and deploy — takes about 60 seconds

### Step 4 — Connect your domain (sharittamarshall.com)
1. In your Railway project, click your service
2. Go to **Settings → Networking → Custom Domain**
3. Click **Add Domain**
4. Type: `sharittamarshall.com`
5. Railway shows you a CNAME record to add
6. Go to wherever you bought your domain (GoDaddy, Namecheap, etc.)
7. Add a CNAME record pointing `@` to the Railway URL they give you
8. Wait 10-30 minutes for it to propagate — then sharittamarshall.com is live

---

## After it's live — updating content

To update the site later:
1. Edit `index.html` on your computer
2. `git add . && git commit -m "update" && git push`
3. Railway auto-redeploys in about 30 seconds
