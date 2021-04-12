---
title: 點狀擴散光源效果
description: 使用點擴散光源效果，建立影像，看起來會是不反射的介面，並以光線散佈在所有方向。 這種效果會使用 Alpha 色板作為高度地圖，並使用點光源來燈光影像。
ms.assetid: C98A4962-B9EB-4095-9AC4-F1C32C574892
keywords:
- 點漫射光源效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de97edfa6c2166d5c29649aabfe97761440f8f18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025371"
---
# <a name="point-diffuse-lighting-effect"></a>點狀擴散光源效果

使用點擴散光源效果，建立影像，看起來會是不反射的介面，並以光線散佈在所有方向。 這種效果會使用 Alpha 色板作為高度地圖，並使用點光源來燈光影像。

輸出點陣圖的色彩是淺色、光線位置和表面幾何的結果。 具有擴散光源之每個圖元的 Alpha 通道輸出一律為1.0。

這項效果的 CLSID 是 CLSID \_ D2D1PointDiffuse。 若要使用這項效果，請將 dxguid 新增至連結器相依性。

-   [範例影像](#example-image)
-   [效果屬性](#effect-properties)
-   [調整模式](#scale-modes)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

此處的範例會顯示點擴散光源效果的輸入和輸出影像。

![效果範例螢幕擷取畫面，顯示點漫射光源效果的輸入和輸出影像。](images/point-diffuse-example.png)

擴散光源指的是以多個方向反映的燈光，如下所示。

![擴散照明光線是散佈在所有方向。](images/point-diffuse-lighting.png)

效果會計算最終輸出圖元值，並使用這些方公式來計算：

![輸出點陣圖計算。](images/point-diffuse-formula1.png)

其中：<dl> k<sub>d</sub> = 擴散光源常數。 由使用者指定。  
![表面標準向量符號。](images/point-spec-mathchar-n.png) = surface 一般單位向量，x 和 y 的函式。  
![單位向量符號。](images/distant-spec-mathchar-l.png) = 從 surface 到 light 的單位向量。  
L<sub>r</sub>、l<sub>g</sub>、l<sub>b</sub> = RGB 元件中的淺色。  
</dl>

## <a name="effect-properties"></a>效果屬性



| 顯示名稱和索引列舉                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1 \_ POINTDIFFUSE \_ 的 \_ 照明 \_ 位置<br/>         | 點燈來源的光線位置。 屬性是 \_ \_ 定義為 (x、y、z) 的 D2D1 向量3F。 這些單位是與裝置無關的圖元 (Dip) 且未系結。 <br/> 此類型為 D2D1 \_ VECTOR \_ 3F。<br/> 預設值為 {0.0 f、0.0 f、0.0 f}。<br/>                                                                                                                                                                                                              |
| DiffuseConstant<br/> D2D1 POINTDIFFUSE 的一種 \_ \_ \_ 擴散 \_ 常數<br/>     | 擴散反映至傳入燈光數量的比率。 這個屬性必須介於0到10000之間，而且沒有用。 <br/> 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                          |
| SurfaceScale<br/> D2D1 \_ POINTDIFFUSE \_ 的 \_ 平面 \_ 縮放比例<br/>           | Z 方向的縮放比例。 介面比例沒有單位，而且必須介於0到10000之間。<br/> 此類型為 FLOAT。<br/> 預設值為 1.0 f。<br/>                                                                                                                                                                                                                                                                                                               |
| Color<br/> D2D1 \_ POINTDIFFUSE \_ 的 \_ 色彩<br/>                           | 傳入光線的色彩。 這個屬性會公開為向量 3 (R、G、B) ，用來計算 L<sub>R</sub>、l<sub>G</sub>、l<sub>b</sub>。 <br/> 此類型為 D2D1 \_ VECTOR \_ 3F。<br/> 預設值為 {1.0 f、1.0 f、1.0 f}。<br/>                                                                                                                                                                                                                                     |
| KernelUnitLength<br/> D2D1 \_ POINTDIFFUSE \_ 的 \_ 核心 \_ 單位 \_ 長度<br/> | Sobel 核心中用來以 X 和 Y 方向產生表面法線的元素大小。 這個屬性會對應至 Sobel 漸層中的 dx 和 dy 值。 這個屬性是 D2D1 \_ 向量 \_ 2F (核心單位長度 X、核心單位長度 Y) ，而且是在 (Dip/核心單位) 中定義。 效果會使用雙線性插補來調整點陣圖，以符合核心元素的大小。 <br/> 此類型為 D2D1 \_ VECTOR \_ 2f。<br/> 預設值為 {1.0 f、1.0 f}。<br/> |
| ScaleMode<br/> D2D1 \_ POINTDIFFUSE \_ 的 \_ 範圍調整 \_ 模式<br/>                 | 效果用來將影像調整為對應核心單位長度的插補模式。 有六個調整模式的品質和速度。 如需詳細資訊，請參閱 [調整模式](#scale-modes) 。 <br/> 此類型為 D2D1 \_ POINTDIFFUSE \_ SCALE \_ 模式。<br/> 預設值為 D2D1 \_ POINTDIFFUSE \_ SCALE \_ MODE \_ 線性。<br/>                                                                                                                                         |



 

## <a name="scale-modes"></a>調整模式



| 列舉型別                                            | 描述                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ \_ 最接近 \_ 鄰近的 D2D1 POINTDIFFUSE 調整模式     | 範例最接近的單一點，並使用該點。 這個模式會使用較少的處理時間，但會輸出最低品質的影像。                                                                           |
| D2D1 \_ POINTDIFFUSE \_ SCALE \_ 模式 \_ 線性                | 使用四個點取樣和線性插補。 此模式會輸出比最接近的鄰近程度更高的品質影像。                                                                                   |
| D2D1 \_ POINTDIFFUSE \_ SCALE \_ 模式 \_ 立方                 | 使用16個範例三核心來進行插補。 這個模式會使用大部分的處理時間，但會輸出較高品質的影像。                                                                        |
| D2D1 \_ POINTDIFFUSE \_ SCALE \_ MODE \_ 多重 \_ 範例 \_ 線性 | 使用單一圖元內的4個線性樣本來取得良好的邊緣消除鋸齒。 這種模式適合用來在具有少量圖元的影像上相應減少量。                                              |
| D2D1 \_ POINTDIFFUSE \_ SCALE \_ 模式 \_ 非等           | 根據點陣圖的轉換圖形，使用非等向篩選來取樣模式。                                                                                                     |
| D2D1 \_ POINTDIFFUSE \_ 調整 \_ 模式 \_ 高 \_ 品質 \_ 三階  | 如果 downscaling 與轉換矩陣有關，則使用可變大小的高品質三核心來執行預先縮小的影像。 然後使用三次插補模式來進行最終輸出。 |



 

> [!Note]  
> 如果您未選取模式，效果會預設為 D2D1 \_ POINTDIFFUSE \_ 縮放 \_ 模式 \_ 線性。

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

 

