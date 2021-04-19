---
description: 在 Direct3D 10 中，裝置狀態會分組為狀態物件，以大幅降低狀態變更的成本。
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: " (Direct3D 10) 的狀態物件"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a06e8603361a83049440774cfd2e12b4148b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970525"
---
# <a name="state-objects-direct3d-10"></a> (Direct3D 10) 的狀態物件

在 Direct3D 10 中，裝置狀態會分組為狀態物件，以大幅降低狀態變更的成本。 有幾個狀態物件，每個設計成針對特定管線階段初始化一組狀態。 您最多可以為每種類型的狀態物件建立4096。

-   [輸入-版面配置狀態](#input-layout-state)
-   [轉譯器狀態](#rasterizer-state)
-   [深度樣板狀態](#depth-stencil-state)
-   [Blend 狀態](#blend-state)
-   [取樣器狀態](#sampler-state)
-   [效能考量](#performance-considerations)
-   [相關主題](#related-topics)

## <a name="input-layout-state"></a>輸入配置狀態

這一組狀態 (請參閱 [**D3D10 \_ 輸入 \_ 元素 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) 指定輸入組合語言 [階段](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) 如何從輸入緩衝區讀取資料，並將它組合供端點著色器使用。 這包括狀態，例如輸入緩衝區中的元素數目和輸入資料簽章。 輸入組譯工具階段是管線中的新階段，其工作是將記憶體中的基本串流串流至管線。

若要建立輸入版面配置狀態物件，請參閱 [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)。

## <a name="rasterizer-state"></a>轉譯器狀態

此狀態群組 (查看 D3D10 轉譯器 [**\_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) 初始化轉譯器 [階段](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md)。 此物件包含填滿或揀選 (Cull) 模式、啟用剪式矩形裁剪和設定多重樣本參數等狀態。 這個階段會將基本類型點陣化成像素，執行像是裁剪及對應基本類型到檢視區等作業。

若要建立轉譯器狀態物件，請參閱 [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate)。

## <a name="depth-stencil-state"></a>深度樣板狀態

此狀態群組 (查看 [**D3D10 \_ 深度樣板 \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) 初始化 [輸出合併階段](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)的深度樣板部分。 更具體而言，這個物件初始化深度和樣板測試。

若要建立深度範本狀態物件，請參閱 [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate)。

## <a name="blend-state"></a>混色狀態

這一組狀態 (請參閱 [**D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) 初始化 [輸出合併階段](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)的混合部分。

若要建立 blend 狀態物件，請參閱 [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate)。

## <a name="sampler-state"></a>取樣器狀態

這一組狀態 (請參閱 [**D3D10 \_ 取樣器 \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) 初始化取樣器物件。 著色器階段使用取樣器物件，以篩選記憶體中的紋理。



|                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Direct3D 9 與 Direct3D 10 之間的差異：<br/> 在 Direct3D 10 中，取樣器物件不再系結至特定材質-它只會說明如何針對任何附加的資源進行篩選。 |



 

若要建立取樣器狀態物件，請參閱 [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate)。

## <a name="performance-considerations"></a>效能考量

設計 API 以使用狀態物件，會建立許多效能優點。 其中包括在物件建立時驗證狀態，在硬體啟用狀態物件快取，並大幅降低狀態設定 API 呼叫期間傳遞的狀態數量（傳遞狀態物件的控制代碼，而不是狀態）。

若要達成這些效能改進，您應該在應用程式啟動時，在轉譯迴圈之前，建立狀態物件。 狀態物件是不變，也就是狀態物件建立之後便無法變更。 相反地，您必須終結並重新建立它們。 若要解決這項限制，您最多可以為每種類型的狀態物件建立4096。 例如，您可以使用各種取樣器狀態組合來建立數個取樣器物件。 然後，藉由呼叫適當的 Set API （將控制碼傳遞給物件 (而不是取樣器狀態) ）來變更取樣器狀態。 這大幅降低變更狀態的每個轉譯畫面期間的額外負荷數量，因為呼叫數目和資料量已大幅降低。

或者，您可以選擇使用效果系統，為您的應用程式自動管理狀態物件的有效建立和解構。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (Direct3D 10) 的 API 功能 ](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
