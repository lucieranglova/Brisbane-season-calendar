# Brisbane-season-calendar
# ☀️ Brisbane Season Calendar

A minimalist, emoji-friendly month-by-month guide to Brisbane's weather, events, and seasonal warnings. Built for people planning a visit or a move to Brisbane.

One file. No backend. No API keys. No build step.

![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-live-4A7C59?style=flat-square) ![Vanilla JS](https://img.shields.io/badge/vanilla%20JS-no%20framework-C8832A?style=flat-square) ![Months](https://img.shields.io/badge/months-12-1A6B9A?style=flat-square)

---

## ✨ Features

- **12 month cards** — each with weather, warnings, events, and surf conditions
- **Temperature bar** — visual min/max range in °C for every month
- **Rainfall indicator** — rain drops scaled to monthly average
- **5 intensity categories** — scored 0–5 with colour-coded bars:
  - ☀️ Weather (heat & humidity)
  - ⛈️ Storm risk
  - 🪼 Stinger season
  - 🦟 Mosquitoes
  - 🏄 Surf conditions
- **Events per month** — major events, sport, and culture (EKKA, Riverfire, Brisbane Festival, Noosa Tri...)
- **Filter bar** — highlight a single category across all 12 months at once
- **Overall badge** — quick vibe summary: *Great / Hot & Stormy / Coolest month / Wild...*
- **Staggered animations** — cards fade in on load

---

## 📅 Month overview

| Month | Overall | Highlight |
|---|---|---|
| January | 🔴 Hot & Stormy | Australia Day · peak storms |
| February | 🔴 Hot & Wet | Hottest month · flash flood risk |
| March | 🟡 Warm, easing | Best surf month · Comedy Festival |
| April | 🟢 Perfect | Easter · Anzac Day · low humidity |
| May | 🟢 Lovely | Paniyiri Festival · Writers Festival |
| June | 🟢 Great | State of Origin · best surf |
| July | 🔵 Coolest month | **EKKA** · dry season peak |
| August | 🟢 Still great | **Riverfire** 🎆 · Brisbane Festival |
| September | 🔵 Warming up | Brisbane Marathon · spring arrives |
| October | 🔵 Lively | Noosa Triathlon · Pride Festival |
| November | 🟠 Stormy build-up | Melbourne Cup · storms ramping up |
| December | 🔴 Festive & hot | Christmas · **New Year's Eve** 🎆 |

---

## 🛠️ Tech stack

- **HTML + CSS + vanilla JavaScript** — single file, zero dependencies
- **Google Fonts** — Playfair Display (serif) + Instrument Sans
- **GitHub Pages** — static hosting, no configuration needed

---

## 📁 File structure

```
brisbane-calendar/
├── index.html      # Everything – data, styles, and logic in one file
└── README.md
```

All month data lives in the `MONTHS` array inside `index.html`. Each entry contains temperatures, rain level, intensity scores for all 5 categories, and a list of events.

---

## 🚀 Deploy to GitHub Pages

1. Create a new repository
2. Upload `index.html` to the root
3. Go to **Settings → Pages → Source** → select `main` branch, `/ (root)`
4. Live at `https://yourusername.github.io/your-repo-name`

---

## ➕ Adding or editing an event

Open `index.html` and find the `MONTHS` array. Each month has an `events` field:

```js
events: [
  { name: "EKKA – Brisbane Show 🎡", type: "major" },
  { name: "Noosa Triathlon 🏊",       type: "sport" },
  { name: "Brisbane Comedy Festival", type: "culture" },
]
```

**Event types and their colours:**

| Type | Colour | Use for |
|---|---|---|
| `major` | 🟡 amber | Public holidays, fireworks, iconic Brisbane events |
| `sport` | 🔵 blue | Races, triathlons, rugby, cricket |
| `culture` | 🩷 pink | Festivals, film, food, music |
| `nature` | 🟢 green | Wildlife, nature, outdoors events |
| `warn` | 🔴 red | Warnings, hazards |

---

## 🌡️ Editing intensity scores

Each category uses a `level` from `0` (none) to `5` (extreme):

```js
storms: { text: "Peak storm season. Severe thunderstorms, hail possible.", level: 5 },
stinger: { text: "Low risk. Safe for most coastal swimming.", level: 1 },
```

The intensity bar renders automatically based on the level.

---


*Built with ❤️ 
