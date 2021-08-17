---
title: ConsumeStructuredBuffer
description: 顯示為數據流的輸入緩衝區，表示著色器可能從中提取值。 只有結構化緩衝區可以採用結構的 T 類型。
ms.assetid: 373bdd97-6186-4bce-99bf-738a153234f6
keywords:
- ConsumeStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- ConsumeStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4e0530c98b78f9b18b0934874fb5a082779694ced2f171293d0a38dc458a08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986088"
---
# <a name="consumestructuredbuffer"></a>ConsumeStructuredBuffer

顯示為數據流的輸入緩衝區，表示著色器可能從中提取值。 只有結構化緩衝區可以採用結構的 T 類型。



| 方法                                                                    | 描述                                 |
|---------------------------------------------------------------------------|---------------------------------------------|
| [**取用**](sm5-object-consumestructuredbuffer-consume.md)             | 從緩衝區的結尾移除值。 |
| [**GetDimensions**](sm5-object-consumestructuredbuffer-getdimensions.md) | 取得資源維度。               |



 

系結到此資源的 UAV 格式必須以 DXGI \_ 格式 \_ 未知格式建立。

系結至此資源的 UAV 必須使用 [**D3D11 \_ BUFFER \_ UAV \_ 旗標 \_ 附加**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag)來建立。

如需使用結構化緩衝區的詳細資訊，請參閱這兩個區段： [附加和使用緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) 和 [結構化緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                                | 支援 |
|-----------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是       |



 

下列著色器類型支援此物件：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 