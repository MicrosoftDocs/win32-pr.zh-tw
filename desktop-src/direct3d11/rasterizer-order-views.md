---
title: 轉譯器順序視圖
description: 以轉譯器排序的視圖 (ROVs) 允許圖元著色器程式碼將 UAV 系結標示為會改變 UAVs 圖形管線結果順序的一般需求。
ms.assetid: 7FCFCD28-E68D-4594-8879-937F57245507
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d891701aeaadd6f4474aeed8303d9b0046d1b656
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093040"
---
# <a name="rasterizer-order-views"></a>轉譯器順序視圖

以轉譯器排序的視圖 (ROVs) 允許圖元著色器程式碼將 UAV 系結標示為會改變 UAVs 圖形管線結果順序的一般需求。 這可讓您 (OIT) 演算法來運作，以提供更好的轉譯結果，當多個透明物件在視圖中彼此對齊時，可提供更好的呈現結果。

-   [概觀](#overview)
-   [執行詳細資料](#implementation-details)
-   [API 摘要](#api-summary)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

標準圖形管線可能無法正確地將多個包含透明度的材質組合在一起。 網路圍牆、冒煙、火、植被指數和彩色玻璃等物件會使用透明效果來取得所需的效果。 如果多個包含透明度的材質 (在包含植被指數的半透明大樓前方的範圍前面，有多個材質出現問題，就會發生問題，例如) 。 以轉譯器排序的視圖 (ROVs) 可讓基礎 OIT 演算法使用硬體的功能，以嘗試正確地解析透明度順序。 透明度是由圖元著色器所處理。

以轉譯器排序的視圖 (ROVs) 允許圖元著色器程式碼將 UAV 系結標示為會改變 UAVs 圖形管線結果順序的一般需求。

ROVs 保證對重迭圖元著色器調用的 UAV 存取順序。 在此情況下，「重迭」表示叫用是由相同的繪製呼叫所產生，並且在圖元頻率執行模式中共用相同的圖元座標，並在取樣頻率模式中共用相同的圖元和樣本座標。

執行圖元著色器調用的重迭 ROV 存取順序，與提交幾何的順序相同。 這表示，針對重迭的圖元著色器調用，圖元著色器調用所執行的 ROV 寫入必須可供後續調用讀取，且不能影響先前調用的讀取。 圖元著色器調用所執行的 ROV 讀取必須反映先前調用的寫入，而且不得反映後續調用的寫入。 這對 UAVs 很重要，因為它們是明確地從輸出 invariance 保證中省略，通常是由圖形管線結果的固定順序來設定。

## <a name="implementation-details"></a>實作詳細資料

 (ROVs) 的瀏覽器排序視圖會使用下列新的高階著色器語言來宣告 (HLSL) 物件，且僅適用于圖元著色器：

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

-   [**D3D11 \_轉譯器 \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) ：包含轉譯器描述的結構，請注意 CD3D12 轉譯 \_ \_ 器 DESC2 協助程式類別來建立轉譯器描述。
-   [**D3D11 \_FEATURE \_ DATA \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) ：包含布林值的結構 `ROVsSupported` ，表示支援。
-   [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) ：存取支援功能的方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11.3 功能](direct3d-11-3-features.md)
</dt> <dt>

[著色器模型5。1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 