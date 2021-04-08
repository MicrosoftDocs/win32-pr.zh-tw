---
title: 關於 Direct2D
description: 介紹 Direct2D，這是一個 API，可讓 Win32 開發人員能夠執行具有優異效能和視覺品質的2D 圖形轉譯工作。
ms.assetid: 05cc230e-6fec-4a15-8e28-c68397392fc5
keywords:
- Direct2D，關於
- Direct2D，互通性
- Direct2D，效能
- Direct2D，可用性
- Direct2D，應用程式
- 互通性，Direct2D
- Direct2D 的效能
- Direct2D 的可用性
- 適用于 Direct2D 的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486c83b7a83ef82983e189977f9f99254b0a1977
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933442"
---
# <a name="about-direct2d"></a><span data-ttu-id="b8c50-112">關於 Direct2D</span><span class="sxs-lookup"><span data-stu-id="b8c50-112">About Direct2D</span></span>

<span data-ttu-id="b8c50-113">本主題將介紹 Direct2D，這是一個 API，可讓 Win32 開發人員能夠執行具有優異效能和視覺品質的2D 圖形轉譯工作。</span><span class="sxs-lookup"><span data-stu-id="b8c50-113">This topic introduces Direct2D, an API that provides Win32 developers with the ability to perform 2-D graphics rendering tasks with superior performance and visual quality.</span></span>

## <a name="what-is-direct2d"></a><span data-ttu-id="b8c50-114">什麼是 Direct2D？</span><span class="sxs-lookup"><span data-stu-id="b8c50-114">What is Direct2D?</span></span>

<span data-ttu-id="b8c50-115">Direct2D 是一種硬體加速的即時模式2d 圖形 API，可為2D 幾何、點陣圖和文字提供高效能和高品質的呈現。</span><span class="sxs-lookup"><span data-stu-id="b8c50-115">Direct2D is a hardware-accelerated, immediate-mode 2-D graphics API that provides high performance and high-quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="b8c50-116">Direct2D API 的設計目的是要與使用 GDI、GDI + 或 Direct3D 的現有程式碼交互操作。</span><span class="sxs-lookup"><span data-stu-id="b8c50-116">The Direct2D API is designed to interoperate with existing code that uses GDI, GDI+, or Direct3D.</span></span>

<span data-ttu-id="b8c50-117">Direct2D 主要是設計來供下列開發人員類別使用：</span><span class="sxs-lookup"><span data-stu-id="b8c50-117">Direct2D is designed primarily for use by the following classes of developers:</span></span>

-   <span data-ttu-id="b8c50-118">大型企業規模原生應用程式的開發人員。</span><span class="sxs-lookup"><span data-stu-id="b8c50-118">Developers of large, enterprise-scale, native applications.</span></span>
-   <span data-ttu-id="b8c50-119">建立可供下游開發人員取用的控制項工具組和程式庫的開發人員。</span><span class="sxs-lookup"><span data-stu-id="b8c50-119">Developers who create control toolkits and libraries for consumption by downstream developers.</span></span>
-   <span data-ttu-id="b8c50-120">需要伺服器端呈現2D 圖形的開發人員。</span><span class="sxs-lookup"><span data-stu-id="b8c50-120">Developers who require server-side rendering of 2-D graphics.</span></span>
-   <span data-ttu-id="b8c50-121">使用 Direct3D 圖形並需要簡單、高效能的2D 和文字轉譯（用於功能表、使用者介面 (UI) 元素，以及 (HUDs) ）的開發人員。</span><span class="sxs-lookup"><span data-stu-id="b8c50-121">Developers who use Direct3D graphics and need simple, high-performance 2-D and text rendering for menus, user interface (UI) elements, and Heads-up Displays (HUDs).</span></span>

## <a name="why-direct2d"></a><span data-ttu-id="b8c50-122">為什麼要 Direct2D？</span><span class="sxs-lookup"><span data-stu-id="b8c50-122">Why Direct2D?</span></span>

<span data-ttu-id="b8c50-123">在 Microsoft Windows 中建立新的2D 圖形 API 的主要動機包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="b8c50-123">The primary motivations for creating a new 2-D graphics API in Microsoft Windows include the following:</span></span>

