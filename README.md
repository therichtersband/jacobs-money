# $$$

Jacob's personal budget app. One screen tells you what's safe to spend, then budgets, savings and upcoming bills. It installs on an iPhone Home Screen and works offline.

Everything you log stays on your phone (browser storage). Nothing is sent to a server.

## Files

| File | What it does |
|:|:|
| `index.html` | The whole app (layout, styles and logic) |
| `manifest.webmanifest` | Name and icon for the Home Screen |
| `sw.js` | Offline support |
| `icons/` | App icons |
| `vercel.json` | Hosting settings (no search indexing, fresh updates) |

## Put it online (free, about 10 minutes)

1. Create a **private** GitHub repo named `jacobs-money` and push this folder to it.
2. Go to vercel.com, sign in with GitHub, choose **Add New**, then **Project**, and import `jacobs-money`.
3. Framework preset: **Other**. Leave the build command and output directory empty. Click **Deploy**.
4. Vercel gives you a link like `jacobs-money.vercel.app`. Every push to `main` updates it automatically.

## Install on your iPhone

1. Open the link in **Safari** (not Chrome).
2. Tap **Share**, then **Add to Home Screen**, then **Add**.
3. Open $$$ from the icon. It runs full screen, like a regular app.

Always open it from the icon. The Home Screen app keeps its own data, separate from Safari tabs.

## Backups

Settings, then **Export backup**, saves a file (choose Save to Files, then iCloud Drive). **Restore from backup** loads one back. Export every few weeks, and before switching phones.

To get help from Claude with your numbers, export a backup and attach the file in a chat.

## Making changes

Edit `index.html`, then bump `VERSION` in `sw.js` (for example `money-v2`) so phones pick up the new version, then push. Close and reopen the app once to see it.

Your data isn't stored in the code. Updating the app never erases what you've logged.

## Starting data

The app starts empty. In Settings, add your paychecks, bills, budgets and savings goal, then tap **Match my bank balances** and type in what your bank app shows.
