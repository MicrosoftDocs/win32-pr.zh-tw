---
title: Windows 圖形架構總覽
description: 描述 Windows 中的 c + +/COM 圖形 Api。
ms.assetid: 9654b18b-d615-455d-a92a-6fc2ccda469e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45ba44f54b947d923b888d51080ff0335119a1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "104116013"
---
# <a name="overview-of-the-windows-graphics-architecture"></a><span data-ttu-id="46189-103">Windows 圖形架構總覽</span><span class="sxs-lookup"><span data-stu-id="46189-103">Overview of the Windows Graphics Architecture</span></span>

<span data-ttu-id="46189-104">Windows 為圖形提供數個 c + +/COM Api。</span><span class="sxs-lookup"><span data-stu-id="46189-104">Windows provides several C++/COM APIs for graphics.</span></span> <span data-ttu-id="46189-105">這些 Api 如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="46189-105">These APIs are shown in the following diagram.</span></span>

![顯示 windows 圖形 api 的圖表。](images/graphics01.png)

-   <span data-ttu-id="46189-107">圖形裝置介面 (GDI) 是適用于 Windows 的原始圖形介面。</span><span class="sxs-lookup"><span data-stu-id="46189-107">Graphics Device Interface (GDI) is the original graphics interface for Windows.</span></span> <span data-ttu-id="46189-108">GDI 是先針對16位 Windows 撰寫，然後針對32位和64位 Windows 進行更新。</span><span class="sxs-lookup"><span data-stu-id="46189-108">GDI was first written for 16-bit Windows and then updated for 32-bit and 64-bit Windows.</span></span>
-   <span data-ttu-id="46189-109">GDI + 是在 Windows XP 中引進，做為 GDI 的後繼。</span><span class="sxs-lookup"><span data-stu-id="46189-109">GDI+ was introduced in Windows XP as a successor to GDI.</span></span> <span data-ttu-id="46189-110">您可以透過一組包裝一般 C 函式的 c + + 類別來存取 GDI + 程式庫。</span><span class="sxs-lookup"><span data-stu-id="46189-110">The GDI+ library is accessed through a set of C++ classes that wrap flat C functions.</span></span> <span data-ttu-id="46189-111">.NET Framework 也會在 **System. 繪圖** 命名空間中提供 managed 版本的 gdi +。</span><span class="sxs-lookup"><span data-stu-id="46189-111">The .NET Framework also provides a managed version of GDI+ in the **System.Drawing** namespace.</span></span>
-   <span data-ttu-id="46189-112">Direct3D 支援立體圖形。</span><span class="sxs-lookup"><span data-stu-id="46189-112">Direct3D supports 3-D graphics.</span></span>
-   <span data-ttu-id="46189-113">Direct2D 是適用于2D 圖形的新式 API，這是 GDI 和 GDI + 的後繼。</span><span class="sxs-lookup"><span data-stu-id="46189-113">Direct2D is a modern API for 2-D graphics, the successor to both GDI and GDI+.</span></span>
-   <span data-ttu-id="46189-114">DirectWrite 是文字版面配置和點陣化引擎。</span><span class="sxs-lookup"><span data-stu-id="46189-114">DirectWrite is a text layout and rasterization engine.</span></span> <span data-ttu-id="46189-115">您可以使用 GDI 或 Direct2D 來繪製柵格化文字。</span><span class="sxs-lookup"><span data-stu-id="46189-115">You can use either GDI or Direct2D to draw the rasterized text.</span></span>
-   <span data-ttu-id="46189-116">DirectX Graphic Infrastructure (DXGI) 會執行低層級的工作，例如呈現輸出的畫面格。</span><span class="sxs-lookup"><span data-stu-id="46189-116">DirectX Graphics Infrastructure (DXGI) performs low-level tasks, such as presenting frames for output.</span></span> <span data-ttu-id="46189-117">大部分的應用程式不會直接使用 DXGI。</span><span class="sxs-lookup"><span data-stu-id="46189-117">Most applications do not use DXGI directly.</span></span> <span data-ttu-id="46189-118">而是做為圖形驅動程式與 Direct3D 之間的中繼層。</span><span class="sxs-lookup"><span data-stu-id="46189-118">Rather, it serves as an intermediate layer between the graphics driver and Direct3D.</span></span>

