---
title: 磚效果
description: 使用磚效果來重複指定的影像區域。
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- 磚效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0df10143a727fb8ce6585264b65b6db46d75c731070f2ea46ff8e7dffd59dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430490"
---
# <a name="tile-effect"></a>磚效果

使用磚效果來重複指定的影像區域。

這項效果的 CLSID 是 CLSID \_ D2D1Tile。

## <a name="example-image"></a>範例影像



| 之前                                                     |
|------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg) |
| After                                                      |
| ![轉換後的影像。](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                | 類型和預設值                                              | 描述                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Rect<br/> D2D1 \_ 圖格的圖示 \_ \_ RECT<br/> | D2D1 \_ 向量 \_ 4F<br/> {0.0 f、0.0 f、100.0 f、100.0 f}<br/> | 要並排顯示之影像的區域。 這個屬性是 D2D1 \_ 向量 \_ 4F，定義為： (左、上、右、下) 。 單位為 Dip。<br/> |



 

## <a name="output-bitmap"></a>輸出點陣圖

此效果會產生邏輯上無限大小的點陣圖。

您可以在呼叫 ID2D1DeviceCoNtext 時設定大小，以並排顯示影像並輸出特定大小，而不會產生任何其他效果 [**：:D rawimage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 7 傳統型應用程式的 Windows 8 和平臺更新 \[ \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects。h                                                                      |
| 程式庫                  | d2d1 .lib，dxguid .lib                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

