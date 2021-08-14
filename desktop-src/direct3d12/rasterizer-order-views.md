---
title: 依轉譯器排序的視圖
description: 依瀏覽器排序的視圖 (ROVs) 允許圖元著色器程式碼將未排序的存取視圖系結標示為變更 UAVs 的圖形管線結果順序的一般需求。
ms.assetid: D308BF3E-8CBE-4DF0-B020-4D202E858D99
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214098f70608d5f20d24edb1312593c6215abea12efecfc6eea97148e8855cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300979"
---
# <a name="rasterizer-ordered-views"></a>依轉譯器排序的視圖

依轉譯器排序的視圖 (ROVs) 允許圖元著色器程式碼將未排序的存取視圖標記 (UAV) 系結，以改變 UAVs 圖形管線結果順序的一般需求。 這會啟用與順序無關的透明度 (OIT) 演算法可運作，如此一來，當多個透明物件在視野中彼此對齊時，就能提供更好的呈現結果。

-   [概觀](#overview)
-   [執行詳細資料](#implementation-details)
-   [API 摘要](#api-summary)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

標準圖形管線可能無法正確地將多個包含透明度的材質組合在一起。 網路圍牆、冒煙、火、植被指數和彩色玻璃等物件會使用透明效果來取得所需的效果。 如果多個包含透明度的材質 (在包含植被指數的半透明大樓前方的範圍前面，有多個材質出現問題，就會發生問題，例如) 。 依瀏覽器排序的視圖 (ROVs) 可讓基礎 OIT 演算法使用硬體的功能，以嘗試正確地解析透明度順序。 透明度是由圖元著色器所處理。

依瀏覽器排序的視圖 (ROVs) 允許圖元著色器程式碼將 UAV 系結標示為可改變 UAVs 圖形管線結果順序的一般需求。

ROVs 保證對重迭圖元著色器調用的 UAV 存取順序。 在此情況下，「重迭」表示叫用是由相同的繪製呼叫所產生，並且在圖元頻率執行模式中共用相同的圖元座標，並在取樣頻率模式中共用相同的圖元和樣本座標。

執行圖元著色器調用的重迭 ROV 存取順序，與提交幾何的順序相同。 這表示，針對重迭的圖元著色器調用，圖元著色器調用所執行的 ROV 寫入必須可供後續調用讀取，且不能影響先前調用的讀取。 圖元著色器調用所執行的 ROV 讀取必須反映先前調用的寫入，而且不得反映後續調用的寫入。 這對 UAVs 很重要，因為它們是明確地從輸出 invariance 保證中省略，通常是由圖形管線結果的固定順序來設定。

## <a name="implementation-details"></a>實作詳細資料

以 ROVs) 的瀏覽器排列檢視 (會使用下列新的高階著色器語言來宣告 (HLSL) 物件，且僅適用于圖元著色器：

-   `RasterizerOrderedBuffer`
-   `RasterizerOrderedByteAddressBuffer`
-   `RasterizerOrderedStructuredBuffer`
-   `RasterizerOrderedTexture1D`
-   `RasterizerOrderedTexture1DArray`
-   `RasterizerOrderedTexture2D`
-   `RasterizerOrderedTexture2DArray`
-   `RasterizerOrderedTexture3D`

使用這些物件的方式與其他 UAV 物件相同， (例如 `RWBuffer` 等 ) 。

## <a name="api-summary"></a>API summary

ROVs 是僅限 HLSL 的結構，可將不同的行為語義套用至 UAVs。 與 UAVs 相關的所有 Api 也都與 ROVs 相關。 請注意，下列方法、結構和 helper 類別都會參考轉譯器：

-   [**D3D12 \_轉譯器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) ：包含轉譯器描述的結構。
-   [**D3D12 \_特徵 \_ 資料 \_ D3D12 \_ 選項**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) ：包含布林值的結構，表示支援。
-   [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) ：存取支援功能的方法。
-   [**CD3DX12 \_轉譯器 \_ DESC**](cd3dx12-rasterizer-desc.md) ：用來建立轉譯器描述的協助程式類別。
-   [**D3D12 \_圖形 \_ 管線 \_ 狀態 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) ：包含管線狀態的結構。

## <a name="related-topics"></a>相關主題

* [保守的點陣化](conservative-rasterization.md)
* [轉譯](rendering.md)
* [HLSL 中的資源系結](resource-binding-in-hlsl.md)
* [著色器模型5。1](/windows/desktop/direct3dhlsl/shader-model-5-1)