-   <span data-ttu-id="b8c50-124">讓 Windows 使用者習慣採用更高程度的視覺豐富視覺效果。</span><span class="sxs-lookup"><span data-stu-id="b8c50-124">To keep pace with the increasing level of visual richness that Windows users are accustomed to.</span></span>
-   <span data-ttu-id="b8c50-125">讓開發人員撰寫2D 轉譯程式碼，以直接調整其執行所在之電腦的圖形處理硬體。</span><span class="sxs-lookup"><span data-stu-id="b8c50-125">To enable developers to write 2-D rendering code that scales directly with the graphics processing hardware of the PC it is running on.</span></span>
-   <span data-ttu-id="b8c50-126">讓開發人員撰寫程式碼，以轉譯可在服務內容中執行的2D 圖形。</span><span class="sxs-lookup"><span data-stu-id="b8c50-126">To enable developers to write code for rendering 2-D graphics that can run in the context of a service.</span></span>

<span data-ttu-id="b8c50-127">在最近幾年，終端使用者開始預期數位體驗的視覺精確度更高。</span><span class="sxs-lookup"><span data-stu-id="b8c50-127">In recent years, end users have begun to expect greater visual fidelity in digital experiences.</span></span> <span data-ttu-id="b8c50-128">此趨勢會反映在消費性電子產品中。</span><span class="sxs-lookup"><span data-stu-id="b8c50-128">This trend is reflected in consumer electronics.</span></span> <span data-ttu-id="b8c50-129">GPS 裝置、媒體播放裝置、行動電話和數位攝影機在一年後提供一致的體驗。</span><span class="sxs-lookup"><span data-stu-id="b8c50-129">GPS devices, media playback devices, mobile phones, and digital cameras deliver consistently richer experiences year after year.</span></span> <span data-ttu-id="b8c50-130">這種趨勢也可以在電影、電視、影片遊戲和網路上的圖形內容多樣性中看到。</span><span class="sxs-lookup"><span data-stu-id="b8c50-130">This trend can also be seen in the diversity of graphical content in film, television, video games, and on the Web.</span></span> <span data-ttu-id="b8c50-131">為了與這些變更保持一致，開發人員會一直要求將現有的 Windows 應用程式帶到下一層的視覺效果豐富。</span><span class="sxs-lookup"><span data-stu-id="b8c50-131">To keep pace with these changes, developers are consistently asked to take their existing Windows applications to the next level of visual richness.</span></span>

<span data-ttu-id="b8c50-132">新式 Windows 電腦上的圖形處理器也不斷演變，並由影片遊戲圖形中的進展以及 windows Media Center 和 Aero 等 Windows 體驗的部分所驅動。</span><span class="sxs-lookup"><span data-stu-id="b8c50-132">Graphics processors in modern Windows PCs have also been evolving steadily, driven by advances in video game graphics and parts of the Windows experience like Windows Media Center and Aero.</span></span> <span data-ttu-id="b8c50-133">某些 Windows 應用程式可以使用 Microsoft Direct3D 和 Windows Presentation Foundation (WPF) 來利用新式 Gpu。</span><span class="sxs-lookup"><span data-stu-id="b8c50-133">Some Windows applications can take advantage of modern GPUs by using Microsoft Direct3D and Windows Presentation Foundation (WPF).</span></span> <span data-ttu-id="b8c50-134">雖然 Direct3D 提供高階的3-d 圖形應用程式，而 WPF 可滿足 .NET 開發人員的需求，但開發人員還是有一些與以 GDI 和 GDI + 為基礎的大型現有程式碼基底，或是想要在 Direct3D 應用程式中納入高品質2D 圖形的程式開發人員的差距。</span><span class="sxs-lookup"><span data-stu-id="b8c50-134">While Direct3D serves high-end 3-D graphics applications and WPF addresses the needs of .NET developers, there are gaps for developers who have large existing codebases of rendering code based on GDI and GDI+ or who want to incorporate high-quality 2-D graphics in their Direct3D-based applications.</span></span>

