---
name: lookdev-analysis
description: Look-development analysis workflow for translating visual targets into shader, texture, lighting, material, VFX, and post-process changes.
---

# LookDev Analysis

## Purpose

Use this skill when comparing a target/reference against the current render and turning visual differences into production actions.

## Analysis Order

1. Identify the focal subject and intended visual hierarchy.
2. Compare large-scale value structure before color details.
3. Compare hue and saturation relationships.
4. Compare material response: diffuse, specular, roughness, metallic, emissive, translucency.
5. Compare lighting direction, softness, contrast, fill, rim, and local accents.
6. Compare texture frequency and breakup.
7. Compare edge treatment, outline, rim, Fresnel, and silhouette readability.
8. Compare motion rhythm and temporal variation for animated effects.
9. Compare VFX layering and focal emphasis.
10. Translate findings into shader/material/texture/lighting/VFX changes.

## Diagnosis Categories

Classify visual issues into one or more of:
- value hierarchy
- color palette
- material model
- spatial breakup
- temporal breakup
- lighting
- silhouette
- texture authoring
- VFX composition
- post-processing

## Output Requirements

Rank recommendations by visual impact and implementation cost.

For each recommendation explain:
- what looks wrong
- what visual principle is missing
- which production asset/system should change
- suggested parameter or implementation direction
- how to verify improvement

Avoid vague advice such as "make it more dynamic" without identifying the concrete spatial or temporal mechanism responsible.
