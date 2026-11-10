# Issho — Activity Library (by Relationship Type)

This is a companion to the main PRD, expanding on how decoration-triggered activities adapt to relationship type (Romantic, Platonic/Best Friend, Sibling) and how "live together" activities work without Issho building its own video calling.

---

## 1. The Model: Issho as the Content Layer, Not the Calling Layer

For activities that work best done live, Issho doesn't need to build video/voice calling. Instead, the app:

1. **Suggests a specific real-time hangout** tied to the decoration (a movie, a game format, a drawing prompt set).
2. **Provides the content/materials** needed (the prompt cards, the movie pick, the discussion questions).
3. **Points the pair to a real-time tool they already use** — FaceTime, Zoom, Google Meet, Discord, Teleparty, a shared whiteboard — rather than building that infrastructure in-house.
4. **Still offers an async fallback** for anyone who can't align schedules that week ("leave your part, get notified when they respond").

This keeps "no in-app video calling" as a valid non-goal in the PRD while still solving the core problem: giving pairs a *specific, ready-made reason* to hop on a call instead of facing the blank "what do you want to do?" problem.

Two content types worth tracking separately:
- **Evergreen prompts** — always available, no dependency on what's currently trending (e.g., "36 Questions" style card decks, classic movie genres).
- **Trending prompts** — refreshed on a regular cadence (e.g., biweekly) to reflect what's currently popular: a viral TikTok craft, a buzzy new streaming release, a trending game format. These need a lightweight content-ops process — someone (or an automated feed + light human curation) reviewing trend sources and slotting new prompts into the rotation.

A small legal/product note: when a prompt references an existing branded game or format (Pictionary, Codenames, a specific streaming show), treat it as "inspired by" / a suggestion to go use that existing game or tool, rather than reproducing its copyrighted materials inside Issho — e.g., "play a Pictionary-style drawing game using your video call app's whiteboard," not a rebuilt version of the game itself.

---

## 2. Activity Variants by Decoration and Relationship Type

| Decoration | Romantic Partner | Platonic / Best Friend | Sibling / Family |
|---|---|---|---|
| **Projector / Movie Night** | "Teleparty date night: pick a rom-com or an 80s thriller and watch in sync, then rate each other's movie-picking skills." | "Watch whatever's trending on Netflix right now via Teleparty and drop live reactions in the activity feed." | "Rewatch a movie from your childhood together on FaceTime, then vote on who does the better impression of a character." |
| **Craft Table** | "Recreate a trending Pinterest date-night craft (candle pouring, paint-your-own-pottery kit) live on a call, then compare results." | "This week's viral craft challenge (from TikTok) — both attempt it separately, then vote on the winner." | "Make a card or small gift together for a parent/relative's birthday, split the steps between you." |
| **Gaming Setup** | "Play a co-op couples game (Overcooked, a Jackbox pack) over Discord/Steam Remote Play, or take a 'how well do you know me' quiz." | "Trending co-op indie game via Remote Play, or a Jackbox Party Pack over a group call." | "Revisit a childhood game (Mario Kart, a retro title) online together, plus a 'who remembers this' trivia round." |
| **Bookshelf** | "Buddy-read a romance novel with a weekly page-sync and reaction thread." | "This month's trending BookTok pick, with a discussion call once you're both done." | "Reread a book a parent used to read to you both, and swap memories about it." |
| **Coffee Table (Cards)** | "36-Questions-style deep conversation deck for couples." | "Friendship deep-talk deck — 'how well do you actually know me' style questions." | "Family history and nostalgia cards — favorite memory of a parent, funniest family trip, etc." |
| **Cooking Station** | "Recreate a trending recipe from social media as a live 'cook-along date,' each cooking your own portion on a video call." | "Trending recipe challenge — cook separately, post photos, vote on presentation." | "Cook a family recipe together on a call and compare it to how a parent/grandparent makes it." |
| **Garden / Balcony** | "Plant the same seed on the same day — a small shared care streak framed as 'watching something grow together.'" | "Shared plant-care streak plus a weekly gratitude check-in." | "Same plant-care streak, framed around a shared family memory or tradition (e.g., a plant like one from a childhood home)." |
| **Fitness Corner** | "A trending workout challenge (e.g., a 30-day mobility challenge) done together on a call." | "Step-count competition for the week, or a live workout class watched together." | "Same step-count competition, lower-pressure framing — more 'let's move' than 'let's compete.'" |
| **Record Player / Music Corner** | "Exchange a 'song that reminds me of you' each week, building a shared playlist." | "Trending song/album discovery swap — one new track a day." | "Build a nostalgia playlist of songs from family road trips or childhood." |

---

## 3. Design Notes

- **Tone shift, not mechanic shift.** The underlying system (decoration → prompt → do it → compare/react) stays identical across relationship types. Only the *content and framing* change. This keeps the engineering/content-pipeline simple: one activity engine, three (or more) content packs per activity type.
- **Sibling/family framing should avoid romantic language** by default (obvious, but worth being explicit in the content-writing guidelines so prompts don't accidentally read as date-night suggestions for a sibling pair).
- **Platonic friend framing sits in between** — warm and personal, but not romantic and not necessarily family-nostalgic either. Treat it as its own voice, not just "romantic minus the romance."
- **Trending content needs a light moderation pass** before going live (make sure a "trending" recipe, game, or show is something reasonably accessible/safe to suggest — no viral extreme challenges, no 18+ content surfaced to a sibling/family pairing, etc.).
- **Deep-linking opportunity (v2):** where possible, prompts could deep-link directly into the suggested tool (e.g., a button that opens Teleparty or starts a Zoom call) rather than just naming it, reducing friction — worth flagging as a fast-follow rather than MVP requirement.

---

## 4. Open Follow-Ups

- Decide the actual content-ops cadence and source for "trending" prompts (manual curation vs. pulling from a trend-data API vs. a hybrid).
- Confirm which relationship-type voice guidelines need sign-off from whoever owns copywriting, so prompt-writing stays consistent as the library grows.
- Decide whether relationship type is locked at onboarding or can be changed later (e.g., if the nature of a pairing changes) — affects how content packs get reassigned.
