# Set Me Up

Start with what I do and how I want to sound. I don't need a posting goal, content direction, or first topic to get started. Ask one short question at a time, and skip anything my message or saved profile already answers.

## Start the conversation

1. **What are you working on these days?** A little about what I do is enough.
2. **How would you like your posts to sound?** For example, casual and direct, or thoughtful and conversational. If I'm unsure, use the general writing rules in [AGENTS.md](../AGENTS.md) and learn from my posts later.

Don't ask what I want to post about or what I want to achieve on LinkedIn during setup. If I volunteer that information, save it without making it a requirement.

## Save each answer before asking the next question

On the first setup, handle the template examples as described below before saving my first answer. Then, after **each** answer, save everything it gives you in the same turn; don't wait for the remaining questions or past posts.

* Update [profile.md](../context/profile.md) with my background and the voice I describe, under the matching headings. Keep existing user material and update only what my answer changes. Posting goals and a posting angle can stay unknown; don't invent them or ask me to fill them in.
* Put explicit instructions that should apply going forward in the **My standing instructions** section of [AGENTS.md](../AGENTS.md#my-standing-instructions), such as a preferred tone, a hashtag for every post, or a rule for working together. Preserve the general rules and any existing user instructions. Keep the profile's writing-style summary consistent with them. Don't turn an inferred habit or a request for one draft into a standing instruction.
* Record project facts in `context/work/`, as in [AGENTS.md](../AGENTS.md#work-notes). If I also describe something I recently did, save it to `inbox/` and update its index as in [daily.md](daily.md); don't log the same account twice.
* If an answer conflicts with existing user information, save the non-conflicting parts and ask about the conflict before replacing it. Never treat template examples as existing user information.
* Briefly say what you saved and provide a clickable link to every changed file, as in [AGENTS.md](../AGENTS.md#keeping-my-files). Ask the next question in that reply, before the saved-file lines. I should be able to open what you saved immediately.

## Then invite past posts

After the background and tone answers have been saved, ask: **Can you share 3–5 past LinkedIn posts that sound most like you? It's fine to skip this.**

If I already supplied them, use them without asking again. Fewer than three is fine; don't keep asking to reach a quota. If I skip, finish setup using what I've told you and the general writing rules, not the example author's style.

For each of my posts, follow [maintain.md](maintain.md#past-posts): save its text in its own file in `posts/`, add it to the existing dashboard data as posted, and learn language, word choice, sentence length, openings, paragraphing, and formatting for [profile.md](../context/profile.md). Preserve the post's wording. Inferred habits belong in the profile, not in AGENTS.md as new instructions. A post by somebody else is only a style reference; don't file it as mine or treat its story as my experience.

Save what I provide in that turn, even if I plan to send more. Show links to the saved posts, the updated profile, and [dashboard data](../assets/posts.json), along with any other changed files.

## Continue with recent work

Once I've shared posts or skipped, say setup is ready and ask one easy question: **What have you been working on lately, or what's been on your mind?** If I've already started telling you, continue from that instead of asking again.

I don't need to arrive with an idea for a post. Follow [daily.md](daily.md): save what I say to the inbox and work notes first, then, if useful, ask one natural follow-up such as why I added a feature. Save that answer too and show the file links. You organize the material; don't ask me to fill in files.

When I ask for post angles, follow [idea.md](idea.md#when-i-ask-what-to-post): suggest angles and short outlines from the saved material, then write and save the one I confirm.

## First setup: remove only untouched template examples

The example flag in [posts.json](../assets/posts.json) is a setup signal, never permission to empty folders. [setup-examples.json](../assets/setup-examples.json) identifies the files and records shipped with this template. It is a fixed reference, not user data; never regenerate it from the current workspace during setup.

If `example` is `true`, inspect that reference and the current files before saving the first answer:

* Only a listed file at its exact path whose SHA-256 matches the reference is an untouched example. Never delete by directory, filename pattern, date, or topic. Preserve added, renamed, modified, or unrecognized files. If you can't verify a match, keep it.
* For posts and inbox days, inspect their dashboard entries or inbox-index lines too. If a related record differs from the reference, preserve both the record and its file, even if the file itself is unchanged.
* Replace an untouched example `context/profile.md` with a short profile containing Background, Writing style, and Avoid headings, then fill only what my answer supports. If the profile has been changed, keep it and merge my answers into it; don't rewrite it wholesale or carry recognizable example details forward as facts about me.
* Delete only the verified untouched example files in `context/work/`, `posts/`, and the inbox days. In `inbox/index.md`, remove only exact reference lines for sample days that were deleted or are already absent; keep every other line.
* Re-read `assets/posts.json` just before editing it. Remove only ideas whose complete objects match the reference. Remove a matching example post entry only if its verified example file was deleted or is already absent. Preserve modified entries, all user entries, unknown fields, and `schemaVersion`. Remove the `example` flag after this pass; don't reset the arrays.
* Keep AGENTS.md's general rules and all user standing instructions. Never reset them at setup.
* Report the files and records changed, with links to the changed files that remain. For a deleted sample file, name its path without a broken link. If anything could not be verified as an untouched example, mention that it was kept; don't make cleanup a barrier to setup.

If `example` is absent or false, skip cleanup. A repeated or resumed setup only fills gaps and updates what my answers change; it preserves existing profiles, work notes, inbox days, posts, ideas, and instructions. Recognizable template content is never evidence about me, even if kept because a file was modified.