<span data-ttu-id="46189-119">Direct2D 和 DirectWrite 是在 Windows 7 中引進的。</span><span class="sxs-lookup"><span data-stu-id="46189-119">Direct2D and DirectWrite were introduced in Windows 7.</span></span> <span data-ttu-id="46189-120">您也可以透過平臺更新，在 Windows Vista 和 Windows Server 2008 上使用這些功能。</span><span class="sxs-lookup"><span data-stu-id="46189-120">They are also available for Windows Vista and Windows Server 2008 through a Platform Update.</span></span> <span data-ttu-id="46189-121">如需詳細資訊，請參閱 [Windows Vista 的平臺更新](../win7ip/platform-update-for-windows-vista-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="46189-121">For more information, see [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span></span>

<span data-ttu-id="46189-122">Direct2D 是此課程模組的焦點。</span><span class="sxs-lookup"><span data-stu-id="46189-122">Direct2D is the focus of this module.</span></span> <span data-ttu-id="46189-123">雖然 GDI 和 GDI + 都能在 Windows 中繼續受到支援，但建議針對新程式使用 Direct2D 和 DirectWrite。</span><span class="sxs-lookup"><span data-stu-id="46189-123">While both GDI and GDI+ continue to be supported in Windows, Direct2D and DirectWrite are recommended for new programs.</span></span> <span data-ttu-id="46189-124">在某些情況下，混合的技術可能更實用。</span><span class="sxs-lookup"><span data-stu-id="46189-124">In some cases, a mix of technologies might be more practical.</span></span> <span data-ttu-id="46189-125">在這些情況下，Direct2D 和 DirectWrite 是設計來與 GDI 交互操作。</span><span class="sxs-lookup"><span data-stu-id="46189-125">For these situations, Direct2D and DirectWrite are designed to interoperate with GDI.</span></span>

<span data-ttu-id="46189-126">下一節將說明 Direct2D 的一些優點。</span><span class="sxs-lookup"><span data-stu-id="46189-126">The next sections describe some of the benefits of Direct2D.</span></span>

### <a name="hardware-acceleration"></a><span data-ttu-id="46189-127">硬體加速</span><span class="sxs-lookup"><span data-stu-id="46189-127">Hardware Acceleration</span></span>

<span data-ttu-id="46189-128">*硬體加速* 的一詞是指圖形處理器 (GPU) （而非 CPU）所執行的圖形計算。</span><span class="sxs-lookup"><span data-stu-id="46189-128">The term *hardware acceleration* refers to graphics computations performed by the graphics processing unit (GPU), rather than the CPU.</span></span> <span data-ttu-id="46189-129">新式 Gpu 已針對轉譯圖形中所使用的計算類型進行高度優化。</span><span class="sxs-lookup"><span data-stu-id="46189-129">Modern GPUs are highly optimized for the types of computation used in rendering graphics.</span></span> <span data-ttu-id="46189-130">一般來說，從 CPU 移至 GPU 的工作越多越好。</span><span class="sxs-lookup"><span data-stu-id="46189-130">Generally, the more of this work that is moved from the CPU to the GPU, the better.</span></span>

<span data-ttu-id="46189-131">雖然 GDI 支援某些作業的硬體加速，但許多 GDI 作業都會系結至 CPU。</span><span class="sxs-lookup"><span data-stu-id="46189-131">While GDI supports hardware acceleration for certain operations, many GDI operations are bound to the CPU.</span></span> <span data-ttu-id="46189-132">Direct2D 會分層置於 Direct3D 之上，並充分利用 GPU 提供的硬體加速。</span><span class="sxs-lookup"><span data-stu-id="46189-132">Direct2D is layered on top of Direct3D, and takes full advantage of hardware acceleration provided by the GPU.</span></span> <span data-ttu-id="46189-133">如果 GPU 不支援 Direct2D 所需的功能，則 Direct2D 會切換回軟體轉譯。</span><span class="sxs-lookup"><span data-stu-id="46189-133">If the GPU does not support the features needed for Direct2D, then Direct2D falls back to software rendering.</span></span> <span data-ttu-id="46189-134">整體來說，Direct2D 在大部分情況下都優於 GDI 和 GDI +。</span><span class="sxs-lookup"><span data-stu-id="46189-134">Overall, Direct2D outperforms GDI and GDI+ in most situations.</span></span>

### <a name="transparency-and-anti-aliasing"></a><span data-ttu-id="46189-135">透明度和消除鋸齒</span><span class="sxs-lookup"><span data-stu-id="46189-135">Transparency and Anti-aliasing</span></span>

<span data-ttu-id="46189-136">Direct2D 支援完整硬體加速的 Alpha 混合 (透明度) 。</span><span class="sxs-lookup"><span data-stu-id="46189-136">Direct2D supports fully hardware-accelerated alpha-blending (transparency).</span></span>

<span data-ttu-id="46189-137">GDI 對 Alpha 混色的支援有限。</span><span class="sxs-lookup"><span data-stu-id="46189-137">GDI has limited support for alpha-blending.</span></span> <span data-ttu-id="46189-138">大部分 GDI 函數不支援 Alpha 混色，雖然 GDI 支援在 bitblt 作業期間進行 Alpha 混色。</span><span class="sxs-lookup"><span data-stu-id="46189-138">Most GDI functions do not support alpha blending, although GDI does support alpha blending during a bitblt operation.</span></span> <span data-ttu-id="46189-139">GDI + 支援透明度，但 Alpha 混合是由 CPU 所執行，因此不會受益于硬體加速。</span><span class="sxs-lookup"><span data-stu-id="46189-139">GDI+ supports transparency, but the alpha blending is performed by the CPU, so it does not benefit from hardware acceleration.</span></span>

<span data-ttu-id="46189-140">硬體加速 Alpha-混合也啟用了消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="46189-140">Hardware-accelerated alpha-blending also enables anti-aliasing.</span></span> <span data-ttu-id="46189-141">*別名* 是藉由取樣連續函式所造成的成品。</span><span class="sxs-lookup"><span data-stu-id="46189-141">*Aliasing* is an artifact caused by sampling a continuous function.</span></span> <span data-ttu-id="46189-142">例如，當曲線轉換成圖元時，別名可能會造成不規則的外觀。 \[3 \] 任何可減少別名所造成之成品的技巧，都會被視為一種消除鋸齒的形式。</span><span class="sxs-lookup"><span data-stu-id="46189-142">For example, when a curved line is converted to pixels, aliasing can cause a jagged appearance.\[3\] Any technique that reduces the artifacts caused by aliasing is considered a form of anti-aliasing.</span></span> <span data-ttu-id="46189-143">在圖形中，消除鋸齒是藉由使用背景來混合邊緣來完成。</span><span class="sxs-lookup"><span data-stu-id="46189-143">In graphics, anti-aliasing is done by blending edges with the background.</span></span> <span data-ttu-id="46189-144">例如，以下是由 GDI 繪製的圓形，以及 Direct2D 所繪製的相同圓形。</span><span class="sxs-lookup"><span data-stu-id="46189-144">For example, here is a circle drawn by GDI and the same circle drawn by Direct2D.</span></span>

![direct2d 中消除鋸齒技術的圖例。](images/graphics02.png)

<span data-ttu-id="46189-146">下圖顯示每個圓形的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="46189-146">The next image shows a detail of each circle.</span></span>

![上一個影像的詳細資料。](images/graphics03.png)

<span data-ttu-id="46189-148">GDI (左) 所繪製的圓形是由黑色圖元所組成，大約是曲線。</span><span class="sxs-lookup"><span data-stu-id="46189-148">The circle drawn by GDI (left) consists of black pixels that approximate a curve.</span></span> <span data-ttu-id="46189-149">Direct2D 繪製的圓形 (right) 使用混色來建立更平滑的曲線。</span><span class="sxs-lookup"><span data-stu-id="46189-149">The circle drawn by Direct2D (right) uses blending to create a smoother curve.</span></span>

<span data-ttu-id="46189-150">當 GDI) 繪製幾何 (線條和曲線時，不支援消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="46189-150">GDI does not support anti-aliasing when it draws geometry (lines and curves).</span></span> <span data-ttu-id="46189-151">GDI 可以使用 ClearType 來繪製消除鋸齒的文字;除此之外，GDI 文字也是別名。</span><span class="sxs-lookup"><span data-stu-id="46189-151">GDI can draw anti-aliased text using ClearType; but otherwise, GDI text is aliased as well.</span></span> <span data-ttu-id="46189-152">文字的別名特別明顯，因為不規則線條會中斷字型設計，讓文字更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="46189-152">Aliasing is particularly noticeable for text, because the jagged lines disrupt the font design, making the text less readable.</span></span> <span data-ttu-id="46189-153">雖然 GDI + 支援消除鋸齒，但是它會由 CPU 套用，因此效能不如 Direct2D。</span><span class="sxs-lookup"><span data-stu-id="46189-153">Although GDI+ supports anti-aliasing, it is applied by the CPU, so the performance is not as good as Direct2D.</span></span>

### <a name="vector-graphics"></a><span data-ttu-id="46189-154">向量圖形</span><span class="sxs-lookup"><span data-stu-id="46189-154">Vector Graphics</span></span>

<span data-ttu-id="46189-155">Direct2D 支援 *向量圖形*。</span><span class="sxs-lookup"><span data-stu-id="46189-155">Direct2D supports *vector graphics*.</span></span> <span data-ttu-id="46189-156">在向量圖形中，數學公式是用來表示線條和曲線。</span><span class="sxs-lookup"><span data-stu-id="46189-156">In vector graphics, mathematical formulas are used to represent lines and curves.</span></span> <span data-ttu-id="46189-157">這些公式與螢幕解析度無關，因此可以調整成任意的維度。</span><span class="sxs-lookup"><span data-stu-id="46189-157">These formulas are not dependent on screen resolution, so they can be scaled to arbitrary dimensions.</span></span> <span data-ttu-id="46189-158">當影像必須調整以支援不同的監視器大小或螢幕解析度時，向量圖形特別有用。</span><span class="sxs-lookup"><span data-stu-id="46189-158">Vector graphics are particularly useful when an image must be scaled to support different monitor sizes or screen resolutions.</span></span>

## <a name="next"></a><span data-ttu-id="46189-159">下一個</span><span class="sxs-lookup"><span data-stu-id="46189-159">Next</span></span>

[<span data-ttu-id="46189-160">桌面視窗管理員</span><span class="sxs-lookup"><span data-stu-id="46189-160">The Desktop Window Manager</span></span>](the-desktop-window-manager.md)

 

 
