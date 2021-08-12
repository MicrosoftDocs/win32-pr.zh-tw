---
title: 透過緩衝區讀回資料
description: 若要從 GPU 讀回資料 (例如，若要捕捉螢幕擷取畫面) ，您可以使用 readback 堆積。
ms.assetid: 2F515B2C-3317-4AA8-81E1-7762ED895F77
ms.localizationpriority: high
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: 56babd93ddd0f06ee331b19db4a4d8ba2dc5ecb314ec3d828e3e3f7c4f4f9a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300871"
---
# <a name="read-back-data-via-a-buffer"></a>透過緩衝區讀回資料

若要從 GPU 讀回資料 (例如，若要捕捉螢幕擷取畫面) ，您可以使用 readback 堆積。 這項技術與透過 [緩衝區上傳紋理資料](upload-and-readback-of-texture-data.md)有關，但有幾項差異。

- 若要讀回資料，您可以建立 **D3D12_HEAP_TYPE** 設定為 [D3D12_HEAP_TYPE_READBACK](/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_type)的堆積，而不是 **D3D12_HEAP_TYPE_UPLOAD**。
- 讀取回堆積上的資源必須一律是 **D3D12_RESOURCE_DIMENSION_BUFFER**。
- 您可以使用隔離來偵測當 GPU 完成將資料寫入至輸出緩衝區) 時， (處理框架何時完成處理。 這點很重要，因為 [**ID3D12Resource：： Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) 方法不會與 GPU 同步 (相反地，Direct3D 11 對等的 *會* 同步處理) 。 Direct3D 12 **Map** 呼叫的行為就如同您使用 NO_OVERWRITE 旗標呼叫了 direct3d 11 對等專案。
- 資料就緒之後 (包括任何必要的資源屏障) ，請呼叫 [**ID3D12Resource：： Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) ，讓 CPU 可以看見 readback 資料。

## <a name="code-example"></a>程式碼範例

下列程式碼範例顯示透過緩衝區將資料從 GPU 讀入 CPU 的程式的一般大綱。

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

如需讀取轉譯目標材質並將其寫入磁片作為檔案的螢幕擷取畫面常式完整執行，請參閱適用于 DX12 之 [ScreenGrab](https://github.com/microsoft/DirectXTK12/blob/master/Src/ScreenGrab.cpp)的 *DirectX 工具套件*。

## <a name="related-topics"></a>相關主題

* [在緩衝區內進行子分配](large-buffers.md)
