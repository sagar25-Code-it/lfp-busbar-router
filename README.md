# Series / Parallel Bus Bar Router
### by PS3D Hub

A free, browser-based layout tool for planning the copper bus bar wiring of large-format LiFePO4 battery packs — before you cut a single piece of copper.

---

## 1. Tool Description

This tool lets you lay out a grid of prismatic battery cells (the default is tuned for the common 3.2 V / 280 Ah class of cells), wire them into a series/parallel pack either by hand or automatically, and watch it calculate the electrical result in real time — pack voltage, capacity, energy, current limits, and the physical bus bar specs needed to carry that current safely.

It runs entirely in your browser. There's no install, no login, no backend server, and no data ever leaves your device — everything from the routing engine to the electrical math is plain HTML, CSS, and JavaScript.

## 2. Use

1. **Set your grid** — choose columns (1–8) and rows (1–20) under *Pack Layout*, or pick a ready-made shape (3×12 slim, 4×9 balanced, 6×6 shortest, 2×18 service lane, 8×5 wide) under *Layout Optimizer*. "Best Cost Layout" scans shapes for you and picks the cheapest one to wire.
2. **Remove any cells you don't need** by clicking the × on them — connections update automatically.
3. **Wire the pack** — click *Auto Series* to route the whole pack in one go, or click two terminals manually to place a single bus bar yourself. Flip a row's orientation if your physical layout needs it.
4. **Enter your real numbers** under *Cell Specifications* — nominal voltage, capacity, max current, your target design current, and the bus bar's width and thickness.
5. **Read the results** — *Pack Output* gives you voltage/capacity/energy the moment your wiring forms a valid topology. *Electrical Check* tells you if your bus bar is thick enough, how hot it'll run, how much copper you'll need, and whether any bars overlap.

## 3. Benefits

- **Catch mistakes on screen, not in the workshop.** Unequal string lengths, overlapping bus bars, and undersized copper all show up as warnings before you've spent a rupee on materials.
- **Buy the right amount of copper.** The copper mass estimate is based on your actual routed length, not a guess — useful for quoting and ordering.
- **Compare layouts in seconds.** Try 3×12 versus 6×6 versus a custom shape and see the cost/length difference instantly instead of re-wiring a real pack to find out.
- **No spreadsheet required.** Voltage, capacity, C-rate, current density, and voltage drop are calculated for you as you design.
- **Nothing to install.** Anyone with a link and a browser can use it — clients, collaborators, or your own team.

## 4. Features

- Adjustable pack grid, 1–8 columns × 1–20 rows, with individual cell removal/restore
- Five one-click layout presets, plus an automatic "best cost" layout finder
- Automatic full-pack wiring (**Auto Series**) or fully manual terminal-by-terminal wiring
- An automatic routing engine that tries multiple path strategies per connection and keeps bus bars clear of terminals and each other
- Per-row flip control for matching real-world cell orientation, with one-click reset
- Undo and clear controls for the routed bus bars
- Editable cell specs: nominal voltage, capacity (Ah), max current, and design current
- Editable bus bar geometry: width and thickness in mm
- Three routing preferences: cost-optimized, straight-priority, or safety-spacing
- Live pack output: auto-detected topology badge (e.g. "16S3P"), pack voltage, capacity, and energy
- Live electrical check: max pack current, design C-rate, bus current density, bus resistance, voltage drop, I²R heat loss, copper mass, and a route/clearance overlap check
- Ordered route list showing exactly how the auto-router connected your pack
- A built-in reminder that this is a **layout helper only** — high-voltage battery work should always be verified by a qualified professional before assembly

## 5. Goal

To give DIY and small-scale LiFePO4 pack builders a free, no-install way to *see* their wiring plan and its electrical consequences before assembly — so fewer packs get built with mismatched strings, undersized bus bars, or wiring that only made sense on paper.

---

## 6. Instructions — Deploying This Site (GitHub + Render)

This is a static site (just `index.html` — no server, no database), so it deploys in a few minutes on Render's free static site hosting.

### Step 1 — Put the files in a GitHub repository

1. Go to [github.com](https://github.com) and sign in (or create a free account).
2. Click the **+** in the top-right corner → **New repository**.
3. Name it something like `ps3d-hub-busbar-router`. Choose **Public** or **Private** — either works with Render. Leave "Add a README file" **unchecked** (we're supplying our own). Click **Create repository**.
4. On the new, empty repo's page, click **uploading an existing file**.
5. Drag in all four files from this folder: `index.html`, `README.md`, `render.yaml`, and `.gitignore`.
6. Scroll down and click **Commit changes**.

That's it — no command line needed.

### Step 2 — Deploy on Render

1. Go to [render.com](https://render.com) and sign in — **"Sign in with GitHub"** is the fastest option since it connects your account automatically.
2. Click **New +** → **Static Site**.
3. Choose the repository you just created (authorize Render to access it if asked) and click **Connect**.
4. Fill in the form:
   - **Name**: anything you like — this becomes part of your free `.onrender.com` web address.
   - **Branch**: `main`
   - **Build Command**: `echo "No build needed - static HTML site"`
   - **Publish Directory**: `.`
5. Click **Create Static Site**.

Render will run its first deploy (usually under two minutes) and give you a live URL like `https://ps3d-hub-busbar-router.onrender.com`. Every time you push a change to this GitHub repo afterward, Render automatically redeploys it — no extra steps.

### Step 3 (optional) — One-click setup with the included `render.yaml`

This folder already includes a `render.yaml`, which describes the exact same setup as Step 2 in code. If you'd rather skip filling in the form by hand:

1. In Render, click **New +** → **Blueprint** instead of *Static Site*.
2. Point it at your GitHub repo. Render reads `render.yaml` automatically and pre-fills everything.
3. Click **Deploy**.

### Adding your own domain later

Once the site is live, Render's Settings tab lets you attach a custom domain (e.g. `busbar.ps3dhub.com`) for free — just point your domain's DNS at Render following the instructions shown there.

---

**Maintained by PS3D Hub**
Sagar Patel · Bengaluru, India
📞 +91 84014 89892 · ✉️ 84014sagar@gmail.com
