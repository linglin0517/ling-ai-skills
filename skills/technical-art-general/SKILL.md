---
name: technical-art-general
description: General professional technical-art workflow for real-time rendering, shaders, materials, look development, DCC tools, debugging, and optimization.
---

# Technical Art General

## Purpose

Use this skill for technical-art tasks involving real-time rendering, shaders, materials, look development, DCC workflows, rendering debugging, and performance optimization.

## Core Approach

1. Identify the visual or technical target.
2. Separate artistic intent from implementation constraints.
3. Determine the rendering stage and data involved.
4. Identify coordinate spaces, texture channels, masks, lighting inputs, and temporal behavior.
5. Design the simplest correct implementation.
6. Validate visually.
7. Diagnose technical errors.
8. Profile performance when relevant.
9. Recommend production-ready improvements.

## Response Requirements

When appropriate:
- explain both artistic reasoning and technical implementation
- distinguish engine/version-specific behavior
- give exact editor operations
- provide complete code when requested
- explain why each major step is necessary
- call out performance and maintainability risks
- avoid deprecated APIs unless explicitly required

## Visual Analysis

For screenshots, concept art, render comparisons, or videos:
- analyze value structure
- hue and saturation
- material response
- lighting hierarchy
- edge treatment
- frequency distribution
- motion rhythm
- VFX hierarchy
- silhouette
- focal emphasis

Translate visual findings into actionable changes to:
- shader
- material
- texture
- lighting
- VFX
- mesh
- post-processing

## Engineering Discipline

Before finalizing implementation:
- verify coordinate spaces
- verify render-pipeline compatibility
- verify required passes
- verify transparency/depth behavior
- verify texture import assumptions
- verify mobile implications when relevant
