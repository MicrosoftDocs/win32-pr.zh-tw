---
title: 高斯模糊效果
description: 使用高斯模糊效果，根據整個輸入影像上的高斯函數來建立模糊。
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- 高斯模糊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b759ed0f5f70c4fc11ad902c7a45db3b3059847ce6895d25c3dbb9c9eee8330
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967080"
---
# <a name="gaussian-blur-effect"></a>高斯模糊效果

使用高斯模糊效果，根據整個輸入影像上的高斯函數來建立模糊。

您可以使用此效果來建立發光和陰影，並使用 [複合](composite.md) 效果將結果套用至原始影像。 它在相片處理時很有用，例如反白顯示和陰影等篩選。 您可以使用此效果的輸出來輸入光源效果，例如 [反射光源](specular-lighting.md) 或 [擴散光源](diffuse-lighting.md) 效果，因為 Alpha 色板的亮度很模糊，而光源則使用 Alpha 色板來判斷 surface 幾何是否為高度地圖。

內建 [陰影](drop-shadow.md) 效果會使用此效果。

這項效果的 CLSID 是 CLSID \_ D2D1GaussianBlur。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [優化模式](#optimization-modes)
-   [框線模式](#border-modes)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像



| 之前                                                       |
|--------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)   |
| After                                                        |
| ![轉換後的影像。](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                                    | 描述                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> D2D1 \_ GAUSSIANBLUR \_ 的 \_ 標準 \_ 偏差<br/> | 要套用到影像的模糊量。 您可以藉由將標準差乘以3來計算核心的模糊半徑。 標準差和模糊半徑的單位為 Dip。 如果值為零，則會完全停用此效果。 此類型為 FLOAT。<br/> 預設值為 3.0 f。<br/> |
| Optimization<br/> D2D1 \_ GAUSSIANBLUR \_ 的 \_ 優化<br/>             | 優化模式。 如需詳細資訊，請參閱 [優化模式](#optimization-modes) 。 此類型為 D2D1 \_ GAUSSIANBLUR \_ 優化。<br/> 預設值為 D2D1 \_ GAUSSIANBLUR \_ 優化 \_ 平衡。<br/>                                                                                                            |
| BorderMode<br/> D2D1 \_ GAUSSIANBLUR \_ 的 \_ 樣式框線 \_ 模式<br/>               | 用來計算影像（軟或硬）框線的模式。 如需詳細資訊，請參閱 [框線模式](#border-modes) 。 <br/> 此類型為 D2D1 \_ GAUSSIANBLUR \_ BORDER \_ 模式。<br/> 預設值為 [D2D1 \_ 框線 \_ 模式] \_ 。<br/>                                                                                   |



 

## <a name="optimization-modes"></a>優化模式



| 名稱                                          | 描述                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 速度    | 套用內部優化，例如在相對較小半徑上進行預先調整。 使用線性篩選。                                  |
| D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 平衡 | 使用與速度模式相同的優化臨界值，但使用三線性篩選。                                                    |
| D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 品質  | 只會使用具有大型模糊半徑的內部優化，其中近似值較不可能可見。 使用三線性篩選。 |



 

## <a name="border-modes"></a>框線模式



| 名稱                     | 描述                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 框線 \_ 模式 \_ 軟 | 效果會對影像進行透明黑色圖元，因為它會套用模糊核心，以產生軟邊緣。 <br/>                                                                                             |
| D2D1 \_ 框線 \_ 模式 \_ 硬性 | 效果會將輸出個至輸入影像的大小。 當效果套用模糊核心時，它會針對輸入界限外的樣本，以鏡像類型的框線轉換來擴充輸入影像。<br/> |



 

## <a name="output-bitmap"></a>輸出點陣圖

此效果的輸出可能會比輸入點陣圖（以模糊半徑和框線模式為基礎）大。 如果框線模式設定為 D2D1 \_ 框線模式， \_ 則 \_ 輸出點陣圖的 s 大小會隨著模糊核心的大小增加（以圖元表示）。 下表提供您可以用來計算輸出點陣圖的方程式。

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

因此，如果影像大小在每個方向增加10個圖元，則影像的左上角將會位於 (-5、-5) ，而右下角會是 (105，105) 。

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

 

