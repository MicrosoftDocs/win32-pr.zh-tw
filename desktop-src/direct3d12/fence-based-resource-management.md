---
title: Fence-Based 資源管理
description: 示範如何透過延伸來追蹤 GPU 進度，以管理資源資料的生命週期。 記憶體可以有效地重複使用，以管理記憶體中可用空間的可用性，例如在上傳堆積的通道緩衝區執行中。
ms.assetid: A7AB6569-EC6B-4B1B-9266-D05B6DB3A27B
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba8afd66f8a50a54b699c6a314ba148ebcef023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105059"
---
# <a name="fence-based-resource-management"></a>Fence-Based 資源管理

示範如何透過延伸來追蹤 GPU 進度，以管理資源資料的生命週期。 記憶體可以有效地重複使用，以管理記憶體中可用空間的可用性，例如在上傳堆積的通道緩衝區執行中。

-   [信號緩衝區案例](#ring-buffer-scenario)
-   [信號緩衝區範例](#ring-buffer-sample)
-   [相關主題](#related-topics)

## <a name="ring-buffer-scenario"></a>信號緩衝區案例

以下是應用程式在上傳堆積記憶體時遇到罕見需求的範例。

信號緩衝區是管理上傳堆積的一種方式。 信號緩衝區會保存接下來幾個框架所需的資料。 應用程式會維護目前的資料輸入指標，以及用來記錄每個畫面格和起始該框架之資源資料位移的框架位移佇列。

應用程式會根據緩衝區建立環形緩衝區，以將資料上傳至每個框架的 GPU。 目前已轉譯框架2，信號緩衝區會在框架4的資料周圍換行，而第5幀所需的所有資料都存在，而框架6所需的大型常數緩衝區則需要進行子配置。

**圖 1** ：應用程式嘗試對常數緩衝區進行子配置，但是找不到足夠的可用記憶體。

![此信號緩衝區中的可用記憶體不足](images/ring-buffer-1.png)

**圖 2** ：透過隔離輪詢，應用程式會探索到畫面格3已轉譯，接著會更新框架位移佇列，而信號緩衝區的目前狀態則如下所示，但可用記憶體仍不夠大，無法容納常數緩衝區。

![在畫面格3轉譯之後仍沒有足夠的記憶體](images/ring-buffer-2.png)

**圖 3** ：在此情況下，CPU 區塊本身 (透過範圍等候) ，直到已轉譯框架4為止，這會釋出針對框架4所配置的記憶體。

![轉譯畫面格4釋出更多信號緩衝區](images/ring-buffer-3.png)

**圖 4** ：現在可用記憶體夠大，足以容納常數緩衝區，而子配置成功;應用程式會將大型常數緩衝區資料複製到先前由資源資料用於框架3和4的記憶體。 最後會更新目前的輸入指標。

![信號緩衝區中的框架6現在有空間](images/ring-buffer-4.png)

如果應用程式會執行信號緩衝區，信號緩衝區必須夠大，才能應付資源資料大小的較糟案例。

## <a name="ring-buffer-sample"></a>信號緩衝區範例

下列範例程式碼示範如何管理信號緩衝區，並注意處理隔離輪詢和等候的子配置常式。 為了簡單起見，此範例使用的記憶體不足，無法 \_ \_ 隱藏「在堆積中找不到足夠的可用記憶體」的詳細資料，因為該邏輯 (根據 *m \_ PDataCur* ，而) *FrameOffsetQueue* 內的位移與堆積或圍牆沒有緊密關聯。 此範例已簡化，以犧牲畫面播放速率，而不是記憶體使用率。

請注意，通道緩衝區支援應該是常見的案例;不過，堆積設計不會排除其他使用方式，例如命令清單參數化和重複使用。

``` syntax
struct FrameResourceOffset
{
    UINT frameIndex;
    UINT8* pResourceOffset;
};
std::queue<FrameResourceOffset> frameOffsetQueue;

void DrawFrame()
{
    float vertices[] = ...;
    UINT verticesOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            vertices, sizeof(float), sizeof(vertices) / sizeof(float), 
            4, // Max alignment requirement for vertex data is 4 bytes.
            verticesOffset
            ));

    float constants[] = ...;
    UINT constantsOffset = 0;
    ThrowIfFailed(
        SetDataToUploadHeap(
            constants, sizeof(float), sizeof(constants) / sizeof(float), 
            D3D12_CONSTANT_BUFFER_DATA_PLACEMENT_ALIGNMENT,
            constantsOffset
            ));

    // Create vertex buffer views for the new binding model. 
    // Create constant buffer views for the new binding model. 
    // ...

    commandQueue->Execute(commandList);
    commandQueue->AdvanceFence();
}

HRESULT SuballocateFromHeap(SIZE_T uSize, UINT uAlign)
{
    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Free up resources for frames processed by GPU; see Figure 2.
        UINT lastCompletedFrame = commandQueue->GetLastCompletedFence();
        FreeUpMemoryUntilFrame( lastCompletedFrame );

        while ( NOT_SUFFICIENT_MEMORY(uSize, uAlign)
            && !frameOffsetQueue.empty() )
        {
            // Block until a new frame is processed by GPU, then free up more memory; see Figure 3.
            UINT nextGPUFrame = frameOffsetQueue.front().frameIndex;
            commandQueue->SetEventOnFenceCompletion(nextGPUFrame, hEvent);
            WaitForSingleObject(hEvent, INFINITE);
            FreeUpMemoryUntilFrame( nextGPUFrame );
        }
    }

    if (NOT_SUFFICIENT_MEMORY(uSize, uAlign))
    {
        // Apps need to create a new Heap that is large enough for this resource.
        return E_HEAPNOTLARGEENOUGH;
    }
    else
    {
        // Update current data pointer for the new resource.
        m_pDataCur = reinterpret_cast<UINT8*>(
            Align(reinterpret_cast<SIZE_T>(m_pHDataCur), uAlign)
            );

        // Update frame offset queue if this is the first resource for a new frame; see Figure 4.
        UINT currentFrame = commandQueue->GetCurrentFence();
        if ( frameOffsetQueue.empty()
            || frameOffsetQueue.back().frameIndex < currentFrame )
        {
            FrameResourceOffset offset = {currentFrame, m_pDataCur};
            frameOffsetQueue.push(offset);
        }

        return S_OK;
    }
}

void FreeUpMemoryUntilFrame(UINT lastCompletedFrame)
{
    while ( !frameOffsetQueue.empty() 
        && frameOffsetQueue.first().frameIndex <= lastCompletedFrame )
    {
        frameOffsetQueue.pop();
    }
}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[在緩衝區內進行子分配](large-buffers.md)
</dt> </dl>

 

 




