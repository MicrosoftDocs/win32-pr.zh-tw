---
title: VIEW 元素
description: VIEW 元素
ms.assetid: e1dfde08-33a0-4f12-8db0-ad62e4a1d467
keywords:
- Windows Media Player 的外觀、VIEW 元素
- 外觀，VIEW 元素
- VIEW 元素
- 外觀的參考、VIEW 元素
- 元素、VIEW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e907cced22b4d1cd498054df06ac8677a7488b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372316"
---
# <a name="view-element"></a><span data-ttu-id="0d0ea-108">VIEW 元素</span><span class="sxs-lookup"><span data-stu-id="0d0ea-108">VIEW Element</span></span>

<span data-ttu-id="0d0ea-109">**VIEW** 元素包含面板的使用者介面詳細資料，並使用下表所示的屬性、方法和事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-109">The **VIEW** element contains the user interface details of a skin, and uses the attributes, methods, and event handlers shown in the following tables.</span></span>

<span data-ttu-id="0d0ea-110">您可以將多個 **VIEW** 專案定義為面板 **主題** 專案的子系，以針對不同的情況提供不同的介面。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-110">Multiple **VIEW** elements can be defined as children of the **THEME** element of a skin to provide different interfaces for different situations.</span></span> <span data-ttu-id="0d0ea-111">**VIEW** 元素不能指定為任何其他專案的子系，而且它們包含所有其他的面板元素。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-111">**VIEW** elements cannot be specified as children of any other element, and they contain all other skin elements.</span></span> <span data-ttu-id="0d0ea-112">請注意，每個視圖都有自己的變數範圍，這表示它無法與其他視圖共用屬性值。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-112">Note that each view has its own variable scope, which means it cannot share attribute values with other views.</span></span>

<span data-ttu-id="0d0ea-113">**View** global 屬性可以用來從它內部的任何位置參考特定的 **view** 元素。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-113">The **view** global attribute can be used to reference a specific **VIEW** element from anywhere within it.</span></span> <span data-ttu-id="0d0ea-114">這是使用其 **id** 屬性的替代方案，必須從其他 **VIEW** 專案或 **主題** 專案內使用。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-114">This is an alternative to using its **id** attribute, which must be used from within other **VIEW** elements or from within the **THEME** element.</span></span>

<span data-ttu-id="0d0ea-115">**VIEW** 元素支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-115">The **VIEW** element supports the following attributes.</span></span> <span data-ttu-id="0d0ea-116">子視圖專案也支援標記有星號 (\*) 的屬性 。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-116">Attributes marked with an asterisk (\*) are also supported by the **SUBVIEW** element.</span></span>



