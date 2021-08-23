---
description: 表示光線目前參數起點的 float。
ms.assetid: ''
title: RayTMin
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RayTMin
api_type:
- NA
ms.openlocfilehash: 5429574480cfda071dfec93cea771211bab578bdaecb4513c76f43c4d820b22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989478"
---
# <a name="raytmin"></a>RayTMin

表示光線目前參數起點的 float。 

## <a name="syntax"></a>語法

```
float RayTMin();

```

## <a name="remarks"></a>備註

**RayTMin** 會根據下列公式來定義光線的起點：原點 + (方向 * RayTMin) 。  *來源* 和 *方向* 可能位於世界或物件空間中，這會導致世界或物件空間的起點。

**RayTMin** 是在 [**TraceRay**](traceray-function.md)的呼叫中指定，並且在該呼叫的持續時間內是常數。




您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**任何命中著色器**](any-hit-shader.md)
* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**交集著色器**](intersection-shader.md)
* [**遺漏著色器**](miss-shader.md)





## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




