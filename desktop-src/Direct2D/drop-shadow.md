---
title: 陰影效果
description: 使用陰影效果，從影像的 Alpha 通道產生陰影。
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- 陰影效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d88924140caac22b688a0ccb6948ee74312411c770bff99360847ef2cd1b4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833044"
---
# <a name="shadow-effect"></a>陰影效果

使用陰影效果，從影像的 Alpha 通道產生陰影。 針對較高的 Alpha 值，陰影較不透明，較低的 Alpha 值則更透明。 您可以設定模糊的數量和陰影的色彩。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [優化模式](#optimization-modes)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

這項效果的 CLSID 是 CLSID \_ D2D1Shadow。

## <a name="example-image"></a>範例影像

此處的範例會顯示陰影效果的輸出，其在原始位置中是由其組成的來源影像。 陰影效果只會輸出陰影。



| 之前                                                  |
|---------------------------------------------------------|
| ![效果之前的影像。](images/8-crop.png)      |
| After                                                   |
| ![轉換後的影像。](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                                        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BlurStandardDeviation<br/> D2D1 \_ 陰影 \_ 樣式 \_ 模糊 \_ 標準 \_ 偏差<br/> | 要套用至影像之 Alpha 通道的模糊數量。 您可以藉由將標準差乘以3來計算核心的模糊半徑。 標準差和模糊半徑的單位為 Dip。<br/> 這個屬性與 [高斯模糊](gaussian-blur.md) 的標準差屬性相同。 <br/> 此類型為 FLOAT。<br/> 預設值為 3.0 f。<br/> |
| Color<br/> D2D1 \_ 陰影 \_ 樣式 \_ 色彩<br/>                                     | 延伸陰影的色彩。 這個屬性是 D2D1 \_ 向量 \_ 4F，定義為： (R、G、B、) 。 您必須以純 Alpha 指定此色彩。<br/> 此類型為 D2D1 \_ VECTOR \_ 4F。<br/> 預設值為 {0.0 f、0.0 f、0.0 f、1.0 f}。<br/>                                                                                                                                                                     |
| Optimization<br/> D2D1 \_ 陰影 \_ 樣式 \_ 優化<br/>                       | 效能優化的層級。<br/> 此類型為 D2D1 \_ 陰影 \_ 優化。<br/> 預設值為 D2D1 \_ 陰影 \_ 優化 \_ 平衡。<br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a>優化模式



| 名稱                                          | 描述                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 速度    | 套用內部優化，例如在相對較小半徑上進行預先調整。 使用線性篩選。                                  |
| D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 平衡 | 使用與速度模式相同的優化臨界值，但使用三線性篩選。                                                    |
| D2D1 \_ DIRECTIONALBLUR \_ 優化 \_ 品質  | 只會使用具有大型模糊半徑的內部優化，其中近似值較不可能可見。 使用三線性篩選。 |



 

## <a name="output-bitmap"></a>輸出點陣圖

輸出點陣圖的大小是模糊輸出的大小。 相對於原始點陣圖的輸出點陣圖成長量，可以使用下列方程式來計算：

輸出點陣圖成長 (X 和 Y) = BlurStandardDeviation (與裝置無關的圖元 (Dip) ) \* 6 \* (使用者 DPI) /96

輸出會在所有方向平均增加，因此，如果大小在每個方向增加10個圖元，點陣圖的左上角就會位於 (-5，-5) ，而右下角會是 (105，105) ，如下圖所示。

![陰影效果輸出大小成長圖表。](images/drop-shadow-output-growth.png)

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

 

