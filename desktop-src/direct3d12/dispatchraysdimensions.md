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
ms.openlocfilehash: 4f68b7bdd5f5ea92074b366b9f981f490a9801079b29def17ba66770abd3c5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989488"
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
