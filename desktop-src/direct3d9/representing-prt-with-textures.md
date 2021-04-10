---
description: DirectX SDK 中包含的 PRTDemo 範例和 PRTCmdLine 模擬器代表網格頂點的傳輸向量。
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: 使用 (Direct3D 9) 的材質表示 PRT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4647cfc85451ede9507e007ed556a203a3cd890a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187547"
---
# <a name="representing-prt-with-textures-direct3d-9"></a>使用 (Direct3D 9) 的材質表示 PRT

DirectX SDK 中包含的 PRTDemo 範例和 PRTCmdLine 模擬器代表網格頂點的傳輸向量。 為了精確代表 PRT 的信號，這可能需要鑲嵌，對於目前的遊戲來說可能不切實際。 代表材質地圖中的傳輸向量是替代方法，其資料成本與網格複雜度無關。 有幾種方式可使用 D3DX PRT 程式庫產生傳輸向量紋理對應。

## <a name="precomputing-transfer-vectors"></a>一般來說傳輸向量

其中一個方法是修改 PRTDemo 和 PRTCmdLine 範例，以在介面參數化中的每個材質計算傳輸向量。 若要這樣做：

1.  修改 [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) 的呼叫，以從網格中解壓縮紋理座標 (ExtractUVs 必須是 **TRUE**) 
2.  使用相同的材質大小，以 [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)取代 [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)呼叫。

所有 ID3DXPRTEngine 方法都適用于每個材質的模擬，但： ComputeBounceAdaptive、ComputeSSAdaptive、ComputeSS 和 ComputeDirectLightingSHAdaptive 除外。 雖然材質空間模擬會產生正確的結果，但通常可能很慢，因為很可能會以高密度的方式計算傳輸向量。

另一種方法是計算可調整的每個頂點 PRT 模擬 (以及將用於每個材質資料) 的材質座標，然後呼叫 [**ID3DXPRTEngine：： ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (使用以 [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) 建立的輸出緩衝區（在適當的解析) 中）。 這適用于 SDK 中的所有 D3DX PRT 功能，而且通常會比直接計算每個材質傳輸緩衝區更有效率。

## <a name="runtime-calculations"></a>執行時間計算

如果使用單一叢集，則可以像任何其他材質一樣篩選和 mip 對應結果，而圖元著色器與 PRTDemo 隨附的頂點著色器程式碼相同。

如果壓縮產生多個叢集，您就無法篩選或 mipmap 資料，因為叢集索引不是連續的。 以下是處理多叢集資料的一些替代方案：

-   在圖元著色器中自行進行篩選。 可惜的是，基於效能的考慮，這通常是不切實際的。
-   如果紋理是低解析度的非 mip 對應紋理 (ie：輕量地圖) ，只要直接在材質空間中計算光源（不會進行篩選），就可能更有效率，並以陰影材質呈現物件。 這基本上是完全在 GPU 上建立的動態燈光地圖。
-   如果使用了材質塔 (請參閱 [使用 UVAtlas (Direct3D 9) ](using-uvatlas.md)) ，您可以藉由將材質空間中已連接元件中的所有傳輸向量都在相同的叢集中，以手動方式叢集場景。 如此一來，您就可以篩選材質，因為所有存取的材質都是在相同的叢集中。 指定臉部的叢集識別碼可以從頂點著色器傳播。

圖元著色器的常數暫存器數目較少，因此圖元著色器與頂點著色器有點不同。 將每個叢集的工作儲存在低解析度的動態材質中，並使用材質載入，會是使用多個叢集時最有效率的轉譯方式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預先計算 Radiance 傳輸](precomputed-radiance-transfer.md)
</dt> <dt>

[PRT 示範範例](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)
</dt> <dt>

[PRT 模擬器 (prtcmdline.exe) ](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)
</dt> </dl>

 

 



