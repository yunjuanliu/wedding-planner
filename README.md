# Wedding Planner

A single-file, self-contained wedding planning app. No build step, no dependencies, no backend.

**Features**

- **Dashboard** — countdown to the big day, overall readiness bar, guest/budget/to-do summaries
- **To-do** — timeframe sections with dates, assignees, due dates, drag-and-drop reordering, completed-items archive
- **Shop List** — items grouped by category, filterable by name and store, linked to to-do tasks
- **Guest count** — searchable household list with party size, kids, travel method, and dietary notes
- **Budget** — total budget, expense log by category, spent vs. remaining
- **Activity table** — tasks with owners, due dates, and status
- **Timeline** — day-of schedule with sections, drag-and-drop, and auto-sort by time
- **Dress** — attire tracking per person through ordering, fittings, and pickup

---

## Project structure

```
wedding-planner/
├── public/
│   └── index.html      # the entire app
├── package.json
├── vercel.json         # static hosting config
├── .gitignore
└── README.md
```

---

## Running locally

Just open `public/index.html` in a browser. Or serve it:

```bash
npm start
```

---

## Step 1 — Push to GitHub

Create an empty repo on GitHub first (no README, no .gitignore — this folder already has them). Then, from inside this folder:

```bash
git init
git add .
git commit -m "Wedding planner app"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

## Step 2 — Deploy on Vercel

1. Go to [vercel.com/new](https://vercel.com/new) and sign in with GitHub.
2. Click **Import** next to your new repository.
3. Leave every setting at its default:
   - **Framework Preset:** Other
   - **Build Command:** *(leave empty)*
   - **Output Directory:** `public`
   - **Install Command:** *(leave empty)*
4. Click **Deploy**.

Vercel gives you a live URL in under a minute. Every future `git push` to `main` redeploys automatically.

---

## Notes on data

All planner data is saved in the browser, per device — it is not synced to a server and not shared between visitors. If you open the site on your phone and your laptop, each will keep its own separate copy.

## License

MIT
