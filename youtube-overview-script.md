# Morph — YouTube Overview Script

**Target length:** 7–8 minutes
**Tone:** energetic but unhurried; talking to a musician friend, not pitching
**Format notes:** `[SCREEN: …]` = what to show. `[ACTION: …]` = what to do on screen while talking. Record all app footage with the transport running and audio audible — Morph sells itself when it's moving. Reference stills from the docs (`docs-site/images/`) are noted where they match.

---

## COLD OPEN (0:00–0:30) — the hook

[SCREEN: Tight shot of the fader grid, transport already playing a full groove. Faders moving on their own. No logo, no intro. — like `images/stage-playing.png`, but live]

**VO:**
This track is playing itself right now. No piano roll. No timeline. Nobody's touching it.

[ACTION: Grab one fader, ride it up — the music visibly/audibly opens up. Let go.]

Every slider you see is a part of this track — and a few seconds ago, I *performed* that filter sweep. The app recorded my hand… and now it loops. Forever.

[ACTION: Tap REC, wiggle a fader, tap REC off. The wiggle now repeats every loop.]

That's the whole idea behind Morph: **you don't program this groovebox. You touch it.**

[SCREEN: Logo card — "MORPH" — 2 seconds, straight back to the app.]

---

## SECTION 1 (0:30–1:30) — what Morph is

[SCREEN: Full UI, slow pan across pages tabs, faders, scene strip — like `images/stage-overview.png`]

**VO:**
Morph is a groovebox for Mac and iOS — standalone, or as a plugin in your DAW. There are synths in here, drum voices, sequencers, effects… but you never see a step grid or a piano roll. Everything in the kit is wired to these faders.

[ACTION: Switch through pages: Drums → Bass → Sound → Perform.]

A kit gives you pages of them. Drums on one page, bass on another, a performance page with XY pads. Every fader does something musical *right now* — there's no setup screen between you and the sound.

[SCREEN: Drums page — sectioned faders, like `images/page-drums.png`]

And these aren't just volume sliders. This kick fader? At the bottom, silence. Push it up — four on the floor. Keep pushing — the pattern fills in, gets driven, gets pitched. One finger, an entire drum performance.

That works because under the hood, every fader can control *anything* — a synth parameter, a sequencer's density, an effect send — through zones and ranges the kit designer chose. More on that in a minute.

---

## SECTION 2 (1:30–3:00) — motion recording, the core trick

[SCREEN: Close on the left button rail — like `images/transport-rail.png` — then back to faders]

**VO:**
Here's the part that makes Morph different from every other groovebox: **motion recording**.

[ACTION: Tap REC (it latches, glows green). Perform a slow filter rise. Tap REC off. Step back — let it loop twice.]

Hit REC, move what you want to move, hit REC again. Done — that gesture is now part of the track, looping in sync. Record another fader on top. And another. You're not editing automation curves — you're *layering performances*, like a looper pedal for your hands.

[SCREEN: Step indicator close-up — dots filling in as recordings stack]

This dot strip shows where your movements live in the loop. Need more room? 

[ACTION: Tap the double button — loop extends. Tap halve — tight loop again.]

Double the loop for a long build, halve it for a tight repetitive groove.

And my favorite button in the entire app:

[ACTION: Move a fader expressively WITHOUT REC. Pause. Then tap Time Jump — flash — the move now loops.]

**Time Jump.** Morph is always quietly remembering what your hands just did. You make a move you love — and *after* you've made it, you tap this button, and Morph reaches back in time and keeps it. You never lose the take. Play first, commit later.