<span data-ttu-id="b8c50-135">最後，可以在服務中使用的圖形 API 需求，已成為在企業和 Web 開發案例中工作之開發人員的新興需求。</span><span class="sxs-lookup"><span data-stu-id="b8c50-135">Finally, the need for a graphics API that can be used in a service has become an emerging requirement for developers working in enterprise and Web-development scenarios.</span></span> <span data-ttu-id="b8c50-136">現有的轉譯 Api 著重在單一使用者會話中的用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="b8c50-136">Existing rendering APIs focus on client-side rendering in a single user session.</span></span> <span data-ttu-id="b8c50-137">因此，在服務內容中使用時，它們可能會在穩定和可調整性區域中縮短。</span><span class="sxs-lookup"><span data-stu-id="b8c50-137">As such, they can fall short in areas of robustness and scalability when used in a service context.</span></span> <span data-ttu-id="b8c50-138">需要新的 API 才能解決此情況。</span><span class="sxs-lookup"><span data-stu-id="b8c50-138">A new API is required to address this.</span></span>

## <a name="high-performance-with-maximum-availability"></a><span data-ttu-id="b8c50-139">具有最高可用性的高效能</span><span class="sxs-lookup"><span data-stu-id="b8c50-139">High Performance with Maximum Availability</span></span>

<span data-ttu-id="b8c50-140">Direct2D 是使用 Direct3D 10.1 API 建立的使用者模式程式庫。</span><span class="sxs-lookup"><span data-stu-id="b8c50-140">Direct2D is a user-mode library that is built using the Direct3D 10.1 API.</span></span> <span data-ttu-id="b8c50-141">這表示 Direct2D 應用程式受益于新式主流 Gpu 上的硬體加速轉譯。</span><span class="sxs-lookup"><span data-stu-id="b8c50-141">This means that Direct2D applications benefit from hardware-accelerated rendering on modern mainstream GPUs.</span></span> <span data-ttu-id="b8c50-142">使用 Direct3D 10 層級9轉譯，也可以在舊版 Direct3D 9 硬體上達成硬體加速。</span><span class="sxs-lookup"><span data-stu-id="b8c50-142">Hardware acceleration is also achieved on earlier Direct3D 9 hardware by using Direct3D 10-level-9 rendering.</span></span> <span data-ttu-id="b8c50-143">這種組合可為現有 Windows 電腦上的圖形硬體提供絕佳的效能。</span><span class="sxs-lookup"><span data-stu-id="b8c50-143">This combination provides excellent performance on graphics hardware on existing Windows PCs.</span></span>

> [!Note]  
> <span data-ttu-id="b8c50-144">從 Windows 8 開始，Direct2D 是使用 Direct3D 11.1 API 所建立。</span><span class="sxs-lookup"><span data-stu-id="b8c50-144">Starting with Windows 8, Direct2D is built using the Direct3D 11.1 API.</span></span>

 

<span data-ttu-id="b8c50-145">下圖顯示 Direct2D 的分層架構。</span><span class="sxs-lookup"><span data-stu-id="b8c50-145">The following diagram shows the layered architecture of Direct2D.</span></span>

![direct2d 分層架構的圖表](images/direct2d-architectual-layering.png)

<span data-ttu-id="b8c50-147">在使用硬體加速的情況下，Direct2D 包含高效能的軟體轉譯器。</span><span class="sxs-lookup"><span data-stu-id="b8c50-147">For scenarios where the use of hardware acceleration is not feasible, Direct2D includes a high-performance software rasterizer.</span></span> <span data-ttu-id="b8c50-148">在軟體中轉譯時，使用 Direct2D 體驗的應用程式明顯比使用 GDI + 更好的轉譯效能，並且具有類似的視覺品質。</span><span class="sxs-lookup"><span data-stu-id="b8c50-148">When rendering in software, applications that use Direct2D experience substantially better rendering performance than with GDI+ and with similar visual quality.</span></span> <span data-ttu-id="b8c50-149">軟體轉譯器也是設計來在服務內容中使用。</span><span class="sxs-lookup"><span data-stu-id="b8c50-149">The software rasterizer is also designed for use in a service context.</span></span>

