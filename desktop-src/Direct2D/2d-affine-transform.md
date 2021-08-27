---
title: 2D 仿射轉換效果
description: 2D 仿射轉換效果會使用 Direct2D 矩陣轉換和六個插補模式的任一個，根據3X2 矩陣將空間轉換套用至影像。
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- 2D 仿射轉換效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 337168db7a422a8a22785316d2af1960e3a78b2f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478094"
---
# <a name="2d-affine-transform-effect"></a>2D 仿射轉換效果

2D 仿射轉換效果會使用 Direct2D 矩陣 [轉換](direct2d-transforms-overview.md) 和六個插補模式的任一個，根據3X2 矩陣將空間轉換套用至影像。 您可以使用此效果來旋轉、縮放、扭曲或轉譯影像。 或者，您可以結合這些作業。 仿射傳輸會保留平行線，以及影像中任何三個點之間的距離比例。

這項效果的 CLSID 是 CLSID \_ D2D12DAffineTransform。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [框線模式](#border-modes)
-   [插補模式](#interpolation-modes)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像



| 之前                                                             |
|--------------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg)         |
| After                                                              |
| ![轉換後的影像。](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



此效果會執行此矩陣作業：

![仿射矩陣運算](images/affine-matrix-calculation.png)

雖然輸入矩陣定義為3x2 矩陣，但最後一個資料行會以0、0和1填補，以產生正方形矩陣。 這可允許矩陣相乘，以便將轉換串連成單一矩陣。

## <a name="effect-properties"></a>效果屬性




| 顯示名稱和索引列舉 | Description | 
|------------------------------------|-------------|
| InterpolationMode<br /> D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE<br /> | 用來調整影像的插補模式。 有6個調整模式的品質和速度範圍。<br /> 類型為 D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE。<br /> 預設值為 D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR。<br /> | 
| BorderMode<br /> D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE<br /> | 用來計算影像（軟或硬）框線的模式。 如需詳細資訊，請參閱 <a href="https://www.bing.com/search?q=Border+modes">框線模式</a> 。 <br /> 類型為 D2D1_BORDER_MODE。<br /> 預設值為 D2D1_BORDER_MODE_SOFT。<br /> | 
| TransformMatrix<br /> D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX<br /> | 使用 Direct2D 矩陣 <a href="direct2d-transforms-overview.md">轉換</a>來轉換影像的3x2 矩陣。 <br /> 類型為 D2D1_MATRIX_3X2_F。<br /> 預設值為 Matrix3x2F：： Identity () 。<br /> | 
| 清晰度<br /> D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS<br /> | 在高品質的三重插補點模式中，調整篩選的清晰度層級是介於0和1之間的浮點數。 這些值沒有用。 您可以使用清晰度來調整影像縮放時的影像品質。<br /> 清晰度因素會影響核心的圖形。 最高的清晰度因數越小，核心就越小。 <br /><blockquote>[!Note]<br />這個屬性只會影響高品質的三次插補模式。</blockquote><br /> 類型為 FLOAT。<br /> 預設值為 1.0 f。<br /> | 




 

## <a name="border-modes"></a>框線模式



| Name                     | 描述                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 框線 \_ 模式 \_ 軟 | 效果會在插補時以透明黑色圖元來填補影像，進而產生軟邊緣。<br/> |
| D2D1 \_ 框線 \_ 模式 \_ 硬性 | 效果會將輸出個至輸入影像的大小。 <br/>                                         |



 

## <a name="interpolation-modes"></a>插補模式



| 列舉型別                                                         | 描述                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 2DAFFINETRANSFORM 插補模式     | 範例最接近的單一點，並使用該點。 這個模式會使用較少的處理時間，但會輸出最低品質的影像。                                                                           |
| D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 線性                | 使用四個點取樣和線性插補。 這個模式所使用的處理時間比最近的鄰近模式更多，但會輸出較高品質的影像。                                           |
| D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 立方                 | 使用16個範例三核心來進行插補。 這個模式會使用大部分的處理時間，但會輸出較高品質的影像。                                                                        |
| D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 多 \_ 樣本 \_ 線性 | 使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。 這種模式適合用來在具有少量圖元的影像上相應減少量。                                              |
| D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 各向異性           | 根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。                                                                                                     |
| D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 高 \_ 品質 \_ 三次  | 如果 downscaling 與轉換矩陣有關，則使用可變大小的高品質三核心來執行預先縮小的影像。 然後使用三次插補模式來進行最終輸出。 |



 

> [!Note]  
> 如果您未選取模式，效果會預設為 D2D1 \_ 2DAFFINETRANSFORM \_ 插補 \_ 模式 \_ 線性。

 

> [!Note]  
> 當調整時，非等向模式會產生 mipmap，不過，如果您在輸入至此效果的效果上將快取 **的屬性設** 為 true，則每次都不會針對足夠的小型影像產生 mipmap。

 

## <a name="output-bitmap"></a>輸出點陣圖

輸出點陣圖的大小取決於套用至影像的轉換矩陣。

效果會執行轉換作業，然後在結果周圍套用周框方塊。 輸出點陣圖是周框方塊的大小。

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

 

