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
# <a name="ray-generation-shader"></a>光線產生著色器

呼叫 [**TraceRay**](traceray-function.md) 以產生光線的著色器。 每個光線的初始使用者定義光線承載都會提供給 **TraceRay** 呼叫位置。  [**CallShader**](callshader-function.md) 也可以在光線產生著色器中用來叫用可呼叫的 [著色](callable-shader.md)器。

**DispatchRays** 會叫用光線產生著色器調用的方格。  光線產生著色器的每個叫用 (執行緒) 都知道其在整體方格中的位置，可以透過 [**TraceRay**](traceray-function.md)產生任意的光線，並且與其他調用分開運作。 每個執行緒都沒有任何定義的執行順序。

## <a name="shader-type-attribute"></a>著色器類型屬性


```
[shader("raygeneration")]
```



## <a name="example"></a>範例

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

 

 




