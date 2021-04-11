---
title: 遠距反射光源效果
description: 使用「最遠反射光源」效果來建立影像，看起來會是一個反射表面，其中光源看似從長距離 (例如 sun 或額外負荷燈) 。
ms.assetid: 74D71A2D-8D1D-4FDE-898A-2D2F5A8D5D31
keywords:
- 遠處反射光源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fa21553e36839f854b4567b2aa2a3805406380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385117"
---
# <a name="distant-specular-lighting-effect"></a>遠距反射光源效果

使用「最遠反射光源」效果來建立影像，看起來會是一個反射表面，其中光源看似從長距離 (例如 sun 或額外負荷燈) 。 這種效果會使用 Alpha 色板作為高度地圖，並使用遠較遠的光源來燈光影像。

輸出點陣圖的色彩是淺色、光線位置和表面幾何的結果。 每個圖元的 Alpha 通道輸出（具有反射光源）是該圖元的紅色、綠色和藍色通道輸出的最大值。

這項效果的 CLSID 是 CLSID \_ D2D1DistantSpecular。

-   [範例影像](#example-image)
-   [遠光源來源](#distant-light-source)
-   [效果屬性](#effect-properties)
-   [調整模式](#scale-modes)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

此處的範例會顯示最遠反射光源效果的輸入和輸出影像。

![效果範例螢幕擷取畫面，顯示最遠反射光源效果的輸入和輸出影像。 ](images/distant-spec-example.png)

最後的輸出點陣圖可以使用下列方公式來計算。

![輸出點陣圖計算](images/distant-spec-formula1.png)

其中 <dl> K？ = 反射光源常數。  
![表面標準符號。 ](images/point-spec-mathchar-n.png)= surface 一般單位向量。  
![中間向量符號。 ](images/point-spec-mathchar-h.png)= 紅眼單位向量和淺色單位向量之間的「半」單位向量。  
C<sub>r</sub>、c<sub>g</sub>、c<sub>b</sub> = RGB 元件中的淺色。  
</dl>

## <a name="distant-light-source"></a>遠光源來源

此處的影像顯示從遠處光源開始的光線方向範例。

![遠光源來源](images/distant-spec-lightsource.png)

效果會使用 azimuth 和提高許可權參數來計算光線向量 ![l 向量。](images/distant-spec-mathchar-l.png) 使用下列方所示：

![light 向量計算](images/distant-spec-formula2.png)

Light？、Light<sub>y</sub>和 Light<sub>z</sub> 是輸入光源位置值。

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 方位<br/> D2D1 \_ DISTANTSPECULAR \_ 的 \_ AZIMUTH<br/>                       | 在 XY 平面中，相對於計數器時鐘方向的 X 軸的方向角度。 單位是以度為單位，且必須介於0到360度之間。<br/> 此類型為 FLOAT。<br/> 預設值為 0.0 f。<br/>                                                                                                                                                                              |
| Elevation<br/> D2D1 \_ DISTANTSPECULAR \_ 的 \_ 高度提升<br/>                   | 在 YZ 平面中，相對於計數器時鐘方向的 Y 軸相對於 Y 軸的方向角度。 單位是以度為單位，且必須介於0到360度之間。 <br/> 此類型為 FLOAT。<br/> 預設值為 0.0 f。<br/>                                                                                                                                                                             |
| SpecularExponent<br/> D2D1 \_ DISTANTSPECULAR 的 \_ \_ \_<br/>   | Phong 光源方程式中反射詞彙的指數。 較大的值會對應至更反射的介面。 值沒有單位，而且必須介於1.0 到128之間。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                          |
| SpecularConstant<br/> D2D1 \_ DISTANTSPECULAR \_ 的 \_ 反射 \_ 常數<br/>   | 反射反映與連入燈光的比率。 值沒有單位，而且必須介於0到10000之間。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                             |
| SurfaceScale<br/> D2D1 \_ DISTANTSPECULAR \_ 的 \_ 平面 \_ 縮放比例<br/>           | Z 方向的縮放比例。 值沒有單位，而且必須介於0到10000之間。 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                |
| Color<br/> D2D1 \_ DISTANTSPECULAR \_ 的 \_ 色彩<br/>                           | 傳入光線的色彩。 這個屬性會公開為 D2D1 \_ 向量 \_ 3F (R、G、B) ，用來計算 L<sub>R</sub>、L<sub>G</sub>、l<sub>b</sub>。 此類型為 D2D1 \_ VECTOR \_ 3F。<br/> 預設值為 {1.0 f、1.0 f、1.0 f}。<br/>                                                                                                                                                                                       |
| KernelUnitLength<br/> D2D1 \_ DISTANTSPECULAR \_ 的 \_ 核心 \_ 單位 \_ 長度<br/> | Sobel 核心中用來以 X 和 Y 方向產生表面法線的元素大小。 這個屬性是 D2D1 \_ 向量 \_ 2F (核心單位長度 X、核心單位長度 Y) ，而且是以 (與裝置無關的圖元來定義， (dip) /Kernel 單位) 。 效果會使用雙線性插補來調整點陣圖，以符合核心元素的大小。 此類型為 D2D1 \_ VECTOR \_ 2f。<br/> 預設值為 {1.0 f、1.0 f}。<br/> |
| ScaleMode<br/> D2D1 \_ DISTANTSPECULAR \_ 的 \_ 範圍調整 \_ 模式<br/>                 | 效果用來將影像調整為對應核心單位長度的插補模式。 有六個調整模式的品質和速度。<br/> 此類型為 D2D1 \_ DISTANTSPECULAR \_ SCALE \_ 模式。<br/> 預設值為 D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ 線性。<br/>                                                                                                                                 |



 

## <a name="scale-modes"></a>調整模式



| 列舉型別                                               | 描述                                                                                                                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 DISTANTSPECULAR 調整模式     | 範例最接近的單一點，並使用該點。 這個模式會使用較少的處理時間，但會輸出最低品質的影像。                                                                           |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ 模式 \_ 線性                | 使用四個點取樣和線性插補。 此模式會輸出比最接近的鄰近程度更高的品質影像。                                                                                   |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ 模式 \_ 立方                 | 使用16個範例三核心來進行插補。 這個模式會使用大部分的處理時間，但會輸出較高品質的影像。                                                                        |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ 多重 \_ 範例 \_ 線性 | 使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。 這種模式適合用來在具有少量圖元的影像上相應減少量。                                              |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ 模式 \_ 非等           | 根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。                                                                                                     |
| D2D1 \_ DISTANTSPECULAR \_ 調整 \_ 模式 \_ 高 \_ 品質 \_ 三階  | 如果 downscaling 與轉換矩陣有關，則使用可變大小的高品質三核心來執行預先縮小的影像。 然後使用三次插補模式來進行最終輸出。 |



 

> [!Note]  
> 如果您未選取模式，效果會預設為 D2D1 \_ DISTANTSPECULAR \_ 縮放 \_ 模式 \_ 線性。

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

 

