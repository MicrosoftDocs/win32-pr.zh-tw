---
title: 改善 Direct2D 應用程式的效能
description: 描述改善 Direct2D 效能的技術。
ms.assetid: e6b02925-4e75-42b0-b0c4-00f1ddb85e46
keywords:
- Direct2D，效能
- Direct2D，點陣圖
- Direct2D，資源使用量
- Direct2D、Flush 方法
- Direct2D、靜態內容
- Direct2D 的效能
- Direct2D 的點陣圖
- Direct2D，GDI 交互操作
- Direct2D，互通性
- 互通性，Direct2D
- '圖形裝置介面 (GDI) '
- 'GDI (圖形裝置介面) '
- '互通性、圖形裝置介面 (GDI) '
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5a413b96e00514b64b3cf1b1ee451a84a9e9ff09
ms.sourcegitcommit: 6eb53540b8d882fd035d428567d7d1c5ec17042c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/12/2020
ms.locfileid: "104463888"
---
# <a name="improving-the-performance-of-direct2d-apps"></a><span data-ttu-id="50e77-116">改善 Direct2D 應用程式的效能</span><span class="sxs-lookup"><span data-stu-id="50e77-116">Improving the performance of Direct2D apps</span></span>

<span data-ttu-id="50e77-117">雖然 [Direct2D](./direct2d-portal.md) 是硬體加速的，且適用于高效能，但您必須正確使用這些功能才能將輸送量最大化。</span><span class="sxs-lookup"><span data-stu-id="50e77-117">Although [Direct2D](./direct2d-portal.md) is hardware accelerated and is meant for high performance, you must use the features correctly to maximize throughput.</span></span> <span data-ttu-id="50e77-118">此處所示的技巧衍生自研究一般案例，可能不適用於所有應用程式案例。</span><span class="sxs-lookup"><span data-stu-id="50e77-118">The techniques we show here are derived from studying common scenarios and might not apply to all app scenarios.</span></span> <span data-ttu-id="50e77-119">因此，請仔細瞭解應用程式行為和效能目標，以協助達到您想要的結果。</span><span class="sxs-lookup"><span data-stu-id="50e77-119">Therefore, careful understanding of app behavior and performance goals can help achieve the results that you want.</span></span>

