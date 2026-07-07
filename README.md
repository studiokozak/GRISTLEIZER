<p align="center">
  <img src="Captures/Studio_Kozak.png" width="500">
</p>

# GRISTLEIZER

LFO-driven dirty tremolo/filter, built to add grit and movement to pretty much anything.

<img width="1438" height="245" alt="image" src="https://github.com/user-attachments/assets/6bc0db01-98b9-4df7-a73f-732cbb0c1773" />

---

## What is it?

The name comes from a very particular piece of gear: **the Gristleizer**, a homemade effects unit built by Chris Carter of Throbbing Gristle in the late 1970s, based on a circuit designed by a then-teenage Roy Gwinn and published in *Practical Electronics* magazine. It combined an LFO with a switchable VCA or VCF stage, and Throbbing Gristle used it on just about everything — guitars, synths, even vocals — to get sounds ranging from pulsing tremolo to metallic ring-mod-like textures. It became one of the defining tools of early industrial music.

Gristleizer takes your signal and brings it to life with an LFO — either by modulating its **volume** (VCA mode, for a tremolo that has grit and bite rather than a squeaky-clean one), or by modulating a **resonant filter** that sweeps across frequencies (VCF mode, for sweeps that breathe).

It's built for guitar, synths, drums, vocals — anywhere you want organic movement instead of overly clean, digital-sounding modulation. The slightly dirty, imperfect character is intentional.

This plugin is a personal, independent reinterpretation of that effect. It's not an emulation of, or affiliated with, any official Gristleizer hardware, Throbbing Gristle, Chris Carter, or Roy Gwinn. Think of it as one more instrument inspired by that idea, built from scratch.

## Installation

1. Download the version for your system:
   - **Windows**: `Gristleizer.vst3`
   - **macOS**: `Gristleizer.vst3` and/or `Gristleizer.component` (AU)
2. Unzip the downloaded archive.
3. Copy the file into your system's plugin folder:

   | OS | Format | Folder |
   |---|---|---|
   | Windows | VST3 | `C:\Program Files\Common Files\VST3\` |
   | macOS | VST3 | `/Library/Audio/Plug-Ins/VST3/` |
   | macOS | AU | `/Library/Audio/Plug-Ins/Components/` |

4. Restart your DAW and rescan plugins if needed (often automatic).

The plugin is available in **VST3** (Windows/macOS) and **AU** (macOS).

## macOS Security

Gristleizer is built as a Universal Binary and supports both Intel and Apple Silicon Macs. Depending on your macOS security settings, you may need to authorize the plugin manually the first time it is loaded.

If macOS blocks the plugin or your DAW doesn't see it, it's likely stuck in quarantine (macOS flags anything downloaded from the internet this way). To clear it, open Terminal and run:

```bash
xattr -cr "/Library/Audio/Plug-Ins/VST3/Gristleizer.vst3"
xattr -cr "/Library/Audio/Plug-Ins/Components/Gristleizer.component"
```

(Only run the line for the format you actually installed.) Then restart your DAW.

## Controls

**Mode**
- **VCA** — tremolo with grit: volume pulses to the LFO, with asymmetric saturation giving it an organic, germanium-like character rather than a squeaky-clean digital tremolo.
- **VCF** — a filter that breathes: a resonant filter sweeps across frequencies in time with the LFO, for textures that move and evolve.

**Waveform** — the shape of the LFO, i.e. the "personality" of the movement:
- **Triangle** — smooth, even back-and-forth
- **Ramp** — gentle rise, sharp drop, for a more rhythmic/percussive feel
- **Pulse** — all-or-nothing, gate/chop effect
- **Skew** — asymmetric triangle, more organic and less predictable

**Bias** — shifts the effect's behavior (more grit/saturation in VCA, octave shift on the filter in VCF).

**Depth** — the intensity of the modulation. All the way up, it moves a lot. Pulled back, it's more subtle.

**Speed** — the LFO's rate, from very slow (movement over several seconds) to well into audible frequencies (ring-mod/robotic-style effects).

**Tempo Sync** — locks the LFO's rate to your track's tempo, with a choice of rhythmic division (whole notes, quarters, eighths, triplets...) instead of a Hz setting. Handy for an effect that always stays rhythmically locked in.

**Stereo Mode** — how the two stereo channels move relative to each other:
- **Linked** — both channels move together
- **Stereo** — slight offset for a wider effect
- **Ping-Pong** — full offset, alternating left/right

**Gain / Output / Mix** — input gain (push harder for more grit), output level, and dry/wet blend.

## A few ways to use it

- **Guitar** in VCA mode with some Depth and a positive Bias → vintage tremolo with some bite
- **Synth/pad** in VCF mode, slow Speed, tempo-synced → a filter that breathes with the track
- **Drum bus** in VCA mode, Pulse waveform, Sync on → rhythmic gating effect
- **Guitar/synth in stereo**, Ping-Pong mode → movement that travels across the stereo field
- **High Speed** (into audible range) → stranger textures, ring-mod-like modulation

## Requirements

- Windows 10/11 or macOS 11+
- A DAW that supports VST3 (Windows/macOS) or Audio Unit (macOS)
- Universal binary on macOS (Intel & Apple Silicon)
