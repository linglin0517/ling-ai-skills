---
name: image-reference-analysis
description: Structured multimodal analysis of concept art, screenshots, material results, reference games, and before/after visual comparisons for production use.
---

# Image Reference Analysis

## Purpose

Use this skill when one or more images are provided as visual evidence for a technical-art, look-development, material, lighting, VFX, modeling, or rendering task.

## Analysis Framework

Analyze in this order when relevant:

1. Composition and focal hierarchy
2. Silhouette and shape language
3. Value structure
4. Hue and saturation relationships
5. Lighting direction and contrast
6. Material separation and response
7. Texture scale and frequency
8. Edge treatment and outline behavior
9. VFX layering and glow structure
10. Temporal implication if comparing frames or video stills

## Comparison Mode

When comparing target vs current result:
- identify the largest perceptual mismatch first
- separate global issues from local issues
- distinguish texture problems from shader problems
- distinguish lighting problems from material problems
- distinguish static breakup from motion breakup
- state which fixes can be made with parameters and which require asset changes

## Production Translation

Translate visual observations into actionable changes to:
- shader logic
- material parameters
- texture authoring
- masks
- mesh or normals
- lighting
- VFX
- post-processing

## Evidence Discipline

Do not infer hidden implementation details from appearance alone without marking them as hypotheses.

When multiple implementations could create the same visual result:
- list the plausible methods
- rank them by likelihood
- explain how to distinguish them in-engine

## Output Requirements

Prefer concrete statements such as:
- "the highlight band has insufficient spatial breakup"
- "the flow field is dominated by one global direction"
- "the rim term is too uniformly distributed around the silhouette"

Avoid generic statements such as:
- "needs more detail"
- "make it more magical"
- "make it more dynamic"

unless immediately followed by a measurable or implementable interpretation.
