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
6. Open the **✍️ Draft** tab to draft a message or clarify a messy idea (see below).

## ✍️ Draft tab — message drafting + idea clarifying

Two helpers for moments when ADHD makes communicating feel hard:

### ✉️ Draft a message
Stuck replying to someone? Give the gist and the app writes a ready-to-copy draft — **you** send it yourself (the app never sends anything).
- **Context** — what's the situation / what you want to say.
- **To** — who it's for (name + who they are, e.g. "Sarah, my manager").
- **Tone** — friendly, warm, casual, professional, formal, apologetic, follow-up, or direct.
- **Where you'll send it** — Email, Slack/Teams, Text, WhatsApp, LinkedIn, Instagram DM, Discord, or Other. **This shapes the format** (email gets a subject line + greeting + signoff; texts stay short and casual; LinkedIn stays professional; etc.).
- **Sign off as** — optional name for the signoff.
- Hit **Draft message** → copy the result, or **Regenerate** for another pass. You can also **+ Add "send" reminder** to drop a task into your list so you actually send it.

### ✨ Clarify an idea
Braindump your messy, rambling thoughts exactly as they come. Pick how it should read (plain & simple, one sentence, short paragraph, or bullet points) and get a clean rewrite you can actually send or say.

### How drafting works (offline templates + optional AI)
- **By default:** a built-in offline template engine composes drafts instantly — no key, no internet, fully private. Great for low-friction, zero-wait help.
- **Optional AI assist:** click the **AI assist** toggle (or the ⚙️ gear in the header → *AI assistance*) and paste your own OpenRouter API key. With AI on, drafts and rewrites are richer and more natural, especially for delicate or complex messages. Your key is stored **only in your browser** and is sent only to OpenRouter when you generate a draft. No key → offline drafts are used automatically. If the AI call ever fails, it falls back to the offline draft so you're never stuck.

You can pick a model in Settings (a few popular presets like `openai/gpt-4o-mini`, `anthropic/claude-3.5-sonnet`, `google/gemini-flash-1.5`, or **Custom** to paste any OpenRouter model ID). Get an OpenRouter key at https://openrouter.ai/keys, and browse available models at https://openrouter.ai/models (including free ones ending in `:free`). The app calls `https://openrouter.ai/api/v1/chat/completions` directly from your browser.

## The ADHD-friendly ideas behind it

- **Quick capture / brain dump** — get thoughts out of your head instantly, sort later. Zero required fields.
- **Break tasks into micro-steps** — big tasks feel overwhelming; a 5-step starter path lowers the bar to starting.
- **Energy-based matching** — set your current energy (🌱 low / ⚡ medium / 🔥 high) and the app surfaces tasks you can actually do right now.
- **One-task-at-a-time mode** — "Now" shows a single next task; Focus mode hides everything else so you're not flooded.
- **Focus timer + body doubling** — a Pomodoro timer with a calm visual ring, plus a companion that "stays with you" the whole session.
- **Dopamine rewards** — confetti, a streak counter, and encouraging toasts on completion.
- **Gentle reminders & forgiveness** — overdue tasks get a soft, non-shaming nudge with one-tap "move to today" or "clear dates." No red alarms, no guilt language.
- **Message drafting** — replies are a known ADHD trap ("I'll respond later" → never). Drafting it for you, in the right tone for the right channel, shrinks the task to "just review & send."
- **Idea clarifying** — when you know what you mean but can't shape it into words, a quick rewrite gets it out of your head and into a message.

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `/` | Focus the capture box |
| `n` / `t` / `i` / `a` | Switch to Now / Today / Inbox / All |
| `c` | Switch to the Draft tab |
| `space` | Start/pause the focus timer |
| `esc` | Close focus mode or popovers |

## Data

Everything is stored in `localStorage` under the keys `gentle.tasks.v1` and `gentle.settings.v1` (the latter includes your optional OpenRouter key and chosen model).
To wipe everything: open DevTools → Application → Local Storage → clear those keys, then refresh.
