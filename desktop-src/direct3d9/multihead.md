---
description: Multihead 卡是具有通用框架緩衝區和加速器、獨立數位到類比轉換器 (Dac) 和監視輸出的卡片。
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: 'Multihead (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4617666ca623795d33bf1dafcaafeabe73323253
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467586"
---
# <a name="multihead-direct3d-9"></a><span data-ttu-id="03d86-103">Multihead (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="03d86-103">Multihead (Direct3D 9)</span></span>

<span data-ttu-id="03d86-104">Multihead 卡是具有通用框架緩衝區和加速器、獨立數位到類比轉換器 (Dac) 和監視輸出的卡片。</span><span class="sxs-lookup"><span data-stu-id="03d86-104">Multihead cards are those that have a common frame buffer and accelerator, independent digital-to-analog converters (DACs), and monitor outputs.</span></span> <span data-ttu-id="03d86-105">這類裝置可提供比相同數量的異類顯示器介面卡更容易使用的多監視器支援。</span><span class="sxs-lookup"><span data-stu-id="03d86-105">Such devices can offer much more usable multiple monitor support than a similar number of heterogeneous display adapters.</span></span>

<span data-ttu-id="03d86-106">Multihead 卡在 API 中公開為單一 API 層級的裝置，可驅動數個全螢幕交換鏈。</span><span class="sxs-lookup"><span data-stu-id="03d86-106">Multihead cards are exposed in the API as a single API-level device that can drive several full-screen swap chains.</span></span> <span data-ttu-id="03d86-107">因此，所有資源都會與所有的標頭共用，而且每個標頭都有完全相同的功能。</span><span class="sxs-lookup"><span data-stu-id="03d86-107">Consequently, all resources are shared with all the heads, and each head has exactly the same capabilities.</span></span> <span data-ttu-id="03d86-108">每個標頭都可以設定為獨立的顯示模式。</span><span class="sxs-lookup"><span data-stu-id="03d86-108">Each head can be set to independent display modes.</span></span> <span data-ttu-id="03d86-109">您可以使用不同的 [**IDirect3DSwapChain9 呼叫：:P**](/windows/desktop/api) 重新傳送以重新整理每個標頭。</span><span class="sxs-lookup"><span data-stu-id="03d86-109">You can use separate calls to [**IDirect3DSwapChain9::Present**](/windows/desktop/api) to refresh each head.</span></span> <span data-ttu-id="03d86-110">您也可以使用一次呼叫 [**IDirect3DDevice9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) 重新傳送以依序重新整理每個標頭。</span><span class="sxs-lookup"><span data-stu-id="03d86-110">You can also use one call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) to refresh each head sequentially.</span></span>

> [!Note]  
> <span data-ttu-id="03d86-111">每個標頭的重新整理不會同時透過單一呼叫 [**IDirect3DDevice9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)重新傳送。</span><span class="sxs-lookup"><span data-stu-id="03d86-111">The refresh of each head does not occur simultaneously with a single call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="03d86-112">Direct3D 9Ex 中的 [顯示統計資料] 可以使用 [**D3DPRESENTSTATS**](d3dpresentstats.md) 結構，讓每個前端的重新整理保持彼此接近，以限制跨多張介面卡的撕裂效果。</span><span class="sxs-lookup"><span data-stu-id="03d86-112">Present statistics in Direct3D 9Ex can use the [**D3DPRESENTSTATS**](d3dpresentstats.md) structure to keep the refreshes to each head close to each other to limit tearing effects across multiple heads of adapters.</span></span> <span data-ttu-id="03d86-113">如需有關同步處理 Direct3D 9Ex flip 模型應用程式之框架的詳細資訊，請參閱 [Direct3d 9Ex 增強功能](../direct3darticles/direct3d-9ex-improvements.md)。</span><span class="sxs-lookup"><span data-stu-id="03d86-113">For information about synchronizing frames of Direct3D 9Ex flip model applications, see [Direct3D 9Ex Improvements](../direct3darticles/direct3d-9ex-improvements.md).</span></span>

 

<span data-ttu-id="03d86-114">Multihead 裝置的每個交換鏈都必須是全螢幕。</span><span class="sxs-lookup"><span data-stu-id="03d86-114">Each swap chain for a multihead device must be full screen.</span></span> <span data-ttu-id="03d86-115">當裝置進入 multihead 模式時，它必須維持全螢幕。</span><span class="sxs-lookup"><span data-stu-id="03d86-115">When a device has entered multihead mode, it must remain full screen.</span></span> <span data-ttu-id="03d86-116">轉換回視窗模式的模式需要終結裝置 (但一般 ALT + TAB 至最小化作業) 除外。</span><span class="sxs-lookup"><span data-stu-id="03d86-116">The transition back to windowed mode requires the destruction of the device (except for the normal ALT+TAB-to-minimize operation).</span></span>

