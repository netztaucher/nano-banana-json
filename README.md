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

## Additional Tools
The skill also covers native Gemini pro tools:
- Built-in brush and text overlays for quick spatial edits.
- Aspect ratio overrides (`9:16`, `1:1`, `21:9`) and Outpainting.
- Automatic upscaling to 4K resolution.

See `SKILL.md` for detailed instructions and prompting techniques.

## About
Created and maintained by [Netztaucher](https://netztaucher.com).
