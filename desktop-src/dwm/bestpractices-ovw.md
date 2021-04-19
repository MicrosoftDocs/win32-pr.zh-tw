---
title: 效能考慮和最佳作法
description: 本主題提供一組使用桌面視窗管理員 (DWM) Api 的最佳做法。
ms.assetid: 5b1f6ff8-1d3f-4a70-8efd-90f8802e8532
keywords:
- 桌面視窗管理員 (DWM) 、最佳作法
- DWM (桌面視窗管理員) 、最佳作法
- 桌面視窗管理員 (DWM) 、應用程式實務
- DWM (桌面視窗管理員) ，應用程式實務
- 桌面視窗管理員 (DWM) 、繪圖實務
- DWM (桌面視窗管理員) 、繪製實務
- 桌面視窗管理員 (DWM) ，模糊背後效果
- DWM (桌面視窗管理員) ，模糊背後效果
- 應用程式實務
- 繪圖實務
- 模糊背後效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec76a4920a91f9502940e866d58641a2550d9354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106999803"
---
# <a name="performance-considerations-and-best-practices"></a><span data-ttu-id="105a0-114">效能考慮和最佳作法</span><span class="sxs-lookup"><span data-stu-id="105a0-114">Performance Considerations and Best Practices</span></span>

<span data-ttu-id="105a0-115">本主題提供一組使用桌面視窗管理員 (DWM) Api 的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="105a0-115">This topic presents a set of best practices for using the Desktop Window Manager (DWM) APIs.</span></span>