<span data-ttu-id="b8c50-150">使用 Direct2D 轉譯的內容也可以使用 Windows 7 作業系統中的遠端桌面通訊協定 (RDP) 基礎結構，在遠端顯示。</span><span class="sxs-lookup"><span data-stu-id="b8c50-150">Content that is rendered by using Direct2D can also be displayed remotely by using the Remote Desktop Protocol (RDP) infrastructure in the Windows 7 operating system.</span></span> <span data-ttu-id="b8c50-151">開發人員可以選取顯示電腦上的 GPU 處理轉譯，還是在本機轉譯並以點陣圖形式傳送。</span><span class="sxs-lookup"><span data-stu-id="b8c50-151">Developers can select whether rendering is handled by the GPU on the display computer or rendered locally and transmitted as bitmaps.</span></span> <span data-ttu-id="b8c50-152">您可以根據所需的填滿率和轉譯的圖形基本數量來建立此選擇。</span><span class="sxs-lookup"><span data-stu-id="b8c50-152">This choice can be made based on the required fill-rate and the quantity of graphics primitives that are rendered.</span></span> <span data-ttu-id="b8c50-153">當顯示電腦執行的是 Windows 7 之前的作業系統時，會透過網路傳輸點陣圖來執行遠端顯示器轉譯。</span><span class="sxs-lookup"><span data-stu-id="b8c50-153">When the display computer is running an operating system earlier than Windows 7, remote display rendering is performed by transmitting bitmaps over the network.</span></span>

<span data-ttu-id="b8c50-154">藉由提供軟體回復、遠端桌面和服務轉譯，提供單一 API 來結合 Direct3D 與高可用性的效能，Direct2D 可讓開發人員在許多不同的案例中，有單一的高效能轉譯效能。</span><span class="sxs-lookup"><span data-stu-id="b8c50-154">By providing a single API that combines the performance of Direct3D and high availability by providing software fallback, remote desktop, and service rendering, Direct2D enables developers to have a single implementation for high-performance rendering in many different scenarios.</span></span>

## <a name="visual-quality"></a><span data-ttu-id="b8c50-155">視覺品質</span><span class="sxs-lookup"><span data-stu-id="b8c50-155">Visual Quality</span></span>

