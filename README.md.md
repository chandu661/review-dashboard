# 📡 ReviewRadar — Dashboard

A clean, interactive **review management dashboard** built as a single HTML file. ReviewRadar helps businesses monitor customer reviews across multiple platforms, track sentiment trends, and respond to reviews — all from one unified interface.

![ReviewRadar Dashboard](https://img.shields.io/badge/status-ready-brightgreen) ![HTML](https://img.shields.io/badge/built%20with-HTML%20%2F%20CSS%20%2F%20JS-blue) ![No dependencies](https://img.shields.io/badge/dependencies-none-lightgrey)

---

## ✨ Features

- **KPI Stat Cards** — Total reviews, average rating, unresolved negatives, and response rate at a glance, with trend indicators.
- **Review Volume Chart** — Stacked bar chart showing Positive / Neutral / Negative counts, switchable between Week, Month, and Quarter views.
- **Sentiment Donut Chart** — Animated donut ring breaking down sentiment percentages (62% Positive, 23% Neutral, 15% Negative).
- **Live Review Feed** — Scrollable, filterable list of reviews from multiple platforms with status badges (Urgent, New, Replied, Neutral).
- **Reply Panel** — Click any review to open a side panel with the full review text, AI-generated reply suggestions, a reply text area with character counter, and a Send button.
- **Urgent Alert Banner** — Real-time alert for spikes in negative reviews with a one-click "Fix Now" shortcut.
- **Platform Breakdown** — Visual progress bars showing review distribution across Google, Amazon, Trustpilot, Yelp, and App Store.
- **Top Mentioned Topics** — Ranked list of frequently mentioned topics with sentiment-coloured progress bars.
- **Response Rate Tracker** — Per-platform response rate bars vs. a 90% target.
- **CSV Export** — Download all review data as a `.csv` file with one click.
- **AI Report Generation** — Simulated AI report trigger with toast notification.
- **Multi-brand / Date Switcher** — Dropdown selectors to switch between brands and date ranges.
- **Toast Notifications** — Lightweight slide-up toasts for all user actions.
- **Sidebar Navigation** — Collapsible-style nav with sections for Overview, Manage, and Account, including badge counts.

---

## 🚀 Getting Started

No build tools, no npm, no server required.

```bash
# Clone the repo
git clone https://github.com/your-username/reviewradar-dashboard.git

# Open the file in any modern browser
open reviewradar-dashboard.html
```

That's it. The entire app is self-contained in one `.html` file.

---

## 🗂️ Project Structure

```
reviewradar-dashboard/
└── reviewradar-dashboard.html   # Complete app — HTML + CSS + JS in one file
```

---

## 🛠️ Tech Stack

| Layer      | Technology                          |
|------------|-------------------------------------|
| Markup     | Semantic HTML5                      |
| Styling    | Vanilla CSS with CSS custom properties (design tokens) |
| Logic      | Vanilla JavaScript (ES6+), no frameworks |
| Font       | [Inter](https://fonts.google.com/specimen/Inter) via Google Fonts |
| Charts     | Custom SVG donut + DOM-rendered stacked bar chart |

No external libraries, no bundler, no build step.

---

## 🎨 Design System

The UI uses a consistent set of CSS variables defined in `:root`:

| Token         | Value     | Usage                    |
|---------------|-----------|--------------------------|
| `--primary`   | `#4F6AF0` | Buttons, active states   |
| `--green`     | `#16A872` | Positive sentiment       |
| `--red`       | `#E85A6A` | Negative / urgent        |
| `--amber`     | `#D97706` | Neutral / warning        |
| `--bg`        | `#F0F2F8` | Page background          |
| `--surface`   | `#FFFFFF` | Card / sidebar surface   |
| `--text`      | `#1E2433` | Primary text             |

---

## 📸 Sections at a Glance

| Section              | Description                                              |
|----------------------|----------------------------------------------------------|
| Sidebar              | Navigation, brand logo, user profile                     |
| Topbar               | Brand switcher, date range, Export & AI Report buttons   |
| Alert Banner         | Urgent spike notification with dismiss / fix shortcut    |
| Stat Cards (×4)      | Total reviews, avg rating, unresolved negatives, response rate |
| Review Volume Chart  | Stacked bar chart with week / month / quarter toggle     |
| Sentiment Donut      | Animated SVG ring with percentage breakdown              |
| Live Review Feed     | Filterable, clickable review list                        |
| Reply Panel          | Full review + AI suggestions + reply composer            |
| Platform Breakdown   | Review counts per platform                               |
| Top Topics           | Ranked keyword mentions                                  |
| Response Rate        | Per-platform response rate progress bars                 |

---

## 🔧 Customisation

All data is defined as JavaScript arrays/objects near the bottom of the `<script>` block. To use real data, replace:

- `REVIEWS` array — your actual review objects
- `barData` object — your review volume per time period
- Stat card values — pull from your analytics API
- Platform counts — update the `pf-count` values in the HTML

For a production version, you'd wire up the fetch calls to a backend or third-party review aggregation API (e.g. Birdeye, Podium, or your own).

---

## 📄 License

MIT — free to use, modify, and distribute.

---

## 🙌 Credits

Designed and built as a UI prototype for a multi-platform review management SaaS. Inspired by modern analytics dashboards with a focus on clarity and actionability.
