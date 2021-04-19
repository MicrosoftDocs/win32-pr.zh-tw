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
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2020
ms.locfileid: "106969946"
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
