# MIDI

Morph speaks MIDI in both directions: external controllers can play Morph's faders and buttons, and Morph's sequencers and faders can drive external hardware and software.

---

## Controlling Morph: MIDI Learn

Map any knob or fader on your MIDI controller to Morph:

1. Open the Kits screen and turn on **MIDI Learn** (under the MIDI heading).
2. Back on the stage, learnable targets highlight — every fader, plus the **REC**, **HOLD**, and **CLEAR** buttons.
3. Tap the target you want to map (it blinks while armed).
4. Move a control on your MIDI device. Mapped.
5. Repeat for more targets — one hardware control can map to several targets. Tap an already-mapped target to clear it.
6. Turn MIDI Learn off and play.

Mappings persist with your setup. Unmapped targets highlight yellow in learn mode; mapped ones violet.

Everything works headless too: external faders record motion, trigger CLEAR, and play scenes whether or not the screen is visible — moving a hardware fader counts as "touching" the on-screen fader, including for REC and Time Jump capture.

---

## Motorized faders: CC Feedback

If your controller has motorized faders (or LED rings), enable **CC Feedback** in settings. Morph sends fader positions back out as CC — so when motion playback moves a fader on screen, your hardware fader physically follows it. Scene switches snap the hardware to the new positions.

Morph filters out the "echo" of its own feedback, so motors don't fight your hands.

---

## Controlling hardware from Morph

Two devices on the [Board](board.md) send MIDI out:

### MIDI Out

A synth-slot device that forwards incoming MIDI to an external output and channel. Wire any sequencer into a MIDI Out and Morph's Euclidean patterns, Turing melodies, and Rameau chord progressions play your hardware synths. Add several MIDI Outs on different channels for multitimbral rigs.

### CC Out

Sends **fader movements** as MIDI CC. Each fader can be wired to one or more CC outputs (channel + CC number). Combined with motion recording, this turns Morph into a looping automation brain for external gear: record a filter sweep once, and your hardware filter loops it forever.

---

## Notes for plugin use

As a VST3/AUv3 plugin, Morph receives MIDI from the host like any instrument, and host tempo/transport drive the sequencers. MIDI Out / CC Out route through the host's MIDI routing where the host allows it.
