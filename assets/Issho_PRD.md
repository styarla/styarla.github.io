# Issho — Product Requirements Document

**Doc status:** Draft v0.1
**Owner:** [Your name]
**Last updated:** September 2026

---

## 1. Overview

**Issho** (from the Japanese "一緒" — "together") is a mobile app that gives people in long-distance relationships a shared virtual home. Each relationship — romantic partners, best friends, married couples, or siblings — gets a private apartment they decorate together. Interactive furniture in each room triggers small shared activities (craft challenges, movie night picks, co-reading prompts, etc.), and both people take care of the apartment together through everyday tasks like cleaning, cooking, and paying rent, earning in-app currency along the way.

The goal is to give distant relationships a recurring, low-effort ritual that makes the other person feel present, without requiring a synced schedule or a big time commitment.

---

## 2. Problem Statement

Long-distance relationships of every kind (romantic, friendship, family) struggle with the same core issues:

- **Time zone barriers** make synchronous connection hard to schedule.
- **Novelty fades** — texting and calling become repetitive over months/years apart.
- **Shared rituals disappear** — no more "let's cook dinner together" or "let's watch a movie" without deliberate, effortful planning.
- **Existing tools don't fit** — video calls require scheduling and full attention; social media is public and passive; couple apps tend to be either purely romantic (excluding friends/siblings) or purely functional (shared calendars, no fun).

Issho fills the gap: a shared, persistent, playful space that both people can check into on their own time and still feel like they're building something together.

---

## 3. Goals

1. Give distant relationships a shared "place" that persists and grows over time, rather than a disappearing chat thread.
2. Make relationship maintenance feel like play, not a chore list.
3. Support **asynchronous** participation — most interactions should not require both people online at once.
4. Work equally well for romantic couples, best friends, spouses, and siblings — not just dating couples.
5. Create a growing archive of shared memories (the photo wall) as a byproduct of normal use.

### Non-goals (for now)
- Replacing video/voice calling.
- Being a public social network — each apartment is private to its members.
- Supporting large group households (v1 is 1:1 pairs; small groups may come later).

---

## 4. Target Users

| Segment | Example scenario |
|---|---|
| Romantic couples | Partners separated by school, work relocation, military deployment, or visa/immigration timelines |
| Best friends | Friends who moved to different cities/countries after school |
| Married couples | Spouses temporarily apart (work assignments, deployment, visa processing) |
| Siblings / family | Adult siblings living in different countries who want a lightweight way to stay close |

At onboarding, the user selects the relationship type, which adjusts the tone of prompts and activity content (romantic vs. platonic framing) but not the core mechanics.

---

## 5. Core Concept

- Every relationship = **one private apartment**, shared by exactly two people (v1).
- The apartment has multiple **rooms** (living room, bedroom, kitchen, study, balcony, etc.).
- Rooms are decorated with **furniture/decorations**, some purely cosmetic and some **interactive**.
- Interactive decorations launch a lightweight **activity** when either person taps them.
- Both people also perform **apartment upkeep tasks** (clean, cook, pay rent, sleep/rest check-ins) that keep the space "alive" and earn currency.
- Currency is spent on new decorations, rooms, and cosmetic items.
- Completed activities can save photos to a shared **photo wall**.

---

## 6. Key Features

### 6.1 Shared Apartment & Rooms
- Apartment starts small (e.g., a studio) and expands as the relationship "levels up" through use.
- Room types (v1): Living Room, Bedroom, Kitchen, Study/Office, Balcony.
- Each room has a grid/layout editor where either partner can place, move, or remove decorations.
- Changes sync to both users; an activity feed shows who changed what ("Sam added a bookshelf to the study").

### 6.2 Interactive Decorations & Activities

Each interactive decoration triggers a specific lightweight activity when tapped. Both people don't need to be online at the same time — one person can start it, the other completes their part later, and results are compared/revealed once both are done.

