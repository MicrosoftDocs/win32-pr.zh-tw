---
description: VMR 與
ms.assetid: 45b3f964-6ec7-48b8-a66e-3c9883e6d780
title: VMR 與先前的 DirectShow 轉譯器比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db40f9789a73446cb2dac4ed7033bdb163141bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974111"
---
# <a name="vmr-vs-previous-directshow-renderers"></a><span data-ttu-id="88a44-103">VMR 與先前的 DirectShow 轉譯器比較</span><span class="sxs-lookup"><span data-stu-id="88a44-103">VMR vs. Previous DirectShow Renderers</span></span>

<span data-ttu-id="88a44-104">使用舊的篩選器時，圖形中會需要不同的轉譯器，視硬體設定而定。</span><span class="sxs-lookup"><span data-stu-id="88a44-104">With the old filters, different renderers would be required in the graph depending on the hardware configuration.</span></span>

<span data-ttu-id="88a44-105">[影片](video-renderer-filter.md)轉譯器篩選器用來轉譯非影片埠案例中的單一影片串流。</span><span class="sxs-lookup"><span data-stu-id="88a44-105">The [Video Renderer](video-renderer-filter.md) filter was used to render a single video stream in non-video port scenarios.</span></span> <span data-ttu-id="88a44-106">它是以圖形硬體技術為基礎，這項技術目前已超過五年，而在較舊版本的 DirectDraw 上。</span><span class="sxs-lookup"><span data-stu-id="88a44-106">It was based on graphics hardware technology which is now over five years old, and on an older version of DirectDraw.</span></span> <span data-ttu-id="88a44-107">在某些情況下，它會使用 GDI 來呈現。</span><span class="sxs-lookup"><span data-stu-id="88a44-107">In certain scenarios, it uses GDI for rendering.</span></span> <span data-ttu-id="88a44-108">這樣做的目的是為了節省影片資源，這些資源在五年前都有更多限制，或在 DirectDraw 中克服與多重監視器支援相關的限制。</span><span class="sxs-lookup"><span data-stu-id="88a44-108">This is done either to conserve video resources, which were much more limited five years ago, or else to overcome limitations in DirectDraw that were related to multi-monitor support.</span></span> <span data-ttu-id="88a44-109">VMR-7 或 VMR-9 都不會使用 GDI 來呈現;VMR-7 完全以 DirectDraw 7 為基礎，而 VMR-9 是以 Direct3D 9 為基礎。</span><span class="sxs-lookup"><span data-stu-id="88a44-109">Neither the VMR-7 nor the VMR-9 ever uses GDI for rendering; the VMR-7 is based completely on DirectDraw 7 and the VMR-9 is based on Direct3D 9.</span></span>

<span data-ttu-id="88a44-110">在涉及影片埠或多個影片輸入串流的案例中，在 VMR 之前，會使用重迭 [混音](overlay-mixer-filter.md) 器篩選器進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="88a44-110">In scenarios involving either a video port or multiple video input streams, prior to the VMR the [Overlay Mixer](overlay-mixer-filter.md) filter was used for rendering.</span></span> <span data-ttu-id="88a44-111">此篩選器只會使用圖形配接器上的硬體重迭，因此通常會限制為大部分卡片所提供的一個重迭表面。</span><span class="sxs-lookup"><span data-stu-id="88a44-111">This filter only uses the hardware overlay on the graphics card, and so is generally limited to the one overlay surface provided by most cards.</span></span> <span data-ttu-id="88a44-112">覆迭混音器會執行目的地色彩的金鑰，但無法進行 Alpha 混色。</span><span class="sxs-lookup"><span data-stu-id="88a44-112">The Overlay Mixer performs destination color keying, but it is not capable of alpha blending.</span></span> <span data-ttu-id="88a44-113">因為它沒有視窗管理員，所以它必須使用第二個篩選器，也就是影片轉譯器，用於視窗管理。</span><span class="sxs-lookup"><span data-stu-id="88a44-113">Because it does not have a window manager, it must use a second filter, the Video Renderer, for window management.</span></span> <span data-ttu-id="88a44-114">VMR 具有真正的 Alpha 混色，而且除了硬體重迭之外，還可以在軟體中建立多個重迭。</span><span class="sxs-lookup"><span data-stu-id="88a44-114">The VMR is capable of true alpha blending, and can create multiple overlays in software in addition to the hardware overlays.</span></span>

