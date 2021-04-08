---
title: 多執行緒 Direct2D 應用程式
description: 描述建立多執行緒 Direct2D 應用程式的最佳做法。
ms.assetid: FDD770D4-817F-44D9-86C4-15DD04D214AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be979b867edd6d36583959c4a595dbd507ca94f
ms.sourcegitcommit: c3243ec4ada05b7faf9d563853cb667ecef825e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/03/2020
ms.locfileid: "103684230"
---
# <a name="multithreaded-direct2d-apps"></a><span data-ttu-id="56ffc-103">多執行緒 Direct2D 應用程式</span><span class="sxs-lookup"><span data-stu-id="56ffc-103">Multithreaded Direct2D Apps</span></span>

<span data-ttu-id="56ffc-104">如果您開發 [Direct2D](./direct2d-portal.md) 應用程式，您可能需要從一個以上的執行緒存取 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="56ffc-104">If you develop [Direct2D](./direct2d-portal.md) apps, you may need to access Direct2D resources from more than one thread.</span></span> <span data-ttu-id="56ffc-105">在其他情況下，您可能會想要使用多執行緒處理，以取得更佳的效能或更佳的回應性 (例如使用一個執行緒進行螢幕顯示，以及使用個別的執行緒來進行離線轉譯) 。</span><span class="sxs-lookup"><span data-stu-id="56ffc-105">In other cases, you may want to use multi-threading to get better performance or better responsiveness (like using one thread for screen display and a separate thread for offline rendering).</span></span>

<span data-ttu-id="56ffc-106">本主題說明在幾乎不需要[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)轉譯的情況下開發多執行緒[Direct2D](./direct2d-portal.md)應用程式的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="56ffc-106">This topic describes the best practices for developing multithreaded [Direct2D](./direct2d-portal.md) apps with little to no [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) rendering.</span></span> <span data-ttu-id="56ffc-107">並行問題所造成的軟體瑕疵可能很難追蹤，而且在規劃多執行緒原則和遵循此處所述的最佳作法方面很有説明。</span><span class="sxs-lookup"><span data-stu-id="56ffc-107">Software defects caused by concurrency issues can be difficult to track down, and it is helpful to plan your multithreading policy and to follow the best practices described here.</span></span>

> [!Note]  
> <span data-ttu-id="56ffc-108">如果您從兩個不同的單一執行緒 Direct2D factory 存取所建立的兩個 [Direct2D](./direct2d-portal.md) 資源，則只要基礎 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 裝置和裝置內容也不同，就不會造成存取衝突。</span><span class="sxs-lookup"><span data-stu-id="56ffc-108">If you access two [Direct2D](./direct2d-portal.md) resources created from two different single threaded Direct2D factories it doesn't cause access conflicts as long as the underlying [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) devices and device contexts are also distinct.</span></span> <span data-ttu-id="56ffc-109">談到本文中的「存取 Direct2D 資源」時，除非另有說明，否則它實際上是指「存取從相同 Direct2D 裝置建立的 Direct2D 資源」。</span><span class="sxs-lookup"><span data-stu-id="56ffc-109">When talking about "accessing Direct2D resources" in this article, it really means "accessing Direct2D resources created from the same Direct2D Device" unless stated otherwise.</span></span>

## <a name="developing-thread-safe-apps-that-call-only-direct2d-apis"></a><span data-ttu-id="56ffc-110">開發只呼叫 Direct2D Api 的 Thread-Safe 應用程式</span><span class="sxs-lookup"><span data-stu-id="56ffc-110">Developing Thread-Safe Apps that Call Only Direct2D APIs</span></span>

<span data-ttu-id="56ffc-111">您可以建立多執行緒 [Direct2D](./direct2d-portal.md) factory 實例。</span><span class="sxs-lookup"><span data-stu-id="56ffc-111">You can create a multithreaded [Direct2D](./direct2d-portal.md) factory instance.</span></span> <span data-ttu-id="56ffc-112">您可以從多個執行緒使用和共用多執行緒處理站和其所有資源，但 (透過 Direct2D 呼叫對這些資源的存取) 由 Direct2D 序列化，因此不會發生存取衝突。</span><span class="sxs-lookup"><span data-stu-id="56ffc-112">You can use and share a multithreaded factory and all its resources from more than one thread, but accesses to those resources (via Direct2D calls) are serialized by Direct2D, so no access conflicts occur.</span></span> <span data-ttu-id="56ffc-113">如果您的應用程式只呼叫 Direct2D Api，則 Direct2D 會自動以較小的額外負荷在細微層級中完成這類保護。</span><span class="sxs-lookup"><span data-stu-id="56ffc-113">If your app calls only Direct2D APIs, such protection is automatically done by Direct2D in a granular level with minimum overhead.</span></span> <span data-ttu-id="56ffc-114">在這裡建立多執行緒處理站的程式碼。</span><span class="sxs-lookup"><span data-stu-id="56ffc-114">The code to create a multithreaded factory here.</span></span>

