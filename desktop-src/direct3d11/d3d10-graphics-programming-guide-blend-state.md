---
title: 設定混合功能
description: 在輸出值寫入轉譯目標之前，會對每個圖元著色器輸出 (RGBA 值) 執行混合作業。 如果啟用取樣，則會在每個執行程式上進行混合;否則，會在每個圖元上執行混色。
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990919"
---
# <a name="configuring-blending-functionality"></a>設定混合功能

在輸出值寫入轉譯目標之前，會對每個圖元著色器輸出 (RGBA 值) 執行混合作業。 如果啟用取樣，則會在每個執行程式上進行混合;否則，會在每個圖元上執行混色。

-   [建立 Blend 狀態](#create-the-blend-state)
-   [系結 Blend 狀態](#bind-the-blend-state)
-   [Advanced 混色主題](#advanced-blending-topics)
    -   [Alpha 到涵蓋範圍](#alpha-to-coverage)
    -   [混合圖元著色器輸出](#blending-pixel-shader-outputs)
-   [相關主題](#related-topics)

## <a name="create-the-blend-state"></a>建立 Blend 狀態

Blend 狀態是用來控制混合的狀態集合。 這些狀態 (定義于 [**D3D11 \_ blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) 用來藉由呼叫 [**ID3D11Device1：： CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1)來建立 BLEND 狀態物件。

例如，以下是一個非常簡單的 blend 狀態建立範例，可停用 Alpha 混合，而不會使用每個元件的圖元遮罩。


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



此範例類似于 [HLSLWithoutFX10 範例](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)。

## <a name="bind-the-blend-state"></a>系結 Blend 狀態

建立 blend 狀態物件之後，請呼叫 [**>id3d11devicecoNtext：： OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate)，將 blend 狀態物件系結至輸出合併階段。


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



此 API 採用三個參數： blend 物件、四個元件的 blend 因數，以及一個範例遮罩。 您可以針對 blend 狀態物件傳遞 **Null** ，以指定預設的 blend 狀態或傳入 blend 物件。 如果您使用 [**D3D11 \_ blend \_ Blend \_ 因數**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) 或 [**D3D11 blend 的 blend \_ \_ \_ \_ 因數**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend)來建立 blend 物件，您可以將 blend 因數傳遞給圖元著色器、轉譯目標或兩者的 lambert 值。 如果您未使用 **D3D11 \_ blend \_ Blend \_ 因數** 或 **D3D11 blend 的 blend \_ \_ \_ \_ 因數** 來建立 blend 物件，您仍然可以傳遞非 Null 的 blend 因數，但是混合階段不會使用 blend 因數; 執行時間會儲存 blend 因數，您稍後可以呼叫 [**>id3d11devicecoNtext：： OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) 來取得 blend 係數。 如果您傳遞 **Null**，則執行時間會使用或儲存相當於 {1，1，1，1} 的 blend 係數。 範例遮罩是使用者定義的遮罩，可決定如何在更新現有的轉譯目標之前對其進行取樣。 預設的取樣遮罩是指定點取樣的0xffffffff。

在最深度的緩衝配置中，最接近相機的圖元是繪製的圖元。 [設定深度樣板狀態](d3d10-graphics-programming-guide-depth-stencil.md)時， [**D3D11 深度樣板 \_ \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)的 **DepthFunc** 成員可以是任何 [**D3D11 的 \_ 比較 \_ FUNC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func)。 一般來說，您會想要讓 **DepthFunc** 的 **D3D11 \_ 比較比較 \_ 少**，因此最接近相機的圖元會覆寫其後的圖元。 不過，視您的應用程式需求而定，您可以使用任何其他的比較函數來進行深度測試。

## <a name="advanced-blending-topics"></a>Advanced 混色主題

-   [Alpha 到涵蓋範圍](#alpha-to-coverage)
-   [混合圖元著色器輸出](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a>Alpha 到涵蓋範圍

「Alpha 到涵蓋範圍」是一種對等情況最有用的多層式技術，例如密集 foliage，其中有數個重迭的多邊形會使用 Alpha 透明度來定義介面內的邊緣。

您可以使用 [**D3D11 \_ BLEND \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)或 [**D3D11 \_ blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)的 **AlphaToCoverageEnable** 成員，來切換執行時間是否會將輸出暫存器 (Alpha) 的元件，[從 \_](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)圖元著色器轉換成 n 步驟涵蓋範圍遮罩 (提供了 n 個範例 **RenderTarget**) 。 執行時間除了範例遮罩之外，也會使用基本 (中圖元的一般樣本涵蓋範圍來執行 **和作業，**) 判斷要在所有使用中的 **RenderTarget** 中更新的範例。

如果圖元著色器輸出 [SV \_ 涵蓋範圍](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)，則執行時間會停用 Alpha 至涵蓋範圍。

> [!Note]  
> 在取樣中，執行時間只會共用所有 **RenderTarget** 的一個涵蓋範圍。 執行時間讀取和轉換的事實。當 **AlphaToCoverageEnable** 為 TRUE 時，從輸出 [SV \_ 目標](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 到涵蓋範圍的事實不會變更。如果 **RenderTarget** 發生在) 中，則會在 **RenderTarget** 0 時移至 blender 的值 (。 一般情況下，如果您啟用 Alpha 至涵蓋範圍，就不會影響圖元著色器的所有色彩輸出如何透過 [輸出合併階段](d3d10-graphics-programming-guide-output-merger-stage.md)與 **RenderTarget** 互動，不同之處在于執行時間會使用 Alpha 對涵蓋範圍遮罩來執行涵蓋範圍遮罩的 **和** 作業。 Alpha 到涵蓋範圍適用于執行時間是否可以 blend **RenderTarget** 或您是否在 **RenderTarget** 上使用 blend。

 

圖形硬體無法精確地指定其轉換圖元著色器 [SV \_ 目標](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 的方式。 (Alpha) 至涵蓋範圍遮罩，但 0 (或較少的) 必須對應至不 (的涵蓋範圍，且小於 1) 或更高的必須對應到完整的涵蓋範圍， (在執行時間使用實際的基本涵蓋範圍) 來執行 **和** 作業之前，必須先 當 Alpha 從0變成1時，產生的涵蓋範圍通常會以單純的方式增加。 不過，硬體可能會執列區域遞色，以提供更好的 Alpha 值量化，代價是空間解析度和雜訊的成本。 NaN 的 Alpha 值 (不是數位) 會導致 (零) mask 沒有涵蓋範圍。

Alpha 到涵蓋範圍也是傳統上用來進行螢幕畫面的透明度或定義詳細的 silhouettes，否則不透明的 sprite。

### <a name="blending-pixel-shader-outputs"></a>混合圖元著色器輸出

這項功能可讓輸出合併同時使用圖元著色器輸出，做為混合作業的輸入來源與位置0的單一轉譯目標。

這個範例會採用兩個結果，並將它們結合在單一行程中，然後將一個乘到目的地，並使用另一個來加上：


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



這個範例會將第一個圖元著色器輸出設定為來源色彩，並將第二個輸出設定為每個色彩元件 blend 係數。


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



此範例說明 blend 因數必須與著色器 swizzles 相符的方式：


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



Blend 因數和著色器程式碼會一起表示需要圖元著色器，才可輸出至少 o0 r 和 o1. a。 著色器可以輸出額外的輸出元件，但會忽略，而較少的元件會產生未定義的結果。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[輸出合併階段](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[ (Direct3D 10) 的管線階段 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 