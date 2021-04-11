---
description: 關於 DirectShow 中的影片轉譯
ms.assetid: 3b064758-2ae5-4441-801c-5400e4ef3790
title: 關於 DirectShow 中的影片轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699e8ecf133f362e699e6b9d650d11da5bf43347
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846747"
---
# <a name="about-video-rendering-in-directshow"></a><span data-ttu-id="79b0d-103">關於 DirectShow 中的影片轉譯</span><span class="sxs-lookup"><span data-stu-id="79b0d-103">About Video Rendering in DirectShow</span></span>

<span data-ttu-id="79b0d-104">DirectShow 提供數個轉譯影片的篩選：</span><span class="sxs-lookup"><span data-stu-id="79b0d-104">DirectShow provides several filters that render video:</span></span>

-   <span data-ttu-id="79b0d-105">[影片](video-renderer-filter.md) 轉譯器篩選。</span><span class="sxs-lookup"><span data-stu-id="79b0d-105">[Video Renderer](video-renderer-filter.md) filter.</span></span> <span data-ttu-id="79b0d-106">此篩選器適用于所有支援 DirectX 的平臺，而且沒有特定的系統需求。</span><span class="sxs-lookup"><span data-stu-id="79b0d-106">This filter is available for all platforms that support DirectX, and has no particular system requirements.</span></span> <span data-ttu-id="79b0d-107">影片轉譯器會盡可能使用 DirectDraw 來呈現影片;否則，它會使用 GDI。</span><span class="sxs-lookup"><span data-stu-id="79b0d-107">The Video Renderer uses DirectDraw whenever possible to render the video; otherwise, it uses GDI.</span></span> <span data-ttu-id="79b0d-108">此篩選器是 Windows XP 之前平臺上的預設影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="79b0d-108">This filter is the default video renderer on platforms earlier than Windows XP.</span></span>
-   <span data-ttu-id="79b0d-109">[影片混合轉譯器篩選器 7](video-mixing-renderer-filter-7.md) (VMR-7) 。</span><span class="sxs-lookup"><span data-stu-id="79b0d-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7).</span></span> <span data-ttu-id="79b0d-110">VMR-7 可在 Windows XP 上取得，其為預設的影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="79b0d-110">The VMR-7 is available on Windows XP, where it is the default video renderer.</span></span> <span data-ttu-id="79b0d-111">VMR-7 一律會使用 DirectDraw 7 來呈現。</span><span class="sxs-lookup"><span data-stu-id="79b0d-111">The VMR-7 always uses DirectDraw 7 for rendering.</span></span> <span data-ttu-id="79b0d-112">它提供了許多較舊的影片轉譯器篩選器中未提供的強大功能，包括外掛程式模型，其中應用程式會控制用來轉譯的 DirectDraw 表面。</span><span class="sxs-lookup"><span data-stu-id="79b0d-112">It provides many powerful features not available in the older Video Renderer filter, including a plug-in model where the application controls the DirectDraw surfaces used for rendering.</span></span>
-   <span data-ttu-id="79b0d-113">[影片混合轉譯器篩選器 9](video-mixing-renderer-filter-9.md) (VMR-9) 。</span><span class="sxs-lookup"><span data-stu-id="79b0d-113">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9).</span></span> <span data-ttu-id="79b0d-114">VMR-9 是較新版本的視頻混合轉譯器，它會使用 Direct3D 9 來呈現。</span><span class="sxs-lookup"><span data-stu-id="79b0d-114">The VMR-9 is a newer version of the Video Mixing Renderer that uses Direct3D 9 for rendering.</span></span> <span data-ttu-id="79b0d-115">它適用于所有支援 DirectX 的平臺。</span><span class="sxs-lookup"><span data-stu-id="79b0d-115">It is available for all platforms that support DirectX.</span></span> <span data-ttu-id="79b0d-116">不過，它並不是預設轉譯器，因為它的系統需求比影片轉譯器篩選器更高。</span><span class="sxs-lookup"><span data-stu-id="79b0d-116">It is not the default renderer, however, because it has higher system requirements than the Video Renderer filter.</span></span>
-   <span data-ttu-id="79b0d-117">覆迭 [混音](overlay-mixer-filter.md) 器篩選器是專門針對 DVD 播放和廣播影片所設計。</span><span class="sxs-lookup"><span data-stu-id="79b0d-117">The [Overlay Mixer](overlay-mixer-filter.md) filter is designed specifically for DVD playback and broadcast video.</span></span> <span data-ttu-id="79b0d-118">它也支援 (VPEs) 的影片埠擴充功能，讓它能夠使用硬體 MPEG-2 解碼器或類比電視調諧器，直接將影片傳送至圖形配接器。</span><span class="sxs-lookup"><span data-stu-id="79b0d-118">It also supports Video Port Extensions (VPEs), enabling it to work with hardware MPEG-2 decoders or analog TV tuners that send video directly to the graphics card.</span></span>
-   <span data-ttu-id="79b0d-119">從 Windows Vista 開始，可以使用 (EVR) 篩選器的 [**增強型影片**](enhanced-video-renderer-filter.md) 轉譯器。</span><span class="sxs-lookup"><span data-stu-id="79b0d-119">The [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter is available starting in Windows Vista.</span></span> <span data-ttu-id="79b0d-120">相較于先前的影片轉譯器，它提供改良的影片效能，特別是在啟用 Windows Vista 桌面電腦群組合的情況下。</span><span class="sxs-lookup"><span data-stu-id="79b0d-120">It offers improved video performance compared with earlier video renderers, especially when Windows Vista desktop composition is enabled.</span></span>

<span data-ttu-id="79b0d-121">一般來說，對於以 Windows Vista 或更新版本為目標的應用程式而言，EVR 是慣用的，而在舊版 Windows 上執行的應用程式則偏好 VMR-9。</span><span class="sxs-lookup"><span data-stu-id="79b0d-121">Generally, the EVR is preferred for applications that target Windows Vista or later, and the VMR-9 is preferred for applications running on earlier versions of Windows.</span></span> <span data-ttu-id="79b0d-122">如需使用 VMR-7 和 VMR-9 篩選器的詳細資訊，請參閱 [使用影片混合](using-the-video-mixing-renderer.md)轉譯器。</span><span class="sxs-lookup"><span data-stu-id="79b0d-122">For more information about using the VMR-7 and VMR-9 filters, see [Using the Video Mixing Renderer](using-the-video-mixing-renderer.md).</span></span>

<span data-ttu-id="79b0d-123">視窗模式和無視窗模式</span><span class="sxs-lookup"><span data-stu-id="79b0d-123">Windowed Mode and Windowless Mode</span></span>

<span data-ttu-id="79b0d-124">DirectShow 影片轉譯器可以在 *視窗* 模式或 *無視窗* 模式下運作。</span><span class="sxs-lookup"><span data-stu-id="79b0d-124">A DirectShow video renderer can operate in either *windowed* mode or *windowless* mode.</span></span>

-   <span data-ttu-id="79b0d-125">在視窗模式中，轉譯器會建立自己的視窗來顯示影片。</span><span class="sxs-lookup"><span data-stu-id="79b0d-125">In windowed mode, the renderer creates its own window to display the video.</span></span> <span data-ttu-id="79b0d-126">通常您會將此視窗設為應用程式視窗的子系。</span><span class="sxs-lookup"><span data-stu-id="79b0d-126">Typically you will make this window the child of an application window.</span></span> <span data-ttu-id="79b0d-127">如需詳細資訊，請參閱 [使用視窗模式](using-windowed-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="79b0d-127">For more information, see [Using Windowed Mode](using-windowed-mode.md).</span></span>
-   <span data-ttu-id="79b0d-128">在無視窗模式中，轉譯器會將影片直接繪製到應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="79b0d-128">In windowless mode, the renderer draws the video directly onto an application window.</span></span> <span data-ttu-id="79b0d-129">它不會建立自己的視窗。</span><span class="sxs-lookup"><span data-stu-id="79b0d-129">It does not create its own window.</span></span> <span data-ttu-id="79b0d-130">如需此模式的詳細資訊，請參閱 [使用無視窗模式](using-windowless-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="79b0d-130">For more information about this mode, see [Using Windowless Mode](using-windowless-mode.md).</span></span>

<span data-ttu-id="79b0d-131">影片轉譯器篩選僅支援視窗模式。</span><span class="sxs-lookup"><span data-stu-id="79b0d-131">The Video Renderer filter supports windowed mode only.</span></span> <span data-ttu-id="79b0d-132">VMR-7 和 VMR-9 篩選器都支援這兩種模式。</span><span class="sxs-lookup"><span data-stu-id="79b0d-132">The VMR-7 and VMR-9 filters support both modes.</span></span> <span data-ttu-id="79b0d-133">它們預設為視窗模式，以提供回溯相容性，但最好是無視窗模式。</span><span class="sxs-lookup"><span data-stu-id="79b0d-133">They default to windowed mode for backward compatibility, but windowless mode is preferred.</span></span> <span data-ttu-id="79b0d-134">EVR 只支援無視窗模式。</span><span class="sxs-lookup"><span data-stu-id="79b0d-134">The EVR supports windowless mode only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="79b0d-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="79b0d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79b0d-136">影片轉譯</span><span class="sxs-lookup"><span data-stu-id="79b0d-136">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



