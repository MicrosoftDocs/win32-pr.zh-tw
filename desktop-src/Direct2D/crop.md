---
title: 裁剪效果
description: 使用裁剪效果來輸出影像的指定區域。
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- 裁剪效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843532"
---
# <a name="crop-effect"></a>裁剪效果

使用裁剪效果來輸出影像的指定區域。

這項效果的 CLSID 是 CLSID \_ D2D1Crop。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像



| 之前                                                     |
|------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg) |
| After                                                      |
| ![轉換後的影像。](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>顯示名稱和索引列舉</th>
<th>類型和預設值</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rect<br/></td>
<td>D2D1_VECTOR_4F<br/></td>
<td>要裁剪的區域 (左、上、寬度、高度) 的形式指定為向量。<br/></td>
</tr>
<tr class="even">
<td>D2D1_CROP_PROP_RECT<br/></td>
<td>{-FLT_MAX、-FLT_MAX、FLT_MAX、FLT_MAX}<br/></td>
<td>單位為 Dip。 <br/>
<blockquote>
<p>[!Note]</p>
<p>如果矩形與輸入影像的邊緣界限重迭，則會截斷。<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D2D1_CROP_PROP_BORDER_MODE<br/></td>
<td>D2D1_BORDER_MODE <br/> D2D1_BORDER_MODE_SOFT <br/></td>
<td><ul>
<li>D2D1_BORDER_MODE_SOFT：如果裁剪矩形落在小數圖元座標上，效果會套用消除鋸齒以產生軟邊緣。</li>
<li>D2D1_BORDER_MODE_HARD：如果裁剪矩形落在小數圖元座標上，效果會個，進而導致硬性邊緣。</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a>輸出點陣圖

這項效果的輸出是 Rect 屬性的大小。 長度和寬度為 calc

ulated 使用以下的方公式： <dl> 輸出長度（以圖元為單位） = (Rect。左) \* (使用者的 DPI/96)   
輸出高度（以圖元為單位） = (Rect.Bottom-Rect.Top) \* (使用者的 DPI/96)   
</dl>

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

 

