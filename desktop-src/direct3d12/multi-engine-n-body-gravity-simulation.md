---
title: 多引擎 n-內文重力模擬
description: D3D12nBodyGravity 範例會示範如何以非同步方式執行計算工作。
ms.assetid: B20C5575-0616-43F7-9AC9-5F802E5597B5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60782519de6f655882717c4ea657668129a6ce3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548373"
---
# <a name="multi-engine-n-body-gravity-simulation"></a><span data-ttu-id="08f80-103">多引擎 n-內文重力模擬</span><span class="sxs-lookup"><span data-stu-id="08f80-103">Multi-engine n-body gravity simulation</span></span>

<span data-ttu-id="08f80-104">**D3D12nBodyGravity** 範例會示範如何以非同步方式執行計算工作。</span><span class="sxs-lookup"><span data-stu-id="08f80-104">The **D3D12nBodyGravity** sample demonstrates how to do compute work asynchronously.</span></span> <span data-ttu-id="08f80-105">此範例會使用計算命令佇列來旋轉多個執行緒，並在執行 n 主體引力模擬的 GPU 上排程計算工作。</span><span class="sxs-lookup"><span data-stu-id="08f80-105">The sample spins up a number of threads each with a compute command queue and schedules compute work on the GPU that performs an n-body gravity simulation.</span></span> <span data-ttu-id="08f80-106">每個執行緒會在已滿位置和速度資料的兩個緩衝區上運作。</span><span class="sxs-lookup"><span data-stu-id="08f80-106">Each thread operates on two buffers full of position and velocity data.</span></span> <span data-ttu-id="08f80-107">在每個反復專案中，計算著色器會從一個緩衝區讀取目前的位置和速度資料，然後將下一個反覆運算寫入至另一個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="08f80-107">With each iteration, the compute shader reads the current position and velocity data from one buffer and writes the next iteration into the other buffer.</span></span> <span data-ttu-id="08f80-108">當反復專案完成時，計算著色器會交換哪個緩衝區是讀取位置/速度資料的 SRV，以及藉由變更每個緩衝區上的資源狀態來寫入位置/速度更新的 UAV。</span><span class="sxs-lookup"><span data-stu-id="08f80-108">When the iteration completes, the compute shader swaps which buffer is the SRV for reading position/velocity data and which is the UAV for writing position/velocity updates by changing the resource state on each buffer.</span></span>

