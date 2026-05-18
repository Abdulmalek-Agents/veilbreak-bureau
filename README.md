# 🕵️ Veilbreak Bureau

> *"The clues fit. The question is whether you do."*

A **procedural detective roguelike** set in an alt-history 1920s city. Each case is generated fresh — suspects, motives, weapons, alibis, timelines — and **each case has exactly one logically consistent solution**. Examine scenes, interview suspects, pin theories on your cork pinboard, and accuse before your deadline expires. Climb the ranks of an occult detective bureau. Wrong accusations persist across the campaign.

**Pitch in one line:** *Obra Dinn's deductive clarity × Hades' run-based depth × Disco Elysium's prose × infinite replay.*

---

## 📂 What's in This Repo

| File | Description |
|---|---|
| [`GAME_DESIGN.md`](./GAME_DESIGN.md) | Full game design document — vision, mechanics, market analysis, monetization, revenue projections (~$34.7M 3-year potential) |
| [`prototype.html`](./prototype.html) | **Playable interactive prototype with a working procedural mystery generator.** A new case (suspects/motive/weapon) generates every run. Examine 4 scenes, interview 5 suspects, pin clues live on the cork pinboard with green/red verdict feedback, and accuse with Suspect + Weapon + Motive. |

## ▶️ Run the Prototype

1. Download or [view raw](./prototype.html) `prototype.html`
2. Open it in any modern browser
3. Click **ENTER THE BUREAU**
4. Read the **Case File** briefing — note the victim, location, time, and persons of interest
5. Click **scenes** in the left panel to discover clue cards on the pinboard
6. Click any **Suspect Card** to interview them and read their alibi
7. **Drag clues onto suspects.** Watch the verdict tag light up: 🟢 *IMPLICATES* / 🔴 *EXONERATES* / 🟡 *AMBIGUOUS*
8. When ready: set **Suspect + Weapon + Motive** in the accusation bar and click **MAKE ACCUSATION**
9. Click **↻ New Case** to generate a brand-new mystery

> 💡 **Try playing 3 cases.** You'll see the generator produces completely different mysteries each time — but every one is solvable.

## 🎯 The Market Gap

The **Procedural Deductive Narrative** quadrant is essentially empty.

| Game | Hand-Authored | Procedural |
|---|---|---|
| Obra Dinn, Golden Idol | ✅ one solve | ❌ |
| Disco Elysium, Sherlock series | ✅ one solve | ❌ |
| Shadows of Doubt | ❌ | ✅ (sim, not narrative) |
| **Veilbreak Bureau** | — | **✅ narrative + replayable** |

Obra Dinn + Golden Idol combined: 2M+ sales at 96–97% positive. Top complaint: *"I beat it. Now what?"* — Veilbreak Bureau answers that question with infinite, fair, logically solvable mysteries.

See [`GAME_DESIGN.md`](./GAME_DESIGN.md) §2 for full demand-signal analysis.

## 💰 Revenue Model

- **Base game $24.99 EA → $29.99 1.0** (Steam + iPad + Switch)
- **Daily Case subscription** ($2.99/mo) — NYT-Crossword for mysteries
- **Two paid expansions** (new cities, new occult cases)
- **3-year projection: ~$34.7M gross / ~$20M net** (conservative)

## 🧭 Core Pillars

1. **The contract is sacred** — every case is logically solvable by deduction alone
2. **Procedural ≠ generic** — every NPC and clue reads as authored
3. **The Pinboard is the game** — all deduction is visible, diegetic, live
4. **Failure is story** — wrong accusations have permanent consequences
5. **Streamer-shaped** — every accusation is a dramatic moment

## 🔬 The Mystery Generator (Technical Note)

The prototype implements a **3-pass case generator**:
1. **World pass** — sample 5 suspects from a 10-NPC pool, each with occupation-linked weapons
2. **Crime pass** — pick culprit, weapon (matching culprit's occupation), motive
3. **Evidence pass** — generate clue cards guaranteeing one *uniquely-implicating* clue per case-element (suspect, weapon, motive), plus alibi clues for every non-culprit, plus red herrings

The full game will extend this to support occult cases, weighted social-graph motive selection, and an automated solver that fail-tests every generated case before serving it to a player. See [`GAME_DESIGN.md`](./GAME_DESIGN.md) §3.2 for the design spec.

---

Part of the **Abdulmalek Agents** game-concept portfolio · 2026
