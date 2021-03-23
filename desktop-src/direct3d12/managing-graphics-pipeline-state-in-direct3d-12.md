---
title: 管理 Direct3D 12 中的圖形管線狀態
description: 本主題說明如何在 Direct3D 12 中設定圖形管線狀態。
ms.assetid: AAF97BD2-D532-469D-9242-CC94C06727C3
keywords:
- 管線狀態
- 管線狀態物件
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7564b5863d3efebdf8a335e2c46945aeebea93e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548473"
---
# <a name="managing-graphics-pipeline-state-in-direct3d-12"></a>管理 Direct3D 12 中的圖形管線狀態

本主題說明如何在 Direct3D 12 中設定圖形管線狀態。

## <a name="pipeline-state-overview"></a>管線狀態總覽

當幾何提交給圖形處理單元時 (要繪製的 GPU) ，有各種不同的硬體設定可決定如何轉譯和轉譯輸入資料。 這些設定統稱為圖形管線狀態，並包含一般設定，例如，轉譯器狀態、blend 狀態和深度樣板狀態，以及所提交幾何的基本拓撲類型，以及將用於轉譯的著色器。 在 Microsoft Direct3D 12 中，大部分的圖形管線狀態都是使用管線狀態物件 (PSO) 來設定。 應用程式可以建立不限數目的這些物件，這些物件是由 [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) 介面所代表，通常是在初始化時。 然後，在轉譯時期，命令清單可以藉由在直接命令清單或組合中呼叫 [**ID3D12GraphicsCommandList：： SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate) ，快速切換管線狀態的多個設定，以設定使用中的 PSO。

在 Direct3D 11 中，圖形管線狀態已配套至大型、粗略的狀態物件（例如 [**ID3D11BlendState**](/windows/win32/api/d3d11/nn-d3d11-id3d11blendstate) ），可以在即時內容中使用 [**>id3d11devicecoNtext：： OMSetBlendState**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-omsetblendstate)這類方法來建立和設定。 這種情況的概念是，GPU 可以藉由設定相關設定（如 blend 狀態設定）來提高效率。 不過，在現今的圖形硬體中，不同的硬體單元之間有相依性。 例如，硬體 blend 狀態可能會相依于點陣狀態和 blend 狀態。 Direct3D 12 中的 Pso 是設計來讓 GPU 在每個管線狀態（通常是在初始化期間）預先處理所有相依的設定，以盡可能有效率地在轉譯時期切換狀態。

請注意，雖然大部分的管線狀態設定都是使用 Pso 來設定，但仍有一些狀態設定會使用 [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)所提供的 api 分開設定。 以下將詳細討論這些設定和相關聯的 Api。 此外，從直接命令清單和組合保存圖形管線狀態的方式也有差異。 本主題提供下列兩者的詳細資料。

## <a name="graphics-pipeline-states-set-with-pipeline-state-objects"></a>使用管線狀態物件設定的圖形管線狀態

若要查看可使用管線狀態物件來設定的各種不同管線狀態，最簡單的方式就是查看 [**D3D12 \_ 圖形 \_ 管線 \_ 狀態 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) 的參考主題，以在初始化物件時傳遞給 [**ID3D12Device：： CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) 。 可設定狀態的快速摘要包括：

-   所有著色器的位元組程式碼，包括、頂點、圖元、定義域、輪廓和幾何著色器。
-   輸入頂點格式。
-   基本拓撲類型。 請注意，輸入組合語言基本拓撲類型 (點、線條、三角形、patch) 是在 PSO 中使用 [**D3D12 \_ 基本 \_ 拓撲 \_ 類型**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) 列舉來設定。 使用 [**ID3D12GraphicsCommandList：： IASetPrimitiveTopology**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology) 方法從命令清單中設定基本的相鄰和排序 (行清單、行條紋、具有相鄰資料的行帶等 ) 。
-   Blend 狀態、光柵器狀態、深度樣板狀態。
-   深度樣板和轉譯目標格式，以及呈現目標計數。
-   多取樣參數。
-   串流輸出緩衝區。
-   根簽章。 如需詳細資訊，請參閱 [根](root-signatures.md)簽章。

## <a name="graphics-pipeline-states-set-outside-of-the-pipeline-state-object"></a>在管線狀態物件外設定的圖形管線狀態

大部分的圖形管線狀態都是使用 Pso 來設定。 不過，有一組管線狀態參數是藉由從命令清單中呼叫 [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面的方法所設定。 下表顯示以這種方式設定的狀態和對應的方法。

|狀態|方法|
|-|-|
|資源系結|[**IASetIndexBuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)<br/>[**IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)<br/>[**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)<br/>[**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)<br/>[**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)<br/>所有 **SetGraphicsRoot ...** 方法<br/>所有 **SetComputeRoot ...** 方法<br/>
|區|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports">**RSSetViewports**</a>|
|剪式矩形|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects">**RSSetScissorRects**</a>|
|Blend 因數|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetblendfactor">**OMSetBlendFactor**</a>|
|深度樣板參考值|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref">**OMSetStencilRef**</a>|
|輸入組合語言基本拓撲順序和相鄰類型|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology">**IASetPrimitiveTopology**</a>|

## <a name="graphics-pipeline-state-inheritance"></a>圖形管線狀態繼承

因為直接命令清單通常是要一次用於一次，且套件組合應同時使用多次，所以它們如何繼承先前命令清單或組合所設定的圖形管線狀態，會有不同的規則。

針對使用 Pso 設定的圖形管線狀態，直接命令清單或組合都不會繼承這些狀態。 直接命令清單和組合的初始圖形管線狀態，會在建立時設定，並將 [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) 參數設定為 [**ID3D12Device：： CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)。 如果未在呼叫中指定 PSO，則會使用預設的初始狀態。 您可以藉由呼叫 [**ID3D12GraphicsCommandList：： SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)，來變更命令清單中的目前 PSO。

直接命令清單也不會繼承以命令清單方法（例如 [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)）設定的狀態。 如需非 PSO 狀態之預設初始值的詳細資訊，請參閱 [**ID3D12GraphicsCommandList：： ClearState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)。

組合會繼承未使用 Pso 設定的所有圖形管線狀態，但基本拓撲類型除外。 當配套開始執行時，基本拓撲一律會設定為 [**\_ \_ \_ \_ 未定義的 D3D12 基本拓撲類型**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) 。 在組合內設定的任何狀態 (PSO 本身、非 PSO 狀態和資源系結) 會影響其父直接命令清單的狀態。 例如，如果從組合內呼叫 [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports) ，則會繼續在父直接命令清單中設定指定的的檢視器，以便在設定檢視器的 [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) 呼叫之後呼叫。

在命令清單或組合內設定的資源系結會持續存在。 因此，直接命令清單中修改的資源系結仍會在後續的子系組合執行內進行設定。 從組合內修改的資源系結仍會針對父直接命令清單中的後續呼叫進行設定。

如需系結的詳細資訊，請參閱 [使用根](using-a-root-signature.md)簽章的組合 **語義** 一節。

## <a name="related-topics"></a>相關主題

* [在 Direct3D 12 中提交工作](command-queues-and-command-lists.md)