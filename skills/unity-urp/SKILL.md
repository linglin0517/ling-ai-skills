---
name: unity-urp
description: Professional workflow for Unity Universal Render Pipeline shader, material, rendering, debugging, and optimization tasks.
---

# Unity URP

## Purpose

Use this skill for Unity URP work involving ShaderLab, HLSL, materials, renderer features, RenderTextures, lighting, and rendering optimization.

## Required Context

Determine when relevant:
- Unity version
- URP version
- target platform
- color space
- renderer type
- shader type
- performance constraints

Do not ask for information already available in the conversation or project context.

## Workflow

1. Identify the visual or technical goal.
2. Determine the responsible render stage.
3. Identify required data and coordinate spaces.
4. Design the smallest correct rendering solution.
5. Implement the solution.
6. Diagnose compile/runtime issues.
7. Validate visual parity.
8. Evaluate GPU and memory cost.
9. Suggest production optimization.

## Shader Rules

- Prefer HLSL.
- Use URP shader libraries rather than legacy Built-in Render Pipeline includes.
- Do not use `UnityCG.cginc` unless explicitly targeting the Built-in Render Pipeline.
- Avoid deprecated Built-in helper functions when a URP equivalent exists.
- Distinguish Unity 2022.3 and Unity 6 APIs.
- Maintain SRP Batcher compatibility where practical.
- Clearly state when a Renderer Feature, custom pass, or additional camera is required.

## Output Requirements

For implementation requests:
- explain architecture
- provide exact editor steps when useful
- provide complete code when requested
- identify version-specific APIs
- explain debugging strategy
- mention performance considerations

## Validation

Before finalizing:
- verify object/world/view/tangent coordinate spaces
- verify URP include paths and helper functions
- verify render queue and transparency behavior
- verify depth and stencil assumptions
- verify required passes
- verify texture import assumptions
- check mobile implications when relevant
