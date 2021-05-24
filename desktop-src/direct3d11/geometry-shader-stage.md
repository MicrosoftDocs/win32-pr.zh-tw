---
title: 幾何著色器階段
description: 幾何著色器 (GS) 階段會執行應用程式指定的著色器程式碼，並以頂點作為輸入，以及在輸出上產生頂點的能力。
ms.assetid: F3208862-980E-403F-9154-13B34A882787
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3099ed5ede8dd89dc607ed838ff6e3fabfb16a69
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335362"
---
# <a name="geometry-shader-stage"></a>幾何著色器階段

幾何著色器 (GS) 階段會執行應用程式指定的著色器程式碼，並以頂點作為輸入，以及在輸出上產生頂點的能力。

## <a name="the-geometry-shader"></a>幾何著色器

不同于在單一頂點上操作的頂點著色器，幾何著色器的輸入是完整基本 (兩個頂點的頂點、三角形的三個頂點，或點) 的單一頂點。 幾何著色器也可以將邊緣-相鄰基本專案的頂點資料帶入輸入 (兩個線條的額外兩個頂點，另外三個用於三角形) 。 下圖顯示具有相鄰頂點的三角形和線條。

![有相鄰頂點的三角形和線條的圖](images/d3d10-gs.png)

|     | 類型                |
|-----|-----------------|
| **電視**  | 三角形頂點 |
| **AV**  | 相鄰頂點 |
| **低壓**  | 線條頂點     |



 

幾何著色器階段可以使用 \_ 由 IA 自動產生的 SV PrimitiveID [系統產生的值](d3d10-graphics-programming-guide-input-assembler-stage-using.md) 。 這樣就可以在需要時提取或運算每個基本類型資料。

幾何著色器階段可以輸出多個頂點來形成單一選取的拓撲 (GS 階段輸出拓撲可用： tristrip、linestrip 和 pointlist) 。 發出的基本類型數目可在幾何著色器的任何叫用內自由改變，雖然可發出的頂點最大數目必須以靜態方式宣告。 從幾何著色器調用發出的移除長度可以是任意的，而且可以透過 [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) HLSL 函式建立新的帶狀。

幾何著色器輸出可能會在記憶體中透過資料流輸出階段，對點陣化階段和/或頂點緩衝區供給。 對記憶體供給的輸出會擴充至個別點/線條/三角形清單 (與它們傳遞進入點陣化一模一樣)。

當幾何著色器為使用中時，它會針對向下傳遞或先前在管線中產生的每個基本類型叫用一次。 每次叫用幾何著色器，都會視為輸入叫用基本類型的資料，無論是單一點、單一線條或單一三角形。 管線中較早的三角形連環會導致針對連環中每個個別三角形叫用幾何著色器 (就像是連環向外擴充至三角形清單)。 您可以使用個別基本型別中每個頂點的所有輸入資料 (例如，三角形) 的3個頂點，以及連續的頂點資料（如果適用/可用）。

幾何著色器一次輸出一個頂點的資料，藉由將頂點附加至輸出資料流物件。 資料流程的拓撲取決於固定的宣告，選擇下列其中一個： PointStream、LineStream 或 TriangleStream 做為 GS 階段的輸出。 有三種類型的資料流程物件可用、PointStream、LineStream 和 TriangleStream，它們都是樣板化物件。 輸出的拓撲是由各自的物件類型決定，而附加至資料流的頂點的格式是由範本類型決定。 從其他叫用執行幾何著色器執行個體是不可部分完成的，除非新增至資料流的資料為序列。 特定幾合著色器叫用的輸出與其他叫用無關 (雖然會遵循順序)。 產生三角形連環的幾何著色易會在每次叫用時開始新的連環。

當幾何著色器輸出識別為系統轉譯值 (例如 SV \_ RenderTargetArrayIndex 或 sv \_ 位置) 時，硬體除了能夠將資料本身傳遞給下一個著色器階段以進行輸入之外，還會查看此資料並執行一些行為。 當幾何著色器的這類資料輸出對每個基本型 (例如 SV \_ RenderTargetArrayIndex 或 sv \_ ViewportArrayIndex) ，而不是依每個頂點的基礎 (例如 sv \_ CLIPDISTANCE \[ n \] 或 sv \_ 位置) 時，會從針對原始物件發出的開頭頂點取得每個基本資料。

部分完成的基本類型可能是由幾合著色器產生，如果幾何著色器結束且基本類型未完成。 未完成的基本類型會捨棄且無訊息。 這類似 IA 處理部分未完成基本類型的方式。

幾何著色器可以執行載入和紋理取樣作業，在不需要螢幕空間衍生項目時 (samplelevel、samplecmplevelzero、samplegrad)。

可以在幾何著色器中執行的演算法包括：

-   Point Sprite Expansion
-   Dynamic Particle Systems
-   Fur/Fin Generation
-   Shadow Volume Generation
-   Single Pass Render-to-Cubemap
-   Per-Primitive Material Swapping
-   Per-Primitive 材質設定-包括將 barycentric 座標產生為基本資料，讓圖元著色器可以執行自訂屬性插補 (如需更高順序的正常插補範例，請參閱 [CubeMapGS 範例](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖形管線](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[ (Direct3D 10) 的管線階段 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 