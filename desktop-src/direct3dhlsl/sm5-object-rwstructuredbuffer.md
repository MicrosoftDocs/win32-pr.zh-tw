---
title: RWStructuredBuffer
description: 可採用結構的 T 類型的讀取/寫入緩衝區。
ms.assetid: 8dd93b81-135d-4f28-898f-38510dc39af1
keywords:
- RWStructuredBuffer HLSL
topic_type:
- apiref
api_name:
- RWStructuredBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f921ca795e761522828de14ede61894defe44f6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375676"
---
# <a name="rwstructuredbuffer"></a>RWStructuredBuffer

可採用結構的 T 類型的讀取/寫入緩衝區。



| 方法                                                                     | 描述                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [**DecrementCounter**](sm5-object-rwstructuredbuffer-decrementcounter.md) | 遞減物件的隱藏計數器。 |
| [**GetDimensions**](sm5-object-rwstructuredbuffer-getdimensions.md)       | 取得資源維度。           |
| [**IncrementCounter**](sm5-object-rwstructuredbuffer-incrementcounter.md) | 遞增物件的隱藏計數器。 |
| [**載入**](rwstructuredbuffer-load.md)                                    | 讀取緩衝區資料。                      |
| [**運算子\[\]**](sm5-object-rwstructuredbuffer-operatorindex.md)        | 傳回資源變數。            |



 

資源變數也可以傳遞至任何未排序或連鎖的作業。

RWStructuredBuffer 物件的前面可以加上儲存類別 **globallycoherent**。 此儲存類別會造成記憶體阻礙和同步處理，以排清整個 GPU 上的資料，讓其他群組可以看到寫入。 如果沒有這個規範，記憶體屏障或同步只會清除目前群組內的 UAV。

系結到此資源的 UAV 格式必須以 DXGI \_ 格式 \_ 未知格式建立。

若要瞭解 [結構化緩衝區](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources)的詳細資訊，請參閱總覽材質。

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此物件。



| 著色器模型                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | 支援 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md)及更高的著色器模型 [著色器模型 4](dx-graphics-hlsl-sm4.md) (可透過 Direct3D 11 API 取得，方法是在支援計算著色器的裝置上，使用10.0 或10.1 功能等級 ([**D3D \_ 功能 \_ 等級**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) 。 如需舊版硬體上計算著色器支援的詳細資訊，請參閱 [下層硬體上的計算](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders)著色器 ) 。<br/> | 是       |



 

下列著色器類型支援此物件：



| 頂點 | 船體 | 網域 | 幾何 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[著色器模型5物件](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

