# 🌿 Gentle — an ADHD-friendly task manager

A single-file, offline web app designed around how ADHD brains actually work.
No account, no server, no install — just open `index.html` in any browser.
Your tasks stay private in your browser's local storage.

## How to use

1. Open `index.html` (double-click it, or run `open index.html` on macOS).
2. Type anything into the box at the top and press **Enter** → it lands in your **Inbox** (brain dump, no friction).
3. Tap **✎** on a task to give it an energy level + time estimate → it moves to **Today**.
4. Tap **🎯** to enter **Focus mode**: one task, full screen, with a Pomodoro timer and a body-doubling companion that stays with you.
5. Tap **✨** to break a scary big task into tiny steps — pick a starter template, then edit.

## The ADHD-friendly ideas behind it

- **Quick capture / brain dump** — get thoughts out of your head instantly, sort later. Zero required fields.
- **Break tasks into micro-steps** — big tasks feel overwhelming; a 5-step starter path lowers the bar to starting.
- **Energy-based matching** — set your current energy (🌱 low / ⚡ medium / 🔥 high) and the app surfaces tasks you can actually do right now.
- **One-task-at-a-time mode** — "Now" shows a single next task; Focus mode hides everything else so you're not flooded.
- **Focus timer + body doubling** — a Pomodoro timer with a calm visual ring, plus a companion that "stays with you" the whole session.
- **Dopamine rewards** — confetti, a streak counter, and encouraging toasts on completion.
- **Gentle reminders & forgiveness** — overdue tasks get a soft, non-shaming nudge with one-tap "move to today" or "clear dates." No red alarms, no guilt language.

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `/` | Focus the capture box |
| `n` / `t` / `i` / `a` | Switch to Now / Today / Inbox / All |
| `space` | Start/pause the focus timer |
| `esc` | Close focus mode or popovers |

## Data

Everything is stored in `localStorage` under the keys `gentle.tasks.v1` and `gentle.settings.v1`.
To wipe everything: open DevTools → Application → Local Storage → clear those keys, then refresh.
