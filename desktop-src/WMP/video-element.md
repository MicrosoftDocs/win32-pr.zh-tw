---
title: 影片元素
description: 影片元素
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Windows Media Player 的外觀、影片元素
- 外觀、影片元素
- 影片元素
- 外觀的參考、影片元素
- 元素、影片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673603"
---
# <a name="video-element"></a><span data-ttu-id="035f9-108">影片元素</span><span class="sxs-lookup"><span data-stu-id="035f9-108">VIDEO Element</span></span>

<span data-ttu-id="035f9-109">**影片** 元素提供一種方式，可讓您使用下列屬性和事件，在面板中操作影片視窗。</span><span class="sxs-lookup"><span data-stu-id="035f9-109">The **VIDEO** element provides a way to manipulate a video window in a skin, using the following attributes and events.</span></span> <span data-ttu-id="035f9-110">為了方便起見，也提供預先定義的 **影片** 元素。</span><span class="sxs-lookup"><span data-stu-id="035f9-110">A predefined **VIDEO** element is also provided for convenience.</span></span>

<span data-ttu-id="035f9-111">**VIDEO** 元素支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="035f9-111">The **VIDEO** element supports the following attributes.</span></span>



| <span data-ttu-id="035f9-112">屬性</span><span class="sxs-lookup"><span data-stu-id="035f9-112">Attribute</span></span>                                            | <span data-ttu-id="035f9-113">描述</span><span class="sxs-lookup"><span data-stu-id="035f9-113">Description</span></span>                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="035f9-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="035f9-114">backgroundColor</span></span>](video-backgroundcolor.md)         | <span data-ttu-id="035f9-115">指定或抓取影片控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="035f9-115">Specifies or retrieves the background color of the Video control.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="035f9-116">cursor</span><span class="sxs-lookup"><span data-stu-id="035f9-116">cursor</span></span>](video-cursor.md)                           | <span data-ttu-id="035f9-117">指定或抓取當滑鼠停留在影片的可點按區域時，所使用的資料指標值。</span><span class="sxs-lookup"><span data-stu-id="035f9-117">Specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>                                                                                                                               |
| [<span data-ttu-id="035f9-118">全屏</span><span class="sxs-lookup"><span data-stu-id="035f9-118">fullScreen</span></span>](video-fullscreen.md)                   | <span data-ttu-id="035f9-119">指定或抓取值，指出影片是否以全螢幕模式顯示。</span><span class="sxs-lookup"><span data-stu-id="035f9-119">Specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span> <span data-ttu-id="035f9-120">只有在執行時間才可設定。</span><span class="sxs-lookup"><span data-stu-id="035f9-120">Can only be set at run time.</span></span>                                                                                                               |
| [<span data-ttu-id="035f9-121">maintainAspectRatio</span><span class="sxs-lookup"><span data-stu-id="035f9-121">maintainAspectRatio</span></span>](video-maintainaspectratio.md) | <span data-ttu-id="035f9-122">指定或抓取值，指出影片是否會在嘗試符合為控制項定義的寬度和高度時維持外觀比例。</span><span class="sxs-lookup"><span data-stu-id="035f9-122">Specifies or retrieves a value indicating whether the video will maintain the aspect ratio when trying to fit within the width and height defined for the control.</span></span>                                                                       |
| [<span data-ttu-id="035f9-123">shrinkToFit</span><span class="sxs-lookup"><span data-stu-id="035f9-123">shrinkToFit</span></span>](video-shrinktofit.md)                 | <span data-ttu-id="035f9-124">指定或抓取值，指出影片是否會壓縮成針對影片控制項定義的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="035f9-124">Specifies or retrieves a value indicating whether the video will shrink to the width and height defined for the Video control.</span></span>                                                                                                           |
| [<span data-ttu-id="035f9-125">stretchToFit</span><span class="sxs-lookup"><span data-stu-id="035f9-125">stretchToFit</span></span>](video-stretchtofit.md)               | <span data-ttu-id="035f9-126">指定或抓取值，指出影片是否將本身延展至為影片控制項定義的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="035f9-126">Specifies or retrieves a value indicating whether the video will stretch itself to the width and height defined for the Video control.</span></span>                                                                                                   |
| [<span data-ttu-id="035f9-127">提示</span><span class="sxs-lookup"><span data-stu-id="035f9-127">toolTip</span></span>](video-tooltip.md)                         | <span data-ttu-id="035f9-128">指定或抓取影片視窗的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="035f9-128">Specifies or retrieves the ToolTip text for the video window.</span></span>                                                                                                                                                                            |
| [<span data-ttu-id="035f9-129">無視窗</span><span class="sxs-lookup"><span data-stu-id="035f9-129">windowless</span></span>](video-windowless.md)                   | <span data-ttu-id="035f9-130">指定或抓取值，指出影片控制項是否為視窗化或無視窗;也就是說，控制項的整個矩形是否隨時都可以看見，或是可以裁剪。</span><span class="sxs-lookup"><span data-stu-id="035f9-130">Specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="035f9-131">只能在設計階段設定。</span><span class="sxs-lookup"><span data-stu-id="035f9-131">Can only be set at design time.</span></span> |
| [<span data-ttu-id="035f9-132">縮放</span><span class="sxs-lookup"><span data-stu-id="035f9-132">zoom</span></span>](video-zoom.md)                               | <span data-ttu-id="035f9-133">指定縮放影片的百分比。</span><span class="sxs-lookup"><span data-stu-id="035f9-133">Specifies the percentage by which to scale the video.</span></span>                                                                                                                                                                                    |



 

