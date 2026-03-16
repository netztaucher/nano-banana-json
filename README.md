# Nano Banana JSON Steering

This skill provides an advanced technique for AI image editing and consistency maintenance using Gemini (Nano Banana 2/Pro) via structured JSON extraction.

## Table of Contents
1. [Overview](#overview)
2. [Why use this?](#why-use-this)
3. [Core Capabilities](#core-capabilities)
4. [Additional Tools](#additional-tools)

## Overview
*This skill was inspired by and structurally adapted from [this excellent YouTube tutorial](https://www.youtube.com/watch?v=gbnmDRcKM0Q&list=WL&index=20&t=12s).*

By extracting the "DNA" of a generated or photographic image into JSON format, users can directly modify specific attributes (like color, material, or spatial properties) without altering the overall style or composition of the image.

This is especially helpful for:
- Avoiding the classic "ruined picture" scenario where tweaking a small detail drastically alters the rest of the image.
- Achieving character consistency across multiple generations.
- Extracting and transferring photographic or illustrative styles seamlessly.

## Why use this?
When using standard prompt descriptions, AI models re-interpret the whole scene from scratch. By supplying a structured JSON representation, Gemini essentially treats the instructions as a precise override for the existing "code" of that scene, ensuring all other variables remain locked.

## Core Capabilities
Refer to `SKILL.md` for exact workflow prompts.

*   **Targeted Editing:** Locate an object node in the JSON and flip a value (e.g., `"color": "red"`).
*   **Style DNA Extraction:** Create a prompt that details lighting, optics, and post-processing from a reference image to replicate its exact feel.
*   **Iterative Character Outfitting:** Supply base character shots and incrementally change their wardrobe using JSON parameters.

## The 6-Component Prompt Model
Nano Banana (Gemini 2.5 Flash Image / Gemini 3 Pro Image) uses LLM-integrated diffusion, meaning it doesn't just translate text to pixels; it understands syntax contextually. Through research, we've identified that the model responds best to a **six-component system**. 

When building or modifying your JSON DNA, ensuring these 6 pillars are explicitly defined guarantees predictable, repeatable style transfers:

1. **Subject definition:** What is the primary entity? (e.g., *a 30-year-old woman with curly hair*)
2. **Action/pose:** What is the subject doing? (e.g., *looking over her shoulder, drinking coffee*)
3. **Location/context:** Where does this take place? What is the environment? (e.g., *a crowded cyberpunk street at night*)
4. **Composition:** How is the shot framed? (e.g., *medium-full shot, low-angle perspective*)
5. **Style and film stock:** What is the artistic treatment? (e.g., *cinematic editorial, shot on medium-format analog film, Kodak Portra 400*)
6. **Camera and lighting:** What are the optical constraints? (e.g., *f/1.8 aperture, shallow depth of field, neon rim lighting*)

By mapping these six variables into your JSON structures, you take full control away from the AI's "guessing" and lock in your style.

## Additional Tools
The skill also covers native Gemini pro tools:
- Built-in brush and text overlays for quick spatial edits.
- Aspect ratio overrides (`9:16`, `1:1`, `21:9`) and Outpainting.
- Automatic upscaling to 4K resolution.

See `SKILL.md` for detailed instructions and prompting techniques.

## About
Created and maintained by [netztaucher | digital](https://netztaucher.com).