```cpp
ID2D1Factory* m_D2DFactory;

// Create a Direct2D factory.
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_MULTI_THREADED,
    &m_D2DFactory
);
```

<span data-ttu-id="56ffc-115">此處的影像顯示 [Direct2D](./direct2d-portal.md) 如何序列化兩個使用 Direct2D API 進行呼叫的執行緒。</span><span class="sxs-lookup"><span data-stu-id="56ffc-115">The image here shows how [Direct2D](./direct2d-portal.md) serializes two threads that make calls using only the Direct2D API.</span></span>

![兩個序列化執行緒的圖表。](images/multi-thread.png)

## <a name="developing-thread-safe-direct2d-apps-with-minimal-direct3d-or-dxgi-calls"></a><span data-ttu-id="56ffc-117">使用極短的 Direct3D 或 DXGI 呼叫來開發 Thread-Safe Direct2D 應用程式</span><span class="sxs-lookup"><span data-stu-id="56ffc-117">Developing Thread-Safe Direct2D Apps with minimal Direct3D or DXGI Calls</span></span>

<span data-ttu-id="56ffc-118">[Direct2D](./direct2d-portal.md)應用程式通常也會進行某些[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)或 DXGI 呼叫。</span><span class="sxs-lookup"><span data-stu-id="56ffc-118">It is more than often that a [Direct2D](./direct2d-portal.md) app also makes some [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) or DXGI calls.</span></span> <span data-ttu-id="56ffc-119">例如，顯示執行緒會在 Direct2D 中繪製，然後使用 [**DXGI 交換鏈**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)呈現。</span><span class="sxs-lookup"><span data-stu-id="56ffc-119">For example, a display thread will draw in Direct2D then present using a [**DXGI swap chain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).</span></span>

<span data-ttu-id="56ffc-120">在此情況下，請確保執行緒安全性更複雜：某些 [Direct2D](./direct2d-portal.md) 呼叫會間接存取基礎 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 資源，而另一個呼叫 direct3d 或 DXGI 的執行緒可能會同時存取這些資源。</span><span class="sxs-lookup"><span data-stu-id="56ffc-120">In this case, assuring thread-safety is more complicated: some [Direct2D](./direct2d-portal.md) calls indirectly access the underlying [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) resources, which might be simultaneously accessed by another thread which calls Direct3D or DXGI.</span></span> <span data-ttu-id="56ffc-121">因為這些 Direct3D 或 DXGI 呼叫不 Direct2d 感知和控制，所以您需要建立多執行緒 Direct2D factory，但您必須執行 mor，以避免發生存取衝突。</span><span class="sxs-lookup"><span data-stu-id="56ffc-121">Since those Direct3D or DXGI calls are out of Direct2D’s awareness and control, you need to create a multithreaded Direct2D factory, but you must do mor to avoid access conflicts.</span></span>

<span data-ttu-id="56ffc-122">此圖表顯示 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 資源存取衝突，因為執行緒 T0 透過 [Direct2D](./direct2d-portal.md) 呼叫間接存取資源，而 T2 直接透過 Direct3D 或 DXGI 呼叫存取相同的資源。</span><span class="sxs-lookup"><span data-stu-id="56ffc-122">The diagram here shows a [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) resource access conflict due to thread T0 accessing a resource indirectly via a [Direct2D](./direct2d-portal.md) call and T2 accessing the same resource directly via a Direct3D or DXGI call.</span></span>

> [!Note]  
> <span data-ttu-id="56ffc-123">[Direct2D](./direct2d-portal.md)提供的執行緒保護 (此映射中的藍色鎖定) 在此案例中並沒有説明。</span><span class="sxs-lookup"><span data-stu-id="56ffc-123">The thread protection that [Direct2D](./direct2d-portal.md) provides (the blue lock in this image) doesn't help in this case.</span></span>

 

