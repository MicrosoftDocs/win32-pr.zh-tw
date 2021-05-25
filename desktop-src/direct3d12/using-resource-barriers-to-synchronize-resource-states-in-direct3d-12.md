---
title: 在 Direct3D 12 中使用資源阻礙來同步處理資源狀態
description: 為了降低整體 CPU 使用率並啟用驅動程式多執行緒處理和預先處理，Direct3D 12 會將每個資源狀態管理的責任從圖形驅動程式移至應用程式。
ms.assetid: 3AB3BF34-433C-400B-921A-55B23CCDA44F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df27e7997b4f3f56ae8e87688e5cc136dc7eb87d
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343473"
---
# <a name="using-resource-barriers-to-synchronize-resource-states-in-direct3d-12"></a>在 Direct3D 12 中使用資源阻礙來同步處理資源狀態

為了降低整體 CPU 使用率並啟用驅動程式多執行緒處理和預先處理，Direct3D 12 會將每個資源狀態管理的責任從圖形驅動程式移至應用程式。 每個資源狀態的範例，是目前是否正在透過著色器資源檢視或轉譯目標視圖來存取材質資源。 在 Direct3D 11 中，需要有驅動程式，才能在背景中追蹤此狀態。 從 CPU 的角度來看，這是很耗費資源的，而且會大幅使多執行緒的設計變得更複雜。 在 Microsoft Direct3D 12 中，大部分的每個資源狀態都是由應用程式使用單一 API （ [**ID3D12GraphicsCommandList：： ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)）來管理。

