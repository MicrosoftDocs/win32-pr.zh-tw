---
title: AppendStructuredBuffer
description: 輸出緩衝區，顯示為著色器可以附加的資料流程。 只有結構化緩衝區可以採用結構的 T 類型。
ms.assetid: 377b0358-0f9d-4021-9140-19c3d1bfed38
keywords:
- AppendStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- AppendStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c140052c861c8da3df6378fc3bc49816998c130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682579"
---
# <a name="appendstructuredbuffer"></a>AppendStructuredBuffer

輸出緩衝區，顯示為著色器可以附加的資料流程。 只有結構化緩衝區可以採用結構的 T 類型。



| 方法                                                                   | 描述                               |
|--------------------------------------------------------------------------|-------------------------------------------|
| [**附加**](sm5-object-appendstructuredbuffer-append.md)               | 將值附加至緩衝區的結尾。 |
| [**GetDimensions**](sm5-object-appendstructuredbuffer-getdimensions.md) | 取得資源維度。             |



 

系結到此資源的 UAV 格式必須以 DXGI \_ 格式 \_ 未知格式建立。

系結至此資源的 UAV 必須使用 [**D3D11 \_ BUFFER \_ UAV \_ 旗標 \_ 附加**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)來建立。

如需有關附加結構化緩衝區的詳細資訊，請參閱這兩個區段： [附加和使用緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) 和 [結構化緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此物件：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 