![執行緒保護圖表。](images/multi-thread2.png)

<span data-ttu-id="56ffc-125">為了避免此處的資源存取衝突，建議您明確取得 [Direct2D](./direct2d-portal.md) 用於內部存取同步處理的鎖定，並線上程需要進行可能會導致存取衝突的 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 或 DXGI 呼叫（如下所示）時套用該鎖定。</span><span class="sxs-lookup"><span data-stu-id="56ffc-125">To avoid resource access conflict here, we recommend you explicitly acquire the lock that [Direct2D](./direct2d-portal.md) uses for internal access synchronization, and apply that lock when a thread needs to make [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) or DXGI calls that might cause access conflict as shown here.</span></span> <span data-ttu-id="56ffc-126">尤其是，您應該特別注意使用例外狀況的程式碼或以 HRESULT 傳回碼為基礎的早期系統。</span><span class="sxs-lookup"><span data-stu-id="56ffc-126">In particular, you should take special care with code that uses exceptions or an early out system based on HRESULT return codes.</span></span> <span data-ttu-id="56ffc-127">基於這個理由，建議您使用 RAII (資源取得是初始化) 模式，以呼叫 [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) 和 [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) 方法。</span><span class="sxs-lookup"><span data-stu-id="56ffc-127">For this reason, we recommend you use an RAII (Resource Acquisition Is Initialization) pattern to call the [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) and [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) methods.</span></span>

> [!Note]  
> <span data-ttu-id="56ffc-128">請務必將呼叫與 [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) 和 [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) 方法配對，否則您的應用程式可能會鎖死。</span><span class="sxs-lookup"><span data-stu-id="56ffc-128">It is important that you pair up calls to the [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) and [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) methods, otherwise your app can deadlock.</span></span>

 

<span data-ttu-id="56ffc-129">此處的程式碼顯示如何鎖定和解除鎖定 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 或 DXGI 呼叫的時機。</span><span class="sxs-lookup"><span data-stu-id="56ffc-129">The code here shows an example of when to lock and then and unlock around [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) or DXGI calls.</span></span>


```C++
void MyApp::DrawFromThread2()
{
    // We are accessing Direct3D resources directly without Direct2D's knowledge, so we
    // must manually acquire and apply the Direct2D factory lock.
    ID2D1Multithread* m_D2DMultithread;
    m_D2DFactory->QueryInterface(IID_PPV_ARGS(&m_D2DMultithread));
    m_D2DMultithread->Enter();
    
    // Now it is safe to make Direct3D/DXGI calls, such as IDXGISwapChain::Present
    MakeDirect3DCalls();

    // It is absolutely critical that the factory lock be released upon
    // exiting this function, or else any consequent Direct2D calls will be blocked.
    m_D2DMultithread->Leave();
}
```



> [!Note]  
> <span data-ttu-id="56ffc-130">某些 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 或 DXGI 呼叫 (特別 [**IDXGISwapChain：:P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) 重新傳送) 可能會在呼叫函式或方法的程式碼中取得鎖定及/或觸發回呼。</span><span class="sxs-lookup"><span data-stu-id="56ffc-130">Some [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) or DXGI calls (notably [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)) may acquire locks and/or trigger callbacks into the code of the calling function or method.</span></span> <span data-ttu-id="56ffc-131">您應該注意這一點，並確保這類行為不會造成鎖死。</span><span class="sxs-lookup"><span data-stu-id="56ffc-131">You should be aware of this and make sure that such behavior doesn't cause deadlocks.</span></span> <span data-ttu-id="56ffc-132">如需詳細資訊，請參閱 [ [DXGI 總覽](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) ] 主題。</span><span class="sxs-lookup"><span data-stu-id="56ffc-132">For more info, see the [DXGI Overview](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) topic.</span></span>

 

![direct2d 和 direct3d 執行緒鎖定圖表。](images/multi-thread3.png)

<span data-ttu-id="56ffc-134">當您使用 [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) 和 [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) 方法時，呼叫會受到自動 [Direct2D](./direct2d-portal.md) 和明確鎖定的保護，因此應用程式不會碰到存取衝突。</span><span class="sxs-lookup"><span data-stu-id="56ffc-134">When you use the [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) and [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) methods, the calls are protected by the automatic [Direct2D](./direct2d-portal.md) and the explicit lock, so the app doesn't hit access conflict.</span></span>

