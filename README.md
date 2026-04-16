# Return to Center 🕊️
### by 3C Thread To Success

> *Tap In · Tune Out · Feel Better*

A mobile-first emotional wellness experience built as a static GitHub Pages app. Users navigate through a guided journey — choosing their emotional entry point, receiving daily mindshift cards, a guided meditation, and a grounding song — completing a full return to center.

---

## ✨ What It Does

- **3 Entry Points**: Users can begin at MindShift Kit, Meditation, or Song — meeting them where they are
- **Full Cycle Flow**: Every path ends at the Thank You screen, completing the emotional reset loop
- **7-Day Card Journey**: Each emotion unlocks one card per day for 7 days (front: quote + reflection / back: mantra + reframe + action)
- **Card Flip**: "Go Deeper" flips the card to reveal deeper tools
- **Guided Meditation**: Audio plays directly in-browser
- **Grounding Song**: Original music by Chef Anica, plays in-browser
- **Zero forced paths**: Users are never locked into a sequence they don't want

---

## 🗂️ File Structure

```
/
├── index.html              ← Auto-redirects to home.html
├── home.html               ← Hub: 3 entry points (MindShift / Meditation / Song)
├── mindshift-1.html        ← Landing / START screen
├── mindshift-2.html        ← Instructions screen
├── mindshift-3.html        ← Emotion picker (10 buttons)
├── meditation.html         ← Guided meditation audio screen
├── song.html               ← Grounding song audio screen
├── thankyou.html           ← Cycle complete screen
├── favicon.png
└── assets/
    ├── 1.png               ← Home hub background
    ├── 2.png               ← MindShift landing background
    ├── 3.png               ← Instructions background
    ├── 4.png               ← Emotion picker background
    ├── 5.png               ← Meditation background
    ├── 6.png               ← Song background
    ├── 7.png               ← Thank You background
    ├── cards.json          ← All card content (7 days × 10 emotions × 2 sides)
    ├── 3C Mindshift Guided Affirmation-Meditation.mp3
    └── 3C Meditation Song - Return to Center.mp3
```

---

## 🔁 Navigation Flow

```
HOME
 ├── [MindShift Kit] → mindshift-1 → mindshift-2 → mindshift-3 → meditation → song → thankyou
 ├── [Meditation]    →                                             meditation → song → thankyou
 └── [Song]          →                                                          song → thankyou
```

---

## 🎨 Design System

| Element | Value |
|---------|-------|
| Background | `#0a0714` (deep space) |
| Title colour | `#61d8e6` (3C sky blue) |
| Body text | `rgba(255,255,255,0.9)` |
| Buttons | Warm earth brown, transparent glass feel |
| Font | Open Sans |
| Style | Glassmorphism · Warm earth tones · No neon |

---

## 🌐 Live

[https://anica-blip.github.io/3c-reframe-to-rise/](https://anica-blip.github.io/3c-reframe-to-rise/)

---

## 🤝 Built By

Built by Claude (Anthropic) × Chef Anica ❤️ · 3C Thread To Success Cooking Lab 🧪

*"Think Smart, Not Harder"*
