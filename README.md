# Awesome Seedance API 🎬 — Prompts, Variants & One-Call Video Generation

> The most complete open guide to **ByteDance Seedance — the cinematic AI video model (Seedance 1 · 1.5 Pro · 2.0 · 2.5)** — a community prompt library and a single API to run every variant.

<p align="center">
  <a href="https://wavespeed.ai/seedance-2-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedance-api"><img src="https://img.shields.io/badge/▶_Run_Seedance_2.5-Get_API_Key-00E5FF?style=for-the-badge&labelColor=0B0B0F" alt="Run Seedance 2.5"></a>
  <a href="https://wavespeed.ai/seedance-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedance-api"><img src="https://img.shields.io/badge/Seedance_2.0-Try_Now-7C3AED?style=for-the-badge&labelColor=0B0B0F" alt="Seedance 2.0"></a>
</p>

<p align="center">
  <b>🌊 Powered by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedance-api">WaveSpeedAI</a> — serverless Seedance API, pay-as-you-go, zero cold starts.</b><br>
  <a href="https://wavespeed.ai/seedance-2-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedance-api"><b>→ Get a Seedance 2.5 API key</b></a> &nbsp;·&nbsp; <a href="https://wavespeed.ai/seedance-2-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedance-api"><b>→ Try Seedance 2.0</b></a>
</p>

<p align="center">
  🖥️ <b>No code?</b> Generate in your browser (no setup, free to start) → <a href="https://wavespeed.ai/video-generator?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedance-api"><b>WaveSpeedAI Video Generator</b></a>
</p>

---

> **Generate right now**
> ```bash
> npm i -g @wavespeed/cli && wavespeed login
> wavespeed run bytedance/seedance-2.5/text-to-video -p "your prompt"
> ```
> No GPU, no cold start — the same endpoint powers every prompt below.

---

