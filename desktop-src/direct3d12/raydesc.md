---
description: 傳遞至 TraceRay 函式來定義光線的原點、方向和範圍。
ms.assetid: ''
title: RayDesc 結構
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
ms.openlocfilehash: a4fa44e68e8747a0a8366ca2d949290f585d4b70d9e75b4ed2d3b6fdda0d05c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123683"
---
# <a name="raydesc-structure"></a>RayDesc 結構

傳遞至 [**TraceRay**](traceray-function.md) 函式來定義光線的原點、方向和範圍。

## <a name="syntax"></a>Syntax


```
struct RayDesc
{
    float3 Origin;
    float  TMin;
    float3 Direction;
    float  TMax;
};

```



## <a name="fields"></a>欄位

<dl> <dt>

<span id="Origin"></span><span id="origin"></span>**起源**
</dt> <dd>

光線的原點。

</dd> <dt>

<span id="TMin"></span><span id="tmin"></span>**TMin**
</dt> <dd>

光線的最小範圍。


</dd> <dt>

<span id="Direction"></span><span id="direction"></span>**方向**
</dt> <dd>

光線的方向。


</dd> <dt>

<span id="TMax"></span><span id="tmax"></span>**TMax**
</dt> <dd>

光線的最大範圍。


</dd>

## <a name="requirements"></a>規格需求



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