<span data-ttu-id="035f9-134">**影片** 元素可以執行下列事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="035f9-134">The **VIDEO** element can implement the following event handlers.</span></span>



| <span data-ttu-id="035f9-135">事件處理常式</span><span class="sxs-lookup"><span data-stu-id="035f9-135">Event handler</span></span>                          | <span data-ttu-id="035f9-136">Description</span><span class="sxs-lookup"><span data-stu-id="035f9-136">Description</span></span>                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="035f9-137">onvideoend</span><span class="sxs-lookup"><span data-stu-id="035f9-137">onvideoend</span></span>](video-onvideoend.md)     | <span data-ttu-id="035f9-138">處理當影片停止轉譯並卸載時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="035f9-138">Handles an event that occurs when the video stops rendering and is unloaded.</span></span> |
| [<span data-ttu-id="035f9-139">onvideostart</span><span class="sxs-lookup"><span data-stu-id="035f9-139">onvideostart</span></span>](video-onvideostart.md) | <span data-ttu-id="035f9-140">處理載入影片並開始轉譯時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="035f9-140">Handles an event that occurs when the video is loaded and begins to render.</span></span>  |



 

<span data-ttu-id="035f9-141">**VIDEO** 元素支援環境屬性，而且可以執行環境事件處理常式（除非有注明）。</span><span class="sxs-lookup"><span data-stu-id="035f9-141">The **VIDEO** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="035f9-142">如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md) 和 [環境事件處理常式](ambient-event-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="035f9-142">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

<span data-ttu-id="035f9-143">預先定義的影片專案是一般的 **影片** 元素，預設會指定各種不同的通用屬性設定。</span><span class="sxs-lookup"><span data-stu-id="035f9-143">Predefined video elements are normal **VIDEO** elements with various common attribute settings specified by default.</span></span> <span data-ttu-id="035f9-144">您可以使用下列預先定義的影片元素。</span><span class="sxs-lookup"><span data-stu-id="035f9-144">The following predefined video elements are available.</span></span>



| <span data-ttu-id="035f9-145">預先定義的影片</span><span class="sxs-lookup"><span data-stu-id="035f9-145">Predefined VIDEO</span></span>         | <span data-ttu-id="035f9-146">Description</span><span class="sxs-lookup"><span data-stu-id="035f9-146">Description</span></span>                                                |
|--------------------------|------------------------------------------------------------|
| [<span data-ttu-id="035f9-147">WMPVIDEO</span><span class="sxs-lookup"><span data-stu-id="035f9-147">WMPVIDEO</span></span>](wmpvideo.md) | <span data-ttu-id="035f9-148">調整大小後，自動調整影片的 **影片** 元素。</span><span class="sxs-lookup"><span data-stu-id="035f9-148">A **VIDEO** element that stretches the video when resized.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="035f9-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="035f9-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="035f9-150">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="035f9-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




