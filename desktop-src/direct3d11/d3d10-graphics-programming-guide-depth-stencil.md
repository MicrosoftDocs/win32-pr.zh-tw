---
title: 設定 Depth-Stencil 功能
description: 本章節涵蓋的步驟，內容為設定深度樣板緩衝區及輸出合併階段的深度樣板狀態。
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682718"
---
# <a name="configuring-depth-stencil-functionality"></a>設定 Depth-Stencil 功能

本章節涵蓋的步驟，內容為設定深度樣板緩衝區及輸出合併階段的深度樣板狀態。

-   [建立 Depth-Stencil 資源](#create-a-depth-stencil-resource)
-   [建立 Depth-Stencil 狀態](#create-depth-stencil-state)
-   [將 Depth-Stencil 資料系結至 OM 階段](#bind-depth-stencil-data-to-the-om-stage)

待您了解如何使用深度樣板緩衝區及其對應的深度樣板狀態之後，請參閱[進階樣板技術](#advanced-stencil-techniques)。

## <a name="create-a-depth-stencil-resource"></a>建立 Depth-Stencil 資源

使用材質資源建立深度樣板緩衝區。


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a>建立深度樣板狀態

深度樣板狀態會告訴輸出合併階段如何執行[深度樣板測試](d3d10-graphics-programming-guide-output-merger-stage.md)。 深度樣板測試決定是否要繪製給定的像素。


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



DepthEnable 和 StencilEnable 可啟用 (並停用) 深度和樣板測試。 將 DepthEnable 設定為 **FALSE** 以停用深度測試，並防止寫入深度緩衝區。 將 StencilEnable 設定為 **false** 以停用樣板測試，並防止寫入至樣板緩衝區 (當 DepthEnable 為 **FALSE** 且 StencilEnable 為 **TRUE** 時，深度測試一律會在樣板作業) 中傳遞。

DepthEnable 只會影響輸出合併階段-在資料輸入至圖元著色器之前，不會影響剪切、深度偏差或值的固定。

## <a name="bind-depth-stencil-data-to-the-om-stage"></a>將深度樣板資料繫結至輸出合併階段

繫結深度樣板狀態。


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



使用檢視繫結深度樣板資源。


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



轉譯目標視圖的陣列可傳遞至 [**>id3d11devicecoNtext：： OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets)，不過所有的呈現目標視圖都將對應至單一深度樣板視圖。 Direct3D 11 中的轉譯目標陣列是一項功能，可讓應用程式在基本層級同時轉譯成多個呈現目標。 轉譯目標陣列可讓您以多個 **>id3d11devicecoNtext：： OMSetRenderTargets** 呼叫來個別設定轉譯目標，以提供更高的效能， (基本上是 Direct3D 9) 中所採用的方法。

轉譯目標必須全部都是相同的資源類型。 若要使用多重採樣消除鋸齒，所有已繫結的轉譯目標及深度緩衝區都必須要有相同的樣本數量。

當緩衝區作為轉譯目標使用時，則不支援深度樣板測試和多重轉譯目標。

-   最多可以同時繫結 8 個轉譯目標。
-   所有的呈現目標在所有維度中都必須具有相同的大小 (寬度和高度，以及 \*) 陣列類型的3d 或陣列大小的深度。
-   各個轉譯目標可能會有不同的資料格式。
-   寫入遮罩可用來控制將寫入轉譯目標的資料。 輸出寫入遮罩可根據每個轉譯目標及每個元件，控制將寫入轉譯目標的資料。

## <a name="advanced-stencil-techniques"></a>進階樣板技術

深度樣板緩衝區的樣板部分可用於建立轉譯效果，例如：合成、印花，以及外框。

-   [合成](#compositing)
-   [Decaling](#decaling)
-   [大綱和 Silhouettes](#outlines-and-silhouettes)
-   [雙側範本](#two-sided-stencil)
-   [以材質的形式讀取 Depth-Stencil 緩衝區](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a>合成

您的應用程式可利用樣板緩衝區將 2D 或 3D 影像合成為 3D 場景。 樣板緩衝區中的遮罩可用於遮蔽轉譯目標的部分表面區域。 儲存的 2D 資訊 (例如文字或點陣圖) 接著便可寫入遮蔽區域。 或者，您的應用程式也可將其他 3D 原始物件轉譯至轉譯目標表面的樣板遮蔽區域。 甚至可以轉譯整個場景。

通常，遊戲會將多個 3D 場景合成在一起。 例如：競速遊戲通常都會顯示後照鏡。 後照鏡便包含了駕駛後方的 3D 場景。 該檢視基本上就是合成於駕駛前方檢視的第二個 3D 場景。

### <a name="decaling"></a>印花

Direct3D 應用程式使用印花來控制從特定原始影像繪製到轉譯目標表面上的像素。 應用程式將印花套用至原始物件的影像，以正確地轉譯共面多邊形。

例如：將輪胎標記及黃線畫上道路之後，標記應該要直接出現在道路上方。 但是，標記和道路的 z 值是相同的。 因此，深度緩衝區不一定會在這兩者之間正常分離。 某些後方原始物件的像素可能會轉譯至前方原始物件的上方，反之亦然。 產生的影像似乎在影格間不斷閃爍。 此效果稱為「z 衝突」或「影格閃爍」。

若要解決這個問題，可使用樣板將後方原始物件上印花出現的區域遮蔽。 關閉 z 緩衝，並將前方原始物件的影像轉譯至轉譯目標表面上已被遮蔽的區域。

多重紋理混合可用於解決此問題。

### <a name="outlines-and-silhouettes"></a>外框及剪影

您可以利用樣板緩衝區以獲得更抽象的效果，例如：外框及剪影。

如果您的應用程式進行了二階段的轉譯 (第一階段產生樣板遮罩，並於第二階段在原始物件稍微變小之後，將樣板遮罩套用至影像)，產生的影像可能只會包含原始物件的外框。 應用程式可以再以單色填滿影像中被樣板遮蔽的區域，給予原始物件浮凸的外觀。

如果樣板遮罩的大小及形狀與您正在轉譯的原始物件相同，產出的影像將會在原先原始物件所在的位置留下一個洞。 您的應用程式可以再以黑色填滿該空洞，產生原始物件的剪影效果。

### <a name="two-sided-stencil"></a>雙面樣板

利用樣板緩衝區繪製陰影時將會使用到陰影錐。 應用程式透過計算剪影的邊緣，將其往光源的反方向突出並形成一組 3D 體積的集合，進而計算遮蔽幾何物的陰影錐。 這些物體接著會在經過兩次的轉譯之後寫入樣板緩衝區。

第一次轉譯會繪製面向前端的多邊形，並遞增樣板緩衝區的值。 第二次轉譯會繪製陰影錐面向後端的多邊形，並遞減樣板緩衝區的值。 一般而言，所有遞增及遞減的值會互相抵銷。不過，當陰影錐被轉譯時，場景已經在一般幾何導致某些像素無法通過 z 衝突測試時轉譯完成。 留在樣板緩衝區的值將會對應到陰影中的像素。 這些剩餘的樣板緩衝區內容會作為遮罩使用，以將一個包括所有內容的巨大黑色四元組 Alpha 混合至場景中。 藉由將樣板緩衝區作為遮罩，陰影中的像素將會進一步加深。

這表示針對每個光源，陰影幾何都會繪製兩次，因此對 GPU 的頂點輸送量形成了壓力。 雙面樣板便是為了避免這種情況而設計出來的功能。 在這種方法之下，會有兩組樣板狀態 (命名如下)：其中一組為針對每個面向前端的三角形設定的樣板狀態，另外一組則是針對面向後端的三角形。 如此一來，針對每個光源及每個陰影錐都只會進行一階段的繪製。

您可以在 [ShadowVolume10 範例](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx)中找到兩個邊樣板執行的範例。

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a>讀取深度樣板緩衝區作為紋理

非使用中的深度樣板緩衝區可由著色器作為紋理讀取。 讀取深度樣板緩衝區作為紋理的應用程式，將會進行二階段的轉譯：在第一階段寫入深度樣板緩衝區，並於第二階段從緩衝區中讀取。 這可以讓著色器將先前寫入緩衝區的深度值或樣板值，與目前轉譯中像素的值互相比較。 比較的結果可用來建立效果，例如陰影貼圖或粒子系統中的軟粒子。

若要建立可做為深度樣板資源和著色器資源的深度樣板緩衝區，必須對 [ [建立 Depth-Stencil 資源](#create-a-depth-stencil-resource) ] 區段中的範例程式碼進行一些變更。

-   深度樣板資源必須有不具格式的格式，例如 DXGI \_ 格式 R32 無型別 \_ \_ 。
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   深度樣板資源必須同時使用 D3D10 系結 \_ 深度樣板 \_ 和 D3D10 系結 \_ \_ \_ 著色器資源系結 \_ 旗標。
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

此外，您必須使用 [**D3D11 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) 結構和 [**ID3D11Device：： CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)，為深度緩衝區建立著色器資源檢視。 著色器資源檢視會使用具類型的格式，例如 **DXGI \_ 格式 \_ R32 \_ FLOAT** ，這相當於建立深度樣板資源時所指定的無類型格式。

在第一次轉譯階段中，深度緩衝區系結，如將 [Depth-Stencil 資料系結至 OM 階段](#bind-depth-stencil-data-to-the-om-stage) 一節中所述。 請注意，傳遞至 [**D3D11 \_ 深度樣板 \_ \_ 視圖 \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)的格式。格式會使用具類型的格式，例如 **DXGI \_ 格式 \_ D32 \_ FLOAT**。 第一次轉譯階段之後，深度緩衝區將包含場景的深度值。

在第二個轉譯階段中， [**>id3d11devicecoNtext：： OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) 函式是用來將深度樣板視圖設定為 **Null** 或不同的深度樣板資源，而著色器資源檢視會使用 [**ID3D11EffectShaderResourceVariable：： SetResource**](id3dx11effectshaderresourcevariable-setresource.md)傳遞給著色器。 這可讓著色器查詢第一次轉譯行程中計算出的深度值。 請注意，如果第一次轉譯傳遞的觀點與第二個轉譯行程不同，則必須套用轉換來取得深度值。 例如，如果使用陰影對應技術，則第一次轉譯階段會從光源的角度來看，而第二次轉譯階段則是從檢視器的觀點來看。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[輸出合併階段](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[ (Direct3D 10) 的管線階段 ](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 