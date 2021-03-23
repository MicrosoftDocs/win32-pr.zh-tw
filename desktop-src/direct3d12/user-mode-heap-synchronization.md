---
title: 多引擎同步處理
description: 本主題討論如何同步處理在大部分新式 Gpu 中找到之多個獨立引擎的存取。
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: d60704e411a1ba45dd4902ad9101a416391743dd
ms.sourcegitcommit: 622d149edf775af5a9633c2d12ccfddf7000b8fd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/31/2020
ms.locfileid: "104548345"
---
# <a name="multi-engine-synchronization"></a>多引擎同步處理

大部分新式 Gpu 包含多個可提供特殊功能的獨立引擎。 許多人都有一或多個專用的複製引擎和一個計算引擎，通常與3D 引擎不同。 這些引擎都可以彼此平行執行命令。 Direct3D 12 使用佇列和命令清單，可讓您更精細地存取3D、計算和複製引擎。

## <a name="gpu-engines"></a>GPU 引擎

下圖顯示標題的 CPU 執行緒，每個執行緒都會填入一或多個複製、計算和3D 佇列。 3D 佇列可以驅動所有三個 GPU 引擎;計算佇列可以驅動計算和複製引擎;而複製佇列則只是複製引擎。

當不同的執行緒擴展佇列時，可能不會有任何簡單的保證執行順序，因此 &mdash; 當標題需要時，需要同步處理機制。

![將命令傳送至三個佇列的四個執行緒](images/gpu-engines.png)

下圖說明標題如何跨多個 GPU 引擎排程工作，包括在必要時進行引擎間同步處理：它會顯示具有引擎間相依性的每個引擎工作負載。 在此範例中，複製引擎會先複製轉譯所需的一些幾何。 3D 引擎會等候這些複本完成，並透過幾何呈現預先傳遞。 然後，計算引擎會使用此功能。 計算引擎 [**分派**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)的結果，以及複製引擎上的數個材質複製作業，都是由3d 引擎用來進行最終 [**繪製**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced) 呼叫。

![複製、圖形和計算引擎通訊](images/gpu-sync.png)

下列虛擬程式碼會說明標題如何提交這類工作負載。

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

下列虛擬程式碼示範複製和3D 引擎之間的同步處理，以透過信號緩衝區完成類似堆積的記憶體配置。 標題可讓您彈性地在最大化平行處理原則 (之間選擇適當的平衡) 並透過小型緩衝區) 減少記憶體耗用量和延遲 (。

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a>多引擎案例

Direct3D 12 可讓您避免意外因非預期的同步處理延遲而發生低效率。 它也可讓您在較高的層級導入同步處理，在這種情況下，您可以更確定所需的同步處理。 多重引擎定址的第二個問題是，更明確地進行昂貴的作業，包括在3D 和影片之間的轉換，因為在多個核心內容之間進行同步處理，所以傳統上會耗費大量的成本。

特別是，下列案例可以透過 Direct3D 12 來解決。

-   非同步和低優先順序的 GPU 工作。 這可並存執行低優先順序的 GPU 工作和不可部分完成的作業，讓一個 GPU 執行緒在不封鎖的情況下，使用另一個未同步處理執行緒的結果。
-   高優先順序的計算工作。 使用背景計算，可以中斷3D 轉譯，以執行少量的高優先順序計算工作。 這項工作的結果可提早取得，以在 CPU 上進行額外的處理。
-   背景計算工作。 計算工作負載的個別低優先順序佇列，可讓應用程式利用備用 GPU 迴圈來執行背景計算，而不會對主要轉譯 (或其他) 工作造成負面影響。 背景工作可能包括解壓縮資源或更新模擬或加速結構。 背景工作應該不常在 CPU 上進行同步處理 (大約每個畫面) ，以避免拖延或減緩前景工作。
-   串流和上傳資料。 個別的複製佇列取代了初始資料和更新資源的 D3D11 概念。 雖然應用程式會負責 Direct3D 12 模型中的更多詳細資料，但這項責任具有強大的功能。 應用程式可以控制用來緩衝處理上傳資料的系統記憶體數量。 應用程式可以選擇 (CPU 與 GPU 的時機和方式、封鎖與非封鎖的) 同步處理，以及追蹤進度及控制已排入佇列的工作量。
-   提高的平行處理原則。 應用程式可以針對背景工作負載使用更深入的佇列 (例如，當它們有個別的佇列可用於前景工作時，) 的影片解碼。

在 Direct3D 12 中，命令佇列的概念是應用程式所提交之大約一連串序列工作的 API 標記法。 屏障和其他技術可讓您在管線中或依循序執行此工作，但應用程式只會看到單一完成時間軸。 這會對應到 D3D11 中的直屬內容。

## <a name="synchronization-apis"></a>同步處理 Api

### <a name="devices-and-queues"></a>裝置和佇列

Direct3D 12 裝置有方法可建立及取出不同類型和優先順序的命令佇列。 大部分的應用程式都應該使用預設的命令佇列，因為它們允許其他元件共用使用量。 具有額外並行需求的應用程式可以建立額外的佇列。 佇列是由其取用的命令清單類型所指定。

請參閱下列 [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device)的建立方法。

-   [**CreateCommandQueue**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) ：根據 [**Direct3D 12 \_ 命令 \_ 佇列 \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) 結構中的資訊建立命令佇列。
-   [**CreateCommandList**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) ：建立 [**Direct3D 12 \_ 命令 \_ 清單 \_ 類型**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type)類型的命令清單。
-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) ：建立一個範圍，並記下 [**Direct3D 12 \_ 隔離 \_ 旗標**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags)中的旗標。 使用的是用來同步處理佇列。

