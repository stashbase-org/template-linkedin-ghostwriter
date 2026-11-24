# Keep the Dashboard Current

The dashboard is `index.html`: my ideas waiting to be written, my drafts waiting to go out, and what I've posted, with a button that opens my inbox. Everything it shows comes from `assets/posts.json`, and keeping that file current is your job. The posts themselves stay in `posts/`, one file each; the JSON only lists them, and the dashboard links to each file. StashBase shows your changes within a couple of seconds, even while the dashboard is open.

I can do two things on the dashboard myself: mark a draft posted, or take it back, and drop an idea. The page saves those to the same file.

## When to update it

* **When I tell you an idea:** add it to the top of `ideas`, as in [idea.md](idea.md). If it builds on one already there, update that one instead.
* **When I supply or confirm an outline:** put it in the idea's `plan`, in a few words. Suggested angles and outlines stay in the reply until I choose them.
* **When an idea turns into a series:** save the plan I supplied or confirmed, including the posts in it and which are already written.
* **After writing a post:** add it to `posts` as a draft, as in [write.md](write.md#saving). Then suggest removing the idea it came from, and remove it if I agree. For a series, mark the post as written in the plan instead, and suggest removing the idea once its last post is written.
* **When I tell you I posted one:** set its `posted` to `true`.
* **When I drop an idea:** remove it.
* **When I give you past posts:** save each to `posts/`, add it here as posted, and update the profile's language habits as described below. Do this in the same turn, including during setup.
* **When a post's file is added, renamed, or gone,** or its title changes: update its entry. A file I add myself is a past post unless I say it's a draft; also learn its style as described below. Check [setup-examples.json](../assets/setup-examples.json) first so a template sample is never imported as my post.
* **At first setup:** remove only verified untouched example files and matching records, as in [setup.md](setup.md#first-setup-remove-only-untouched-template-examples). Preserve all user material; never clear the arrays or folders. Repeated setup doesn't run cleanup again.

## Past posts

At setup, invite 3–5 of my own past posts that sound most like me, and make skipping explicit. Accept fewer, and accept more later without making a quota a requirement.

* Save each post in its own Markdown file in `posts/`, preserving its original wording and paragraph breaks. Use its title as the `#` heading, or derive a short title from its opening if it has none. Don't rewrite a past post to fit the current style or length rules.
* Use `YYYY-MM-DD-<slug>.md` if I give its publication date, otherwise `<slug>.md`. Don't use today's date as an invented publication date. Reuse a file only when it's the same post; choose a distinct slug for a different post rather than overwriting it.
* Add each to the existing `posts` array with `posted: true`, without duplicating a post already listed. Keep known dates newest first; don't guess dates to sort undated posts. Preserve the current order of other entries.
* Read the posts for language, word choice, sentence length, openings, paragraphing, emoji, and formatting. Update **Writing style** and **Avoid** in [profile.md](../context/profile.md) with supported habits, referring to posts by title rather than file path. Distinguish a repeated habit from a one-off example, and respect my explicit preferences. Don't create standing instructions in AGENTS.md from inference.
* Record new background and work facts supported by my posts as in [AGENTS.md](../AGENTS.md#record-what-i-tell-you). Keep their time context; an old post isn't proof of today's project status. Ask before replacing conflicting user information.
* A post I identify as someone else's is only a style reference. Don't save it as my post or add its experiences to my profile or work notes.
* Save each batch when I share it and end with clickable links to every changed file, including the posts, profile, and dashboard data. Don't wait for the rest of setup.

## Editing rules

* Read the file right before you change it. I may have marked a post or dropped an idea on the dashboard since you last looked, and my changes stay.
* Keep it valid JSON. Change only what you need, and leave every other field as it is, including fields not listed here.
* Dates are `YYYY-MM-DD`.
* Don't change `schemaVersion` or `index.html`.

## Format

```json
{
  "example": true,
  "ideas": [
    { "date": "2026-11-04", "idea": "Done means something different in someone else's project", "plan": "A series: an intro, three examples, one per post, and a wrap-up. The intro is written." },
    { "date": "2026-11-02", "idea": "Reading a stranger's codebase is a skill nobody teaches", "plan": "" }
  ],
  "posts": [
    { "title": "My first month sending PRs into other people's code", "file": "2026-11-04-first-month-sending-prs.md", "posted": true }
  ]
}
```

* `example` is `true` before the first setup cleanup; the dashboard then also tells people to say "Set me up." Setup removes the flag after its conservative cleanup pass, even if modified sample files are kept. It never authorizes deleting everything.
* `ideas` are my ideas waiting to be written, newest first.
  * `date` is the day it was added. `idea` is the idea, close to my words.
  * `plan` is an outline I supplied or confirmed, including one the Agent suggested. For a series, it's the posts in it, which are written, and what's still open; a series stays here until its last post is written. Leave the plan empty until I supply or confirm it.
* `posts` are my posts, past and new, newest first.
  * `title` is the `#` heading in its file. `file` is its file name in `posts/`. The dashboard links to it and displays the date at the start of the name. For an imported past post, use its publication date only if known; an undated filename is valid.
  * `posted` is `true` once it's out, `false` while it's a draft. Past posts I give you are posted.

## Size

The dashboard holds up to 500 KB and 20,000 values. Each idea and post is one short entry, so that's thousands of them. If it ever gets close, move the oldest posted posts to `assets/archive-<year>.json` and tell me. Their files stay in `posts/`.
