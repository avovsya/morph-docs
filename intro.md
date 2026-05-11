# Morph: A Quick Introduction

Morph is a music-making app built around one idea: **record your hands, play them back**. You move faders, Morph remembers the movements, and they loop in time. Stack layers, build patterns, shape sounds — all by touch.

This guide walks through the core concepts in order, from "how do I make sound" to "how do I wire everything together."

---

## Opening and Saving Kits

A **kit** is a complete snapshot of everything in Morph — sounds, fader layouts, pages, patterns, scenes. Kits are saved as `.morph` files.

When you first open Morph, a default kit is already loaded. The current kit name appears near the top of the screen. An asterisk (`*`) next to the name means you have unsaved changes.

- **To save:** tap the kit name → Save
- **To load a different kit:** tap the kit name → browse factory or user kits
- **To start fresh:** tap the kit name → New Kit

Factory kits are read-only — saving them creates a copy in your user library.

> 📸 *[Screenshot: Kit name button with asterisk, save menu open]*

---

## Transport and BPM

The **Play** button starts and stops the clock. When the transport is running, sequencers fire, motion recordings play back, and everything moves in sync.

The **BPM button** (showing the current tempo, e.g. `120 BPM`) opens a dialog where you can set:
- **Tempo** — beats per minute
- **Swing** — shifts off-beat 16ths late for a groove

Morph runs at 192 PPQN internally, so timing is extremely precise.

> 📸 *[Screenshot: Play button and BPM button in header]*

---

## Faders: Your Main Control Surface

Faders are the vertical sliders that fill the main screen. Each one is mapped to a parameter — a synth's filter cutoff, reverb amount, pitch, whatever the kit designer chose.

**Drag a fader up or down to change its value.** That's it.

A thin dashed white line on each fader marks its **saved position** — the value it will snap back to when you press play. This is your reference point.

Morph also shows small colored dots to the left of the fader label:
- **Green dot** — this fader has a recorded motion
- **Camera icon** — a Time Jump gesture is waiting in the buffer

> 📸 *[Screenshot: Fader grid with saved position notch visible]*

---

## REC, HOLD, CLEAR

These three buttons modify what touching a fader does. By default they work in **Latch** mode: tap once to activate, tap again to deactivate — no need to hold.

> A note on **Momentary mode**: if you switch a button to Momentary, it's only active while you physically hold it. To latch it manually in Momentary mode, press the button and drag your finger away before releasing.

Moving a fader normally updates its saved position — the fader stays wherever you leave it, like a physical knob you turn and leave alone.

### REC — Record movements

Activate **REC**, then touch faders. Every movement is recorded into the loop in real time. Deactivate REC to stop recording.

The recording loops in sync with the transport. The next time through, Morph plays back exactly what you did.

### CLEAR — Erase a fader's recording

Activate **CLEAR**, then tap or drag a fader. Its motion recording is erased and the fader sticks to wherever you touched it.

### HOLD — Play without committing

Activate **HOLD** to temporarily suspend position saving. While HOLD is on, moving a fader does not update its saved position — useful for auditioning a value without locking it in. Deactivate HOLD and the fader snaps back to its last saved position.

> There is an alternative **Play mode** (switchable in settings) where the default behavior is reversed: faders spring back to their saved position on release, and HOLD is used to commit a new position. Play mode is designed for live performance — push a fader for emphasis, let go to return. Factory kits use Build mode, so you won't encounter this unless you switch it.

> 📸 *[Screenshot: REC/HOLD/CLEAR buttons]*

---

## The Step Indicator

The **step indicator** is the row of small dots between the fader grid and the scene controls. Each dot represents one 16th-note step in the current loop.

- **Filled dot** — at least one fader has a recorded movement at this step
- **Empty dot** — nothing recorded here
- **Highlighted dot** — the current playback position

This gives you a bird's-eye view of where your recordings are. A sparse indicator means a spacious pattern; a dense one means lots of activity.

> 📸 *[Screenshot: Step indicator with mix of filled/empty dots, playback position highlighted]*

---

## Extending and Shrinking Recordings

