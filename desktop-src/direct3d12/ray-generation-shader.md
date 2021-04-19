---
description: 呼叫 TraceRay 以產生光線的著色器。
ms.assetid: ''
title: 光線產生著色器
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 75d67293e489eee0f1d100002965c017de7c682c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991653"
---
# <a name="ray-generation-shader"></a><span data-ttu-id="178dc-103">光線產生著色器</span><span class="sxs-lookup"><span data-stu-id="178dc-103">Ray Generation Shader</span></span>

<span data-ttu-id="178dc-104">呼叫 [**TraceRay**](traceray-function.md) 以產生光線的著色器。</span><span class="sxs-lookup"><span data-stu-id="178dc-104">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span> <span data-ttu-id="178dc-105">每個光線的初始使用者定義光線承載都會提供給 **TraceRay** 呼叫位置。</span><span class="sxs-lookup"><span data-stu-id="178dc-105">The initial user-defined ray payload for each ray is provided to the **TraceRay** call site.</span></span>  <span data-ttu-id="178dc-106">[**CallShader**](callshader-function.md) 也可以在光線產生著色器中用來叫用可呼叫的 [著色](callable-shader.md)器。</span><span class="sxs-lookup"><span data-stu-id="178dc-106">[**CallShader**](callshader-function.md) may also be used in ray generation shaders to invoke [callable shaders](callable-shader.md).</span></span>

<span data-ttu-id="178dc-107">**DispatchRays** 會叫用光線產生著色器調用的方格。</span><span class="sxs-lookup"><span data-stu-id="178dc-107">**DispatchRays** invokes a grid of ray generation shader invocations.</span></span>  <span data-ttu-id="178dc-108">光線產生著色器的每個叫用 (執行緒) 都知道其在整體方格中的位置，可以透過 [**TraceRay**](traceray-function.md)產生任意的光線，並且與其他調用分開運作。</span><span class="sxs-lookup"><span data-stu-id="178dc-108">Each invocation (thread) of a ray generation shader knows its location in the overall grid, can generate arbitrary rays via [**TraceRay**](traceray-function.md), and operates independently of other invocations.</span></span> <span data-ttu-id="178dc-109">每個執行緒都沒有任何定義的執行順序。</span><span class="sxs-lookup"><span data-stu-id="178dc-109">There is no defined order of execution of threads with respect to each other.</span></span>

## <a name="shader-type-attribute"></a><span data-ttu-id="178dc-110">著色器類型屬性</span><span class="sxs-lookup"><span data-stu-id="178dc-110">Shader Type attribute</span></span>


```
[shader("raygeneration")]
```



## <a name="example"></a><span data-ttu-id="178dc-111">範例</span><span class="sxs-lookup"><span data-stu-id="178dc-111">Example</span></span>

```
struct SceneConstantStructure { ... };
ConstantBuffer<SceneConstantStructure> SceneConstants;
RaytracingAccelerationStructure MyAccelerationStructure : register(t3);
struct MyPayload { ... };

[shader("raygeneration")]
void raygen_main()
{
    RayDesc myRay = {
        SceneConstants.CameraOrigin,
        SceneConstants.TMin,
        computeRayDirection(SceneConstants.LensParams, DispatchRaysIndex(), 
                            DispatchRaysDimensions()),
        SceneConstants.TMax};
    MyPayload payload = { ... };    // init payload
    TraceRay(
        MyAccelerationStructure,
        SceneConstants.RayFlags,
        SceneConstants.InstanceInclusionMask,
        SceneConstants.RayContributionToHitGroupIndex,
        SceneConstants.MultiplierForGeometryContributionToHitGroupIndex,
        SceneConstants.MissShaderIndex,
        myRay,
        payload);
    WriteFinalPixel(DispatchRaysIndex(), payload);
}
```

 

 




