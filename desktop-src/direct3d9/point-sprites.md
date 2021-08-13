---
description: Direct3D 9 中點 sprite 的支援可讓您以高效能轉譯 (物件) 的點。 點 sprite 是泛用的泛用點，可讓任意圖形依照材質的定義來呈現。
ms.assetid: a9046c7e-779c-4f33-b8ff-f189da3dcfc5
title: '點 Sprite (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90abd21207d9b3866ff93bd6c73069b655056f1c28811689762b0ce669183793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520463"
---
# <a name="point-sprites-direct3d-9"></a>點 Sprite (Direct3D 9) 

Direct3D 9 中點 sprite 的支援可讓您以高效能轉譯 (物件) 的點。 點 sprite 是泛用的泛用點，可讓任意圖形依照材質的定義來呈現。

-   [點基本呈現控制項](#point-primitive-rendering-controls)
-   [點大小計算](#point-size-computations)
-   [點轉譯](#point-rendering)

## <a name="point-primitive-rendering-controls"></a>點基本呈現控制項

Direct3D 9 支援其他參數，以控制點 sprite (點基本) 的呈現。 這些參數可讓點成為變數大小，並套用完整紋理對應。 每個點的大小是由應用程式指定的大小所決定，並結合 Direct3D 所計算的以距離為基礎的函式。 應用程式可以將點大小指定為每個頂點，或設定 D3DRS \_ dialog，以套用至沒有每個頂點大小的點。 點大小是以相機空間單位來表示，但應用程式在將轉換後的彈性頂點格式傳遞 (FVF) 頂點時除外。 在此情況下，不會套用以距離為基礎的函式，而且點大小會以轉譯目標的圖元單位表示。

當轉譯點取決於 D3DRS POINTSPRITEENABLE 的設定時，會計算並使用材質座標 \_ 。 當此值設定為 **TRUE** 時，會設定材質座標，讓每個點都顯示完整紋理。 一般來說，這只適用于點明顯大於一個圖元時。 當 D3DRS \_ POINTSPRITEENABLE 設定為 **FALSE** 時，每個點的頂點材質座標都會用於整個點。

## <a name="point-size-computations"></a>點大小計算

點大小取決於 D3DRS \_ POINTSCALEENABLE。 如果此值設定為 **FALSE**，則會使用應用程式指定的點大小做為螢幕空間 (轉換後的) 大小。 在螢幕空間中傳遞給 Direct3D 的頂點沒有計算的點大小;指定的點大小會轉譯為螢幕空間大小。

如果 D3DRS \_ POINTSCALEENABLE 為 **TRUE**，Direct3D 會根據下列公式計算螢幕空間點大小。 應用程式指定的點大小以相機空間單位表示。

S = Vh \* s <sub>i</sub> \* (1/ (A + B \* D ₑ + C \* ( D ₑ² ) ) ) 

在此公式中，輸入點大小（ <sub>i</sub>）是每個頂點或 D3DRS dialog 轉譯狀態的值 \_ 。 點縮放因數、D3DRS \_ POINTSCALE \_ A、D3DRS \_ POINTSCALE \_ B 和 D3DRS \_ POINTSCALE \_ C 會以點 A、B 和 c 表示。視口的高度（V h）是代表視口的 [**D3DVIEWPORT9**](d3dviewport9.md) 結構高度成員。 D ₑ，從眼睛到) 原點 (眼睛的距離，會以點的眼睛空間位置 (X ₑ、Y ₑ、Z ₑ) ，然後執行下列作業來計算。

D ₑ = sqrt (X ₑ² + Y ₑ² + Z ₑ²) 

最大點數大小（Pm ₐₓ）是以 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 MaxPointSize 成員或 D3DRS \_ dialog 最大轉譯狀態的較小者來決定 \_ 。 最小的點大小（P<sub>分鐘</sub>）是藉由查詢 D3DRS dialog min 的值來決定 \_ \_ 。 因此，最後的畫面空間點大小是以下列方式決定。

-   如果 Ss > Pm ₐₓ，則 S = P m ₐₓ
-   如果 S < P<sub>分鐘</sub>，則 s = p <sub>分鐘</sub>
-   否則，S = S

## <a name="point-rendering"></a>點轉譯

螢幕空間大小 S 的螢幕空間點、P = ( X、Y、Z、W) ，會以下列四個頂點的四邊形來進行柵格化。

 ( ( X + S/2、Y + S/2、Z、W) 、 ( X + S/2、Y-S/2、Z、W) 、 ( X-S/2、Y-S/2、Z、W) 、 ( X-S/2、Y + S/2、Z、W) ) 

頂點色彩屬性會在每個頂點複製;因此，每個點一律會以固定色彩呈現。

紋理索引的指派是由 [D3DRS POINTSPRITEENABLE 轉譯 \_ 狀態] 設定所控制。 如果 D3DRS \_ POINTSPRITEENABLE 設定為 **FALSE**，則頂點材質座標會在每個頂點上重複。 如果 D3DRS \_ POINTSPRITEENABLE 設定為 **TRUE**，則四個頂點上的材質座標會設定為下列值。

 (0. F、0 F) 、 (0 F.、1. F) 、 (1. F、0 F) 、 (1. F、1. F) 

如下圖所示。

![正方形的圖表，其中包含 (u、v) 和 (x、y) 座標值的標記頂點](images/spritepoint.png)

啟用裁剪時，會以下列方式裁剪點點。 如果頂點超過深度值的範圍（ [**D3DVIEWPORT9**](d3dviewport9.md) 結構的 MinZ 和 MaxZ），將會在其中呈現場景，則點會存在於視圖的分割區之外，而且不會呈現。 如果考慮點大小的點是完全在 X 和 Y 的視口之外，則不會呈現點;其餘的點都會呈現。 點位置可能會位於 X 或 Y 的視口之外，而且仍然是部分可見的。

點可能會或可能不會正確地裁剪到使用者定義的剪輯平面。 如果 \_ 未在 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 PrimitiveMiscCaps 成員中設定 D3DPMISCCAPS CLIPPLANESCALEDPOINTS，則只會根據頂點位置將點裁剪到使用者定義的剪輯平面，以忽略點大小。 在此情況下，當頂點位置位於剪輯平面內時，會完全轉譯縮放點，並在頂點位置超出剪輯平面時捨棄。 應用程式可以藉由將框線幾何新增至與最大點數大小相同的剪輯平面，來防止可能的成品。

如果 \_ 已設定 D3DPMISCCAPS CLIPPLANESCALEDPOINTS 位，則會將縮放點正確地裁剪到使用者定義的剪輯平面。

硬體頂點處理不一定會支援點大小。 例如，如果在 \_ \_ 硬體抽象層上使用 D3DCREATE 硬體 VERTEXPROCESSING 建立裝置 (HAL) 裝置 (D3DDEVTYPE \_ Hal) 將 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構的 MaxPointSize 成員設定為1.0 或0.0，則所有點都是單一圖元。 若要轉譯小於1.0 的圖元點 sprite，您必須使用 FVF TL (轉換和亮) 頂點或軟體頂點處理 (D3DCREATE \_ software \_ VERTEXPROCESSING) ，在這種情況下，Direct3D 執行時間會模擬點 sprite 轉譯。

執行頂點處理並支援點 sprite-MaxPointSize 設定為大於 1.0 f-的硬體裝置必須執行 nontransformed sprite 的大小計算，而且必須正確設定 TL 頂點的每個頂點或 D3DRS \_ POINTSIZED3DRS \_ dialog。

如需有關點、線條和三角形之轉譯規則的詳細資訊，請參閱 [ (Direct3D 9) 的點陣化規則 ](rasterization-rules.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點管線](vertex-pipeline.md)
</dt> </dl>

 

 



