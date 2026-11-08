# Vocals Plugin — Manual

Version 1.0.0 · Windows 10 / 11 (64-bit) · VST3 plugin and standalone app

- [Getting started](#getting-started)
- [The signal chain](#the-signal-chain)
- [Mic Modeler](#mic-modeler)
- [Mic Preamp](#mic-preamp)
- [Opto Leveler](#opto-leveler)
- [Effects rack](#effects-rack)
- [Presets](#presets)
- [Tips](#tips)
- [Troubleshooting](#troubleshooting)

---

## Getting started

1. Plug your microphone into your audio interface. If it is a condenser mic, switch on the
   interface's phantom power (48V).
2. Put on **headphones**. An open microphone near speakers will feed back.
3. Run `VocalsPlugin-1.0.0-Setup.exe` and choose the standalone app, the VST3 plugin or both.
   **Standalone:** open **Vocals Plugin** from the Start menu, then **Options → Audio/MIDI Settings**. Choose your
   interface as input and output and untick **Mute audio input**. The input starts muted
   for safety.
   **Plugin:** insert Vocals Plugin on a mono or stereo vocal track in your DAW and arm or monitor the track.
4. In **MIC PREAMP**, set **MIC INPUT** to the interface input your mic is plugged into.
5. In **MIC MODELER**, set **YOU SING INTO** to the kind of mic you own, and choose a model under
   **SOUNDS LIKE**, or simply pick a preset at the top right.
6. Sing at your normal level. The **IN** meter should move into the green and yellow without
   touching red. If it doesn't, use the preamp's **GAIN** knob.

Every knob shows its value while you turn it. Double-click a knob to reset it.

## The signal chain

```
mic → MIC MODELER → MIC PREAMP → OPTO LEVELER → GATE → CHARACTER → EQ → DE-ESSER → DOUBLER → DELAY → REVERB → OUTPUT
```

The top row is the "studio": the mic, the preamp and the compressor. The bottom row is the effects
rack, processed left to right. Each block has its own POWER or on/off switch with a red LED. When a
block is off it is dimmed and bypassed.

The header shows three meters: **IN** (your mic), **GR** (how much the Opto Leveler is reducing) and
**OUT** (the final signal).

## Mic Modeler

Vocals Plugin first removes the typical colour of the mic you own, then adds the colour of the
model you choose.

**YOU SING INTO**: the kind of mic you actually use.

| Setting | Use it for |
|---|---|
| Bright large condenser | most home-studio large-diaphragm condensers, which have a bright, airy top |
| Neutral condenser | flatter, more expensive condensers |
| Dynamic | handheld stage and broadcast dynamics |
| Flat (no correction) | if you don't know, or want only the model's colour |

**SOUNDS LIKE**: the model you hear. Use the **<** and **>** arrows to step through them.

| Model | Character |
|---|---|
| Your mic (no model) | your microphone as it is |
| N-87 Studio | the studio standard: smooth, open, a touch of presence |
| N-47 Tube | big tube condenser: thick low-mids, warm rounded top |
| T-251 Tube | silky tube condenser: airy, sweet and detailed |
| C-800 Pop | modern pop condenser: bright, crisp, lots of air |
| D-7 Broadcast | broadcast dynamic: dark, smooth, close and intimate |
| D-58 Stage | the stage dynamic: mid forward, bright bite, light bass |
| V-55 Fifties | fifties chrome dynamic: narrow, honky, rock'n'roll |
| R-44 Ribbon | vintage ribbon: dark, velvety, big and round |

The models are level-matched, so switching between them changes the tone, not the volume.

| Control | What it does |
|---|---|
| FILTER | low cut: removes rumble, handling noise and boominess |
| PROXIMITY | how close you are: more low end and warmth as you turn it up |
| AXIS | singing off to the side of the mic: darker and softer as you turn it up |
| Ø | polarity invert, useful when you blend Vocals Plugin with other tracks of the same voice |

## Mic Preamp

| Control | What it does |
|---|---|
| TYPE | the preamp's character (see below) |
| MIC INPUT | Input 1, Input 2 or both inputs mixed |
| GAIN | input gain, −12 to +30 dB |
| DRIVE | how hard the preamp is pushed: more harmonics and saturation |
| TONE | darker ← → brighter |
| LEVEL | the preamp's output, −18 to +12 dB |
| POWER | bypasses the preamp's colour when off |

| Type | Character |
|---|---|
| Clean | transparent, lots of headroom |
| Studio Pro | polished studio channel: presence and air |
| Vintage Tube | warm tube, rounded top, soft even harmonics |
| British Console | punchy console mids, transformer bite |
| Vintage Blues | narrow and smoky, a bluesy tube pushed hard |
| Rough | gritty and raspy, for rough rock vocals |
| Distortion | full-on distortion for screams and effects |

Turning up DRIVE doesn't make the preamp much louder, only more saturated. The amber VU meter shows the
preamp's output level.

## Opto Leveler

An optical-style compressor that keeps your voice at an even level.

| Control | What it does |
|---|---|
| PEAK REDUCTION | how much it compresses. Watch the GAIN REDUCTION meter |
| GAIN | output make-up gain, 0 to +18 dB |
| COMP / LIMIT | down = COMP, gentle; up = LIMIT, firm, for loud singing or screaming |
| POWER | compressor on or off |

Like an optical cell, it releases quickly after short peaks and more slowly after long, loud passages.
For most voices, 3 to 6 dB of reduction on the louder words is a good start.

## Effects rack

| Effect | Controls |
|---|---|
| **GATE** | THRESH (−80 to −30 dB), RELEASE. Silences breaths and room noise between phrases |
| **CHARACTER** | TYPE: Telephone, Old Radio, Megaphone, Lo-Fi · AMOUNT · MIX |
| **EQ** | LOW · MID FREQ (200 Hz – 5 kHz) · MID (±12 dB) · HIGH |
| **DE-ESSER** | FREQ (3 – 10 kHz) · AMOUNT. Tames harsh "s" and "t" sounds |
| **DOUBLER** | MIX · WIDTH. Two slightly delayed, slightly detuned copies of your voice, one left and one right, so it sounds sung twice |
| **DELAY** | TIME (60 – 900 ms) · FEEDBACK · MIX. Short times give a fifties slapback |
| **REVERB** | TYPE: Hall, Plate, Room · DECAY · TONE · MIX |
| **OUTPUT** | VOLUME, −24 to +12 dB. A soft limiter keeps the output from clipping |

## Presets

All factory presets are set to the same loudness, so you can compare them fairly.

| Preset | Sound |
|---|---|
| Init (natural) | your voice with a clean preamp and light leveling |
| Pop Pro Vocal | bright modern pop: C-800, Studio Pro, doubler and plate |
| Memphis '56 Slapback | fifties rock'n'roll: V-55, tube preamp, slapback echo, small room |
| Golden Tube Ballad | big and warm for ballads: N-47 and tube preamp |
| Silky Studio Air | airy and detailed: T-251 and Studio Pro |
| Classic Studio 87 | the classic studio vocal, through the British console |
| Late Night Radio Host | close, dark and intimate broadcast voice |
| Live Stage Rock | a stage dynamic pushed through the console |
| Velvet Crooner | dark, smooth ribbon for crooning |
| Vintage Blues Shouter | narrow, smoky and pushed |
| Telephone Verse | the classic telephone effect for a verse |
| Old Radio Broadcast | an old radio set in the next room |
| Megaphone | loud, honky megaphone |
| Rough & Raspy | gritty rock vocal |
| Distortion Scream | heavy distortion with a gate, for screams and effects |
| Lo-Fi Bedroom | soft, lo-fi bedroom pop with doubler |
| Cathedral Hall | a long, bright hall |

Choosing a factory preset resets every control except **MIC INPUT** and **YOU SING INTO**, so your
setup stays.

**Your presets:** click **Save preset**, give it a name and it appears under *My presets* in the
preset menu. Presets are saved as `.vocpreset` files in `Documents\Vocals Plugin Presets`, where you can
rename, delete or back them up.

## Tips

- Set **YOU SING INTO** correctly first: it makes the models much more convincing.
- Sing about a hand's width from a condenser and closer to a dynamic. Then fine-tune with PROXIMITY.
- For a strong effect (Telephone, Megaphone), leave CHARACTER MIX full. For a subtle colour, blend it in.
- When recording in a DAW, you can record your dry voice and use Vocals Plugin while monitoring and mixing,
  so you can change the sound later.

## Troubleshooting

**No sound in the standalone app.** Check that a yellow bar saying *"Audio input is muted"* isn't showing.
If it is, click **Settings…** and untick **Mute audio input**. Also check that the IN meter moves. If it doesn't, check
**MIC INPUT** and the input chosen in **Options → Audio/MIDI Settings**.

**Feedback or whistling.** Use headphones, or turn the speakers down and move the mic away from them.

**Crackles.** Choose a larger buffer size in **Options → Audio/MIDI Settings**.

**Latency.** In the standalone app choose **Windows Audio (Low Latency Mode)** and the smallest buffer that
plays cleanly. In a DAW, use your interface's ASIO driver. The plugin itself adds only 3 samples.

**The plugin doesn't show up in my DAW.** Check that you ticked the VST3 plugin in the installer, and that the
`Vocals Plugin.vst3` folder is in `C:\Program Files\Common Files\VST3`. If you installed it only for yourself,
it is in `%LOCALAPPDATA%\Programs\Common\VST3`; add that folder to your DAW's plugin paths. Then rescan plugins.
