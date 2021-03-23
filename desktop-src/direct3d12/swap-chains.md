---
title: 交換鏈
description: 交換鏈會控制背景的緩衝區旋轉，形成圖形動畫的基礎。
ms.assetid: AABF5FDE-DB49-4B29-BC0E-032E0C7DF9EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbc7ec1b62ba620b42bc85c1c1f491ff7ba952d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/12/2021
ms.locfileid: "104548407"
---
# <a name="swap-chains"></a><span data-ttu-id="8d9ae-103">交換鏈</span><span class="sxs-lookup"><span data-stu-id="8d9ae-103">Swap Chains</span></span>

<span data-ttu-id="8d9ae-104">交換鏈會控制背景的緩衝區旋轉，形成圖形動畫的基礎。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-104">Swap chains control the back buffer rotation, forming the basis of graphics animation.</span></span>

## <a name="overview"></a><span data-ttu-id="8d9ae-105">概觀</span><span class="sxs-lookup"><span data-stu-id="8d9ae-105">Overview</span></span>

<span data-ttu-id="8d9ae-106">Direct3D 12 中交換鏈的程式設計模型與舊版 D3D 中的程式設計模型不同。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-106">The programming model for swap chains in Direct3D 12 is not identical to that in earlier versions of D3D.</span></span> <span data-ttu-id="8d9ae-107">現在不支援在 D3D10 和 D3D11 中提供的程式設計便利性，例如支援自動資源輪替。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-107">The programming convenience, for example, of supporting automatic resource rotation that was present in D3D10 and D3D11 is not now supported.</span></span> <span data-ttu-id="8d9ae-108">自動啟用資源輪替的應用程式，可在呈現的實際介面變更每個畫面時轉譯相同的 API 物件。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-108">Automatic resource rotation enabled apps to render the same API object while the actual surface being rendered changes each frame.</span></span> <span data-ttu-id="8d9ae-109">使用 Direct3D 12 變更交換鏈的行為，讓 Direct3D 12 的其他功能具有低 CPU 的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-109">The behavior of swap chains is changed with Direct3D 12 to enable other features of Direct3D 12 to have low CPU overhead.</span></span> <span data-ttu-id="8d9ae-110">不支援自動色彩索引鍵和取樣，但明顯的延展和旋轉仍是。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-110">Automatic color key and multisampling are not supported, although notably stretching and rotation still are.</span></span>

### <a name="buffer-lifetime"></a><span data-ttu-id="8d9ae-111">緩衝區存留期</span><span class="sxs-lookup"><span data-stu-id="8d9ae-111">Buffer lifetime</span></span>

<span data-ttu-id="8d9ae-112">您可以藉由確保交換鏈所擁有的一組緩衝區在交換鏈的存留期內不會變更，讓應用程式儲存參考緩衝區的預建描述項。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-112">Apps are allowed to store pre-created descriptors which reference back buffers This is enabled by ensuring that the set of buffers owned by a swap chain never changes for the lifetime of the swap chain.</span></span> <span data-ttu-id="8d9ae-113">在呼叫特定 Api 之前， [**IDXGISwapChain：： GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) 所傳回的緩衝區集不會變更：</span><span class="sxs-lookup"><span data-stu-id="8d9ae-113">The set of buffers returned by [**IDXGISwapChain::GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) doesn't change until certain APIs are called:</span></span>

-   [<span data-ttu-id="8d9ae-114">**IDXGISwapChain::ResizeTarget**</span><span class="sxs-lookup"><span data-stu-id="8d9ae-114">**IDXGISwapChain::ResizeTarget**</span></span>](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)
-   [<span data-ttu-id="8d9ae-115">**IDXGISwapChain::ResizeBuffers**</span><span class="sxs-lookup"><span data-stu-id="8d9ae-115">**IDXGISwapChain::ResizeBuffers**</span></span>](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers)

<span data-ttu-id="8d9ae-116">[**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)傳回的緩衝區順序永遠不會變更。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-116">The order of buffers returned by [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) never changes.</span></span>

<span data-ttu-id="8d9ae-117">[**IDXGISwapChain3：： GetCurrentBackBufferIndex**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) 會將目前背景緩衝區的索引傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-117">[**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) returns the index of the current back buffer to the app.</span></span>

### <a name="swap-effects"></a><span data-ttu-id="8d9ae-118">交換效果</span><span class="sxs-lookup"><span data-stu-id="8d9ae-118">Swap effects</span></span>

<span data-ttu-id="8d9ae-119">唯一支援的交換效果是 [**DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) 和 [**DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect)，其要求緩衝區計數必須大於1。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-119">The only supported swap effects are [**DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) and [**DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect), which requires the buffer count to be greater than one.</span></span>

### <a name="transitioning-between-windowed-and-full-screen-modes"></a><span data-ttu-id="8d9ae-120">在視窗模式和全螢幕模式之間轉換</span><span class="sxs-lookup"><span data-stu-id="8d9ae-120">Transitioning between windowed and full-screen modes</span></span>

