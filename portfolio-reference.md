# davidfliesen.github.io — Working State Reference
**Date:** April 22, 2026 — All sections confirmed working at this checkpoint.

---

## File Structure (GitHub repo: DavidFliesen/davidfliesen.github.io)

```
index.html          ← Single file: all HTML + CSS (in <style> block) + JS
images/             ← All image assets (avatar, project thumbnails, storytelling images, etc.)
music/              ← Local MP3 files for audio players
  last-call.mp3
  bees-knees.mp3
  cutting-through.mp3
  rush-rush-rush.mp3
  small-town.mp3
  chatgpt-gypped-me.mp3
  front-porch-swings.mp3
  femme-fatale.mp3
  cast-it-all-away.mp3
```

---

## index.html Structure

| Lines (approx) | Content |
|---|---|
| 1–9 | DOCTYPE, meta, Google Fonts (Orbitron, Crimson Pro, JetBrains Mono) |
| 10–420 | `<style>` block — all CSS |
| 406 | NAV |
| 421 | HERO section |
| 462 | AI & CODE section (Projects) |
| 591 | MUSIC section |
| 627 | MULTIMEDIA & STORYTELLING section |
| 765 | AI ROOTS section |
| 803 | CONNECT section |
| 815 | FOOTER |
| 837 | LIGHTBOX overlay |
| 842 | `<script>` — lightbox JS + Now Playing tracker |

---

## CSS Color Palette (CSS variables in :root)
```css
--bg:      #07090c   /* page background */
--surface: #0d1117   /* card backgrounds */
--border:  #1a2030   /* borders */
--cyan:    #00ffc8   /* primary accent */
--gold:    #f0c040   /* secondary accent */
--rose:    #ff4d6d   /* storytelling section accent */
--text:    #c8d8e8   /* body text */
--muted:   #4a6070   /* subdued labels */
--nav-h:   56px      /* nav bar height */
```

## Fonts
- **Orbitron** — headings, nav logo, project titles (TRON aesthetic)
- **Crimson Pro** — body text
- **JetBrains Mono** — labels, tags, terminal, nav links, track titles

---

## Nav Order (matches page scroll order)
AI & Code → Music → Multimedia → AI Roots → Connect + LinkedIn button (right)

---

## Hero Section
- **Left column (420px):** Avatar image (`images/david-fliesen.png`) + terminal card
- **Right column (1fr):** Name, pills, body text, View Projects + LinkedIn buttons
- Name: "David" white, "Fliesen" cyan outline with blinking cursor
- Terminal shows: skills, experience, status

---

## Projects Section (AI & Code)
Grid: **3 columns desktop**, 2 col tablet, 1 col mobile

**Row 1:**
1. AHA · Agentic Healthcare Assistant — `https://youtu.be/QECOr-wRevM` — Badge: Capstone · Purdue Online
2. InsightForge — `https://youtu.be/s0zfirf2sdk` — Badge: Capstone · Purdue Online
3. Aladdin's News Genie (ANG) — `https://youtu.be/aXyeG0BJ7P4` — Badge: Agentic Frameworks Course

**Row 2:**
4. Sisters of Summerville — `https://sisters-of-summerville.github.io/Sisters-of-Summerville/`
5. RenderCraft AI — `https://youtu.be/Qq5K601TFcg` — Badge: Building LLMs Course

---

## Music Section
- **Intro text** + Lira Album link
- **YouTube embed** (above audio clips): `https://www.youtube-nocookie.com/embed/NmVU5NulA5A` — "Last Call (on the old me) by Lira"
- **"// Audio Clips" label** above the player list
- **9 audio players** — all served from local `music/` folder (NOT cdn1.suno.ai — those are 403 blocked)
- **Now Playing** label driven by JS at bottom of file

### Audio file mapping:
| Title | File |
|---|---|
| Last Call (on the old me) | music/last-call.mp3 |
| The Bee's Knees & the Cat's Pajamas | music/bees-knees.mp3 |
| Cutting Through Me Like Lightning | music/cutting-through.mp3 |
| Rush Rush Rush | music/rush-rush-rush.mp3 |
| Small Town | music/small-town.mp3 |
| ChatGPT Just Gypped Me! | music/chatgpt-gypped-me.mp3 |
| Front Porch Swings (all doggone day) | music/front-porch-swings.mp3 |
| Femme Fatale of the Feline World | music/femme-fatale.mp3 |
| Cast It All Away | music/cast-it-all-away.mp3 |

> **NOTE:** cdn1.suno.ai direct MP3 URLs return HTTP 403 (host_not_allowed) from external sites. Always use the local music/ folder files.

---

## Multimedia Section
- **Animation & Rigging grid: 4 columns** — Soldier, Zombiefication, Project Gemini, Contractions
- **Storytelling/3D/Game Design grid: 4 columns** — Creatures of Magic, WTC Hub, SimWars, MEDATAR, ISTE 2017
- Storytelling images open in a **lightbox** (click to expand, ESC to close)
- Creative links row: Voice Over, Character Animation, Cibola Studios

---

## AI Roots Section
- Two-column: Sun Tzu avatar image (left) + timeline (right)
- Timeline entries: 2008–2009, 2009, 2010

---

## Responsive Breakpoints
| Breakpoint | Change |
|---|---|
| max-width: 960px | Hero left col shrinks to 340px |
| max-width: 900px | Projects 2-col, MM grid 2-col, Story grid 2-col, Roots 1-col |
| max-width: 820px | (music layout collapses if two-col ever re-added) |
| max-width: 640px | Hero 1-col, all grids 1-col (MM stays 2-col), nav links hidden |

---

## Key External Links
- LinkedIn: `https://www.linkedin.com/in/fliesen/`
- Sisters of Summerville: `https://sisters-of-summerville.github.io/Sisters-of-Summerville/`
- Suno profile: `https://suno.com/@cibola`
- Lira playlist: `https://suno.com/playlist/8f7963c6-b967-4a59-8835-9accdd64325f`
- Voice Over: `https://www.voices.com/profile/suntzu`
- Character Animation: `https://character-animator.weebly.com`
- Cibola Studios: `https://cibolastudios.weebly.com`

---

## Things NOT to change without caution
- `cdn1.suno.ai` URLs — do not use, they are blocked. Always use `music/` folder.
- Sisters of Summerville `index.html` — always edit directly in GitHub web editor, never download/re-upload (Cloudflare email obfuscation issue).
- YouTube embeds use `youtube-nocookie.com` with `playsinline=1` for iOS compatibility.
