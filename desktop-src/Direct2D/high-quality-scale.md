---
title: 調整效果
description: 使用此效果可將影像向上或向下調整。 效果具有最接近鄰近、線性、三次、多取樣線性、非線性和高品質的三種調整模式。
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- 調整效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db3a4ef93fcdd2e93580157e0bb73b172975fe4a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472927"
---
# <a name="scale-effect"></a>調整效果

使用此效果可將影像向上或向下調整。 效果具有六個調整模式：最接近的鄰近、線性、三、多取樣線性、非等向和高品質的三層。

這項效果的 CLSID 是 CLSID \_ D2D1Scale。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
    -   [框線模式](#border-modes)
-   [插補模式](#interpolation-modes)
-   [輸出點陣圖](#output-bitmap)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

此範例會顯示縮放效果，縮放比例為輸入和裁剪至原始大小的2倍。



| 之前                                                     |
|------------------------------------------------------------|
| ![效果之前的影像。](images/default-before.jpg) |
| After                                                      |
| ![轉換後的影像。](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性




| 顯示名稱和索引列舉 | 描述 | 
|------------------------------------|-------------|
| 調整<br /> D2D1_SCALE_PROP_SCALE<br /> | 以 X 和 Y 方向的比例量，作為輸出大小與輸入大小的比率。 這個屬性會 D2D1_VECTOR_2Fdefined 為： (X 刻度、Y 刻度) 。 尺規數量為 FLOAT、無量，且必須為正數或0。<br /> 此類型為 D2D1_VECTOR_2F。<br /> 預設值為 {1.0 f、1.0 f}。<br /> | 
| CenterPoint<br /> D2D1_SCALE_PROP_CENTER_POINT<br /> | 影像縮放中心點。 這個屬性是定義為： (點 X、點 Y) 的 D2D1_VECTOR_2F。 單位為 Dip。<br /> 使用中央點屬性來圍繞左上角的某個點進行縮放。<br /> 此類型為 D2D1_VECTOR_2F。<br /> 預設值為 {0.0 f，0.0 f}。<br /> | 
| BorderMode<br /> D2D1_SCALE_PROP_BORDER_MODE<br /> | 用來計算影像（軟或硬）框線的模式。 如需詳細資訊，請參閱 <a href="#border-modes">框線模式</a> 。 <br /> 此類型為 D2D1_BORDER_MODE。<br /> 預設值為 D2D1_BORDER_MODE_SOFT。<br /> | 
| 清晰度<br /> D2D1_SCALE_PROP_SHARPNESS<br /> | 在高品質的三重插補點模式中，調整篩選的清晰度層級是介於0和1之間的浮點數。 這些值沒有用。 您可以使用「清晰度」來調整影像向下調整時的影像品質。<br /> 清晰度因素會影響核心的圖形。 最高的清晰度因數越小，核心就越小。<br /><blockquote>[!Note]<br />這個屬性只會影響高品質的三次插補模式。</blockquote><br /> 此類型為 FLOAT。<br /> 預設值為 0.0 f。<br /> | 
| InterpolationMode<br /> D2D1_SCALE_PROP_INTERPOLATION_MODE<br /> | 效果用來調整影像的插補模式。 有6個調整模式的品質和速度範圍。 如需詳細資訊，請參閱 <a href="#interpolation-modes">插補模式</a> 。 <br /> 此類型為 D2D1_SCALE_INTERPOLATION_MODE。<br /> 預設值為 D2D1_SCALE_INTERPOLATION_MODE_LINEAR。<br /> | 




 

### <a name="border-modes"></a>框線模式



| Name                     | 描述                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 框線 \_ 模式 \_ 軟 | 此效果會在輸入影像套用卷積核心時，以透明的黑色圖元為單位，以透明的方式在輸入界限之外取得樣本。 這會建立影像的軟邊緣，並且在進程中依核心的大小展開輸出點陣圖。<br/> |
| D2D1 \_ 框線 \_ 模式 \_ 硬性 | 效果會使用鏡像類型的框線轉換來擴充輸入界限之外樣本的輸入影像。 輸出點陣圖的大小等於輸入點陣圖的大小。<br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a>插補模式



| 列舉型別                                             | 描述                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 縮放 \_ 插補 \_ 模式 \_ 最接近 \_ 鄰近     | 範例最接近的單一點，並使用該點。 這個模式會使用較少的處理時間，但會輸出最低品質的影像。                                                                           |
| D2D1 \_ SCALE \_ 插補 \_ 模式 \_ 線性                | 使用四個點取樣和線性插補。 這個模式所使用的處理時間比最近的鄰近模式更多，但會輸出較高品質的影像。                                           |
| D2D1 \_ SCALE \_ 插補 \_ 模式 \_ 立方                 | 使用16個範例三核心來進行插補。 這個模式會使用大部分的處理時間，但會輸出較高品質的影像。                                                                        |
| D2D1 \_ SCALE \_ 內插補點 \_ 模式 \_ 多 \_ 樣本 \_ 線性 | 使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。 這種模式適合用來在具有少量圖元的影像上相應減少量。                                              |
| D2D1 \_ 調整 \_ 內插補點 \_ 模式 \_           | 根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。                                                                                                     |
| D2D1 \_ 調整 \_ 插補 \_ 模式 \_ 高品質的 \_ \_ 三階  | 如果 downscaling 與轉換矩陣有關，則使用可變大小的高品質三核心來執行預先縮小的影像。 然後使用三次插補模式來進行最終輸出。 |



 

> [!Note]  
> 如果您未選取模式，效果會預設為 D2D1 \_ 縮放 \_ 插補 \_ 模式 \_ 線性。

 

> [!Note]  
> 當調整時，非等向模式會產生 mipmap，不過，如果您在輸入至此效果的效果上將快取 **的屬性設** 為 true，則每次都不會針對足夠的小型影像產生 mipmap。

 

## <a name="output-bitmap"></a>輸出點陣圖

輸出點陣圖的位置和大小取決於指定的縮放比例和中心點。

您可以使用此方程式來計算輸出點陣圖的大小：<dl> BitmapSize？ (圖元) = 調整？ \*原始點陣圖大小？  (Dip) \* (UserDPI/96)   
BitmapSize<sub>y</sub> (圖元) = 縮放<sub>y</sub> \* 原始點陣圖大小<sub>y</sub> (dip) \* (UserDPI/96)   
</dl>

效果會將圖元的分數四捨五入到最接近的整個圖元。

點陣圖的位置是 (0、0) 或中心點屬性的值。

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

 

