---
title: D3D12 參考中的範例程式碼
description: 說明如何使用 Direct3D 12 檔中的範例程式碼。
ms.assetid: C2323482-D06D-43B7-9BDE-BFB9A6A6B70D
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d65dd8db64dd829a7a318717e44a64ea189c7a3
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "104548357"
---
# <a name="example-code-in-the-d3d12-reference"></a><span data-ttu-id="db1f8-103">D3D12 參考中的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="db1f8-103">Example Code in the D3D12 Reference</span></span>

<span data-ttu-id="db1f8-104">說明如何使用 Direct3D 12 檔中的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="db1f8-104">Explains the use of example code in the Direct3D 12 documentation.</span></span>

-   [<span data-ttu-id="db1f8-105">範例程式碼片段程式碼</span><span class="sxs-lookup"><span data-stu-id="db1f8-105">Example snippet code</span></span>](#example-snippet-code)
-   [<span data-ttu-id="db1f8-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="db1f8-106">Related topics</span></span>](#related-topics)

## <a name="example-snippet-code"></a><span data-ttu-id="db1f8-107">範例程式碼片段程式碼</span><span class="sxs-lookup"><span data-stu-id="db1f8-107">Example snippet code</span></span>

<span data-ttu-id="db1f8-108">Direct3D 12 參考中所顯示的範例程式碼無法編譯或可執行檔程式碼，它只是一個程式碼片段，提供 API 的呼叫範例。</span><span class="sxs-lookup"><span data-stu-id="db1f8-108">The example code shown in the Direct3D 12 reference is not compilable or run-able code, it is simply a snippet of code giving an example of how the API is called.</span></span> <span data-ttu-id="db1f8-109">某些範例會列出呼叫所使用的全域變數和類別成員，例如：</span><span class="sxs-lookup"><span data-stu-id="db1f8-109">Some examples list the global variables and class members used by the calls, for example:</span></span>

<span data-ttu-id="db1f8-110">全域管線物件。</span><span class="sxs-lookup"><span data-stu-id="db1f8-110">Global pipeline objects.</span></span>


```C++
D3D12_VIEWPORT m_viewport;
D3D12_RECT m_scissorRect;
ComPtr<IDXGISwapChain3> m_swapChain;
ComPtr<ID3D12Device> m_device;
ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
ComPtr<ID3D12CommandAllocator> m_commandAllocator;
ComPtr<ID3D12CommandQueue> m_commandQueue;
ComPtr<ID3D12RootSignature> m_rootSignature;
ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
ComPtr<ID3D12PipelineState> m_pipelineState;
ComPtr<ID3D12GraphicsCommandList> m_commandList;
UINT m_rtvDescriptorSize;
```



<span data-ttu-id="db1f8-111">填入命令清單。</span><span class="sxs-lookup"><span data-stu-id="db1f8-111">Populating command lists.</span></span>


```C++
// Command list allocators can only be reset when the associated 
// command lists have finished execution on the GPU; apps should use 
// fences to determine GPU execution progress.
ThrowIfFailed(m_commandAllocator->Reset());

// However, when ExecuteCommandList() is called on a particular command 
// list, that command list can then be reset at any time and must be before 
// re-recording.
ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

// Set necessary state.
m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
m_commandList->RSSetViewports(1, &m_viewport);
m_commandList->RSSetScissorRects(1, &m_scissorRect);

// Indicate that the back buffer will be used as a render target.
auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
m_commandList->ResourceBarrier(1, &barrier);

CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

// Record commands.
const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
m_commandList->DrawInstanced(3, 1, 0, 0);

// Indicate that the back buffer will now be used to present.
m_commandList->ResourceBarrier(1, &barrier);
barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
ThrowIfFailed(m_commandList->Close());
```



## <a name="related-topics"></a><span data-ttu-id="db1f8-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="db1f8-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db1f8-113">建立基本的 Direct3D 12 元件</span><span class="sxs-lookup"><span data-stu-id="db1f8-113">Creating a basic Direct3D 12 component</span></span>](creating-a-basic-direct3d-12-component.md)
</dt> <dt>

[<span data-ttu-id="db1f8-114">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="db1f8-114">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="db1f8-115">D3D12 程式碼逐步解說-解說</span><span class="sxs-lookup"><span data-stu-id="db1f8-115">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="db1f8-116">工作範例</span><span class="sxs-lookup"><span data-stu-id="db1f8-116">Working Samples</span></span>](working-samples.md)
</dt> </dl>

 

 