<span data-ttu-id="03d86-117">在 head 之間分割影片記憶體的舊方法，將每個標頭視為完全獨立的加速器，仍然是常見的使用案例。</span><span class="sxs-lookup"><span data-stu-id="03d86-117">The old method of dividing video memory between the heads and treating each head as a fully independent accelerator will still be a common usage scenario.</span></span> <span data-ttu-id="03d86-118">除非應用程式已特別編碼為在 Direct3D 9 multihead 模式下運作，否則此建議程式不會取代該機制。</span><span class="sxs-lookup"><span data-stu-id="03d86-118">This proposal does not replace that mechanism unless the application has been specifically coded to function in the Direct3D 9 multihead mode.</span></span>

<span data-ttu-id="03d86-119">驅動程式會獲得足夠的知識，以便在這兩種作業模式之間切換。</span><span class="sxs-lookup"><span data-stu-id="03d86-119">Drivers are given adequate knowledge to switch between the two modes of operation.</span></span>

<span data-ttu-id="03d86-120">其中一個標頭稱為主要 head，而同一張卡片上的所有其他標頭則稱為「次級」。</span><span class="sxs-lookup"><span data-stu-id="03d86-120">One head will be called the master head, and all other heads on the same card be called subordinate heads.</span></span> <span data-ttu-id="03d86-121">如果系統中有一個以上的 multihead 介面卡，則單一 multihead 介面卡上的主要和其從屬電腦稱為群組。</span><span class="sxs-lookup"><span data-stu-id="03d86-121">If more than one multihead adapter is present in a system, the master and its subordinates from one multihead adapter are called a group.</span></span> <span data-ttu-id="03d86-122">群組是由其主要 head 的介面卡序數表示。</span><span class="sxs-lookup"><span data-stu-id="03d86-122">Groups are denoted by the adapter ordinal of their master head.</span></span>

<span data-ttu-id="03d86-123">[**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)結構已更新為公開下列新的硬體上限。</span><span class="sxs-lookup"><span data-stu-id="03d86-123">The [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure has been updated to expose the following new hardware caps.</span></span>


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   <span data-ttu-id="03d86-124">適用于傳統介面卡的 NumberOfAdaptersInGroup 是1，而 multihead 卡的主要介面卡則大於1。</span><span class="sxs-lookup"><span data-stu-id="03d86-124">NumberOfAdaptersInGroup is 1 for conventional adapters, and greater than 1 for the master adapter of a multihead card.</span></span> <span data-ttu-id="03d86-125">Multihead 卡的從屬介面卡的值會是0。</span><span class="sxs-lookup"><span data-stu-id="03d86-125">The value will be 0 for a subordinate adapter of a multihead card.</span></span> <span data-ttu-id="03d86-126">每張卡片最多可以有一個主要主機，但可能有許多附屬。</span><span class="sxs-lookup"><span data-stu-id="03d86-126">Each card can have at most one master, but might have many subordinates.</span></span>
-   <span data-ttu-id="03d86-127">MasterAdapterOrdinal 指出哪個裝置是此從屬的主要節點。</span><span class="sxs-lookup"><span data-stu-id="03d86-127">MasterAdapterOrdinal indicates which device is the master for this subordinate.</span></span>
-   <span data-ttu-id="03d86-128">AdapterOrdinalInGroup 指出 API 參考標頭的順序。</span><span class="sxs-lookup"><span data-stu-id="03d86-128">AdapterOrdinalInGroup indicates the order in which heads are referenced by the API.</span></span> <span data-ttu-id="03d86-129">主要介面卡一律會有 AdapterOrdinalInGroup 0。</span><span class="sxs-lookup"><span data-stu-id="03d86-129">The master adapter always has AdapterOrdinalInGroup 0.</span></span> <span data-ttu-id="03d86-130">這些值不會對應至傳遞給 IDirect3D9 方法的介面卡序數，而只會套用至群組內的標頭。</span><span class="sxs-lookup"><span data-stu-id="03d86-130">These values do not correspond to the adapter ordinals passed to the IDirect3D9 methods, but apply only to heads within a group.</span></span>

<span data-ttu-id="03d86-131">此定義可讓 multihead 卡片繼續以獨立卡形式來顯示多個介面卡，就像在 DirectX 8 中一樣。</span><span class="sxs-lookup"><span data-stu-id="03d86-131">This definition allows multihead cards to continue to present multiple adapters as if they were independent cards, just as they did in DirectX 8.</span></span>

<span data-ttu-id="03d86-132">若要建立 multihead 裝置，請 \_ \_ 在 [**IDirect3D9：： CreateDevice**](/windows/desktop/api)中指定行為旗標 D3DCREATE ADAPTERGROUP 裝置。</span><span class="sxs-lookup"><span data-stu-id="03d86-132">To create a multihead device, specify the behavior flag D3DCREATE\_ADAPTERGROUP\_DEVICE in [**IDirect3D9::CreateDevice**](/windows/desktop/api).</span></span> <span data-ttu-id="03d86-133">呈現參數 ([**D3DPRESENT \_ 參數**](d3dpresent-parameters.md) 的陣列) 應該包含 NumberOfAdaptersInGroup 元素。</span><span class="sxs-lookup"><span data-stu-id="03d86-133">The presentation parameters (an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md)) should contain NumberOfAdaptersInGroup elements.</span></span> <span data-ttu-id="03d86-134">執行時間會將每個元素指派給每個標頭，並以 AdapterOrdinalInGroup 的數值順序排列。</span><span class="sxs-lookup"><span data-stu-id="03d86-134">The runtime will assign each element to each head in AdapterOrdinalInGroup numerical order.</span></span> <span data-ttu-id="03d86-135">設定 D3DCREATE \_ ADAPTERGROUP \_ 裝置時，每個呈現參數都必須有：</span><span class="sxs-lookup"><span data-stu-id="03d86-135">When D3DCREATE\_ADAPTERGROUP\_DEVICE is set, each presentation parameter must have:</span></span>

