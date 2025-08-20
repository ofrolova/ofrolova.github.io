+++
date = '2024-12-12T09:43:40-04:00'
draft = false
title = 'Gen AI Highlights of 2024: A Year in Review'
+++

As 2024 wraps up, I wanted to share a quick rundown of the major generative AI developments that stood out this year. This post is based on a presentation I gave back in December, drawing from research and hands-on experience applying these tools to projects (especially at the prototype stage) in the video game industry.  

Let’s dive in.

## GPT-4o: Smarter, Clearer, More Capable

The biggest leap came from [OpenAI](https://openai.com) with the release of GPT-4o. What makes this model stand out isn’t just its speed but how well it reasons. It walks you through its logic step by step, which makes it especially useful for complex math, debugging code, or explaining difficult concepts.

What’s even more interesting is where the next wave of OpenAI models is heading. In evaluation tests, their reasoning-focused model has started to perform on par with PhD-level researchers in subjects like physics, chemistry, and biology. The jump in math and coding ability has been even more striking: in one qualifying exam for the International Mathematics Olympiad, GPT-4o managed to solve about 13% of problems, while the reasoning model got to 83%. In competitive programming trials on [Codeforces](https://codeforces.com), it ranked around the 89th percentile.  

Alongside this, OpenAI also launched o1-mini — a smaller reasoning model designed to be both faster and more affordable. It’s tuned heavily toward coding tasks, coming in at about 80% cheaper to run than o1-preview. For teams that need reasoning without the overhead of full world knowledge, o1-mini is shaping up to be a cost-effective option.

Another big shift was the introduction of OpenAI Canvas, a new interface designed for writing and coding directly with ChatGPT. It’s a sign OpenAI is moving toward more specialized workflows. Personally, I still lean on [Cursor.ai](https://cursor.sh), especially with [Anthropic’s Claude](https://www.anthropic.com/claude) code interpreter integrated. It offers a better coding experience overall, but Canvas is a step in the right direction.

![Alt text for accessibility](/images/code_4o.png "Optional hover title")

They also rolled out voice and image recognition, pushing toward a truly multimodal AI assistant. Voice input is smoother than before (though still best in English), and image interpretation has gotten smarter (though not flawless yet).

## Image Generation: Flux AI and Recraft

### [Flux AI](https://bfl.ai/)

Flux AI stayed ahead of the curve in 2024, delivering consistently high-quality image generation and flexible integration via API. What sets it apart:

- Trained on licensed/public domain datasets  
- Works well with [Adobe](https://www.adobe.com) tools  
- Can be fine-tuned on domain-specific datasets  

But as long as we talk about image generation nothing works better than demonstration. To showcase its latest model, I used this prompt:

> *"A majestic castle perched on a rugged, mist-shrouded mountain, surrounded by an ancient forest glowing softly under a twilight sky. The castle's soaring towers and intricate spires are adorned with elven carvings and shimmering banners. A cascading waterfall flows beside the castle, feeding a crystal-clear river winding through the forest below. In the foreground, a stone bridge crosses the river, leading to the grand, vine-covered gates of the castle. The scene is illuminated by the soft golden glow of lanterns, with distant snow-capped peaks and a crescent moon adding to the Tolkien-inspired fantasy ambiance."*

![Alt text for accessibility](/images/castle.png "Optional hover title")

The result? Visually stunning. The model nailed atmospheric lighting, architecture, and fantasy detail with an impressive degree of coherence. That said, like all current models, it still stumbles on finer anatomical features like hands. For production art, human touch remains essential — but this is a major leap forward for concepting and iteration.

### [Recraft AI](https://www.recraft.ai) V3 

Recraft took everybody by surprise. You don’t see a small startup at the top of [artificialanalysis.ai](https://artificialanalysis.ai)’s leaderboard every day. 

![Alt text for accessibility](/images/recraftai.png "Optional hover title")

The model ended up dominating design-centric tasks. It’s the only image model in 2024 that generates vector-native (SVG) images, which means crisp, infinitely scalable assets straight out of the box.

Standout features include:

- Long-form, accurate text rendering (think logos, headlines, slogans)  
- Built-in tools for background removal, mockups, upscaling, and style merging  

If your work involves visual branding or web assets, Recraft is hard to beat. 

I also tested Recraft using the same fantasy castle prompt I had tried with Flux AI to push the limits of the model. The results were close: Flux AI produced more intricate architectural details, while Recraft leaned toward a more realistic overall look but dropped a few finer elements. Both were impressive in different ways. Check the [slides below](#slides-from-the-presentation) for more examples.  

![Alt text for accessibility](/images/castle_recraft.png "Optional hover title")

During the model testing stage I ran a second prompt describing an elf character to test models’ abilities with humanoid type characters. I happened to write the prompt in a gender-neutral way since I was much more interested if the model can produce a correct position of hands rather than whether it be a male or female elf. I used it across [DALL·E](https://openai.com/dall-e), Flux AI, and Recraft. Both DALL·E and Flux defaulted to a female elf, while Recraft generated a male one. Maybe it is a coincidence. But given that only Recraft’s founder is female, I couldn’t help but find it both funny and thought-provoking. Either way, it’s another reminder of how datasets, design choices, and maybe even culture subtly shape these tools.

## Video

### [RunwayML](https://runwayml.com)

Runway grew into a true multimedia platform. Beyond its well-known video generation tools, it now includes:

- Text-to-speech: Perfect for prototypes and cosept art presentation. 
- Camera angle and motion control: Instead of static, one-shot clips, you can define pans, zooms, and dynamic angles to create more cinematic sequences.
- Facial mimicry transfer: Upload reference footage of an actor, and Runway can map subtle facial expressions onto generated characters. I haven't used this one myself but worth mentioning. 

All of these can be combined in a single workflow. The platform is not replacing traditional 3D or video editing suites yet, but it’s getting close enough that for early iterations, it’s often faster and cheaper to go “AI-first” and polish later. 

<iframe width="560" height="315" 
src="https://www.youtube.com/embed/VRBOMOG2IZY?start=112" 
title="YouTube video player" frameborder="0" 
allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
allowfullscreen>
</iframe>

### Motion Brush by [Kling AI](https://app.klingai.com/)

This tool lets you animate static images with lifelike movement — ideal for breathing life into concept art. It’s intuitive, fast, and surprisingly accurate for stylized content.

### [HeyGen](https://www.heygen.com)’s Unlimited Looks

HeyGen allows you to create a realistic video avatar using just a few minutes of footage. For marketers and content creators, this makes producing personalized, scalable video content much faster and more cost-effective.

## Audio

### [Suno AI](https://www.suno.ai)

Suno nailed the niche of AI-powered music generation. It lets you create custom soundtracks in specific genres and moods without relying on stock libraries. For prototyping games or interactive experiences, this creates a tighter and more immersive feel from the start.

### [Google](https://illuminate.google.com/explore?pli=1) Illuminate

This lesser-known but highly promising tool turns written content into engaging audio conversations. It’s designed to simplify complex topics and make learning or onboarding more interactive. Think of it as a podcast generator for your documentation or product guides.

### [ElevenLabs](https://elevenlabs.io)

ElevenLabs keeps pushing voice synthesis forward. The realism and language support are so good now that we’ve been using it to generate multilingual placeholder dialogue for early builds. It’s definitely good enough for testing — sometimes good enough to keep.

## Developer Tools: Coding Workflows

Two tools have become essential parts of our stack:

### [Cursor.ai](https://cursor.sh)

Cursor is like having a senior developer on call 24/7. It goes beyond autocomplete: Cursor understands your entire codebase, makes meaningful suggestions, catches bugs, and helps implement new features. The Claude integration adds depth to its reasoning and makes it the best AI dev environment I’ve used so far.

### [GitHub Copilot](https://github.com/features/copilot)

Copilot keeps getting smarter. It’s great for generating boilerplate, writing unit tests, or jumping into unfamiliar code. Its integration into mainstream IDEs means it’s always right there when you need it. Between these two tools, we’ve seen major gains in both speed and quality.

## Wrapping Up

2024 wasn’t just about better models, it was about better workflows. The most exciting developments weren’t just smarter tools, but tools that slot seamlessly into how we already work.

If you’re experimenting with generative AI or planning to adopt it more fully, now’s the time. The tech has matured to the point where it can genuinely accelerate creative and technical work — not just impress in demos.

---

## Slides from the Presentation

You can view the full slide deck here:  
[Open the slides on Google Drive](https://docs.google.com/presentation/d/1n9pot616svMK5U0GrL93E6_eYThGCG9b7S4zZthiXPY/present)