| <span data-ttu-id="0d0ea-117">屬性</span><span class="sxs-lookup"><span data-stu-id="0d0ea-117">Attribute</span></span>                                                       | <span data-ttu-id="0d0ea-118">描述</span><span class="sxs-lookup"><span data-stu-id="0d0ea-118">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0ea-119">[backgroundColor](view-backgroundcolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="0d0ea-119">[backgroundColor](view-backgroundcolor.md) \*</span></span>                  | <span data-ttu-id="0d0ea-120">指定或抓取 **視圖** 或 **子視圖的背景色彩。**</span><span class="sxs-lookup"><span data-stu-id="0d0ea-120">Specifies or retrieves the background color of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| <span data-ttu-id="0d0ea-121">[backgroundImage](view-backgroundimage.md) \*</span><span class="sxs-lookup"><span data-stu-id="0d0ea-121">[backgroundImage](view-backgroundimage.md) \*</span></span>                  | <span data-ttu-id="0d0ea-122">指定或抓取 **視圖** 或 **子視圖的背景影像。**</span><span class="sxs-lookup"><span data-stu-id="0d0ea-122">Specifies or retrieves the background image of the **VIEW** or **SUBVIEW**.</span></span>                                             |
| [<span data-ttu-id="0d0ea-123">backgroundImageHueShift</span><span class="sxs-lookup"><span data-stu-id="0d0ea-123">backgroundImageHueShift</span></span>](view-backgroundimagehueshift.md)     | <span data-ttu-id="0d0ea-124">指定或抓取背景影像色調的位移量。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-124">Specifies or retrieves the amount by which the hue of the background image is shifted.</span></span>                                  |
| [<span data-ttu-id="0d0ea-125">backgroundImageSaturation</span><span class="sxs-lookup"><span data-stu-id="0d0ea-125">backgroundImageSaturation</span></span>](view-backgroundimagesaturation.md) | <span data-ttu-id="0d0ea-126">指定或抓取背景影像的飽和度值。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-126">Specifies or retrieves the saturation value of the background image.</span></span>                                                    |
| <span data-ttu-id="0d0ea-127">[backgroundTiled](view-backgroundtiled.md)\*</span><span class="sxs-lookup"><span data-stu-id="0d0ea-127">[backgroundTiled](view-backgroundtiled.md) \*</span></span>                  | <span data-ttu-id="0d0ea-128">指定或抓取值，指出 **視圖** 或子視圖的背景 **影像是否已** 平鋪。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-128">Specifies or retrieves a value indicating whether the background image of the **VIEW** or **SUBVIEW** is tiled.</span></span>         |
| [<span data-ttu-id="0d0ea-129">類別</span><span class="sxs-lookup"><span data-stu-id="0d0ea-129">category</span></span>](view-category.md)                                   | <span data-ttu-id="0d0ea-130">指定或抓取將顯示使用者介面的分類。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-130">Specifies or retrieves the category for which the user interface will appear.</span></span>                                           |
| [<span data-ttu-id="0d0ea-131">focusObjectID</span><span class="sxs-lookup"><span data-stu-id="0d0ea-131">focusObjectID</span></span>](view-focusobjectid.md)                         | <span data-ttu-id="0d0ea-132">指定或抓取值，指出哪個元素具有鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-132">Specifies or retrieves a value indicating which element has keyboard focus.</span></span>                                             |
| [<span data-ttu-id="0d0ea-133">maxHeight</span><span class="sxs-lookup"><span data-stu-id="0d0ea-133">maxHeight</span></span>](view-maxheight.md)                                 | <span data-ttu-id="0d0ea-134">當調整大小時，指定或抓取 **視圖** 的最大高度。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-134">Specifies or retrieves the maximum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="0d0ea-135">maxWidth</span><span class="sxs-lookup"><span data-stu-id="0d0ea-135">maxWidth</span></span>](view-maxwidth.md)                                   | <span data-ttu-id="0d0ea-136">當調整大小時，指定或抓取 **視圖** 的最大寬度。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-136">Specifies or retrieves the maximum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="0d0ea-137">minHeight</span><span class="sxs-lookup"><span data-stu-id="0d0ea-137">minHeight</span></span>](view-minheight.md)                                 | <span data-ttu-id="0d0ea-138">在調整大小時，指定或抓取 **視圖** 的最小高度。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-138">Specifies or retrieves the minimum height of the **VIEW** when resizing.</span></span>                                                |
| [<span data-ttu-id="0d0ea-139">minWidth</span><span class="sxs-lookup"><span data-stu-id="0d0ea-139">minWidth</span></span>](view-minwidth.md)                                   | <span data-ttu-id="0d0ea-140">當調整大小時，指定或抓取 **視圖** 的寬度下限。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-140">Specifies or retrieves the minimum width of the **VIEW** when resizing.</span></span>                                                 |
| [<span data-ttu-id="0d0ea-141">小時</span><span class="sxs-lookup"><span data-stu-id="0d0ea-141">resizable</span></span>](view-resizable.md)                                 | <span data-ttu-id="0d0ea-142">指定或抓取值，指出是否可以調整 **視圖** 的大小。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-142">Specifies or retrieves a value indicating whether the **VIEW** can be resized.</span></span>                                          |
| [<span data-ttu-id="0d0ea-143">resizeBackgroundImage</span><span class="sxs-lookup"><span data-stu-id="0d0ea-143">resizeBackgroundImage</span></span>](view-resizebackgroundimage.md)         | <span data-ttu-id="0d0ea-144">指定或抓取值，指出背景影像是否可以調整大小。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-144">Specifies or retrieves a value indicating whether the background image can be resized.</span></span>                                  |
| [<span data-ttu-id="0d0ea-145">scriptFile</span><span class="sxs-lookup"><span data-stu-id="0d0ea-145">scriptFile</span></span>](view-scriptfile.md)                               | <span data-ttu-id="0d0ea-146">指定隨附之 JScript 檔案的檔案名。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-146">Specifies the file names of accompanying JScript files.</span></span>                                                                 |
| [<span data-ttu-id="0d0ea-147">timerInterval</span><span class="sxs-lookup"><span data-stu-id="0d0ea-147">timerInterval</span></span>](view-timerinterval.md)                         | <span data-ttu-id="0d0ea-148">指定或抓取計時器引發事件至 **ontimer** 事件處理常式的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-148">Specifies or retrieves the interval, in milliseconds, at which the timer fires events to the **ontimer** event handler.</span></span> |
| [<span data-ttu-id="0d0ea-149">title</span><span class="sxs-lookup"><span data-stu-id="0d0ea-149">title</span></span>](view-title.md)                                         | <span data-ttu-id="0d0ea-150">指定或抓取 **視圖** 的標題。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-150">Specifies or retrieves the title of the **VIEW**.</span></span> <span data-ttu-id="0d0ea-151">只能在設計階段設定。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-151">Can only be set at design time.</span></span>                                       |
| [<span data-ttu-id="0d0ea-152">標題列</span><span class="sxs-lookup"><span data-stu-id="0d0ea-152">titleBar</span></span>](view-titlebar.md)                                   | <span data-ttu-id="0d0ea-153">指定或抓取值，指出是否顯示視窗標題列。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-153">Specifies or retrieves a value indicating whether the window title bar is shown.</span></span>                                        |
| <span data-ttu-id="0d0ea-154">[transparencyColor](view-transparencycolor.md)\*</span><span class="sxs-lookup"><span data-stu-id="0d0ea-154">[transparencyColor](view-transparencycolor.md) \*</span></span>              | <span data-ttu-id="0d0ea-155">指定或抓取背景影像的透明色彩。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-155">Specifies or retrieves the transparency color of the background image.</span></span>                                                  |



 

