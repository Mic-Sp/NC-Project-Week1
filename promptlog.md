# Prompt Log: Vivi's Dream

## Prompt 1
**Context:** I am building a single-page web tech demo for an AI upscaling project called "Vivi's Dream" (a Final Fantasy IX FMV remaster). I am building this iteratively using a strict build loop where I must understand every line of code and stay firm within the constraints of the design.

**Task:** Generate the vanilla HTML, CSS, and JS structural files. Create the main page layout structure with empty container div or section tags for exactly three sections: "The Dream", "The First Attempt", and "The Direction Forward", plus one header for a title at the top of the page and one final container for a call to action at the bottom.

**Format:** The files should be named `index.html`, `style.css`, and `script.js`.

**Constraint:** Do not write any content, text, or advanced styling for the sections yet. Only provide the structural skeleton and link the files together. Do not use any external frameworks or bonus features.

---

## Prompt 2
Let's create the first section utilizing this text and image. The image should be placed above the text.

> "Final Fantasy IX has remained my favorite game of all time, but its breathtaking full-motion videos are still trapped behind the heavy compression and standard-definition limits of the year 2000. Vivi's Dream was born from a simple desire: to bring these iconic cinematics into the modern era with the visual fidelity they deserve, without sacrificing an ounce of their original soul. Rather than settling for a generic smoothing of nostalgic memories, this project is about honoring the world of Gaia and revitalizing every frame so the story, atmosphere, and emotion feel just as vivid on modern displays as they did the very first time we saw them."

---

## Prompt 3
**Task:** Now that we have the content of section 1, lets add some CSS styling in `style.css` and make any necessary changes in `index.html` to ensure they are linked properly. 
*   **Section blocks** - Define the styles for the generic section container class used above. It needs a smooth visual adding depth and a noticeable outline. Add significant padding, rounded corners, and a background color that complements the nighttime background image. Apply a noticeable but soft border. Also include a soft, wide box-shadow effect to provide the requested visual depth. 
*   **Image style** - Style the image placed in Section 1 above the paragraph. Make the image horizontally centered within the section block. Apply the necessary CSS attributes to ensure the image resizes smoothly with the browser window - ensuring that when the image resizes the transition is visually fluid.

**Constraint:** Stay in scope. Style only these elements using vanilla CSS, do not add other details not discussed. Add comments to the code so I can understand what is happening with each section.

---

## Prompt 4
**Task:** Add stylization to the page header that compelements the section style but stands out as distinct.

**Constraint:** Stay in scope. Style only these elements using vanilla CSS, do not add other details not discussed. Add comments to the code so I can understand what is happening with each section. Edit only `index.html` and `style.css` as necessary.

---

## Prompt 5
**Task:** Change the font color for the 3 sections to an off-white color that stands out against the dark background with a low level of text shadowing that matches the overall aesthetics of the page. Also, pick a background color that matches the aesthetics of the dark section boxes while keeping the depth a prominent feature.

**Constraint:** Stay in scope. Style only these elements using vanilla CSS, do not add other details not discussed. Add comments to the code so I can understand what is happening with each section. Edit only `index.html` and `style.css` as necessary.

---

## Prompt 6
**Task:** Add the content to section 2. We will start with the text first. 

> "The initial phase of the project tackled the FMVs through an automated super-resolution pipeline using a custom-tuned Real-ESRGAN model. Raw cutscene video was demuxed into uncompressed frame sequences via FFmpeg, passed through model weights optimized to suppress heavy 240p compression artifacts, and reassembled with lossless audio. While this approach effectively suppressed macroblocking and aggressive color banding, it quickly exposed the fundamental limits of traditional GAN-based upscalers: Real-ESRGAN can only interpolate and smooth existing pixel clusters, incapable of inferring fine architectural textures, fabric weaves, or cinematic lighting that never existed in the source renders. Ultimately, the process gave scenes an unnatural, "painted-over" look while introducing distinct visual artifacts—most notably smeared pixels, blurred micro-details, and temporal inconsistencies across the individual frames and finalized video." 

This should be a single paragraph and below we will have bullet points for each of the following.

*   **Software Stack**
    *   **Frame Demuxing & Assembly:** FFmpeg (lossless image sequence extraction, color tagging, and audio mapping)
    *   **Upscaling Engine:** Custom Real-ESRGAN architecture using fine-tuned model checkpoints
    *   **Inference Runtime:** Python, PyTorch (CUDA-accelerated batch execution), and OpenCV
    *   **Encoding & Delivery:** FFmpeg (NVENC H.265 / ProRes encoding for minimal generation loss)
*   **Hardware Profile**
    *   **Machine:** Lenovo Legion Pro 7i Gen 10
    *   **Processor:** Intel Core Ultra 9 275HX
    *   **GPU:** NVIDIA GeForce RTX 5080 Laptop GPU (16GB GDDR7 VRAM)
    *   **System Memory:** 32GB DDR5 RAM

