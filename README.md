# SlotSync — Interview Scheduling Automation

> **Zero-backend interview scheduler.** Add candidates and interviewers, and SlotSync instantly finds the best overlapping slots — then generates a calendar invite, email draft, and interview brief in one click.

---

## 🚀 Live Demo

👉 **[Open SlotSync](https://9599602428sid-lgtm.github.io/slotsync/)** *(update link after GitHub Pages deploy)*

---

## ✨ Features

| Feature | Description |
|---|---|
| 🙋 **Multi-candidate support** | Schedule interviews for multiple candidates in one session |
| 👥 **Panel matching** | Add 2–5 interviewers with individual availability windows |
| ⚡ **Smart slot engine** | Finds overlapping slots ranked by panel coverage % |
| 📅 **`.ics` Download** | One-click calendar invite for Google Calendar, Outlook & Apple Calendar |
| 📧 **Email Draft** | Pre-filled invite email — just add the video link and send |
| 📄 **Interview Brief** | Shareable panel summary with slot reasoning and coverage stats |
| 🔁 **3-step workflow** | Set Availability → Pick Slots → Confirm |
| 📱 **Fully responsive** | Works on desktop and mobile |
| ⚙️ **Zero dependencies** | Pure HTML, CSS, and vanilla JavaScript — no build step, no backend |

---


## 🛠️ How It Works

```
Step 1 — Set Availability
  Add candidates (name, role, availability windows)
  Add interviewers (name, availability windows)
  Select interview duration (30 / 45 / 60 / 90 min)

Step 2 — Pick Slots
  SlotSync computes all overlapping time windows
  Ranks slots by panel coverage percentage
  You pick the best slot per candidate

Step 3 — Confirmed
  Download .ics calendar invite
  Copy pre-filled email draft
  Download interview brief (.txt)
```

---

## 📦 Getting Started

### Option 1: Open directly in browser
```bash
# Clone the repo
git clone https://github.com/9599602428sid-lgtm/slotsync.git
cd slotsync

# Open in your default browser
open index.html         # macOS
start index.html        # Windows
xdg-open index.html     # Linux
```

### Option 2: Use live server (recommended for development)
```bash
# If you have VS Code with Live Server extension:
# Right-click index.html → "Open with Live Server"

# Or with Python
python -m http.server 8000
# Visit http://localhost:8000
```

### Option 3: Deploy on GitHub Pages (free hosting)
1. Push repo to GitHub
2. Go to **Settings → Pages**
3. Source: **Deploy from branch → main → / (root)**
4. Your app goes live at `https://your-username.github.io/slotsync/`

---

## 🧠 Slot Matching Algorithm

SlotSync converts all availability windows to **minute-offsets from midnight**, then:

1. For each candidate's availability window, intersects it with **every interviewer's** windows
2. Finds contiguous overlapping blocks ≥ selected interview duration
3. Scores each slot by `(available interviewers / total interviewers) × 100` → **Panel Coverage %**
4. Returns top 3 slots per candidate, ranked by coverage descending

No server. No API. All computed client-side in milliseconds.

---

## 🗂️ Project Structure

```
slotsync/
├── index.html          ← Entire app (HTML + CSS + JS, single file)
├── README.md           ← You are here
├── LICENSE             ← MIT License
├── .gitignore
├── docs/
│   └── screenshots/    ← Add app screenshots here
└── .github/
    └── ISSUE_TEMPLATE/ ← Bug report & feature request templates
```

---

## 🔮 Roadmap

- [ ] Google Calendar API integration (auto-send invites)
- [ ] Time zone support (convert slots to candidate's local timezone)
- [ ] Recurring availability patterns (e.g., "every Tuesday 2–5 PM")
- [ ] Export to CSV / Google Sheets
- [ ] Slack / email notification integration
- [ ] Dark mode

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

1. Fork the repo
2. Create your feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📄 License

[MIT](LICENSE) — free to use, modify, and distribute.

---

## 👨‍💻 Author

**Siddhant** — Finance & Operations + Cloud Automation  
🔗 [GitHub](https://github.com/9599602428sid-lgtm) · [LinkedIn](www.linkedin.com/in/siddhant-suri-856a75315)

---  
> Deployed on [Netlify](https://jazzy-trifle-e8a7b5.netlify.app/)) · Zero backend · 100% client-side.
