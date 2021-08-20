---
title: 點狀反射光源效果
description: 使用點反射光源效果，建立看似反射表面的影像。
ms.assetid: 89E22FD0-BB7F-465F-A79C-056CA9F14F5D
keywords:
- 點反射光源效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37adb0c6ea0ca946abf819730dcc378f421bf2c220dc0ab8d41916f570501d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075139"
---
# <a name="point-specular-lighting-effect"></a>點狀反射光源效果

使用點反射光源效果，建立看似反射表面的影像。 效果會使用影像的 Alpha 色板作為高度地圖和您放置的點光源，並根據 Phong 光源模型的反射部分計算反映和淺色。

輸出點陣圖的色彩是淺色、光線位置和表面幾何的結果。 每個圖元的 Alpha 通道輸出（具有反射光源）是該圖元的紅色、綠色和藍色通道輸出的最大值。

這項效果的 CLSID 是 CLSID \_ D2D1PointSpecular。

-   [範例影像](#example-image)
-   [點燈來源](#point-light-source)
-   [高度地圖和一般向量](#height-map-and-normal-vector)
-   [反射光源常數和指數](#specular-lighting-constant-and-exponent)
-   [效果屬性](#effect-properties)
-   [縮放模式](#scales-modes)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

此處的範例會顯示點反射光源效果的輸入和輸出影像。

![顯示點反射光源效果之輸入和輸出影像的效果範例螢幕擷取畫面。](images/point-spec-example.png)

反射光源指的是根據 Phong 光源模型反映在特定方向的燈光。

![用來 cacluate 點陣圖反射光源輸出的向量圖。](images/point-spec-reflected1.png)

效果會使用以下的方公式來計算最終輸出圖元值：

![用於計算最終圖元值的方程式。 ](images/point-spec-formula-output.png)

其中<dl> K？ = 反射光源常數。  
![表面標準單元向量符號。 ](images/point-spec-mathchar-n.png)= surface 一般單位向量，也就是 x 和 y 的函式。 請參閱計算的 [高度地圖和一般向量](#height-map-and-normal-vector) 。  
![中間的單位向量符號。 ](images/point-spec-mathchar-h.png)= 紅眼單位向量和淺色單位向量之間的「半」單位向量。 請參閱計算的 [Point light 來源](#point-light-source) 。  
L<sub>r</sub>、l<sub>g</sub>、l<sub>b</sub> = RGB 元件中的淺色。  
</dl>

您將反射光源常數設定為 [ *SpecularConstant* ] 屬性，並將 [淺色] 色彩設定為 [ *色彩* ] 屬性。

## <a name="point-light-source"></a>點燈來源

點燈光來源會以所有方向發出燈光，例如影像中的影像。

![點燈會以所有方向發出燈光。](images/point-spec-light.png)

您可以使用 *LightPosition* 屬性設定光源來源的位置。 效果會使用此處的方程式，計算點光源的燈光向量 L：

![淺向量方程式。](images/point-spec-formula3.png)

光在哪裡？、Light<sub>y</sub>和淺色<sub>z</sub> 是輸入光線位置。 效果會計算中間向量的中向量 ![ 符號。](images/point-spec-mathchar-h.png) 如 Phong 光源模型中所定義，在這裡使用方程式。 光源模型假設眼睛向量（ ![ 眼睛向量符號 ](images/point-spec-mathchar-e.png) ）位於 (0、0、1) 。

![中間向量方程式。](images/point-spec-formula4.png)

L 和 H 都會正規化為單位長度向量。

## <a name="height-map-and-normal-vector"></a>高度地圖和一般向量

效果會根據其 Alpha 色板產生輸入影像的高度地圖。

高度 (Z) 元件會使用方程式來計算：

![用來計算介面高度 (z) 的方程式。](images/point-spec-formula6.png)

效果會計算 surface normal， ![一般向量符號。](images/point-spec-mathchar-n.png)，適用于使用 Sobel 漸層的輸入點陣圖。

## <a name="specular-lighting-constant-and-exponent"></a>反射光源常數和指數

反射光線代表從影像高度地圖的表面反映出來的光線。 您可以指定 *SpecularExponent* 屬性，以判斷來自點陣圖的反射反映數量。

較大的指數代表 shinier 物件，並以更具焦點的形狀來反映淺色。

*SpecularConstant* 屬性 K？將反映的燈光數量定義為連入燈光的比率。

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1 \_ POINTSPECULAR \_ 的 \_ 照明 \_ 位置<br/>         | 點燈來源的光線位置。 屬性是 \_ \_ 定義為 (x、y、z) 的 D2D1 向量3F。 單位是以與裝置無關的圖元為單位， (Dip) 且值沒有單位或未系結。 此類型為 D2D1 \_ VECTOR \_ 3F。<br/> 預設值為 {0.0 f、0.0 f、0.0 f}。<br/>                                                                                                                                                                                      |
| SpecularExponent<br/> D2D1 \_ POINTSPECULAR 的 \_ \_ \_<br/>   | Phong 光源方程式中反射詞彙的指數。 較大的值會對應至更反射的介面。 此值沒有單位，而且必須介於1.0 到128之間。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> D2D1 \_ POINTSPECULAR \_ 的 \_ 反射 \_ 常數<br/>   | 反射反映與連入燈光的比率。 值沒有單位，而且必須介於0到10000之間。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> D2D1 \_ POINTSPECULAR \_ 的 \_ 平面 \_ 縮放比例<br/>           | 用來產生高度地圖之 Z 方向的縮放比例。 值沒有單位，而且必須介於0到10000之間。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ POINTSPECULAR \_ 的 \_ 色彩<br/>                           | 傳入光線的色彩。 這個屬性會公開為 D2D1 \_ 向量 \_ 3F (R、G、B) ，用來計算 L<sub>R</sub>、L<sub>G</sub>、l<sub>b</sub>。 此類型為 D2D1 \_ VECTOR \_ 3F。<br/> 預設值為 {1.0 f、1.0 f、1.0 f}。<br/>                                                                                                                                                                                                                             |
| KernelUnitLength<br/> D2D1 \_ POINTSPECULAR \_ 的 \_ 核心 \_ 單位 \_ 長度<br/> | Sobel 核心中用來以 X 和 Y 方向產生表面法線的元素大小。 這個屬性會對應至 Sobel 漸層中的 dx 和 dy 值。 這個屬性是 D2D1 \_ 向量 \_ 2F (核心單位長度 X、核心單位長度 Y) ，而且是在 (Dip/核心單位) 中定義。 效果會使用雙線性插補來調整點陣圖，以符合核心元素的大小。 此類型為 D2D1 \_ VECTOR \_ 2f。<br/> 預設值為 {1.0 f、1.0 f}。<br/> |
| ScaleMode<br/> D2D1 \_ POINTSPECULAR \_ 的 \_ 範圍調整 \_ 模式<br/>                 | 效果用來將影像調整為對應核心單位長度的插補模式。 有六個調整模式的品質和速度。 如需詳細資訊，請參閱 [調整模式](#scales-modes) 。 <br/> 此類型為 D2D1 \_ POINTSPECULAR \_ SCALE \_ 模式。<br/> 預設值為 D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ 線性。<br/>                                                                                                                          |



 

## <a name="scales-modes"></a>縮放模式



| 列舉型別                                             | 描述                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 POINTSPECULAR 調整模式     | 範例最接近的單一點，並使用該點。 這個模式會使用較少的處理時間，但會輸出最低品質的影像。                                                                           |
| D2D1 \_ POINTSPECULAR \_ SCALE \_ 模式 \_ 線性                | 使用四個點取樣和線性插補。 此模式會輸出比最接近的鄰近程度更高的品質影像。                                                                                   |
| D2D1 \_ POINTSPECULAR \_ SCALE \_ 模式 \_ 立方                 | 使用16個範例三核心來進行插補。 這個模式會使用大部分的處理時間，但會輸出較高品質的影像。                                                                        |
| D2D1 \_ POINTSPECULAR \_ SCALE \_ MODE \_ 多重 \_ 範例 \_ 線性 | 使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。 這種模式適合用來在具有少量圖元的影像上相應減少量。                                              |
| D2D1 \_ POINTSPECULAR \_ SCALE \_ 模式 \_ 非等           | 根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。                                                                                                     |
| D2D1 \_ POINTSPECULAR \_ 調整 \_ 模式 \_ 高 \_ 品質 \_ 三階  | 如果 downscaling 與轉換矩陣有關，則使用可變大小的高品質三核心來執行預先縮小的影像。 然後使用三次插補模式來進行最終輸出。 |



 

> [!Note]  
> 如果您未選取模式，效果會預設為 D2D1 \_ POINTSPECULAR \_ 縮放 \_ 模式 \_ 線性。

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

 

