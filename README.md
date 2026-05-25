# 🟢 Business Tracker

A **single-file, offline-first business activity tracker** built entirely in HTML, CSS, and JavaScript. No installation, no server, no account — just open the file in any browser and start tracking.

---

## ✨ Features

### 📊 Dashboard
- Live stats — Total, Done, In Progress, Blocked activity counts
- Donut chart breakdown by status
- 7-day activity volume bar chart
- Today's activities snapshot

### ✅ Activities
- Add activities with **title, category, priority, due date, notes**
- **Link activities to goals** for end-to-end tracking
- Update status: `To-do` → `In progress` → `Done` → `Blocked`
- Progress slider (0–100%) with color-coded bars (green / orange / red)
- **Re-link** any activity to a different goal at any time
- Filter by status, category, or goal
- **Mark All Done** in one click
- **Clear All Activities** with confirmation prompt
- Latest-updated activities always shown first

### 🎯 Goals
- Set goals with target value, unit (deals, %, calls…), and deadline
- Linked activities and recent log entries shown directly under each goal
- Color-coded progress bars (green ≥ 100%, orange ≥ 60%, red < 60%)
- **Quick Log button** on each goal card — add a log entry via modal without leaving the Goals tab
- Update current progress at any time

### 📝 Activity Log
- Log entries with **tag** (Update / Milestone / Decision / Blocker / Note)
- **Link log entries to goals** for traceability
- **Due date per log entry** — turns red with "Overdue" label if date has passed
- Delete individual entries, or **Clear All Logs** with confirmation
- Filter log by goal
- Latest entries always on top

---

## 💾 Data Storage

| Storage | How it works |
|---|---|
| **Browser (auto)** | Data is saved to `localStorage` automatically on every change — survives browser restarts |
| **JSON to disk** | Export a timestamped `.json` file you can reload, share, or upload to an AI |
| **Load from disk** | Load any previously saved `.json` file back into the tracker |

**File naming:** All exports use the format `business-tracker_YYYY-MM-DD_HH-MM-SS` so they sort naturally in your file explorer.

> **Tip — auto-save without dialogs:**
> Chrome/Edge: `Settings → Downloads` → turn off *"Ask where to save each file before downloading"*
> Firefox: `Settings → General → Downloads` → select *"Save files to"* and uncheck *"Always ask"*

---

## 📤 Exports

### Excel (.xlsx)
- 4 color-coded sheets: **Activities**, **Goals**, **Log**, **Goal Relationships**
- Status cells colored green / orange / red / gray
- Priority cells colored by severity
- Log tag cells colored by type
- Goal Relationships sheet groups every linked activity and log entry under its goal
- Downloads as a real `.xlsx` file directly to your Downloads folder

### PDF
- Opens a **color-coded report in a new browser tab** and auto-triggers the Print dialog
- Set destination to **Save as PDF** → saves to Downloads in one step
- Includes: dark cover page with summary stats, goal cards with progress bars, colored status/priority pills, linked log entries per goal, full activity table, full log table

### JSON
- Full data dump including all goal links, timestamps, and metadata
- Upload directly to **Claude.ai** or **Microsoft Copilot** for AI analysis

---

## 🤖 AI Analysis

The **Export & AI tab** includes 8 ready-made prompts you can copy and paste into Claude or Copilot alongside your exported JSON or Excel file:

- Goal risk analysis and deadline tracking
- Executive summary (wins, risks, completion rate)
- Blocker pattern detection from log entries
- Weekly prioritised action plan
- Category imbalance analysis
- Activities below 50% progress needing attention

---

## 🚀 Getting Started

1. **Download** `business-tracker.html`
2. **Double-click** to open in any browser (Chrome, Edge, Firefox, Safari)
3. Start adding goals and activities
4. Use **Save to disk** regularly to keep a portable backup
5. Use **Export → Excel or PDF** for reports and AI analysis

No internet required after first open (Google Fonts and icon library load on first visit; everything else is offline).

---

## 🗂️ File Structure

```
business-tracker.html   ← The entire app (HTML + CSS + JS, ~84 KB)
business-tracker_*.json ← Your saved data files (auto-named with timestamp)
business-tracker_*.xlsx ← Excel exports
business-tracker_*.html ← PDF source files (open → Print → Save as PDF)
```

Keep all files in the same folder for easy access.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| UI | Vanilla HTML5 + CSS3 (CSS Variables, Grid, Flexbox) |
| Logic | Vanilla JavaScript (ES6+) |
| Charts | HTML5 Canvas (donut chart) |
| Icons | [Tabler Icons](https://tabler-icons.io/) |
| Fonts | [DM Sans + DM Mono](https://fonts.google.com/) (Google Fonts) |
| Excel export | [SheetJS (xlsx)](https://sheetjs.com/) via CDN |
| Storage | Browser `localStorage` + File System API (download/upload) |

**Single file. Zero dependencies to install. Zero build step.**

---

## 📸 Screens

| Tab | Description |
|---|---|
| Dashboard | Stats overview, donut chart, 7-day bar chart, today's snapshot |
| Activities | Full activity list with progress sliders, goal links, filters |
| Goals | Goal cards with linked activities and logs inline |
| Log | Chronological log with due dates, tags, and goal links |
| Export & AI | JSON / Excel / PDF export + AI prompt library |

---

## 🔒 Privacy

- **All data stays on your device** — nothing is sent to any server
- No analytics, no tracking, no ads
- The only outbound requests are for Google Fonts and Tabler Icons on first load (can be used fully offline after that if your browser has cached them)

---

## 📄 License

MIT — free to use, modify, and distribute.

---

*Built as a single-file offline productivity tool. Designed for daily business activity tracking, goal management, and AI-ready data exports.*
