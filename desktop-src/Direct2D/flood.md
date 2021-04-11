---
title: 大量效果
description: 使用洪水效果，根據指定的色彩和 Alpha 值產生點陣圖。 當您想要特定色彩作為效果的輸入（例如背景色彩）時，可以使用此效果。
ms.assetid: F80A6DC0-E18C-4324-BE4A-FE40C5722988
keywords:
- 大量效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92d34a41c0913a0d250fc24467b37b0d347b4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934759"
---
# <a name="flood-effect"></a>大量效果

使用洪水效果，根據指定的色彩和 Alpha 值產生點陣圖。 當您想要特定色彩作為效果的輸入（例如背景色彩）時，可以使用此效果。

> [!Note]  
> 效果會依照指定的色彩值沿著指定的色彩值傳遞。 如果您打算將輸出傳遞到預期已預先相乘輸入的效果，則必須手動將值相乘。

 

這項效果的 CLSID 是 CLSID \_ D2D1Flood。

洪水效果沒有輸入影像。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

![輸出綠色的洪水效果影像範例。](images/20-flood.png)


```C++
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(0.0f, 1.0f, 0.0f, 1.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(floodEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                   | Description                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color<br/> D2D1 \_ 洪水 \_ 的 \_ 色彩<br/> | 點陣圖的色彩和不透明度。 這個屬性是 D2D1 \_ 向量 \_ 4F。 每個通道的個別值都屬於 FLOAT、未系結和無數量的型別。 效果不會修改通道的值。<br/> 每個通道的 RGBA 值範圍從0到1。<br/> 此類型為 D2D1 \_ VECTOR \_ 4F。<br/> 預設值為 {0.0 f、0.0 f、0.0 f、1.0 f}。<br/> |



 

## <a name="output-bitmap"></a>輸出點陣圖

此效果會產生邏輯上無限大小的點陣圖。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 最低支援的伺服器 | 適用于 Windows 7 desktop app 的 Windows 8 和平臺更新 \[ \| windows Store 應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

