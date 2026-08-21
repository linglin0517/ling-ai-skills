---
name: unreal-engine
description: Professional Unreal Engine technical-art workflow for materials, rendering, Niagara, post process, Blueprints, debugging, and optimization.
---

# Unreal Engine

## Purpose

Use this skill for Unreal Engine technical-art tasks involving materials, Custom HLSL, Niagara, post process, lighting, Blueprints, rendering features, and performance.

## Required Context

Determine when relevant:
- Unreal Engine version
- rendering path
- target platform
- mobile/desktop/console constraints
- Deferred or Forward rendering
- Lumen/Nanite/Virtual Shadow Maps usage
- material domain and blend mode

## Workflow

1. Identify the artistic and technical target.
2. Determine whether the solution belongs in Material Editor, Custom HLSL, Niagara, Blueprint, post process, or rendering configuration.
3. Identify required data sources and coordinate spaces.
4. Build the simplest reproducible version first.
5. Validate material/rendering behavior.
6. Diagnose artifacts systematically.
7. Profile GPU/CPU cost when relevant.
8. Propose production-ready optimization.

## Material Rules

- Prefer native Material Editor nodes when they are clear and maintainable.
- Use Custom HLSL when it materially improves control, reuse, or complexity.
- Explain node equivalents when converting from another DCC or engine.
- Distinguish UE4 and UE5 behavior.
- Call out features unavailable or expensive on mobile.

## Output Requirements

When teaching a node graph:
- describe every major node
- state pin connections explicitly
- give parameter names and suggested starting values
- explain coordinate spaces and expected visual result

When using Custom HLSL:
- provide the code
- specify Custom node inputs/outputs
- explain where the code belongs
- mention shader model or platform constraints

## Validation

Before finalizing:
- verify material domain and blend mode
- verify tangent/world/view-space assumptions
- verify depth/custom depth/stencil behavior
- verify translucency limitations
- verify mobile compatibility when relevant
- verify Niagara bounds and overdraw implications for VFX
