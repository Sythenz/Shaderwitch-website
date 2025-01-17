+++
title = 'Creating a Shading Model'
date = 2024-03-21T15:37:22+01:00
draft = true
weight = 0
+++

{{% notice style="info primary" title="Work in Progress" icon="cat" %}}
This page is a **current topic of research**, some things may not be accurate.
{{% /notice %}}

{{% badge style="primary" icon="user" title="Author" %}}Alessa "Codekitten" Baker{{% /badge %}}
{{% badge style="primary" icon="info-circle" title="Page Status" %}}WIP{{% /badge %}}
{{% badge style="primary" icon="star" title="Unreal Version" %}}5.2{{% /badge %}}

## Getting Started

Implementing a custom shading model in Unreal Engine can be one of the most enjoyable and rewarding experiences, because
it opens up so much more opportunity to experiment in custom rendering with minimal code changes. A lot of it comes down
to just replicating an existing implementation of another shading model.

Here are the files we'll modify today.

| Files Modified            | Description                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| EngineTypes.h             | Standard definitions for different types across Unreal Engine.                                                                    |
| MaterialShared.cpp        | Test3                                                                                                                             |
| Material.cpp              | Base class for a material, defines all that needs to be handled. Base class for a material, defines all that needs to be handled. |
| MaterialGraph.cpp         | Test3                                                                                                                             |
| SceneRenderTargets.cpp    | Test3                                                                                                                             |
| HLSLMaterialTranslator.h  | Test3                                                                                                                             |
| ShadingCommon.ush         | Test3                                                                                                                             |
| BasePassCommon.ush        | Test3                                                                                                                             |
| ShadingModelsMaterial.ush | Test3                                                                                                                             |
| BasePassPixelShader.ush   | Test3                                                                                                                             |

### Prerequisites

At the time of this document being written, go ahead and git clone and then compile **5.2 branch** of Unreal Engine. 
When you have a successful compile, we can get started by modifying our first file. If you are using an engine version
ahead of this branch, I cannot guarantee you won't have a little headache if any of these things change.

## Adding our Shading Model

> TODO: Adding to EngineTypes.h, and other files to inform Unreal that a new shading model exists.

### Modifying the Material Editor

### Enabling/Disabling Pins

> TODO: MP_ and switch cases to add and modify pins

## Custom Data

> TODO: Describe Custom Data, and how it applies to our HLSL and is passed from the material editor as a compiled parameter.

## Playing with some HLSL

> TODO: Add our custom data output to Diffuse Color in Base Pass. As a quick example of passing the parameter around.


---

### Additional Resources
> [1] [Shading Models Official Documentation](https://docs.unrealengine.com/4.27/en-US/RenderingAndGraphics/Materials/MaterialProperties/LightingModels/) docs.unrealengine.com  
> [2] [New shading models and changing the GBuffer by One3y3](https://dev.epicgames.com/community/learning/tutorials/2R5x/unreal-engine-new-shading-models-and-changing-the-gbuffer) dev.epicgames.com.  
> [3] [Unreal Engine 4 Rendering Part 6: Adding a new Shading Model](https://medium.com/@lordned/ue4-rendering-part-6-adding-a-new-shading-model-e2972b40d72d) medium.com/@lordned    
> [4] [Implement Cel-Shading w/ Outline Using Custom Shading Model in UE4.22 (1)](https://medium.com/@solaslin/learning-unreal-engine-4-implement-cel-shading-w-outline-using-custom-shading-model-in-ue4-22-1-775bccdb9ffb) medium.com/@solaslin  
> [5] [[UE4] Custom Shading Model](https://zhuanlan.zhihu.com/p/212785666) zhuanlan.zhihu.com    
> [6] [Porting custom UE4 shading models to UE5 (or how to tackle the new GBuffer codegen)](https://markjg.com/blog/porting-custom-shading-models-to-ue5/) markjg.com