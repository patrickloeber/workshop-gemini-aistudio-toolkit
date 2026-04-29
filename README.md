# 🧪 Prompt Guide

**Research to Reality: Mastering the Gemini & AI Studio Toolkit**

This guide contains all the prompts and instructions for the live demos and hands-on exercises. Follow along with the instructor or try them yourself in [Google AI Studio](https://aistudio.google.com).

---

## Table of Contents

1. [Part 1 — Model Demos](#part-1--model-demos)
2. [Part 2 — Creative & Media Generation](#part-2--creative--media-generation)
3. [Part 3 — Voice, Music & Real-Time](#part-3--voice-music--real-time)
4. [Part 4 — Tools & Ecosystem](#part-4--tools--ecosystem)
5. [Part 5 — Vibe Coding in AI Studio](#part-5--vibe-coding-in-ai-studio)
6. [Part 6 — Gemini API + Antigravity](#part-6--gemini-api--antigravity)

---

## Part 1 — Model Demos

**Where:** [ai.studio](ai.studio)

### Demo 1: Gemini 3.1 Pro — Video Understanding + Coding

**Model:** `Gemini 3.1 Pro`

**Input:** Enter this YouTube video → https://youtu.be/4iEF6JXeZqI?si=rvdOvizL6jH8_EQZ

**Prompt:**

```
Draw this play and all the movements step by step like a coach drawing it
on a whiteboard. Output as a storyboard in HTML.
```

**What to notice:** Pro's ability to understand video content, extract complex spatial information, and produce structured HTML output in a single shot.

---

### Demo 2: Gemini 3 Flash — Invoice Extraction

**Model:** `Gemini 3 Flash`

**Input:** Upload an invoice image (can also be a PDF) → `example-data/invoice-7eleven.png`

**Prompt:**

```
Extract all items from this invoice and return it as json,
everything should be english.
```

**Follow-up:** Enable *Thinking* (minimal) and re-run to compare quality.

**What to notice:** Flash is fast and great for structured extraction tasks. The thinking mode can improve accuracy with minimal latency cost.

---

### Demo 3: Gemini 3.1 Flash-Lite — Audio Transcription

**Model:** `Gemini 3.1 Flash-Lite`

**Input:** Upload the audio file → `example-data/sports-injuries.mp3`

**Prompt:**

```
Transcribe this file.
```

**What to notice:** Flash-Lite is the cheapest and fastest model. For straightforward tasks like transcription, it delivers great results at minimal cost.

---

## Part 2 — Creative & Media Generation

### Demo 4: Nano Banana — Image Reimagination

**Model:** `Nano Banana 1`

**Input:** Upload the image → `example-data/pat.jpg`

**Prompt:**

```
Reimagine this person as if they were living in the 1980s.
```

**What to notice:** Nano Banana can take an image as input and generate a creative new image based on it.

---

### Demo 5: Nano Banana + Search Grounding — Personalized Pixel Art

**Model:** `Nano Banana 2` or `Nano Banana Pro`

**Settings:** Enable **Search Grounding** (Google Search as a tool).

**Prompt:**

```
Search the web then generate an image of isometric perspective,
detailed pixel art that shows the career of Patrick Loeber.
```

**What to notice:** The model searches the web first to gather real-world context, then uses that information to generate a grounded, factual image.

---

### Demo 6: Meta-Prompting for Image Generation

This is a two-step workflow where one model writes the image prompt, and another generates the image.

**Step 1 — Generate the prompt**

**Model:** `Gemini 3 Flash`

```
Give me a short text-to-image prompt for a professional image of a
lemonade that I can use for an ad in Korea.
```

**Step 2 — Generate the image**

**Model:** `Nano Banana 2`

Use the output from Step 1 as your prompt.

**What to notice:** Using a language model to craft the image prompt often produces better, more targeted results than writing the prompt yourself.

---

### Demo 7: Veo 3.1 Fast — Cinematic Video Generation

**Model:** `Veo 3.1 Fast`

**Prompt:**

```
Create an ultra-photorealistic, cinematic video titled "The Chocolate Echo."
The video is a journey through time, connected by the singular, universal
moment of pure joy experienced when a person tastes chocolate for the first
time in their era. The core visual anchor is a seamless "match cut" transition
that occurs at the peak moment of tasting — as a character's eyes close in
bliss, the scene instantly transforms to a new time and place.

Cinematic Style:
- Shot on ARRI Alexa with vintage anamorphic lenses
- Rich, warm color grading with high dynamic range
- Slow dolly-ins, gentle tracking shots, shallow depth of field
- Pacing: contemplative → emotional crescendo

Scenes:
1. (2s) Misty Mesoamerican jungle — a Mayan priestess grinds cacao on
   a stone metate, takes a sip, eyes close in bliss → MATCH CUT to...
2. (3s) Candle-lit Baroque salon, 17th century Paris — a French aristocrat
   in silk delicately sips hot chocolate from a porcelain cup,
   eyes close → MATCH CUT to...
3. (3s) Futuristic Tokyo-style megacity, 2099 — a woman in a silver
   jumpsuit tastes "real, ancient chocolate," a single tear rolls down
   her cheek, eyes close → RAPID MONTAGE
```

**What to notice:** Veo can handle rich, detailed cinematic descriptions with specific shot composition, era-accurate settings, and narrative structure.

---

### Demo 8: Flow + Veo — Image-to-Video Animation

**Where:** [https://labs.google/fx/tools/flow/](https://labs.google/fx/tools/flow/)

**Input:** Upload the image → `example-data/pat.jpg`

**Prompt:**

```
Create an 8-second animation where this person waves and smiles.
```

**What to notice:** You can start from a still image and animate it into a video.

---

## Part 3 — Voice, Music & Real-Time

### Demo 9: Text-to-Speech (TTS)

**Reference guide:** https://www.fofr.ai/gemini-tts-guide

Try these prompts and compare the results:

**Basic:**

```
Hey there, I'm a new text to speech model, and I can say things
in many different ways. How can I help you today?
```

**With tone control:**

```
[bored] Hey there, I'm a new text to speech model...
```

```
[very fast] Hey there, I'm a new text to speech model...
```

**Multilingual (Korean 🇰🇷):**

First, use a text model to translate:

```
Translate this to Korean: Hey there, I'm a new text to speech model,
and I can say things in many different ways. How can I help you today?
```

Then generate speech from the Korean text:

```
[very fast] 안녕하세요! 저는 새로운 텍스트 음성 변환(TTS) 모델이에요.
다양한 방식으로 말을 할 수 있답니다. 오늘 어떻게 도와드릴까요?
```

**What to notice:** Tone tags like `[bored]`, `[very fast]`, `[whispering]` give you fine-grained control over delivery. Multilingual support works seamlessly.

---

### Demo 10: Lyria — Music Generation

**Where:** [gemini.google.com](https://gemini.google.com)

**Prompt idea:**

```
K-pop + Startup scene in Korea
```

**What to notice:** Lyria generates full music tracks from text descriptions. Think about using this for product demos, videos, or app soundtracks.

---

### Demo 11: Gemini Live — Real-Time Conversation

**Where:** [ai.studio/live](https://ai.studio/live)

Have a real-time voice conversation with Gemini. Try using your microphone and camera for a multimodal live session.

**What to notice:** Real-time streaming, turn-taking, and how naturally the model handles back-and-forth conversation.

---

## Part 4 — Tools & Ecosystem

### Demo 12: Embeddings — Multimodal Search

**Where:** [ai.studio/apps/bundled/multimodal_search](https://ai.studio/apps/bundled/multimodal_search)

Explore multimodal search using `gemini-embedding-2`. Upload documents and images, then search across them using natural language queries.

---

### Demo 13: Project Genie

**Where:** https://labs.google/projectgenie

Explore Genie for interactive 3D world generation.

---

### Demo 14: Gemma 4 — Local Agent

**Reference:** https://patloeber.com/gemma-4-pi-agent/

Run a local coding agent powered by Gemma 4 on your own machine.

---

## Part 5 — Vibe Coding in AI Studio

### Demo 15a: Build AI-Native Apps in AI Studio

AI Studio supports user input like file upload, webcam, and microphone out of the box. Try building these apps:

**App 1 — Pixel Art Generator:**

```
Build me an app where I can upload a picture or use my webcam.
It should use Nano Banana to create a pixel art image for me.
```

**App 2 — Sports Commentator (Live API):**

```
Create an app for me with the Live API where I can use my microphone
and webcam. Use a sports commentator.
```

**What to notice:** You can ship interactive, AI-native apps directly from AI Studio without writing any code.

---

### Demo 15b: Brainstorm → Plan → Build Workflow

This is the full "vibe coding" workflow: brainstorm a problem, plan the solution, then build it.

**Step 1 — Brainstorm problems for your hobby:**

```
My hobby is: {hobby}. Brainstorm 4 distinct common problems or frustrations
people have with this hobby that could be solved with a simple web
or mobile app.

For each option, also create a one paragraph "Vibe Coding Prompt".

The prompt should be the starting prompt for an AI Coding agent in Google
AI Studio to build this initial MVP. It MUST start with "Create an app
that...". Do NOT mention specific tech stacks. FOCUS on the vibe and
functionality.

The app should have AI features from the Gemini API.
```

> 💡 Replace `{hobby}` with your actual hobby (e.g., running, cooking, photography).

**Step 2 — Get feedback on your idea (planning):**

```
I want to vibe code an app in Google AI Studio with the following
functionality: [describe your idea]. Is that feasible? If so, suggest
2-3 simple features that I can add. Ask me any questions to identify
the needs for my app.

If my idea is not feasible or simple, suggest how I can simplify my idea
and make it suitable to create in AI Studio. DO NOT create any code
for this step.
```

**Step 3 — Build it!** Use the vibe coding prompt from Step 1 or your refined idea from Step 2 in AI Studio to generate your app.

---

## Part 6 — Gemini API + Antigravity

### Demo 16: Interactions API — Build a Minimal Coding Agent

Use Antigravity (the AI coding assistant) with the Gemini Interactions API to build a coding agent.

**Setup — Add Gemini skills:**

Add skills from https://github.com/google-gemini/gemini-skills/ to one of these directories:

| Scope | Path |
|---|---|
| Workspace | `<workspace-root>/.agent/skills/<skill-folder>/` |
| Global | `~/.gemini/antigravity/skills/<skill-folder>/` |

**Prompt for Antigravity:**

```
Use the Interactions API and build me a minimal coding agent in Python
with the following tools: read_file, write_file, and list_dir.
```

**What to notice:** With the right skills installed, Antigravity can scaffold a fully functional AI agent with tool use in minutes.

---

## Useful Links

| Resource | URL |
|---|---|
| Google AI Studio | https://aistudio.google.com |
| Gemini Live | https://ai.studio/live |
| Multimodal Search | https://ai.studio/apps/bundled/multimodal_search |
| Project Genie | https://labs.google/projectgenie |
| Gemma 4 Local Agent Guide | https://patloeber.com/gemma-4-pi-agent/ |
| TTS Guide | https://www.fofr.ai/gemini-tts-guide |
| Gemini Skills (GitHub) | https://github.com/google-gemini/gemini-skills/ |

---

*Happy building! 🚀*