| Decoration | Room | Activity |
|---|---|---|
| Gaming setup | Living room / study | Suggests a co-op game to play together, or a quick trivia/challenge mini-game |
| Bookshelf | Study / bedroom | Shared reading list + discussion prompts; both log progress and reactions |
| Craft table | Study / living room | Spin-the-wheel random craft prompt; both complete it separately, then compare and vote on a "winner" |
| Projector / TV | Living room | Movie night picker (swipe/vote on suggestions) plus a synced or "watch on your own time" mode with a shared reaction thread |
| Record player / radio | Any | "Song of the day" exchange, builds a shared collaborative playlist |
| Coffee table | Living room | Deck of conversation-starter cards for deeper check-ins |
| Cooking station | Kitchen | Recipe swap — one suggests a recipe, both cook it separately and post photos |
| Garden / balcony plants | Balcony | Daily care streak; occasional reflective prompts ("what are you grateful for today?") |
| Fitness corner | Bedroom / study | Weekly workout challenge or step-count competition |

Additional decoration/activity ideas can be added post-launch without changing the core system — new decorations are just new (activity type + content pack) pairs.

**Relationship-aware content:** the same decoration produces different activity suggestions depending on the pair's relationship type (romantic / platonic friend / sibling). A projector suggests a rom-com "movie date" for a couple, a trending show for friends, and a nostalgic childhood rewatch for siblings — same mechanic, different content pack. See the companion **Activity Library** doc for the full set of examples.

**Trending content pipeline:** some activity prompts should be pulled from what's currently popular (a trending TikTok craft, a buzzy new release, a viral game format) rather than being fully static, so the app needs a lightweight content-ops process to refresh a rotating set of prompts on a regular cadence (e.g., biweekly), separate from an evergreen baseline library that always works.

### 6.3 Apartment Care & Chores
- Everyday tasks: **clean**, **cook**, **pay rent**, **sleep/rest check-in**.
- Tasks can be individual (your own "sleep" check-in) or shared (both must "pay rent" for the week to keep the lease active).
- Neglecting tasks has soft, non-punishing consequences (e.g., a plant droops, a room looks dusty) — never lockouts or guilt-driven mechanics.
- Completing tasks earns currency and contributes to a couple/pair "streak."

### 6.4 Currency & Progression
- Earn **Issho Coins** (name TBD) through completing tasks and activities.
- Spend coins on: new decorations, room unlocks, cosmetic packs, seasonal/limited items.
- Apartment has a level or "coziness score" that grows with use, unlocking new rooms and decoration slots — gives long-term reasons to keep coming back.

### 6.5 Photo Wall
- A dedicated space (physically represented as a wall/board in the apartment) where photos from activities and manual uploads collect over time.
- Timeline/scrapbook view to browse memories chronologically.
- Stretch goal: export/print the photo wall as a physical photo book.

