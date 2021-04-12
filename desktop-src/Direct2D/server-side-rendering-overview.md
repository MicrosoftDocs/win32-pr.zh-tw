---
title: 使用 Direct2D 進行 Server-Side 轉譯
description: 描述如何使用 Direct2D 進行伺服器端轉譯。
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D，伺服器端轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375557"
---
# <a name="using-direct2d-for-server-side-rendering"></a><span data-ttu-id="98773-104">使用 Direct2D 進行 Server-Side 轉譯</span><span class="sxs-lookup"><span data-stu-id="98773-104">Using Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="98773-105">Direct2D 適用于需要在 Windows Server 上進行伺服器端轉譯的圖形應用程式。</span><span class="sxs-lookup"><span data-stu-id="98773-105">Direct2D is well-suited for graphics applications that require server-side rendering on Windows Server.</span></span> <span data-ttu-id="98773-106">本總覽說明使用 Direct2D 進行伺服器端轉譯的基本概念。</span><span class="sxs-lookup"><span data-stu-id="98773-106">This overview describes the basics of using Direct2D for server-side rendering.</span></span> <span data-ttu-id="98773-107">它包含下列區段：</span><span class="sxs-lookup"><span data-stu-id="98773-107">It contains the following sections:</span></span>

-   [<span data-ttu-id="98773-108">Server-Side 轉譯的需求</span><span class="sxs-lookup"><span data-stu-id="98773-108">Requirements for Server-Side Rendering</span></span>](#requirements-for-server-side-rendering)
-   [<span data-ttu-id="98773-109">可用 Api 的選項</span><span class="sxs-lookup"><span data-stu-id="98773-109">Options for Available APIs</span></span>](#options-for-available-apis)
    -   [<span data-ttu-id="98773-110">GDI</span><span class="sxs-lookup"><span data-stu-id="98773-110">GDI</span></span>](#gdi)
    -   [<span data-ttu-id="98773-111">GDI+</span><span class="sxs-lookup"><span data-stu-id="98773-111">GDI+</span></span>](#gdi)
    -   [<span data-ttu-id="98773-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="98773-112">Direct2D</span></span>](#using-direct2d-for-server-side-rendering)
-   [<span data-ttu-id="98773-113">如何使用 Direct2D 進行 Server-Side 轉譯</span><span class="sxs-lookup"><span data-stu-id="98773-113">How to Use Direct2D for Server-Side Rendering</span></span>](#how-to-use-direct2d-for-server-side-rendering)
    -   [<span data-ttu-id="98773-114">軟體轉譯</span><span class="sxs-lookup"><span data-stu-id="98773-114">Software Rendering</span></span>](#software-rendering)
    -   [<span data-ttu-id="98773-115">多執行緒</span><span class="sxs-lookup"><span data-stu-id="98773-115">Multithreading</span></span>](#multithreading)
    -   [<span data-ttu-id="98773-116">產生點陣圖檔案</span><span class="sxs-lookup"><span data-stu-id="98773-116">Generating a Bitmap File</span></span>](#generating-a-bitmap-file)
-   [<span data-ttu-id="98773-117">結論</span><span class="sxs-lookup"><span data-stu-id="98773-117">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="98773-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="98773-118">Related topics</span></span>](#related-topics)

## <a name="requirements-for-server-side-rendering"></a><span data-ttu-id="98773-119">Server-Side 轉譯的需求</span><span class="sxs-lookup"><span data-stu-id="98773-119">Requirements for Server-Side Rendering</span></span>

<span data-ttu-id="98773-120">以下是圖表伺服器的一般案例：圖表和圖形會轉譯在伺服器上，並以點陣圖形式傳遞，以回應 Web 要求。</span><span class="sxs-lookup"><span data-stu-id="98773-120">The following is a typical scenario for a chart server: charts and graphics are rendered on a server and delivered as bitmaps in response to Web requests.</span></span> <span data-ttu-id="98773-121">伺服器可能具有低端圖形介面卡，或沒有任何圖形卡。</span><span class="sxs-lookup"><span data-stu-id="98773-121">The server might be equipped with a low-end graphics card or no graphics card at all.</span></span>

<span data-ttu-id="98773-122">此案例會顯示三個應用程式需求。</span><span class="sxs-lookup"><span data-stu-id="98773-122">This scenario reveals three application requirements.</span></span> <span data-ttu-id="98773-123">首先，應用程式必須有效率地處理多個並行要求，尤其是在多核心伺服器上。</span><span class="sxs-lookup"><span data-stu-id="98773-123">First, the application must handle multiple concurrent requests efficiently, especially on multicore servers.</span></span> <span data-ttu-id="98773-124">第二，應用程式必須在具有低終端圖形配接器或沒有圖形配接器的伺服器上執行時，使用軟體轉譯。</span><span class="sxs-lookup"><span data-stu-id="98773-124">Second, the application must use software rendering when running on servers with a low-end graphics card or no graphics card.</span></span> <span data-ttu-id="98773-125">最後，應用程式必須在會話0中以服務的形式執行，如此就不需要使用者登入。</span><span class="sxs-lookup"><span data-stu-id="98773-125">Finally, the application must run as a service in Session 0 so that it does not require a user to be logged in.</span></span> <span data-ttu-id="98773-126">如需會話0的詳細資訊，請參閱對 [Windows 中的服務和驅動程式進行會話0隔離的影響](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx)。</span><span class="sxs-lookup"><span data-stu-id="98773-126">For more information about Session 0, see [Impact of Session 0 Isolation on Services and Drivers in Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span></span>

## <a name="options-for-available-apis"></a><span data-ttu-id="98773-127">可用 Api 的選項</span><span class="sxs-lookup"><span data-stu-id="98773-127">Options for Available APIs</span></span>

<span data-ttu-id="98773-128">伺服器端呈現有三個選項： GDI、GDI + 和 Direct2D。</span><span class="sxs-lookup"><span data-stu-id="98773-128">There are three options for server-side rendering: GDI, GDI+ and Direct2D.</span></span> <span data-ttu-id="98773-129">如同 GDI 和 GDI +，Direct2D 是原生2D 轉譯 API，可讓應用程式更充分掌控圖形裝置的使用。</span><span class="sxs-lookup"><span data-stu-id="98773-129">Like GDI and GDI+, Direct2D is a native 2D rendering API that gives applications more control over the use of graphics devices.</span></span> <span data-ttu-id="98773-130">此外，Direct2D 可唯一支援單一執行緒和多執行緒處理站。</span><span class="sxs-lookup"><span data-stu-id="98773-130">In addition, Direct2D uniquely supports a single-threaded and a multithreaded factory.</span></span> <span data-ttu-id="98773-131">下列各節會根據繪圖品質和多執行緒伺服器端轉譯來比較每個 API。</span><span class="sxs-lookup"><span data-stu-id="98773-131">The following sections compare each API in terms of drawing qualities and multithreaded server-side rendering.</span></span>

### <a name="gdi"></a><span data-ttu-id="98773-132">GDI</span><span class="sxs-lookup"><span data-stu-id="98773-132">GDI</span></span>

<span data-ttu-id="98773-133">與 Direct2D 和 GDI + 不同的是，GDI 不支援高品質的繪圖功能。</span><span class="sxs-lookup"><span data-stu-id="98773-133">Unlike Direct2D and GDI+, GDI does not support high-quality drawing features.</span></span> <span data-ttu-id="98773-134">比方說，GDI 不支援建立平滑線的消除鋸齒功能，而且只對透明度的支援有限。</span><span class="sxs-lookup"><span data-stu-id="98773-134">For instance, GDI does not support antialiasing for creating smooth lines and has only limited support for transparency.</span></span> <span data-ttu-id="98773-135">Direct2D 會根據 Windows 7 和 Windows Server 2008 R2 上的圖形效能測試結果，以更有效率的方式調整，而不是在 GDI 中重新設計鎖定。</span><span class="sxs-lookup"><span data-stu-id="98773-135">Based on the graphics performance test results on Windows 7 and Windows Server 2008 R2, Direct2D scales more efficiently than GDI, despite the redesign of locks in GDI.</span></span> <span data-ttu-id="98773-136">如需這些測試結果的詳細資訊，請參閱 [工程 Windows 7 圖形效能](/archive/blogs/e7/engineering-windows-7-graphics-performance)。</span><span class="sxs-lookup"><span data-stu-id="98773-136">For more information about these test results, see [Engineering Windows 7 Graphics Performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span></span>

<span data-ttu-id="98773-137">此外，使用 GDI 的應用程式限制為每個進程10240個 GDI 控制碼，以及每個會話65536個 GDI 控制碼。</span><span class="sxs-lookup"><span data-stu-id="98773-137">In addition, applications using GDI are limited to 10240 GDI handles per process and 65536 GDI handles per session.</span></span> <span data-ttu-id="98773-138">原因是，內部 Windows 使用16位字組來儲存每個會話之控制碼的索引。</span><span class="sxs-lookup"><span data-stu-id="98773-138">The reason is that internally Windows uses a 16-bit WORD to store the index of handles for each session.</span></span>

### <a name="gdi"></a><span data-ttu-id="98773-139">GDI+</span><span class="sxs-lookup"><span data-stu-id="98773-139">GDI+</span></span>

<span data-ttu-id="98773-140">雖然 GDI + 支援高品質繪圖的消除鋸齒和 Alpha 混色，但在伺服器案例中，GDI + 的主要問題在於它不支援在會話0中執行。</span><span class="sxs-lookup"><span data-stu-id="98773-140">While GDI+ supports antialiasing and alpha blending for high-quality drawing, the main problem with GDI+ for server-scenarios is that it does not support running in Session 0.</span></span> <span data-ttu-id="98773-141">因為會話0只支援非互動式功能，所以直接或間接與顯示裝置互動的函式將會收到錯誤。</span><span class="sxs-lookup"><span data-stu-id="98773-141">Since Session 0 only supports non-interactive functionality, functions that directly or indirectly interact with display devices will therefore receive errors.</span></span> <span data-ttu-id="98773-142">函式的特定範例不僅包括處理顯示裝置的程式，也包括間接處理設備磁碟機的函式。</span><span class="sxs-lookup"><span data-stu-id="98773-142">Specific examples of functions include not only those dealing with display devices, but also those indirectly dealing with device drivers.</span></span>

<span data-ttu-id="98773-143">與 GDI 類似，GDI + 受限於其鎖定機制。</span><span class="sxs-lookup"><span data-stu-id="98773-143">Similar to GDI, GDI+ is limited by its locking mechanism.</span></span> <span data-ttu-id="98773-144">在 Windows 7 和 Windows Server 2008 R2 中，GDI + 中的鎖定機制與舊版相同。</span><span class="sxs-lookup"><span data-stu-id="98773-144">The locking mechanisms in GDI+ are the same in Windows 7 and Windows Server 2008 R2 as in previous versions.</span></span>

### <a name="direct2d"></a><span data-ttu-id="98773-145">Direct2D</span><span class="sxs-lookup"><span data-stu-id="98773-145">Direct2D</span></span>

<span data-ttu-id="98773-146">Direct2D 是一種硬體加速、即時模式、2D 圖形 API，可提供高效能和高品質的呈現。</span><span class="sxs-lookup"><span data-stu-id="98773-146">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering.</span></span> <span data-ttu-id="98773-147">它提供單一執行緒和多執行緒處理站，以及進行課程更精細的軟體轉譯的線性調整。</span><span class="sxs-lookup"><span data-stu-id="98773-147">It offers a single-threaded and a multithreaded factory and the linear scaling of course-grained software rendering.</span></span>

<span data-ttu-id="98773-148">若要這樣做，Direct2D 會定義根 factory 介面。</span><span class="sxs-lookup"><span data-stu-id="98773-148">To do this, Direct2D defines a root factory interface.</span></span> <span data-ttu-id="98773-149">作為規則，在處理站上建立的物件只能與其他從相同 factory 建立的物件搭配使用。</span><span class="sxs-lookup"><span data-stu-id="98773-149">As a rule, an object created on a factory can only be used with other objects created from the same factory.</span></span> <span data-ttu-id="98773-150">呼叫端可以在建立時要求單一執行緒或多執行緒處理站。</span><span class="sxs-lookup"><span data-stu-id="98773-150">The caller can request either a single-threaded or a multithreaded factory when it is created.</span></span> <span data-ttu-id="98773-151">如果要求單一執行緒 factory，則不會執行任何鎖定執行緒。</span><span class="sxs-lookup"><span data-stu-id="98773-151">If a single-threaded factory is requested, then no locking of threads is performed.</span></span> <span data-ttu-id="98773-152">如果呼叫端要求多執行緒處理站，則每次呼叫 Direct2D 時，就會取得 factory 範圍的執行緒鎖定。</span><span class="sxs-lookup"><span data-stu-id="98773-152">If the caller requests a multithreaded factory, then, a factory-wide thread lock is acquired whenever a call is made into Direct2D.</span></span>

<span data-ttu-id="98773-153">此外，在 Direct2D 中鎖定執行緒的速度比 GDI 和 GDI + 更細微，因此執行緒數目的增加會對效能造成最大的影響。</span><span class="sxs-lookup"><span data-stu-id="98773-153">In addition, the locking of threads in Direct2D is more granular than in GDI and GDI+, so that the increase of the number of threads has minimal impact on the performance.</span></span>

## <a name="how-to-use-direct2d-for-server-side-rendering"></a><span data-ttu-id="98773-154">如何使用 Direct2D 進行 Server-Side 轉譯</span><span class="sxs-lookup"><span data-stu-id="98773-154">How to Use Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="98773-155">下列各節說明如何使用軟體轉譯、如何以最佳方式使用單一執行緒和多執行緒處理站，以及如何繪製複雜的繪圖並將其儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="98773-155">The following sections describe how to use software rendering, how to optimally use a single-threaded and a multithreaded factory, and how to draw and save a complex drawing to a file.</span></span>

### <a name="software-rendering"></a><span data-ttu-id="98773-156">軟體轉譯</span><span class="sxs-lookup"><span data-stu-id="98773-156">Software Rendering</span></span>

<span data-ttu-id="98773-157">伺服器端應用程式會藉由建立 [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) 轉譯目標來使用軟體轉譯，而轉譯目標型別會設定為 D2D1 轉譯 \_ \_ 目標 \_ 類型 \_ 軟體或 D2D1 轉譯 \_ \_ 目標 \_ 類型 \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="98773-157">Server-side applications use software rendering by creating [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target, with the render target type set to either D2D1\_RENDER\_TARGET\_TYPE\_SOFTWARE or D2D1\_RENDER\_TARGET\_TYPE\_DEFAULT.</span></span> <span data-ttu-id="98773-158">如需 [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) 轉譯目標的詳細資訊，請參閱 [**ID2D1Factory：： CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) 方法。如需呈現目標型別的詳細資訊，請參閱 [**D2D1 轉譯 \_ \_ 目標 \_ 類型**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)。</span><span class="sxs-lookup"><span data-stu-id="98773-158">For more information about [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render targets, see the [**ID2D1Factory::CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) method; for more information about the render target types, see [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span></span>

### <a name="multithreading"></a><span data-ttu-id="98773-159">多執行緒</span><span class="sxs-lookup"><span data-stu-id="98773-159">Multithreading</span></span>

<span data-ttu-id="98773-160">瞭解如何線上程之間建立和共用處理站和轉譯目標，可能會大幅影響應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="98773-160">Knowing how to create and share factories and render targets across threads can significantly impact the performance of an application.</span></span> <span data-ttu-id="98773-161">下列三個圖形顯示三種不同的方法。</span><span class="sxs-lookup"><span data-stu-id="98773-161">The following three figures show three varied approaches.</span></span> <span data-ttu-id="98773-162">[圖 3] 顯示最佳的方法。</span><span class="sxs-lookup"><span data-stu-id="98773-162">The optimal approach is shown in figure 3.</span></span>

![使用單一轉譯目標 direct2d 多執行緒圖表。](images/server-side-rendering-1.png)

<span data-ttu-id="98773-164">在 [圖 1] 中，不同的執行緒共用相同的 factory 和相同的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="98773-164">In figure 1, different threads share the same factory and the same render target.</span></span> <span data-ttu-id="98773-165">當多個執行緒同時變更共用轉譯目標的狀態（例如同時設定轉換矩陣）時，此方法可能會導致無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="98773-165">This approach can lead to unpredictable results in cases when multiple threads simultaneously change the state of the shared render target, such as simultaneously setting the transformation matrix.</span></span> <span data-ttu-id="98773-166">由於 Direct2D 中的內部鎖定並不會同步處理共用資源（例如轉譯目標），因此此方法可能會導致執行緒1中的 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 呼叫失敗，因為線上程2中， **BeginDraw** 呼叫已使用共用轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="98773-166">As the internal locking in Direct2D does not synchronize a shared resource such as render targets, this approach can cause the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) call to fail in thread 1, because in thread 2, the **BeginDraw** call is already using the shared render target.</span></span>

![具有多個呈現目標的 direct2d 多執行緒圖表。](images/server-side-rendering-2.png)

<span data-ttu-id="98773-168">為了避免在 [圖 1] 中發生無法預期的結果，[圖 2] 顯示每個執行緒都有自己呈現目標的多執行緒處理站。</span><span class="sxs-lookup"><span data-stu-id="98773-168">To avoid the unpredictable results encountered in figure 1, figure 2 shows a multithreaded factory with each thread having its own render target.</span></span> <span data-ttu-id="98773-169">這種方法可以運作，但它會有效地當作單一執行緒應用程式。</span><span class="sxs-lookup"><span data-stu-id="98773-169">This approach works but it effectively functions as a single-threaded application.</span></span> <span data-ttu-id="98773-170">原因是，factory 範圍鎖定只適用于繪圖作業層級，而相同處理站中的所有繪圖呼叫則會進行序列化。</span><span class="sxs-lookup"><span data-stu-id="98773-170">The reason is that the factory-wide lock applies only to the drawing-operation level and all the drawing calls in the same factory consequently are serialized.</span></span> <span data-ttu-id="98773-171">如此一來，當執行緒2在執行另一個繪製呼叫的過程中，執行緒1會遭到封鎖而無法進入繪圖呼叫。</span><span class="sxs-lookup"><span data-stu-id="98773-171">As a result, thread 1 becomes blocked when trying to enter a drawing call, while thread 2 is in the middle of executing another drawing call.</span></span>

![具有多個 factory 和多個呈現目標的 direct2d 多執行緒圖表。](images/server-side-rendering-3.png)

<span data-ttu-id="98773-173">[圖 3] 顯示最佳的方法，其中會使用單一執行緒的處理站和單一執行緒的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="98773-173">Figure 3 shows the optimal approach, where a single-threaded factory and a single-threaded render target are used.</span></span> <span data-ttu-id="98773-174">由於使用單一執行緒處理站時不會執行任何鎖定，因此每個執行緒中的繪圖作業可以同時執行，以達到最佳效能。</span><span class="sxs-lookup"><span data-stu-id="98773-174">Since no locking is performed when using a single-threaded factory, drawing operations in each thread can run concurrently to achieve optimal performance.</span></span>

### <a name="generating-a-bitmap-file"></a><span data-ttu-id="98773-175">產生點陣圖檔案</span><span class="sxs-lookup"><span data-stu-id="98773-175">Generating a Bitmap File</span></span>

<span data-ttu-id="98773-176">若要使用軟體呈現來產生點陣圖檔案，請使用 [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) 轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="98773-176">To generate a bitmap file using software rendering, use an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="98773-177">使用 [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) 將點陣圖寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="98773-177">Use an [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) to write the bitmap to a file.</span></span> <span data-ttu-id="98773-178">使用 [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) 將點陣圖編碼為指定的影像格式。</span><span class="sxs-lookup"><span data-stu-id="98773-178">Use [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap into a specified image format.</span></span> <span data-ttu-id="98773-179">下列程式碼範例示範如何繪製下列影像並將其儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="98773-179">The following code example shows how to draw and save the following image to a file.</span></span>

![範例輸出影像。](images/saveasimagefile-sample.png)

<span data-ttu-id="98773-181">這個程式碼範例會先建立 [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) 和 [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) 轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="98773-181">This code example first creates an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) and an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="98773-182">然後，它會呈現包含一些文字的繪圖、代表一個小時玻璃的路徑幾何，以及將小時的半透明轉譯成 WIC 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="98773-182">It then renders a drawing with some text, a path geometry representing an hour glass, and a transformed hour glass into a WIC bitmap.</span></span> <span data-ttu-id="98773-183">然後，它會使用 [IWICStream：： InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) 將點陣圖儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="98773-183">It then uses [IWICStream::InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) to save the bitmap to a file.</span></span> <span data-ttu-id="98773-184">如果您的應用程式需要將點陣圖儲存在記憶體中，請改用 [IWICStream：： InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) 。</span><span class="sxs-lookup"><span data-stu-id="98773-184">If your application needs to save the bitmap in memory, use [IWICStream::InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) instead.</span></span> <span data-ttu-id="98773-185">最後，它會使用 [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) 來編碼點陣圖。</span><span class="sxs-lookup"><span data-stu-id="98773-185">Finally, it uses [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap.</span></span>


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a><span data-ttu-id="98773-186">結論</span><span class="sxs-lookup"><span data-stu-id="98773-186">Conclusion</span></span>

<span data-ttu-id="98773-187">如上所示，使用 Direct2D 進行伺服器端轉譯相當簡單明瞭。</span><span class="sxs-lookup"><span data-stu-id="98773-187">As seen from the above, using Direct2D for server-side rendering is simple and straightforward.</span></span> <span data-ttu-id="98773-188">此外，它還提供高品質且高度可並行的轉譯，可在伺服器的低許可權環境中執行。</span><span class="sxs-lookup"><span data-stu-id="98773-188">In addition, it provides high quality and highly parallelizable rendering that can run in low-privilege environments of the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98773-189">相關主題</span><span class="sxs-lookup"><span data-stu-id="98773-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98773-190">Direct2D 參考</span><span class="sxs-lookup"><span data-stu-id="98773-190">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 