-   [使用 ResourceBarrier API 來管理每個資源的狀態](#using-the-resourcebarrier-api-to-manage-per-resource-state)
    -   [資源狀態](#using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
    -   [資源的初始狀態](#initial-states-for-resources)
    -   [讀取/寫入資源狀態限制](#readwrite-resource-state-restrictions)
    -   [用來呈現回緩衝區的資源狀態](#resource-states-for-presenting-back-buffers)
    -   [捨棄資源](#discarding-resources)
-   [隱含狀態轉換](#implicit-state-transitions)
    -   [一般狀態提升](#common-state-promotion)
    -   [狀態衰減至一般](#state-decay-to-common)
    -   [效能影響](#performance-implications)
-   [分割阻礙](#split-barriers)
-   [資源屏障範例案例](#resource-barrier-example-scenario)
-   [一般狀態提升和衰減範例](#common-state-promotion-and-decay-sample)
-   [分割障礙的範例](#example-of-split-barriers)
-   [相關主題](#related-topics)

## <a name="using-the-resourcebarrier-api-to-manage-per-resource-state"></a>使用 ResourceBarrier API 來管理每個資源的狀態

[**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 會通知圖形驅動程式，其中驅動程式可能需要將多個存取與儲存資源的記憶體進行同步處理。 呼叫方法時，會使用一或多個資源關卡描述結構，指出所宣告的資源屏障類型。

有三種類型的資源阻礙：

-   **轉換屏障** -轉換屏障指出不同使用方式之間的一組子資源轉換。 [**D3D12 \_ 資源 \_ 轉換 \_ 屏障**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_transition_barrier)結構是用來指定正在轉換的 subresource，以及 subresource *之前* 和 *之後* 的狀態。

    系統會確認命令清單中的 subresource 轉換與先前的轉換在相同的命令清單中是一致的。 Debug 層會進一步追蹤 subresource 狀態以找出其他錯誤，不過這項驗證很保守且不詳盡。

    請注意，您可以使用 D3D12 \_ 資源 \_ 關卡 \_ 所有 \_ 子資源旗標，指定要轉換資源內的所有子資源。

-   **別名屏障** -別名屏障表示兩個不同資源的使用方式之間的轉換，這些資源在相同堆積中有重迭的對應。 這同時適用于保留和放置的資源。 [**D3D12 \_ 資源 \_ 別名 \_ 屏障**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_aliasing_barrier)結構是用來同時指定資源和 *之後**資源。*

    請注意，其中一個或兩個資源可以是 Null，這表示任何已並排顯示的資源可能會造成別名。 如需使用並排顯示資源的詳細資訊， [請參閱並排顯示的資源和](../direct3d11/tiled-resources.md) 磁片區並排顯示的 [資源](volume-tiled-resources.md)。

-   未 **排序的存取視圖 (UAV) 屏障**-UAV 屏障指出任何未來的 UAV 存取（讀取或寫入）之間的所有 UAV 存取（讀取或寫入）都必須完成。 應用程式不需要在唯讀取 UAV 的兩個繪製或分派呼叫之間放置 UAV 關卡。 此外，如果應用程式知道可以安全地以任何循序執行 UAV 存取，就不需要在兩個繪製或分派呼叫之間放置 UAV 關卡，以寫入相同的 UAV。 [**D3D12 \_ 資源 \_ UAV \_ 屏障**](/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_uav_barrier)結構是用來指定要套用關卡的 UAV 資源。 應用程式可以針對關卡的 UAV 指定 Null，這表示任何 UAV 存取都可能需要關卡。

使用資源屏障描述的陣列來呼叫 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 時，API 的行為就像是針對每個專案呼叫一次一樣，依照提供的順序。

在任何指定的時間，subresource 都只會在一種狀態中，取決於提供給 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)的一組 [**D3D12 \_ 資源 \_ 狀態**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)旗標。 應用程式必須確定連續呼叫 **ResourceBarrier** 的 *前後**狀態同意*。

> [!TIP]
>
> 應用程式應該盡可能將多個轉換批次處理成一個 API 呼叫。

 

### <a name="resource-states"></a>資源狀態

如需資源可在其之間轉換的資源狀態完整清單，請參閱 [**D3D12 \_ 資源 \_ 狀態**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) 列舉的參考主題。

針對分割資源阻礙，也請參閱 [**D3D12 \_ 資源 \_ 屏障 \_ 旗標**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_barrier_flags)。

### <a name="initial-states-for-resources"></a>資源的初始狀態

您可以使用任何使用者指定的初始狀態來建立資源 (適用于資源描述) ，但有下列例外狀況：

-   上傳堆積必須在狀態 D3D12 \_ 資源 \_ 狀態一般讀取中開始， \_ \_ 它是的位 or 組合：
    -   D3D12 \_ 資源 \_ 狀態 \_ 頂點 \_ 和 \_ 常數 \_ 緩衝區
    -   D3D12 \_ 資源 \_ 狀態 \_ 索引 \_ 緩衝區
    -   D3D12 \_ 資源 \_ 狀態 \_ 複製 \_ 來源
    -   D3D12 \_ 資源 \_ 狀態 \_ 非 \_ 圖元 \_ 著色器 \_ 資源
    -   D3D12 \_ 資源 \_ 狀態 \_ 圖元 \_ 著色器 \_ 資源
    -   D3D12 \_ 資源 \_ 狀態 \_ 間接 \_ 引數
-   Readback 堆積必須以 D3D12 \_ 資源 \_ 狀態 \_ 複製 \_ 目的地狀態開始。
-   交換鏈回緩衝區會自動以 D3D12 \_ 資源狀態的 \_ \_ 常見狀態開始。

在堆積可以成為 GPU 複製作業的目標之前，通常必須先將堆積轉換成 D3D12 \_ 資源 \_ 狀態 \_ 複製 \_ 目的地狀態。 不過，在上傳堆積上建立的資源必須以開始，而且無法從一般 \_ 讀取狀態變更，因為只有 CPU 會進行寫入。 相反地，在 READBACK 堆積中建立的認可資源必須在中開始，而且無法從複製 \_ 目的地狀態變更。

### <a name="readwrite-resource-state-restrictions"></a>讀取/寫入資源狀態限制

用來描述資源狀態的資源狀態使用位會分成隻讀和讀取/寫入狀態。 [**D3D12 \_ 資源 \_ 狀態**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)的參考主題指出列舉中每個位的讀取/寫入存取層級。

最多隻能為任何資源設定一個讀取/寫入位。 如果已設定寫入位，則可能不會針對該資源設定唯讀位。 如果未設定寫入位，則可能會設定任何數目的讀取位。

### <a name="resource-states-for-presenting-back-buffers"></a>用來呈現回緩衝區的資源狀態

在顯示背景緩衝區之前，它必須處於 D3D12 \_ 資源 \_ 狀態的 \_ 一般狀態。 請注意，目前的資源狀態 D3D12 \_ 資源 \_ 狀態 \_ 是 D3D12 \_ 資源狀態的 \_ 同義字 \_ ，而且兩者的值都是0。 如果 [**IDXGISwapChain：:P**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) 重新傳送 (或 [**IDXGISwapChain1：:P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)) 是在目前非此狀態的資源上呼叫，則會發出 debug layer 警告。

### <a name="discarding-resources"></a>捨棄資源

資源中的所有子資源都必須分別在轉譯 \_ 目標/深度寫入狀態中，以轉譯目標/深度樣板資源，同時也會在 \_ 呼叫 [**ID3D12GraphicsCommandList：:D iscardresource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource) 。

## <a name="implicit-state-transitions"></a>隱含狀態轉換

資源只能「升級」超出 D3D12 的 \_ 資源 \_ 狀態 \_ 。 同樣地，資源只會「衰減」以 D3D12 \_ 資源 \_ 狀態 \_ 。

### <a name="common-state-promotion"></a>一般狀態提升

所有緩衝區資源以及具有 D3D12 資源旗標的 \_ 材質 \_ \_ ，都可讓您 \_ \_ \_ \_ \_ 在第一次 GPU 存取時，以隱含的方式從 D3D12 資源狀態（包括一般 \_ 讀取來涵蓋任何讀取案例），將同時存取旗標設定為隱含地升級為相關狀態。 任何處于一般狀態的資源都可以透過其在單一狀態中進行存取，

<dl> 1寫入旗標，或  
1或多個讀取旗標  
</dl>

您可以根據下表，從一般狀態升級資源：



| 狀態旗標                    | 緩衝區和 Simultaneous-Access 紋理                             | 非同時存取的材質                                     |
|-------------------------------|----------------------------------------------|--------------------------------------|
| 頂點 \_ 和 \_ 常數 \_ 緩衝區 | 是                                          | 否                                   |
| 索引 \_ 緩衝區                 | 是                                          | 否                                   |
| 呈現 \_ 目標                | 是                                          | 否                                   |
| 未排序的 \_ 存取             | 是                                          | 否                                   |
| 深度 \_ 寫入                  | 不<sup>\*</sup>                              | No                                   |
| 深度 \_ 讀取                   | 不<sup>\*</sup>                              | No                                   |
| 非 \_ 圖元 \_ 著色器 \_ 資源  | 是                                          | 是                                  |
| 圖元 \_ 著色器 \_ 資源       | 是                                          | 是                                  |
| 串流 \_ 輸出                   | 是                                          | 否                                   |
| 間接 \_ 引數            | 是                                          | 否                                   |
| 複製 \_ 目的地                    | 是                                          | 是                                  |
| 複製 \_ 來源                  | 是                                          | 是                                  |
| 解析 \_ 目的地                 | 是                                          | 否                                   |
| 解析 \_ 來源               | 是                                          | 否                                   |
| 預測                   | 是                                          | 否                                   |



 

<sup>\*</sup>深度樣板資源必須是不可同時存取的材質，因此永遠不會隱含地升級。

當此存取進行時，升級的作用就像是隱含的資源屏障。 針對後續的存取，必要時，資源屏障將需要變更資源狀態。 請注意，從一個已升級的讀取狀態升階為多個讀取狀態是有效的，但這不是寫入狀態的情況。  
例如，如果在繪製呼叫中將共通狀態的資源升級為圖元 \_ 著色器 \_ 資源，它仍然可以升級為 NON_PIXEL \_ 著色器 \_ 資源 |\_ \_ 另一個繪製呼叫中的圖元著色器資源。 但是，如果在寫入作業（例如複製目的地）中使用它，則資源狀態轉換會從合併的已升級讀取狀態中阻礙，此處 NON_PIXEL \_ 著色器 \_ 資源 |\_ \_ 需要複製目的地的圖元著色器資源 \_ 。  
同樣地，如果從共通升級為複製 \_ 目的地，仍然需要關卡從複製目的地轉換 \_ 成轉譯 \_ 目標。

請注意，一般狀態提升為「免費」，因為 GPU 不需要執行任何同步處理等候。 此促銷代表一般狀態中的資源應該不需要額外的 GPU 工作或驅動程式追蹤來支援特定存取。

### <a name="state-decay-to-common"></a>狀態衰減至一般

一般狀態升級的翻轉端會衰減回 D3D12 的 \_ 資源 \_ 狀態 \_ 。 符合特定需求的資源會被視為無狀態，而且在 GPU 完成執行 [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) 作業時，會有效地回到一般狀態。 在相同的 **ExecuteCommandLists** 呼叫中一起執行的命令清單之間，不會發生衰減。

當 GPU 上的 [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) 作業完成時，下列資源將會衰減：

-   在複製佇列上存取的資源， *或*
-   任何佇列類型上的緩衝區資源， *或*
-   具有 D3D12 資源旗標之任何佇列類型上的材質資源 \_ \_ \_ 允許 \_ 同時 \_ 存取旗標， *或*
-   任何以隱含方式升級為唯讀狀態的資源。

如同一般狀態升級，衰減是免費的，不需要額外的同步處理。 結合一般狀態升階和衰減有助於消除許多不必要的 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 轉換。 在某些情況下，這可提供顯著的效能改進。

緩衝區和 Simultaneous-Access 資源將會衰減至一般狀態，而不論它們是使用資源阻礙明確轉換或隱含地升級。

### <a name="performance-implications"></a>效能影響

在一般狀態的資源上記錄明確的 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)轉換時，請正確地使用 D3D12 \_ 資源 \_ 狀態 \_ 一般或任何可提升狀態，作為 D3D12 資源 \_ \_ 轉換屏障結構中的 BeforeState 值 \_ 。 這可讓傳統的狀態管理忽略自動衰減的緩衝區和同時存取的材質。 不過，這可能不是理想的做法，因為避免使用已知處於一般狀態之資源的轉換 **ResourceBarrier** 呼叫，可大幅提升效能。 資源障礙的成本可能很高。 它們是設計來強制快取排清、記憶體配置變更，以及對已處於一般狀態的資源而言，可能不需要的其他同步處理。 在目前處於一般狀態的資源上使用資源屏障的命令清單，可能會造成許多不必要的額外負荷。

此外，除非絕對必要 (，否則請避免明確的 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 轉換 D3D12 \_ 資源 \_ 狀態， \_ 例如，下一次存取是在需要在一般) 狀態下啟動資源的複製命令佇列。 過度轉換成常見狀態可能會大幅降低 GPU 效能。

總而言之，您可以在不發出 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 呼叫的情況下，嘗試依賴一般狀態提升和衰減。

## <a name="split-barriers"></a>分割阻礙

具有 D3D12 資源屏障旗標「僅限開始」旗標的資源轉換屏障會 \_ \_ \_ \_ \_ 開始分割關卡，而「轉換」關卡則稱為「擱置中」。 當屏障暫止時，GPU 無法讀取或寫入 (子) 資源。 唯一可套用至具有暫止屏障之 (子) 資源的合法轉換屏障是具有相同 *之前* 和 *之後* 狀態的資源，以及 D3D12 \_ 資源 \_ 關卡旗標 \_ \_ 結束旗標 \_ ，這會阻礙完成暫止的轉換。

分割屏障提供提示給 GPU，之後狀態 *a* 中的資源將在稍後於狀態 *B* 中使用。 這會提供 GPU 優化轉換工作負載的選項，可能會減少或避免執行停止。 發出僅限結束的屏障可保證所有 GPU 轉換工作完成後，再移至下一個命令。

使用分割關卡有助於改善效能，特別是在多重引擎案例中，或是資源在一或多個命令清單中的讀取/寫入更稀疏的轉換。

## <a name="resource-barrier-example-scenario"></a>資源屏障範例案例

下列程式碼片段示範如何在多執行緒範例中使用 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 方法。

建立深度樣板視圖，並將其轉換為可寫入狀態。


```C++
// Create the depth stencil.
{
    CD3DX12_RESOURCE_DESC shadowTextureDesc(
        D3D12_RESOURCE_DIMENSION_TEXTURE2D,
        0,
        static_cast<UINT>(m_viewport.Width), 
        static_cast<UINT>(m_viewport.Height), 
        1,
        1,
        DXGI_FORMAT_D32_FLOAT,
        1, 
        0,
        D3D12_TEXTURE_LAYOUT_UNKNOWN,
        D3D12_RESOURCE_FLAG_ALLOW_DEPTH_STENCIL | D3D12_RESOURCE_FLAG_DENY_SHADER_RESOURCE);

    D3D12_CLEAR_VALUE clearValue;    // Performance tip: Tell the runtime at resource creation the desired clear value.
    clearValue.Format = DXGI_FORMAT_D32_FLOAT;
    clearValue.DepthStencil.Depth = 1.0f;
    clearValue.DepthStencil.Stencil = 0;

    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &shadowTextureDesc,
        D3D12_RESOURCE_STATE_DEPTH_WRITE,
        &clearValue,
        IID_PPV_ARGS(&m_depthStencil)));

    // Create the depth stencil view.
    m_device->CreateDepthStencilView(m_depthStencil.Get(), nullptr, m_dsvHeap->GetCPUDescriptorHandleForHeapStart());
}
```



建立頂點緩衝區視圖，先將它從一般狀態變更為目的地，然後從目的地變更為一般可讀取的狀態。


```C++
// Create the vertex buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_vertexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::VertexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the vertex buffer.
        D3D12_SUBRESOURCE_DATA vertexData = {};
        vertexData.pData = pAssetData + SampleAssets::VertexDataOffset;
        vertexData.RowPitch = SampleAssets::VertexDataSize;
        vertexData.SlicePitch = vertexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy vertex buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_vertexBuffer.Get(), m_vertexBufferUpload.Get(), 0, 0, 1, &vertexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_vertexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER));

        PIXEndEvent(commandList.Get());
    }
```



建立索引緩衝區視圖，先將它從一般狀態變更為目的地，然後從目的地變更為一般可讀取的狀態。


```C++
// Create the index buffer.
{
    ThrowIfFailed(m_device->CreateCommittedResource(
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
        D3D12_HEAP_FLAG_NONE,
        &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
        D3D12_RESOURCE_STATE_COPY_DEST,
        nullptr,
        IID_PPV_ARGS(&m_indexBuffer)));

    {
        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
            D3D12_HEAP_FLAG_NONE,
            &CD3DX12_RESOURCE_DESC::Buffer(SampleAssets::IndexDataSize),
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_indexBufferUpload)));

        // Copy data to the upload heap and then schedule a copy 
        // from the upload heap to the index buffer.
        D3D12_SUBRESOURCE_DATA indexData = {};
        indexData.pData = pAssetData + SampleAssets::IndexDataOffset;
        indexData.RowPitch = SampleAssets::IndexDataSize;
        indexData.SlicePitch = indexData.RowPitch;

        PIXBeginEvent(commandList.Get(), 0, L"Copy index buffer data to default resource...");

        UpdateSubresources<1>(commandList.Get(), m_indexBuffer.Get(), m_indexBufferUpload.Get(), 0, 0, 1, &indexData);
        commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_indexBuffer.Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_INDEX_BUFFER));

        PIXEndEvent(commandList.Get());
    }

    // Initialize the index buffer view.
    m_indexBufferView.BufferLocation = m_indexBuffer->GetGPUVirtualAddress();
    m_indexBufferView.SizeInBytes = SampleAssets::IndexDataSize;
    m_indexBufferView.Format = SampleAssets::StandardIndexFormat;
}
```



建立紋理和著色器資源檢視。 材質會從一般狀態變更為目的地，然後從目的地變更為圖元著色器資源。


```C++
    // Create each texture and SRV descriptor.
    const UINT srvCount = _countof(SampleAssets::Textures);
    PIXBeginEvent(commandList.Get(), 0, L"Copy diffuse and normal texture data to default resources...");
    for (int i = 0; i < srvCount; i++)
    {
        // Describe and create a Texture2D.
        const SampleAssets::TextureResource &tex = SampleAssets::Textures[i];
        CD3DX12_RESOURCE_DESC texDesc(
            D3D12_RESOURCE_DIMENSION_TEXTURE2D,
            0,
            tex.Width, 
            tex.Height, 
            1,
            static_cast<UINT16>(tex.MipLevels),
            tex.Format,
            1, 
            0,
            D3D12_TEXTURE_LAYOUT_UNKNOWN,
            D3D12_RESOURCE_FLAG_NONE);

        ThrowIfFailed(m_device->CreateCommittedResource(
            &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT),
            D3D12_HEAP_FLAG_NONE,
            &texDesc,
            D3D12_RESOURCE_STATE_COPY_DEST,
            nullptr,
            IID_PPV_ARGS(&m_textures[i])));

        {
            const UINT subresourceCount = texDesc.DepthOrArraySize * texDesc.MipLevels;
            UINT64 uploadBufferSize = GetRequiredIntermediateSize(m_textures[i].Get(), 0, subresourceCount);
            ThrowIfFailed(m_device->CreateCommittedResource(
                &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_UPLOAD),
                D3D12_HEAP_FLAG_NONE,
                &CD3DX12_RESOURCE_DESC::Buffer(uploadBufferSize),
                D3D12_RESOURCE_STATE_GENERIC_READ,
                nullptr,
                IID_PPV_ARGS(&m_textureUploads[i])));

            // Copy data to the intermediate upload heap and then schedule a copy 
            // from the upload heap to the Texture2D.
            D3D12_SUBRESOURCE_DATA textureData = {};
            textureData.pData = pAssetData + tex.Data->Offset;
            textureData.RowPitch = tex.Data->Pitch;
            textureData.SlicePitch = tex.Data->Size;

            UpdateSubresources(commandList.Get(), m_textures[i].Get(), m_textureUploads[i].Get(), 0, 0, subresourceCount, &textureData);
            commandList->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_textures[i].Get(), D3D12_RESOURCE_STATE_COPY_DEST, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
        }

        // Describe and create an SRV.
        D3D12_SHADER_RESOURCE_VIEW_DESC srvDesc = {};
        srvDesc.ViewDimension = D3D12_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Shader4ComponentMapping = D3D12_DEFAULT_SHADER_4_COMPONENT_MAPPING;
        srvDesc.Format = tex.Format;
        srvDesc.Texture2D.MipLevels = tex.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = 0;
        srvDesc.Texture2D.ResourceMinLODClamp = 0.0f;
        m_device->CreateShaderResourceView(m_textures[i].Get(), &srvDesc, cbvSrvHandle);

        // Move to the next descriptor slot.
        cbvSrvHandle.Offset(cbvSrvDescriptorSize);
    }
```



開始畫面格;這並不只會使用 [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) 來指出要使用背景緩衝區做為轉譯目標，也會初始化框架資源 (在深度樣板緩衝區) 上呼叫 **ResourceBarrier** 。


```C++
// Assemble the CommandListPre command list.
void D3D12Multithreading::BeginFrame()
{
    m_pCurrentFrameResource->Init();

    // Indicate that the back buffer will be used as a render target.
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET));

    // Clear the render target and depth stencil.
    const float clearColor[] = { 0.0f, 0.0f, 0.0f, 1.0f };
    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_pCurrentFrameResource->m_commandLists[CommandListPre]->ClearDepthStencilView(m_dsvHeap->GetCPUDescriptorHandleForHeapStart(), D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPre]->Close());
}

// Assemble the CommandListMid command list.
void D3D12Multithreading::MidFrame()
{
    // Transition our shadow map from the shadow pass to readable in the scene pass.
    m_pCurrentFrameResource->SwapBarriers();

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListMid]->Close());
}
```



結束畫面格，表示現在會使用背景緩衝區來呈現。


```C++
// Assemble the CommandListPost command list.
void D3D12Multithreading::EndFrame()
{
    m_pCurrentFrameResource->Finish();

    // Indicate that the back buffer will now be used to present.
    m_pCurrentFrameResource->m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT));

    ThrowIfFailed(m_pCurrentFrameResource->m_commandLists[CommandListPost]->Close());
}
```



初始化框架資源，在開始畫面格時呼叫，會將深度樣板緩衝區轉換為可寫入。


```C++
void FrameResource::Init()
{
    // Reset the command allocators and lists for the main thread.
    for (int i = 0; i < CommandListCount; i++)
    {
        ThrowIfFailed(m_commandAllocators[i]->Reset());
        ThrowIfFailed(m_commandLists[i]->Reset(m_commandAllocators[i].Get(), m_pipelineState.Get()));
    }

    // Clear the depth stencil buffer in preparation for rendering the shadow map.
    m_commandLists[CommandListPre]->ClearDepthStencilView(m_shadowDepthView, D3D12_CLEAR_FLAG_DEPTH, 1.0f, 0, 0, nullptr);

    // Reset the worker command allocators and lists.
    for (int i = 0; i < NumContexts; i++)
    {
        ThrowIfFailed(m_shadowCommandAllocators[i]->Reset());
        ThrowIfFailed(m_shadowCommandLists[i]->Reset(m_shadowCommandAllocators[i].Get(), m_pipelineStateShadowMap.Get()));

        ThrowIfFailed(m_sceneCommandAllocators[i]->Reset());
        ThrowIfFailed(m_sceneCommandLists[i]->Reset(m_sceneCommandAllocators[i].Get(), m_pipelineState.Get()));
    }
}
```



阻礙會在框架中交換，將陰影地圖從可寫入轉換為可讀取。


```C++
void FrameResource::SwapBarriers()
{
    // Transition the shadow map from writeable to readable.
    m_commandLists[CommandListMid]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_DEPTH_WRITE, D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE));
}
```



當框架結束時，會呼叫 Finish，將陰影對應轉換為一般狀態。


```C++
void FrameResource::Finish()
{
    m_commandLists[CommandListPost]->ResourceBarrier(1, &CD3DX12_RESOURCE_BARRIER::Transition(m_shadowTexture.Get(), D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE, D3D12_RESOURCE_STATE_DEPTH_WRITE));
}
```



## <a name="common-state-promotion-and-decay-sample"></a>一般狀態提升和衰減範例

``` syntax
    // Create a buffer resource using D3D12_RESOURCE_STATE_COMMON as the init state
    ID3D12Resource *pResource;
    CreateCommittedVertexBufferInCommonState(1024, &pResource);

    // Copy data to the buffer without the need for a barrier.
    // Promotes pResource state to D3D12_RESOURCE_STATE_COPY_DEST.
    pCommandList->CopyBufferRegion(pResource, 0, pOtherResource, 0, 1024); 

    // To use pResource as a vertex buffer a transition barrier is needed.
    // Note the StateBefore is D3D12_RESOURCE_STATE_COPY_DEST.
    D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TYPE_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_FLAG_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COPY_DEST;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_VERTEX_AND_CONSTANT_BUFFER;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    // Use pResource as a vertex buffer
    D3D12_VERTEX_BUFFER_VIEW vbView;
    vbView.BufferLocation = pResource->GetGPUVirtualAddress();
    vbView.SizeInBytes = 1024;
    vbView.StrideInBytes = sizeof(MyVertex);

    pCommandList->IASetVertexBuffers(0, 1, &vbView);
    pCommandList->Draw();

    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 
    pCommandList->Reset(pAllocator, pPipelineState);

    // Since the reset command list will be executed in a separate call to 
    // ExecuteCommandLists, the previous state of pResource
    // will have decayed to D3D12_RESOURCE_STATE_COMMON so, again, no barrier is needed
    pCommandList->CopyBufferRegion(pResource, 0, pDifferentResource, 0, 1024);

    FinishRecordingCommandList(pCommandList);
    pCommandQueue->ExecuteCommandLists(1, &pCommandList); 

    WaitForQueue(pCommandQueue);

    // The previous ExecuteCommandLists call has finished so 
    // pResource has decayed to D3D12_RESOURCE_STATE_COMMON
```

## <a name="example-of-split-barriers"></a>分割障礙的範例

下列範例示範如何使用分割關卡來減少管線的停止。 接下來的程式碼不會使用分割障礙：

``` syntax
 D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource
    OtherStuff(); // .. other gpu work

    // Transition pResource to PIXEL_SHADER_RESOURCE
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    Read(pResource); // ... read from pResource
```

下列程式碼會使用分割障礙：

``` syntax
D3D12_RESOURCE_BARRIER BarrierDesc = {};
    BarrierDesc.Type = D3D12_RESOURCE_BARRIER_TRANSITION;
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_NONE;
    BarrierDesc.Transition.pResource = pResource;
    BarrierDesc.Transition.Subresource = 0;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_COMMON;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_RENDER_TARGET;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    
    Write(pResource); // ... render to pResource

    // Done writing to pResource. Start barrier to PIXEL_SHADER_RESOURCE and
    // then do other work
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_BEGIN_ONLY;
    BarrierDesc.Transition.StateBefore = D3D12_RESOURCE_STATE_RENDER_TARGET;
    BarrierDesc.Transition.StateAfter = D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE;
    pCommandList->ResourceBarrier( 1, &BarrierDesc );

    OtherStuff(); // .. other gpu work

    // Need to read from pResource so end barrier
    BarrierDesc.Flags = D3D12_RESOURCE_BARRIER_END_ONLY;

    pCommandList->ResourceBarrier( 1, &BarrierDesc );
    Read(pResource); // ... read from pResource
```

## <a name="related-topics"></a>相關主題

[DirectX advanced learning 影片教學課程：資源阻礙和狀態追蹤](https://www.youtube.com/watch?v=nmB2XMasz2o)

[多引擎同步處理](./user-mode-heap-synchronization.md)

[在 Direct3D 12 中提交工作](command-queues-and-command-lists.md)

[深入瞭解 D3D12 資源狀態的障礙](https://devblogs.microsoft.com/directx/a-look-inside-d3d12-resource-state-barriers/)

