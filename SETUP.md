# SETUP — Return to Center
### Content Architecture & Card System Guide

---

## ✅ Decision: No Supabase Needed

This is a one-time, static project hosted on GitHub Pages.  
All card content lives in **one JSON file** (`assets/cards.json`).  
No database. No backend. No API keys. Nothing to maintain.

> The browser reads the JSON, tracks unlock days in `localStorage`, and serves the right card automatically.

---

## 📦 The Card System

### Structure
- **10 emotions** × **7 days** × **2 sides** = 140 card entries
- **Front side**: Quote + Reflection paragraph
- **Back side** (Go Deeper): Mantra + Reframe + Action

### How Unlocking Works
- Day 1 is available immediately on first visit
- Each subsequent day unlocks 24 hours after the previous one
- The unlock timestamp is stored in the user's browser (`localStorage`)
- Key format: `rtc_unlock_[emotion]` — e.g. `rtc_unlock_anxious`

### Card Popup Behaviour
1. User taps an emotion button on `mindshift-3.html`
2. Popup appears showing today's unlocked card (front side)
3. User taps **"Go Deeper"** → card flips to reveal back side
4. User taps **"Return"** → popup closes, back to emotion picker

---

## 📊 How to Add Content (Excel → JSON)

### Step 1 — Fill the Excel Template

Use this column structure (one row per card):

| emotion | day | quote | reflection | mantra | reframe | action |
|---------|-----|-------|------------|--------|---------|--------|
| Anxious | 1 | "Courage is not..." | Anxiety often signals... | I breathe in calm... | My anxiety shows... | Practice 4-7-8... |
| Anxious | 2 | ... | ... | ... | ... | ... |
| ... | | | | | | |
| Lonely | 7 | ... | ... | ... | ... | ... |

**Total rows: 70** (10 emotions × 7 days)

> 💡 Get Jan to generate all 70 rows. Give Jan the emotion name + day number and ask for quote, reflection, mantra, reframe, and action. Review and adjust tone before converting.

### Step 2 — Convert to JSON

Use [https://csvjson.com/csv2json](https://csvjson.com/csv2json):
1. Export Excel as CSV
2. Paste into the tool
3. Download as JSON

Then restructure using the format below (or ask Claude to restructure it).

---

## 🗃️ `cards.json` Format

```json
{
  "anxious": [
    {
      "day": 1,
      "front": {
        "quote": "Courage is not the absence of fear, but action in spite of it.",
        "reflection": "Anxiety often signals that something matters to you deeply. Take a moment to breathe slowly and recognise that feeling anxious is natural."
      },
      "back": {
        "mantra": "I breathe in calm, I breathe out fear.",
        "reframe": "My anxiety shows me what matters. I can take one small step forward.",
        "action": "Practice 4-7-8 breathing: inhale for 4, hold for 7, exhale for 8. Repeat 3 times."
      }
    },
    {
      "day": 2,
      "front": { "quote": "...", "reflection": "..." },
      "back": { "mantra": "...", "reframe": "...", "action": "..." }
    }
  ],
  "frustrated": [ ... ],
  "unworthy": [ ... ],
  "ashamed": [ ... ],
  "overwhelmed": [ ... ],
  "embarrassed": [ ... ],
  "heartbroken": [ ... ],
  "numb": [ ... ],
  "guilty": [ ... ],
  "lonely": [ ... ]
}
```

---

## 🔑 Emotion Key Reference

Use these exact lowercase keys in `cards.json`:

| Button Label | JSON Key |
|---|---|
| Anxious | `anxious` |
| Frustrated | `frustrated` |
| Unworthy | `unworthy` |
| Ashamed | `ashamed` |
| Overwhelmed | `overwhelmed` |
| Embarrassed | `embarrassed` |
| Heartbroken | `heartbroken` |
| Numb | `numb` |
| Guilty | `guilty` |
| Lonely | `lonely` |

---

## 🚀 Deployment Checklist

- [ ] All 7 HTML files uploaded to GitHub root
- [ ] `assets/` folder contains all 7 PNGs + 2 MP3s
- [ ] `assets/cards.json` uploaded once content is ready
- [ ] `favicon.png` in root
- [ ] GitHub Pages set to deploy from `main` branch / root
- [ ] Test each entry point (MindShift / Meditation / Song)
- [ ] Test card flip on at least 2 emotions
- [ ] Test audio plays on meditation + song screens

---

## 📋 Content Status Tracker

| Emotion | Jan Content | Reviewed | In JSON |
|---------|------------|---------|---------|
| Anxious | ⬜ | ⬜ | ⬜ |
| Frustrated | ⬜ | ⬜ | ⬜ |
| Unworthy | ⬜ | ⬜ | ⬜ |
| Ashamed | ⬜ | ⬜ | ⬜ |
| Overwhelmed | ⬜ | ⬜ | ⬜ |
| Embarrassed | ⬜ | ⬜ | ⬜ |
| Heartbroken | ⬜ | ⬜ | ⬜ |
| Numb | ⬜ | ⬜ | ⬜ |
| Guilty | ⬜ | ⬜ | ⬜ |
| Lonely | ⬜ | ⬜ | ⬜ |

---

*Built by Claude (Anthropic) × Chef Anica ❤️ · 3C Thread To Success Cooking Lab 🧪*
