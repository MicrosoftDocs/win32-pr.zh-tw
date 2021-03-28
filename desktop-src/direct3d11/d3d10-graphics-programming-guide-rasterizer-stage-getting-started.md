---
title: 使用轉譯器階段開始使用
description: 本節說明如何設定視口、剪刀矩形、轉譯器狀態和多取樣。
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- '取樣器、轉譯器狀態 (Direct3D 10) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95a15221f6fd4bd422e96c0686816afb35d4e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315214"
---
# <a name="getting-started-with-the-rasterizer-stage"></a>使用轉譯器階段開始使用

本節說明如何設定視口、剪刀矩形、轉譯器狀態和多取樣。

## <a name="set-the-viewport"></a>設定區

視口會將剪輯) 空間中 (的頂點位置對應到轉譯目標位置。 此步驟會將3D 位置調整成2D 空間。 轉譯目標的方向是指向下 Y 軸;這需要在視口縮放期間翻轉 Y 座標。 此外，x 和 y 值的 x 和 y 範圍 (範圍的 x 和 y) 值會根據下列公式進行調整，以符合各區大小：


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



教學課程1使用 [**D3D11 的 \_ 視口**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) 和呼叫 [**>id3d11devicecoNtext：： RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports)來建立640×480的區。


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



[區描述] 會指定區的大小、使用 *MinDepth* 和 *MaxDepth*) 的地圖深度至 (的範圍，以及區左上角的位置。 *MinDepth* 必須小於或等於 *MaxDepth*; *MinDepth* 和 *MaxDepth* 的範圍介於0.0 到1.0 （含）之間。 區通常會對應至轉譯目標，但不是必要的;此外，此區的大小或位置不一定要與轉譯目標相同。

您可以建立一個範圍的陣列，但只能將一個可套用至幾何著色器的基本輸出。 一次只能設定一個使用中的區。 管線會使用預設的區域 (和剪式矩形，下一節會在點陣化期間) 討論。 預設值一律是陣列中 (或剪下矩形) 的第一個視口。 若要在幾何著色器中執行每個基本的區選，請在 GS 輸出簽章宣告中的適當 GS 輸出元件上，指定 ViewportArrayIndex 語義。

可在任何時間系結至轉譯器階段的最大視口 (和剪式矩形) 數目是 16 (由 **D3D11 \_ 區 \_ 和 \_ \_ \_ \_ 每個 \_ 管線) 的 SCISSORRECT 物件計數** 所指定。

## <a name="set-the-scissor-rectangle"></a>設定剪式矩形

剪式矩形讓您有機會減少將傳送至輸出合併階段的圖元數目。 剪式矩形外的圖元會被捨棄。 剪式矩形的大小是以整數指定。 根據 [系統值語義](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)中的 *ViewportArrayIndex* ，只有一個剪式矩形 () 可以在點陣期間套用至三角形。

若要啟用剪式矩形，請使用 D3D11 轉譯器 [**\_ \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)中的 *ScissorEnable* 成員 () 。 預設的剪式矩形是空的矩形;也就是說，所有 rect 值都是0。 換句話說，如果您未設定剪式矩形，且已啟用剪下，則不會將任何圖元傳送到輸出合併階段。 最常見的設定是將剪式矩形初始化為視口的大小。

若要將剪式矩形的陣列設定至裝置，請使用 [**D3D11 \_ RECT**](d3d11-rect.md)呼叫 [**>id3d11devicecoNtext：： RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) 。


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



這個方法會採用兩個參數： (1) 陣列中的矩形數目， (2) 矩形的陣列。

管線會在點陣 (使用預設的剪式矩形索引，預設值為零大小的矩形，並已停用剪切) 。 若要覆寫此項，請 \_ 在 gs 輸出簽章宣告中指定 gs 輸出元件的 SV ViewportArrayIndex 語義。 這會造成 GS 階段將此 GS 輸出元件標示為系統產生的元件，並具備此語義。 轉譯器階段會辨識此語義，並使用它附加的參數做為剪式矩形索引，以存取剪式矩形的陣列。 別忘了，您可以在建立轉譯器物件之前，先啟用 [轉譯器描述] 中的 [ *ScissorEnable* ] 值，讓轉譯器階段使用您定義的剪矩形。

## <a name="set-rasterizer-state"></a>設定轉譯器狀態

從 Direct3D 10 開始，轉譯器的狀態會封裝在轉譯器的狀態物件中。 您最多可以建立4096個轉譯器狀態物件，然後藉由將控制碼傳遞給狀態物件，將其設定為裝置。

使用 [**ID3D11Device1：： CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) 從轉譯器描述建立轉譯器狀態物件 (參閱 D3D11 轉譯器 [**\_ \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) 。


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



這一組範例狀態的完成可能是最基本的轉譯器設定：

-   純色填滿模式
-   挑選出或移除臉部;假設基本物件的逆時針繞組順序
-   關閉深度偏差但啟用深度緩衝，並啟用剪式矩形
-   關閉取樣和線條消除鋸齒

此外，基本的轉譯器作業一律包含下列各項：將 (剪切至視圖的錐分割) 、透視圖和圖區尺規。 成功建立轉譯器狀態物件之後，請將它設定為裝置，如下所示：


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a>多重採樣

多級取樣會以較高的解析度來取樣影像的部分或所有元件， (接著將解析度縮小至原始解析度) ，以減少繪製多邊形邊緣所造成的最明顯鋸齒形式。 雖然取樣器需要子圖元範例，但新式 GPU 會執行多重取樣，以便每個圖元執行一次圖元著色器。 這可在效能 (特別是在 GPU 系結應用程式) 和消除最終影像的消除鋸齒之間提供可接受的取捨。

若要使用取樣，請在 [點陣化 [**描述**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)] 中設定 [啟用] 欄位、建立多重取樣轉譯目標，然後使用著色器讀取轉譯目標，將範例解析成單一圖元色彩，或呼叫 [**>id3d11devicecoNtext：： ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) ，以使用視訊卡來解析範例。 最常見的案例是繪製至一個或多個多重取樣轉譯目標。

交叉取樣與使用範例遮罩無關、已啟用 [Alpha 至涵蓋範圍](d3d10-graphics-programming-guide-blend-state.md) ，還是每個樣本) 一律執行的樣板作業 (。

深度測試會受到取樣的影響：

-   啟用取樣時，深度會依樣本插入，且深度/樣板測試會依樣本進行：所有傳遞範例的圖元著色器輸出色彩都是重複的。 如果圖元著色器輸出深度，則所有樣本的深度值都會重複 (雖然此案例失去了取樣) 的優點。
-   當您停用取樣時，深度/樣板測試仍會依樣本進行，但深度不會依樣本插補。

在單一轉譯目標內混用多重取樣和非多重取樣轉譯沒有任何限制。 如果您啟用取樣器並繪製至非多重取樣轉譯目標，則會產生與未啟用取樣器相同的結果;取樣的完成方式為每圖元一個樣本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯器階段](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 