[ACTION: Tap the side Freeze (snowflake) to enter freeze mode — snowflakes appear on every fader. Tap one fader's snowflake — it holds still while the others keep moving. Tap it again — it resumes.]

Freeze lets you lock individual faders in place — the beat keeps running, the other faders keep moving — and you release each one on tap. Instant tension and release, exactly where you want it.

---

## SECTION 3 (3:00–4:00) — scenes: arrangement, live

[SCREEN: Scene strip at the bottom — like `images/scene-strip.png`]

**VO:**
So a loop is great — but a track needs sections. That's scenes.

[ACTION: Tap through scenes: Intro → Building → Blown. Music transforms each time.]

Each scene is a full snapshot — every fader position, every recorded movement. Same sounds, same wiring, completely different state. Intro, build, drop, breakdown — and you switch between them live.

[ACTION: Tap a scene while playing; it glows cyan, then switches on the bar.]

Switches are quantized — queue one anywhere in the bar, it lands exactly on the downbeat. You literally cannot miss the drop.

[ACTION: Tap "+" — new scene appears, tweak two faders, record one new gesture.]

New scene is one tap: duplicate, tweak, done. This is arranging by performing — build the next section *while the current one plays*.

---

## SECTION 4 (4:00–5:30) — what's under the hood: the Board

[SCREEN: Open the Board — the full signal-flow view, like `images/board.png`]

**VO:**
Now — where does all that sound actually come from? Tap one button, and Morph opens the hood.

This is the Board. Every device in the kit, and every wire between them. Modulators, faders, sequencers, synths, effects, master — signal flows left to right. Cyan lines are MIDI. Pink is audio. Orange is modulation. Green is fader control.

[ACTION: Slow pan/zoom across the columns.]

The sound engines are serious: **Syrinx**, a macro synth with twenty-four engines from the legendary Mutable Instruments Plaits — analog, FM, wavetables, physical modeling. **Zhalo**, a proper TB-303 with slides and accents. Two drone machines. **Tymbal** drum voices. Plus tempo-synced delay, a filtered reverb, a sidechain pump, and a tape-and-compression master chain.

[SCREEN: Tap a sequencer card — Euclid sheet opens, like `images/halfsheet-euclid.png`]

The sequencers generate the patterns: Euclidean rhythms — pick how many hits, they spread out perfectly. A Turing machine that *mutates* melodies — one knob between "locked loop" and "never repeats."

[SCREEN: Rameau sheet — chord banks, like `images/halfsheet-rameau.png`]

And Rameau — a full chord-progression engine with voicings, inversions, strum. Here's the clever bit: every other sequencer can *follow* it. Change the chord, and the bassline, the arp, the melody — the whole kit moves with the harmony. Music theory, handled.

[SCREEN: Tap a port — connect mode, like `images/tap-to-connect.png`]

And rewiring is two taps: tap a port, tap a destination. Point a different sequencer at a different synth. Aim an LFO at any fader — and watch it move *the fader itself*, the same fader you play and record. Your hands, the modulators, and the recordings all speak the same language. That's Morph's whole philosophy in one sentence.

---

## SECTION 5 (5:30–6:30) — performance extras

[SCREEN: Mixer page — like `images/mixer-page.png`]

**VO:**
Some quick hits before we wrap.

A real mixer — eight strips, volume and pan on XY pads, with metering. And yes — mixer moves record into the loop like everything else.

[SCREEN: FX page — like `images/fx-page.png`]

A dedicated FX page: delay feedback, dub sends into the reverb, the pump, the tape… and a proper DJ filter on the master for transitions.

[SCREEN: MIDI learn highlights / hardware controller on desk]

Hardware? Full MIDI learn — map your controller to any fader in seconds. Got motorized faders? Turn on CC feedback and watch them physically play back your recorded motion. And it works the other way too: Morph's sequencers and recorded fader moves can drive your hardware synths over MIDI.

[SCREEN: iOS — camera button, then a vertical jam video saving to Photos]

On iOS: tilt control from the gyroscope, haptics on every detent — and a camera button that records your jam as a vertical video with full audio, straight to your Photos. Loop to post in one tap.

---

## OUTRO (6:30–7:30) — the why + CTA

[SCREEN: Back to the full stage, playing. One unbroken take: switch a scene, ride a fader, Time Jump a move.]

**VO:**
Look — there are a lot of grooveboxes. What Morph is really about is removing the gap between *having an idea* and *hearing it*. No grid to program. No automation lanes to draw. You touch the music, it remembers, and it loops. The instrument plays on while you build the next moment.

If that's how your brain wants to make music, links are below: grab Morph for Mac or iOS, and start with the factory kits — press play and touch things. That's genuinely the manual.

[SCREEN: End card — logo, download links, docs URL]

If this video earned it, a like and subscribe help a lot — and post what you make with it. I want to hear it.

See you in the next one.

---

## Shot checklist (for the edit)

- [ ] Cold open: live groove, fader grab, REC wiggle (audio must be on point — this is the conversion moment)
- [ ] Page flips: Drums / Bass / Sound / Perform
- [ ] Kick sectioned-fader push (silence → 4/4 → driven)
- [ ] REC layering ×2–3 faders, step indicator filling
- [ ] Time Jump: expressive move → tap → loop (replay twice, it's the wow)
- [ ] Freeze mode: snowflakes on faders, lock one fader while others keep moving
- [ ] Scene tour + queued switch landing on the bar + "+" duplicate
- [ ] Board pan; Euclid sheet; Rameau banks; tap-to-connect
- [ ] LFO wired to a fader → fader visibly moves on its own
- [ ] Mixer + FX pages
- [ ] MIDI learn + (if available) motorized fader following playback
- [ ] iOS: gyro tilt + jam video export
- [ ] Outro single-take performance