<span data-ttu-id="0d0ea-156">**VIEW** 元素支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-156">The **VIEW** element supports the following methods.</span></span>



| <span data-ttu-id="0d0ea-157">方法</span><span class="sxs-lookup"><span data-stu-id="0d0ea-157">Method</span></span>                                              | <span data-ttu-id="0d0ea-158">描述</span><span class="sxs-lookup"><span data-stu-id="0d0ea-158">Description</span></span>                                                |
|-----------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="0d0ea-159">close</span><span class="sxs-lookup"><span data-stu-id="0d0ea-159">close</span></span>](view-close.md)                             | <span data-ttu-id="0d0ea-160">關閉 **VIEW**。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-160">Closes the **VIEW**.</span></span>                                       |
| [<span data-ttu-id="0d0ea-161">最大化</span><span class="sxs-lookup"><span data-stu-id="0d0ea-161">maximize</span></span>](view-maximize.md)                       | <span data-ttu-id="0d0ea-162">將 **視圖** 最大化。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-162">Maximizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="0d0ea-163">最小 化</span><span class="sxs-lookup"><span data-stu-id="0d0ea-163">minimize</span></span>](view-minimize.md)                       | <span data-ttu-id="0d0ea-164">將 **視圖** 降至最低。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-164">Minimizes the **VIEW**.</span></span>                                    |
| [<span data-ttu-id="0d0ea-165">restore</span><span class="sxs-lookup"><span data-stu-id="0d0ea-165">restore</span></span>](view-restore.md)                         | <span data-ttu-id="0d0ea-166">還原 **視圖**。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-166">Restores the **VIEW**.</span></span>                                     |
| [<span data-ttu-id="0d0ea-167">returnToMediaCenter</span><span class="sxs-lookup"><span data-stu-id="0d0ea-167">returnToMediaCenter</span></span>](view-returntomediacenter.md) | <span data-ttu-id="0d0ea-168">將使用者返回 Windows Media Player 的完整模式。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-168">Returns the user to the full mode of Windows Media Player.</span></span> |
| [<span data-ttu-id="0d0ea-169">size</span><span class="sxs-lookup"><span data-stu-id="0d0ea-169">size</span></span>](view-size.md)                               | <span data-ttu-id="0d0ea-170">調整指定邊緣的 **視圖** 大小。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-170">Resizes the **VIEW** on a specified edge.</span></span>                  |



 

<span data-ttu-id="0d0ea-171">**VIEW** 元素可以執行下列事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-171">The **VIEW** element can implement the following event handlers.</span></span>



| <span data-ttu-id="0d0ea-172">事件處理常式</span><span class="sxs-lookup"><span data-stu-id="0d0ea-172">Event handler</span></span>               | <span data-ttu-id="0d0ea-173">Description</span><span class="sxs-lookup"><span data-stu-id="0d0ea-173">Description</span></span>                                                                |
|-----------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="0d0ea-174">onclose</span><span class="sxs-lookup"><span data-stu-id="0d0ea-174">onclose</span></span>](view-onclose.md) | <span data-ttu-id="0d0ea-175">處理 **視圖** 即將關閉時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-175">Handles an event that occurs when the **VIEW** is about to be closed.</span></span>      |
| [<span data-ttu-id="0d0ea-176">onerror</span><span class="sxs-lookup"><span data-stu-id="0d0ea-176">onerror</span></span>](view-onerror.md) | <span data-ttu-id="0d0ea-177">如果設定 **. enableErrorDialogs** 設定為 false，則會處理錯誤事件。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-177">Handles an error event if **Settings.enableErrorDialogs** is set to false.</span></span> |
| [<span data-ttu-id="0d0ea-178">onload</span><span class="sxs-lookup"><span data-stu-id="0d0ea-178">onload</span></span>](view-onload.md)   | <span data-ttu-id="0d0ea-179">處理第一次顯示 **視圖** 時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-179">Handles an event that occurs when the **VIEW** is first displayed.</span></span>         |
| [<span data-ttu-id="0d0ea-180">ontimer</span><span class="sxs-lookup"><span data-stu-id="0d0ea-180">ontimer</span></span>](view-ontimer.md) | <span data-ttu-id="0d0ea-181">處理計時器事件。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-181">Handles timer events.</span></span>                                                      |



 

<span data-ttu-id="0d0ea-182">**VIEW** 元素支援環境屬性，而且可以執行環境事件處理常式（除非有注明）。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-182">The **VIEW** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="0d0ea-183">如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md) 和 [環境事件處理常式](ambient-event-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="0d0ea-183">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md),</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d0ea-184">相關主題</span><span class="sxs-lookup"><span data-stu-id="0d0ea-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d0ea-185">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="0d0ea-185">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