<span data-ttu-id="8d9ae-121">Direct3D 12 不支援 (FSE) 的全螢幕獨佔模式。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-121">Direct3D 12 doesn't support full-screen exclusive mode (FSE).</span></span> <span data-ttu-id="8d9ae-122">相反地，當遊戲是唯一顯示在畫面上的應用程式時，OS 會使用稱為全螢幕 optimisations 的策略 (FSO) 來達成與 FSE 類似的效果，而不會有效能上的缺點。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-122">Instead, when a game is the only visible application on-screen, the OS uses a strategy called full-screen optimisations (FSO) to achieve a similar effect to FSE without the performance drawbacks.</span></span> <span data-ttu-id="8d9ae-123">如需 FSO 的詳細資訊，請參閱 [揭開全螢幕 Optimisations](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/)。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-123">For more info about FSO, see [Demystifying Fullscreen Optimisations](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/).</span></span>

<span data-ttu-id="8d9ae-124">Direct3D 12 在視窗模式和全螢幕模式之間進行轉換時，會維持應用程式必須呼叫 [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) 的限制 (D3D11 翻轉模型交換鏈的限制) 。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-124">Direct3D 12 maintains the restriction that applications must call [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) after transitioning between windowed and full-screen modes (D3D11 flip-model swap chains have the same restrictions).</span></span>

<span data-ttu-id="8d9ae-125">[**IDXGISwapChain：： SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)轉換不會變更交換鏈中應用程式可見的緩衝區集合。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-125">The [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) transitions do not change the set of app-visible buffers in the swap chain.</span></span> <span data-ttu-id="8d9ae-126">只有 [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) 和 [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) 呼叫會建立或終結應用程式可見的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-126">Only the [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) and [**ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) calls create or destroy app-visible buffers.</span></span> <span data-ttu-id="8d9ae-127">不過，在 Direct3D 12 [**IDXGISwapChain：： SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) 中不會進入全螢幕獨佔模式，而只會變更解析度和重新整理速率以允許全螢幕 optimisations。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-127">However, in Direct3D 12 [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) doesn't enter full-screen exclusive mode, and simply changes resolutions and refresh rates to allow full-screen optimisations.</span></span> <span data-ttu-id="8d9ae-128">應用程式不需要使用此方法即可進行這些變更</span><span class="sxs-lookup"><span data-stu-id="8d9ae-128">These changes can be made by an app without the use of this method</span></span>

<span data-ttu-id="8d9ae-129">當或 [**IDXGISwapChain**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) 時，會呼叫:P 重新傳送或 [**IDXGISwapChain1：:P**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) 重新傳送，要顯示的背景緩衝區必須處於 [**D3D12 \_ 資源 \_ 狀態 \_ 目前**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) 狀態。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-129">When or [**IDXGISwapChain::Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) or [**IDXGISwapChain1::Present**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) is called, the back buffer to be presented must be in the [**D3D12\_RESOURCE\_STATE\_PRESENT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) state.</span></span> <span data-ttu-id="8d9ae-130">如果不是這種情況，就會發生 **DXGI \_ 錯誤 \_ 無效 \_ 呼叫** 而失敗。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-130">Present will fail with **DXGI\_ERROR\_INVALID\_CALL** if this is not the case.</span></span>

<span data-ttu-id="8d9ae-131">全螢幕交換鏈會繼續具有 [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) (FALSE 的限制，Null) 必須在交換鏈的最終版本之前呼叫。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-131">Full-screen swap chains continue to have the restriction that [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)(FALSE, NULL) must be called before the final release of the swap chain.</span></span> <span data-ttu-id="8d9ae-132">在 Direct3D 12 裝置上執行的交換鏈上， **SetFullscreenState** (FALSE) 成功。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-132">**SetFullscreenState**(FALSE) succeeds on swap chains running on Direct3D 12 devices.</span></span>

<span data-ttu-id="8d9ae-133">目前的作業會在建立 swapchain 時所提供的3D 佇列上執行，而應用程式可自由地顯示多個交換鏈，以及記錄和執行命令清單。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-133">Present operations occur on the 3D queue provided at swapchain creation, and apps are free to concurrently present multiple swap chains, and record and execute command lists.</span></span>

<span data-ttu-id="8d9ae-134">當圖形的最後一部分運作 (例如，在計算佇列上進行框架後處理) ，或不包含裝置的圖形佇列，建立第二個要呈現的3D 佇列可能會很有説明，並防止呈現延遲時間延遲到下一個畫面格的開始。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-134">When the final part of the graphics work (for example, frame postprocessing) is done on a compute queue, or doesn't involve the device's graphics queue, creating a second 3D queue to present on can be beneficial and prevent the latency of presentation delaying the start of the next frame.</span></span> 

### <a name="example"></a><span data-ttu-id="8d9ae-135">範例</span><span class="sxs-lookup"><span data-stu-id="8d9ae-135">Example</span></span>

<span data-ttu-id="8d9ae-136">下列範例程式碼會出現在主要轉譯迴圈中：</span><span class="sxs-lookup"><span data-stu-id="8d9ae-136">The following example code would be present in the main rendering loop:</span></span>