## 📖 Contents
1. [What is Seedance?](#what-is-seedance)
2. [Run it via API](#run-it-via-api)
3. [Model Variants](#model-variants)
4. [Prompt Library](#prompt-library) — 12 community prompts
5. [Related Model Guides](#related-model-guides)
6. [Contributing](#contributing)

---

## What is Seedance?

**Seedance** is ByteDance's cinematic AI video model — text or image in, high-motion video out, with strong subject consistency, explicit camera control, and native audio sync on the 2.x line. WaveSpeedAI serves the full family: Seedance 1, 1.5 Pro, 2.0 (fast/mini) and the flagship **2.5**.

---

## Run it via API

One endpoint, submit + poll. Swap the model path for any variant below.

```bash
curl -s -X POST "https://api.wavespeed.ai/api/v3/bytedance/seedance-2.5/text-to-video" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY" -H "Content-Type: application/json" \
  -d '{"prompt": "A cinematic tracking shot through a neon-lit night market, rain, 8k", "aspect_ratio": "16:9"}'
# → {"data": {"id": "<prediction_id>"}}

curl -s "https://api.wavespeed.ai/api/v3/predictions/<prediction_id>/result" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY"
# → status: completed → outputs: ["<url>"]
```

**[→ Get your Seedance 2.5 API key](https://wavespeed.ai/seedance-2-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedance-api)** · pay-as-you-go, live pricing on each model page.

**Python wrapper:** [seedance-2.5-api](https://github.com/WaveSpeedAI/seedance-2.5-api) — one typed function per Seedance 2.5 endpoint, built on the official SDK.

---

## Model Variants

All variants open in-browser with a copy-paste API snippet.

### Seedance 2.5 — flagship &nbsp;[▶ API](https://wavespeed.ai/seedance-2-5-api)
[text-to-video](https://wavespeed.ai/models/bytedance/seedance-2.5/text-to-video) · [image-to-video](https://wavespeed.ai/models/bytedance/seedance-2.5/image-to-video) · [video-edit](https://wavespeed.ai/models/bytedance/seedance-2.5/video-edit) · [video-extend](https://wavespeed.ai/models/bytedance/seedance-2.5/video-extend)

### Seedance 2.0 / fast / mini &nbsp;[▶ API](https://wavespeed.ai/seedance-2-api)
[2.0 t2v](https://wavespeed.ai/models/bytedance/seedance-2.0/text-to-video) · [2.0-fast](https://wavespeed.ai/models/bytedance/seedance-2.0-fast/text-to-video) · [2.0-mini](https://wavespeed.ai/models/bytedance/seedance-2.0-mini/text-to-video)

### Seedance 1.5 Pro / 1
[1.5-pro t2v](https://wavespeed.ai/models/bytedance/seedance-v1.5-pro/text-to-video) · [1-pro 1080p](https://wavespeed.ai/models/bytedance/seedance-v1-pro-t2v-1080p)

> Full catalog: **[wavespeed.ai/seedance-2-5-api](https://wavespeed.ai/seedance-2-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedance-api)**

---

## Prompt Library

12 prompts curated from the Seedance creator community. Credit stays with the original author. Fill in `{...}` placeholders.

### 1. Hollywood Professional Racing Movie Style
*by [@johnAGI168](https://x.com/johnAGI168)*

```
Style: Hollywood Professional Racing Movie (Le Mans Style), Cinematic Night, Rain, High Stakes Sport.
Duration: 15s.

[00-05s] Shot 1: The Veteran (Interior/Close-up).
Rain lashes the windshield of a high-tech race car on a track. The Veteran driver (in helmet) looks over, calm and focused. Dashboard lights reflect on his visor.
Dialogue Cue: He gives a subtle nod and mouths "Let's go."

[05-10s] Shot 2: The Challenger (Interior/Close-up).
Cut to the rival car next to him. The younger driver grips the wheel tight, breathing heavily. Eyes wide with adrenaline.
Dialogue Cue: He whispers "Focus" to himself.

[10-15s] Shot 3: The Green Light (Wide Action).
The starting lights turn Green. Both cars accelerate in perfect sync on the wet asphalt. Water sprays massively into the camera lens. Motion blur turns the stadium lights into long streaks of color.
```

### 2. Denis Villeneuve Style Epic Desert Scene
*by [@johnAGI168](https://x.com/johnAGI168)*

```
Style: IMAX 70mm Film, Denis Villeneuve Style, Gritty Realism, Epic Scale, Desaturated.
Duration: 15s.
[00-05s] Extreme Wide Shot (The Scale). A colossal sandstorm, miles high, swallows a vast desert landscape. A tiny convoy of armored military vehicles races away from it. The scale of nature vs man is terrifying. Hans Zimmer style tension.
[05-10s] Cockpit Cam (The Panic). Inside the lead rover. The pilot screams "GO! GO!" (Subtitle: MAX POWER!). Camera shakes violently. Sand blasts the windshield. The sun is blocked out by the approaching wall of dust.
[10-15s] The Jump (The Climax). The rover hits a massive dune and launches into the air (Slow Motion). Silhouette against the dark storm. Lightning strikes within the dust cloud. Debris flies past the lens. Cut to black on impact.
```

### 3. Wong Kar-wai Film Style (Rainy Phone Booth Scene)
*by [@johnAGI168](https://x.com/johnAGI168)*

```
[Film Style]: 90s Hong Kong Art Cinema style, retro film feel, high ISO grain, ambiguous yellow-green tint, frame stepping effect, melancholic atmosphere.

[Core Dialogue (for emotion control)]: "If memories were canned food, I hope they never expire."

[Video Duration]: 10 seconds
[Script]:

[00:00-00:04] Shot 1: Through the Glass Peeping.
Scene: A rain-covered red public telephone booth.
Character: A man (or woman) in a khaki trench coat holding the receiver tightly, not speaking, just listening.
Emotional Performance: Through the glass refraction, see his/her eyes hollow yet deeply emotional. Rain flows down the glass, distorting his face like an oil painting.
Subtitle/Narrative sense: The picture seems frozen, only the sound of rain.

[00:04-00:07] Shot 2: Extreme Close-up & Micro-expression.
Scene: Focus on the character's lips and half face.
Action: He/She whispers softly into the receiver. Lips tremble slightly, seeming to want to say something but swallow it back.
Lighting: Street neon bokeh flows across his face, bright and dim alternately.
Dialogue Emotion Mapping: Shows the ultimate restraint and loneliness of "wanting to touch but drawing back".

[00:07-00:10] Shot 3: Signature Slow-shutter Drag Shadow.
Scene: Character hangs up phone, turns around and walks into the rainy crowd.
Visual Effect: Using frame stepping effect (stop-motion feel), the character's back becomes blurred with trailing shadows (motion blur), as if the soul stayed in place while only the body walks away.
Environment: Background is flowing city car lights forming elongated light trails.

[Technical Parameters]: Simulated handheld camera, shallow depth of field, color shift, emotionally intense.
```

### 4. Perfume MG Animation Style
*by [@BFAVicky](https://x.com/BFAVicky)*

```
Based on the script from Image 1, generate advertising content for the perfume product in Image 2. The voiceover should reference a natural female voice speaking in English. Pay attention to the proportions of the perfume bottle, integrating it into the background with natural lighting. Avoid heavy texture overlay and cutout effects. The pace can be more brisk.
```

### 5. Giant Orange Cat Meme Style
*by [@johnAGI168](https://x.com/johnAGI168)*

```
【Style】Mockumentary, mobile Vlog perspective, hyperrealistic CG combined with real scenes, 8K quality, perfect fur physics simulation.
【Duration】15 seconds
【Scene】Hongya Cave in Chongqing or a busy overpass intersection (with magical 8D city feel).
[00:00-00:05] Shot 1: Visual spectacle (The Reveal).
The scene shows a bustling city street. The camera lifts up to reveal a **Gozilla-sized orange tabby cat** stuck between two skyscrapers.
Action: The giant cat is stuck because it's too fat, waving its huge paws with a pitiful expression, trying to pull itself out.
Detail: Cat fur is clearly visible in the sunlight, huge paw pads pressing against glass curtain walls, deforming the glass.
[00:05-00:10] Shot 2: Absurd interaction (The Interaction).
The camera switches to ground-level perspective. Traffic flows on the street, traffic lights flashing. The giant cat lowers its head, bringing its huge cat face close to the ground, curiously sniffing a bus waiting at a red light.
Action: The bus driver calmly reaches out and pets the giant cat's nose. The cat sneezes, instantly blowing away roadside leaves and pedestrians' hats (wind effect).
[00:10-00:15] Shot 3: Memetic ending (The Punchline).
The giant cat finally squeezes past the buildings and sits down on a cross-river bridge, causing the bridge deck to sink slightly (physical feedback).
Narrative sense: It lazily lies down and starts grooming itself, blocking the entire evening rush hour traffic. The camera finally freezes on its innocent big eyes.
```

### 6. Surrealistic Documentary Style
*by [@johnAGI168](https://x.com/johnAGI168)*

```
【Style】Mockumentary (Vlog Style), hyperrealism, fixed-camera real-shot feel, natural lighting, with a slight suspenseful comedy tone.
【Duration】15 seconds
【Main Character】An ordinary young beautiful woman, in front of the bathroom sink at home.
[00:00-00:06] Shot 1: Daily setup (Normalcy).
Scene: In front of a regular bathroom mirror.
Action: The protagonist is brushing her teeth, mouth full of foam. She makes various funny faces (squinting, eyebrow-wiggling) at the mirror while brushing her teeth.
Key detail: At this point, the reflection in the mirror is completely normal, movements synchronized.
[00:06-00:11] Shot 2: BUG appears (The Glitch).
Action: After brushing teeth, the protagonist lowers her head to spit out foam, then turns around to leave the bathroom.
High-impact moment (core climax): Just as the protagonist's real body has turned and left the mirror frame, the "reflection" in the mirror **doesn't move**! That "reflection" still maintains the tooth-brushing pose, even mischievously raising eyebrows at the camera with a bad smile, staying for a full 2 seconds, before suddenly panicking and "fast-forwarding" to catch up with the original body's movements before disappearing.
Director's note: Must create an extremely realistic "network delay" feel, as if the reflection has independent consciousness.
[00:11-00:15] Shot 3: Comedic callback (The Punchline).
Action: The protagonist, who has already walked to the door, seems to sense something is wrong, suddenly turning back to look at the mirror.
Result: The mirror has now completely returned to normal, completely empty, only reflecting the opposite wall. The protagonist scratches her head in confusion, showing a life-questioning expression toward the camera. The frame freezes on the protagonist's confused face (comedy effect).
```

### 7. Nezha and Ao Bing Ice-Fire Clash (Space-Time Folding)
*by [@Adam38363368936](https://x.com/Adam38363368936)*

```
Act 1: Stillness and Burst (Testing Acceleration from Standstill)
Visual: Close-up. Nezha's Red Armillary Sash gently sways in the wind with sparks flying. The camera suddenly zooms out rapidly.
Action: Nezha suddenly kicks off the ground, causing the earth to shatter.
Visual Focus: Testing Seedance 2.0's simulation of debris trajectory, and the transition from stillness to ultra-high-speed movement.

Act 2: Attribute Transition (Testing Match Cut Editing)
Visual: Nezha swings his Fire-Tipped Spear in a sweeping motion, creating a circular ring of flames.
Transition Design: The flame ring seamlessly transforms into Ao Bing's rotating ice blade while spinning.
Action: The camera follows the rotation axis of the weapons, achieving an instant, smooth transition from red tones to blue tones.

Act 3: Fierce Battle Interaction (Testing Physics Collision and Cinematography)
Visual: Mid-shot from the side. The Fire-Tipped Spear and ice sword collide in mid-air.
Action: Sparks and ice fragments explode simultaneously. Ao Bing's body moves like a dragon, spiraling upward around a fire pillar; Nezha inverts in the air, feet-first toward the ground on his Wind-Fire Wheels.
Visual Focus: Testing whether the model's limbs break down during "high-speed dueling" of the two characters.

Act 4: Ultimate Transition (Testing Space Folding)
Visual: Nezha punches and shatters an ice wall.
Transition Design: The shattered ice crystals transform into dancing red leaves or fire feathers in the air. The camera passes through the ice fragments and instantly cuts to the next scene.
Visual Focus: Testing Seedance 2.0's logical continuity using particle continuity.
```

### 8. Otter Mecha Anime Battle (Mech vs. Octopus)
*by [@emollick](https://x.com/emollick)*

```
An anime where an otter goes into a large mech, with lots of quick shots of mechanical parts and gears turning. The otter gives a grim thumbs up, and then pilots the mech, flying into battle against an octopus made of marble.
```

### 9. Motion Graphics
*by [@BFAVicky](https://x.com/BFAVicky)*

```
Create motion graphics animation inspired by traditional animation techniques. Based on the three examples shown, develop an animated sequence that captures the essence of classic animation while leveraging Seedance 2.0's advanced capabilities.
```

### 10. Van Gogh Post-Impressionism Style Animation
*by [@johnAGI168](https://x.com/johnAGI168)*

```
【Style】Van Gogh Post-Impressionism oil painting, thick paint texture (Heavy Impasto), signature swirling brushstrokes, dreamy feel, high saturation blue-yellow contrast.
【Duration】15 second animation
[Visual Content] This is a completely dynamic world made of thick oil paint.
Sky: In the deep blue night sky, huge yellow celestial bodies and crescent moon are surrounded by radiating short brushstrokes, nebulae swirling wildly in the air like rushing rivers (Swirling motion).
Foreground: On the left is a huge cypress tree, twisted like burning black flames, shooting up to the sky.
Background: A sleeping town in the valley, windows of houses emit warm, circularly painted yellow light. The entire scene slowly flows and breathes following the direction of brushstrokes.
```

### 11. Tournament of Power with Famous Anime Characters
*by [@NACHOS2D_](https://x.com/NACHOS2D_)*

```
A massive cosmic arena forms in a blinding void, Tournament-of-Power scale. Crowds from countless universes roar.
At the center stands the narrator: Gintoki Sakata, relaxed, wooden sword on his shoulder, bored eyes, sharp tongue.
He announces the rules casually, almost mocking fate: "This tournament decides the strongest. Winner gets a harem." Beat. The crowd explodes. Gintoki sighs. "Yeah, yeah. Don't look at me like that. I didn't write the rules."
The camera glides to elevated platforms revealing the women of legend, all clearly unimpressed in different ways:
Bulma adjusts her device, already annoyed.
Android 18 crosses her arms, deadpan.
Hinata watches quietly, composed.
Sakura cracks her knuckles.
Nami smiles like she's already planning something.
Boa Hancock looks away, offended by existence itself.
Mikasa doesn't react. At all.
Erza stands like a judge.
Nico Robin smiles politely—dangerously.
Rukia tilts her head, curious.

Gintoki points. "First match. Try not to destroy the universe before lunch."
Two tunnels ignite.

From the left: Saitama walks out slowly, hands in pockets, face empty. He looks around. "Huh. This again."
From the right: Goku steps forward, serious, focused, sensing something deeply wrong. "You're strong… but you look like you don't care."
Close-ups alternate. Dust rises. Energy crackles.
Gintoki stands between them.
"Alright. Bald guy who's bored versus spiky guy who lives for this."
Lights drop.
Power surges.
Comedy and catastrophe collide.
```

### 12. Chinese New Year Gala Style: Zhen Huan & Hu Fei Show
*by [@johnAGI168](https://x.com/johnAGI168)*

```
10 second Chinese New Year Gala style stage performance: "Zhen Huan & Hu Fei Talk Show"

0–2 seconds:
Medium two-shot.
Stage overall is "living room sketch" setting, but surrounded by grandiose New Year red-gold LED screens.
Zhen Huan (left) and Hu Fei (right) sit side-by-side on a modern talk show sofa.
 Key historical accuracy requirement: Both are dressed in magnificent, clearly distinct Qing Dynasty court robes with standing collars, intricate embroidery; hairstyles are authentic "big pull horns" or "dot heads" with tassel decorations.
Hu Fei appears casual, holding a pickled cucumber to bite, fingers wearing long golden nail guards (finger guards).

2–4 seconds:
Shot switches to over-the-shoulder (OTS), perspective on Hu Fei.
Hu Fei exaggerates eye-rolling (classic "eye roll" expression).
She holds a pickle with her long nail guards while pointing and gesturing, speaking with an arrogant tone (lip-sync):
"This year's KPI is beating these little devils again, what aesthetic does that old man emperor know?"

4–6 seconds:
Quickly switch to Zhen Huan's over-the-shoulder shot (OTS).
 Contrasting detail: Zhen Huan wears a modern white Bluetooth earphone on one ear (strong contrast with ancient jewelry), holding a thin tablet computer sliding with her hand.
She responds calmly, professionally (lip-sync):
"Sister don't be angry, this is called workplace involution. I'm thinking of quitting to sell 'Truth Serum' (healing balm)."

6–8 seconds:
Close-up shot on the coffee table between the two.
A modern plastic pearl milk tea cup with "One Red Stripe" (a famous punishment from the drama) printed on it sits next to a traditional porcelain vase.
Lens quickly swings back to the two.

8–10 seconds:
Full stage panorama.
Audience laughter effect (presented through lighting changes/gap lights).
Hu Fei poses for the final freeze: leg crossed, chin lifted, eye-rolling again.
Zhen Huan smiles professionally toward the camera like a news anchor.
Golden confetti falls from the air.
Festival red atmosphere reaches its peak.
Style and atmosphere:

**Visuals:** High saturation New Year red and gold tones
**Costumes:** Museum-grade Qing Dynasty court attire (silk, fine embroidery, heavy headwear)
**Core contrast:** Formal Qing court protocol × Relaxing workplace/sketch performer attitude
**Cinematography:** Sharp rhythm, clear comedy points, sketch-style editing
**Aspect ratio:** 16:9
```

*Add yours via a PR — keep the original author's credit. See [Contributing](#contributing).*

---

## Related Model Guides
Part of the WaveSpeedAI **Awesome Model** series — one guide per frontier model, all runnable through one API:

- 🎬 [awesome-seedance-api](https://github.com/WaveSpeedAI/awesome-seedance-api) — ByteDance Seedance video *(this repo)*
- 🌊 [awesome-wan-api](https://github.com/WaveSpeedAI/awesome-wan-api) — Alibaba Wan video
- ⚡ [awesome-minimax-h3-api](https://github.com/WaveSpeedAI/awesome-minimax-h3-api) — MiniMax Hailuo H3 video
- 🎞️ [awesome-kling-api](https://github.com/WaveSpeedAI/awesome-kling-api) — Kling video
- 🖼️ [awesome-seedream-api](https://github.com/WaveSpeedAI/awesome-seedream-api) — ByteDance Seedream image
- 🎨 [awesome-gpt-image-api](https://github.com/WaveSpeedAI/awesome-gpt-image-api) — OpenAI GPT Image
- 🍌 [awesome-nano-banana-api](https://github.com/WaveSpeedAI/awesome-nano-banana-api) — Google Nano Banana image

---

## Contributing
PRs welcome:
1. Reusable prompts (`{placeholders}` for swappable parts).
2. **Credit the original author** with a link.
3. No output images unless you own and can license them.

## License
[CC0-1.0](LICENSE) — text & prompts are free to use. Model outputs follow the model provider's and [WaveSpeed](https://wavespeed.ai)'s terms.

---
<p align="center"><sub>Maintained by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedance-api">WaveSpeedAI</a> — the fastest way to run frontier image & video models via one API. <a href="https://wavespeed.ai/seedance-2-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedance-api"><b>Run Seedance →</b></a></sub></p>
