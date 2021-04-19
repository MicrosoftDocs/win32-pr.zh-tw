---
description: 使用影片混合轉譯器
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: 使用影片混合轉譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983718"
---
# <a name="using-the-video-mixing-renderer"></a><span data-ttu-id="f6118-103">使用影片混合轉譯器</span><span class="sxs-lookup"><span data-stu-id="f6118-103">Using the Video Mixing Renderer</span></span>

<span data-ttu-id="f6118-104">就效能和廣泛的功能而言， (VMR) 濾波器的影片混合轉譯器代表 Windows 平臺上的下一代影片轉譯。</span><span class="sxs-lookup"><span data-stu-id="f6118-104">In terms of both performance and breadth of features, the Video Mixing Renderer (VMR) filter represents the next generation in video rendering on the Windows platform.</span></span> <span data-ttu-id="f6118-105">VMR 會取代重迭 [混音](overlay-mixer-filter.md) 器和 [影片](video-renderer-filter.md)轉譯器，並新增許多新的混合功能。</span><span class="sxs-lookup"><span data-stu-id="f6118-105">The VMR replaces the [Overlay Mixer](overlay-mixer-filter.md) and [Video Renderer](video-renderer-filter.md), and adds many new mixing features.</span></span>

<span data-ttu-id="f6118-106">VMR 有兩個版本：</span><span class="sxs-lookup"><span data-stu-id="f6118-106">There are two versions of the VMR:</span></span>

-   <span data-ttu-id="f6118-107">VMR-7，使用 DirectDraw 7 進行轉譯。</span><span class="sxs-lookup"><span data-stu-id="f6118-107">The VMR-7, which uses DirectDraw 7 for rendering.</span></span>
-   <span data-ttu-id="f6118-108">使用 Direct3D 9 的 VMR-9。</span><span class="sxs-lookup"><span data-stu-id="f6118-108">The VMR-9, which uses Direct3D 9.</span></span>

<span data-ttu-id="f6118-109">VMR-7 可在 Windows XP 和更新版本上使用，但無法再轉散發。</span><span class="sxs-lookup"><span data-stu-id="f6118-109">The VMR-7 is available on Windows XP and later, but is not available for redistribution.</span></span> <span data-ttu-id="f6118-110">VMR-9 可在 DirectX 9 支援的所有平臺上轉散發。</span><span class="sxs-lookup"><span data-stu-id="f6118-110">The VMR-9 is available for redistribution on all platforms supported by DirectX 9.</span></span> <span data-ttu-id="f6118-111">這兩個 VMR 篩選在其執行和其公開的介面中非常類似。</span><span class="sxs-lookup"><span data-stu-id="f6118-111">The two VMR filters are very similar in their implementation and the interfaces that they expose.</span></span>

<span data-ttu-id="f6118-112">VMR-9 有自己的 CLSID 以及本身的一組介面、結構和列舉型別，這些型別與 VMR-7 的對應資料類型不一定相同，原因是 DirectDraw 7 和 Direct3D 9 之間的根本差異。</span><span class="sxs-lookup"><span data-stu-id="f6118-112">The VMR-9 has its own CLSID and its own set of interfaces, structures and enumeration types which are not always identical to the corresponding data types for the VMR-7, due to the underlying differences between DirectDraw 7 and Direct3D 9.</span></span> <span data-ttu-id="f6118-113">VMR-9 介面的結尾都是 "9"，例如 **IVMRStreamConfig9**，而結構和列舉型別在其名稱中都有 "VMR9"，以區別于與 VMR-7 搭配使用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="f6118-113">The VMR-9 interfaces all end with "9", for example **IVMRStreamConfig9**, and the structures and enumeration types all have "VMR9" in their name to distinguish them from the data types used with the VMR-7.</span></span>

<span data-ttu-id="f6118-114">若要確保回溯相容性，VMR-9 不是任何系統上的預設轉譯器。</span><span class="sxs-lookup"><span data-stu-id="f6118-114">To ensure backward-compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="f6118-115">若要使用 VMR-9，您必須使用 [**IFilterGraph：： AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) 方法，明確地將它新增至篩選圖形，並在連接到任何上游篩選器之前進行設定。</span><span class="sxs-lookup"><span data-stu-id="f6118-115">To use the VMR-9, you must explicitly add it to the filter graph using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method, and configure it before connecting it to any upstream filters.</span></span>

<span data-ttu-id="f6118-116">本文包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="f6118-116">This article contains the following sections.</span></span> <span data-ttu-id="f6118-117">除非有注明，否則這些章節中的資訊適用于 VMR-7 和 VMR 9 的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="f6118-117">Except where noted, the information in these sections applies to both the VMR-7 and the VMR-9 filters.</span></span>

-   [<span data-ttu-id="f6118-118">關於影片混合轉譯</span><span class="sxs-lookup"><span data-stu-id="f6118-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
-   [<span data-ttu-id="f6118-119">作業的 VMR 模式</span><span class="sxs-lookup"><span data-stu-id="f6118-119">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
-   [<span data-ttu-id="f6118-120">建立 VMR 9 篩選圖形</span><span class="sxs-lookup"><span data-stu-id="f6118-120">Building a VMR-9 Filter Graph</span></span>](building-a-vmr-9-filter-graph.md)
-   [<span data-ttu-id="f6118-121">使用 VMR 混合模式</span><span class="sxs-lookup"><span data-stu-id="f6118-121">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
-   [<span data-ttu-id="f6118-122">設定交錯喜好設定</span><span class="sxs-lookup"><span data-stu-id="f6118-122">Setting Deinterlace Preferences</span></span>](setting-deinterlace-preferences.md)
-   [<span data-ttu-id="f6118-123">使用 VMR 來進行 DirectShow 篩選器開發人員</span><span class="sxs-lookup"><span data-stu-id="f6118-123">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
-   [<span data-ttu-id="f6118-124">使用認證輸出保護通訊協定 (COPP) </span><span class="sxs-lookup"><span data-stu-id="f6118-124">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a><span data-ttu-id="f6118-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="f6118-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6118-126">影片混合轉譯器篩選器7</span><span class="sxs-lookup"><span data-stu-id="f6118-126">Video Mixing Renderer Filter 7</span></span>](video-mixing-renderer-filter-7.md)
</dt> <dt>

[<span data-ttu-id="f6118-127">影片混合轉譯器篩選器9</span><span class="sxs-lookup"><span data-stu-id="f6118-127">Video Mixing Renderer Filter 9</span></span>](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



