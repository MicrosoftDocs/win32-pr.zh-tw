---
title: 使用 DirectX 搭配高動態範圍顯示和進階色彩
description: 本主題提供使用 Windows 10 advanced color support 將高動態範圍 Direct3D 11 和 Direct3D 12 內容轉譯為 HDR10 顯示的技術總覽。
ms.assetid: ''
ms.topic: article
ms.date: 04/23/2020
ms.openlocfilehash: 14d025e5431c42299c2c7f20ff198efa93959d7b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "104564048"
---
# <a name="using-directx-with-high-dynamic-range-displays-and-advanced-color"></a><span data-ttu-id="4acf5-103">使用具有高動態範圍的 DirectX 顯示和先進的色彩</span><span class="sxs-lookup"><span data-stu-id="4acf5-103">Using DirectX with high dynamic range Displays and Advanced Color</span></span>

<span data-ttu-id="4acf5-104">本主題提供使用 Windows 10 advanced color support 將高動態範圍 (HDR) Direct3D 11 和 Direct3D 12 內容輸出至 HDR10 顯示器的技術總覽。</span><span class="sxs-lookup"><span data-stu-id="4acf5-104">This topic provides a technical overview of outputting high dynamic range (HDR) Direct3D 11 and Direct3D 12 content to an HDR10 display using Windows 10 advanced color support.</span></span> <span data-ttu-id="4acf5-105">它會摘要說明輸出至 HDR10 顯示器的一些主要概念差異，相較于傳統標準動態範圍 (SDR) 顯示。</span><span class="sxs-lookup"><span data-stu-id="4acf5-105">It summarizes some key conceptual differences between outputting to HDR10 displays as compared to traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="4acf5-106">它也涵蓋了您的應用程式正確支援 Windows advanced color 以及建議和最佳作法的關鍵技術需求。</span><span class="sxs-lookup"><span data-stu-id="4acf5-106">It also covers the key technical requirements for your app to properly support Windows advanced color, as well as recommendations and best practices.</span></span>

## <a name="introduction"></a><span data-ttu-id="4acf5-107">簡介</span><span class="sxs-lookup"><span data-stu-id="4acf5-107">Introduction</span></span>

<span data-ttu-id="4acf5-108">Windows 10 支援 HDR 和其他先進的色彩顯示，可提供比傳統 SDR 顯示明顯更高的色彩精確度。</span><span class="sxs-lookup"><span data-stu-id="4acf5-108">Windows 10 supports HDR and other advanced color displays, which provide significantly higher color fidelity than traditional SDR displays.</span></span> <span data-ttu-id="4acf5-109">您可以使用 Direct3D、Direct2D 和其他圖形 Api，將 HDR 內容轉譯成可顯示的功能。</span><span class="sxs-lookup"><span data-stu-id="4acf5-109">You can use Direct3D, Direct2D and other graphics APIs to render HDR content to a capable display.</span></span>

<span data-ttu-id="4acf5-110">Windows advanced color 指的是數個相關技術，第一次是在 Windows 10 1703 版中引進，可提供超過傳統標準動態範圍 (SDR) 顯示色彩功能的支援。</span><span class="sxs-lookup"><span data-stu-id="4acf5-110">Windows advanced color refers to several related technologies, first introduced with Windows 10 version 1703, that provide support for displays that exceed the color capabilities of traditional standard dynamic range (SDR) displays.</span></span> <span data-ttu-id="4acf5-111">以下說明這三個主要的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="4acf5-111">The three major extended capabilities are described below.</span></span> <span data-ttu-id="4acf5-112">最常見的 advanced color display （HDR10）類型支援這三種擴充功能。</span><span class="sxs-lookup"><span data-stu-id="4acf5-112">The most common type of advanced color display, HDR10, supports all three extended capabilities.</span></span>

### <a name="high-dynamic-range"></a><span data-ttu-id="4acf5-113">高動態範圍</span><span class="sxs-lookup"><span data-stu-id="4acf5-113">High dynamic range</span></span>

