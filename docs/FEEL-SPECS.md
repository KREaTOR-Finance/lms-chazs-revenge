# Feel specs — tutorial + AI waves
**Title:** LMS: Last Man Standing — Chaz's Revenge  
**Owner:** Loom  
**Consumers:** Forge (eng), Stride (locomotion/cam), Rigs (pad/haptics), Cull (gate)  
**Refs:** `docs/culling-sot-keys-brief.md` (Culling wins weight/camera/clarity; SoT informs locomotion fantasy only if it does not soften stick)

These are **targets**, not vibes. Numbers from Keys are ship targets until Cull reopens them.

---

## Player fantasy (slice)
You are **Chaz** in a last-man arena: planted third-person melee, readable commits, revenge clarity. Every verb must feel good on stick + face buttons before it ships. Tutorial teaches the fight language; AI waves prove the same language under pressure.

Fantasy tests (Cull):
- Weapon silhouette never lost on a non-stagger swing.
- A miss feels like your fault (recovery), not a soft root.
- A clean jab/shove/block exchange reads at TV distance on pad.

---

## Verb map (pad-first)
Default Xbox map (Rigs owns final EI; Loom owns verb intent):

| Verb | Input (default) | Feel contract |
|---|---|---|
| Move | LS | Planted gait; anim rate locked to walk/run/sprint; no ice skate |
| Look | RS | Soft spring; aim stays stable during swing |
| Sprint | LS click | SprintOK tools only; SprintBlock on heavy carry (future); never dead LS-click when allowed |
| Jump / mantle | A | Commit; no float hang |
| Interact / contextual | X | Hold-to-mount stations; prompt on look-at only |
| Stow / cancel | B | Exit block / exit station; never dead |
| Primary (jab / fire) | RT | **Never dead** — empty/swap degrades accuracy or dry-fires with haptic, does not no-op |
| Secondary (block / aim tool) | LT | Block holds; shove aligns with attack/block startup |
| Shove | (face or LT+RT per Rigs) | Startup aligned with attack/block; inter-shove CD; 0.1s duration delta = spam feel — avoid |
| Radial (≤2) | D-pad / bumper radial | Hold→select→release; high-contrast icons |

Queue polish (Rigs + Forge): tight melee queue; separate exit-block queue.

---

## Combat feel targets (Culling wins)
Hard RPS: **jab > shove > block > jab** with consistent stagger.

| Beat | Target |
|---|---|
| Jab anim | **0.67s** all weapons |
| Shove anim | **0.8s** |
| Shove range | **1.75m** |
| Active vs recovery | **Active ≪ recovery** (no hitbox surfing) |
| Telegraph | **3P windup == 1P windup** (mandatory for player and AI) |
| Miss | → recovery / stun read — **never move-lock** |
| Partial charge | Scales damage continuously; charge meter visible on hold |
| Chain | 3-hit chain + distinct charged unblockable |
| Block | Mutual impulse on successful block |
| Knockback | Melee / short-ToF only; ballistic = flat damage on connect |
| Ready gate | Anim-notify enable — prefer over input blacklist |

Hit confirm: sting SFX + light rumble (jab) / heavy rumble (stagger, block-break). Dry-fire pulse when primary empty. Impulse Trigger pass is a Rigs stretch, not slice blocker.

---

## Camera / locomotion (Stride + Forge)
| System | Target |
|---|---|
| Attack cam spring | Damp **8–12**; pitch kick **≤3–4°** |
| Silhouette rule | Never lose weapon silhouette on non-stagger |
| Sprint FOV | **+5–12°** over **0.2–0.4s** ease; return must not yank reticle |
| Body lean | Spine twist **≤8–12°** at full yaw rate |
| Moving base | Platform-relative CMC velocities |
| Attrition | Cripple ≈ absolute % base run ~**5s**; empty stamina limp **≤70–80%** move — soft-lock sprint, no hard freeze |

SoT locomotion fantasy allowed only as plant/lean/carry pose juice — **Cull vetoes float**.

---

## Tutorial flow (implementable beats)
Closed arena. No wall of text. Every prompt is a pad verb with real weight.

1. **Plant** — LS move + RS look. Gate: hold a facing for 1s without cam fight.
2. **Weight** — Walk → sprint → stop. Gate: no slide; sprint FOV eases clean.
3. **Jab** — RT into a dummy. Gate: 0.67s timing, weapon silhouette held, light haptic.
4. **Miss punish** — Whiff on purpose. Gate: recovery plays; movement stays free.
5. **Block** — LT vs scripted jab. Gate: mutual impulse; heavy haptic on break if forced.
6. **Shove** — Open a block or create space at 1.75m. Gate: 0.8s; startup aligned.
7. **RPS read** — One scripted exchange: jab beats shove, shove beats block, block beats jab. Gate: player wins by reading telegraph (3P==1P).
8. **Chrome on delta** — Take a hit, heal/full. Gate: HUD fades when full; mid-fight stays clean.
9. **Go** — Prompt: survive waves. No lore dump.

Tutorial fail rules: soft fail → replay beat, never soft-stick the cam to "help."

---

## AI waves (same language as players)
Closed space. Escalating waves until clear or death → rematch.

| Wave | Composition | Prove |
|---|---|---|
| 1 | 1 jabber | Telegraph read, jab timing |
| 2 | 1 jabber + 1 blocker | RPS, shove open |
| 3 | 2 mixed + one charged unblockable attempt | Chain space, block impulse, cam under pressure |
| 4+ | Add aggression / count (not HP sponges) | Readable commits at pad distance |

AI contracts (non-negotiable):
- **3P telegraph == 1P windup** — same anim language as the player.
- No spongy HP; difficulty = count, aggression, mix — not bullet-sponge.
- No soft hit-read; wound VFX/SFX family distinct on connect.
- Miss / whiff uses recovery, never mini-root stun-lock on the player.
- Death → rematch loop in-arena (no full BR flow).

---

## UI / feedback (slice)
- Chrome on delta: health/status fade when full.
- Charge meter visible while holding power.
- Tutorial prompts: contextual, look-at or beat-gated; dismiss on successful verb.
- No permanent HUD junk. No placeholder-as-shipped chrome.

---

## Handoff checklist
**Forge** — EI actions for verb map; CMC + cam stubs to numbers above; anim-notify ready gates; combat timing table; AI uses player telegraph assets.  
**Stride** — Gait lock, spring/damp, silhouette rule, miss→recovery locomotion, moving-base if arena has it.  
**Rigs** — Default map, remapping hooks, melee/exit-block queues, haptics (jab/stagger/dry-fire), tutorial UI nav, hold-vs-toggle where relevant; TRC-clean.  
**Cull** — Gate on veto list in Keys + fantasy tests above. "I'd feel this on Xbox."

## Out of feel-spec (still out of slice)
Full BR loot/matchmaking/voice; KBM-first path; fixing feel via input blacklist; float cam; mush telegraphs.