-   [<span data-ttu-id="50e77-120">資源使用量</span><span class="sxs-lookup"><span data-stu-id="50e77-120">Resource usage</span></span>](#resource-usage)
    -   [<span data-ttu-id="50e77-121">重複使用資源</span><span class="sxs-lookup"><span data-stu-id="50e77-121">Reuse resources</span></span>](#reuse-resources)
-   [<span data-ttu-id="50e77-122">限制使用 flush</span><span class="sxs-lookup"><span data-stu-id="50e77-122">Restrict the use of flush</span></span>](#restrict-the-use-of-flush)
-   [<span data-ttu-id="50e77-123">點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-123">Bitmaps</span></span>](#create-large-bitmaps)
    -   [<span data-ttu-id="50e77-124">建立大型點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-124">Create large bitmaps</span></span>](#create-large-bitmaps)
    -   [<span data-ttu-id="50e77-125">建立點陣圖的塔</span><span class="sxs-lookup"><span data-stu-id="50e77-125">Create an atlas of bitmaps</span></span>](#create-an-atlas-of-bitmaps)
    -   [<span data-ttu-id="50e77-126">建立共用點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-126">Create shared bitmaps</span></span>](#create-shared-bitmaps)
    -   [<span data-ttu-id="50e77-127">複製點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-127">Copying bitmaps</span></span>](#copying-bitmaps)
-   [<span data-ttu-id="50e77-128">在虛線區分上使用磚點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-128">Use tiled bitmap over dashing</span></span>](#use-tiled-bitmap-over-dashing)
-   [<span data-ttu-id="50e77-129">呈現複雜靜態內容的一般指導方針</span><span class="sxs-lookup"><span data-stu-id="50e77-129">General guidelines for rendering complex static content</span></span>](#general-guidelines-for-rendering-complex-static-content)
    -   [<span data-ttu-id="50e77-130">使用色彩點陣圖的完整場景快取</span><span class="sxs-lookup"><span data-stu-id="50e77-130">Full scene caching using a color bitmap</span></span>](#full-scene-caching-using-a-color-bitmap)
    -   [<span data-ttu-id="50e77-131">使用 A8 點陣圖和 FillOpacityMask 方法的每一基本快取</span><span class="sxs-lookup"><span data-stu-id="50e77-131">Per primitive caching using an A8 bitmap and the FillOpacityMask method</span></span>](#per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method)
-   [<span data-ttu-id="50e77-132">使用 geometry 實踐的每個基本快取</span><span class="sxs-lookup"><span data-stu-id="50e77-132">Per-primitive caching using geometry realizations</span></span>](#per-primitive-caching-using-geometry-realizations)
-   [<span data-ttu-id="50e77-133">幾何轉譯</span><span class="sxs-lookup"><span data-stu-id="50e77-133">Geometry rendering</span></span>](#geometry-rendering)
    -   [<span data-ttu-id="50e77-134">針對繪製幾何使用特定的繪圖基本</span><span class="sxs-lookup"><span data-stu-id="50e77-134">Use specific draw primitive over draw geometry</span></span>](#use-specific-draw-primitive-over-draw-geometry)
    -   [<span data-ttu-id="50e77-135">呈現靜態幾何</span><span class="sxs-lookup"><span data-stu-id="50e77-135">Rendering static geometry</span></span>](#rendering-static-geometry)
    -   [<span data-ttu-id="50e77-136">使用多執行緒裝置內容</span><span class="sxs-lookup"><span data-stu-id="50e77-136">Use a multithreaded device context</span></span>](#use-a-multithreaded-device-context)
-   [<span data-ttu-id="50e77-137">使用 Direct2D 繪製文字</span><span class="sxs-lookup"><span data-stu-id="50e77-137">Drawing text with Direct2D</span></span>](#use-a-multithreaded-device-context)
    -   [<span data-ttu-id="50e77-138">DrawTextLayout 與 DrawText 的比較</span><span class="sxs-lookup"><span data-stu-id="50e77-138">DrawTextLayout Vs. DrawText</span></span>](#drawtextlayout-vs-drawtext)
    -   [<span data-ttu-id="50e77-139">選擇正確的文字呈現模式</span><span class="sxs-lookup"><span data-stu-id="50e77-139">Choosing the right text rendering mode</span></span>](#choosing-the-right-text-rendering-mode)
    -   [<span data-ttu-id="50e77-140">Caching</span><span class="sxs-lookup"><span data-stu-id="50e77-140">Caching</span></span>](#full-scene-caching-using-a-color-bitmap)
-   [<span data-ttu-id="50e77-141">裁剪任意圖形</span><span class="sxs-lookup"><span data-stu-id="50e77-141">Clipping an arbitrary shape</span></span>](#clipping-an-arbitrary-shape)
    -   [<span data-ttu-id="50e77-142">Windows 8 中的 PushLayer</span><span class="sxs-lookup"><span data-stu-id="50e77-142">PushLayer in Windows 8</span></span>](#pushlayer-in-windows-8)
    -   [<span data-ttu-id="50e77-143">軸對齊的剪輯</span><span class="sxs-lookup"><span data-stu-id="50e77-143">Axis-aligned clips</span></span>](#axis-aligned-clips)
-   [<span data-ttu-id="50e77-144">DXGI 互通性：避免頻繁切換</span><span class="sxs-lookup"><span data-stu-id="50e77-144">DXGI interoperability: avoid frequent switches</span></span>](#dxgi-interoperability-avoid-frequent-switches)
-   [<span data-ttu-id="50e77-145">知道您的像素格式</span><span class="sxs-lookup"><span data-stu-id="50e77-145">Know Your Pixel Format</span></span>](#know-your-pixel-format)
-   [<span data-ttu-id="50e77-146">場景複雜性</span><span class="sxs-lookup"><span data-stu-id="50e77-146">Scene Complexity</span></span>](#scene-complexity)
    -   [<span data-ttu-id="50e77-147">瞭解場景複雜性</span><span class="sxs-lookup"><span data-stu-id="50e77-147">Understand Scene Complexity</span></span>](#understand-scene-complexity)
-   [<span data-ttu-id="50e77-148">改善 Direct2D 列印應用程式的效能</span><span class="sxs-lookup"><span data-stu-id="50e77-148">Improving performance for Direct2D printing apps</span></span>](#improving-performance-for-direct2d-printing-apps)
    -   [<span data-ttu-id="50e77-149">當您建立 D2D 列印控制項時，設定正確的屬性值</span><span class="sxs-lookup"><span data-stu-id="50e77-149">Set the right property values when you create the D2D print control</span></span>](#set-the-right-property-values-when-you-create-the-d2d-print-control)
    -   [<span data-ttu-id="50e77-150">避免使用特定的 Direct2D 繪製模式</span><span class="sxs-lookup"><span data-stu-id="50e77-150">Avoid using certain Direct2D drawing patterns</span></span>](#avoid-using-certain-direct2d-drawing-patterns)
    -   [<span data-ttu-id="50e77-151">以直接且簡單的方式繪製文字</span><span class="sxs-lookup"><span data-stu-id="50e77-151">Draw text in a direct and plain way</span></span>](#draw-text-in-a-direct-and-plain-way)
    -   [<span data-ttu-id="50e77-152">盡可能繪製原始點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-152">Draw the original bitmaps when possible</span></span>](#draw-the-original-bitmaps-when-possible)
-   [<span data-ttu-id="50e77-153">結論</span><span class="sxs-lookup"><span data-stu-id="50e77-153">Conclusion</span></span>](#conclusion)

## <a name="resource-usage"></a><span data-ttu-id="50e77-154">資源使用量</span><span class="sxs-lookup"><span data-stu-id="50e77-154">Resource usage</span></span>

<span data-ttu-id="50e77-155">在影片或系統記憶體中，資源是某種類型的配置。</span><span class="sxs-lookup"><span data-stu-id="50e77-155">A resource is an allocation of some kind, either in video or system memory.</span></span> <span data-ttu-id="50e77-156">點陣圖和筆刷是資源的範例。</span><span class="sxs-lookup"><span data-stu-id="50e77-156">Bitmaps and brushes are examples of resources.</span></span>

<span data-ttu-id="50e77-157">在 Direct2D 中，您可以在軟體和硬體中建立資源。</span><span class="sxs-lookup"><span data-stu-id="50e77-157">In Direct2D, resources can be created both in software and hardware.</span></span> <span data-ttu-id="50e77-158">在硬體上建立和刪除資源是昂貴的作業，因為它們需要大量的額外負荷來與視訊卡通訊。</span><span class="sxs-lookup"><span data-stu-id="50e77-158">Resource creation and deletion on hardware are expensive operations because they require lots of overhead for communicating with the video card.</span></span> <span data-ttu-id="50e77-159">讓我們來看看 Direct2D 如何將內容轉譯為目標。</span><span class="sxs-lookup"><span data-stu-id="50e77-159">Let's see how Direct2D renders content to a target.</span></span>

<span data-ttu-id="50e77-160">在 Direct2D 中，所有轉譯命令都包含在呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 和 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)的呼叫之間。</span><span class="sxs-lookup"><span data-stu-id="50e77-160">In Direct2D, all the rendering commands are enclosed between a call to [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and a call to [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span> <span data-ttu-id="50e77-161">這些呼叫會對轉譯目標進行。</span><span class="sxs-lookup"><span data-stu-id="50e77-161">These calls are made to a render target.</span></span> <span data-ttu-id="50e77-162">呼叫轉譯作業之前，您必須先呼叫 **BeginDraw** 方法。</span><span class="sxs-lookup"><span data-stu-id="50e77-162">You must call the **BeginDraw** method before you call rendering operations .</span></span> <span data-ttu-id="50e77-163">呼叫 **BeginDraw** 之後，內容通常會建立一批轉譯命令，但是會延遲這些命令的處理，直到下列其中一個陳述成立為止：</span><span class="sxs-lookup"><span data-stu-id="50e77-163">After you call **BeginDraw** , a context typically builds up a batch of rendering commands, but delays processing of these commands until one of these statements is true:</span></span>

-   <span data-ttu-id="50e77-164">發生 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-164">[**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) occurred.</span></span> <span data-ttu-id="50e77-165">呼叫 **EndDraw** 時，會導致任何批次繪製作業完成，並傳回作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="50e77-165">When **EndDraw** is called, it causes any batched drawing operations to complete and returns the status of the operation.</span></span>
-   <span data-ttu-id="50e77-166">您可以明確呼叫 [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)： **flush** 方法會導致處理批次，併發出所有暫止的命令。</span><span class="sxs-lookup"><span data-stu-id="50e77-166">You make an explicit call to [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush): The **Flush** method causes the batch to be processed and all pending commands to be issued.</span></span>
-   <span data-ttu-id="50e77-167">保存呈現命令的緩衝區已滿。</span><span class="sxs-lookup"><span data-stu-id="50e77-167">The buffer holding the rendering commands is full.</span></span> <span data-ttu-id="50e77-168">如果在完成前兩個條件之前，此緩衝區已滿，則會清除轉譯命令。</span><span class="sxs-lookup"><span data-stu-id="50e77-168">If this buffer becomes full before the previous two conditions are fulfilled, the rendering commands are flushed out.</span></span>

<span data-ttu-id="50e77-169">在清除基本專案之前，Direct2D 會保留對應資源的內部參考，例如點陣圖和筆刷。</span><span class="sxs-lookup"><span data-stu-id="50e77-169">Until the primitives are flushed, Direct2D keeps internal references to corresponding resources like bitmaps and brushes.</span></span>

### <a name="reuse-resources"></a><span data-ttu-id="50e77-170">重複使用資源</span><span class="sxs-lookup"><span data-stu-id="50e77-170">Reuse resources</span></span>

<span data-ttu-id="50e77-171">如先前所述，資源的建立和刪除在硬體上很昂貴。</span><span class="sxs-lookup"><span data-stu-id="50e77-171">As already mentioned, resource creation and deletion is expensive on hardware.</span></span> <span data-ttu-id="50e77-172">因此，請盡可能重複使用資源。</span><span class="sxs-lookup"><span data-stu-id="50e77-172">So reuse resources when possible.</span></span> <span data-ttu-id="50e77-173">在遊戲開發過程中建立點陣圖建立範例。</span><span class="sxs-lookup"><span data-stu-id="50e77-173">Take the example of bitmap creation in game development.</span></span> <span data-ttu-id="50e77-174">通常會在遊戲中構成場景的點陣圖，同時以後續的框架對框架轉譯所需的所有不同變化來建立。</span><span class="sxs-lookup"><span data-stu-id="50e77-174">Usually, bitmaps that make up a scene in a game are all created at the same time with all the different variations that are required for later frame-to-frame rendering.</span></span> <span data-ttu-id="50e77-175">在實際的場景轉譯和重新呈現時，會重複使用這些點陣圖，而不是重新建立。</span><span class="sxs-lookup"><span data-stu-id="50e77-175">At the time of actual scene rendering and re-rendering, these bitmaps are reused instead of re-created.</span></span>

> [!Note]  
> <span data-ttu-id="50e77-176">您無法重複使用資源來調整視窗大小。</span><span class="sxs-lookup"><span data-stu-id="50e77-176">You can't reuse resources for the window resize operation.</span></span> <span data-ttu-id="50e77-177">調整視窗大小時，必須重新建立某些隨比例依存的資源，例如相容轉譯目標，而且可能需要重新建立某些圖層資源，因為視窗內容必須重新繪製。</span><span class="sxs-lookup"><span data-stu-id="50e77-177">When a window is resized, some scale-dependent resources such as compatible render targets and possibly some layer resources must be re-created because the window content has to be redrawn.</span></span> <span data-ttu-id="50e77-178">這對於維護轉譯場景的整體品質而言很重要。</span><span class="sxs-lookup"><span data-stu-id="50e77-178">This can be important for maintaining the overall quality of the rendered scene.</span></span>

 

## <a name="restrict-the-use-of-flush"></a><span data-ttu-id="50e77-179">限制使用 flush</span><span class="sxs-lookup"><span data-stu-id="50e77-179">Restrict the use of flush</span></span>

<span data-ttu-id="50e77-180">因為 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法會導致批次處理轉譯命令的處理，所以建議您不要使用它。</span><span class="sxs-lookup"><span data-stu-id="50e77-180">Because the [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) method causes the batched rendering commands to be processed, we recommend that you don't use it.</span></span> <span data-ttu-id="50e77-181">針對大部分的常見案例，請將資源管理留給 Direct2D。</span><span class="sxs-lookup"><span data-stu-id="50e77-181">For most common scenarios, leave resource management to Direct2D.</span></span>

## <a name="bitmaps"></a><span data-ttu-id="50e77-182">點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-182">Bitmaps</span></span>

<span data-ttu-id="50e77-183">如先前所述，建立和刪除資源在硬體上是相當昂貴的作業。</span><span class="sxs-lookup"><span data-stu-id="50e77-183">As mentioned earlier, resource creation and deletion are very expensive operations in hardware.</span></span> <span data-ttu-id="50e77-184">點陣圖是經常使用的一種資源。</span><span class="sxs-lookup"><span data-stu-id="50e77-184">A bitmap is a kind of resource that is used often.</span></span> <span data-ttu-id="50e77-185">在視訊卡上建立點陣圖很昂貴。</span><span class="sxs-lookup"><span data-stu-id="50e77-185">Creating bitmaps on the video card is expensive.</span></span> <span data-ttu-id="50e77-186">重複使用它們可讓應用程式更快。</span><span class="sxs-lookup"><span data-stu-id="50e77-186">Reusing them can help make the application faster.</span></span>

### <a name="create-large-bitmaps"></a><span data-ttu-id="50e77-187">建立大型點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-187">Create large bitmaps</span></span>

<span data-ttu-id="50e77-188">視訊卡通常會有最小的記憶體配置大小。</span><span class="sxs-lookup"><span data-stu-id="50e77-188">Video cards typically have a minimum memory allocation size.</span></span> <span data-ttu-id="50e77-189">如果要求的配置小於此值，系統就會配置此最小大小的資源，而剩餘的記憶體會被浪費，並無法供其他專案使用。</span><span class="sxs-lookup"><span data-stu-id="50e77-189">If an allocation is requested that is smaller than this, a resource of this minimum size is allocated and the surplus memory is wasted and unavailable for other things.</span></span> <span data-ttu-id="50e77-190">如果您需要許多小型點陣圖，更好的方法是配置一個大型點陣圖，並將所有小點陣圖內容儲存在這個大型點陣圖中。</span><span class="sxs-lookup"><span data-stu-id="50e77-190">If you need many small bitmaps, a better technique is to allocate one large bitmap and store all the small bitmap contents in this large bitmap.</span></span> <span data-ttu-id="50e77-191">然後，您可以在需要較小點陣圖的位置讀取較大點陣圖的子領域。</span><span class="sxs-lookup"><span data-stu-id="50e77-191">Then subareas of the larger bitmap can be read where the smaller bitmaps are needed.</span></span> <span data-ttu-id="50e77-192">通常，您應該在小型點陣圖之間包含填補 (透明的黑色圖元) ，以避免在作業期間較小影像之間的任何互動。</span><span class="sxs-lookup"><span data-stu-id="50e77-192">Often, you should include padding (transparent black pixels) in between the small bitmaps to avoid any interaction between the smaller images during operations.</span></span> <span data-ttu-id="50e77-193">這也稱為 *塔*，其優點是減少點陣圖建立的額外負荷，以及小型點陣圖配置的記憶體浪費。</span><span class="sxs-lookup"><span data-stu-id="50e77-193">This is also known as an *atlas*, and it has the benefit of reducing bitmap creation overhead and the memory waste of small bitmap allocations.</span></span> <span data-ttu-id="50e77-194">建議您將大部分的點陣圖保持至少為 64 KB，並限制小於 4 KB 的點陣圖數目。</span><span class="sxs-lookup"><span data-stu-id="50e77-194">We recommend that you keep most bitmaps to at least 64 KB and limit the number of bitmaps that are smaller than 4 KB.</span></span>

### <a name="create-an-atlas-of-bitmaps"></a><span data-ttu-id="50e77-195">建立點陣圖的塔</span><span class="sxs-lookup"><span data-stu-id="50e77-195">Create an atlas of bitmaps</span></span>

<span data-ttu-id="50e77-196">有一些常見的案例，例如點陣圖塔可以提供很好的服務。</span><span class="sxs-lookup"><span data-stu-id="50e77-196">There are some common scenarios for which a bitmap atlas can serve very well.</span></span> <span data-ttu-id="50e77-197">小型點陣圖可以儲存在大型點陣圖內。</span><span class="sxs-lookup"><span data-stu-id="50e77-197">Small bitmaps can be stored inside a large bitmap.</span></span> <span data-ttu-id="50e77-198">當您藉由指定目的地矩形來需要這些小型點陣圖時，可以從較大的點陣圖提取這些小點陣圖。</span><span class="sxs-lookup"><span data-stu-id="50e77-198">These small bitmaps can be pulled out of the larger bitmap when you need them by specifying the destination rectangle.</span></span> <span data-ttu-id="50e77-199">例如，應用程式必須繪製多個圖示。</span><span class="sxs-lookup"><span data-stu-id="50e77-199">For example, an application has to draw multiple icons.</span></span> <span data-ttu-id="50e77-200">所有與圖示相關聯的點陣圖都可以預先載入大型點陣圖。</span><span class="sxs-lookup"><span data-stu-id="50e77-200">All the bitmaps associated with the icons can be loaded into a large bitmap up front.</span></span> <span data-ttu-id="50e77-201">而且在轉譯時，可以從大型點陣圖取出它們。</span><span class="sxs-lookup"><span data-stu-id="50e77-201">And at rendering time, they can be retrieved from the large bitmap.</span></span>

> [!Note]  
> <span data-ttu-id="50e77-202">在視訊記憶體中建立的 Direct2D 點陣圖受限於儲存該點陣圖的介面卡所支援的點陣圖大小上限。</span><span class="sxs-lookup"><span data-stu-id="50e77-202">A Direct2D bitmap created in video memory is limited to the maximum bitmap size supported by the adapter on which it is stored.</span></span> <span data-ttu-id="50e77-203">建立大於該點陣圖的點陣圖可能會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="50e77-203">Creating a bitmap larger than that might result in an error.</span></span>

 

> [!Note]  
> <span data-ttu-id="50e77-204">從 Windows 8 開始，Direct2D 包含可讓此程式變得更容易的 [塔效果](atlas.md) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-204">Starting in Windows 8, Direct2D includes an [Atlas effect](atlas.md) that can make this process easier.</span></span>

 

### <a name="create-shared-bitmaps"></a><span data-ttu-id="50e77-205">建立共用點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-205">Create shared bitmaps</span></span>

<span data-ttu-id="50e77-206">建立共用點陣圖可讓 advanced 呼叫者建立 Direct2D 點陣圖物件，這些物件是直接由現有物件所支援，且已與轉譯目標相容。</span><span class="sxs-lookup"><span data-stu-id="50e77-206">Creating shared bitmaps enables advanced callers to create Direct2D bitmap objects that are backed directly by an existing object, already compatible with the render target.</span></span> <span data-ttu-id="50e77-207">這可避免建立多個表面，並有助於減少效能負擔。</span><span class="sxs-lookup"><span data-stu-id="50e77-207">This avoids creating multiple surfaces and helps in reducing performance overhead.</span></span>

> [!Note]  
> <span data-ttu-id="50e77-208">共用點陣圖通常僅限於軟體目標或可與 DXGI 互通的目標。</span><span class="sxs-lookup"><span data-stu-id="50e77-208">Shared bitmaps are usually limited to software targets or to targets interoperable with DXGI.</span></span> <span data-ttu-id="50e77-209">使用 [**CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1))、 [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))和 [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) 方法來建立共用點陣圖。</span><span class="sxs-lookup"><span data-stu-id="50e77-209">Use the [**CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)), [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1)), and [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) methods to create shared bitmaps.</span></span>

 

### <a name="copying-bitmaps"></a><span data-ttu-id="50e77-210">複製點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-210">Copying bitmaps</span></span>

<span data-ttu-id="50e77-211">建立 DXGI 介面是一項昂貴的作業，因此當您可以時重複使用現有的表面。</span><span class="sxs-lookup"><span data-stu-id="50e77-211">Creating a DXGI surface is an expensive operation so reuse existing surfaces when you can.</span></span> <span data-ttu-id="50e77-212">即使是在軟體中，如果點陣圖大多是您想要的表單，但不只是小部分，最好是更新該部分，而不是將整個點陣圖擲回並重新建立所有專案。</span><span class="sxs-lookup"><span data-stu-id="50e77-212">Even in software, if a bitmap is mostly in the form you want except for a small portion, it is better to update that portion than to throw the whole bitmap away and re-create everything.</span></span> <span data-ttu-id="50e77-213">雖然您可以使用 [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) 來達到相同的結果，但轉譯通常是比複製更昂貴的作業。</span><span class="sxs-lookup"><span data-stu-id="50e77-213">Although you can use [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) to achieve the same results, rendering is generally a much more expensive operation than copying.</span></span> <span data-ttu-id="50e77-214">這是因為若要改善快取位置，硬體實際上不會將點陣圖儲存為點陣圖所定址的相同記憶體順序。</span><span class="sxs-lookup"><span data-stu-id="50e77-214">This is because, to improve cache locality, the hardware doesn't actually store a bitmap in the same memory order that the bitmap is addressed.</span></span> <span data-ttu-id="50e77-215">相反地，點陣圖可能會 swizzled。</span><span class="sxs-lookup"><span data-stu-id="50e77-215">Instead, the bitmap might be swizzled.</span></span> <span data-ttu-id="50e77-216">驅動程式 (會隱藏 CPU 的 swizzling，因為驅動程式很慢，而且只用于較低的元件) ，或 GPU 上的記憶體管理員。</span><span class="sxs-lookup"><span data-stu-id="50e77-216">The swizzling is hidden from the CPU either by the driver (which is slow and used only on lower-end parts), or by the memory manager on the GPU.</span></span> <span data-ttu-id="50e77-217">由於在轉譯時，資料如何寫入轉譯目標的條件約束，因此通常不會 swizzled 轉譯目標，或在您知道永遠不需要轉譯為介面的情況下，以較不理想的方式來 swizzled。</span><span class="sxs-lookup"><span data-stu-id="50e77-217">Because of constraints on how data is written into a render target when rendering, render targets are typically either not swizzled, or swizzled in a way that is less optimal than can be achieved if you know that you never have to render to the surface.</span></span> <span data-ttu-id="50e77-218">因此， [](/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap) \* 系統會提供 CopyFrom 方法，將矩形從來源複製到 Direct2D 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="50e77-218">Therefore, the [CopyFrom](/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap)\* methods are provided for copying rectangles from a source to the Direct2D bitmap.</span></span>

<span data-ttu-id="50e77-219">CopyFrom 可用於下列三種形式：</span><span class="sxs-lookup"><span data-stu-id="50e77-219">CopyFrom can be used in any of its three forms:</span></span>

-   [<span data-ttu-id="50e77-220">**CopyFromBitmap**</span><span class="sxs-lookup"><span data-stu-id="50e77-220">**CopyFromBitmap**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [<span data-ttu-id="50e77-221">**CopyFromRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="50e77-221">**CopyFromRenderTarget**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)
-   [<span data-ttu-id="50e77-222">**CopyFromMemory**</span><span class="sxs-lookup"><span data-stu-id="50e77-222">**CopyFromMemory**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)

## <a name="use-tiled-bitmap-over-dashing"></a><span data-ttu-id="50e77-223">在虛線區分上使用磚點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-223">Use tiled bitmap over dashing</span></span>

<span data-ttu-id="50e77-224">由於基礎演算法的高品質和精確度，轉譯虛線是非常耗費資源的作業。</span><span class="sxs-lookup"><span data-stu-id="50e77-224">Rendering a dashed line is a very expensive operation because of the high quality and accuracy of the underlying algorithm.</span></span> <span data-ttu-id="50e77-225">對於大部分不涉及直線幾何的案例，使用並排點陣圖可以更快速地產生相同的效果。</span><span class="sxs-lookup"><span data-stu-id="50e77-225">For most of the cases not involving rectilinear geometries, the same effect can be generated faster by using tiled bitmaps.</span></span>

## <a name="general-guidelines-for-rendering-complex-static-content"></a><span data-ttu-id="50e77-226">呈現複雜靜態內容的一般指導方針</span><span class="sxs-lookup"><span data-stu-id="50e77-226">General guidelines for rendering complex static content</span></span>

<span data-ttu-id="50e77-227">如果您在框架上轉譯相同的內容框架，則快取內容，特別是當場景很複雜時。</span><span class="sxs-lookup"><span data-stu-id="50e77-227">Cache content if you render the same content frame over frame, especially when the scene is complex.</span></span>

<span data-ttu-id="50e77-228">有三種快取技術可供您使用：</span><span class="sxs-lookup"><span data-stu-id="50e77-228">There are three caching techniques that you can use:</span></span>

-   <span data-ttu-id="50e77-229">使用色彩點陣圖的完整場景快取。</span><span class="sxs-lookup"><span data-stu-id="50e77-229">Full scene caching using a color bitmap.</span></span>
-   <span data-ttu-id="50e77-230">使用 A8 點陣圖和 [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) 方法的每一基本快取。</span><span class="sxs-lookup"><span data-stu-id="50e77-230">Per primitive caching using an A8 bitmap and the [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) method.</span></span>
-   <span data-ttu-id="50e77-231">使用 geometry 實踐的每個基本的快取。</span><span class="sxs-lookup"><span data-stu-id="50e77-231">Per-primitive caching using geometry realizations.</span></span>

<span data-ttu-id="50e77-232">讓我們更詳細地查看每一個。</span><span class="sxs-lookup"><span data-stu-id="50e77-232">Let's look at each of these in more detail.</span></span>

### <a name="full-scene-caching-using-a-color-bitmap"></a><span data-ttu-id="50e77-233">使用色彩點陣圖的完整場景快取</span><span class="sxs-lookup"><span data-stu-id="50e77-233">Full scene caching using a color bitmap</span></span>

<span data-ttu-id="50e77-234">當您轉譯靜態內容時，在動畫這類案例中，請建立另一個完整色彩點陣圖，而不是直接寫入螢幕點陣圖。</span><span class="sxs-lookup"><span data-stu-id="50e77-234">When you render static content, in scenarios like animation, create another full color bitmap instead of writing directly to the screen bitmap.</span></span> <span data-ttu-id="50e77-235">儲存目前的目標、將目標設定為中繼點陣圖，然後轉譯靜態內容。</span><span class="sxs-lookup"><span data-stu-id="50e77-235">Save the current target, set target to the intermediate bitmap, and render the static content.</span></span> <span data-ttu-id="50e77-236">然後切換回原始的螢幕點陣圖，並在其上繪製中繼點陣圖。</span><span class="sxs-lookup"><span data-stu-id="50e77-236">Then, switch back to the original screen bitmap and draw the intermediate bitmap on it.</span></span>

<span data-ttu-id="50e77-237">以下為範例：</span><span class="sxs-lookup"><span data-stu-id="50e77-237">Here's an example:</span></span>


```C++
// Create a bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_B8G8R8A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &sceneBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render static content to the sceneBitmap.
m_d2dContext->SetTarget(sceneBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Render sceneBitmap to oldTarget.
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->DrawBitmap(sceneBitmap.Get());
```



<span data-ttu-id="50e77-238">此範例會使用中繼點陣圖來快取，並在轉譯時切換裝置內容指向的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="50e77-238">This example uses intermediate bitmaps for caching and switches the bitmap that the device context points to when it renders.</span></span> <span data-ttu-id="50e77-239">這樣就不需要針對相同的目的建立相容的轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="50e77-239">This avoids the need to create a compatible render target for the same purpose.</span></span>

### <a name="per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method"></a><span data-ttu-id="50e77-240">使用 A8 點陣圖和 FillOpacityMask 方法的每一基本快取</span><span class="sxs-lookup"><span data-stu-id="50e77-240">Per primitive caching using an A8 bitmap and the FillOpacityMask method</span></span>

<span data-ttu-id="50e77-241">當完整場景不是靜態的，但包含像是靜態的幾何或文字等元素時，您可以使用每個基本的快取技術。</span><span class="sxs-lookup"><span data-stu-id="50e77-241">When the full scene is not static, but consists of elements like geometry or text that are static, you can use a per primitive caching technique.</span></span> <span data-ttu-id="50e77-242">這項技術可保留所快取之基本的消除鋸齒特性，並且可與變更的筆刷類型搭配使用。</span><span class="sxs-lookup"><span data-stu-id="50e77-242">This technique preserves the antialiasing characteristics of the primitive being cached and works with changing brush types.</span></span> <span data-ttu-id="50e77-243">它會使用 A8 點陣圖，其中 A8 是一種像素格式，代表8位的 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="50e77-243">It uses an A8 bitmap where A8 is a kind of pixel format which represents an alpha channel with 8 bits.</span></span> <span data-ttu-id="50e77-244">A8 點陣圖適合用來以遮罩的形式繪製幾何/文字。</span><span class="sxs-lookup"><span data-stu-id="50e77-244">A8 bitmaps are useful for drawing geometry/text as a mask.</span></span> <span data-ttu-id="50e77-245">當您必須操作靜態內容的不透明度，而不是自行操作內容時，您可以轉譯、旋轉、扭曲或調整遮罩的不透明度。</span><span class="sxs-lookup"><span data-stu-id="50e77-245">When you must manipulate the opacity of static content , instead of manipulating the content itself, you can translate, rotate, skew, or scale the opacity of the mask.</span></span>

<span data-ttu-id="50e77-246">以下為範例：</span><span class="sxs-lookup"><span data-stu-id="50e77-246">Here's an example:</span></span>


```C++
// Create an opacity bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render to the opacityBitmap.
m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Call the FillOpacityMask method
// Note: for this call to work correctly the anti alias mode must be D2D1_ANTIALIAS_MODE_ALIASED. 
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->FillOpacityMask(
    opacityBitmap.Get(),
    m_contentBrush().Get(),
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS);
```



## <a name="per-primitive-caching-using-geometry-realizations"></a><span data-ttu-id="50e77-247">使用 geometry 實踐的每個基本快取</span><span class="sxs-lookup"><span data-stu-id="50e77-247">Per-primitive caching using geometry realizations</span></span>

<span data-ttu-id="50e77-248">另一項依基本的快取技術，稱為 geometry 實踐，可在處理幾何時提供更大的彈性。</span><span class="sxs-lookup"><span data-stu-id="50e77-248">Another per-primitive caching technique, called geometry realizations, provides greater flexibility when dealing with geometry.</span></span> <span data-ttu-id="50e77-249">當您想要重複繪製別名或防鋸齒型幾何時，將其轉換成幾何實踐並重複繪製實踐，會比重複繪製幾何本身更快速。</span><span class="sxs-lookup"><span data-stu-id="50e77-249">When you want to repeatedly draw aliased or anti-aliased geometries, it is faster to convert them to geometry realizations and repeatedly draw the realizations than it is to repeatedly draw the geometries themselves.</span></span> <span data-ttu-id="50e77-250">幾何實踐通常也會耗用比不透明度遮罩更少的記憶體 (特別是對於大型幾何) 而言，它們對調整的變更較不敏感。</span><span class="sxs-lookup"><span data-stu-id="50e77-250">Geometry realizations also generally consume less memory than opacity masks (especially for large geometries), and they are less sensitive to changes in scale.</span></span> <span data-ttu-id="50e77-251">如需詳細資訊，請參閱 [幾何實踐總覽](geometry-realizations-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="50e77-251">For more information, see [Geometry Realizations Overview](geometry-realizations-overview.md).</span></span>

<span data-ttu-id="50e77-252">以下為範例：</span><span class="sxs-lookup"><span data-stu-id="50e77-252">Here's an example:</span></span>


```C++
    // Compute a flattening tolerance based on the scales at which the realization will be used.
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(...);

    ComPtr<ID2D1GeometryRealization> geometryRealization;

    // Create realization of the filled interior of the geometry.
    m_d2dDeviceContext1->CreateFilledGeometryRealization(
        geometry.Get(),
        flatteningTolerance,
        &geometryRealization
        );

    // In your app's rendering code, draw the geometry realization with a brush.
    m_d2dDeviceContext1->BeginDraw();
    m_d2dDeviceContext1->DrawGeometryRealization(
        geometryRealization.Get(),
        m_brush.Get()
        );
    m_d2dDeviceContext1->EndDraw();
```



## <a name="geometry-rendering"></a><span data-ttu-id="50e77-253">幾何轉譯</span><span class="sxs-lookup"><span data-stu-id="50e77-253">Geometry rendering</span></span>

### <a name="use-specific-draw-primitive-over-draw-geometry"></a><span data-ttu-id="50e77-254">針對繪製幾何使用特定的繪圖基本</span><span class="sxs-lookup"><span data-stu-id="50e77-254">Use specific draw primitive over draw geometry</span></span>

<span data-ttu-id="50e77-255">使用更特定的繪製 *基本* 呼叫，例如透過一般 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry)呼叫的 [**graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-255">Use more specific draw *primitive* calls like [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) over generic [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) calls.</span></span> <span data-ttu-id="50e77-256">這是因為使用 **graphicswindow.drawrectangle** 時，幾何已經是已知的，所以轉譯速度更快。</span><span class="sxs-lookup"><span data-stu-id="50e77-256">This is because with **DrawRectangle**, the geometry is already known so rendering is faster.</span></span>

### <a name="rendering-static-geometry"></a><span data-ttu-id="50e77-257">呈現靜態幾何</span><span class="sxs-lookup"><span data-stu-id="50e77-257">Rendering static geometry</span></span>

<span data-ttu-id="50e77-258">在幾何為靜態的案例中，請使用上述的每一基本快取技術。</span><span class="sxs-lookup"><span data-stu-id="50e77-258">In scenarios where the geometry is static, use the per-primitive caching techniques explained above.</span></span> <span data-ttu-id="50e77-259">不透明度遮罩和幾何實踐可以大幅改善包含靜態幾何的場景呈現速度。</span><span class="sxs-lookup"><span data-stu-id="50e77-259">Opacity masks and geometry realizations can greatly improve the rendering speed of scenes that contain static geometry..</span></span>

### <a name="use-a-multithreaded-device-context"></a><span data-ttu-id="50e77-260">使用多執行緒裝置內容</span><span class="sxs-lookup"><span data-stu-id="50e77-260">Use a multithreaded device context</span></span>

<span data-ttu-id="50e77-261">預期會轉譯大量複雜幾何內容的應用程式，應該考慮在建立 [Direct2D](./direct2d-portal.md)裝置內容時，指定 [**D2D1 \_ 裝置 \_ 內容 \_ 選項來 \_ 啟用 \_ 多 \_ 執行緒 \_ 優化**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_device_context_options)旗標。</span><span class="sxs-lookup"><span data-stu-id="50e77-261">Applications that expect to render significant amounts of complex geometric content should consider specifying the [**D2D1\_DEVICE\_CONTEXT\_OPTIONS\_ENABLE\_MULTI\_THREADED\_OPTIMIZATIONS**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_device_context_options) flag when creating a [Direct2D](./direct2d-portal.md) device context.</span></span> <span data-ttu-id="50e77-262">當指定這個旗標時，Direct2D 會將轉譯分佈到系統上所有的邏輯核心，這可能會大幅降低整體轉譯時間。</span><span class="sxs-lookup"><span data-stu-id="50e77-262">When this flag is specified, Direct2D will distribute rendering across all of the logical cores present on the system, which can significantly decrease overall rendering time.</span></span>

<span data-ttu-id="50e77-263">注意：</span><span class="sxs-lookup"><span data-stu-id="50e77-263">Notes:</span></span>

-   <span data-ttu-id="50e77-264">從 Windows 8.1 起，此旗標只會影響路徑幾何轉譯。</span><span class="sxs-lookup"><span data-stu-id="50e77-264">As of Windows 8.1, this flag only affects path geometry rendering.</span></span> <span data-ttu-id="50e77-265">它對僅包含其他基本類型 (例如文字、點陣圖或幾何實踐) 的場景沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="50e77-265">It has no impact on scenes containing only other primitive types (such as text, bitmaps, or geometry realizations).</span></span>
-   <span data-ttu-id="50e77-266">在 (軟體中轉譯時，此旗標也不會有任何影響，也就是使用變形 Direct3D 裝置) 轉譯時。</span><span class="sxs-lookup"><span data-stu-id="50e77-266">This flag also has no impact when rendering in software (i.e. when rendering with a WARP Direct3D device).</span></span> <span data-ttu-id="50e77-267">若要控制軟體多執行緒，呼叫端在 \_ \_ \_ \_ \_ \_ 建立變形 DIRECT3D 裝置時，應使用 D3D11 建立裝置防止內部執行緒優化旗標。</span><span class="sxs-lookup"><span data-stu-id="50e77-267">To control software multithreading, callers should use the D3D11\_CREATE\_DEVICE\_PREVENT\_INTERNAL\_THREADING\_OPTIMIZATIONS flag when creating the WARP Direct3D device.</span></span>
-   <span data-ttu-id="50e77-268">指定此旗標可能會在轉譯期間增加尖峰工作集，也可能會在已利用多執行緒處理的應用程式中增加執行緒爭用。</span><span class="sxs-lookup"><span data-stu-id="50e77-268">Specifying this flag can increase peak working set during rendering and can also increase thread contention in applications that already take advantage of multithreaded processing.</span></span>

## <a name="drawing-text-with-direct2d"></a><span data-ttu-id="50e77-269">使用 Direct2D 繪製文字</span><span class="sxs-lookup"><span data-stu-id="50e77-269">Drawing text with Direct2D</span></span>

<span data-ttu-id="50e77-270">Direct2D 文字轉譯功能提供兩個部分。</span><span class="sxs-lookup"><span data-stu-id="50e77-270">Direct2D text rendering functionality is offered in two parts.</span></span> <span data-ttu-id="50e77-271">第一個部分（公開為 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 和 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法）可讓呼叫端傳遞字串和格式化參數，或針對多種格式傳遞 DWrite 文字版面設定物件。</span><span class="sxs-lookup"><span data-stu-id="50e77-271">The first part, exposed as the [**ID2D1RenderTarget::DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) and [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, enables a caller to pass either a string and formatting parameters or a DWrite text layout object for multiple formats.</span></span> <span data-ttu-id="50e77-272">這應該適用于大部分的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="50e77-272">This should be suitable for most callers.</span></span> <span data-ttu-id="50e77-273">轉譯文字（公開為 [**ID2D1RenderTarget：:D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) 方法）的第二種方式，為已經知道要轉譯之圖像位置的客戶提供了點陣化。</span><span class="sxs-lookup"><span data-stu-id="50e77-273">The second way to render text, exposed as the [**ID2D1RenderTarget::DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) method, provides rasterization for customers who already know the position of the glyphs they want to render.</span></span> <span data-ttu-id="50e77-274">下列兩個一般規則可協助改善在 Direct2D 中繪製的文字效能。</span><span class="sxs-lookup"><span data-stu-id="50e77-274">The following two general rules can help improve text performance when drawing in Direct2D.</span></span>

### <a name="drawtextlayout-vs-drawtext"></a><span data-ttu-id="50e77-275">DrawTextLayout 與 DrawText 的比較</span><span class="sxs-lookup"><span data-stu-id="50e77-275">DrawTextLayout Vs. DrawText</span></span>

<span data-ttu-id="50e77-276">[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))和 [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)都可讓應用程式輕鬆地轉譯由 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) API 格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="50e77-276">Both [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) and [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) enable an application to easily render text that is formatted by the [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) API.</span></span> <span data-ttu-id="50e77-277">**DrawTextLayout** 會將現有的 [**DWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) 物件繪製至 [**RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)， **DrawText** 會根據傳入的參數，為呼叫端建立 DirectWrite 配置。</span><span class="sxs-lookup"><span data-stu-id="50e77-277">**DrawTextLayout** draws an existing [**DWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) object to the [**RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), and **DrawText** constructs a DirectWrite layout for the caller, based on the parameters that are passed in.</span></span> <span data-ttu-id="50e77-278">如果相同的文字必須轉譯多次，請使用 **DrawTextLayout** 而不是 **DrawText**，因為 **DrawText** 會在每次呼叫它時建立版面配置。</span><span class="sxs-lookup"><span data-stu-id="50e77-278">If the same text has to be rendered multiple times, use **DrawTextLayout** instead of **DrawText**, because **DrawText** creates a layout every time that it is called.</span></span>

### <a name="choosing-the-right-text-rendering-mode"></a><span data-ttu-id="50e77-279">選擇正確的文字呈現模式</span><span class="sxs-lookup"><span data-stu-id="50e77-279">Choosing the right text rendering mode</span></span>

<span data-ttu-id="50e77-280">將文字消除鋸齒模式設定為明確 [**D2D1 \_ 文字 \_ 消除鋸齒 \_ 模式 \_ 灰階**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-280">Set the text antialias mode to [**D2D1\_TEXT\_ANTIALIAS\_MODE\_GRAYSCALE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) explicitly.</span></span> <span data-ttu-id="50e77-281">轉譯灰階文字的品質相當於 ClearType，但速度更快。</span><span class="sxs-lookup"><span data-stu-id="50e77-281">The quality of rendering grayscale text is comparable to ClearType but is much faster.</span></span>

### <a name="caching"></a><span data-ttu-id="50e77-282">快取</span><span class="sxs-lookup"><span data-stu-id="50e77-282">Caching</span></span>

<span data-ttu-id="50e77-283">使用完整場景或每個基本點陣圖快取，例如繪製其他基本專案。</span><span class="sxs-lookup"><span data-stu-id="50e77-283">Use full scene or per primitive bitmap caching like with drawing other primitives.</span></span>

## <a name="clipping-an-arbitrary-shape"></a><span data-ttu-id="50e77-284">裁剪任意圖形</span><span class="sxs-lookup"><span data-stu-id="50e77-284">Clipping an arbitrary shape</span></span>

<span data-ttu-id="50e77-285">這裡的圖顯示將剪輯套用至影像的結果。</span><span class="sxs-lookup"><span data-stu-id="50e77-285">The figure here shows the result of applying a clip to an image.</span></span>

![顯示剪輯前後影像範例的影像。](images/clip.png)

<span data-ttu-id="50e77-287">您可以使用具有幾何遮罩的圖層或具有不透明度筆刷的 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法來取得這個結果。</span><span class="sxs-lookup"><span data-stu-id="50e77-287">You can get this result by using layers with a geometry mask or the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method with an opacity brush.</span></span>

<span data-ttu-id="50e77-288">以下是使用圖層的範例：</span><span class="sxs-lookup"><span data-stu-id="50e77-288">Here's an example that uses a layer:</span></span>


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



<span data-ttu-id="50e77-289">以下是使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法的範例：</span><span class="sxs-lookup"><span data-stu-id="50e77-289">Here's an example that uses the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method:</span></span>


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



<span data-ttu-id="50e77-290">在此程式碼範例中，當您呼叫 PushLayer 方法時，不會傳入應用程式所建立的圖層。</span><span class="sxs-lookup"><span data-stu-id="50e77-290">In this code example, when you call the PushLayer method, you don't pass in an app created layer.</span></span> <span data-ttu-id="50e77-291">Direct2D 會為您建立圖層。</span><span class="sxs-lookup"><span data-stu-id="50e77-291">Direct2D creates a layer for you.</span></span> <span data-ttu-id="50e77-292">Direct2D 可以管理此資源的配置和終結，而不需要應用程式的任何介入。</span><span class="sxs-lookup"><span data-stu-id="50e77-292">Direct2D is able to manage the allocation and destruction of this resource without any involvement from the app.</span></span> <span data-ttu-id="50e77-293">這可讓 Direct2D 在內部重複使用圖層，並套用資源管理優化。</span><span class="sxs-lookup"><span data-stu-id="50e77-293">This allows Direct2D to reuse layers internally and apply resource management optimizations.</span></span>

<span data-ttu-id="50e77-294">在 Windows 8 已對層級使用進行許多優化，建議您盡可能嘗試使用層 Api，而不是 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-294">In Windows 8 many optimizations have been made to the usage of layers and we recommend you try using layer APIs instead of [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) whenever possible.</span></span>

### <a name="pushlayer-in-windows-8"></a><span data-ttu-id="50e77-295">Windows 8 中的 PushLayer</span><span class="sxs-lookup"><span data-stu-id="50e77-295">PushLayer in Windows 8</span></span>

<span data-ttu-id="50e77-296">[**ID2D1DeviceCoNtext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)介面衍生自 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)介面，也是在 Windows 8 中顯示 Direct2D 內容的關鍵。如需此介面的詳細資訊，請參閱 [裝置和裝置](devices-and-device-contexts.md)內容。</span><span class="sxs-lookup"><span data-stu-id="50e77-296">The [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface is derived from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface and is key to displaying Direct2D content in Windows 8, for more information about this interface see [Devices and Device Contexts](devices-and-device-contexts.md).</span></span> <span data-ttu-id="50e77-297">您可以使用裝置內容介面略過呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) 方法，然後將 Null 傳遞至 [**ID2D1DeviceCoNtext：:P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) 方法。</span><span class="sxs-lookup"><span data-stu-id="50e77-297">With the device context interface, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**ID2D1DeviceContext::PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span> <span data-ttu-id="50e77-298">Direct2D 會自動管理圖層資源，並可在圖層和效果圖形之間共用資源。</span><span class="sxs-lookup"><span data-stu-id="50e77-298">Direct2D automatically manages the layer resource and can share resources between layers and effect graphs.</span></span>

### <a name="axis-aligned-clips"></a><span data-ttu-id="50e77-299">軸對齊的剪輯</span><span class="sxs-lookup"><span data-stu-id="50e77-299">Axis-aligned clips</span></span>

<span data-ttu-id="50e77-300">如果要裁剪的區域對齊繪圖介面的軸，而不是任意的。</span><span class="sxs-lookup"><span data-stu-id="50e77-300">If the region to be clipped is aligned to the axis of the drawing surface, instead of arbitrary.</span></span> <span data-ttu-id="50e77-301">此案例適用于使用剪輯矩形而非圖層。</span><span class="sxs-lookup"><span data-stu-id="50e77-301">This case is suited for using a clip rectangle instead of a layer.</span></span> <span data-ttu-id="50e77-302">效能提升比反鋸齒幾何的別名幾何更多。</span><span class="sxs-lookup"><span data-stu-id="50e77-302">The performance gain is more for aliased geometry than antialiased geometry.</span></span> <span data-ttu-id="50e77-303">如需軸對齊剪輯的詳細資訊，請參閱 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) 主題。</span><span class="sxs-lookup"><span data-stu-id="50e77-303">For more info on axis aligned clips, see the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) topic.</span></span>

## <a name="dxgi-interoperability-avoid-frequent-switches"></a><span data-ttu-id="50e77-304">DXGI 互通性：避免頻繁切換</span><span class="sxs-lookup"><span data-stu-id="50e77-304">DXGI interoperability: avoid frequent switches</span></span>

<span data-ttu-id="50e77-305">Direct2D 可與 Direct3D 介面無縫交互操作。</span><span class="sxs-lookup"><span data-stu-id="50e77-305">Direct2D can interoperate seamlessly with Direct3D surfaces.</span></span> <span data-ttu-id="50e77-306">這非常適合用來建立可轉譯2D 和3D 內容混合的應用程式。</span><span class="sxs-lookup"><span data-stu-id="50e77-306">This is very useful for creating applications that render a mixture of 2D and 3D content.</span></span> <span data-ttu-id="50e77-307">但在繪製 Direct2D 和 Direct3D 內容之間的每個切換都會影響效能。</span><span class="sxs-lookup"><span data-stu-id="50e77-307">But each switch between drawing Direct2D and Direct3D content affects performance.</span></span>

<span data-ttu-id="50e77-308">當轉譯為 DXGI 介面時，Direct2D 會在轉譯時儲存 Direct3D 裝置的狀態，並在轉譯完成時加以還原。</span><span class="sxs-lookup"><span data-stu-id="50e77-308">When rendering to a DXGI surface, Direct2D saves the state of the Direct3D devices while rendering and restores it when rendering is completed.</span></span> <span data-ttu-id="50e77-309">每次 Direct2D 轉譯批次完成時，這個儲存和還原的成本以及排清所有2D 作業的成本都是付費的，但是 Direct3D 裝置也不會排清。</span><span class="sxs-lookup"><span data-stu-id="50e77-309">Every time that a batch of Direct2D rendering is completed, the cost of this save and restore and the cost of flushing all the 2D operations are paid, and yet, the Direct3D device is not flushed.</span></span> <span data-ttu-id="50e77-310">因此，若要提高效能，請限制 Direct2D 與 Direct3D 之間的轉譯切換數目。</span><span class="sxs-lookup"><span data-stu-id="50e77-310">Therefore, to increase performance, limit the number of rendering switches between Direct2D and Direct3D.</span></span>

## <a name="know-your-pixel-format"></a><span data-ttu-id="50e77-311">知道您的像素格式</span><span class="sxs-lookup"><span data-stu-id="50e77-311">Know Your Pixel Format</span></span>

<span data-ttu-id="50e77-312">當您建立轉譯目標時，您可以使用 [**D2D1 \_ 圖元 \_ 格式**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) 結構來指定呈現目標所使用的像素格式和 Alpha 模式。</span><span class="sxs-lookup"><span data-stu-id="50e77-312">When you create a render target, you can use the [**D2D1\_PIXEL\_FORMAT**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) structure specify the pixel format and alpha mode used by the render target.</span></span> <span data-ttu-id="50e77-313">Alpha 色板是像素格式的一部分，可指定涵蓋範圍值或不透明度資訊。</span><span class="sxs-lookup"><span data-stu-id="50e77-313">An alpha channel is part of the pixel format that specifies the coverage value or opacity information.</span></span> <span data-ttu-id="50e77-314">如果轉譯目標未使用 Alpha 色板，則應該使用 [**D2D1 \_ Alpha \_ 模式 \_ 忽略**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Alpha 模式來建立它。</span><span class="sxs-lookup"><span data-stu-id="50e77-314">If a render target does not use the alpha channel, it should be created by using the [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) alpha mode.</span></span> <span data-ttu-id="50e77-315">這會讓您花費在轉譯不需要的 Alpha 通道時所花費的時間。</span><span class="sxs-lookup"><span data-stu-id="50e77-315">This spares the time that is spent on rendering an alpha channel that is not needed.</span></span>

<span data-ttu-id="50e77-316">如需像素格式和 Alpha 模式的詳細資訊，請參閱 [支援的像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)。</span><span class="sxs-lookup"><span data-stu-id="50e77-316">For more information about pixel formats and alpha modes, see [Supported Pixel Formats and Alpha Modes](supported-pixel-formats-and-alpha-modes.md).</span></span>

## <a name="scene-complexity"></a><span data-ttu-id="50e77-317">場景複雜性</span><span class="sxs-lookup"><span data-stu-id="50e77-317">Scene Complexity</span></span>

<span data-ttu-id="50e77-318">當您在將呈現的場景中分析效能作用點時，瞭解場景是否為填滿速率系結或端點系結，可提供有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="50e77-318">When you analyze performance hot spots in a scene that will be rendered, knowing whether the scene is fill-rate bound or vertex bound can provide useful information.</span></span>

-   <span data-ttu-id="50e77-319">填滿率：填滿速率是指圖形配接器可轉譯和寫入視訊記憶體的圖元數（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="50e77-319">Fill Rate: Fill rate refers to the number of pixels that a graphics card can render and write to video memory per second.</span></span>
-   <span data-ttu-id="50e77-320">頂點系結：當場景包含許多複雜幾何時，即為頂點系結。</span><span class="sxs-lookup"><span data-stu-id="50e77-320">Vertex Bound: A scene is vertex bound when it contains lots of complex geometry.</span></span>

### <a name="understand-scene-complexity"></a><span data-ttu-id="50e77-321">瞭解場景複雜性</span><span class="sxs-lookup"><span data-stu-id="50e77-321">Understand Scene Complexity</span></span>

<span data-ttu-id="50e77-322">您可以藉由改變轉譯目標的大小來分析場景的複雜度。</span><span class="sxs-lookup"><span data-stu-id="50e77-322">You can analyze your scene complexity by altering the size of the render target.</span></span> <span data-ttu-id="50e77-323">如果顯示效能提升的比例減少轉譯目標的大小，則應用程式會有填滿速率的限制。</span><span class="sxs-lookup"><span data-stu-id="50e77-323">If performance gains are visible for a proportional reduction in size of the render target, then the application is fill-rate bound.</span></span> <span data-ttu-id="50e77-324">否則，場景複雜性就是效能瓶頸。</span><span class="sxs-lookup"><span data-stu-id="50e77-324">Otherwise, the scene complexity is the performance bottleneck.</span></span>

<span data-ttu-id="50e77-325">當場景為填滿速率時，減少轉譯目標的大小可改善效能。</span><span class="sxs-lookup"><span data-stu-id="50e77-325">When a scene is fill-rate bound, reducing the size of the render target can improve the performance.</span></span> <span data-ttu-id="50e77-326">這是因為要轉譯的圖元數會隨著轉譯目標的大小而按比例減少。</span><span class="sxs-lookup"><span data-stu-id="50e77-326">This is because the number of pixels to be rendered will be reduced proportionally with the size of the render target.</span></span>

<span data-ttu-id="50e77-327">當場景是頂點系結時，請降低幾何的複雜度。</span><span class="sxs-lookup"><span data-stu-id="50e77-327">When a scene is vertex bound, reduce the complexity of the geometry.</span></span> <span data-ttu-id="50e77-328">但請記住，這是以影像品質的費用來完成。</span><span class="sxs-lookup"><span data-stu-id="50e77-328">But remember that this is done at the expense of image quality.</span></span> <span data-ttu-id="50e77-329">因此，您應該在所需的品質與所需的效能之間做出謹慎的取捨決策。</span><span class="sxs-lookup"><span data-stu-id="50e77-329">Therefore, a careful tradeoff decision should be made between the desired quality and the performance that is required.</span></span>

## <a name="improving-performance-for-direct2d-printing-apps"></a><span data-ttu-id="50e77-330">改善 Direct2D 列印應用程式的效能</span><span class="sxs-lookup"><span data-stu-id="50e77-330">Improving performance for Direct2D printing apps</span></span>

<span data-ttu-id="50e77-331">[Direct2D](./direct2d-portal.md) 提供與列印的相容性。</span><span class="sxs-lookup"><span data-stu-id="50e77-331">[Direct2D](./direct2d-portal.md) offers compatibility with printing.</span></span> <span data-ttu-id="50e77-332">您可以傳送相同的 Direct2D 繪圖命令 (格式為 Direct2D 命令清單) 至 Direct2D 列印控制項以進行列印，如果您不知道要繪製的裝置，或如何將繪圖轉譯成列印。</span><span class="sxs-lookup"><span data-stu-id="50e77-332">You can send the same Direct2D drawing commands (in the form of Direct2D command lists) to the Direct2D print control for printing, if you don't know what devices you are drawing to, or how the drawing is translated to printing.</span></span>

<span data-ttu-id="50e77-333">您可以進一步微調其 [Direct2D](./direct2d-portal.md) 列印控制項和 Direct2D 繪圖命令的使用方式，以提供更佳效能的列印結果。</span><span class="sxs-lookup"><span data-stu-id="50e77-333">You can further fine-tune their usage of the [Direct2D](./direct2d-portal.md) print control and your Direct2D drawing commands to deliver printing results with better performance.</span></span>

<span data-ttu-id="50e77-334">當 [Direct2D](./direct2d-portal.md) print 控制項看到 Direct2D 程式碼模式時，會導致列印品質或效能降低 (例如，本主題稍後所列的程式碼模式) 提醒您可避免效能問題的情況下，會輸出 debug 訊息。</span><span class="sxs-lookup"><span data-stu-id="50e77-334">The [Direct2D](./direct2d-portal.md) print control outputs debug messages when it sees a Direct2D code pattern that leads to lower printing quality or performance (like, code patterns listed later in this topic) to remind you where you can avoid performance problems.</span></span> <span data-ttu-id="50e77-335">若要查看這些偵錯工具訊息，您需要在程式碼中啟用 [Direct2D Debug 層](direct2ddebuglayer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-335">To see those debug messages, you need to enable [Direct2D Debug Layer](direct2ddebuglayer-portal.md) in your code.</span></span> <span data-ttu-id="50e77-336">請參閱 [偵錯工具訊息](direct2ddebuglayer-debugmessages.md) ，以取得啟用偵錯工具訊息輸出的指示。</span><span class="sxs-lookup"><span data-stu-id="50e77-336">See [Debug Messages](direct2ddebuglayer-debugmessages.md) for instructions to enable debug message output.</span></span>

### <a name="set-the-right-property-values-when-you-create-the-d2d-print-control"></a><span data-ttu-id="50e77-337">當您建立 D2D 列印控制項時，設定正確的屬性值</span><span class="sxs-lookup"><span data-stu-id="50e77-337">Set the right property values when you create the D2D print control</span></span>

<span data-ttu-id="50e77-338">當您建立 [Direct2D](./direct2d-portal.md) 列印控制項時，可以設定三個屬性。</span><span class="sxs-lookup"><span data-stu-id="50e77-338">There are three properties that you can set when you create the [Direct2D](./direct2d-portal.md) print control.</span></span> <span data-ttu-id="50e77-339">其中有兩個屬性會影響 Direct2D 列印控制項處理特定 Direct2D 命令的方式，進而影響整體效能。</span><span class="sxs-lookup"><span data-stu-id="50e77-339">Two of these properties impact how the Direct2D print control handles certain Direct2D commands and in turn impact the overall performance.</span></span>

-   <span data-ttu-id="50e77-340">字型子集模式： [Direct2D](./direct2d-portal.md) 列印控制項會在傳送要列印的頁面之前，在每個頁面中使用這些字型資源。</span><span class="sxs-lookup"><span data-stu-id="50e77-340">Font Subset Mode: The [Direct2D](./direct2d-portal.md) print control subsets font resources used in each page before it sends the page to be printed.</span></span> <span data-ttu-id="50e77-341">此模式可減少列印所需的頁面資源大小。</span><span class="sxs-lookup"><span data-stu-id="50e77-341">This mode reduces the size of page resources needed to print.</span></span> <span data-ttu-id="50e77-342">根據頁面上的字型使用方式，您可以選擇不同的字型子集模式來獲得最佳效能。</span><span class="sxs-lookup"><span data-stu-id="50e77-342">Depending on font usage on the page, you can choose different font subset modes for the best performance.</span></span>
    -   <span data-ttu-id="50e77-343">[**D2D1 \_列印 \_ 字型 \_ 子集 \_ 模式 \_ 預設**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) 會在大部分情況下提供最佳的列印效能。</span><span class="sxs-lookup"><span data-stu-id="50e77-343">[**D2D1\_PRINT\_FONT\_SUBSET\_MODE\_DEFAULT**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) provides the best printing performance in most cases.</span></span> <span data-ttu-id="50e77-344">當設定為此模式時， [Direct2D](./direct2d-portal.md) 列印控制項會使用啟發學習法策略來決定何時要設定字型的子集。</span><span class="sxs-lookup"><span data-stu-id="50e77-344">When set to this mode, the [Direct2D](./direct2d-portal.md) print control uses a heuristic strategy to decide when to subset fonts.</span></span>
    -   <span data-ttu-id="50e77-345">針對具有1或2個頁面的簡短列印工作，建議使用 [**D2D1 \_ 列印 \_ 字型 \_ 子集 \_ 模式 \_ EACHPAGE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) ，其中 [Direct2D](./direct2d-portal.md) 列印控制項會在每個頁面中將字型資源子集及內嵌，然後在頁面列印後捨棄該字型子集。</span><span class="sxs-lookup"><span data-stu-id="50e77-345">For short print jobs with 1 or 2 pages, we recommend [**D2D1\_PRINT\_FONT\_SUBSET\_MODE\_EACHPAGE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) , where the [Direct2D](./direct2d-portal.md) print control subsets and embeds font resources in each page, then discards that font subset after the page prints.</span></span> <span data-ttu-id="50e77-346">此選項可確保每個頁面都能在產生後立即列印，但會稍微增加列印 (所需的頁面資源大小（通常是大型字型子集) ）。</span><span class="sxs-lookup"><span data-stu-id="50e77-346">This option makes sure each page can be printed immediately after it is generated but slightly increases size of page resources needed for printing (with usually large font subsets).</span></span>
    -   <span data-ttu-id="50e77-347">針對具有許多文字頁面和小型字型大小的列印工作 (例如使用單一字型) 的100頁面，我們建議 [**D2D1 \_ 列印 \_ 字型 \_ 子集 \_ 模式 \_ NONE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode)，其中 [Direct2D](./direct2d-portal.md) 列印控制項完全不會子集字型資源; 相反地，它會連同首次使用字型的頁面一起送出原始字型資源，然後重新使用字型資源來取得較新的頁面，而不需要重新傳送這些字型資源。</span><span class="sxs-lookup"><span data-stu-id="50e77-347">For print jobs with many pages of texts and small font sizes (like 100 pages of text that uses a single font), we recommend [**D2D1\_PRINT\_FONT\_SUBSET\_MODE\_NONE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode), where the [Direct2D](./direct2d-portal.md) print control doesn't subset font resources at all; instead, it sends out the original font resources along with the page that first uses the font, and re-uses the font resources for later pages without resending them.</span></span>
-   <span data-ttu-id="50e77-348">點陣 DPI：當 [Direct2D](./direct2d-portal.md) 列印控制項在 DIRECT2D-XPS 轉換期間需要將 Direct2D 命令進行點陣化時，它會使用此 DPI 來進行點陣。</span><span class="sxs-lookup"><span data-stu-id="50e77-348">Rasterization DPI: When the [Direct2D](./direct2d-portal.md) print control needs to rasterize Direct2D commands during Direct2D-XPS conversion, it uses this DPI for rasterization.</span></span> <span data-ttu-id="50e77-349">換句話說，如果頁面沒有任何柵格化的內容，則設定任何 DPI 將不會變更效能和品質。</span><span class="sxs-lookup"><span data-stu-id="50e77-349">In other words, if the page doesn't have any rasterized contents, setting any DPI won't change performance and quality.</span></span> <span data-ttu-id="50e77-350">根據頁面上的柵格化使用方式，您可以選擇不同的柵格化 Dpi，以獲得精確度與效能之間的最佳平衡。</span><span class="sxs-lookup"><span data-stu-id="50e77-350">Depending on rasterization usage on the page, you can choose different rasterization DPIs for the best balance between fidelity and performance.</span></span>
    -   <span data-ttu-id="50e77-351">如果您在建立 [Direct2D](./direct2d-portal.md) 列印控制項時未指定值，則150是預設值，在大部分情況下，這是列印品質和列印效能的最佳平衡。</span><span class="sxs-lookup"><span data-stu-id="50e77-351">150 is the default value if you don't specify a value when you create the [Direct2D](./direct2d-portal.md) print control, which is the best balance of printing quality and printing performance in most cases.</span></span>
    -   <span data-ttu-id="50e77-352">較高的 DPI 值通常會產生更佳的列印品質 (如更詳細的保留) 但較低的效能，因為它會產生較大的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="50e77-352">Higher DPI values usually result in better printing quality (as in more details preserved) but lower performance due to the larger bitmaps it generates.</span></span> <span data-ttu-id="50e77-353">我們不建議任何大於300的 DPI 值，因為這不會導致人類眼睛以視覺化方式可感知額外的資訊。</span><span class="sxs-lookup"><span data-stu-id="50e77-353">We don't recommend any DPI value greater than 300 since that won't introduce extra information visually perceivable by human eyes.</span></span>
    -   <span data-ttu-id="50e77-354">較低的 DPI 可能表示效能較佳，但也可能產生較低的品質。</span><span class="sxs-lookup"><span data-stu-id="50e77-354">Lower DPI may mean better performance but may also produce lower quality.</span></span>

### <a name="avoid-using-certain-direct2d-drawing-patterns"></a><span data-ttu-id="50e77-355">避免使用特定的 Direct2D 繪製模式</span><span class="sxs-lookup"><span data-stu-id="50e77-355">Avoid using certain Direct2D drawing patterns</span></span>

<span data-ttu-id="50e77-356">[Direct2D](./direct2d-portal.md)可以用視覺化方式呈現，以及列印子系統可以在整個列印管線中維護和傳輸的內容之間有一些差異。</span><span class="sxs-lookup"><span data-stu-id="50e77-356">There are differences between what [Direct2D](./direct2d-portal.md) can represent visually and what the print subsystem can maintain and transport along the whole print pipeline.</span></span> <span data-ttu-id="50e77-357">Direct2D 列印控制項會藉由將逼近或柵格化列印子系統原本不支援的 Direct2D 基本專案，來橋接這些間距。</span><span class="sxs-lookup"><span data-stu-id="50e77-357">The Direct2D print control bridges those gaps by either approximating or rasterizing Direct2D primitives that the print subsystem doesn't natively support.</span></span> <span data-ttu-id="50e77-358">這類近似值通常會導致列印精確度較低、列印效能較低，或兩者都有。</span><span class="sxs-lookup"><span data-stu-id="50e77-358">Such approximation usually results in lower printing fidelity, lower printing performance, or both.</span></span> <span data-ttu-id="50e77-359">因此，即使客戶可以針對螢幕和列印轉譯使用相同的繪圖模式，在所有情況下都不是理想的做法。</span><span class="sxs-lookup"><span data-stu-id="50e77-359">Therefore, even though a customer can use the same drawing patterns for both screen and print rendering, it is not ideal in all cases.</span></span> <span data-ttu-id="50e77-360">最好不要盡可能針對列印路徑使用這類 Direct2D 的基本和模式，或者您也可以在圖形化的位置，完全掌控您的品質和柵格化影像的大小。</span><span class="sxs-lookup"><span data-stu-id="50e77-360">It's best not to use such Direct2D primitives and patterns as much as possible for the print path, or to do you own rasterization where you have full control of the quality and the size of the rasterized images.</span></span>

<span data-ttu-id="50e77-361">以下是列印效能和品質不理想的案例清單，而您可能會想要考慮將程式碼路徑改變為最佳列印效能。</span><span class="sxs-lookup"><span data-stu-id="50e77-361">The here is a list of cases where the print performance and quality won't be ideal and the you might want to consider varying the code path for optimal print performance.</span></span>

-   <span data-ttu-id="50e77-362">避免使用 [**D2D1 \_ 基本 \_ blend \_ SOURCEOVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)以外的基本 blend 模式。</span><span class="sxs-lookup"><span data-stu-id="50e77-362">Avoid using primitive blend mode other than [**D2D1\_PRIMITIVE\_BLEND\_SOURCEOVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend).</span></span>
-   <span data-ttu-id="50e77-363">在繪製非 [**D2D1 \_ 複合 \_ 模式 \_ 來源 \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_composite_mode) 的影像以及 **D2D1 \_ 複合 \_ 模式 \_ 目的地 \_** 時，請避免使用撰寫模式。</span><span class="sxs-lookup"><span data-stu-id="50e77-363">Avoid using Composition Modes when drawing an image other than [**D2D1\_COMPOSITE\_MODE\_SOURCE\_OVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_composite_mode) and **D2D1\_COMPOSITE\_MODE\_DESTINATION\_OVER**.</span></span>
-   <span data-ttu-id="50e77-364">避免繪製 GDI 中繼檔案。</span><span class="sxs-lookup"><span data-stu-id="50e77-364">Avoid drawing a GDI Meta File.</span></span>
-   <span data-ttu-id="50e77-365">避免將複製來源背景的層級資源 (呼叫 [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer) ，並將 [**D2D1 \_ layer \_ OPTIONS1 \_ INITIALIZE \_ 從 \_ 背景初始化**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) 為 **D2D1 \_ layer \_ PARAMETERS1** 結構) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-365">Avoid pushing a layer resource that copies the source background (calling [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer) with passing [**D2D1\_LAYER\_OPTIONS1\_INITIALIZE\_FROM\_BACKGROUND**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) to the **D2D1\_LAYER\_PARAMETERS1** struct).</span></span>
-   <span data-ttu-id="50e77-366">避免使用 D2D1 延伸模式的夾具來建立點陣圖筆刷或影像筆刷 \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="50e77-366">Avoid creating Bitmap Brush or Image Brush with D2D1\_EXTEND\_MODE\_CLAMP.</span></span> <span data-ttu-id="50e77-367">\_ \_ \_ 如果您不在意任何 (（例如）所系結的影像以外的圖元，建議您使用 D2D1 延伸模式鏡像，而附加至筆刷的影像已知大於填滿的目的地區域) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-367">We recommend you use D2D1\_EXTEND\_MODE\_MIRROR if don't care about pixels outside of the image bound at all (like, the image attached to the brush is known to be larger than the filled target region).</span></span>
-   <span data-ttu-id="50e77-368">避免使用 [透視轉換](3d-perspective-transform.md)繪製點陣圖。</span><span class="sxs-lookup"><span data-stu-id="50e77-368">Avoid drawing Bitmaps with [Perspective Transforms](3d-perspective-transform.md).</span></span>

### <a name="draw-text-in-a-direct-and-plain-way"></a><span data-ttu-id="50e77-369">以直接且簡單的方式繪製文字</span><span class="sxs-lookup"><span data-stu-id="50e77-369">Draw text in a direct and plain way</span></span>

<span data-ttu-id="50e77-370">當轉譯文字以顯示，以提升效能及/或更佳的視覺品質時，Direct2D 有數個優化。</span><span class="sxs-lookup"><span data-stu-id="50e77-370">Direct2D has several optimizations when rendering texts to display for better performance and/or better visual quality.</span></span> <span data-ttu-id="50e77-371">但並非所有優化都能改善列印效能和品質，因為紙張列印通常是以更高的 DPI 呈現，而列印並不需要容納動畫等案例。</span><span class="sxs-lookup"><span data-stu-id="50e77-371">But not all optimizations improve the printing performance and quality since the printing on paper is usually in a much higher DPI, and printing does not need to accommodate scenarios like animation.</span></span> <span data-ttu-id="50e77-372">因此，我們建議您直接繪製原始文字或字元，並在建立要列印的命令清單時，避免下列任何優化。</span><span class="sxs-lookup"><span data-stu-id="50e77-372">So, we recommend you draw the original text or glyphs directly and avoid any of the following optimizations when creating the command list for printing.</span></span>

-   <span data-ttu-id="50e77-373">避免使用 [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask) 方法來繪製文字。</span><span class="sxs-lookup"><span data-stu-id="50e77-373">Avoid drawing text with the [**FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask) method.</span></span>
-   <span data-ttu-id="50e77-374">避免在別名模式中繪製文字。</span><span class="sxs-lookup"><span data-stu-id="50e77-374">Avoid drawing text in Aliased Mode.</span></span>

### <a name="draw-the-original-bitmaps-when-possible"></a><span data-ttu-id="50e77-375">盡可能繪製原始點陣圖</span><span class="sxs-lookup"><span data-stu-id="50e77-375">Draw the original bitmaps when possible</span></span>

<span data-ttu-id="50e77-376">如果目標點陣圖是 JPEG、PNG、TIFF 或 JPEG XR，您可以從磁片檔案或記憶體內資料流程建立 WIC 點陣圖，然後使用 [**ID2D1DeviceCoNtext：： CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))從該 WIC 點陣圖建立 [Direct2D](./direct2d-portal.md)點陣圖，最後直接將該 Direct2D 點陣圖傳遞給 Direct2D 列印控制項，而不需進一步操作。</span><span class="sxs-lookup"><span data-stu-id="50e77-376">If the target bitmap is a JPEG, PNG, TIFF, or JPEG-XR, you can create a WIC bitmap either from a disk file or from an in-memory stream, then create a [Direct2D](./direct2d-portal.md) bitmap from that WIC bitmap using [**ID2D1DeviceContext::CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1)), and finally directly pass that Direct2D bitmap to the Direct2D print control without further manipulation.</span></span> <span data-ttu-id="50e77-377">如此一來，Direct2D 列印控制項就能夠重複使用點陣圖串流，這通常會略過多餘的點陣圖編碼和解碼) ，以更佳的列印效能 (，並在) 時保留點陣圖中的中繼資料（例如色彩設定檔）時，提供更好的列印品質 (。</span><span class="sxs-lookup"><span data-stu-id="50e77-377">By doing so, the Direct2D print control is able to reuse the bitmap stream, which usually leads to better printing performance (by skipping redundant bitmap encoding and decoding), and better printing quality (when metadata, such as color profiles, in the bitmap will be preserved).</span></span>

<span data-ttu-id="50e77-378">繪製原始點陣圖可為應用程式提供下列優點。</span><span class="sxs-lookup"><span data-stu-id="50e77-378">Drawing the original bitmap provides the following benefit for applications.</span></span>

-   <span data-ttu-id="50e77-379">一般情況下， [Direct2D](./direct2d-portal.md) 列印會保留原始資訊 (而不會遺失或雜訊) 直到管線中的延遲為止，特別是當應用程式不知道 (或不想) 知道列印管線的詳細資料時 (像是列印到的印表機、目標印表機的 DPI，以及) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-379">In general, [Direct2D](./direct2d-portal.md) print preserves the original information (without loss or noise) until late in the pipeline, especially when apps don't know (or do not want to know) the details of the print pipeline (like which printer it is printing to, what DPI is the target printer, and so on).</span></span>
-   <span data-ttu-id="50e77-380">在許多情況下，延遲點陣圖柵格化表示較佳的效能 (例如，將96DPI 相片列印到600DPI 印表機) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-380">In many cases, delaying bitmap rasterization means better performance (like when printing an 96dpi photo to a 600dpi printer).</span></span>
-   <span data-ttu-id="50e77-381">在某些情況下，傳遞原始影像是接受高精確度 (的唯一方法，例如內嵌色彩設定檔) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-381">In certain cases, passing the original images is the only way to honor high fidelity (like embedded color profiles).</span></span>

<span data-ttu-id="50e77-382">不過，您無法選擇這樣的優化，因為：</span><span class="sxs-lookup"><span data-stu-id="50e77-382">However, an you can't opt in such optimization because:</span></span>

-   <span data-ttu-id="50e77-383">藉由查詢印表機資訊和早期的點陣化，您可以完全掌控紙上的最終外觀，來點陣化內容。</span><span class="sxs-lookup"><span data-stu-id="50e77-383">By querying printer info and early rasterization, you can rasterize contents themselves with full control of the final appearance on paper.</span></span>
-   <span data-ttu-id="50e77-384">在某些情況下，早期的點陣化實際上可能會改善應用程式的端對端效能 (例如列印錢包大小的相片) 。</span><span class="sxs-lookup"><span data-stu-id="50e77-384">In certain cases, early rasterization might actually improves an app’s end-to-end performance (like printing wallets-size photos).</span></span>
-   <span data-ttu-id="50e77-385">在某些情況下，傳遞原始點陣圖需要大幅變更現有的程式碼架構 (例如，影像延遲載入，以及在特定應用程式) 中找到的資源更新路徑。</span><span class="sxs-lookup"><span data-stu-id="50e77-385">In certain cases, passing the original bitmaps require significant change of existing code architecture (like image delay loading and resource update paths found in certain applications).</span></span>

## <a name="conclusion"></a><span data-ttu-id="50e77-386">結論</span><span class="sxs-lookup"><span data-stu-id="50e77-386">Conclusion</span></span>

<span data-ttu-id="50e77-387">雖然 Direct2D 是硬體加速的，且適用于高效能，但您必須正確使用這些功能才能將輸送量最大化。</span><span class="sxs-lookup"><span data-stu-id="50e77-387">Although Direct2D is hardware accelerated and is meant for high performance, you must use the features correctly to maximize throughput.</span></span> <span data-ttu-id="50e77-388">我們在這裡探討的技巧衍生自研究一般案例，可能不適用於所有應用程式案例。</span><span class="sxs-lookup"><span data-stu-id="50e77-388">The techniques we looked at here are derived from studying common scenarios and might not apply to all application scenarios.</span></span>

 

 
