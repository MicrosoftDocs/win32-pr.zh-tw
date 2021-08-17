---
description: 取得以 [**DispatchRaysDimensions**](dispatchraysdimensions.md) 系統值內建的寬度、高度和深度所取得的目前位置。
title: DispatchRaysIndex
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: 1b40987c76f42d41d74b7cb3d41f35cc20bd5a6ac1414ae9b010cedcfa7ef9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124162"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex

取得以 [**DispatchRaysDimensions**](dispatchraysdimensions.md) 系統值內建的寬度、高度和深度所取得的目前位置。

## <a name="syntax"></a>語法

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>備註

您可以從下列 raytracing 著色器類型呼叫這個函數。

* [**任何命中著色器**](any-hit-shader.md)
* [**可呼叫著色器**](callable-shader.md)
* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**交集著色器**](intersection-shader.md)
* [**遺漏著色器**](miss-shader.md)
* [**光線產生著色器**](ray-generation-shader.md)

## <a name="see-also"></a>另請參閱

* [Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
