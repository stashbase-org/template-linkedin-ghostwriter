# LinkedIn Ghostwriter

Good LinkedIn posts usually come from your own work: something you built, a mistake you learned from, a call you made. You don't need a complete topic to start.

Tell the Agent what you've been working on, in your own words. It organizes the material, helps you find an angle when you're ready, and writes in your voice. Each answer is saved as you go, with links so you can open what changed and correct it.

## Getting started

Open this project in StashBase and tell the Agent:

1. **"Set me up."** It first asks what you're working on, then how you'd like your posts to sound, one question at a time. Each answer is saved immediately: background and voice in [your profile](context/profile.md), explicit ongoing instructions in [AGENTS.md](AGENTS.md#my-standing-instructions), and project details in your work notes. You don't need to choose posting goals, content directions, or a first topic.
2. **Share 3–5 past posts, or skip.** After saving those answers, it invites posts that sound most like you. Fewer is fine too. Each goes in `posts/` and onto the dashboard as posted. The Agent learns your language and writing habits from them and updates your profile, with links to the saved files.
3. **Talk about recent work.** Setup ends with "What have you been working on lately, or what's been on your mind?" A few sentences or a messy brain dump is enough. If you say you added a feature, it saves that first and may ask why you built it. It saves the answer too, keeping the day's account in `inbox/` and current project facts in `context/work/`. You don't have to fill in files yourself.
4. **"What post angles do you see?"** When you're ready, it suggests two or three angles from your saved material, each with a short outline and links to the source notes. Choose one and it writes the post, saves it to `posts/`, and adds it to the dashboard as a draft. It asks for specific missing facts only when the post needs them. You can then ask for edits, like "Make the opening more casual."

You can jump in anywhere. **"Today I …"** saves a day. **"I have an idea: …"** saves an idea and helps shape it; a sentence is enough. **"Write about …"** starts a draft from the idea you name. You can also add a day directly to `inbox/`; the Agent indexes it and picks up what's new.

Open the [dashboard](index.html) to see ideas waiting to be written, drafts waiting to go out, and what you've posted.

The template comes with an example: a software developer a month into contributing to open source, with work notes, ideas, drafts, past posts, and a few inbox days. First setup removes only verified, untouched template examples using [the example reference](assets/setup-examples.json). It preserves your added or edited material and dashboard records. Running setup again keeps your existing files and only updates what your answers change.

## The dashboard

Everything works in Chat, and you never have to open anything else. The dashboard shows where each post is at, kept current by the Agent.

* **Ideas:** ideas waiting to be written. Tell the Agent one, or choose an angle it suggests. Click one to see its outline. To drop one, use the trash can that shows when you hover over it. A series, like an intro, three examples, and a wrap-up, stays here with its plan until the last post is written.
* **Drafts:** posts written but not out yet. Click one to open it.
* **Posted:** what's out, newest first, past posts included. Tick a draft's circle once you've posted it, or just tell the Agent.

Switch to **All posts** to see every post in one table, with its status and the day it was written. **📬 Inbox** opens [inbox/index.md](inbox/index.md), a list of every day you've told it about, newest first; click a day to open it.

## Make it yours

You can change things anytime:

* **Your background and writing style** are in [context/profile.md](context/profile.md). Tell the Agent about changes or edit it yourself. Habits learned from past posts go here; goals and a posting angle are optional.
* **Your standing instructions** are in [AGENTS.md](AGENTS.md#my-standing-instructions), alongside the general rules. Tell the Agent a preference that should apply going forward and it saves it there.
* **Your work notes** are in `context/work/`, organized by project, like `open-source.md`. The Agent keeps them current as you talk.
* **Your posts** are in `posts/`, one file per post, named like `2026-11-04-first-month-sending-prs.md`. Paste past posts to the Agent or add them yourself. Start with 3–5 that best show your style; you can share more whenever you like.
* **The Agent's persona and rules** are in [AGENTS.md](AGENTS.md). How it keeps the dashboard is in [workflows/maintain.md](workflows/maintain.md).

## Files

* `AGENTS.md`: the AI's persona, general rules, your standing instructions, the task index, and how it keeps your files.
* `CLAUDE.md`: points Claude Code to `AGENTS.md`.
* `context/profile.md`: your background and writing style, plus any goals or recurring views you've shared.
* `context/work/`: what the Agent knows about your work, organized by project.
* `inbox/`: what you've told it about your days, one file per day, with `index.md` listing them.
* `posts/`: your LinkedIn posts, past and new, one file each.
* `workflows/setup.md`: the setup conversation, saving each answer, and safe example cleanup.
* `workflows/daily.md`: saving recent work and following up naturally.
* `workflows/idea.md`: shaping ideas and suggesting angles with short outlines.
* `workflows/write.md`: writing and editing LinkedIn posts.
* `workflows/maintain.md`: keeping the dashboard current, importing past posts, and the data format.
* `index.html`: the dashboard.
* `assets/posts.json`: the dashboard's ideas and post list.
* `assets/setup-examples.json`: the fixed reference for identifying untouched template examples at first setup.
* `assets/`: also holds the dashboard banner.
