---
description: 選擇正確的影片轉譯器
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: 選擇正確的影片轉譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972753"
---
# <a name="choosing-the-right-video-renderer"></a><span data-ttu-id="8b1e2-103">選擇正確的影片轉譯器</span><span class="sxs-lookup"><span data-stu-id="8b1e2-103">Choosing the Right Video Renderer</span></span>

<span data-ttu-id="8b1e2-104">DirectShow 提供數個影片轉譯器篩選，在下表中摘要說明。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-104">DirectShow provides several video renderer filters, summarized in the following table.</span></span>



| <span data-ttu-id="8b1e2-105">篩選</span><span class="sxs-lookup"><span data-stu-id="8b1e2-105">Filter</span></span>                                                                  | <span data-ttu-id="8b1e2-106">備註</span><span class="sxs-lookup"><span data-stu-id="8b1e2-106">Remarks</span></span>                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="8b1e2-107">[**增強的影片**](enhanced-video-renderer-filter.md) 轉譯器 (EVR) </span><span class="sxs-lookup"><span data-stu-id="8b1e2-107">[**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR)</span></span> | <span data-ttu-id="8b1e2-108">使用 Direct3D 9。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-108">Uses Direct3D 9.</span></span> <span data-ttu-id="8b1e2-109">需要 Windows Vista 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-109">Requires Windows Vista or later.</span></span> |
| <span data-ttu-id="8b1e2-110">[影片混合](video-mixing-renderer-filter-9.md) 轉譯器 9 (VMR-9) </span><span class="sxs-lookup"><span data-stu-id="8b1e2-110">[Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>   | <span data-ttu-id="8b1e2-111">使用 Direct3D 9。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-111">Uses Direct3D 9.</span></span> <span data-ttu-id="8b1e2-112">需要 Windows XP 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-112">Requires Windows XP or later.</span></span>    |
| <span data-ttu-id="8b1e2-113">[影片混合篩選器 7](video-mixing-renderer-filter-7.md) (VMR-7) </span><span class="sxs-lookup"><span data-stu-id="8b1e2-113">[Video Mixing Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>     | <span data-ttu-id="8b1e2-114">使用 DirectDraw。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-114">Uses DirectDraw.</span></span> <span data-ttu-id="8b1e2-115">需要 Windows XP 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-115">Requires Windows XP or later.</span></span>    |
| [<span data-ttu-id="8b1e2-116">覆蓋混音器</span><span class="sxs-lookup"><span data-stu-id="8b1e2-116">Overlay Mixer</span></span>](using-the-overlay-mixer-in-video-capture.md)           | <span data-ttu-id="8b1e2-117">透過 DirectDraw 支援硬體覆蓋。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-117">Supports hardware overlays through DirectDraw.</span></span>    |
| <span data-ttu-id="8b1e2-118">舊版 [影片](video-renderer-filter.md) 轉譯器篩選。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-118">Legacy [Video Renderer](video-renderer-filter.md) filter.</span></span>              | <span data-ttu-id="8b1e2-119">使用 DirectDraw 或 (很少) GDI</span><span class="sxs-lookup"><span data-stu-id="8b1e2-119">Uses DirectDraw or (rarely) GDI</span></span>                   |



 

<span data-ttu-id="8b1e2-120">要使用哪一個轉譯器主要取決於您需要支援的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-120">Which renderer to use depends largely on which versions of Windows you need to support.</span></span>

-   <span data-ttu-id="8b1e2-121">在 Windows Vista 和更新版本中，如果硬體支援，應用程式應該使用 EVR。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-121">In Windows Vista and later, applications should use the EVR if the hardware supports it.</span></span> <span data-ttu-id="8b1e2-122">否則，會切換回 VMR 9 或 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-122">Otherwise, fall back to the VMR-9 or VMR-7.</span></span> <span data-ttu-id="8b1e2-123">EVR 提供比先前轉譯器更佳的效能和更佳的影片品質。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-123">The EVR offers better performance and better video quality than previous renderers.</span></span> <span data-ttu-id="8b1e2-124">此外，它是設計來搭配桌面視窗管理員 (DWM) 。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-124">Also, it is designed to work with the Desktop Window Manager (DWM).</span></span>
-   <span data-ttu-id="8b1e2-125">在 Windows Vista 之前，如果硬體支援，則使用 VMR-9，且不需要影片埠功能。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-125">Prior to Windows Vista, use the VMR-9 if the hardware supports it and video port functionality is not required.</span></span> <span data-ttu-id="8b1e2-126">否則，請使用 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-126">Otherwise, use the VMR-7.</span></span>
-   <span data-ttu-id="8b1e2-127">在較舊的系統上，您可能需要使用重迭混音器 (的影片埠或硬體重迭支援) 或舊版的影片轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-127">On older systems, you might need to use the Overlay Mixer (for video port or hardware overlay support) or the legacy Video Renderer filter.</span></span>

<span data-ttu-id="8b1e2-128">[**IGraphBuilder：： Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)和 [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)方法預設會使用 VMR-7。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-128">The [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) and [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) methods use the VMR-7 by default.</span></span> <span data-ttu-id="8b1e2-129">如果硬體不支援 VMR-7，則這些方法會切換回舊版的影片轉譯器篩選器。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-129">If the hardware does not support the VMR-7, these methods fall back to the legacy Video Renderer filter.</span></span> <span data-ttu-id="8b1e2-130">EVR 和 VMR 不是預設轉譯器。</span><span class="sxs-lookup"><span data-stu-id="8b1e2-130">The EVR and VMR-9 are never the default renderers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b1e2-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b1e2-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b1e2-132">影片轉譯</span><span class="sxs-lookup"><span data-stu-id="8b1e2-132">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