<span data-ttu-id="b8c50-156">使用 Direct2D for graphics 的應用程式可提供比使用 GDI 來達成更高的視覺品質。</span><span class="sxs-lookup"><span data-stu-id="b8c50-156">Applications that use Direct2D for graphics can deliver higher visual quality than what can be achieved using GDI.</span></span> <span data-ttu-id="b8c50-157">Direct2D 會使用每個基本的消除鋸齒，在呈現的內容中提供更平滑的曲線和線條。</span><span class="sxs-lookup"><span data-stu-id="b8c50-157">Direct2D uses per-primitive antialiasing to deliver smoother looking curves and lines in rendered content.</span></span> <span data-ttu-id="b8c50-158">當轉譯2D 基本專案時，也有完整的透明度和 Alpha 混合支援。</span><span class="sxs-lookup"><span data-stu-id="b8c50-158">There is also full support for transparency and alpha blending when rendering 2-D primitives.</span></span> <span data-ttu-id="b8c50-159">下圖會比較在左側) 上使用 GDI (轉譯的別名內容，以及右邊) 上 Direct2D (轉譯的反鋸齒內容。</span><span class="sxs-lookup"><span data-stu-id="b8c50-159">The following images compare aliased content rendered by using GDI (on the left) with antialiased content rendered by Direct2D (on the right).</span></span>

![以 gdi 和 direct2d 呈現的曲線和線條圖例](images/rendering-curves-and-lines.png)

<span data-ttu-id="b8c50-161">開發人員可以指定以別名呈現的向量圖形。</span><span class="sxs-lookup"><span data-stu-id="b8c50-161">Developers can specify aliased rendering of vector graphics.</span></span> <span data-ttu-id="b8c50-162">這適用于需要貼齊至固定圖元界限的案例中，例如指標或尺規等 UI 元素。如果輸出的 GDI 樣式必須相符，或在轉譯程式中透過多重取樣消除鋸齒或其他其他機制來執行消除鋸齒，則會使用此專案。</span><span class="sxs-lookup"><span data-stu-id="b8c50-162">This is used in scenarios where snapping to hard pixel boundaries is required, such as UI elements like pointers or rulers, if the GDI style of output must be matched, or if antialiasing will be performed downstream in the rendering process via Multisample Antialiasing or some other mechanism.</span></span>

## <a name="interoperability"></a><span data-ttu-id="b8c50-163">互通性</span><span class="sxs-lookup"><span data-stu-id="b8c50-163">Interoperability</span></span>

<span data-ttu-id="b8c50-164">使用 GDI 和 Direct3D 的介面層級互通性，讓開發人員能夠更輕鬆地整合以 Direct2D 為基礎的呈現。</span><span class="sxs-lookup"><span data-stu-id="b8c50-164">Integrating Direct2D-based rendering is made easier for developers through surface-level interoperability with GDI and Direct3D.</span></span> <span data-ttu-id="b8c50-165">使用 GDI、GDI + 或 Direct3D 來轉譯內容的應用程式，可以從使用 Direct2D 來呈現其應用程式的特定區域開始，然後隨著時間移至透過 Direct2D 執行轉譯的模型，主要是針對外掛程式或舊版擴充性使用 GDI。</span><span class="sxs-lookup"><span data-stu-id="b8c50-165">Applications that render content primarily with GDI, GDI+, or Direct3D, can begin by using Direct2D to render specific areas of their application, and over time move to a model where rendering is performed primarily via Direct2D, using GDI primarily for plug-ins or legacy extensibility.</span></span>

<span data-ttu-id="b8c50-166">Direct2D 也可讓您輕鬆地使用 [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) 來處理高品質的文字，以及 [MICROSOFT Windows 影像處理元件 (WIC) ](https://msdn.microsoft.com/library/ms737408.aspx)的先進映射功能。</span><span class="sxs-lookup"><span data-stu-id="b8c50-166">Direct2D also makes it easy to use [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) for high quality text and the advanced imaging features of the [Microsoft Windows Imaging Component (WIC)](https://msdn.microsoft.com/library/ms737408.aspx).</span></span>

<span data-ttu-id="b8c50-167">如需有關 Direct2D 互通性的詳細資訊，請參閱 [DIRECT2D SDK 的互通性一節。](interoperability.md)</span><span class="sxs-lookup"><span data-stu-id="b8c50-167">For more information about Direct2D interoperability, see the [Interoperability section of the Direct2D SDK.](interoperability.md)</span></span>

## <a name="summary"></a><span data-ttu-id="b8c50-168">總結</span><span class="sxs-lookup"><span data-stu-id="b8c50-168">Summary</span></span>

<span data-ttu-id="b8c50-169">Microsoft Direct2D 可讓開發人員在其應用程式中建立2D 圖形功能，以提供透過 GDI 改善的視覺品質，以及利用新式 Gpu 進行調整的效能特性。</span><span class="sxs-lookup"><span data-stu-id="b8c50-169">Microsoft Direct2D enables developers to build 2-D graphics features in their applications that deliver improved visual quality over GDI, and performance characteristics that scale with modern GPUs.</span></span> <span data-ttu-id="b8c50-170">Direct2D 互通性模型可讓開發人員一次選擇性地將其應用程式的部分和 GDI、GDI + 或 Direct3D 轉譯一起遷移。</span><span class="sxs-lookup"><span data-stu-id="b8c50-170">The Direct2D interoperability model enables developers to selectively migrate portions of their application at a time alongside GDI, GDI+, or Direct3D-based rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8c50-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8c50-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8c50-172">Windows 8 的 Direct2D 快速入門</span><span class="sxs-lookup"><span data-stu-id="b8c50-172">Direct2D Quickstart for Windows 8</span></span>](direct2d-quickstart-with-device-context.md)
</dt> <dt>

[<span data-ttu-id="b8c50-173">Direct2D API 概觀</span><span class="sxs-lookup"><span data-stu-id="b8c50-173">Direct2D API Overview</span></span>](the-direct2d-api.md)
</dt> </dl>

 

 