### 6.6 Async-First Communication
- Every activity supports "leave your part, get notified when they respond" — no requirement to be online simultaneously.
- Timezone-aware notifications (don't ping someone at 3am their time for a non-urgent nudge).
- Lightweight activity feed: "Alex watered the plant," "Jordan left you a movie pick."

### 6.7 Onboarding & Pairing
- Invite-code or link-based pairing, one relationship per apartment (v1).
- Relationship type selection (romantic / best friend / married / sibling) adjusts prompt tone and default decor themes, not core functionality.

---

## 7. Key User Flows

1. **Onboarding:** Download app → create account → choose relationship type → send/accept invite → apartment created → guided tour of first room.
2. **Daily use:** Open app → see activity feed/notifications → do a task or two → maybe interact with a decoration → check photo wall.
3. **Decoration interaction:** Tap decoration → activity prompt appears → complete your part → notify partner → both notified when complete → result (vote, reveal, comparison) shown to both.
4. **Task completion:** Task list/reminders → mark complete (or auto-detected where possible, e.g., a check-in) → earn coins → apartment state updates.
5. **Decorating:** Open room → drag/place decoration from inventory → partner sees update in real time or next login.

---

## 8. Success Metrics

- **Retention:** D1 / D7 / D30 retention per relationship (both members active).
- **Engagement:** average activities completed per week per relationship pair.
- **Streaks:** % of pairs maintaining a 7-day+ task streak.
- **Photo wall growth:** average photos added per month per relationship.
- **Balance:** ratio of romantic vs. friend vs. family relationship types (validates broader positioning, not just a couples app).
- **Virality:** invite acceptance rate.

---

## 9. MVP Scope (Suggested)

**In scope for v1:**
- 1:1 pairing, relationship type selection
- 3 rooms (Living Room, Bedroom, Kitchen)
- 4–5 interactive decorations with one activity each (gaming setup, bookshelf, craft table, projector/movie night)
- Basic task system (clean, cook, pay rent) with currency rewards
- Photo wall (manual upload + auto-save from activities)
- Push notifications, timezone-aware
- Basic decoration shop with starter cosmetic items

**Deferred to v2+:**
- Additional rooms (Study, Balcony) and decorations (garden, fitness corner, record player)
- Apartment leveling/coziness score with unlockable expansions
- Group/small-household support (more than 2 people per apartment)
- Printable photo book export
- Seasonal/limited-time content drops
- Subscription tier

---

## 10. Technical Considerations

- **Real-time sync:** shared apartment state (decoration placement, task status) should sync promptly across both devices — likely needs a lightweight real-time layer (e.g., WebSockets or a managed real-time DB) rather than pure polling.
- **Offline-friendly:** since users are async by design, actions taken offline should queue and sync when reconnected.
- **Media storage:** photo wall needs scalable image storage/CDN; consider compression and storage limits per plan tier.
- **Notifications:** timezone-aware scheduling per user, not per relationship.
- **Cross-platform:** a single codebase (e.g., React Native or Flutter) is likely more efficient than separate native iOS/Android builds, given the UI-heavy, non-performance-critical nature of the app.
- **Pairing/security:** invite-link or code-based pairing with expiration; apartments should be private by default with no discoverability by other users.

---

## 11. Monetization (Future Consideration)
- Cosmetic microtransactions: furniture skins, themed room packs, seasonal decor.
- Subscription tier: extra rooms, unlimited photo storage, exclusive activity packs, no ads (if any).
- No pay-to-win mechanics — currency should be earnable at a reasonable pace through normal use.

---

## 12. Open Questions & Risks

- ~~**Synchronicity mismatch:** how do we handle activities like "movie night" when partners are rarely online at the same time?~~ **Resolved:** for activities that work best live, the app suggests a specific real-time hangout (e.g., "watch an 80s thriller together on Teleparty," "play a Pictionary-style drawing game on a Zoom whiteboard") and provides the content/materials (movie pick, drawing prompts, discussion cards), but the actual call happens in whatever tool the pair already uses (FaceTime, Zoom, Google Meet, Discord). Issho does not need to build in-app video calling — it stays the content and coordination layer, not the calling layer. Async fallback (leave your part, get notified) remains available for activities that don't require a live moment together. See the companion **Activity Library** doc for relationship-type-specific examples.
- **Relationship changes:** how do we handle breakups, friend fallouts, or a sibling relationship ending? Data ownership and export need clear policy.
- **Content moderation:** user-generated content (craft photos, recipe photos) is private to the pair, but should we still scan for safety/abuse given photo uploads?
- **Scope creep risk:** the decoration/activity system can grow indefinitely — need a clear content pipeline and cadence rather than trying to launch with too many activity types.
- **Group support:** should sibling groups (3+ people) be supported later, and how would that change the pairing/apartment model?
- **Neglect mechanic tone:** need to carefully test that "soft consequences" for neglected tasks feel encouraging, not guilt-inducing, especially given the emotional stakes of LDRs.

---

## 13. Appendix: Naming/Tone Notes
- App name "Issho" (一緒, "together") supports the cohabitation metaphor well across all relationship types (not just romantic), which is a differentiator worth preserving in marketing and copy.