所有類型 (3D、計算和複製) 的佇列會共用相同的介面，並以所有命令清單為基礎。

請參閱下列 [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)方法。

-   [**ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) ：提交要執行的命令清單陣列。 每個命令清單都是由 [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)所定義。
-   [**信號**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) ：當 (在 GPU 上執行的佇列) 達到特定點時，設定隔離值。
-   [**等候**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) ：佇列會等到指定的範圍達到指定的值為止。

請注意，所有佇列都不會使用組合，因此不能使用此類型來建立佇列。

### <a name="fences"></a>柵欄

多引擎 API 提供明確的 Api，以使用圍牆來建立和同步處理。 範圍是由 UINT64 值所控制的同步處理結構。 隔離值是由應用程式設定。 信號作業會修改隔離值，而等候作業會封鎖，直到範圍達到要求的值或更高的值。 當範圍達到特定值時，就會引發事件。

請參閱 [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) 介面的方法。

-   [**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) ：傳回目前的範圍值。
-   [**SetEventOnCompletion**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) ：當範圍達到指定值時，就會引發事件。
-   [**信號**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) ：將範圍設定為指定的值。

範圍可讓 CPU 存取目前的隔離值，以及 CPU 等候和信號。

[**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)介面上的 [**信號**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal)方法會更新 CPU 端的隔離。 此更新會立即進行。 [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)上的 [**信號**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)方法會更新 GPU 端的隔離。 此更新會在命令佇列上的所有其他作業都已完成之後發生。

多引擎安裝程式中的所有節點都可以讀取和回應任何範圍，達到正確的值。

應用程式會設定自己的隔離值，好的起點可能會針對每個框架增加一次範圍。

*可* 倒轉的範圍 *。* 這表示，隔離值不需要單獨遞增。 如果在兩個不同的命令佇列上將 **信號** 作業排入佇列，或兩個 CPU 執行緒都在一個範圍上呼叫 **信號** ，則可能會有一個競爭來判斷最後最後一個 **信號** 的完成，因此會保留哪一個隔離值。 如果已倒轉範圍，任何新的等候 (包括 **SetEventOnCompletion** 要求) 將會與新的較低範圍值進行比對，因此即使此範圍值之前夠高足以滿足這些要求，也可能不會對其感到滿意。 如果發生競爭情形，則在可滿足未完成等候的值與較低的值之間， *將會符合等候，* 而不考慮之後剩下的值。

隔離 Api 提供功能強大的同步處理功能，但可能會導致難以偵測的問題。 建議您只使用每個隔離來指出某個時間軸上的進度，以防止 signalers 之間的競爭。

### <a name="copy-and-compute-command-lists"></a>複製和計算命令清單

