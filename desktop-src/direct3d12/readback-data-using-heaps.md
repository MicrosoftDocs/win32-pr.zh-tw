---
title: 透過緩衝區讀回資料
description: 若要從 GPU 讀回資料 (例如，若要捕捉螢幕擷取畫面) ，您可以使用 readback 堆積。
ms.assetid: 2F515B2C-3317-4AA8-81E1-7762ED895F77
ms.localizationpriority: high
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: 752d97d517a48a38adabc7c8fe51d11d47c1d8d3
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548429"
---
# <a name="read-back-data-via-a-buffer"></a><span data-ttu-id="8c460-103">透過緩衝區讀回資料</span><span class="sxs-lookup"><span data-stu-id="8c460-103">Read back data via a buffer</span></span>

<span data-ttu-id="8c460-104">若要從 GPU 讀回資料 (例如，若要捕捉螢幕擷取畫面) ，您可以使用 readback 堆積。</span><span class="sxs-lookup"><span data-stu-id="8c460-104">To read back data from the GPU (for example, to capture a screen shot), you use a readback heap.</span></span> <span data-ttu-id="8c460-105">這項技術與透過 [緩衝區上傳紋理資料](upload-and-readback-of-texture-data.md)有關，但有幾項差異。</span><span class="sxs-lookup"><span data-stu-id="8c460-105">This technique is related to [Uploading texture data via a buffer](upload-and-readback-of-texture-data.md), with a few differences.</span></span>

- <span data-ttu-id="8c460-106">若要讀回資料，您可以建立 **D3D12_HEAP_TYPE** 設定為 [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)的堆積，而不是 **D3D12_HEAP_TYPE_UPLOAD**。</span><span class="sxs-lookup"><span data-stu-id="8c460-106">To read back data, you create a heap with the **D3D12_HEAP_TYPE** set to [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type), instead of **D3D12_HEAP_TYPE_UPLOAD**.</span></span>
- <span data-ttu-id="8c460-107">讀取回堆積上的資源必須一律是 **D3D12_RESOURCE_DIMENSION_BUFFER**。</span><span class="sxs-lookup"><span data-stu-id="8c460-107">The resource on the read-back heap must always be a **D3D12_RESOURCE_DIMENSION_BUFFER**.</span></span>
- <span data-ttu-id="8c460-108">您可以使用隔離來偵測當 GPU 完成將資料寫入至輸出緩衝區) 時， (處理框架何時完成處理。</span><span class="sxs-lookup"><span data-stu-id="8c460-108">You use a fence to detect when the GPU completes processing a frame (when it is done writing data into your output buffer).</span></span> <span data-ttu-id="8c460-109">這點很重要，因為 [**ID3D12Resource：： Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) 方法不會與 GPU 同步 (相反地，Direct3D 11 對等的 *會* 同步處理) 。</span><span class="sxs-lookup"><span data-stu-id="8c460-109">This is important, because the [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) method doesn't synchronize with the GPU (conversely, the Direct3D 11 equivalent *does* synchronize).</span></span> <span data-ttu-id="8c460-110">Direct3D 12 **Map** 呼叫的行為就如同您使用 NO_OVERWRITE 旗標呼叫了 direct3d 11 對等專案。</span><span class="sxs-lookup"><span data-stu-id="8c460-110">Direct3D 12 **Map** calls behave as if you called the Direct3D 11 equivalent with the NO_OVERWRITE flag.</span></span>
- <span data-ttu-id="8c460-111">資料就緒之後 (包括任何必要的資源屏障) ，請呼叫 [**ID3D12Resource：： Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) ，讓 CPU 可以看見 readback 資料。</span><span class="sxs-lookup"><span data-stu-id="8c460-111">After the data is ready (including any necessary resource barrier), call [**ID3D12Resource::Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) to make the readback data visible to the CPU.</span></span>

## <a name="code-example"></a><span data-ttu-id="8c460-112">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="8c460-112">Code example</span></span>

<span data-ttu-id="8c460-113">下列程式碼範例顯示透過緩衝區將資料從 GPU 讀入 CPU 的程式的一般大綱。</span><span class="sxs-lookup"><span data-stu-id="8c460-113">The code example below shows the general outline of the process of reading back data from the GPU to the CPU via a buffer.</span></span>

```cppwinrt

// The output buffer (created below) is on a default heap, so only the GPU can access it.

D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
D3D12_RESOURCE_DESC outputBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize, D3D12_RESOURCE_FLAG_ALLOW_UNORDERED_ACCESS) };
winrt::com_ptr<::ID3D12Resource> outputBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &defaultHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &outputBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(outputBuffer),
    outputBuffer.put_void()));

// The readback buffer (created below) is on a readback heap, so that the CPU can access it.

D3D12_HEAP_PROPERTIES readbackHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_READBACK) };
D3D12_RESOURCE_DESC readbackBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(outputBufferSize) };
winrt::com_ptr<::ID3D12Resource> readbackBuffer;
winrt::check_hresult(d3d12Device->CreateCommittedResource(
    &readbackHeapProperties,
    D3D12_HEAP_FLAG_NONE,
    &readbackBufferDesc,
    D3D12_RESOURCE_STATE_COPY_DEST,
    nullptr,
    __uuidof(readbackBuffer),
    readbackBuffer.put_void()));

{
    D3D12_RESOURCE_BARRIER outputBufferResourceBarrier
    {
        CD3DX12_RESOURCE_BARRIER::Transition(
            outputBuffer.get(),
            D3D12_RESOURCE_STATE_COPY_DEST,
            D3D12_RESOURCE_STATE_COPY_SOURCE)
    };
    commandList->ResourceBarrier(1, &outputBufferResourceBarrier);
}

commandList->CopyResource(readbackBuffer.get(), outputBuffer.get());

// Code goes here to close, execute (and optionally reset) the command list, and also
// to use a fence to wait for the command queue.

// The code below assumes that the GPU wrote FLOATs to the buffer.

D3D12_RANGE readbackBufferRange{ 0, outputBufferSize };
FLOAT * pReadbackBufferData{};
winrt::check_hresult(
    readbackBuffer->Map
    (
        0,
        &readbackBufferRange,
        reinterpret_cast<void**>(&pReadbackBufferData)
    )
);

// Code goes here to access the data via pReadbackBufferData.

D3D12_RANGE emptyRange{ 0, 0 };
readbackBuffer->Unmap
(
    0,
    &emptyRange
);
```

<span data-ttu-id="8c460-114">如需讀取轉譯目標材質並將其寫入磁片作為檔案的螢幕擷取畫面常式完整執行，請參閱適用于 DX12 之 [ScreenGrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp)的 *DirectX 工具套件*。</span><span class="sxs-lookup"><span data-stu-id="8c460-114">For a full implementation of a screenshot routine that reads the render target texture, and writes it to disk as a file, see *DirectX Tool Kit for DX12*'s [ScreenGrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c460-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c460-115">Related topics</span></span>

* [<span data-ttu-id="8c460-116">在緩衝區內進行子分配</span><span class="sxs-lookup"><span data-stu-id="8c460-116">Suballocation within a buffer</span></span>](large-buffers.md)