<span data-ttu-id="88a44-115">在影片埠案例中，應用程式會在影片上覆迭隱藏式輔助字幕或其他 VBI 資料，需要額外的篩選器（ [VBI Surface](vbi-surface-allocator.md)配置器），才能為 VBI 文字配置額外的視訊記憶體。</span><span class="sxs-lookup"><span data-stu-id="88a44-115">In video port scenarios where applications were overlaying closed captioning or other VBI data on the video, an additional filter, the [VBI Surface Allocator](vbi-surface-allocator.md), was required in order to allocate the additional video memory for the VBI text.</span></span> <span data-ttu-id="88a44-116">針對 Isv，VMR 7 會將配置和轉譯功能合併成用於所有案例的單一篩選，以簡化應用程式開發。</span><span class="sxs-lookup"><span data-stu-id="88a44-116">For ISVs, the VMR-7 simplifies application development by combining allocation and rendering functionality into a single filter that is used in all scenarios.</span></span> <span data-ttu-id="88a44-117">有了 VMR，就不再需要 VBI Surface 配置器。</span><span class="sxs-lookup"><span data-stu-id="88a44-117">With the VMR, the VBI Surface Allocator is no longer needed.</span></span> <span data-ttu-id="88a44-118">此篩選器會由新的 [影片埠管理員](video-port-manager.md) 篩選在 Windows XP 中取代，此篩選器會執行所有先前由重迭混音器執行的影片埠工作。</span><span class="sxs-lookup"><span data-stu-id="88a44-118">This filter is replaced in Windows XP by the new [Video Port Manager](video-port-manager.md) filter which performs all of the video port tasks previously performed by the Overlay Mixer.</span></span>

> [!Note]  
> <span data-ttu-id="88a44-119">VMR-9 不支援視訊連接埠。</span><span class="sxs-lookup"><span data-stu-id="88a44-119">The VMR-9 does not support video ports.</span></span>

 

<span data-ttu-id="88a44-120">VMR 比舊版轉譯器更健全，部分是因為如果您使用的是 VMR-9) 介面，則只會使用 DirectDraw 7 (或 Direct3D 9，而不是舊的轉譯器，其使用舊版和新版 DirectDraw 的混合介面。</span><span class="sxs-lookup"><span data-stu-id="88a44-120">The VMR is more robust than the earlier renderers, in part because it only uses DirectDraw 7 (or Direct3D 9 if you are using the VMR-9) interfaces, as opposed to the old renderers which used a mixture of interfaces from older and newer versions of DirectDraw.</span></span> <span data-ttu-id="88a44-121">VMR 也採用新的映射呈現機制，其設計目的是要支援 Direct3D、更高的 VRAM 和影片記憶體頻寬，以及硬體加速功能。</span><span class="sxs-lookup"><span data-stu-id="88a44-121">The VMR also employs a new image presentation mechanism which is designed for current and future generations of adapters, which have support for Direct3D, increased VRAM and video memory bandwidth, and hardware acceleration features.</span></span> <span data-ttu-id="88a44-122">有了 VMR，重點在於處理前端，並減少對影片埠和覆迭的相依性。</span><span class="sxs-lookup"><span data-stu-id="88a44-122">With the VMR, the focus is on front-end processing, and reduced dependence on video ports and overlays.</span></span> <span data-ttu-id="88a44-123">但即使是所有的新功能，VMR 的設計是為了與現有應用程式的最大相容性。</span><span class="sxs-lookup"><span data-stu-id="88a44-123">But even with all its new functionality, the VMR is designed for maximum compatibility with existing applications.</span></span>

<span data-ttu-id="88a44-124">VMR 也是可擴充的。</span><span class="sxs-lookup"><span data-stu-id="88a44-124">The VMR is also extensible.</span></span> <span data-ttu-id="88a44-125">應用程式可以提供自己的子元件來執行自訂的影片效果，以及/或掌控配置和轉譯流程。</span><span class="sxs-lookup"><span data-stu-id="88a44-125">Applications can provide their own sub-components to perform custom video effects and/or take control of the allocation and rendering process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88a44-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="88a44-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88a44-127">關於影片混合轉譯</span><span class="sxs-lookup"><span data-stu-id="88a44-127">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