The **`:2`** and **`*2`** buttons change the length of the loop.

- **`:2` (Halve)** — cuts the loop in half. Data beyond the new endpoint is discarded.
- **`*2` (Double) — short press** — doubles the loop length. Existing data stays; new space is empty.
- **`*2` (Double) — long press** — doubles the loop length and clears any old data that was there before.

Use these to quickly change the feel of a loop: halving creates tight, repetitive patterns; doubling gives you room to build a longer arc.

The loop length is always measured in musical steps (8, 16, 32, or 64 sixteenth-notes).

> 📸 *[Screenshot: :2 and *2 buttons]*

---

## Freeze and Time Jump

These two buttons give you precise control over motion playback.

### Freeze (Stop Motion)

**Freeze** pauses all motion playback without stopping the transport. Sequencers and audio keep running, but faders freeze in place. Tap again to resume.

This is useful when you want the music to keep going but hold a moment — like a DJ holding a filter position while the beat plays on.

### Time Jump

**Time Jump** is a retroactive capture. Morph is always silently recording your fader movements into a short buffer in the background. Tap the Time Jump button and Morph reaches back in time and commits your last gesture into the loop — as if you'd hit REC just before you started moving.

The button glows when there's a capturable gesture waiting.

**Long-press Time Jump** to undo the last capture.

This is one of Morph's most powerful features for live performance: play freely, then keep the moments you liked.

> 📸 *[Screenshot: Freeze button and Time Jump button with availability glow]*

---

## Scenes

A **scene** is a snapshot of all your fader positions and motion recordings. Switching scenes swaps the entire state of the fader grid in one move — different positions, different recorded movements — while the sounds, routing, and device settings stay the same.

Think of scenes as variations or sections of a track: intro, verse, chorus, breakdown. Each has its own feel; switching between them live is how you create arrangement on the fly.

The **scene strip** runs along the bottom of the main screen. The active scene is highlighted. Scroll horizontally if you have more than seven scenes.

### Adding a scene

Tap the **`+`** button at the end of the scene strip. Morph duplicates the current scene — copying all saved fader positions and motion recordings — and switches to the new copy. From there you can record different movements to make it its own thing.

### Switching scenes

Tap any scene button to switch to it. By default the switch is immediate. If you've set a quantization mode (see below), the switch is deferred and the target scene button pulses with a cyan glow and shows **"Queued"** until the boundary arrives.

### Deleting and renaming scenes

Tap the **edit button** (pencil icon, glows orange when active) to enter edit mode. In edit mode:
- A **delete button** appears on each scene — tap it to remove that scene. You can't delete the last remaining scene.
- **Long-press** a scene button to rename it.
- **Long-press and drag** a scene button to reorder it.

Tap the edit button again to exit edit mode.

> 📸 *[Screenshot: Scene strip with multiple scenes, active scene highlighted, edit mode with delete buttons visible]*

### Scene switch quantization

By default, scene switches happen immediately. To snap switches to a musical boundary, open the **Kit screen** (tap the kit name) and find the **Scene Switch** setting:

| Option | When the switch happens |
|--------|------------------------|
| Immediate | Right now |
| Next Beat | Next quarter note |
| Next Bar | Next 4-beat bar |
| Next 2 Bars | Next 2-bar boundary |
| Next 4 Bars | Next 4-bar boundary |
| End of Pattern | End of the current loop length |

With any quantized mode, you can queue a switch mid-loop and it will land cleanly on the beat. The queued scene button pulses until the switch fires.

> 📸 *[Screenshot: Kit screen showing Scene Switch dropdown set to "Next Bar"]*

---

## Pages of Faders

A **page** is a named group of faders. Instead of fitting every fader on one screen, you can organize them across multiple pages — "Drums", "Bass", "FX", and so on.

Tabs at the top of the screen show all your pages. Tap a tab to switch. On iOS, swipe left and right to navigate.

Two special tabs are always present:
- **Mixer** — 8 XY faders for volume and pan of each synth slot
- **FX** — faders for global effects (filter, tape, reverb, delay, etc.)

Not every factory kit uses multiple pages — some are designed to fit on one screen.