```cpp
void Present()
{
    m_swapChain->Present(0, m_presentFlags);
    m_backBufferIndex = (m_backBufferIndex + 1) % m_backBufferCount;
}
```

### <a name="creating-swap-chains"></a><span data-ttu-id="8d9ae-137">建立交換鏈</span><span class="sxs-lookup"><span data-stu-id="8d9ae-137">Creating swap chains</span></span>

<span data-ttu-id="8d9ae-138">使用 [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)、 [**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)或 [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) 呼叫時，請注意 *pDevice* 參數實際上需要 Direct3D 12 中直接命令佇列的指標，而不是裝置。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-138">When using the [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), [**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow), or [**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) calls, note that the *pDevice* parameter actually requires a pointer to a direct command queue in Direct3D 12, and not a device.</span></span>

### <a name="presenting-on-windows-7"></a><span data-ttu-id="8d9ae-139">在 Windows 7 上展示</span><span class="sxs-lookup"><span data-stu-id="8d9ae-139">Presenting on Windows 7</span></span>

<span data-ttu-id="8d9ae-140">在 Windows 7 上以 Direct3D 12 為目標時，不會顯示 Direct3D 12 的必要 DXGI 類型，因此您必須使用 D3D12On7 提供的 **ID3D12CommandQueueDownLevel** (從直接命令佇列中查詢，) 才會出現。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-140">When targeting Direct3D 12 on Windows 7, the necessary DXGI types for Direct3D 12 are not present, so you must use the D3D12On7-provided **ID3D12CommandQueueDownLevel** (queried off of the direct command queue) to present.</span></span>

<span data-ttu-id="8d9ae-141">您可以將開啟的命令清單提供給 Windows 7 目前的方法，然後使用、關閉，並自動提交給裝置。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-141">You provide an open command list to the Windows 7 present method, which will then be used, closed, and automatically submitted to the device for you.</span></span> <span data-ttu-id="8d9ae-142">您必須提供必須為應用程式建立的後置緩衝區、必須是已認可的資源、必須是單一取樣，而且必須是下列其中一種格式。</span><span class="sxs-lookup"><span data-stu-id="8d9ae-142">You must provide a back buffer which must be app-created, must be a committed resource, must be single-sampled, and must be one of the following formats.</span></span>

* <span data-ttu-id="8d9ae-143">**DXGI_FORMAT_R16G16B16A16_FLOAT**</span><span class="sxs-lookup"><span data-stu-id="8d9ae-143">**DXGI_FORMAT_R16G16B16A16_FLOAT**</span></span>
* <span data-ttu-id="8d9ae-144">**DXGI_FORMAT_R10G10B10A2_UNORM**</span><span class="sxs-lookup"><span data-stu-id="8d9ae-144">**DXGI_FORMAT_R10G10B10A2_UNORM**</span></span>
* <span data-ttu-id="8d9ae-145">**DXGI_FORMAT_R8G8B8A8_UNORM**</span><span class="sxs-lookup"><span data-stu-id="8d9ae-145">**DXGI_FORMAT_R8G8B8A8_UNORM**</span></span>
* <span data-ttu-id="8d9ae-146">**DXGI_FORMAT_R8G8B8A8_UNORM_SRGB**</span><span class="sxs-lookup"><span data-stu-id="8d9ae-146">**DXGI_FORMAT_R8G8B8A8_UNORM_SRGB**</span></span>
* <span data-ttu-id="8d9ae-147">**DXGI_FORMAT_B8G8R8X8_UNORM**</span><span class="sxs-lookup"><span data-stu-id="8d9ae-147">**DXGI_FORMAT_B8G8R8X8_UNORM**</span></span>
* <span data-ttu-id="8d9ae-148">**DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM**</span><span class="sxs-lookup"><span data-stu-id="8d9ae-148">**DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM**</span></span>
* <span data-ttu-id="8d9ae-149">**DXGI_FORMAT_B8G8R8A8_UNORM**</span><span class="sxs-lookup"><span data-stu-id="8d9ae-149">**DXGI_FORMAT_B8G8R8A8_UNORM**</span></span>
* <span data-ttu-id="8d9ae-150">**DXGI_FORMAT_B8G8R8A8_UNORM_SRGB**</span><span class="sxs-lookup"><span data-stu-id="8d9ae-150">**DXGI_FORMAT_B8G8R8A8_UNORM_SRGB**</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d9ae-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="8d9ae-151">Related topics</span></span>

* [<span data-ttu-id="8d9ae-152">D3D12_HEAP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="8d9ae-152">D3D12_HEAP_FLAGS</span></span>](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)
* [<span data-ttu-id="8d9ae-153">DirectX advanced learning 影片教學課程：調節幀</span><span class="sxs-lookup"><span data-stu-id="8d9ae-153">DirectX advanced learning video tutorials : Unthrottled Framerate</span></span>](https://www.youtube.com/watch?v=wn02zCXa9IU)
* [<span data-ttu-id="8d9ae-154">轉譯</span><span class="sxs-lookup"><span data-stu-id="8d9ae-154">Rendering</span></span>](rendering.md)