<span data-ttu-id="105a0-116">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="105a0-116">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="105a0-117">DWM 的應用程式實務</span><span class="sxs-lookup"><span data-stu-id="105a0-117">Application Practices for DWM</span></span>](#application-practices-for-dwm)
-   [<span data-ttu-id="105a0-118">DWM 的繪圖實務</span><span class="sxs-lookup"><span data-stu-id="105a0-118">Drawing Practices for DWM</span></span>](#drawing-practices-for-dwm)
-   [<span data-ttu-id="105a0-119">DWM Blur-Behind 用戶端區域</span><span class="sxs-lookup"><span data-stu-id="105a0-119">DWM Blur-Behind Client Region</span></span>](#dwm-blur-behind-client-region)

## <a name="application-practices-for-dwm"></a><span data-ttu-id="105a0-120">DWM 的應用程式實務</span><span class="sxs-lookup"><span data-stu-id="105a0-120">Application Practices for DWM</span></span>

<span data-ttu-id="105a0-121">如果您的應用程式處理每英寸的點 (DPI) 調整，您可以將應用程式宣告為 DPI 感知並防止自動調整，方法是在程式的資訊清單中設定 DPI 感知旗標，或在程式初始化期間呼叫 [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) 函式。</span><span class="sxs-lookup"><span data-stu-id="105a0-121">If your application handles dots per inch (dpi) scaling, you can declare an application as dpi-aware and prevent automatic scaling by setting the dpi-aware flag in the program's manifest or by calling the [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function during program initialization.</span></span>

<span data-ttu-id="105a0-122">開啟了 DWM 組合之後，隱藏的應用程式就不會再收到 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，也不會被要求重新呈現。</span><span class="sxs-lookup"><span data-stu-id="105a0-122">With DWM composition turned on, obscured applications no longer receive [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) messages and are not asked to re-render.</span></span> <span data-ttu-id="105a0-123">每個視窗的內容都已經可用來撰寫螢幕影像。</span><span class="sxs-lookup"><span data-stu-id="105a0-123">Each window's content is already available to compose the screen image.</span></span>

<span data-ttu-id="105a0-124">最上層的 [**WS \_ ex \_ 透明**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 視窗應該結合 **WS \_ ex \_ 分層** 樣式來進行點擊測試。</span><span class="sxs-lookup"><span data-stu-id="105a0-124">Top-level [**WS\_EX\_TRANSPARENT**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) windows should be combined with a **WS\_EX\_LAYERED** style for the purposes of hit testing.</span></span> <span data-ttu-id="105a0-125">**WS \_例如 \_ ，在傳統** 上，沒有重新導向的一般情況下，適用于屬於相同執行緒的 windows 階層中的子視窗，但不適合最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="105a0-125">**WS\_EX\_TRANSPARENT** in the classic sense, without redirection, is useful for child windows in a hierarchy of windows that belong to the same thread, but is not intended for top-level windows.</span></span>

<span data-ttu-id="105a0-126">使用區域或分層來建立成形或混合式視窗。</span><span class="sxs-lookup"><span data-stu-id="105a0-126">Use regions or layering to create shaped or blended windows.</span></span> <span data-ttu-id="105a0-127">請注意，在 Windows Vista 和更新版本的 Windows 中，自訂繪圖只是最上層視窗的一部分，並不會在 undrawn 區域中提供所需的過時內容。</span><span class="sxs-lookup"><span data-stu-id="105a0-127">Note that in Windows Vista and later versions of Windows, custom drawing only part of a top-level window will not provide the desired stale content in undrawn regions.</span></span>

<span data-ttu-id="105a0-128">您可以使用 [**GetDCOrgEx**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) 之類的 api 來判斷特定的實際值。</span><span class="sxs-lookup"><span data-stu-id="105a0-128">APIs such as [**GetDCOrgEx**](/windows/desktop/api/wingdi/nf-wingdi-getdcorgex) can be used to determine certain actual values.</span></span> <span data-ttu-id="105a0-129">如果您在重新導向的視窗中有 (DC) 的裝置內容， **GetDCOrgEx** 所傳回的原始來源將不會與畫面上視窗的原點相符。</span><span class="sxs-lookup"><span data-stu-id="105a0-129">If you have a device context (DC) for a redirected window, the origin returned by **GetDCOrgEx** will not match the origin of your window on the screen.</span></span> <span data-ttu-id="105a0-130">來源會改為視窗的後置緩衝區介面： (0，0) 。</span><span class="sxs-lookup"><span data-stu-id="105a0-130">The origin will instead be the origin of the back-buffer surface for your window: (0, 0).</span></span>

<span data-ttu-id="105a0-131">當所有其他動作都失敗時，藉由呼叫 [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) 函數來停用視窗轉譯。</span><span class="sxs-lookup"><span data-stu-id="105a0-131">When all else fails, disable window rendering by calling the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function.</span></span>

## <a name="drawing-practices-for-dwm"></a><span data-ttu-id="105a0-132">DWM 的繪圖實務</span><span class="sxs-lookup"><span data-stu-id="105a0-132">Drawing Practices for DWM</span></span>

<span data-ttu-id="105a0-133">避免直接繪製至主要顯示介面。</span><span class="sxs-lookup"><span data-stu-id="105a0-133">Avoid drawing directly to the primary display surface.</span></span> <span data-ttu-id="105a0-134">這麼做會強制 DWM 停用組合，直到您的應用程式放開主要裝置介面為止。</span><span class="sxs-lookup"><span data-stu-id="105a0-134">Doing so will force the DWM to disable composition until your application releases the primary device surface.</span></span>

<span data-ttu-id="105a0-135">評估您的應用程式是否必須提供自己的雙重緩衝。</span><span class="sxs-lookup"><span data-stu-id="105a0-135">Evaluate whether your application must provide its own double buffering.</span></span> <span data-ttu-id="105a0-136">DWM 會有效地雙重緩衝內容，並將視窗呈現在單一框架中。</span><span class="sxs-lookup"><span data-stu-id="105a0-136">The DWM effectively double buffers content and presents the window in a single frame.</span></span>

<span data-ttu-id="105a0-137">避免讀取或寫入至顯示 DC。</span><span class="sxs-lookup"><span data-stu-id="105a0-137">Avoid reading from or writing to a display DC.</span></span> <span data-ttu-id="105a0-138">雖然 DWM 支援，但因為效能降低，所以不建議使用。</span><span class="sxs-lookup"><span data-stu-id="105a0-138">Although supported by DWM, we do not recommend it because of decreased performance.</span></span>

<span data-ttu-id="105a0-139">避免在非工作區中繪圖。</span><span class="sxs-lookup"><span data-stu-id="105a0-139">Avoid drawing in the non-client area.</span></span> <span data-ttu-id="105a0-140">雖然此區域可以由應用程式存取，而 Microsoft WIN32 API 也支援繪圖，但是這樣做可能會導致視窗遺失任何半透明框線。</span><span class="sxs-lookup"><span data-stu-id="105a0-140">Although this area can be accessed by the application, and drawing there is supported by the Microsoft Win32 API, doing this can cause the window to lose any glass border it has.</span></span>

<span data-ttu-id="105a0-141">除非 Windows 圖形裝置介面不會重迭，否則請避免混用 Windows (GDI) 和 Microsoft DirectX。</span><span class="sxs-lookup"><span data-stu-id="105a0-141">Avoid mixing Windows Graphics Device Interface (GDI) and Microsoft DirectX unless they do not overlap.</span></span> <span data-ttu-id="105a0-142">如果需要混合，請將 GDI 內容繪製到 DirectX 軟體介面，並在組合到畫面之前將其合併，或在不同的視窗中繪製。</span><span class="sxs-lookup"><span data-stu-id="105a0-142">If mixing is necessary, either draw the GDI content into a DirectX software surface and combine them before composing to the screen, or else draw them in separate windows.</span></span>

<span data-ttu-id="105a0-143">使用 [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) 或 [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) 函式，而不是使用 Windows gdi + 來呈現您的繪圖以進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="105a0-143">Use [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) or [**StretchBlt**](/windows/desktop/api/wingdi/nf-wingdi-stretchblt) function instead of Windows GDI+ to present your drawing for rendering.</span></span> <span data-ttu-id="105a0-144">GDI + 以軟體轉譯一次轉譯一個掃描行。</span><span class="sxs-lookup"><span data-stu-id="105a0-144">GDI+ renders one scan line at a time with software rendering.</span></span> <span data-ttu-id="105a0-145">這可能會導致您的應用程式發生閃爍。</span><span class="sxs-lookup"><span data-stu-id="105a0-145">This can cause flickering in your applications.</span></span>

## <a name="dwm-blur-behind-client-region"></a><span data-ttu-id="105a0-146">DWM Blur-Behind 用戶端區域</span><span class="sxs-lookup"><span data-stu-id="105a0-146">DWM Blur-Behind Client Region</span></span>

<span data-ttu-id="105a0-147">轉譯模糊後變效果是 CPU 和圖形處理器 (GPU) 的大量資源操作。</span><span class="sxs-lookup"><span data-stu-id="105a0-147">Rendering the blur-behind effect is a resource-intensive operation for both the CPU and the graphics processing unit (GPU).</span></span> <span data-ttu-id="105a0-148">應用程式開發人員呼籲考慮使用用戶端區域模糊的含意，讓它不會消耗過多的資源。</span><span class="sxs-lookup"><span data-stu-id="105a0-148">Application developers are urged to consider the implications of using client-area blur so that it does not consume excessive resources.</span></span> <span data-ttu-id="105a0-149">在下列情況下，請特別注意：</span><span class="sxs-lookup"><span data-stu-id="105a0-149">You should use particular caution in the following cases:</span></span>

-   <span data-ttu-id="105a0-150">當您預期用戶端區域模糊的大小變得很明顯，即使沒有任何更新會出現在模糊的區域內也是一樣。</span><span class="sxs-lookup"><span data-stu-id="105a0-150">When you expect the size of the client-area blur to be significant, even if no updates will occur in the blurred area itself.</span></span> <span data-ttu-id="105a0-151">如果在視窗的模糊區域下發生任何更新，就必須轉譯模糊，以產生 CPU 和 GPU 成本。</span><span class="sxs-lookup"><span data-stu-id="105a0-151">The blur has to be rendered in case any updates occur under the blurred area of the window, which incurs CPU and GPU costs.</span></span> <span data-ttu-id="105a0-152">此外，視窗的視窗作業 (移動/調整大小/轉換) 會產生更多成本。</span><span class="sxs-lookup"><span data-stu-id="105a0-152">In addition, window operations on the window (move/resize/transitions) will incur more costs.</span></span>
-   <span data-ttu-id="105a0-153">當您預期模糊的用戶端區域有重大更新時。</span><span class="sxs-lookup"><span data-stu-id="105a0-153">When you expect significant updates in the blurred client area.</span></span> <span data-ttu-id="105a0-154">這將需要在每次更新時重新繪製模糊，並耗用過度的資源。</span><span class="sxs-lookup"><span data-stu-id="105a0-154">This will require a repaint of the blur on every update and consume excessive resources.</span></span>
-   <span data-ttu-id="105a0-155">如果模糊預期會涵蓋重要區域，而且也預期會有該區域的更新，強烈建議您不要模糊工作區。</span><span class="sxs-lookup"><span data-stu-id="105a0-155">If the blur is expected to cover a significant area, and updates to that area are also expected, we strongly recommended that you do not blur the client area.</span></span>

 

 