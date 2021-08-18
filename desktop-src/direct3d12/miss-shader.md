---
description: 找不到或不接受光線交集時，所叫用的著色器。
ms.assetid: ''
title: 遺漏著色器
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
ms.openlocfilehash: 30f7ce32e66a19984ce43737d9fc9cae83652c851174d7db350ca34628a33033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850821"
---
# <a name="miss-shader"></a>遺漏著色器

找不到或不接受光線交集時，所叫用的著色器。 這適用于背景或天空陰影。  遺漏的著色器可能會使用 [**CallShader**](callshader-function.md) 和 **TraceRay** 來排程更多工作。

遺漏的著色器必須包含使用者定義的結構類型承載參數，其符合提供給 [**TraceRay**](traceray-function.md)的類型。


## <a name="shader-type-attribute"></a>著色器類型屬性


```
[shader("miss")]
```



## <a name="example"></a>範例

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 




