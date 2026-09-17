# Where Rowkeeper could go next

Today Rowkeeper is a private page on a claude.ai account. That covers the whole job with
nothing to set up, but it has three edges:

1. **Links can't be opened.** You paste captions or a transcript, or upload a screen
   recording, instead of pasting a YouTube or Instagram link.
2. **It lives on claude.ai.** It isn't an icon on your home screen with its own sign-in.
3. **Very long patterns** have to be added in parts.

A standalone version fixes all three. It is a bigger commitment: accounts to create, a small
monthly cost, and steps to follow.

## What a standalone version needs

| Piece | What it's for | Likely choice |
| --- | --- | --- |
| Hosting | Puts the app on the internet | Vercel (free to start) |
| Database + sign-in | Your patterns, private to your login | Supabase (free to start) |
| File storage | The PDFs, photos and videos you add | Supabase storage |
| Claude API key | Does the translating, kept on the server | Anthropic API, a few cents per pattern |
| Video handling | Fetches a YouTube or reel link and transcribes the audio | A small server job (yt-dlp + a speech-to-text model) |
| Installable app | Adds an icon to the phone home screen | A progressive web app (PWA) |

## A sensible order

1. **Keep using the current version.** Fine-tune how the checklists read and which extras
   are actually useful while crocheting. That knowledge is what makes the next step cheap.
2. **Move the same screens to a standalone app** with a login and a real database. Same look,
   same checklist, now installable on the phone.
3. **Add link handling:** paste a YouTube or Instagram link and let the server fetch and
   transcribe it, so no screen recording is needed.
4. **Extras worth considering:** a stitch counter with a tap target, per-project notes and
   photos, yarn substitution help, offline use so a pattern works without signal.

## Things to decide before step 2

- Only you, or family and friends with their own logins?
- Phone only, or phone and computer?
- How much per month is acceptable for hosting and translating?
