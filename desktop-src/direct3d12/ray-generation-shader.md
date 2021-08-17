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
ms.openlocfilehash: fdc177040cac7324545172319c318d07cded6dba42cfeed4756a7afaa88439aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123710"
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

 

 