> 📸 *[Screenshot: Page tabs at top, multiple pages visible]*

---

## Fader Types

Morph has four kinds of faders. They all record and play back motion the same way, but they control different things.

### Regular Fader

A single vertical slider. Maps to one parameter (or a stack of parameters via sections — see below).

### Sectioned Fader

A regular fader divided into **sections**, where each section of the slider range controls a different parameter. For example, the bottom third controls filter cutoff on synth A, and the top two-thirds controls filter cutoff on synth B. One physical fader, multiple destinations.

### XY Fader (2D Pad)

Two axes of control in one touch surface. Drag up/down for the Y parameter, left/right for the X parameter. When given more horizontal space, it becomes a full 2D pad with a crosshair.

Common use: X = pan, Y = volume. Or X = reverb dry/wet, Y = delay feedback. Both axes record and play back independently.

A small **dead zone** in the center can be configured to help you hold center without drifting.

### Range Fader

Two thumbs on a single vertical track — a low handle and a high handle. The filled region between them represents the active range. Drag the band to shift both together; drag individual thumbs to change the range width.

Useful for frequency bands, EQ ranges, or any "from X to Y" parameter.

> 📸 *[Screenshot: All four fader types side by side]*

---

## Video Jam Recording *(iOS Standalone only)*

Tap the **camera button** to arm video recording. When you press play, Morph records a 9:16 portrait video of your fader grid along with the audio — ready for TikTok, Reels, or Shorts.

The video captures:
- Full audio mix (exactly what you hear)
- Real-time animation of the fader grid

When the transport stops, Morph saves the video to your Photos library. From there you can share it directly.

Note: This feature is only available in the iOS Standalone app, not in AUv3 or macOS.

> 📸 *[Screenshot: Camera button, and example video frame]*

---

## Importing and Exporting Kits

**To share a kit** with someone else (or back it up):
- Tap the kit name → Export → share via AirDrop, Files, or Messages
- The kit is saved as a `.morph` file

**To load a kit someone shared with you:**
- Open the `.morph` file from Files app, email, or AirDrop
- Morph opens automatically and loads it

Exported kits are self-contained — they include all sounds, fader layouts, patterns, and scenes. The only things not included are host-specific settings from a DAW session.

> 📸 *[Screenshot: Share sheet with .morph file]*

---

## The Board

The **Board** is an advanced view showing all of Morph's devices and how they connect. Think of it as the patch bay or signal flow diagram behind the fader grid.

Devices are arranged in columns from left to right, following the signal path:

```
Modulators → Faders → Sequencers → Synths → FX → Master
```

| Column | What's Here |
|--------|------------|
| **Modulators** | LFOs, Envelopes, Gyroscope sensors |
| **Faders** | Your pages of faders (collapsible by page) |
| **Sequencers** | Euclidean, Chord, Turing Machine, Trigger |
| **Synths** | PlaitsSynth, DroneSynth, 303, WeirdDrums, MIDI, etc. |
| **FX** | Delay, Reverb, Sidechain Pump |
| **Master** | Filter, Mixer, Tape, Compression, Limiter |

Colored lines show what's connected to what:
- **Cyan** — MIDI from sequencer to synth
- **Pink** — audio from synth to master mixer
- **Orange** — modulation from LFO/Envelope to a fader
- **Green** — fader controlling a device parameter
- **Purple** — FX send level from synth to delay/reverb

Tap a device card to open its parameter panel. Tap a port (the small colored circle on a card) to start a connection, then tap a destination port to complete it.

The Board is where you build the architecture of a kit: which sequencer triggers which synth, which LFO modulates which fader, how effects are routed.

> 📸 *[Screenshot: Board view with connection lines visible across all columns]*

---

## Where to Go Next

Once you're comfortable with faders, recording, and scenes, explore:

- **Modulators** — LFOs and envelopes that move faders automatically
- **Chord Sequencer** — a full progression builder with voice leading and arpeggiator
- **Turing Machine** — generative sequences that mutate over time
- **MIDI Learn** — map external MIDI controllers to any fader

The best way to learn is to open a factory kit, press play, and start touching things.
