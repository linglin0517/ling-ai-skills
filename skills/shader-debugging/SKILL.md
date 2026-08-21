---
name: shader-debugging
description: Systematic shader debugging workflow for compile errors, visual artifacts, coordinate-space mistakes, render-state issues, and performance problems.
---

# Shader Debugging

## Purpose

Use this skill when diagnosing shader compile failures, incorrect rendering, unexpected lighting, broken UVs, depth/stencil issues, transparency problems, or GPU cost.

## Debug Order

1. Reproduce the smallest failing case.
2. Read the exact compiler/runtime error before changing code.
3. Verify render pipeline and engine version.
4. Verify include files, macros, and API availability.
5. Verify vertex-to-fragment data flow.
6. Verify coordinate spaces and normalization.
7. Verify texture import and sampler assumptions.
8. Verify render states: queue, blend, ZWrite, ZTest, Cull, stencil.
9. Replace complex outputs with debug colors to isolate data.
10. Reintroduce features incrementally.
11. Profile only after correctness is established.

## Coordinate-Space Checks

Always identify whether vectors are in:
- object space
- world space
- view space
- tangent space
- clip space
- screen/UV space

Do not mix spaces without an explicit transform.

## Visual Debugging

When useful, temporarily visualize:
- normals as RGB
- UVs
- masks
- depth
- Fresnel terms
- lighting terms
- flow vectors
- intermediate scalar values

## Compile Error Discipline

For unresolved identifiers:
- verify whether the helper belongs to Built-in, URP, HDRP, Unreal, or a custom library
- prefer the pipeline-native equivalent
- do not fix by adding legacy includes unless the target pipeline actually requires them

## Output Requirements

For each suspected bug, provide:
- likely cause
- how to verify it
- minimal fix
- why the fix works
- side effects or compatibility concerns

When multiple causes are possible, rank them by likelihood and test cost.
