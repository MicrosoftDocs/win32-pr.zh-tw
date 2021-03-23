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
# <a name="fence-based-resource-management"></a><span data-ttu-id="f8bcf-104">Fence-Based 資源管理</span><span class="sxs-lookup"><span data-stu-id="f8bcf-104">Fence-Based Resource Management</span></span>

<span data-ttu-id="f8bcf-105">示範如何透過延伸來追蹤 GPU 進度，以管理資源資料的生命週期。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-105">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="f8bcf-106">記憶體可以有效地重複使用，以管理記憶體中可用空間的可用性，例如在上傳堆積的通道緩衝區執行中。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-106">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span>

-   [<span data-ttu-id="f8bcf-107">信號緩衝區案例</span><span class="sxs-lookup"><span data-stu-id="f8bcf-107">Ring buffer scenario</span></span>](#ring-buffer-scenario)
-   [<span data-ttu-id="f8bcf-108">信號緩衝區範例</span><span class="sxs-lookup"><span data-stu-id="f8bcf-108">Ring buffer sample</span></span>](#ring-buffer-sample)
-   [<span data-ttu-id="f8bcf-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8bcf-109">Related topics</span></span>](#related-topics)

## <a name="ring-buffer-scenario"></a><span data-ttu-id="f8bcf-110">信號緩衝區案例</span><span class="sxs-lookup"><span data-stu-id="f8bcf-110">Ring buffer scenario</span></span>

<span data-ttu-id="f8bcf-111">以下是應用程式在上傳堆積記憶體時遇到罕見需求的範例。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-111">The following is an example in which an app experiences a rare demand for upload heap memory.</span></span>

<span data-ttu-id="f8bcf-112">信號緩衝區是管理上傳堆積的一種方式。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-112">A ring buffer is one way to manage an upload heap.</span></span> <span data-ttu-id="f8bcf-113">信號緩衝區會保存接下來幾個框架所需的資料。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-113">The ring buffer holds data required for the next few frames.</span></span> <span data-ttu-id="f8bcf-114">應用程式會維護目前的資料輸入指標，以及用來記錄每個畫面格和起始該框架之資源資料位移的框架位移佇列。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-114">The app maintains a current data input pointer, and a frame offset queue to record each frame and starting offset of resource data for that frame.</span></span>

<span data-ttu-id="f8bcf-115">應用程式會根據緩衝區建立環形緩衝區，以將資料上傳至每個框架的 GPU。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-115">An app creates a ring-buffer based upon a buffer to upload data to the GPU for each frame.</span></span> <span data-ttu-id="f8bcf-116">目前已轉譯框架2，信號緩衝區會在框架4的資料周圍換行，而第5幀所需的所有資料都存在，而框架6所需的大型常數緩衝區則需要進行子配置。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-116">Currently frame 2 has been rendered, the ring buffer wraps around the data for frame 4, all the data required for frame 5 is present, and a large constant buffer required for frame 6 needs to be sub-allocated.</span></span>

<span data-ttu-id="f8bcf-117">**圖 1** ：應用程式嘗試對常數緩衝區進行子配置，但是找不到足夠的可用記憶體。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-117">**Figure 1** : the app tries to sub-allocate for the constant buffer, but finds insufficient free memory.</span></span>

![此信號緩衝區中的可用記憶體不足](images/ring-buffer-1.png)

<span data-ttu-id="f8bcf-119">**圖 2** ：透過隔離輪詢，應用程式會探索到畫面格3已轉譯，接著會更新框架位移佇列，而信號緩衝區的目前狀態則如下所示，但可用記憶體仍不夠大，無法容納常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-119">**Figure 2** : through fence polling, the app discovers that frame 3 has been rendered, the frame offset queue is then updated, and the current state of the ring buffer follows - however, free memory is still not large enough to accommodate the constant buffer.</span></span>

![在畫面格3轉譯之後仍沒有足夠的記憶體](images/ring-buffer-2.png)

<span data-ttu-id="f8bcf-121">**圖 3** ：在此情況下，CPU 區塊本身 (透過範圍等候) ，直到已轉譯框架4為止，這會釋出針對框架4所配置的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-121">**Figure 3** : given the situation, the CPU blocks itself (via fence waiting) until frame 4 has been rendered, which frees up the memory sub-allocated for frame 4.</span></span>

![轉譯畫面格4釋出更多信號緩衝區](images/ring-buffer-3.png)

<span data-ttu-id="f8bcf-123">**圖 4** ：現在可用記憶體夠大，足以容納常數緩衝區，而子配置成功;應用程式會將大型常數緩衝區資料複製到先前由資源資料用於框架3和4的記憶體。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-123">**Figure 4** : now free memory is large enough for the constant buffer, and sub-allocation succeeds; the app copies the big constant buffer data to memory previously used by resource data for both frames 3 and 4.</span></span> <span data-ttu-id="f8bcf-124">最後會更新目前的輸入指標。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-124">The current input pointer is finally updated.</span></span>

![信號緩衝區中的框架6現在有空間](images/ring-buffer-4.png)

<span data-ttu-id="f8bcf-126">如果應用程式會執行信號緩衝區，信號緩衝區必須夠大，才能應付資源資料大小的較糟案例。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-126">If an app implements a ring buffer, the ring buffer must be large enough to cope with the worse-case scenario of the sizes of resource data.</span></span>

## <a name="ring-buffer-sample"></a><span data-ttu-id="f8bcf-127">信號緩衝區範例</span><span class="sxs-lookup"><span data-stu-id="f8bcf-127">Ring buffer sample</span></span>

<span data-ttu-id="f8bcf-128">下列範例程式碼示範如何管理信號緩衝區，並注意處理隔離輪詢和等候的子配置常式。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-128">The following sample code shows how a ring buffer can be managed, paying attention to the sub-allocation routine that handles fence polling and waiting.</span></span> <span data-ttu-id="f8bcf-129">為了簡單起見，此範例使用的記憶體不足，無法 \_ \_ 隱藏「在堆積中找不到足夠的可用記憶體」的詳細資料，因為該邏輯 (根據 *m \_ PDataCur* ，而) *FrameOffsetQueue* 內的位移與堆積或圍牆沒有緊密關聯。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-129">For simplicity, the sample uses NOT\_SUFFICIENT\_MEMORY to hide the details of “not sufficient free memory found in the heap” since that logic (based on *m\_pDataCur* and offsets inside *FrameOffsetQueue*) is not tightly related to heaps or fences.</span></span> <span data-ttu-id="f8bcf-130">此範例已簡化，以犧牲畫面播放速率，而不是記憶體使用率。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-130">The sample is simplified to sacrifice frame rate instead of memory utilization.</span></span>

<span data-ttu-id="f8bcf-131">請注意，通道緩衝區支援應該是常見的案例;不過，堆積設計不會排除其他使用方式，例如命令清單參數化和重複使用。</span><span class="sxs-lookup"><span data-stu-id="f8bcf-131">Note that, ring-buffer support is expected to be a popular scenario; however, the heap design does not preclude other usage, such as command list parameterization and re-use.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f8bcf-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="f8bcf-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8bcf-133">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="f8bcf-133">**ID3D12Fence**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence)
</dt> <dt>

[<span data-ttu-id="f8bcf-134">在緩衝區內進行子分配</span><span class="sxs-lookup"><span data-stu-id="f8bcf-134">Suballocation Within Buffers</span></span>](large-buffers.md)
</dt> </dl>

 

 




