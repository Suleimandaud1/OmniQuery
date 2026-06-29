# OmniQuery 🗄️✨

**AI-Powered SQL & Pandas Query Generator** — describe your data and your question in plain English, and let Google Gemini write the SQL or Pandas code for you.

OmniQuery is a single-file, zero-build, fully client-side web app. Define a schema (or drop in a CSV), ask a business question, pick SQL or Python, and get clean, ready-to-run code with an explanation — all rendered in a sleek dark-mode UI.

![Made with React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-via_CDN-38BDF8?logo=tailwindcss&logoColor=white)
![Gemini API](https://img.shields.io/badge/Powered_by-Gemini_API-4285F4?logo=google&logoColor=white)
![No backend](https://img.shields.io/badge/Backend-None_required-brightgreen)

---

## ✨ Features

- **Schema builder** — manually define columns (name, type, description) or auto-infer them by dragging in a CSV file
- **Built-in templates** — Employee Directory, Sales Transactions, and SaaS Subscriptions presets to get started instantly
- **SQL or Pandas** — toggle between ANSI SQL and Python/Pandas output for the same question
- **Live prompt preview** — see exactly what's sent to the model before you run it
- **Session history** — restore any of your last 10 generated queries with one click
- **Bring your own API key** — each visitor enters their own Gemini API key, stored only in their own browser (`localStorage`). No keys are baked into the code or sent anywhere except Google's API.
- **No build step, no server** — it's a single `index.html` file using React, Babel, and Tailwind via CDN. Open it in a browser and go.

## 🚀 Getting Started

### 1. Get a free Gemini API key
Grab one from [Google AI Studio](https://aistudio.google.com/apikey) — it's free to start.

### 2. Run the app
No installation needed — this is a static HTML file.

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

Then either:
- **Double-click `index.html`** to open it directly in your browser, or
- **Serve it locally** (recommended, avoids any local file restrictions):

```bash
# Python
python3 -m http.server 8000

# or Node
npx serve .
```

Then visit `http://localhost:8000`.

### 3. Add your API key
On first load, you'll be prompted to paste your Gemini API key. It's saved locally in your browser only — you only need to do this once per browser/device.

## 🔐 Security & Privacy

- Your API key is **never hardcoded** anywhere in this repo.
- The key lives only in your browser's `localStorage` and is sent directly from your browser to Google's API (`generativelanguage.googleapis.com`) — it never passes through any third-party server.
- You can remove your saved key at any time via the **API Key** button in the header.

> ⚠️ Because this app calls the Gemini API directly from the browser, your API key is visible in network requests made by your own browser. Don't share screen recordings of your network tab, and use a key with appropriate usage limits if deploying this publicly.

## 🛠️ Tech Stack

| Layer        | Tool                                   |
|--------------|-----------------------------------------|
| UI Framework | React 18 (via CDN, in-browser JSX/Babel) |
| Styling      | Tailwind CSS (via CDN)                  |
| Icons        | Lucide                                  |
| AI Model     | Google Gemini (`gemini-2.5-flash`)      |
| Hosting      | Any static host (GitHub Pages, Netlify, Vercel, S3, etc.) |

## 📁 Project Structure

```
.
└── index.html   # Everything — markup, styles, and app logic — lives in this single file
```

## 🌐 Deploying

Since it's a single static file, you can deploy it anywhere static files are served:

- **GitHub Pages**: enable Pages on this repo, pointing to the root or `/docs` folder
- **Netlify / Vercel**: drag-and-drop deploy, or connect the repo directly
- **Any static bucket**: S3, Cloudflare Pages, Firebase Hosting, etc.

No environment variables or server-side secrets are required — each user supplies their own key client-side.

## 🤝 Contributing

Issues and pull requests are welcome! If you spot a bug or have an idea for a new schema preset, feel free to open an issue.

## 📄 License

[MIT](LICENSE) — free to use, modify, and distribute.