<span data-ttu-id="4acf5-114">動態範圍是指場景中最大和最小亮度之間的差異;這通常是以 nits) 的每個平方英尺 (candelas 來測量。</span><span class="sxs-lookup"><span data-stu-id="4acf5-114">Dynamic range refers to the difference between the maximum and minimum luminance in a scene; this is often measured in nits (candelas per square centimeter).</span></span> <span data-ttu-id="4acf5-115">真實世界的場景（例如此終止）通常會有10個量級的亮度的動態範圍;人們可以在調整之後辨別更大的範圍。</span><span class="sxs-lookup"><span data-stu-id="4acf5-115">Real world scenes, such as this sunset, often have dynamic ranges of 10 orders of magnitude of luminance; the human eye can discern an even greater range after adaptation.</span></span>

![在標示的場景中具有亮度和最深點的終止圖](images/HDR-HDR.jpg)

<span data-ttu-id="4acf5-117">自從 Direct3D 9 以來，圖形引擎能夠在內部呈現其幕後，且實際精確的精確度。</span><span class="sxs-lookup"><span data-stu-id="4acf5-117">Ever since Direct3D 9, graphics engines have been able to internally render their scenes with this level of physically accurate fidelity.</span></span> <span data-ttu-id="4acf5-118">不過，一般標準動態範圍顯示只會重現3倍以上的亮度數量級，因此任何 HDR 轉譯的內容都必須 tonemapped (壓縮) 到有限的顯示範圍內。</span><span class="sxs-lookup"><span data-stu-id="4acf5-118">However, a typical standard dynamic range display can reproduce only a little more than 3 orders of magnitude of luminance, and therefore any HDR-rendered content had to be tonemapped (compressed) into the limited range of the display.</span></span> <span data-ttu-id="4acf5-119">新的 HDR 顯示，包括符合 HDR10 (BT) standard 的新 HDR，並突破這項限制。</span><span class="sxs-lookup"><span data-stu-id="4acf5-119">New HDR displays, including those that comply with the HDR10 (BT.2100) standard, break through this limitation.</span></span>

### <a name="wide-color-gamut-with-automatic-system-color-management"></a><span data-ttu-id="4acf5-120">具有自動系統色彩管理的寬色彩範圍</span><span class="sxs-lookup"><span data-stu-id="4acf5-120">Wide color gamut with automatic system color management</span></span>

<span data-ttu-id="4acf5-121">色彩色域指的是顯示可能重現之色調的範圍和飽和度。</span><span class="sxs-lookup"><span data-stu-id="4acf5-121">Color gamut refers to the range and saturation of hues that a display can reproduce.</span></span> <span data-ttu-id="4acf5-122">人類眼所能觀察到的最飽和自然色彩是純粹的單色 light，例如，鐳射產生什麼。</span><span class="sxs-lookup"><span data-stu-id="4acf5-122">The most saturated natural color the human eye can perceive is pure, monochromatic light such as what is produced by a laser.</span></span> <span data-ttu-id="4acf5-123">不過，主流取用者顯示器通常只能在 sRGB 範圍內重現色彩，這只代表所有人類可感知色彩的35%。</span><span class="sxs-lookup"><span data-stu-id="4acf5-123">However, mainstream consumer displays can often reproduce colors only within the sRGB gamut, which represents only about 35% of all human-perceivable colors.</span></span> <span data-ttu-id="4acf5-124">下圖是 "光譜 locus" 的標記法，或指定的亮度層級 (的所有可感知色彩) ，其中較小的三角形是 sRGB 範圍。</span><span class="sxs-lookup"><span data-stu-id="4acf5-124">The diagram below is a representation of the human "spectral locus", or all perceivable colors (at a given luminance level), where the smaller triangle is the sRGB gamut.</span></span>

![人力光譜 locus 和 sRGB gamut 的圖表](images/HDR-WCG.jpg)

<span data-ttu-id="4acf5-126">高層級的電腦顯示器具有長時間支援的色彩 gamuts，其寬度遠高於 sRGB，例如 Adobe RGB 和 D65-P3。</span><span class="sxs-lookup"><span data-stu-id="4acf5-126">High end, professional PC displays have long supported color gamuts that are significantly wider than sRGB, such as Adobe RGB and D65-P3.</span></span> <span data-ttu-id="4acf5-127">而這些寬範圍顯示變得更為普遍。</span><span class="sxs-lookup"><span data-stu-id="4acf5-127">And these wide gamut displays are becoming more common.</span></span> <span data-ttu-id="4acf5-128">不過，在 advanced 色彩之前，Windows 不會針對應用程式執行任何系統層級的色彩管理。</span><span class="sxs-lookup"><span data-stu-id="4acf5-128">However, prior to advanced color, Windows didn't perform any system-level color management for applications.</span></span> <span data-ttu-id="4acf5-129">這表示，如果將 DirectX 應用程式轉譯為純紅色或 RGB (1.0、0.0、0.0) 至其交換鏈，則 Windows 只會掃描顯示器可能重現的最飽和紅色，不論顯示器的實際色彩範圍為何。</span><span class="sxs-lookup"><span data-stu-id="4acf5-129">This meant that if a DirectX app rendered, for example, a pure red or RGB(1.0, 0.0, 0.0) to its swap chain, then Windows would simply scan out the most saturated red that the display could reproduce, regardless of what the actual color gamut of the display was.</span></span>

<span data-ttu-id="4acf5-130">需要高顏色精確度的應用程式可以查詢顯示器的色彩功能 (例如，使用 ICC 設定檔) ，以及執行自己的同進程色彩管理，以正確地鎖定顯示器的色彩範圍。</span><span class="sxs-lookup"><span data-stu-id="4acf5-130">Apps that needed high color accuracy could query the color capabilities of the display (for example, using ICC profiles), and perform their own in-process color management to correctly target the display's color gamut.</span></span> <span data-ttu-id="4acf5-131">不過，大部分的應用程式和視覺內容會假設顯示為 sRGB，而且它們依賴作業系統來滿足此假設。</span><span class="sxs-lookup"><span data-stu-id="4acf5-131">However, the vast majority of apps and visual content assume that the display is sRGB, and they rely on the operating system to fulfill this assumption.</span></span>

<span data-ttu-id="4acf5-132">Windows advanced color 會新增系統層級的自動色彩管理。</span><span class="sxs-lookup"><span data-stu-id="4acf5-132">Windows advanced color adds automatic system-level color management.</span></span> <span data-ttu-id="4acf5-133">桌面視窗管理員 (DWM) 是 Windows 的組合器。</span><span class="sxs-lookup"><span data-stu-id="4acf5-133">The Desktop Window Manager (DWM) is Windows' compositor.</span></span> <span data-ttu-id="4acf5-134">啟用 advanced color 時，DWM 會從應用程式視覺內容的 colorspace 執行明確的色彩轉換，到標準的組合色彩空間，也就是 scRGB。</span><span class="sxs-lookup"><span data-stu-id="4acf5-134">When advanced color is enabled, the DWM performs an explicit color conversion from the app visual content's colorspace to a canonical composition color space, which is scRGB.</span></span> <span data-ttu-id="4acf5-135">然後，Windows 會將組成的畫面格緩衝區內容轉換成顯示器的原生色彩空間。</span><span class="sxs-lookup"><span data-stu-id="4acf5-135">Windows then color-converts the composed framebuffer content to the display's native color space.</span></span> <span data-ttu-id="4acf5-136">如此一來，傳統的 sRGB 內容就會自動取得色彩精確的行為，而 advanced color 感知的應用程式可以利用顯示器的完整色彩功能。</span><span class="sxs-lookup"><span data-stu-id="4acf5-136">In this way, traditional sRGB content automatically gets color-accurate behavior, while advanced color-aware apps can take advantage of the full color capabilities of the display.</span></span>

### <a name="deep-precisionbit-depth"></a><span data-ttu-id="4acf5-137">深度精確度/位深度</span><span class="sxs-lookup"><span data-stu-id="4acf5-137">Deep precision/bit depth</span></span>

<span data-ttu-id="4acf5-138">數值有效位數（或位深度）指的是表示或區分相似但不同的色彩，而不含內條紋或成品。</span><span class="sxs-lookup"><span data-stu-id="4acf5-138">Numerical precision, or bit depth, refers to representing or distinguishing between similar but distinct colors without banding nor artifacts.</span></span> <span data-ttu-id="4acf5-139">主要電腦會顯示每個色頻支援8個位，而人類眼需要至少10-12 位的精確度來避免可感知扭曲，而不需要利用遞色或不同的視圖條件等技術。</span><span class="sxs-lookup"><span data-stu-id="4acf5-139">Mainstream PC displays support 8 bits per color channel, while the human eye requires at least 10-12 bits of precision to avoid perceivable distortions, without resorting to techniques such as dithering or depending on viewing conditions.</span></span>

![風車在每個顏色通道的模擬2位上的圖片，與每個通道8個位的圖片](images/HDR-bitdepth.jpg)

<span data-ttu-id="4acf5-141">在使用 advanced 色彩之前，DWM 限制視窗化應用程式只會在每個顏色通道的8個位輸出內容，即使顯示器支援較高的位深度也一樣。</span><span class="sxs-lookup"><span data-stu-id="4acf5-141">Prior to advanced color, the DWM restricted windowed apps to output content at only 8 bits per color channel, even if the display supported a higher bit depth.</span></span> <span data-ttu-id="4acf5-142">啟用 advanced color 時，DWM 會使用 IEEE 半精確度浮點數來執行其組合 (FP16) ，消除任何瓶頸，並允許使用顯示的完整精確度。</span><span class="sxs-lookup"><span data-stu-id="4acf5-142">When advanced color is enabled, the DWM performs its composition using IEEE half-precision floating point (FP16), eliminating any bottlenecks, and allowing the full precision of the display to be used.</span></span>

## <a name="system-requirements"></a><span data-ttu-id="4acf5-143">系統需求</span><span class="sxs-lookup"><span data-stu-id="4acf5-143">System Requirements</span></span>

### <a name="operating-system-os"></a><span data-ttu-id="4acf5-144">作業系統 (OS)</span><span class="sxs-lookup"><span data-stu-id="4acf5-144">Operating system (OS)</span></span>

<span data-ttu-id="4acf5-145">先進的色彩支援首次隨附于 Windows 10，版本1703，並已在每次更新時大幅改進。</span><span class="sxs-lookup"><span data-stu-id="4acf5-145">Advanced color support first shipped with Windows 10, version 1703, and it has been significantly improved with each update.</span></span> <span data-ttu-id="4acf5-146">本主題假設您的應用程式是以 Windows 10、1903版或更新版本為目標。</span><span class="sxs-lookup"><span data-stu-id="4acf5-146">This topic assumes that your app is targeting Windows 10, version 1903, or later.</span></span>

### <a name="display"></a><span data-ttu-id="4acf5-147">顯示</span><span class="sxs-lookup"><span data-stu-id="4acf5-147">Display</span></span>

<span data-ttu-id="4acf5-148">若要利用高動態範圍，您必須具有支援 HDR10 標準的顯示器。</span><span class="sxs-lookup"><span data-stu-id="4acf5-148">To take advantage of high dynamic range, you must have a display that supports the HDR10 standard.</span></span> <span data-ttu-id="4acf5-149">Windows 最適合與 [DisplayHDR 認證](https://displayhdr.org/)的顯示器搭配使用。</span><span class="sxs-lookup"><span data-stu-id="4acf5-149">Windows works best with displays that are [VESA DisplayHDR certified](https://displayhdr.org/).</span></span>

### <a name="graphics-processor-gpu"></a><span data-ttu-id="4acf5-150">圖形處理器 (GPU) </span><span class="sxs-lookup"><span data-stu-id="4acf5-150">Graphics processor (GPU)</span></span>

<span data-ttu-id="4acf5-151">需要最新的 GPU。</span><span class="sxs-lookup"><span data-stu-id="4acf5-151">A recent GPU is required.</span></span> <span data-ttu-id="4acf5-152">若要支援 HDR10 顯示，Windows 10 需要下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="4acf5-152">To support HDR10 displays, Windows 10 requires one of the following.</span></span>

* <span data-ttu-id="4acf5-153">Nvidia GeForce 1000 系列 (Pascal) 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4acf5-153">Nvidia GeForce 1000 series (Pascal), or newer</span></span>
* <span data-ttu-id="4acf5-154">AMD Radeon RX 400 系列 (Polaris) 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4acf5-154">AMD Radeon RX 400 series (Polaris), or newer</span></span>
* <span data-ttu-id="4acf5-155">選取的 Intel Core 7 系列 (Kaby Lake) 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4acf5-155">Selected Intel Core 7 series (Kaby Lake), or newer</span></span>

<span data-ttu-id="4acf5-156">請注意，視案例而定，需要額外的硬體需求，包括硬體編解碼器加速 (10 位 HEVC、10位 VP9 等等 ) 和 PlayReady 支援 (SL3000) 。</span><span class="sxs-lookup"><span data-stu-id="4acf5-156">Note that additional hardware requirements apply depending on the scenarios, including hardware codec acceleration (10 bit HEVC, 10 bit VP9, etc.) and PlayReady support (SL3000).</span></span> <span data-ttu-id="4acf5-157">如需更具體的資訊，請洽詢您的 GPU 廠商。</span><span class="sxs-lookup"><span data-stu-id="4acf5-157">Contact your GPU vendor for more specific information.</span></span>

### <a name="graphics-driver-wddm"></a><span data-ttu-id="4acf5-158">圖形驅動程式 (WDDM) </span><span class="sxs-lookup"><span data-stu-id="4acf5-158">Graphics driver (WDDM)</span></span>

<span data-ttu-id="4acf5-159">強烈建議您從 Windows Update 或從 GPU 廠商或電腦製造商的網站，取得最新的可用圖形驅動程式。</span><span class="sxs-lookup"><span data-stu-id="4acf5-159">The latest available graphics driver is strongly recommended, either from Windows Update or from the GPU vendor or PC manufacturer's website.</span></span> <span data-ttu-id="4acf5-160">針對 Windows 10、1903版和更新版本，建議至少支援 Windows 顯示驅動程式模型的驅動程式 (WDDM) 2.6 版。</span><span class="sxs-lookup"><span data-stu-id="4acf5-160">For Windows 10, version 1903, and later, we recommend drivers that support at least Windows Display Driver Model (WDDM) version 2.6.</span></span>

## <a name="supported-rendering-apis"></a><span data-ttu-id="4acf5-161">支援的轉譯 Api</span><span class="sxs-lookup"><span data-stu-id="4acf5-161">Supported rendering APIs</span></span>

<span data-ttu-id="4acf5-162">Windows 10 支援各種不同的轉譯 Api 和架構。</span><span class="sxs-lookup"><span data-stu-id="4acf5-162">Windows 10 supports a wide variety of rendering APIs and frameworks.</span></span> <span data-ttu-id="4acf5-163">先進的色彩支援基本上依賴您的應用程式，能夠使用 DXGI 或 Visual Layer Api 來執行新式簡報。</span><span class="sxs-lookup"><span data-stu-id="4acf5-163">Advanced color support fundamentally relies on your app being able to perform modern presentation using either DXGI or the Visual Layer APIs.</span></span>

* [<span data-ttu-id="4acf5-164">DirectX Graphic Infrastructure (DXGI) </span><span class="sxs-lookup"><span data-stu-id="4acf5-164">DirectX Graphics Infrastructure (DXGI)</span></span>](../direct3ddxgi/dx-graphics-dxgi.md)
* [<span data-ttu-id="4acf5-165">視覺分層 (的) </span><span class="sxs-lookup"><span data-stu-id="4acf5-165">Visual Layer (Windows.UI.Composition)</span></span>](/windows/uwp/composition/visual-layer)

<span data-ttu-id="4acf5-166">因此，任何可以輸出至其中一種展示方法的轉譯 API 都可以支援 advanced 色彩。</span><span class="sxs-lookup"><span data-stu-id="4acf5-166">Therefore, any rendering API that can output to one of these presentations methods can support advanced color.</span></span> <span data-ttu-id="4acf5-167">這包括但不限於這些。</span><span class="sxs-lookup"><span data-stu-id="4acf5-167">This includes but is not limited to these.</span></span>

* [<span data-ttu-id="4acf5-168">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="4acf5-168">Direct3D 11</span></span>](../direct3d11/atoc-dx-graphics-direct3d-11.md)
* [<span data-ttu-id="4acf5-169">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4acf5-169">Direct3D 12</span></span>](../direct3d12/direct3d-12-graphics.md)
* [<span data-ttu-id="4acf5-170">Direct2D</span><span class="sxs-lookup"><span data-stu-id="4acf5-170">Direct2D</span></span>](../direct2d/direct2d-portal.md)
* [<span data-ttu-id="4acf5-171">Win2D</span><span class="sxs-lookup"><span data-stu-id="4acf5-171">Win2D</span></span>](https://github.com/Microsoft/Win2D)
  * <span data-ttu-id="4acf5-172">需要使用較低層級的 **CanvasSwapChain** 或 **CanvasSwapChainPanel** api。</span><span class="sxs-lookup"><span data-stu-id="4acf5-172">Requires using the lower level **CanvasSwapChain** or **CanvasSwapChainPanel** APIs.</span></span>
* [<span data-ttu-id="4acf5-173">**Windows.UI.Input.Inking**</span><span class="sxs-lookup"><span data-stu-id="4acf5-173">**Windows.UI.Input.Inking**</span></span>](/uwp/api/Windows.UI.Input.Inking)
  * <span data-ttu-id="4acf5-174">支援使用 DirectX 進行自訂的幹筆墨轉譯。</span><span class="sxs-lookup"><span data-stu-id="4acf5-174">Supports custom dry ink rendering using DirectX.</span></span>
* [<span data-ttu-id="4acf5-175">XAML</span><span class="sxs-lookup"><span data-stu-id="4acf5-175">XAML</span></span>](/windows/uwp/xaml-platform/)
  * <span data-ttu-id="4acf5-176">支援使用 **MediaPlayerElement** 播放 HDR 影片。</span><span class="sxs-lookup"><span data-stu-id="4acf5-176">Supports playback of HDR videos using **MediaPlayerElement**.</span></span>
  * <span data-ttu-id="4acf5-177">支援使用 **Image** 元素解碼 JPEG XR 影像。</span><span class="sxs-lookup"><span data-stu-id="4acf5-177">Supports decode of JPEG XR images using **Image** element.</span></span>
  * <span data-ttu-id="4acf5-178">支援使用 **SwapChainPanel** 的 DirectX interop。</span><span class="sxs-lookup"><span data-stu-id="4acf5-178">Supports DirectX interop using **SwapChainPanel**.</span></span>

## <a name="handling-dynamic-display-capabilities"></a><span data-ttu-id="4acf5-179">處理動態顯示功能</span><span class="sxs-lookup"><span data-stu-id="4acf5-179">Handling dynamic display capabilities</span></span>

<span data-ttu-id="4acf5-180">Windows 10 支援從電源有效率的整合式面板，到高階遊戲監視器和電視的強大高度色彩顯示。</span><span class="sxs-lookup"><span data-stu-id="4acf5-180">Windows 10 supports an enormous range of advanced color-capable displays, from power-efficient integrated panels to high end gaming monitors and TVs.</span></span> <span data-ttu-id="4acf5-181">Windows 使用者預期您的應用程式會順暢地處理所有這些變化，包括無所不在的現有 SDR 顯示器。</span><span class="sxs-lookup"><span data-stu-id="4acf5-181">Windows users expect that your app will seamlessly handle all of these variations, including ubiquitous existing SDR displays.</span></span>

<span data-ttu-id="4acf5-182">Windows 10 可對使用者提供 HDR 和 advanced color 功能的控制權。</span><span class="sxs-lookup"><span data-stu-id="4acf5-182">Windows 10 provides control over HDR and advanced color capabilities to the user.</span></span> <span data-ttu-id="4acf5-183">您的應用程式必須偵測目前顯示器的設定，並動態回應功能的任何變更。</span><span class="sxs-lookup"><span data-stu-id="4acf5-183">Your app must detect the current display's configuration, and respond dynamically to any changes in capability.</span></span> <span data-ttu-id="4acf5-184">可能的原因有很多，例如，使用者啟用或停用某項功能，或是在不同顯示器之間移動應用程式，或系統的電源狀態變更。</span><span class="sxs-lookup"><span data-stu-id="4acf5-184">This could occur for many reasons, for example, because the user enabled or disabled a feature, or moved the app between different displays, or the system's power state changed.</span></span>

### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="4acf5-185">通用 Windows 平台 (UWP) 應用程式</span><span class="sxs-lookup"><span data-stu-id="4acf5-185">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="4acf5-186">如果您要撰寫 UWP 應用程式，而不論您所使用的圖形轉譯 API 為何，請使用 [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) 來取得顯示功能。</span><span class="sxs-lookup"><span data-stu-id="4acf5-186">If you're writing a UWP app, regardless of the graphics rendering API you're using, use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get display capabilities.</span></span> <span data-ttu-id="4acf5-187">從 [**DisplayInformation：： GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo)取得 **AdvancedColorInfo** 的實例。</span><span class="sxs-lookup"><span data-stu-id="4acf5-187">Obtain an instance of **AdvancedColorInfo** from [**DisplayInformation::GetAdvancedColorInfo**](/uwp/api/windows.graphics.display.displayinformation.getadvancedcolorinfo).</span></span>

<span data-ttu-id="4acf5-188">若要檢查目前作用中的「高級」色彩種類，請使用 [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4acf5-188">To check what advanced color kind is currently active, use the [**CurrentAdvancedColorKind**](/uwp/api/windows.graphics.display.advancedcolorinfo.currentadvancedcolorkind) property.</span></span> <span data-ttu-id="4acf5-189">在 Windows 10、1903版和更新版本中，這會傳回三個可能值的其中一個： **SDR**、 **WCG** 或 **HDR**。</span><span class="sxs-lookup"><span data-stu-id="4acf5-189">In Windows 10, version 1903, and later, this returns one of three possible values: **SDR**, **WCG**, or **HDR**.</span></span> <span data-ttu-id="4acf5-190">這是最重要的檢查屬性，您應該設定轉譯和呈現管線以回應使用中的種類。</span><span class="sxs-lookup"><span data-stu-id="4acf5-190">This is the most important property to check, and you should configure your render and presentation pipeline in response to the active kind.</span></span>

<span data-ttu-id="4acf5-191">若要檢查支援的 advanced 色彩種類，但不一定要使用，請呼叫 [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable)。</span><span class="sxs-lookup"><span data-stu-id="4acf5-191">To check what advanced color kinds are supported, but not necessarily active, call [**IsAdvancedColorKindAvailable**](/uwp/api/windows.graphics.display.advancedcolorinfo.isadvancedcolorkindavailable).</span></span> <span data-ttu-id="4acf5-192">例如，您可以使用此資訊來提示使用者流覽至 Windows [設定] 應用程式，讓他們可以啟用 HDR 或 WCG。</span><span class="sxs-lookup"><span data-stu-id="4acf5-192">You could use this information, for example, to prompt the user to navigate to the Windows Settings app so that they can enable HDR or WCG.</span></span>

<span data-ttu-id="4acf5-193">**AdvancedColorInfo** 的其他成員會提供有關面板實體色彩磁片區的量化資訊 (明亮度和色度) ，其對應于2006靜態 HDR 中繼資料。</span><span class="sxs-lookup"><span data-stu-id="4acf5-193">The other members of **AdvancedColorInfo** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="4acf5-194">您應使用此資訊來設定應用程式的 HDR tonemapping 和 gamut 對應。</span><span class="sxs-lookup"><span data-stu-id="4acf5-194">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="4acf5-195">若要處理 advanced color 功能的變更，請註冊 [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) 事件。</span><span class="sxs-lookup"><span data-stu-id="4acf5-195">To handle changes in advanced color capabilities, register for the [**AdvancedColorInfoChanged**](/uwp/api/windows.graphics.display.displayinformation.advancedcolorinfochanged) event.</span></span> <span data-ttu-id="4acf5-196">如果顯示的 advanced color 功能的任何參數因任何原因而變更，就會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="4acf5-196">This event is raised if any parameter of the display's advanced color capabilities changes for any reason.</span></span>

<span data-ttu-id="4acf5-197">藉由取得 **AdvancedColorInfo** 的新實例，並檢查哪些值已變更，來處理這個事件。</span><span class="sxs-lookup"><span data-stu-id="4acf5-197">Handle this event by obtaining a new instance of **AdvancedColorInfo**, and checking which values have changed.</span></span>

### <a name="desktop-win32-directx-apps"></a><span data-ttu-id="4acf5-198">Desktop (Win32) DirectX 應用程式</span><span class="sxs-lookup"><span data-stu-id="4acf5-198">Desktop (Win32) DirectX apps</span></span>

<span data-ttu-id="4acf5-199">如果您要撰寫 Win32 應用程式，並使用 DirectX 轉譯，請使用 [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) 來取得顯示功能。</span><span class="sxs-lookup"><span data-stu-id="4acf5-199">If you're writing a Win32 app, and using DirectX to render, then use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get display capabilities.</span></span> <span data-ttu-id="4acf5-200">透過 [**IDXGIOutput6：： GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1)取得此結構的實例。</span><span class="sxs-lookup"><span data-stu-id="4acf5-200">Obtain an instance of this struct via [**IDXGIOutput6::GetDesc1**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-getdesc1).</span></span>

<span data-ttu-id="4acf5-201">若要檢查目前作用中的「高階」色彩種類，請使用 [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)類型的 **ColorSpace** 屬性，並包含下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="4acf5-201">To check what advanced color kind is currently active, use the **ColorSpace** property, which is of type [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), and contains one of the following values:</span></span>

* <span data-ttu-id="4acf5-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**，SDR</span><span class="sxs-lookup"><span data-stu-id="4acf5-202">**DXGI_COLOR_SPACE_RGB_FULL_G22_NONE_P709**, SDR</span></span>
* <span data-ttu-id="4acf5-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**、HDR</span><span class="sxs-lookup"><span data-stu-id="4acf5-203">**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**, HDR</span></span>

> [!Note]
> <span data-ttu-id="4acf5-204">其他 advanced 色彩類型（例如 WCG）會被 DXGI 視為 SDR。</span><span class="sxs-lookup"><span data-stu-id="4acf5-204">Other advanced color kinds such as WCG are treated as SDR by DXGI.</span></span> <span data-ttu-id="4acf5-205">您無法使用 DXGI 來識別 WCG 顯示器。</span><span class="sxs-lookup"><span data-stu-id="4acf5-205">You can't use DXGI to identify a WCG display.</span></span>

> [!Note]
> <span data-ttu-id="4acf5-206">DXGI 不會讓您檢查目前支援的 advanced 色彩類型，但目前不會使用。</span><span class="sxs-lookup"><span data-stu-id="4acf5-206">DXGI doesn't let you check what advanced color kinds are supported but not active at the moment.</span></span>

<span data-ttu-id="4acf5-207">**DXGI_OUTPUT_DESC1** 的其他成員大部分會提供與2006靜態 HDR 中繼資料相關之面板實體色彩磁片區的量化資訊， (亮度和色度) 。</span><span class="sxs-lookup"><span data-stu-id="4acf5-207">Most of the other members of **DXGI_OUTPUT_DESC1** provide quantitative information about the panel's physical color volume (luminance and chrominance), corresponding to SMPTE ST.2086 static HDR metadata.</span></span> <span data-ttu-id="4acf5-208">您應使用此資訊來設定應用程式的 HDR tonemapping 和 gamut 對應。</span><span class="sxs-lookup"><span data-stu-id="4acf5-208">You should use this information to configure your app's HDR tonemapping and gamut mapping.</span></span>

<span data-ttu-id="4acf5-209">Win32 應用程式沒有原生機制可回應 advanced color 功能變更。</span><span class="sxs-lookup"><span data-stu-id="4acf5-209">Win32 apps don't have a native mechanism to respond to advanced color capability changes.</span></span> <span data-ttu-id="4acf5-210">相反地，如果您的應用程式使用轉譯迴圈，則您應該使用每個畫面格來查詢 [**IDXGIFactory1：： IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) 。</span><span class="sxs-lookup"><span data-stu-id="4acf5-210">Instead, if your app uses a render loop, then you should query [**IDXGIFactory1::IsCurrent**](/windows/desktop/api/DXGI/nf-dxgi-idxgifactory1-iscurrent) with each frame.</span></span> <span data-ttu-id="4acf5-211">如果報告 **為 FALSE**，則您應該取得新的 **DXGI_OUTPUT_DESC1**，並檢查哪些值已變更。</span><span class="sxs-lookup"><span data-stu-id="4acf5-211">If it reports **FALSE**, then you should obtain a new **DXGI_OUTPUT_DESC1**, and check which values have changed.</span></span>

<span data-ttu-id="4acf5-212">此外，您的 Win32 訊息抽取應該會處理 [**WM_SIZE**](../winmsg/wm-size.md) 訊息，這表示您的應用程式可能已在不同顯示器之間移動。</span><span class="sxs-lookup"><span data-stu-id="4acf5-212">In addition, your Win32 message pump should handle the [**WM_SIZE**](../winmsg/wm-size.md) message, which indicates that your app may have moved between different displays.</span></span>

> [!Note]
> <span data-ttu-id="4acf5-213">若要取得新的 **DXGI_OUTPUT_DESC1**，您必須取得目前的顯示。</span><span class="sxs-lookup"><span data-stu-id="4acf5-213">To obtain a new **DXGI_OUTPUT_DESC1**, you must obtain the current display.</span></span> <span data-ttu-id="4acf5-214">不過，您不應該呼叫 **IDXGISwapChain：： GetContainingOutput**。</span><span class="sxs-lookup"><span data-stu-id="4acf5-214">However, you should not call **IDXGISwapChain::GetContainingOutput**.</span></span> <span data-ttu-id="4acf5-215">這是因為當 **DXGIFactory：： IsCurrent** 為 false，並重新建立交換鏈以將目前的輸出結果設為暫時性的黑色畫面時，交換鏈會傳回過時的 DXGI 輸出。</span><span class="sxs-lookup"><span data-stu-id="4acf5-215">This is because swap chains will return a stale DXGI output once **DXGIFactory::IsCurrent** is false, and recreating the swap chain to get a current output results in a temporary black screen.</span></span> <span data-ttu-id="4acf5-216">相反地，我們建議您列舉所有 DXGI 輸出的界限，並判斷哪一個輸出與您應用程式視窗的範圍有最大的交集。</span><span class="sxs-lookup"><span data-stu-id="4acf5-216">Instead, we recommend that you enumerate through the bounds of all DXGI outputs, and determine which one has the greatest intersection with your app window's bounds.</span></span>

<span data-ttu-id="4acf5-217">下列程式碼範例來自于 [DirectX-圖形範例存放庫](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR)。</span><span class="sxs-lookup"><span data-stu-id="4acf5-217">The following code example comes from the [DirectX-Graphics-Samples repository](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span>

```cpp
// Retrieve the current default adapter.
ComPtr<IDXGIAdapter1> dxgiAdapter;
ThrowIfFailed(m_dxgiFactory->EnumAdapters1(0, &dxgiAdapter));

// Iterate through the DXGI outputs associated with the DXGI adapter,
// and find the output whose bounds have the greatest overlap with the
// app window (i.e. the output for which the intersection area is the
// greatest).

UINT i = 0;
ComPtr<IDXGIOutput> currentOutput;
ComPtr<IDXGIOutput> bestOutput;
float bestIntersectArea = -1;

while (dxgiAdapter->EnumOutputs(i, &currentOutput) != DXGI_ERROR_NOT_FOUND)
{
    // Get the retangle bounds of the app window
    int ax1 = m_windowBounds.left;
    int ay1 = m_windowBounds.top;
    int ax2 = m_windowBounds.right;
    int ay2 = m_windowBounds.bottom;

    // Get the rectangle bounds of current output
    DXGI_OUTPUT_DESC desc;
    ThrowIfFailed(currentOutput->GetDesc(&desc));
    RECT r = desc.DesktopCoordinates;
    int bx1 = r.left;
    int by1 = r.top;
    int bx2 = r.right;
    int by2 = r.bottom;

    // Compute the intersection
    int intersectArea = ComputeIntersectionArea(ax1, ay1, ax2, ay2, bx1, by1, bx2, by2);
    if (intersectArea > bestIntersectArea)
    {
        bestOutput = currentOutput;
        bestIntersectArea = static_cast<float>(intersectArea);
    }

    i++;
}

// Having determined the output (display) upon which the app is primarily being 
// rendered, retrieve the HDR capabilities of that display by checking the color space.
ComPtr<IDXGIOutput6> output6;
ThrowIfFailed(bestOutput.As(&output6));

DXGI_OUTPUT_DESC1 desc1;
ThrowIfFailed(output6->GetDesc1(&desc1));
```

## <a name="setting-up-your-directx-swap-chain"></a><span data-ttu-id="4acf5-218">設定您的 DirectX 交換鏈</span><span class="sxs-lookup"><span data-stu-id="4acf5-218">Setting up Your DirectX swap chain</span></span>

<span data-ttu-id="4acf5-219">一旦您判斷出目前的顯示器支援 advanced color 功能之後，請依照下列方式設定交換鏈。</span><span class="sxs-lookup"><span data-stu-id="4acf5-219">Once you have determined that the display currently supports advanced color capabilities, configure your swap chain as follows.</span></span>

### <a name="use-a-flip-presentation-model-effect"></a><span data-ttu-id="4acf5-220">使用翻轉展示模型效果</span><span class="sxs-lookup"><span data-stu-id="4acf5-220">Use a flip presentation model effect</span></span>

<span data-ttu-id="4acf5-221">使用 CreateSwapChainFor 建立交換鏈時 **[Hwnd |組合 |CoreWindow]** 方法中，您必須選取 [ **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** ] 或 [ **DXGI_SWAP_EFFECT_FLIP_DISCARD** ] 選項來使用 DXGI 翻轉模型，讓您的交換鏈符合從 DWM 和各種全螢幕優化進行的 advanced color 處理。</span><span class="sxs-lookup"><span data-stu-id="4acf5-221">When creating your swap chain using the **CreateSwapChainFor[Hwnd|Composition|CoreWindow]** methods, you must use the DXGI flip model by selecting either the **DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL** or **DXGI_SWAP_EFFECT_FLIP_DISCARD** option, which makes your swap chain eligible for advanced color processing from DWM and various fullscreen optimizations.</span></span> <span data-ttu-id="4acf5-222">如需詳細資訊，請參閱，以取得 [最佳效能，請使用 [DXGI 反轉模型](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) ] 主題。</span><span class="sxs-lookup"><span data-stu-id="4acf5-222">For more information, refer to the [For best performance, use DXGI flip model](../direct3ddxgi/for-best-performance--use-dxgi-flip-model.md) topic.</span></span>

### <a name="option-1-use-fp16-pixel-format-and-scrgb-color-space"></a><span data-ttu-id="4acf5-223">選項 1。</span><span class="sxs-lookup"><span data-stu-id="4acf5-223">Option 1.</span></span> <span data-ttu-id="4acf5-224">使用 FP16 像素格式和 scRGB 色彩空間</span><span class="sxs-lookup"><span data-stu-id="4acf5-224">Use FP16 pixel format and scRGB color space</span></span>

<span data-ttu-id="4acf5-225">Windows 10 支援兩種主要的像素格式和色彩空間組合，以用於 advanced 色彩。</span><span class="sxs-lookup"><span data-stu-id="4acf5-225">Windows 10 supports two main combinations of pixel format and color space for advanced color.</span></span> <span data-ttu-id="4acf5-226">根據您應用程式的特定需求選取一個。</span><span class="sxs-lookup"><span data-stu-id="4acf5-226">Select one based on your app's specific requirements.</span></span>

<span data-ttu-id="4acf5-227">針對一般用途的應用程式，在建立交換鏈時，建議您指定 [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)。</span><span class="sxs-lookup"><span data-stu-id="4acf5-227">For general-purpose apps, when creating your swap chain we recommend specifying [**DXGI_FORMAT_R16G16B16A16_FLOAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="4acf5-228">這在您的 [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)也稱為 *FP16* 。</span><span class="sxs-lookup"><span data-stu-id="4acf5-228">That's also known as *FP16* in your [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="4acf5-229">根據預設，以浮點數像素格式建立的交換鏈會視為使用 [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) 色彩空間，也稱為 *scRGB*。</span><span class="sxs-lookup"><span data-stu-id="4acf5-229">By default, a swap chain created with a floating point pixel format is treated as if it uses the [**DXGI_COLOR_SPACE_RGB_FULL_G10_NONE_P709**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) color space, which is also known as *scRGB*.</span></span>

<span data-ttu-id="4acf5-230">這種組合可提供您數位範圍和精確度，以指定幾乎任何實際可能的色彩，並執行任意處理，包括混色。</span><span class="sxs-lookup"><span data-stu-id="4acf5-230">This combination provides you with the numeric range and precision to specify almost any physically possible color, and perform arbitrary processing including blending.</span></span> <span data-ttu-id="4acf5-231">此外，如果您使用的是 Direct2D、Win2D 或 Windows，則這是包含 advanced color 內容之任何交換鏈或中繼目標的唯一支援組合。</span><span class="sxs-lookup"><span data-stu-id="4acf5-231">In addition, if you're using Direct2D, Win2D, or Windows.UI.Composition, then this is the only supported combination for any swap chain or intermediate target that contains advanced color content.</span></span> 

<span data-ttu-id="4acf5-232">此選項的主要缺點是，它會每圖元耗用64位，相較于傳統 UINT8 的 SDR 像素格式，這會使 GPU 頻寬和記憶體耗用量加倍。</span><span class="sxs-lookup"><span data-stu-id="4acf5-232">The main tradeoff of this option is that it consumes 64 bits per pixel, which doubles GPU bandwidth and memory consumption compared to the traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="4acf5-233">此外，scRGB 使用非正規化 [0，1] 範圍內的數值，表示位於 sRGB 範圍之外的色彩，以及/或大於 80 nits 的亮度。</span><span class="sxs-lookup"><span data-stu-id="4acf5-233">In addition, scRGB uses numeric values that are outside the normalized [0, 1] range to represent colors that are outside the sRGB gamut and/or greater than 80 nits of luminance.</span></span> <span data-ttu-id="4acf5-234">例如，scRGB (1.0、1.0、1.0) 以 80 nits 編碼標準 D65 白色;但是，scRGB (12.5、12.5、12.5) 會以較亮的 1000 nits 編碼相同的 D65 白色。</span><span class="sxs-lookup"><span data-stu-id="4acf5-234">For example, scRGB (1.0, 1.0, 1.0) encodes the standard D65 white at 80 nits; but scRGB (12.5, 12.5, 12.5) encodes the same D65 white at a much brighter 1000 nits.</span></span> <span data-ttu-id="4acf5-235">某些圖形作業需要標準化的數值範圍，您必須修改作業或重新標準化色彩值。</span><span class="sxs-lookup"><span data-stu-id="4acf5-235">Some graphics operations require a normalized numeric range, and you must either modify the operation, or re-normalize color values.</span></span>

### <a name="option-2-use-uint10rgb10-pixel-format-and-hdr10bt2100-color-space"></a><span data-ttu-id="4acf5-236">選項2：使用 UINT10/RGB10 像素格式和 HDR10/BT. 2100 色彩空間</span><span class="sxs-lookup"><span data-stu-id="4acf5-236">Option 2: Use UINT10/RGB10 pixel format and HDR10/BT.2100 color space</span></span>

<span data-ttu-id="4acf5-237">針對使用 HDR10 編碼內容的應用程式（例如 media player），或是預期在全螢幕案例（例如遊戲）中使用的應用程式，在建立交換鏈時，您應該考慮在 [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)中指定 [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 。</span><span class="sxs-lookup"><span data-stu-id="4acf5-237">For apps that consume HDR10-encoded content, such as media players, or apps that are expected to be used mainly in fullscreen scenarios such as games, when creating your swap chain you should consider specifying [**DXGI_FORMAT_R10G10B10A2_UNORM**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) in [**DXGI_SWAP_CHAIN_DESC1**](/windows/win32/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1).</span></span> <span data-ttu-id="4acf5-238">根據預設，這會被視為使用 sRGB 色彩空間;因此，您必須明確地呼叫 [**IDXGISwapChain3：： SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1)，並設定為您的色彩空間 [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)，也稱為 HDR10/BT. 2100。</span><span class="sxs-lookup"><span data-stu-id="4acf5-238">By default, this is treated as using the sRGB color space; therefore, you must explicitly call [**IDXGISwapChain3::SetColorSpace1**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1), and set as your color space [**DXGI_COLOR_SPACE_RGB_FULL_G2084_NONE_P2020**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type), also known as HDR10/BT.2100.</span></span>

<span data-ttu-id="4acf5-239">相較于 FP16，此組合具有更嚴格的限制。</span><span class="sxs-lookup"><span data-stu-id="4acf5-239">This combination has more stringent restrictions than FP16.</span></span> <span data-ttu-id="4acf5-240">您只能將此使用於 Direct3D 11 或 Direct3D 12。</span><span class="sxs-lookup"><span data-stu-id="4acf5-240">You can use this only with Direct3D 11 or Direct3D 12.</span></span> <span data-ttu-id="4acf5-241">此外，UINT10/HDR10 具有中繼格式的限制，因為它會使用 2084 EOTF ( "gamma" 函式) （高度非線性），並將其優化為電傳格式，因為它只提供2位的 Alpha。</span><span class="sxs-lookup"><span data-stu-id="4acf5-241">In addition, UINT10/HDR10 has limitations as an intermediate format because it uses the ST.2084 EOTF ("gamma" function), which is highly nonlinear, and optimized as a wire format, and because it offers only 2 bits of alpha.</span></span>

<span data-ttu-id="4acf5-242">不過，在應用程式的最終輸出中使用時，此組合可以提供強大的效能優化。</span><span class="sxs-lookup"><span data-stu-id="4acf5-242">However, this combination can offer powerful performance optimizations when used in your app's final output.</span></span> <span data-ttu-id="4acf5-243">它會使用與傳統 UINT8 SDR 像素格式相同的每個圖元32位。</span><span class="sxs-lookup"><span data-stu-id="4acf5-243">It consumes the same 32 bits per pixel as traditional UINT8 SDR pixel formats.</span></span> <span data-ttu-id="4acf5-244">此外，在特定的全螢幕案例中，作業系統可以直接掃描 HDR10 介面，以優化效能。</span><span class="sxs-lookup"><span data-stu-id="4acf5-244">In addition, in certain fullscreen scenarios, the OS can optimize performance by directly scanning out the HDR10 surface.</span></span>

### <a name="using-an-advanced-color-swap-chain-when-the-display-is-in-sdr-mode"></a><span data-ttu-id="4acf5-245">當顯示器處於 SDR 模式時使用 advanced 色交換鏈</span><span class="sxs-lookup"><span data-stu-id="4acf5-245">Using an advanced color swap chain when the display is in SDR mode</span></span>

<span data-ttu-id="4acf5-246">即使顯示器不支援您的內容所需的部分或所有高階色彩功能，您也可以使用 advanced color swap chain。</span><span class="sxs-lookup"><span data-stu-id="4acf5-246">You can use an advanced color swap chain even if the display doesn't support some or all of the advanced color capabilities your content requires.</span></span> <span data-ttu-id="4acf5-247">在這些情況下，桌面視窗管理員 (DWM) 會 downconvert 您的內容以符合顯示器的功能。</span><span class="sxs-lookup"><span data-stu-id="4acf5-247">In those cases, the Desktop Window Manager (DWM) will downconvert your content to fit the display's capabilities.</span></span> <span data-ttu-id="4acf5-248">在 Windows 10、1903版和更新版本中，它會執行數位裁剪;例如，如果您轉譯成 FP16 的 scRGB 交換鏈，則會裁剪 [0，1] 數值範圍以外的所有專案。</span><span class="sxs-lookup"><span data-stu-id="4acf5-248">In Windows 10, version 1903, and later, it will perform numeric clipping; for example, if you render to an FP16 scRGB swap chain, then everything outside of the [0, 1] numeric range is clipped.</span></span>

<span data-ttu-id="4acf5-249">如果您的應用程式視窗 straddling 了具有不同 advanced 色彩功能的兩個或多個顯示，也會發生此 downconversion 行為。</span><span class="sxs-lookup"><span data-stu-id="4acf5-249">This downconversion behavior will also occur if your app window is straddling two or more displays with differing advanced color capabilities.</span></span> <span data-ttu-id="4acf5-250">**AdvancedColorInfo** 和 **IDXGIOutput6** 是抽象化的，只會報告「主要」顯示的特性 (定義為包含視窗) 中央的顯示。</span><span class="sxs-lookup"><span data-stu-id="4acf5-250">**AdvancedColorInfo** and **IDXGIOutput6** are abstracted to report only the "main" display's characteristics (defined as the display containing the center of the window).</span></span>

## <a name="correctly-render-sdr-content-with-sdr-reference-white-level"></a><span data-ttu-id="4acf5-251">使用 SDR 參考白色層級正確轉譯 SDR 內容</span><span class="sxs-lookup"><span data-stu-id="4acf5-251">Correctly render SDR content with SDR reference white level</span></span>

<span data-ttu-id="4acf5-252">在許多案例中，您的應用程式會想要同時轉譯 SDR 和 HDR 內容;例如，透過 HDR 影片轉譯字幕或傳輸控制項，或將 UI 轉譯為遊戲場景。</span><span class="sxs-lookup"><span data-stu-id="4acf5-252">In many scenarios, your app will want to render both SDR and HDR content; for example, rendering subtitles or transport controls over HDR video, or UI into a game scene.</span></span> <span data-ttu-id="4acf5-253">請務必瞭解 *sdr 參考白色層級* 的概念，以確保您的 sdr 內容在 HDR 顯示器上看起來正確。</span><span class="sxs-lookup"><span data-stu-id="4acf5-253">It is important to understand the concept of *SDR reference white level* to ensure that your SDR content looks correct on an HDR display.</span></span>

<span data-ttu-id="4acf5-254">Windows 會將 HDR 內容視為 _場景_，表示特定的色彩值應顯示在特定的亮度層級;例如，scRGB (1.0、1.0、1.0) 和 HDR10 (497、497、497) 都會以 80 nits 的亮度來精確編碼 D65 的白色。</span><span class="sxs-lookup"><span data-stu-id="4acf5-254">Windows treats HDR content as _scene-referred_, meaning that a particular color value should be displayed at a specific luminance level; for example, scRGB (1.0, 1.0, 1.0) and HDR10 (497, 497, 497) both encode exactly D65 white at 80 nits luminance.</span></span> <span data-ttu-id="4acf5-255">同時，通常會將 SDR 內容視為 _輸出參考_ (或顯示) ，這表示其亮度會保留給使用者或裝置;例如，sRGB (1.0、1.0、1.0) 將 D65 白色編碼為 HDR 範例中的白色，但在任何亮度最高的情況下，會為其設定顯示的亮度。</span><span class="sxs-lookup"><span data-stu-id="4acf5-255">Meanwhile, SDR content traditionally has been _output-referred_ (or display-referred), meaning that its luminance is left up to the user or the device; for example sRGB (1.0, 1.0, 1.0) encodes D65 white as in the HDR examples, but at whatever maximum luminance the display is configured for.</span></span> <span data-ttu-id="4acf5-256">Windows 可讓使用者將 [ _SDR 參考] 的白色層級_ 調整為其喜好設定;這是 Windows 會轉譯 sRGB (1.0、1.0、1.0) 的亮度。</span><span class="sxs-lookup"><span data-stu-id="4acf5-256">Windows allows the user to adjust the _SDR reference white level_ to their preference; this is the luminance that Windows will render sRGB (1.0, 1.0, 1.0) at.</span></span> <span data-ttu-id="4acf5-257">在桌面 HDR 監視器上，SDR 參考白色層級通常設定為大約 200 nits。</span><span class="sxs-lookup"><span data-stu-id="4acf5-257">On desktop HDR monitors, SDR reference white levels are typically set to around 200 nits.</span></span>

> [!Note]
> <span data-ttu-id="4acf5-258">在支援亮度控制項的顯示器（例如膝上型電腦）上，Windows 也會調整 HDR 的亮度 (場景參考的) 內容，以符合使用者所需的亮度等級，但應用程式看不到這一點。</span><span class="sxs-lookup"><span data-stu-id="4acf5-258">On a display that supports a brightness control, such as on a laptop, Windows will also adjust the luminance of HDR (scene-referred) content to match the user's desired brightness level, but this is invisible to the app.</span></span> <span data-ttu-id="4acf5-259">除非您嘗試保證 HDR 信號的精確度重現，否則您通常可以忽略此情況。</span><span class="sxs-lookup"><span data-stu-id="4acf5-259">Unless you're trying to guarantee bit-accurate reproduction of the HDR signal, you can generally ignore this.</span></span>

<span data-ttu-id="4acf5-260">如果您的應用程式一律會將 SDR 和 HDR 轉譯成不同的表面，並依賴作業系統組合，則 Windows 會自動執行正確的調整，以將 SDR 內容提升為所需的白色層級。</span><span class="sxs-lookup"><span data-stu-id="4acf5-260">If your app always renders SDR and HDR to separate surfaces, and relies on OS composition, then Windows will automatically perform the correct adjustment to boost SDR content to the desired white level.</span></span> <span data-ttu-id="4acf5-261">例如，如果您的應用程式使用 XAML，並將 HDR 內容轉譯為它自己的 **SwapChainPanel**。</span><span class="sxs-lookup"><span data-stu-id="4acf5-261">For example, if your app uses XAML and renders HDR content to its own **SwapChainPanel**.</span></span>

<span data-ttu-id="4acf5-262">但是，如果您的應用程式會將自己的 SDR 和 HDR 內容組合成單一介面，您就必須自行負責執行 SDR 參考白色層級調整。</span><span class="sxs-lookup"><span data-stu-id="4acf5-262">However, if your app performs its own composition of SDR and HDR content into a single surface, then you're responsible for performing the SDR reference white level adjustment yourself.</span></span> <span data-ttu-id="4acf5-263">否則，如果有一般的桌上型電腦觀賞條件，則 SDR 內容可能會顯得太暗。</span><span class="sxs-lookup"><span data-stu-id="4acf5-263">Otherwise the SDR content might appear too dim assuming typical desktop viewing conditions.</span></span> <span data-ttu-id="4acf5-264">首先，您必須取得目前的 SDR 參考白色層級，然後您必須調整您正在轉譯之任何 SDR 內容的色彩值。</span><span class="sxs-lookup"><span data-stu-id="4acf5-264">First, you must obtain the current SDR reference white level, and then you must adjust the color values of any SDR content you're rendering.</span></span>

### <a name="step-1-obtain-the-current-sdr-reference-white-level"></a><span data-ttu-id="4acf5-265">步驟 1：</span><span class="sxs-lookup"><span data-stu-id="4acf5-265">Step 1.</span></span> <span data-ttu-id="4acf5-266">取得目前的 SDR 參考白色層級</span><span class="sxs-lookup"><span data-stu-id="4acf5-266">Obtain the current SDR reference white level</span></span>

<span data-ttu-id="4acf5-267">目前，只有 UWP 應用程式可以透過 [**AdvancedColorInfo SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits)取得目前的 SDR 參考白色層級。</span><span class="sxs-lookup"><span data-stu-id="4acf5-267">Currently, only UWP apps can obtain the current SDR reference white level via [**AdvancedColorInfo.SdrWhiteLevelInNits**](/uwp/api/windows.graphics.display.advancedcolorinfo.sdrwhitelevelinnits).</span></span> <span data-ttu-id="4acf5-268">此 API 需要 [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)。</span><span class="sxs-lookup"><span data-stu-id="4acf5-268">This API requires a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

### <a name="step-2-adjust-color-values-of-sdr-content"></a><span data-ttu-id="4acf5-269">步驟 2：</span><span class="sxs-lookup"><span data-stu-id="4acf5-269">Step 2.</span></span> <span data-ttu-id="4acf5-270">調整 SDR 內容的色彩值</span><span class="sxs-lookup"><span data-stu-id="4acf5-270">Adjust color values of SDR content</span></span>

<span data-ttu-id="4acf5-271">Windows 會定義 80 nits; 的名義或預設參考白色層級因此，如果您要轉譯標準 sRGB (1.0、1.0、1.0) 白色 FP16 交換鏈，則會以 80 nits 的亮度重現。</span><span class="sxs-lookup"><span data-stu-id="4acf5-271">Windows defines the nominal, or default, reference white level at 80 nits; therefore if you were to render a standard sRGB (1.0, 1.0, 1.0) white to an FP16 swap chain, it would be reproduced at 80 nits luminance.</span></span> <span data-ttu-id="4acf5-272">為了符合實際的使用者定義參考白色層級，您必須將來自 80 nits 的 SDR 內容調整為透過 **AdvancedColorInfo SdrWhiteLevelInNits** 所指定的層級。</span><span class="sxs-lookup"><span data-stu-id="4acf5-272">In order to match the actual user-defined reference white level, you must adjust SDR content from 80 nits to the level specified via **AdvancedColorInfo.SdrWhiteLevelInNits**.</span></span>

<span data-ttu-id="4acf5-273">如果您是使用 FP16 和 scRGB 進行轉譯，或是使用線性 (1.0) gamma 的任何色彩空間，則您只要將 SDR 色彩值乘以 _AdvancedColorInfo. SdrWhiteLevelInNits_  /  _80_ 就可以了。</span><span class="sxs-lookup"><span data-stu-id="4acf5-273">If you're rendering using FP16 and scRGB, or any color space that uses linear (1.0) gamma, then you can simply multiply the SDR color value by _AdvancedColorInfo.SdrWhiteLevelInNits_ / _80_.</span></span> <span data-ttu-id="4acf5-274">如果您使用的是 Direct2D，則會有預先定義的常數 [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f)，其值為80。</span><span class="sxs-lookup"><span data-stu-id="4acf5-274">If you're using Direct2D, there is a predefined constant [**D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL**](../direct2d/direct2d-constants.md#d2d1_scene_referred_sdr_white_level-800f), which has a value of 80.</span></span>

```cpp
D2D1_VECTOR_4F inputColor; // Input SDR color value.
D2D1_VECTOR_4F outputColor; // Output color adjusted for SDR white level.
auto acInfo; // AdvancedColorInfo

float sdrAdjust = acInfo->SdrWhiteLevelInNits / D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL;

// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
outputColor.r = inputColor.r * sdrAdjust; // Assumes linear gamma color values.
outputColor.g = inputColor.g * sdrAdjust;
outputColor.b = inputColor.b * sdrAdjust;
outputColor.a = inputColor.a;
```

<span data-ttu-id="4acf5-275">如果您要使用非線性 gamma 色彩空間（例如 HDR10）進行轉譯，則執行 SDR 白色層級調整更為複雜;如果您要撰寫自己的圖元著色器，您應該考慮轉換成線性 gamma 以套用調整。</span><span class="sxs-lookup"><span data-stu-id="4acf5-275">If you're rendering using a nonlinear gamma color space such as HDR10, then performing SDR white level adjustment is more complex; if you're writing your own pixel shader you should consider converting into linear gamma to apply the adjustment.</span></span>

## <a name="adapt-hdr-content-to-the-displays-capabilities-using-tonemapping"></a><span data-ttu-id="4acf5-276">使用 tonemapping 將 HDR 內容調整為顯示器的功能</span><span class="sxs-lookup"><span data-stu-id="4acf5-276">Adapt HDR content to the display's capabilities using tonemapping</span></span>

<span data-ttu-id="4acf5-277">HDR 和 advanced 色彩的顯示方式在其功能方面會有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="4acf5-277">HDR and advanced color displays vary greatly in terms of their capabilities.</span></span> <span data-ttu-id="4acf5-278">例如，最小和最大的亮度，以及它們能夠重現的色彩範圍。</span><span class="sxs-lookup"><span data-stu-id="4acf5-278">For example, the minimum and maximum luminance and the color gamut they are capable of reproducing.</span></span> <span data-ttu-id="4acf5-279">在許多情況下，您的 HDR 內容將包含超過顯示功能的色彩。</span><span class="sxs-lookup"><span data-stu-id="4acf5-279">In many cases, your HDR content will contain colors that exceed the display's capabilities.</span></span> <span data-ttu-id="4acf5-280">為了獲得最佳的影像品質，您必須執行 HDR tonemapping，基本上是壓縮色彩範圍以符合顯示，同時最能保留內容的視覺意圖。</span><span class="sxs-lookup"><span data-stu-id="4acf5-280">For the best image quality it is important for you to perform HDR tonemapping, essentially compressing the range of colors to fit the display while best preserving the visual intent of the content.</span></span>

<span data-ttu-id="4acf5-281">要適應的最重要單一參數是最大的亮度，也稱為 MaxCLL (內容精簡級) ;更精密的 tonemappers 也會調整最小的亮度 (MinCLL) 和/或色彩主要複本。</span><span class="sxs-lookup"><span data-stu-id="4acf5-281">The most important single parameter to adapt for is max luminance, also known as MaxCLL (content light level); more sophisticated tonemappers will also adapt min luminance (MinCLL) and/or color primaries.</span></span>

### <a name="step-1-get-the-displays-color-volume-capabilities"></a><span data-ttu-id="4acf5-282">步驟 1：</span><span class="sxs-lookup"><span data-stu-id="4acf5-282">Step 1.</span></span> <span data-ttu-id="4acf5-283">取得顯示器的色彩音量功能</span><span class="sxs-lookup"><span data-stu-id="4acf5-283">Get the display's color volume capabilities</span></span>

#### <a name="universal-windows-platform-uwp-apps"></a><span data-ttu-id="4acf5-284">通用 Windows 平台 (UWP) 應用程式</span><span class="sxs-lookup"><span data-stu-id="4acf5-284">Universal Windows Platform (UWP) apps</span></span>

<span data-ttu-id="4acf5-285">使用 [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) 來取得顯示器的色彩音量。</span><span class="sxs-lookup"><span data-stu-id="4acf5-285">Use [**AdvancedColorInfo**](/uwp/api/windows.graphics.display.advancedcolorinfo) to get the display's color volume.</span></span>

#### <a name="win32-desktop-directx-apps"></a><span data-ttu-id="4acf5-286">Win32 (desktop) DirectX 應用程式</span><span class="sxs-lookup"><span data-stu-id="4acf5-286">Win32 (desktop) DirectX apps</span></span>

<span data-ttu-id="4acf5-287">使用 [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) 取得顯示器的色彩音量。</span><span class="sxs-lookup"><span data-stu-id="4acf5-287">Use [**DXGI_OUTPUT_DESC1**](/windows/desktop/api/DXGI1_6/ns-dxgi1_6-dxgi_output_desc1) to get the display's color volume.</span></span>

### <a name="step-2-get-the-contents-color-volume-information"></a><span data-ttu-id="4acf5-288">步驟 2：</span><span class="sxs-lookup"><span data-stu-id="4acf5-288">Step 2.</span></span> <span data-ttu-id="4acf5-289">取得內容的色彩量資訊</span><span class="sxs-lookup"><span data-stu-id="4acf5-289">Get the content's color volume information</span></span>

<span data-ttu-id="4acf5-290">根據您的 HDR 內容來源位置而定，有多種可能的方式可判斷其亮度和色域資訊。</span><span class="sxs-lookup"><span data-stu-id="4acf5-290">Depending on where your HDR content came from, there are multiple potential ways to determine its luminance and color gamut information.</span></span> <span data-ttu-id="4acf5-291">某些 HDR 影片和影像檔案包含2006中繼資料。</span><span class="sxs-lookup"><span data-stu-id="4acf5-291">Certain HDR video and image files contain SMPTE ST.2086 metadata.</span></span> <span data-ttu-id="4acf5-292">如果您的內容是以動態方式轉譯，則您可以從內部轉譯階段中解壓縮場景資訊，例如場景中最亮的光源。</span><span class="sxs-lookup"><span data-stu-id="4acf5-292">If your content was rendered dynamically, then you may be able to extract scene information from the internal rendering stages, for example the brightest light source in a scene.</span></span>

<span data-ttu-id="4acf5-293">更一般但計算成本昂貴的解決方案，是在轉譯的框架上執行長條圖或其他分析階段。</span><span class="sxs-lookup"><span data-stu-id="4acf5-293">A more general but computationally expensive solution is to run a histogram or other analysis pass on the rendered frame.</span></span> <span data-ttu-id="4acf5-294">[Direct2D advanced color IMAGES SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)示範如何使用 Direct2D 進行此作業;最相關的程式碼片段包含在下面：</span><span class="sxs-lookup"><span data-stu-id="4acf5-294">The [Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages) demonstrates how to do this using Direct2D; the most relevant code snippets are included below:</span></span>

```cpp
// Perform histogram pipeline setup; this should occur as part of image resource creation.
// Histogram results in no visual output but is used to calculate HDR metadata for the image.
void D2DAdvancedColorImagesRenderer::CreateHistogramResources()
{
    auto context = m_deviceResources->GetD2DDeviceContext();

    // We need to preprocess the image data before running the histogram.
    // 1. Spatial downscale to reduce the amount of processing needed.
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1Scale, &m_histogramPrescale)
        );

    DX::ThrowIfFailed(
        m_histogramPrescale->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(0.5f, 0.5f))
        );

    // The right place to compute HDR metadata is after color management to the
    // image's native colorspace but before any tonemapping or adjustments for the display.
    m_histogramPrescale->SetInputEffect(0, m_colorManagementEffect.Get());

    // 2. Convert scRGB data into luminance (nits).
    // 3. Normalize color values. Histogram operates on [0-1] numeric range,
    //    while FP16 can go up to 65504 (5+ million nits).
    // Both steps are performed in the same color matrix.
    ComPtr<ID2D1Effect> histogramMatrix;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1ColorMatrix, &histogramMatrix)
        );

    histogramMatrix->SetInputEffect(0, m_histogramPrescale.Get());

    float scale = sc_histMaxNits / sc_nominalRefWhite;

    D2D1_MATRIX_5X4_F rgbtoYnorm = D2D1::Matrix5x4F(
        0.2126f / scale, 0, 0, 0,
        0.7152f / scale, 0, 0, 0,
        0.0722f / scale, 0, 0, 0,
        0              , 0, 0, 1,
        0              , 0, 0, 0);
    // 1st column: [R] output, contains normalized Y (CIEXYZ).
    // 2nd column: [G] output, unused.
    // 3rd column: [B] output, unused.
    // 4th column: [A] output, alpha passthrough.
    // We explicitly calculate Y; this deviates from the CEA 861.3 definition of MaxCLL
    // which approximates luminance with max(R, G, B).

    DX::ThrowIfFailed(histogramMatrix->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, rgbtoYnorm));

    // 4. Apply a gamma to allocate more histogram bins to lower luminance levels.
    ComPtr<ID2D1Effect> histogramGamma;
    DX::ThrowIfFailed(
        context->CreateEffect(CLSID_D2D1GammaTransfer, &histogramGamma)
        );

    histogramGamma->SetInputEffect(0, histogramMatrix.Get());

    // Gamma function offers an acceptable tradeoff between simplicity and efficient bin allocation.
    // A more sophisticated pipeline would use a more perceptually linear function than gamma.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_RED_EXPONENT, sc_histGamma));
    // All other channels are passthrough.
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_GREEN_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_BLUE_DISABLE, TRUE));
    DX::ThrowIfFailed(histogramGamma->SetValue(D2D1_GAMMATRANSFER_PROP_ALPHA_DISABLE, TRUE));

    // 5. Finally, the histogram itself.
    HRESULT hr = context->CreateEffect(CLSID_D2D1Histogram, &m_histogramEffect);
    
    if (hr == D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES)
    {
        // The GPU doesn't support compute shaders and we can't run histogram on it.
        m_isComputeSupported = false;
    }
    else
    {
        DX::ThrowIfFailed(hr);
        m_isComputeSupported = true;

        DX::ThrowIfFailed(m_histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, sc_histNumBins));

        m_histogramEffect->SetInputEffect(0, histogramGamma.Get());
    }
}

// Uses a histogram to compute a modified version of MaxCLL (ST.2086 max content light level).
// Performs Begin/EndDraw on the D2D context.
void D2DAdvancedColorImagesRenderer::ComputeHdrMetadata()
{
    // Initialize with a sentinel value.
    m_maxCLL = -1.0f;

    // MaxCLL is not meaningful for SDR or WCG images.
    if ((!m_isComputeSupported) ||
        (m_imageInfo.imageKind != AdvancedColorKind::HighDynamicRange))
    {
        return;
    }

    // MaxCLL is nominally calculated for the single brightest pixel in a frame.
    // But we take a slightly more conservative definition that takes the 99.99th percentile
    // to account for extreme outliers in the image.
    float maxCLLPercent = 0.9999f;

    auto ctx = m_deviceResources->GetD2DDeviceContext();

    ctx->BeginDraw();

    ctx->DrawImage(m_histogramEffect.Get());

    // We ignore D2DERR_RECREATE_TARGET here. This error indicates that the device
    // is lost. It will be handled during the next call to Present.
    HRESULT hr = ctx->EndDraw();
    if (hr != D2DERR_RECREATE_TARGET)
    {
        DX::ThrowIfFailed(hr);
    }

    float *histogramData = new float[sc_histNumBins];
    DX::ThrowIfFailed(
        m_histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT,
            reinterpret_cast<BYTE*>(histogramData),
            sc_histNumBins * sizeof(float)
            )
        );

    unsigned int maxCLLbin = 0;
    float runningSum = 0.0f; // Cumulative sum of values in histogram is 1.0.
    for (int i = sc_histNumBins - 1; i >= 0; i--)
    {
        runningSum += histogramData[i];
        maxCLLbin = i;

        if (runningSum >= 1.0f - maxCLLPercent)
        {
            break;
        }
    }

    float binNorm = static_cast<float>(maxCLLbin) / static_cast<float>(sc_histNumBins);
    m_maxCLL = powf(binNorm, 1 / sc_histGamma) * sc_histMaxNits;

    // Some drivers have a bug where histogram will always return 0. Treat this as unknown.
    m_maxCLL = (m_maxCLL == 0.0f) ? -1.0f : m_maxCLL;
}
```

### <a name="step-3-perform-the-hdr-tonemapping-operation"></a><span data-ttu-id="4acf5-295">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="4acf5-295">Step 3.</span></span> <span data-ttu-id="4acf5-296">執行 HDR tonemapping 操作</span><span class="sxs-lookup"><span data-stu-id="4acf5-296">Perform the HDR tonemapping operation</span></span>

<span data-ttu-id="4acf5-297">Tonemapping 本身就是一個失真的程式，可針對許多感知或目標計量進行優化，因此沒有一個標準演算法。</span><span class="sxs-lookup"><span data-stu-id="4acf5-297">Tonemapping is inherently a lossy process, and can be optimized for a number of perceptual or objective metrics, so there is no one standard algorithm.</span></span> <span data-ttu-id="4acf5-298">Windows 在 Direct2D 和媒體基礎 HDR 影片播放管線中提供內建的 [HDR tonemapper 效果](../direct2d/hdr-tone-map-effect.md) 。</span><span class="sxs-lookup"><span data-stu-id="4acf5-298">Windows provides a built-in [HDR tonemapper effect](../direct2d/hdr-tone-map-effect.md) as part of Direct2D as well as in the Media Foundation HDR video playback pipeline.</span></span> <span data-ttu-id="4acf5-299">一些其他常用的演算法包括 ACE Filmic、Reinhard 和 ITU-R BT. 2390-3 EETF (電氣傳輸功能) 。</span><span class="sxs-lookup"><span data-stu-id="4acf5-299">Some other commonly used algorithms include ACES Filmic, Reinhard, and ITU-R BT.2390-3 EETF (electrical-electrical transfer function).</span></span>

<span data-ttu-id="4acf5-300">簡化的 Reinhard tonemapper 運算子如下所示。</span><span class="sxs-lookup"><span data-stu-id="4acf5-300">A simplified Reinhard tonemapper operator is shown below.</span></span>

```cpp
// Normally in DirectX, color values are manipulated in shaders on GPU textures.
// This example performs scaling on a CPU color value.
D2D1_VECTOR_4F simpleReinhardTonemapper(
    float inputMax, // Content's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    float outputMax, // Display's maximum luminance in scRGB values, e.g. 1.0 = 80 nits.
    D2D1_VECTOR_4F input // scRGB color.
)
{
    D2D1_VECTOR_4F output = input;

    // Vanilla Reinhard normalizes color values to [0, 1].
    // This modification scales to the luminance range of the display.
    output.r /= inputMax;
    output.g /= inputMax;
    output.b /= inputMax;

    output.r = (output.r / 1 + output.r);
    output.g = (output.g / 1 + output.g);
    output.b = (output.b / 1 + output.b);

    output.r *= outputMax;
    output.g *= outputMax;
    output.b *= outputMax;

    return output;
}
```

## <a name="capturing-hdr-and-wcg-content"></a><span data-ttu-id="4acf5-301">捕獲 HDR 和 WCG 內容</span><span class="sxs-lookup"><span data-stu-id="4acf5-301">Capturing HDR and WCG content</span></span>

<span data-ttu-id="4acf5-302">支援指定圖元 [**格式的 api**](/uwp/api/windows.graphics.capture) （例如， [**IDXGIOutput5：：:D uplicateoutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) 方法）可提供在不遺失圖元資訊的情況下，捕獲 HDR 和 WCG 內容的功能。</span><span class="sxs-lookup"><span data-stu-id="4acf5-302">APIs that support specifying pixel formats, such as those in the [**Windows.Graphics.Capture**](/uwp/api/windows.graphics.capture) namespace, and the [**IDXGIOutput5::DuplicateOutput1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1) method, provide the capability to capture HDR and WCG content without losing pixel information.</span></span> <span data-ttu-id="4acf5-303">請注意，在取得內容畫面格之後，需要進行額外的處理。</span><span class="sxs-lookup"><span data-stu-id="4acf5-303">Note that after acquiring content frames, additional processing is required.</span></span> <span data-ttu-id="4acf5-304">例如，HDR 與 SDR 的音調對應 (例如，SDR 螢幕擷取畫面會複製網際網路共用) ，並以適當的格式儲存內容 (例如，JPEG XR) 。</span><span class="sxs-lookup"><span data-stu-id="4acf5-304">For example, HDR-to-SDR tone mapping (for example, SDR screenshot copy for Internet sharing) and content saving with proper format (for example, JPEG XR).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4acf5-305">其他資源</span><span class="sxs-lookup"><span data-stu-id="4acf5-305">Additional resources</span></span>

* <span data-ttu-id="4acf5-306">搭配 directx [11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering)directx 12 *的 directx 工具套件使用 HDR* 轉譯  /  [](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering)。</span><span class="sxs-lookup"><span data-stu-id="4acf5-306">*Using HDR Rendering with the DirectX Tool Kit* for [DirectX 11](https://github.com/Microsoft/DirectXTK/wiki/Using-HDR-rendering) / [DirectX 12](https://github.com/microsoft/DirectXTK12/wiki/Using-HDR-rendering).</span></span> <span data-ttu-id="4acf5-307">逐步解說如何使用 DirectX 工具套件 (DirectXTK) ，將 HDR 支援新增至 DirectX 應用程式。</span><span class="sxs-lookup"><span data-stu-id="4acf5-307">Walkthrough of how to add HDR support to a DirectX app using the DirectX Tool Kit (DirectXTK).</span></span>
* <span data-ttu-id="4acf5-308">[Direct2D advanced color IMAGES SDK 範例](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)。</span><span class="sxs-lookup"><span data-stu-id="4acf5-308">[Direct2D advanced color images SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages).</span></span> <span data-ttu-id="4acf5-309">UWP SDK 範例會使用 Direct2D 來執行 advanced color 感知 HDR 和 WCG 影像檢視器。</span><span class="sxs-lookup"><span data-stu-id="4acf5-309">UWP SDK sample implementing an advanced color-aware HDR and WCG image viewer using Direct2D.</span></span> <span data-ttu-id="4acf5-310">示範 UWP 應用程式的各種最佳做法，包括回應顯示功能變更，以及對 SDR 白色層級進行調整。</span><span class="sxs-lookup"><span data-stu-id="4acf5-310">Demonstrates the full range of best practices for UWP apps, including responding to display capability changes and adjusting for SDR white level.</span></span>
* <span data-ttu-id="4acf5-311">[Direct3D 12 HDR desktop 範例](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR)。</span><span class="sxs-lookup"><span data-stu-id="4acf5-311">[Direct3D 12 HDR desktop sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/Desktop/D3D12HDR).</span></span> <span data-ttu-id="4acf5-312">執行基本 Direct3D 12 HDR 場景的桌面 SDK 範例。</span><span class="sxs-lookup"><span data-stu-id="4acf5-312">Desktop SDK sample implementing a basic Direct3D 12 HDR scene.</span></span>
* <span data-ttu-id="4acf5-313">[Direct3D 12 HDR UWP 範例](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR)。</span><span class="sxs-lookup"><span data-stu-id="4acf5-313">[Direct3D 12 HDR UWP sample](https://github.com/microsoft/DirectX-Graphics-Samples/tree/master/Samples/UWP/D3D12HDR).</span></span> <span data-ttu-id="4acf5-314">與上述範例相同的 UWP。</span><span class="sxs-lookup"><span data-stu-id="4acf5-314">UWP equivalent of the above sample.</span></span>
* <span data-ttu-id="4acf5-315">[XBOX ATG SIMPLEHDR PC 範例](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC)。</span><span class="sxs-lookup"><span data-stu-id="4acf5-315">[Xbox ATG SimpleHDR PC sample](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/PCSamples/Graphics/SimpleHDR_PC).</span></span> <span data-ttu-id="4acf5-316">執行基本 Direct3D 11 HDR 場景的桌面 SDK 範例。</span><span class="sxs-lookup"><span data-stu-id="4acf5-316">Desktop SDK sample implementing a basic Direct3D 11 HDR scene.</span></span>
