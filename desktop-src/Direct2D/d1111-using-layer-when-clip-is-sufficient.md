---
title: 當剪輯足夠時使用圖層 D1111
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: 正在搭配 Null 不透明度遮罩、1.0 不透明度和軸對齊矩形幾何遮罩來使用圖層。 推送/Pop 剪輯 API 應該以更高的效能達成相同的結果。
keywords:
- 當剪輯足夠 Direct2D 時使用圖層 D1111
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: a30bbfd7b8ca448928249018a28bc4d6a8a2f57f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683050"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a>D1111：當剪輯足夠時使用圖層

效能-正在搭配 **Null** 不透明度遮罩、1.0 不透明度和軸對齊矩形幾何遮罩使用層。 推送/Pop 剪輯 API 應該以更高的效能達成相同的結果。

## <a name="placeholders"></a>預留位置

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*介面*
</dt> <dd>

介面的位址。

</dd> </dl> 

|             |             |
|-------------|-------------|
| 錯誤層級 | 資訊 |



 

## <a name="examples"></a>範例

下列程式碼會在圖層僅包含一個基本 (矩形) ，而且 [**D2D1 \_ 圖層 \_ 參數**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)結構的欄位設定為預設值時使用 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))和 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 。 如需 **D2D1 \_ 圖層 \_ 參數** 結構的預設值，請參閱 [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters)。


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



此範例會產生下列 debug 訊息：

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a>可能的原因

[**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))和 [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip)方法有 sufficed 時，會使用一層。

 

 