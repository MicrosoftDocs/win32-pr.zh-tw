---
title: 方向模糊效果
description: 方向模糊效果與高斯模糊類似，不同之處在于您可以在特定方向扭曲模糊。
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- 方向模糊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685496"
---
# <a name="directional-blur-effect"></a>方向模糊效果

方向模糊效果與 [高斯模糊](gaussian-blur.md)類似，不同之處在于您可以在特定方向扭曲模糊。 您可以使用此效果，讓影像看起來像是移動中或強調動畫影像。

這項效果的 CLSID 是 CLSID \_ D2D1DirectionalBlur。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [優化模式](#optimization-modes)
-   [框線模式](#border-modes)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像



| 之前                                                          |
|-----------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)      |
| After                                                           |
| ![轉換後的影像。](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation<br/> D2D1 \_ DIRECTIONALBLUR \_ 的 \_ 標準 \_ 偏差<br/> | 要套用到影像的模糊量。 您可以藉由將標準差乘以3來計算核心的模糊半徑。 標準差和模糊半徑的單位為 Dip。 值為 0 Dip 會停用此效果。 此類型為 FLOAT。<br/> 預設值為 3.0 f。<br/>                                                                            |
| 角度<br/> D2D1 \_ DIRECTIONALBLUR \_ 的 \_ 角度<br/>                           | 相對於 X 軸之模糊的角度（以逆時針方向）。 單位是以度為單位來指定。<br/> 模糊核心會先使用與 [高斯模糊](gaussian-blur.md) 效果相同的進程產生。 核心值接著會根據模糊角度進行轉換。<br/> 此類型為 FLOAT。<br/> 預設值為 0.0 f。<br/> |
| Optimization<br/> D2D1 \_ DIRECTIONALBLUR \_ 的 \_ 優化<br/>             | 優化模式。 如需詳細資訊，請參閱 [優化模式](#optimization-modes) 。<br/> 此類型為 D2D1 \_ DIRECTIONALBLUR \_ 優化。<br/> 預設值為 D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 平衡。 <br/>                                                                                                                                                         |
| BorderMode<br/> D2D1 \_ DIRECTIONALBLUR \_ 的 \_ 樣式框線 \_ 模式<br/>               | 用來計算影像（軟或硬）框線的模式。 如需詳細資訊，請參閱 [框線模式](#border-modes) 。<br/> 此類型為 D2D1 \_ 框線 \_ 模式。<br/> 預設值為 [D2D1 \_ 框線 \_ 模式] \_ 。<br/>                                                                                                                                                                 |



 

## <a name="optimization-modes"></a>優化模式



| Name                                          | 描述                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 速度    | 套用內部優化，例如在相對較小半徑上進行預先調整。 使用線性篩選。                                  |
| D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 平衡 | 使用與速度模式相同的優化臨界值，但使用三線性篩選。                                                    |
| D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 品質  | 只會使用具有大型模糊半徑的內部優化，其中近似值較不可能可見。 使用三線性篩選。 |



 

## <a name="border-modes"></a>框線模式



| Name                     | 描述                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 框線 \_ 模式 \_ 軟 | 效果會對影像進行透明黑色圖元，因為它會套用模糊核心，以產生軟邊緣。 <br/>                                                                                             |
| D2D1 \_ 框線 \_ 模式 \_ 硬性 | 效果會將輸出個至輸入影像的大小。 當效果套用模糊核心時，它會針對輸入界限外的樣本，以鏡像類型的框線轉換來擴充輸入影像。<br/> |



 

## <a name="output-bitmap"></a>輸出點陣圖

輸出點陣圖的大小會根據標準差、效果的角度和框線模式而增加。 如果框線模式設定為 D2D1 \_ 框線 \_ 模式，則 \_ 輸出點陣圖的大小會隨著模糊核心的大小增加（以圖元表示）。 您可以使用這些方程式來計算輸出點陣圖的大小。



| 需求 | 值 |
|------------------------|-------------------------------------------------------------------|
| 輸出點陣圖成長 X | List.standarddeviation (Dip) \* 6 \* ( (使用者 DPI) /96) \* cos (角度) )  |
| 輸出點陣圖成長 Y | List.standarddeviation (Dip) \* 6 \* ( (使用者 DPI) /96) \* Angle (角度) )  |



 

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

 

