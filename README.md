# DigiArp

**Arpeggiator and Melody Engine for Digitakt OG — audio and MIDI.**

By **BonVoyage ModularForms** · [MatthCrn](https://github.com/MatthCrn)

DigiArp turns a source trig into an arpeggio or an evolving phrase on the original Digitakt. Shape its rhythm, movement and register, introduce small changes or wider variations, freeze a phrase, then edit its steps while playing.

## Downloads

Public beta **D620 / 0.62.0dev0**, for **Digitakt MK1 OS 1.54**, using **elekloader Core 4.1**.

- [Download the DigiArp module](https://raw.githubusercontent.com/MatthCrn/DigiArp/b8814471ab11671ed422465e21f4477d2c703468/DigiArp-0.62.0dev0.elemod)
- [Download sources, licences, full guide and test reports](https://raw.githubusercontent.com/MatthCrn/DigiArp/16e1d3324dbd70edec974bfdd67a8c3d5670aa7d/DigiArp-Public-Beta-D620.zip)

Module SHA-256 `b7c8bbe77faefbf0b16863babcbc563b64a999e9f31d7717e91cba5056ab6456`.

Build a custom OS locally using [elekloader](https://elekloader.github.io/shop/#build), your own official Digitakt OS 1.54 file, Core 4.1 and the DigiArp module. Keep an official OS copy and back up projects and samples before installing. This is unofficial experimental firmware.

## Start playing

1. Choose an ONESHOT sound on an audio track, or assign an output channel to a MIDI track. Place a source trig. For sustained audio playback, begin with native LEN set to INF.
2. Open DigiArp with **FUNC + TRIG**, choose **TRUE** on its main page and start playback.
3. Press **YES** for **Note Source**, select the source notes and scale, then **YES** for **Melody Engine**. Its prepared phrase starts on the next accepted source trig.
4. Choose a preset, adjust RHY and MOT, then raise VAR gradually. FREEZE holds a phrase.
5. Press **YES** to return to the main step editor. It displays the phrase being played as it evolves. Stop the transport to stop playback.

## Melody Engine

| Encoder | Function |
| --- | --- |
| A RHY | Rhythmic placement and density, from silence to sixteen attacks |
| B MOT | Pitch movement and musical activity |
| C OCT | Four register positions |
| D PRESET | FREE, BASS, ARP, ROLL, MELO and FLOW |
| E VAR | Six increasing variation depths |
| F FREEZE | Hold the phrase ON, allow evolution OFF |
| G RISE | Introduce higher-register notes |
| H FREQ | Native audio filter frequency |

**YES** moves Main → Note Source → Melody Engine → Main. **NO** moves back through Note Source to Main, and exits from Main. After returning from Melody Engine, the main editor offers selected-step velocity, speed, audio filter and probability, plus step and Euclidean controls.

**FUNC + REC** captures a phrase as pattern trigs. Follow the on-screen confirmation prompts and try this on a disposable pattern first. **FUNC + CLEAR** clears the track and resets its DigiArp state.

Audio tracks T1–T8 also gain a third LFO page. Press LFO to cycle **1/3 → 2/3 → 3/3**. Additional destinations include ME RHY, MOT, OCT, VAR, PRESET and RISE.

## Beta status and compatibility

The author tested D620 on a Digitakt and reports **below 90% CPU with eight active tracks and LFOs**. Full conditions, duration and free RAM remain to be documented. The outcome of previously reported audible clicks remains to be confirmed.

- **LFO 3 parameter locks remain unimplemented.**
- Audio generation supports the native **ONESHOT** machine.
- Other instruments and OS versions are unqualified.
- DigiPoly, DigiMatrix and the separate project-data-dt1 module are declared conflicts.
- A static Modwerk audit also found overlaps with Machine Pages, digichain, NEIGHBOR, Digi Perform and Euclidean Sequencing. Avoid combining this beta with these modules until integration is resolved.
- **Modwerk catalogue integration is in preparation.** The author build uses Core 4.1; the checked Modwerk profile announces interface 2.1.
- Project persistence is implemented and has software test coverage. Physical save/reload and power-cycle results for this exact version still need to be recorded.

The supplied sources rebuild to a byte-for-byte identical D620 module using its original toolchain. The archive contains the detailed test report and compatibility audit.

## Sources and licences

The source archive includes the corresponding C and assembly, guarded build recipe, rebuild tool, GPL-2.0-or-later licence and MIT component notice. Firmware integration is GPL-2.0-or-later. Components marked MIT retain their licence. Original DigiArp contributor notices are preserved.

Musical design, direction and hardware testing by BonVoyage ModularForms, with Codex-assisted implementation and testing. The external elekloader SDK and Core retain their authorship and licences.

## Feedback

[Open an issue](https://github.com/MatthCrn/DigiArp/issues) with the version, track type, preset, source mode, tempo, track length, companion modules and reproduction steps. Keep firmware images and personal projects private.