-   [<span data-ttu-id="08f80-109">建立根簽章</span><span class="sxs-lookup"><span data-stu-id="08f80-109">Create the root signatures</span></span>](#create-the-root-signatures)
-   [<span data-ttu-id="08f80-110">建立 SRV 和 UAV 緩衝區</span><span class="sxs-lookup"><span data-stu-id="08f80-110">Create the SRV and UAV buffers</span></span>](#create-the-srv-and-uav-buffers)
-   [<span data-ttu-id="08f80-111">建立 CBV 和頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="08f80-111">Create the CBV and vertex buffers</span></span>](#create-the-cbv-and-vertex-buffers)
-   [<span data-ttu-id="08f80-112">同步處理轉譯和計算執行緒</span><span class="sxs-lookup"><span data-stu-id="08f80-112">Synchronize the rendering and compute threads</span></span>](#synchronize-the-rendering-and-compute-threads)
-   [<span data-ttu-id="08f80-113">執行範例</span><span class="sxs-lookup"><span data-stu-id="08f80-113">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="08f80-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="08f80-114">Related topics</span></span>](#related-topics)

## <a name="create-the-root-signatures"></a><span data-ttu-id="08f80-115">建立根簽章</span><span class="sxs-lookup"><span data-stu-id="08f80-115">Create the root signatures</span></span>

<span data-ttu-id="08f80-116">我們一開始會在 **LoadAssets** 方法中建立圖形和計算根簽章。</span><span class="sxs-lookup"><span data-stu-id="08f80-116">We start out by creating both a graphics and a compute root signature, in the **LoadAssets** method.</span></span> <span data-ttu-id="08f80-117">這兩個根簽章都有 (CBV) 的根常數緩衝區視圖，以及 (SRV) 描述中繼資料表的著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="08f80-117">Both root signatures have a root constant buffer view (CBV) and a shader resource view (SRV) descriptor table.</span></span> <span data-ttu-id="08f80-118">計算根簽章也有未排序的存取視圖 (UAV) 描述中繼資料表。</span><span class="sxs-lookup"><span data-stu-id="08f80-118">The compute root signature also has an unordered access view (UAV) descriptor table.</span></span>

``` syntax
 // Create the root signatures.
       {
              CD3DX12_DESCRIPTOR_RANGE ranges[2];
              ranges[0].Init(D3D12_DESCRIPTOR_RANGE_TYPE_SRV, 1, 0);
              ranges[1].Init(D3D12_DESCRIPTOR_RANGE_TYPE_UAV, 1, 0);

              CD3DX12_ROOT_PARAMETER rootParameters[RootParametersCount];
              rootParameters[RootParameterCB].InitAsConstantBufferView(0, 0, D3D12_SHADER_VISIBILITY_ALL);
              rootParameters[RootParameterSRV].InitAsDescriptorTable(1, &ranges[0], D3D12_SHADER_VISIBILITY_VERTEX);
              rootParameters[RootParameterUAV].InitAsDescriptorTable(1, &ranges[1], D3D12_SHADER_VISIBILITY_ALL);

              // The rendering pipeline does not need the UAV parameter.
              CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
              rootSignatureDesc.Init(_countof(rootParameters) - 1, rootParameters, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

              ComPtr<ID3DBlob> signature;
              ComPtr<ID3DBlob> error;
              ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

              // Create compute signature. Must change visibility for the SRV.
              rootParameters[RootParameterSRV].ShaderVisibility = D3D12_SHADER_VISIBILITY_ALL;

              CD3DX12_ROOT_SIGNATURE_DESC computeRootSignatureDesc(_countof(rootParameters), rootParameters, 0, nullptr);
              ThrowIfFailed(D3D12SerializeRootSignature(&computeRootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));

              ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_computeRootSignature)));
       }
```



| <span data-ttu-id="08f80-119">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="08f80-119">Call flow</span></span>                                                             | <span data-ttu-id="08f80-120">參數</span><span class="sxs-lookup"><span data-stu-id="08f80-120">Parameters</span></span>                                                            |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="08f80-121">**CD3DX12 \_ 描述元 \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="08f80-121">**CD3DX12\_DESCRIPTOR\_RANGE**</span></span>](cd3dx12-descriptor-range.md)        | [<span data-ttu-id="08f80-122">**D3D12 \_ 描述項 \_ 範圍 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="08f80-122">**D3D12\_DESCRIPTOR\_RANGE\_TYPE**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_descriptor_range_type) |
| [<span data-ttu-id="08f80-123">**CD3DX12 \_ 根 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="08f80-123">**CD3DX12\_ROOT\_PARAMETER**</span></span>](cd3dx12-root-parameter.md)            | [<span data-ttu-id="08f80-124">**D3D12 \_ 著色器 \_ 可見度**</span><span class="sxs-lookup"><span data-stu-id="08f80-124">**D3D12\_SHADER\_VISIBILITY**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_shader_visibility)          |
| [<span data-ttu-id="08f80-125">**CD3DX12 \_ 根目錄 \_ 簽名 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="08f80-125">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) | [<span data-ttu-id="08f80-126">**D3D12 \_ 根簽章 \_ \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="08f80-126">**D3D12\_ROOT\_SIGNATURE\_FLAGS**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_root_signature_flags)   |
| <span data-ttu-id="08f80-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08f80-127">[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))</span></span>                                   |                                                                       |
| [<span data-ttu-id="08f80-128">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="08f80-128">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="08f80-129">**D3D \_ 根簽章 \_ \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="08f80-129">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="08f80-130">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="08f80-130">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |
| [<span data-ttu-id="08f80-131">**CD3DX12 \_ 根目錄 \_ 簽名 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="08f80-131">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md) |                                                                       |
| [<span data-ttu-id="08f80-132">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="08f80-132">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)    | [<span data-ttu-id="08f80-133">**D3D \_ 根簽章 \_ \_ 版本**</span><span class="sxs-lookup"><span data-stu-id="08f80-133">**D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d_root_signature_version)   |
| [<span data-ttu-id="08f80-134">**CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="08f80-134">**CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)       |                                                                       |



 

## <a name="create-the-srv-and-uav-buffers"></a><span data-ttu-id="08f80-135">建立 SRV 和 UAV 緩衝區</span><span class="sxs-lookup"><span data-stu-id="08f80-135">Create the SRV and UAV buffers</span></span>

<span data-ttu-id="08f80-136">SRV 和 UAV 緩衝區是由位置和速度資料的陣列所組成。</span><span class="sxs-lookup"><span data-stu-id="08f80-136">The SRV and UAV buffers consist of an array of position and velocity data.</span></span>

``` syntax
 // Position and velocity data for the particles in the system.
       // Two buffers full of Particle data are utilized in this sample.
       // The compute thread alternates writing to each of them.
       // The render thread renders using the buffer that is not currently
       // in use by the compute shader.
       struct Particle
       {
              XMFLOAT4 position;
              XMFLOAT4 velocity;
       };
```



| <span data-ttu-id="08f80-137">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="08f80-137">Call flow</span></span>                       | <span data-ttu-id="08f80-138">參數</span><span class="sxs-lookup"><span data-stu-id="08f80-138">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="08f80-139">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="08f80-139">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

## <a name="create-the-cbv-and-vertex-buffers"></a><span data-ttu-id="08f80-140">建立 CBV 和頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="08f80-140">Create the CBV and vertex buffers</span></span>

<span data-ttu-id="08f80-141">針對圖形管線，CBV 是一個 **結構** ，其中包含幾何著色器所使用的兩個矩陣。</span><span class="sxs-lookup"><span data-stu-id="08f80-141">For the graphics pipeline, the CBV is a **struct** containing two matrices used by the geometry shader.</span></span> <span data-ttu-id="08f80-142">幾何著色器會取得系統中每個物件的位置，並產生四個，以使用這些矩陣來表示它。</span><span class="sxs-lookup"><span data-stu-id="08f80-142">The geometry shader takes the position of each particle in the system and generates a quad to represent it using these matrices.</span></span>

``` syntax
 struct ConstantBufferGS
       {
              XMMATRIX worldViewProjection;
              XMMATRIX inverseView;

              // Constant buffers are 256-byte aligned in GPU memory. Padding is added
              // for convenience when computing the struct's size.
              float padding[32];
       };
```



| <span data-ttu-id="08f80-143">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="08f80-143">Call flow</span></span>                       | <span data-ttu-id="08f80-144">參數</span><span class="sxs-lookup"><span data-stu-id="08f80-144">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="08f80-145">**XMMATRIX**</span><span class="sxs-lookup"><span data-stu-id="08f80-145">**XMMATRIX**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) |            |



 

<span data-ttu-id="08f80-146">因此，頂點著色器所使用的頂點緩衝區實際上不包含任何位置資料。</span><span class="sxs-lookup"><span data-stu-id="08f80-146">As a result, the vertex buffer used by the vertex shader actually does not contain any positional data.</span></span>

``` syntax
 // "Vertex" definition for particles. Triangle vertices are generated 
       // by the geometry shader. Color data will be assigned to those 
       // vertices via this struct.
       struct ParticleVertex
       {
              XMFLOAT4 color;
       };
```



| <span data-ttu-id="08f80-147">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="08f80-147">Call flow</span></span>                       | <span data-ttu-id="08f80-148">參數</span><span class="sxs-lookup"><span data-stu-id="08f80-148">Parameters</span></span> |
|---------------------------------|------------|
| [<span data-ttu-id="08f80-149">**XMFLOAT4**</span><span class="sxs-lookup"><span data-stu-id="08f80-149">**XMFLOAT4**</span></span>](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) |            |



 

<span data-ttu-id="08f80-150">針對計算管線，CBV 是一種 **結構** ，其中包含計算著色器中 n 主體重力模擬所使用的一些常數。</span><span class="sxs-lookup"><span data-stu-id="08f80-150">For the compute pipeline, the CBV is a **struct** containing some constants used by the n-body gravity simulation in the compute shader.</span></span>

``` syntax
 struct ConstantBufferCS
       {
              UINT param[4];
              float paramf[4];
       };
```

## <a name="synchronize-the-rendering-and-compute-threads"></a><span data-ttu-id="08f80-151">同步處理轉譯和計算執行緒</span><span class="sxs-lookup"><span data-stu-id="08f80-151">Synchronize the rendering and compute threads</span></span>

<span data-ttu-id="08f80-152">緩衝區全部初始化之後，轉譯和計算工作就會開始。</span><span class="sxs-lookup"><span data-stu-id="08f80-152">After the buffers are all initialized, the rendering and compute work will begin.</span></span> <span data-ttu-id="08f80-153">計算執行緒會在其逐一查看模擬時，于 SRV 和 UAV 之間來回變更兩個位置/速度緩衝區的狀態，而且轉譯執行緒必須確保它會在在 SRV 上操作的圖形管線上進行處理。</span><span class="sxs-lookup"><span data-stu-id="08f80-153">The compute thread will be changing the state of the two position/velocity buffers back and forth between SRV and UAV as it iterates on the simulation, and the rendering thread needs to ensure that it schedules work on the graphics pipeline that operates on the SRV.</span></span> <span data-ttu-id="08f80-154">用來同步處理兩個緩衝區的存取權。</span><span class="sxs-lookup"><span data-stu-id="08f80-154">Fences are used to synchronize access to the two buffers.</span></span>

<span data-ttu-id="08f80-155">在轉譯執行緒上：</span><span class="sxs-lookup"><span data-stu-id="08f80-155">On the Render thread:</span></span>

``` syntax
// Render the scene.
void D3D12nBodyGravity::OnRender()
{
       // Let the compute thread know that a new frame is being rendered.
       for (int n = 0; n < ThreadCount; n++)
       {
              InterlockedExchange(&m_renderContextFenceValues[n], m_renderContextFenceValue);
       }

       // Compute work must be completed before the frame can render or else the SRV 
       // will be in the wrong state.
       for (UINT n = 0; n < ThreadCount; n++)
       {
              UINT64 threadFenceValue = InterlockedGetValue(&m_threadFenceValues[n]);
              if (m_threadFences[n]->GetCompletedValue() < threadFenceValue)
              {
                     // Instruct the rendering command queue to wait for the current 
                     // compute work to complete.
                     ThrowIfFailed(m_commandQueue->Wait(m_threadFences[n].Get(), threadFenceValue));
              }
       }

       // Record all the commands we need to render the scene into the command list.
       PopulateCommandList();

       // Execute the command list.
       ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
       m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

       // Present the frame.
       ThrowIfFailed(m_swapChain->Present(0, 0));

       MoveToNextFrame();
}
```



| <span data-ttu-id="08f80-156">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="08f80-156">Call flow</span></span>                                                              | <span data-ttu-id="08f80-157">參數</span><span class="sxs-lookup"><span data-stu-id="08f80-157">Parameters</span></span> |
|------------------------------------------------------------------------|------------|
| [<span data-ttu-id="08f80-158">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="08f80-158">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                  |            |
| [<span data-ttu-id="08f80-159">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="08f80-159">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)           |            |
| [<span data-ttu-id="08f80-160">**GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="08f80-160">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)             |            |
| [<span data-ttu-id="08f80-161">**等候**</span><span class="sxs-lookup"><span data-stu-id="08f80-161">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                |            |
| [<span data-ttu-id="08f80-162">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="08f80-162">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [<span data-ttu-id="08f80-163">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="08f80-163">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [<span data-ttu-id="08f80-164">**IDXGISwapChain1::Present1**</span><span class="sxs-lookup"><span data-stu-id="08f80-164">**IDXGISwapChain1::Present1**</span></span>](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

<span data-ttu-id="08f80-165">為了簡化範例一點，計算執行緒會先等候 GPU 完成每個反復專案，再排程任何更多計算工作。</span><span class="sxs-lookup"><span data-stu-id="08f80-165">To simplify the sample a bit, the compute thread waits for the GPU to complete each iteration before scheduling any more compute work.</span></span> <span data-ttu-id="08f80-166">在實務上，應用程式可能會想要讓計算佇列保持完整，以達到 GPU 的最大效能。</span><span class="sxs-lookup"><span data-stu-id="08f80-166">In practice, applications will likely want to keep the compute queue full to achieve maximum performance from the GPU.</span></span>

<span data-ttu-id="08f80-167">在計算執行緒上：</span><span class="sxs-lookup"><span data-stu-id="08f80-167">On the Compute thread:</span></span>

``` syntax
DWORD D3D12nBodyGravity::AsyncComputeThreadProc(int threadIndex)
{
       ID3D12CommandQueue* pCommandQueue = m_computeCommandQueue[threadIndex].Get();
       ID3D12CommandAllocator* pCommandAllocator = m_computeAllocator[threadIndex].Get();
       ID3D12GraphicsCommandList* pCommandList = m_computeCommandList[threadIndex].Get();
       ID3D12Fence* pFence = m_threadFences[threadIndex].Get();

       while (0 == InterlockedGetValue(&m_terminating))
       {
              // Run the particle simulation.
              Simulate(threadIndex);

              // Close and execute the command list.
              ThrowIfFailed(pCommandList->Close());
              ID3D12CommandList* ppCommandLists[] = { pCommandList };

              pCommandQueue->ExecuteCommandLists(1, ppCommandLists);

              // Wait for the compute shader to complete the simulation.
              UINT64 threadFenceValue = InterlockedIncrement(&m_threadFenceValues[threadIndex]);
              ThrowIfFailed(pCommandQueue->Signal(pFence, threadFenceValue));
              ThrowIfFailed(pFence->SetEventOnCompletion(threadFenceValue, m_threadFenceEvents[threadIndex]));
              WaitForSingleObject(m_threadFenceEvents[threadIndex], INFINITE);

              // Wait for the render thread to be done with the SRV so that
              // the next frame in the simulation can run.
              UINT64 renderContextFenceValue = InterlockedGetValue(&m_renderContextFenceValues[threadIndex]);
              if (m_renderContextFence->GetCompletedValue() < renderContextFenceValue)
              {
                     ThrowIfFailed(pCommandQueue->Wait(m_renderContextFence.Get(), renderContextFenceValue));
                     InterlockedExchange(&m_renderContextFenceValues[threadIndex], 0);
              }

              // Swap the indices to the SRV and UAV.
              m_srvIndex[threadIndex] = 1 - m_srvIndex[threadIndex];

              // Prepare for the next frame.
              ThrowIfFailed(pCommandAllocator->Reset());
              ThrowIfFailed(pCommandList->Reset(pCommandAllocator, m_computeState.Get()));
       }

       return 0;
}
```



| <span data-ttu-id="08f80-168">呼叫流程</span><span class="sxs-lookup"><span data-stu-id="08f80-168">Call flow</span></span>                                                                   | <span data-ttu-id="08f80-169">參數</span><span class="sxs-lookup"><span data-stu-id="08f80-169">Parameters</span></span> |
|-----------------------------------------------------------------------------|------------|
| [<span data-ttu-id="08f80-170">**ID3D12CommandQueue**</span><span class="sxs-lookup"><span data-stu-id="08f80-170">**ID3D12CommandQueue**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)                            |            |
| [<span data-ttu-id="08f80-171">**ID3D12CommandAllocator**</span><span class="sxs-lookup"><span data-stu-id="08f80-171">**ID3D12CommandAllocator**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator)                    |            |
| [<span data-ttu-id="08f80-172">**ID3D12GraphicsCommandList**</span><span class="sxs-lookup"><span data-stu-id="08f80-172">**ID3D12GraphicsCommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)              |            |
| [<span data-ttu-id="08f80-173">**ID3D12Fence**</span><span class="sxs-lookup"><span data-stu-id="08f80-173">**ID3D12Fence**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)                                          |            |
| [<span data-ttu-id="08f80-174">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="08f80-174">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="08f80-175">**關閉**</span><span class="sxs-lookup"><span data-stu-id="08f80-175">**Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)                            |            |
| [<span data-ttu-id="08f80-176">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="08f80-176">**ID3D12CommandList**</span></span>](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist)                              |            |
| [<span data-ttu-id="08f80-177">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="08f80-177">**ExecuteCommandLists**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)       |            |
| [<span data-ttu-id="08f80-178">**InterlockedIncrement**</span><span class="sxs-lookup"><span data-stu-id="08f80-178">**InterlockedIncrement**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedincrement)                     |            |
| [<span data-ttu-id="08f80-179">**信號**</span><span class="sxs-lookup"><span data-stu-id="08f80-179">**Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)                                 |            |
| [<span data-ttu-id="08f80-180">**SetEventOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="08f80-180">**SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)            |            |
| [<span data-ttu-id="08f80-181">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="08f80-181">**WaitForSingleObject**</span></span>](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)                         |            |
| [<span data-ttu-id="08f80-182">**InterlockedGetValue**</span><span class="sxs-lookup"><span data-stu-id="08f80-182">**InterlockedGetValue**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedcompareexchange)                |            |
| [<span data-ttu-id="08f80-183">**GetCompletedValue**</span><span class="sxs-lookup"><span data-stu-id="08f80-183">**GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)                  |            |
| [<span data-ttu-id="08f80-184">**等候**</span><span class="sxs-lookup"><span data-stu-id="08f80-184">**Wait**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait)                                     |            |
| [<span data-ttu-id="08f80-185">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="08f80-185">**InterlockedExchange**</span></span>](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-interlockedexchange)                       |            |
| [<span data-ttu-id="08f80-186">**ID3D12CommandAllocator：： Reset**</span><span class="sxs-lookup"><span data-stu-id="08f80-186">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)       |            |
| [<span data-ttu-id="08f80-187">**ID3D12GraphicsCommandList：： Reset**</span><span class="sxs-lookup"><span data-stu-id="08f80-187">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset) |            |



 

## <a name="run-the-sample"></a><span data-ttu-id="08f80-188">執行範例</span><span class="sxs-lookup"><span data-stu-id="08f80-188">Run the sample</span></span>

![最後 n 個主體重力模擬的螢幕擷取畫面](images/nbodygravity.png)

## <a name="related-topics"></a><span data-ttu-id="08f80-190">相關主題</span><span class="sxs-lookup"><span data-stu-id="08f80-190">Related topics</span></span>

[<span data-ttu-id="08f80-191">D3D12 程式碼逐步解說-解說</span><span class="sxs-lookup"><span data-stu-id="08f80-191">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)

[<span data-ttu-id="08f80-192">多引擎同步處理</span><span class="sxs-lookup"><span data-stu-id="08f80-192">Multi-engine synchronization</span></span>](./user-mode-heap-synchronization.md)