-   <span data-ttu-id="03d86-136">設定為 **FALSE** 的視窗成員 (換言之，是全螢幕) 。</span><span class="sxs-lookup"><span data-stu-id="03d86-136">The Windowed member set to **FALSE** (in other words, be full screen).</span></span>
-   <span data-ttu-id="03d86-137">[**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)之 EnableAutoDepthStencil 成員的相同值。</span><span class="sxs-lookup"><span data-stu-id="03d86-137">The same value for the EnableAutoDepthStencil member of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="03d86-138">此外，如果 EnableAutoDepthStencil 為 **TRUE**，則下列每個欄位的每個 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)都必須有相同的值：</span><span class="sxs-lookup"><span data-stu-id="03d86-138">In addition, if EnableAutoDepthStencil is **TRUE**, then each of the following fields must have the same value for each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md):</span></span>

-   <span data-ttu-id="03d86-139">AutoDepthStencilFormat</span><span class="sxs-lookup"><span data-stu-id="03d86-139">AutoDepthStencilFormat</span></span>
-   <span data-ttu-id="03d86-140">BackBufferWidth</span><span class="sxs-lookup"><span data-stu-id="03d86-140">BackBufferWidth</span></span>
-   <span data-ttu-id="03d86-141">BackBufferHeight</span><span class="sxs-lookup"><span data-stu-id="03d86-141">BackBufferHeight</span></span>
-   <span data-ttu-id="03d86-142">BackBufferFormat</span><span class="sxs-lookup"><span data-stu-id="03d86-142">BackBufferFormat</span></span>

<span data-ttu-id="03d86-143">如果設定 DAC， [**IDirect3DDevice9：： CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) 的其他呼叫不合法。</span><span class="sxs-lookup"><span data-stu-id="03d86-143">If DAC is set, additional calls to [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) are illegal.</span></span>

<span data-ttu-id="03d86-144">如果裝置是使用 DAC 建立的， [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) 將會預期 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)的陣列。</span><span class="sxs-lookup"><span data-stu-id="03d86-144">If the device was created with the DAC, [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) will expect an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="03d86-145">傳遞至 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)的每個 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md)結構都必須是全螢幕。</span><span class="sxs-lookup"><span data-stu-id="03d86-145">Each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure passed to [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) must be full screen.</span></span> <span data-ttu-id="03d86-146">若要切換回視窗模式，應用程式必須終結裝置，並在視窗模式中重新建立非 multihead 裝置。</span><span class="sxs-lookup"><span data-stu-id="03d86-146">To switch back to windowed mode, the application must destroy the device and re-create a non-multihead device in windowed mode.</span></span>

<span data-ttu-id="03d86-147">以下是基本使用案例：</span><span class="sxs-lookup"><span data-stu-id="03d86-147">Here is a basic usage scenario:</span></span>


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



<span data-ttu-id="03d86-148">如需詳細資訊，請參閱 [**IDirect3D9：： CreateDevice**](/windows/desktop/api) 和 [**IDirect3DDevice9：： GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains)。</span><span class="sxs-lookup"><span data-stu-id="03d86-148">For more information, see [**IDirect3D9::CreateDevice**](/windows/desktop/api) and [**IDirect3DDevice9::GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03d86-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="03d86-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03d86-150">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="03d86-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