<span data-ttu-id="56ffc-135">有其他方法可以解決此問題。</span><span class="sxs-lookup"><span data-stu-id="56ffc-135">There are other approaches to work around this issue.</span></span> <span data-ttu-id="56ffc-136">不過，我們建議您明確地使用[Direct2D](./direct2d-portal.md)鎖定來保護[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)或 DXGI 呼叫，因為它通常會提供較佳的效能，因為它會以更細微的層級來保護平行存取，而且在 direct2d 涵蓋下的額外負荷較低。</span><span class="sxs-lookup"><span data-stu-id="56ffc-136">However, we recommend you explicitly guard [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) or DXGI calls with the [Direct2D](./direct2d-portal.md) lock because it usually provides better performance as it protects concurrency at a much finer level and with lower overhead under Direct2D’s cover.</span></span>

## <a name="ensuring-atomicity-of-stateful-operations"></a><span data-ttu-id="56ffc-137">確保具狀態作業的不可部分完成性</span><span class="sxs-lookup"><span data-stu-id="56ffc-137">Ensuring Atomicity of Stateful Operations</span></span>

<span data-ttu-id="56ffc-138">雖然 [DirectX](/previous-versions//ee663301(v=vs.85)) 的安全線程功能可協助確保不會同時進行兩個個別的 api 呼叫，您也必須確定讓具狀態 API 呼叫的執行緒不會互相干擾。</span><span class="sxs-lookup"><span data-stu-id="56ffc-138">While thread-safety features of [DirectX](/previous-versions//ee663301(v=vs.85)) can help ensure that no two individual API calls are made concurrently, you must also ensure that threads that make stateful API calls don't interfere with each other.</span></span> <span data-ttu-id="56ffc-139">範例如下。</span><span class="sxs-lookup"><span data-stu-id="56ffc-139">Here is an example.</span></span>

1.  <span data-ttu-id="56ffc-140">有兩行文字是您想要以執行緒0呈現的螢幕 () ，以及執行緒 1) 的非畫面 (：行 \# 1 是 "A"，而第 \# 2 行是 "B"，這兩個都是以實心黑色筆刷繪製。</span><span class="sxs-lookup"><span data-stu-id="56ffc-140">There are two lines of text that you want to render to both on-screen (by Thread 0) and off-screen (by Thread 1): Line \#1 is "A is greater" and Line \#2 is "than B", both of which will be drawn using a solid black brush.</span></span>
2.  <span data-ttu-id="56ffc-141">執行緒1會繪製第一行文字。</span><span class="sxs-lookup"><span data-stu-id="56ffc-141">Thread 1 draws the first line of text.</span></span>
3.  <span data-ttu-id="56ffc-142">執行緒0會對使用者輸入做出反應，並將兩個文字行分別更新為 "B" 和 "，以及將筆刷色彩變更為純紅色，以供自己的繪圖使用;</span><span class="sxs-lookup"><span data-stu-id="56ffc-142">Thread 0 reacts to a user input, updates both text lines to "B is smaller" and "than A" respectively, and changed the brush color to solid red for its own drawing;</span></span>
4.  <span data-ttu-id="56ffc-143">執行緒1會繼續以紅色色彩筆刷繪製第二行文字（現在是 "of"）。</span><span class="sxs-lookup"><span data-stu-id="56ffc-143">Thread 1 continues drawing the second line of text, which is now "than A", with the red color brush;</span></span>
5.  <span data-ttu-id="56ffc-144">最後，我們會在非畫面繪圖目標上取得兩行文字：以黑色顯示「A」，並以紅色顯示「大於」。</span><span class="sxs-lookup"><span data-stu-id="56ffc-144">Finally, we get two lines of text on the off-screen drawing target: "A is greater" in black and "than A" in red.</span></span>

![開啟和關閉畫面執行緒的圖表。](images/multi-thread4.png)

<span data-ttu-id="56ffc-146">在頂端的資料列中，執行緒0會使用目前的文字字串和目前的黑色筆刷來繪製。</span><span class="sxs-lookup"><span data-stu-id="56ffc-146">In the top row, Thread 0 draws with current text strings and the current black brush.</span></span> <span data-ttu-id="56ffc-147">執行緒1只會在上半部完成全螢幕繪製。</span><span class="sxs-lookup"><span data-stu-id="56ffc-147">Thread 1 only finishes off-screen drawing on the top half.</span></span>

<span data-ttu-id="56ffc-148">在中間的資料列中，執行緒0會回應使用者互動、更新文字字串和筆刷，然後重新整理畫面。</span><span class="sxs-lookup"><span data-stu-id="56ffc-148">In the middle row, Thread 0 responds to user interaction, updates the text strings and the brush, then refreshes the screen.</span></span> <span data-ttu-id="56ffc-149">此時，執行緒1會遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="56ffc-149">At this point, Thread 1 is blocked.</span></span> <span data-ttu-id="56ffc-150">在底部的資料列中，執行緒1之後的最後一個離螢幕轉譯會繼續使用改變的筆刷和改變的文字字串來繪製下半部。</span><span class="sxs-lookup"><span data-stu-id="56ffc-150">In the bottom row, the final off-screen rendering after Thread 1 resumes drawing the bottom half with an altered brush and an altered text string.</span></span>

<span data-ttu-id="56ffc-151">若要解決此問題，建議您針對每個執行緒都有個別的內容，以便：</span><span class="sxs-lookup"><span data-stu-id="56ffc-151">To address this issue, we recommend you have a separate context for each thread, so that:</span></span>

-   <span data-ttu-id="56ffc-152">您應建立裝置內容的複本，讓可變動的資源 (也就是在顯示或列印期間可能會有所不同的資源，例如文字內容或範例中的純色筆刷，在轉譯時不會變更) 不會變更。</span><span class="sxs-lookup"><span data-stu-id="56ffc-152">You should create a copy of the device context so that mutable resources (i.e. resources that may vary during display or printing, such as text contents or the solid color brush in the example) don't change when you render.</span></span> <span data-ttu-id="56ffc-153">在此範例中，您應該在繪製前維護這兩行文字和色彩筆刷的複本。</span><span class="sxs-lookup"><span data-stu-id="56ffc-153">In this sample, you should maintain a copy of those two lines of texts and the color brush before you draw.</span></span> <span data-ttu-id="56ffc-154">如此一來，您就能確保每個執行緒都有完整且一致的內容可供繪製和呈現。</span><span class="sxs-lookup"><span data-stu-id="56ffc-154">By doing so, you guarantee each thread has complete and consistent content to draw and present.</span></span>
-   <span data-ttu-id="56ffc-155">您應該共用大量資源 (例如點陣圖和複雜效果圖形) ，這些會初始化一次，然後不會線上程之間修改來提高效能。</span><span class="sxs-lookup"><span data-stu-id="56ffc-155">You should share heavy-weight resources (like bitmaps and complex effect graphs) that are initialized once and then never modified across threads to increase performance.</span></span>
-   <span data-ttu-id="56ffc-156">您可以共用輕量資源 (例如純色筆刷和文字格式) 這些會初始化一次，然後不會線上程之間修改</span><span class="sxs-lookup"><span data-stu-id="56ffc-156">You can either share light-weight resources (like solid color brushes and text formats) that are initialized once and then never modified across threads or not</span></span>

## <a name="summary"></a><span data-ttu-id="56ffc-157">總結</span><span class="sxs-lookup"><span data-stu-id="56ffc-157">Summary</span></span>

<span data-ttu-id="56ffc-158">當您開發多執行緒 [Direct2D](./direct2d-portal.md) 應用程式時，您必須建立多執行緒 Direct2D factory，然後從該 factory 衍生所有 Direct2D 資源。</span><span class="sxs-lookup"><span data-stu-id="56ffc-158">When you develop multithreaded [Direct2D](./direct2d-portal.md) apps, you must create a multithreaded Direct2D factory then derive all Direct2D resources from that factory.</span></span> <span data-ttu-id="56ffc-159">如果執行緒會進行 [direct3d](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 或 dxgi 呼叫，您也必須明確取得，然後套用 Direct2D 鎖定來保護這些 DIRECT3D 或 dxgi 呼叫。</span><span class="sxs-lookup"><span data-stu-id="56ffc-159">If a thread will make [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) or DXGI calls, you also must explicitly acquire then apply the Direct2D lock to guard those Direct3D or DXGI calls.</span></span> <span data-ttu-id="56ffc-160">此外，您必須針對每個執行緒擁有可變動資源的複本，以確保內容完整性。</span><span class="sxs-lookup"><span data-stu-id="56ffc-160">Moreover, you must ensure context integrity by having a copy of mutable resources for each thread.</span></span>
