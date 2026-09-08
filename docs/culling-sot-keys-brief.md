# Keys brief — The Culling × Sea of Thieves
**Bar:** premium pad feel. **House split:** Culling = weight / camera / combat clarity. SoT = art / movement / combat feel.  
**Use:** Cull veto ammo. Owners: Forge (eng), Loom (design), Vesper/Stage (art), Stride/Rigs (pad).

---

## Camera / Weight
| Key | Eng | Design | Art | Pad |
|---|---|---|---|---|
| Soft attack cam | Spring damp ~8–12; pitch kick ≤3–4°; never lose weapon silhouette on non-stagger | 1P primary; 3P only for aim-locked tools (SoT cannon rule) | Viewmodel readable vs enemy silhouette | Stick aim stays stable during swing |
| Sprint FOV | +5–12° FOV over 0.2–0.4s ease | Speed read without aim loss | Horizon stay readable at widen | FOV return must not yank reticle |
| Body lean on turn | Spine twist ≤8–12° at full yaw rate | Weight without fighting look stick | Hip/shoulder silhouette sells mass | Look accel/deadzone shipped tuned (not Input.ini homework) |
| Moving base | Velocities relative to platform (UE moving-base CM) | Ship/vehicle weight ≠ world drift | Pitch/roll inherited; damp head to horizon when not ADS | Freelook usable on tilting floor |

## Locomotion
| Key | Eng | Design | Art | Pad |
|---|---|---|---|---|
| Speed = combat dial | Anim rate locked to walk/crouch/sprint; no foot slide | Melee engage distance so circle-strafe ≠ outrun jab | Plant/brush procedural lean on soft overlap | Stick feels planted, not ice |
| No miss soft-lock | Miss → recovery/stun, never move lock | Culling: remove mini-stagger roots that enable stun-lock | Recovery anim is the punish read | Chase stays fluid (SoT cutlass lesson) |
| Carry classes | SprintOK vs SprintBlock flags | Chests/heavy = risk; tools stay mobile | Carry pose sells class at a glance | Sprint input still works when allowed — no dead LS-click |
| Attrition limp | Cripple = absolute % of base run (~5s); empty stamina ≤70–80% move | Short kite windows, readable | Limp cycle distinct | Soft lock sprint when empty, not hard freeze |

## Combat clarity / feel
| Key | Eng | Design | Art | Pad |
|---|---|---|---|---|
| Hard RPS | Jab > shove > block > jab; consistent stagger rules | Jab anim **0.67s** all weapons; shove **0.8s**; shove range **1.75m** | 3P telegraph == 1P windup (mandatory) | Timings survive latency; predict windup, auth connect |
| Active frames short | Active ≪ recovery (avoid hitbox surfing) | Partial charge scales damage continuously | Unique wound VFX per family (bleed/cripple/expose) | Charge meter always visible on hold |
| Combo / space | Mutual impulse on successful block | 3-hit chain + distinct charged unblockable (SoT cutlass shape) | Block push creates re-aim air | Button always does something — degrade accuracy, never dead primary |
| Knockback clarity | KB only on short-ToF / melee / impact weapons | Flat damage once ballistic hit registers (SoT) | Tracers always visible | Hit confirm = sting SFX + rumble, not music stinger loop |
| Anim gates | Fire enable on anim notify (gun rests), not invisible CD | Reload commits at earliest readable beat | Wield settle = ready silhouette | Prefer anim gate over input blacklist |

## Input / Pad (Rigs)
| Key | Eng | Design | Art | Pad |
|---|---|---|---|---|
| Layout | Enhanced Input: RT primary / LT secondary / ≤2 radials | Hold→select→release equip; D-pad consumables | Radial icons high-contrast | Xbox defaults: LS sprint, A jump, X interact, B stow |
| Queue polish | Tight melee queue; separate exit-block queue | Align shove startup with attack/block; inter-shove CD | — | 0.1s shove duration delta = spam feel |
| Stations | Hold-to-mount contextual; B exit | Hands stay on sticks — no menu for ship/work stations | Prompt only on look-at | Contextual interact > menus |
| Haptics | Light rumble jab; heavy stagger/block-break; dry-fire pulse | Impulse Triggers opportunity (SoT underused) | — | RT fire/clash; LT tension tools |

## UI
| Key | Eng | Design | Art | Pad |
|---|---|---|---|---|
| Chrome on delta | Health/status fade when full | Near-HUD-less mid-fight | TV silhouette stays clean | Glanceable on 10-ft |
| Diegetic info | Charge meter + throw meter always for hold-power | Critical nav as held prop / world object (SoT map table) | Rarity color + outline glyphs | Look-up scoreboard / dome status OK |
| Fair telegraphs | Clutch perk broadcast to opponent HUD | Man-tracker style mutual audio info | Short impairment FX (blind 2s + blur 4s max) | No surprise second lives |

## Lighting / Art readability (Vesper)
| Key | Eng | Design | Art | Pad |
|---|---|---|---|---|
| Separation | Tone/contrast volumes; haze↑ with weather, keep horizon | Gas/VFX align to damage volume | ≤2–3 dominant hues/vista; flatten midtone noise | Blur test: 50% Gaussian still IDs land/sea/ship/sky |
| TOD / landmarks | 4 TOD LUTs + blend; local lights punch ≥ sky | Torch = nav + reveal | Wonky-with-logic / patched wear on all props | Far LOD = max silhouette vs sky before cosmetics |
| Edges | — | Info tools tax visibility (optic glint) | No long straight silhouettes on organic/wood; asymmetry budget on characters | Threat readable mid-range on pad |

## Pacing / Audio
| Key | Eng | Design | Art | Pad |
|---|---|---|---|---|
| Quiet tension | Hyper-real attenuation biased loud on footstep/door/craft | No constant score; contact = spike | Worn/creaky palette matches patched art | Distinct one-shots: Hit / Kill / Block on SFX bus |
| Match beats | Phase timers readable (Culling gas: 10→6 / 4 / 1) | Combo-after-success shortens downtime | — | Offline bot arena for block/shove timings |

---

## Cull veto lines (ammo)
1. **Camera fights the stick** (erratic attack kick, lost weapon silhouette).
2. **Miss soft-locks move** or mini-root enables stun-lock.
3. **3P telegraph ≠ 1P** windup.
4. **Active frames longer than recovery** (jousty hitboxes).
5. **Dead primary** (button does nothing when empty/swapping).
6. **Permanent HUD chrome** when full health / no status.
7. **Vista smear** — >3 dominant hues or midtone noise kills TV read.
8. **Feel fixed by input blacklist** instead of anim gate / recovery.

## Steal priority (ship first)
1. Culling jab/shove timing table + RPS stagger consistency  
2. Soft camera spring + weapon-silhouette rule  
3. SoT chrome-on-delta + diegetic nav  
4. SoT color/tone separation + patched silhouette checklist  
5. Anim-notify ready gates + never-dead primary  
6. Pad haptics map (jab/stagger/dry-fire) + Impulse Trigger pass