**Constraint:** Stay in scope. Add the text content to `index.html`. Use CSS to stylize the bullet points in `style.css`. Add comments to the code so I can understand what is happening with each section.

---

## Prompt 7
**Task:** Add a clean media container above the text of section 2 that can play a video from YouTube seamlessly (https://www.youtube.com/watch?v=OFzxl3kdh3c). Ensure there is no layout shift while the video is loading. Style the video container to match the depth established for the sections and use a modern aspect-ratio of 16/9.

**Constraint:** Stay in scope. Do not use any external JS libraries or third-party players. Adhere strictly to vanilla HTML/CSS/JS. Provide a line-by-line explanation of the method used. Edit `index.html`, `script.js`, and `style.css` only as needed to add the media.

---

## Prompt 8
**Task:** For the video container we just added, wrap the iframe in an outer container with hidden overflow. Scale the iframe slightly larger than the container (e.g., 115% to 120%) and offset its vertical position so the controls are cropped and it only shows the video without the youtube controls.

**Constraint:** Stay in scope. Stick to vanilla HTML/CSS. Make changes to `index.html` and `style.css` only as needed for the change to the container. Add comments detailing exactly what the code is doing.

---

## Prompt 9
**Task:** Add the content for section 3. Start with the text:

> "Moving beyond the limitations of traditional super-resolution means abandoning simple pixel interpolation in favor of true generative reconstruction. To eliminate the smoothed, painted-over artifacts and smeared pixels introduced by GAN models, the next phase of Vivi's Dream transitions the entire workflow into a generative pipeline powered by FLUX.1 [dev] within ComfyUI. Instead of guessing details from corrupted low-resolution data, this architecture uses guided diffusion to rebuild each frame from the ground up while strictly honoring the cinematic direction of the original cutscenes." 

And have bullet points for the following below.

*   **Next-Gen Pipeline Architecture**
    *   **Generative Engine (FLUX.1 [dev] via ComfyUI):** Replaces legacy upscaling networks with a high-parameter diffusion model running inside a modular node graph, synthesizing realistic textures and volumetric light rather than stretching existing pixels.
    *   **Deterministic Geometry Control (ControlNet):** Extracts depth maps, edge lines, and character silhouettes directly from the original PS1 frames, anchoring the generative model so camera perspective and character anatomy remain structurally identical without visual hallucination.
    *   **Aesthetic Accuracy (Custom LoRA Training):** Integrates custom-trained Low-Rank Adaptation (LoRA) weights focused on Final Fantasy IX's distinct storybook aesthetic, precisely directing the synthesis of Vivi's coarse fabric weave, Alexandria’s weathered cobblestone, and stylized architectural proportions.
    *   **Temporal Coherence & Sequence Assembly (FFmpeg & Latent Blending):** Sequences cutscene frames into batches with linked latent noise seeds and optical flow masking, using FFmpeg for pre-processing extraction and final high-bitrate master encoding to prevent inter-frame flickering.

**Constraint:** Stay in scope. Add the text content to `index.html`. Use CSS to stylize the bullet points in `style.css`. Add comments to the code so I can understand what is happening with each section.

---

## Prompt 10
**Task:** In section 3 above the text, Add 2 images for a side-by-side comparison: `assets/garnet.png` and `assets/garnet-rerender.png`. Use a similar format/style as that used in section 1 for the image.

**Constraint:** Stay in scope. Stick to the same methods used for previous image. Modify `index.html` and `style.css` as needed to add the images to the page.

---

## Prompt 11
**Task:** Add a header for each of the 3 sections in `index.html` stating what that section is, i.e. "The Dream", "The First Attempt", and "The Direction Forward". Use the same css styling for each of these, using a light goldish color with a subtle shadow/glow effect.

**Constraint:** Stay in scope. Add the text content to `index.html`. Use CSS to stylize the headers in `style.css`.

---

## Prompt 12
**Task:** I'm not too fond of the gold glow, lets make the section headers' style match that of the page header.

**Constraint:** Stay in scope. Only change the css styling for the headers as needed.

---

## Prompt 13
**Task:** The final element is the call to action at the end of the page. Create a button in a style that matches the rest of the page that says "View Professional Profile". The button should link to `https://www.linkedin.com/in/michael-sprague-it/` and open in a new tab with a noreferrer attribute. Add a smooth hover animation that matches the depth and lighting of the previous sections.

**Constraint:** Stay in scope. Do not make changes to any other sections and only change what is necessary to add the button and the desired style effects.

---

## Developer Notes & Fixes

### Errors encountered
*   The model failed to make changes to `style.css`, possibly because I hadn’t saved previous edits.
*   The model left empty rulesets in the CSS file that were never used; manually deleted rulesets.
*   The model cropped the video too much; reverted back to the previous version.

### Small fixes applied
*   Changed youtube embedded url to limit controls and autoplay.
*   Didn’t like the side-by-side comparison for section 3; removed old image and went with the modern render.
