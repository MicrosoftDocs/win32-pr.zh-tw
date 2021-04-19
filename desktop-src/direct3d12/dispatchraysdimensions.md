---
description: 原始 DispatchRays 呼叫中所指定之 D3D12_DISPATCH_RAYS_DESC 結構的寬度、高度和深度值。
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: e35c967ad831c82912d2962da72d9ad17eab1c15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972578"
---
# <a name="dispatchraysdimensions"></a>DispatchRaysDimensions

原始 [**DispatchRays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays)呼叫中所指定之 **D3D12 \_ 分派 \_ 放射放射 \_** 值結構的寬度、高度和深度值。

## <a name="syntax"></a>語法

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a>備註

您可以從下列 raytracing 著色器類型呼叫這個函數：

* [**任何命中著色器**](any-hit-shader.md)
* [**可呼叫著色器**](callable-shader.md)
* [**最接近的點擊著色器**](closest-hit-shader.md)
* [**交集著色器**](intersection-shader.md)
* [**遺漏著色器**](miss-shader.md)
* [**光線產生著色器**](ray-generation-shader.md)

## <a name="see-also"></a>另請參閱

* [Direct3D 12 Raytracing HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)
