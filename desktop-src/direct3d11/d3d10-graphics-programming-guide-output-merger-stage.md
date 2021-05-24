---
title: 輸出合併階段
description: " (OM) 階段的輸出合併會使用管線狀態的組合、圖元著色器所產生的圖元資料、轉譯目標的內容，以及深度/樣板緩衝區的內容，來產生最終呈現的圖元色彩。"
ms.assetid: 8be68c15-2deb-4804-b683-30080a876189
keywords:
- " (Direct3D 10) 的輸出合併階段"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8de2851fdea3a22cc42033d2c13454be72ba8ab
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335212"
---
# <a name="output-merger-stage"></a>輸出合併階段

 (OM) 階段的輸出合併會使用管線狀態的組合、圖元著色器所產生的圖元資料、轉譯目標的內容，以及深度/樣板緩衝區的內容，來產生最終呈現的圖元色彩。 OM 階段是決定哪些圖元可見 (具有深度樣板測試) 和混合最後圖元色彩的最後一個步驟。



Direct3D 9 與 Direct3D 10 之間的差異：

- Direct3D 9 使用 [Alpha 測試狀態](/windows/desktop/direct3d9/alpha-testing-state) 來實行 Alpha 測試 (，) 來控制是否要將圖元寫入輸出呈現目標。
- Direct3D 10 和更新版本不會) 執行 Alpha 測試 (或 Alpha 測試狀態。 這可以使用圖元著色器或深度/樣板功能來控制。



 

## <a name="depth-stencil-testing-overview"></a>Depth-Stencil 測試總覽

深度樣板緩衝區，這會建立為紋理資源，可以包含深度資料和樣板資料這兩個資料。 深度資料用於判斷哪些像素最靠近相機，以及樣板資料用於遮罩哪一個可以更新的像素。 最後，深度與樣板數值資料二者都由輸出合併階段，用於判斷是否已繪製像素。 下圖顯示如何完成深度樣板測試的概念方式。

![深度樣板測試的運作方式的圖表](images/d3d10-depth-stencil-test.png)

若要設定深度樣板測試，請參閱[設定深度樣板功能](d3d10-graphics-programming-guide-depth-stencil.md)。 深度樣板物件封裝深度樣板狀態。 應用程式可以指定深度樣板的狀態，否則 OM 階段將會使用預設值。 如果已停用多重取樣，就以像素為基礎執行混合作業。 如果啟用多重取樣，會以每個多重取樣為基礎進行混合。

使用深度緩衝區的程序來判斷哪一個像素應繪製，這稱為「深度緩衝」，有時也稱為「z 緩衝」。

一旦深度值到達輸出合併階段 (不論從插補或從像素著色器)，它們永遠都箝制︰z = min(Viewport.MaxDepth,max(Viewport.MinDepth,z))，根據深度緩衝區的格式/精準度，使用浮點規則。 鉗制之後，比較深度值 (使用 DepthFunc) 與現有深度緩衝區值。 如果未繫結任何深度緩衝區，一律通過深度測試。

如果沒有任何深度緩衝區格式的樣板元件，或者未繫結任何深度緩衝區，則一律通過樣板測試。 否則，功能會與 Direct3D 9 的功能不相同。

一次只有一個深度/樣板緩衝區可以使用；任何繫結的資源檢視必須符合 (相同的大小和維度) 深度/樣板檢視。 這不表示資源大小必須符合，只是檢視大小必須符合。

如需深度樣板測試的詳細資訊，請參閱 [教學課程 14](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)。

## <a name="blending-overview"></a>混色總覽

混合結合了一個或多個像素值，以建立最終像素色彩。 下圖顯示混合像素資料的程序。

![混合資料的運作方式的圖表](images/d3d10-blend-state.png)

在概念上，您可以將此流程圖表視覺化在輸出合併階段中執行兩次：第一個是混合 RGB 資料，而第二個則會混合 Alpha 資料。 若要瞭解如何使用 API 建立並設定混合狀態，請參閱[設定混合功能](d3d10-graphics-programming-guide-blend-state.md)。

固定函式混合可以針對每個轉譯目標單獨啟用。 不過，只有一組混合控制項，如此相同混合才會套用到所有啟用混合的 RenderTarget。 混合值 (包括 BlendFactor) 始終會限制為混合之前的轉譯目標格式的範圍之內。 關於轉譯目標類型，按照每個轉譯目標完成鉗制。 唯一例外是，位鉗制的 float16、float11 或 float10 格式，如此這些格式的混合作業都可以至少等於精確度/範圍，完成為輸出格式。 NaN 的及簽署的零會針對所有案例傳播 (包括 0.0 混合重量)。

當您使用 sRGB 轉譯目標時，執行階段會在執行混合之前，將轉譯目標色彩轉換為線性空間。 執行階段會在其將值儲存回轉譯目標之前，將最終混合值轉換回 sRGB 空間。

Direct3D 9 與 Direct3D 10 之間的差異：

- 在 Direct3D 9 中，固定函式的混合可以針對每個呈現目標個別啟用。
- 在 Direct3D 10 和更新版本中，有一個 blend 狀態原因;因此，可以為所有呈現目標設定一個混合值。



 

### <a name="dual-source-color-blending"></a>Dual-Source 色彩混合

這項功能可讓輸出合併階段同時使用圖元著色器輸出 (o0 和 o1) 做為混合作業的輸入，並在插槽0使用單一轉譯目標。 有效的混合作業包括︰新增、減除和 revsubtract。 SrcBlend、DestBlend、SrcBlendAlpha 或 DestBlendAlpha 的有效 blend 選項包括： **D3D11 \_ blend \_ SRC1 \_ color**、 **D3D11 \_ blend \_ INV \_ SRC1 \_ color**、 **D3D11 \_ blend \_ SRC1 \_ ALPHA**、 **D3D11 \_ blend \_ inv \_ SRC1 \_ Alpha**。 混合方程式和輸出寫入遮罩會指定像素著色器將輸出哪些元件。 忽略額外的元件。

寫入到其他像素著色器輸出 (o2、o3 等) 未定義；若不是繫結到插槽 0，您可能不寫入轉譯目標。 寫入 oDepth 在雙來源色彩混合期間是有效的。

如需範例，請參閱 [混色圖元著色器輸出](d3d10-graphics-programming-guide-blend-state.md)。

## <a name="multiple-rendertargets-overview"></a>多個 RenderTargets 總覽

像素著色器可用來轉譯為至少 8 個不同轉譯目標，所有都必須是相同類型 (緩衝、Texture1D、Texture1DArray 等等）。 此外，所有轉譯目標在所有維度 (寬地、高度、深度、陣列大小、樣本計數) 中必須有相同的大小。 各個轉譯目標可能會有不同的資料格式。

您可以使用任何組合的轉譯目標插槽 (最多達 8 個)。 不過，資源檢視無法同時繫結到多個轉譯目標插槽。 檢視可重複使用，只要不同時使用資源。

## <a name="output-write-mask-overview"></a>Output-Write Mask 總覽

使用輸出寫入遮罩來控制 (按每個元件) 可寫入轉譯目標的資料。

## <a name="sample-mask-overview"></a>範例遮罩總覽

樣本遮罩是 32 位元多重取樣涵蓋範圍的遮罩，判斷哪些樣本在作用中的轉譯目標中已更新。 只允許一個樣本遮罩。 樣本遮罩中位元到資源中樣本的對應，是由使用者定義。 若是 n 樣本轉譯，會使用樣本遮罩的第一個 n 位元 (從 LSB)(32 位元它的上限位元)。


## <a name="in-this-section"></a>本節內容



| 主題                                                                                                    | 描述                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [設定 Depth-Stencil 功能](d3d10-graphics-programming-guide-depth-stencil.md)<br/> | 本章節涵蓋的步驟，內容為設定深度樣板緩衝區及輸出合併階段的深度樣板狀態。<br/>                                                                                                                           |
| [設定混合功能](d3d10-graphics-programming-guide-blend-state.md)<br/>        | 在輸出值寫入轉譯目標之前，會對每個圖元著色器輸出 (RGBA 值) 執行混合作業。 如果啟用取樣，則會在每個執行程式上進行混合;否則，會在每個圖元上執行混色。<br/> |
| [深度偏差](d3d10-graphics-programming-guide-output-merger-stage-depth-bias.md)<br/>             | 在3D 空間中有共置的多邊形，會顯示為不是共置的多邊形，方法是將 z 偏差 (或深度偏差) 新增至每一個。<br/>                                                                                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖形管線](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[ (Direct3D 10) 的管線階段 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