所有三種類型的命令清單都會使用 [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面，不過複製和計算只支援方法的子集。

複製和計算命令清單可以使用下列方法。

-   [**關閉**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyTiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**重設**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

計算命令清單也可以使用下列方法。

-   [**ClearState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [**ClearUnorderedAccessViewFloat**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ClearUnorderedAccessViewUint**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**分派**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**ExecuteIndirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [**SetComputeRoot32BitConstant**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetComputeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

在呼叫 [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)時，計算命令清單必須設定計算 PSO。

套件組合無法搭配計算或複製命令清單或佇列使用。

## <a name="pipelined-compute-and-graphics-example"></a>管線計算和圖形範例

此範例示範如何使用範圍同步處理，在佇列上建立計算工作的管線 (由佇列中的 `pComputeQueue` 圖形工作所使用的) 所參考 `pGraphicsQueue` 。 計算和圖形工作會使用圖形佇列來進行管線處理，從數個畫面格取用計算工作的結果，而 CPU 事件則是用來節流整個佇列的總工作。

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

若要支援此管線，必須有 `ComputeGraphicsLatency+1` 從計算佇列傳遞至圖形佇列的不同資料複本的緩衝區。 命令清單必須使用 UAVs 和間接取值，從緩衝區中資料的適當「版本」中讀取和寫入。 計算佇列必須等到圖形佇列完成讀取畫面格 N 的資料後，才能寫入框架 `N+ComputeGraphicsLatency` 。

請注意，相對於 CPU 的計算佇列數量不會直接取決於所需的緩衝量，不過，將 GPU 的工作量超過可用的緩衝區空間量並不重要。

避免間接取值的替代機制是建立多個對應到每個「重新命名」版本資料的命令清單。 下一個範例會使用這項技術來擴充先前的範例，讓計算和圖形佇列以非同步方式執行。

## <a name="asynchronous-compute-and-graphics-example"></a>非同步計算和圖形範例

下一個範例可讓圖形從計算佇列以非同步方式呈現。 這兩個階段之間仍有固定的緩衝資料量，但現在圖形工作會獨立執行，並使用在圖形工作排入佇列時 CPU 上已知的計算階段最新結果。 如果圖形工作正在由其他來源（例如使用者輸入）進行更新，這將會很有用。 必須要有多個命令清單，才能讓 `ComputeGraphicsLatency` 圖形工作的框架一次在飛行，而此函式 `UpdateGraphicsCommandList` 代表更新命令清單來包含最新的輸入資料，並從適當的緩衝區讀取計算資料。

計算佇列仍然必須等待圖形佇列完成管道緩衝區，但導入了第三個範圍 () ， `pGraphicsComputeFence` 讓圖形讀取計算工作的進度和一般圖形進度都可以追蹤。 這會反映出現在連續圖形框架可以從相同計算結果讀取的事實，或可能略過計算結果。 更有效率但稍微複雜的設計只會使用單一圖形範圍，並將對應儲存至每個圖形框架所使用的計算框架。

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a>多佇列資源存取

若要存取一個以上佇列的資源，應用程式必須遵守下列規則。

-   資源存取 (請參閱 [**Direct3D 12 \_ 資源 \_ 狀態**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) ，) 由佇列類型類別非佇列物件所決定。 佇列的類型有兩種：計算/3D 佇列是一種類型類別，Copy 是第二種類型類別。 因此，在 \_ \_ 一個3d 佇列上具有非圖元著色器資源狀態之障礙的資源 \_ ，可以在任何3d 或計算佇列上以該狀態使用，受限於需要序列化大部分寫入的同步處理需求。 在兩個類型類別之間共用的資源狀態 (複製 \_ 來源和複製 \_ 目的地) 會視為每個類型類別的不同狀態。 如此一來，如果資源轉換為複製 \_ 佇列上的目的地，則無法從3d 或計算佇列的複製目的地存取該資源，反之亦然。

    總結。

    -   佇列「物件」是任何單一佇列。
    -   佇列「類型」是下列三種之一：計算、3D 和複製。
    -   佇列「類型類別」是下列其中一項：計算/3D 和複製。

-   複製旗標 (複製 \_ 目的地和複製 \_ 來源) 當做初始狀態使用，代表 3D/計算類型類別中的狀態。 若要在一開始就在複製佇列上使用資源，它應該會在一般狀態中啟動。 您可以使用隱含狀態轉換，將一般狀態用於複製佇列上的所有使用量。 
-   雖然資源狀態會跨所有計算和3D 佇列共用，但不允許在不同佇列上同時寫入資源。 這裡的「同時」表示未同步處理，請注意，在某些硬體上並不可能執行未同步執行。 適用下列規則。

    -   一次只能有一個佇列寫入資源。
    -   多個佇列可以從資源讀取，只要它們未讀取寫入器所修改的位元組 (讀取同時寫入的位元組會產生未定義的結果) 。
    -   在寫入之前，必須先使用隔離來同步處理，另一個佇列可以讀取寫入的位元組或進行寫入存取。

-   所呈現的背景緩衝區必須處於 Direct3D 12 \_ 資源 \_ 狀態的 \_ 一般狀態。 

## <a name="related-topics"></a>相關主題

[Direct3D 12 程式設計指南](directx-12-programming-guide.md)

[在 Direct3D 12 中使用資源阻礙來同步處理資源狀態](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[Direct3D 12 中的記憶體管理](memory-management.md)
