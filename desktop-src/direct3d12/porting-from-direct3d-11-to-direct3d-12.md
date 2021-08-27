---
title: 從 Direct3D 11 移植到 Direct3D 12
description: 本節提供從自訂 Direct3D 11 圖形引擎移植到 Direct3D 12 的一些指引。
ms.assetid: 9EB4AC6B-AFDD-4673-8EB3-54272C151784
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ccf4a0bd10032d94ecaf4a88cc442f3a7ad516
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812561"
---
# <a name="porting-from-direct3d-11-to-direct3d-12"></a>從 Direct3D 11 移植到 Direct3D 12

本節提供從自訂 Direct3D 11 圖形引擎移植到 Direct3D 12 的一些指引。

-   [裝置建立](#device-creation)
-   [認可的資源](#committed-resources)
-   [保留的資源](#reserved-resources)
-   [上傳資料](#uploading-data)
-   [著色器和著色器物件](#shaders-and-shader-objects)
-   [將工作提交至 GPU](#submitting-work-to-the-gpu)
-   [CPU/GPU 同步處理](#cpugpu-synchronization)
-   [資源系結](#resource-binding)
-   [資源狀態](#resource-state)
-   [Swapchains](#swapchains)
-   [修正函式轉譯](#fixed-function-rendering)
-   [機率和結束](#odds-and-ends)
-   [相關主題](#related-topics)

## <a name="device-creation"></a>裝置建立

Direct3D 11 和 Direct3D 12 都共用類似的裝置建立模式。 現有的 Direct3D 12 驅動程式全都 **D3D_FEATURE_LEVEL_11_0** 或更好，因此您可以忽略較舊的功能層級和相關聯的限制。

也請記住，使用 Direct3D 12 時，您應該使用 DXGI 介面明確地列舉裝置資訊。 在 Direct3D 11 中，您可以從 Direct3D 裝置 *串連回* DXGI 裝置，但不支援 direct3d 12。

您可以藉由提供從 **IDXGIFactory4：： EnumWarpAdapter** 取得的明確介面卡，來建立 Direct3D 12 上的變形 software 裝置。 Direct3D 12 的變形裝置只適用于已啟用 [ **圖形工具** ] 選用功能的系統。

> [!NOTE]
> 沒有對等的 **D3D11CreateDeviceAndSwapChain**。 即使使用 Direct3D 11，我們也不鼓勵使用此函式，因為通常最好是在不同的步驟中建立裝置和 swapchain。

## <a name="committed-resources"></a>認可的資源

使用 Direct3D 11 中的下列介面所建立的物件，會轉譯為 Direct3D 12 中所謂的「認可的資源」。 認可的資源是具有虛擬位址空間和相關聯之實體頁面的資源。 這是以 Direct3D 12 為基礎之 Microsoft Windows 設備磁碟機 2 (WDD2) 記憶體模型的概念。

Direct3D 11 資源：

-   [**ID3D11Resource**](/windows/win32/api/d3d11/nn-d3d11-id3d11resource)
-   [**ID3D11Buffer**](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer)和 [ **ID3D11Device：： CreateBuffer**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createbuffer)
-   [**ID3D11Texture1D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture1d)和 [ **ID3D11Device： CreateTexture1D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture1d)
-   [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d)和 [ **ID3D11Device：： CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d)
-   [**ID3D11Texture3D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture3d)和 [ **ID3D11Device：： CreateTexture3D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture3d)

在 Direct3D 12 中，這些全都以 [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) 和 [**ID3D12Device：： CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)表示。

## <a name="reserved-resources"></a>保留的資源

保留的資源是只配置虛擬位址空間的資源，在呼叫 [**ID3D12Device：： CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap)之前，不會配置實體記憶體。 這基本上與 Direct3D 11 中的磚資源概念相同。

旗標 ([**D3D11 \_ 資源 \_ 其他 \_ 旗**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) 標) 在 Direct3D 11 中用來設定並排的資源，然後將它們對應到實體記憶體。

-   D3D11 \_ 資源 \_ 其他 \_ 磚
-   D3D11 \_ 資源 \_ 其他 \_ 磚 \_ 集區

## <a name="uploading-data"></a>上傳資料

在 Direct3D 11 中，單一時間軸的外觀 (在序列之後進行呼叫，例如使用 [**D3D11 \_ SUBRESOURCE \_ 資料**](/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data)初始化的資料，然後呼叫 [**>id3d11devicecoNtext：： UpdateSubresource**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource)，然後呼叫 [**>id3d11devicecoNtext：： Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) 。 對 Direct3D 11 開發人員而言，資料建立的複本數目並不明顯。

在 Direct3D 12 中有兩個時間軸，GPU 時間軸 (透過呼叫 [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)來設定，並從可對應記憶體) 和 CPU 時間軸進行 [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) ， (由呼叫來 [**對應**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)) 。 Helper 函式 (在 d3dx12 .h 檔案中提供，) 稱為使用共用時間軸的 [**Updatesubresources**](updatesubresources1.md) 。 此 helper 函式有數種變化，一個使用 [**ID3D12Device：： GetCopyableFootprints**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)，另一個使用堆積配置機制，另一個則使用堆疊配置機制。 這些 helper 函式會透過記憶體的中繼臨時區域，將資源複製到 GPU 和 CPU。

一般來說，GPU 和 CPU 都有自己的資源複本，並系結至自己的時間軸。 共用的時間軸方法同樣會維護兩份複本。

## <a name="shaders-and-shader-objects"></a>著色器和著色器物件

在 Direct3D 11 中，有許多著色器和狀態物件的建立，並使用 [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) 建立方法和 [**>id3d11devicecoNtext**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) set 方法來設定這些物件的狀態。 通常會對這些方法進行大量呼叫，然後由驅動程式在繪製時間合併，以設定正確的管線狀態。

在 Direct3D 12 中，管線狀態的這項設定已合併為單一物件 (計算引擎的 [**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) ，而圖形引擎的 CreateGraphicsPipelineState 則是圖形) 引擎的 [](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) ，接著會在使用 [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)的呼叫之前附加至命令清單。

在 Direct3D 11 中，這些呼叫會取代所有個別的呼叫，以設定著色器、輸入配置、blend 狀態、轉譯器狀態、深度樣板狀態等等。

- 裝置11方法： ``CreateInputLayout`` 、 ``CreateXShader`` 、 ``CreateDepthStencilState`` 、andD ``CreateRasterizerState`` 。
- 裝置內容11方法：  ``IASetInputLayout`` 、 ``xxSetShader`` 、 ``OMSetBlendState`` 、 ``OMSetDepthStencilState`` 和 ``RSSetState`` 。

雖然 Direct3D 12 可以支援較舊的編譯著色器 blob，但是著色器應該使用著色器模型5.1 搭配 FXC.EXE/D3DCompile Api，或使用著色器模型6（使用 DXIL DXC 編譯器）來建立。 您應使用 [**CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) 和 **D3D12_FEATURE_SHADER_MODEL** 來驗證著色器模型6支援。

## <a name="submitting-work-to-the-gpu"></a>將工作提交至 GPU

在 Direct3D 11 中，實際上不會控制提交工作的方式，而是由驅動程式來處理，但透過 [**>id3d11devicecoNtext：： Flush**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-flush) 和 [**IDXGISwapChain1：:P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) 呼叫來啟用某些控制項。

在 Direct3D 12 中，工作提交非常明確，而且是由應用程式所控制。 提交工作的主要結構是用來記錄所有應用程式命令 (的 [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)，在概念上與 ID3D11 延後的內容) 很類似。 命令清單的備份存放區是由 [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)所提供，可讓應用程式藉由實際公開 Direct3D 12 驅動程式即將用來儲存命令清單的記憶體，來管理命令清單的記憶體使用量。

最後， [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) 是先進先出佇列，可儲存命令清單的正確順序，以提交給 GPU。 只有當某個命令清單在 GPU 上已完成執行時，驅動程式才會提交佇列中的下一個命令清單。

在 Direct3D 11 中，命令佇列沒有明確的概念。 在 Direct3D 12 的一般設定中，目前的框架目前開啟的 **D3D12_COMMAND_LIST_TYPE_DIRECT** 命令清單，可視為與 Direct3D 11 立即內容類別似。 這提供許多相同的功能。


| D3D11DeviceCoNtext                  | ID3D12GraphicsCommand 清單     |
|-------------------------------------|--------------------------------|
| ClearDepthStencilView               | ClearDepthStencilView          |
| ClearRenderTargetView               | ClearRenderTargetView          |
| ClearUnorderedAccess*               | ClearUnorderedAccess*          |
| Draw、DrawInstanced                 | DrawInstanced                  |
| DrawIndexed、DrawIndexedInstanced   | DrawIndexedInstanced           |
| 分派                            | 分派                       |
| IASetInputLayout、xxSetShader 等。 | SetPipelineState               |
| OMSetBlendState                     | OMSetBlendFactor               |
| OMSetDepthStencilState              | OMSetStencilRef                |
| OMSetRenderTargets                  | OMSetRenderTargets             |
| RSSetViewports                      | RSSetViewports                 |
| RSSetScissorRects                   | RSSetScissorRects              |
| IASetPrimitiveTopology              | IASetPrimitiveTopology         |
| IASetVertexBuffers                  | IASetVertexBuffers             |
| IASetIndexBuffer                    | IASetIndexBuffer               |
| ResolveSubresource                  | ResolveSubresource             |
| CopySubresourceRegion               | CopyBufferRegion               |
| UpdateSubresource                   | CopyTextureRegion              |
| CopyResource                        | CopyResource                   |

> [!NOTE]
> 使用 **D3D12_COMMAND_LIST_TYPE_BUNDLE** 所建立的命令清單會會至延遲的內容。 Direct3D 12 也支援 abiilty，以同時存取 *立即內容* 的一些功能，以透過 **D3D12_COMMAND_LIST_TYPE_COPY** 和 **D3D12_COMMAND_LIST_TYPE_COMPUTE** 命令清單類型來呈現。

## <a name="cpugpu-synchronization"></a>CPU/GPU 同步處理

在 Direct3D 11 中，CPU/GPU 同步處理大多是自動的，而且應用程式不需要維護實體記憶體的狀態。

在 Direct3D 12 中，應用程式必須明確地管理兩個時間軸 (CPU 和 GPU) 。 這需要由應用程式維護資訊、GPU 需要哪些資源，以及有多長的時間。 這也表示應用程式必須負責確保資源 (認可資源、堆積、命令配置器等資源的內容，例如) 不會變更，直到 GPU 完成使用為止。

用於同步處理時間軸的主要物件是 [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) 物件。 使用 GPU 的作業相當簡單，它們可讓 GPU 在完成工作時發出信號。 GPU 和 CPU 都可以是信號，也可以等候圍牆。

這種方法通常是在提交命令清單以執行時，GPU 會在完成 (完成讀取資料) 時傳輸，讓 CPU 可以重複使用或終結資源。

在 Direct3D 11 中， [**>id3d11devicecoNtext：： map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map) 旗標 D3D11 \_ Map \_ WRITE \_ 捨棄基本上會將每個資源視為無限的記憶體供應，應用程式可以寫入 (稱為「重新命名」 ) 的進程。 在 Direct3D 12 中，此程式是明確的：需要配置額外的記憶體，而且應該使用「配置」來同步處理作業。 通道緩衝區 (由大型緩衝區組成) 這可能是很好的方法，請參閱以 [隔離為基礎的資源管理](fence-based-resource-management.md)中的信號緩衝區案例。

![使用信號緩衝區](images/ring-buffer-1.png)

## <a name="resource-binding"></a>資源系結

Direct3D 11 中的 Views (著色器資源檢視、轉譯目標視圖等) ，在 Direct3D 12 中，主要是以描述項的概念取代。 建立方法仍然存在於 Direct3D 12 (例如 [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview) 和 [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)) ，在建立描述元堆積之後呼叫，以將資料寫入堆積。 Direct3D 12 中的系結現在是由根簽章中所述的描述項控制碼處理，並使用 [**SetGraphicsRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) 或 [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) 方法來提交。

根簽章會詳細說明根簽章位置編號和描述中繼資料表之間的對應，其中描述項資料表可包含指向頂點著色器、圖元著色器和其他著色器的資源參考，例如常數緩衝區、著色器資源檢視器和取樣器。 這種彈性會中斷 HLSL 登錄空間與 Direct3D 12 中的 API 系結空間之間的連線，與 Direct3D 11 不同，後者之間會有一對一的對應。

此系統的其中一個含意是，應用程式會負責重新命名描述中繼資料表，讓開發人員瞭解變更每個繪製呼叫的單一描述項的效能成本。

Direct3D 12 的新功能是，應用程式可以控制哪些描述元在哪些著色器階段之間共用。 在 Direct3D 11 資源（例如 UAVs）中，所有著色器階段都會共用這些資源。 藉由啟用針對某些著色器階段停用的描述項，已停用的描述項所使用的暫存器可供針對特定著色器階段啟用的描述項使用。

下表顯示範例根簽章。



| 根參數位置 | 描述項資料表專案         |
|---------------------|--------------------------------|
| 0                   | VS 描述項範圍 b0-b13     |
| 1                   | VS 描述項範圍 t0-t127    |
| 2                   | VS 描述項範圍 s0-s16     |
| 3                   | PS 描述項範圍 b0-b13     |
| ...                 |                                |
| 14                  | DS 描述項範圍 s0-16      |
| 15                  | 共用描述項範圍 u0-u63 |



 

## <a name="resource-state"></a>資源狀態

在 Direct3D 11 中，應用程式不會維護資源狀態，而是由驅動程式維護。

在 Direct3D 12 中，維護資源狀態會成為應用程式的責任，以便在記錄命令清單時啟用完整平行處理原則：應用程式必須處理命令清單的錄製時間軸 (可以平行) ，以及必須是連續的執行時間軸。

資源狀態轉換是由 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 方法處理。 主要應用程式必須在資源使用量變更時通知驅動程式。 例如，如果資源當做轉譯目標使用，然後在下一次繪製呼叫中當做頂點著色器的輸入使用，則在處理頂點著色器之前，可能需要短暫的 GPU 作業，才能完成轉譯目標操作。

此系統可進行精細的同步處理 (GPU 會停止圖形管線) ，以及快取排清以及可能的一些記憶體配置變更 (例如，將目標視圖轉譯為深度樣板視圖解壓縮) 。

這就是所謂的轉換屏障。 在 Direct3D 11 中有其他阻礙， [**ID3D11DeviceCoNtext2：： TiledResourceBarrier**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) 啟用了兩個不同的並排資源所使用的相同實體記憶體。 在 Direct3D 12 中，這稱為「別名屏障」。 您可以在 Direct3D 12 中，針對已並排和放置的資源使用別名。 此外，還有 UAV 關卡。 在 Direct3D 11 中，所有 UAV 分派和繪製作業都必須進行序列化，即使這些作業可以進行管線處理或平行處理也是一樣。 針對 Direct3D 12，這項限制會透過新增 UAV 關卡來移除。 UAV 關卡可確保 UAV 作業是連續的，因此，如果第二個作業需要第一個完成，則會強制第二個作業因新增關卡而等候。 UAVs 的預設作業只是要儘快進行作業。

如果可以平行處理工作負載，顯然會提高效能。

## <a name="swapchains"></a>Swapchains

DXGI 交換鏈是 Direct3D 11 和12中交換鏈的基礎。 在 Direct3D 11 中有一些微的差異，這三種交換鏈類型為連續、捨棄和翻轉 \_ 順序。 針對 Direct3D 12，只有兩種類型：反轉 \_ 順序和翻轉 \_ 捨棄。 如先前所述，您應該透過 **IDXGIFactory4** 或更新版本明確地建立 swapchain，並對任何介面卡列舉使用相同的介面。

在 Direct3D 11 中，有自動背景緩衝區輪替：後置緩衝區0只需要一個呈現目標視圖。 在 Direct3D 12 中，緩衝區輪替是明確的，每個後置緩衝區都必須有一個呈現目標視圖。 您可以使用 [**IDXGISwapChain3：： GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) 方法來選取要轉譯至哪一個。 同樣地，這種額外的彈性也能提高平行化。

> [!NOTE]
> 雖然有許多方式可以設定您的應用程式，但應用程式的每個交換鏈緩衝區通常都有一個 **ID3D12CommandAllocator** 。 這可讓應用程式在 GPU 轉譯之前，繼續為下一個框架建立一組命令。

## <a name="fixed-function-rendering"></a>修正函式轉譯

在 Direct3D 11 中，有幾種方法可簡化各種較高層級的作業，例如 [**GenerateMips**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips) (建立完整的 mip 鏈) 和 [**DrawAuto**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto) (使用串流輸出做為著色器輸入，而不需要從應用程式) 進一步輸入。 在 Direct3D 12 中不提供這些方法，應用程式必須藉由建立著色器來執行這些作業，以處理這些作業。

## <a name="odds-and-ends"></a>機率和結束

下表顯示 Direct3D 11 和12之間有許多類似的功能，但不完全相同。



| Direct3D 11                                                                            | Direct3D 12                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Query**](/windows/win32/api/d3d11/nn-d3d11-id3d11query)                                              | [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) 允許將查詢群組在一起，以降低成本。                                                                                                                                                                                                                                                                                                                                     |
| [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate)                                      | Predication 現在藉由在完全透明的緩衝區中提供資料來啟用。 Direct3D 11 [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate) 物件是由 [**ID3D12Resource：： Map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)所取代，它必須遵循 [**ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) 的呼叫，以及使用隔離來等候資料準備就緒的 GPU 同步作業。 請參閱 [Predication](predication.md)。 |
| UAV/SO hidden 計數器                                                                  | 應用程式會負責配置和管理 UAV 計數器。 請參閱 [Stream 輸出計數器](stream-output-counters.md) 和 [UAV 計數器](uav-counters.md)。                                                                                                                                                                                                                                                             |
| 資源動態 MinLOD (minium 現任層級的詳細資料)                                        | 這已經移至 SRV 描述項靜態 MinLOD。                                                                                                                                                                                                                                                                                                                                                                                 |
| 繪製 \* 間接/[**DispatchIndirect**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect) | 繪圖間接方法全都合併到一個 [**ExecuteIndirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) 方法中。                                                                                                                                                                                                                                                                                                        |
| DepthStencil 格式是交錯的                                                   | DepthStencil 格式為平面。 例如，24位深度的格式，將會以24/8/24/8 格式儲存8位的樣板 .。。在 Direct3D 11 中，但 24/24/24 .。。後面接著 8/8/8 .。。在 Direct3D 12 中。 請注意，每個平面在 D3D12 中都是自己的 subresource (請參閱 [子資源](subresources.md)) 。                                                                                                                    |
| [**ResizeTilePool**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)                   | 保留的資源可以對應至多個堆積。 當磚集區在 D3D11 中已成長時，可以改為在 D3D12 中配置額外的堆積。                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectX advanced learning 影片教學課程： DirectX 11 至 DirectX 12 移植指南](https://www.youtube.com/watch?v=BV64mdOCgZo)
</dt> <dt>

[瞭解 Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[使用 Direct3D 11、Direct3D 10 和 Direct2D](direct3d-12-interop.md)
</dt> </dl>
