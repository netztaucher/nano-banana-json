---
name: nano-banana-json
description: Use structured JSON to precisely control, edit, and restyle AI images using Gemini and Nano Banana Pro. Preserves exact style, composition, and character consistency through JSON extraction and injection.
origin: Brain
---

# Nano Banana JSON Steering

A technique to extract an image's "DNA" into structured JSON using Gemini (Nano Banana 2/Pro), allowing for precise editing, character consistency, and style transfers without losing original composition or style.

## When to Activate

- When editing specific details (colors, objects, clothing) in an generated image without changing its overall style or structure.
- When applying a specific photographic or illustrative style to new images.
- When generating consistent characters across multiple angles or scenes.
- When performing aspect ratio changes (outpainting) or upscaling without trial and error.

## Core Workflows

### 1. Consistent Image Editing (The "DNA" Extraction)
1. **Extract:** Provide the reference image.
2. **Prompt:** "Extract all the information from this image and convert it into structured JSON."
   *(Gemini generates a JSON block containing style, colors, objects, and spatial structure).*
3. **Modify:** Provide the original image again + Prompt: "Modify the image based on the following JSON data. \\n\\n [Insert modified JSON here]".
4. **Action:** Manually modify specific properties in the JSON (e.g., changing `"color": "black"` to `"color": "red"` for a lounge chair) and submit. The overall structure remains completely intact.

### 2. Style Transfer & Character Consistency
1. **Extract Style:** Provide a reference image (e.g., a portrait with a specific style).
2. **Prompt:** "Describe the photography techniques in this image in JSON format."
   *(Gemini outputs JSON including lighting, composition, color palette, optics, focus, and post-processing).*
3. **Target Character:** Provide 2-3 photos of the target person from different angles to establish facial consistency.
4. **Generate:** Prompt: "Generate a photo of this person based on the following JSON file. \\n\\n [Insert Style JSON here]".

### 3. Iterative Element Tweaks via Prompting
If the user prefers not to manually edit the JSON:
1. **Prompt:** "Add a suit and a red shirt to this person in the JSON prompt. \\n\\n [Paste previous JSON]"
2. **Iterate:** Download the newly generated image and upload it again to maintain maximum consistency, then hit submit with the new instructions.

### 4. Direct Brush & Text Edits
For precise spatial edits using Gemini's native UI:
1. **Annotate:** Provide the image and click it to open built-in tools.
2. **Point:** Select the brush tool and draw a pointer/arrow to the specific area.
3. **Instruct:** Use the text tool to write instructions directly on the image (e.g., "turn the couch red" or "put a teddy bear on the chair").
4. **Cleanup:** Once generated, if the instruction text remains visible in the final image, prompt: "Remove the red text" to clean it up.

### 5. Aspect Ratio & Outpainting (Pro Features)
- **Resize:** Prompt: "Aspect ratio 9:16" (or "1:1", "21:9"). Gemini resizes the canvas instantly.
- **Outpaint:** Prompt: "Generate a full body image of this person wearing jeans and holding a briefcase, 9:16 aspect ratio."
- **Upscale:** Prompt: "Upscale this image to 4K."

## Best Practices
- **Re-uploading:** Always download your latest generated image and re-upload it when making further iterative changes. This reinforces the "source of truth" and locks in consistency.
- **Multiple Angles:** When establishing a new character, providing 2-3 photos from different angles significantly improves facial recognition and consistency.
