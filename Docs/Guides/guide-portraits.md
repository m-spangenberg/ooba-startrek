# Portraits

To generate your own character portraits using Stable Diffusion and ControlNet, follow these steps:

1. Make sure you have a working installation of [Automatic1111's stable-diffusion-web-ui](https://github.com/AUTOMATIC1111/stable-diffusion-webui).

2. Download the [Stable-Diffusion 1.5](https://huggingface.co/runwayml/stable-diffusion-v1-5) model from HuggingFace and place it in the `models` folder of the stable-diffusion-web-ui.

3. Add the [ControlNet extension](https://github.com/lllyasviel/ControlNet) from inside the stable diffusion web UI. Here's a [video tutorial](https://www.youtube.com/watch?v=zrGLEgGFJY4) on how to do that.

4. Find and prepare a suitable 512x512 headshot of your character. You can use the examples provided in the `Docs` folder.

5. Start the stable diffusion web UI and navigate to the "IMG2IMG" tab.

6. Upload your headshot image to the web UI.

7. Enable ControlNet below the uploaded image and upload the same headshot image to ControlNet as a reference.

8. Set the preprocessor to `reference_only` and fill all the desired parameters. Don't forget to a run the preprocessor.

9. Use the following prompt and configurations to generate your portraits:

```bash
# - prompt: Portrait of, Star Trek, the next generation, intricate, elegant, highly detailed, digital painting, artstation, concept art, smooth, sharp focus, illustration, art by artgerm and greg rutkowski and alphonse mucha and william - adolphe bouguereau

# - negative prompt: Muted colors, dripping paint, 2 heads, 2 faces, cropped image, out of frame, deformed hands, twisted fingers, double image, malformed hands, multiple heads, extra limb, ugly, poorly drawn hands, missing limb, disfigured, cut off, low res, blurry, bad anatomy, disfigured, poorly drawn face, mutation, mutated, floating limbs, disconnected limbs, disgusting, poorly drawn, mutilated, mangled, extra fingers, duplicate artifacts, missing arms, mutated hands, mutilated hands, cloned face, malformed, text, logo, wordmark, writing, heading, signature, long neck

# - configurations: Steps: 30, Sampler: Euler a, CFG scale: 14.5, Seed: 3068781511, Size: 512x512, Denoising strength: 0.75, ControlNet: "preprocessor: reference_only, model: None, weight: 1, starting/ending: (0.25, 0.5), resize mode: Crop and Resize, pixel perfect: True, control mode: Balanced, preprocessor params: (512, 64, 64)"
```

Notes: Make sure to adjust the prompt and configurations according to your desired style and settings. Making the resolution slightly smaller (448x448) will speed up generation, and yield more interesting results. It is possible to get more accurate likeness by injecting the [actor name] as [character name], eg: Patrick Stewart as Jean-Luc Picard, and swapping out the show title, eg: next generation. So the start of the prompt would appear as: `Portrait of Patrick Stewart as Jean-Luc Picard, Star Trek, the next generation`. Cranking up the CFG from 14.5 to 18.5 will also stick more closely to the source image, dial it back to 7-9 for more creative portraits.

Enjoy creating your own unique portraits using Stable Diffusion and ControlNet!