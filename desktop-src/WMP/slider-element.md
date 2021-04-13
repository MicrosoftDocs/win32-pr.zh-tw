---
title: 滑杆元素
description: 滑杆元素
ms.assetid: f1da8987-5430-46ef-b7d7-ac92f34a2185
keywords:
- Windows Media Player 面板，滑杆元素
- 外觀，滑杆元素
- 滑杆元素
- 外觀、滑杆元素的參考
- 元素、滑杆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34607c8706fccc8f416ebc83ae483c98a784c08b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301148"
---
# <a name="slider-element"></a><span data-ttu-id="75001-108">滑杆元素</span><span class="sxs-lookup"><span data-stu-id="75001-108">SLIDER Element</span></span>

<span data-ttu-id="75001-109">**滑杆** 元素提供建立和操作簡單水準或垂直滑杆控制項的方式。</span><span class="sxs-lookup"><span data-stu-id="75001-109">The **SLIDER** element provides a way to create and manipulate a simple horizontal or vertical slider control.</span></span> <span data-ttu-id="75001-110">它支援下列屬性和事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="75001-110">It supports the following attributes and event handlers.</span></span> <span data-ttu-id="75001-111">為了方便起見，也提供預先定義的 **滑杆** 元素。</span><span class="sxs-lookup"><span data-stu-id="75001-111">Predefined **SLIDER** elements are also provided for convenience.</span></span>

<span data-ttu-id="75001-112">**滑杆** 元素支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="75001-112">The **SLIDER** element supports the following attributes.</span></span>



| <span data-ttu-id="75001-113">屬性</span><span class="sxs-lookup"><span data-stu-id="75001-113">Attribute</span></span>                                                 | <span data-ttu-id="75001-114">描述</span><span class="sxs-lookup"><span data-stu-id="75001-114">Description</span></span>                                                                                                       |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75001-115">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="75001-115">backgroundColor</span></span>](slider-backgroundcolor.md)             | <span data-ttu-id="75001-116">指定或抓取滑杆控制項的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="75001-116">Specifies or retrieves the background color of the slider control.</span></span>                                                |
| [<span data-ttu-id="75001-117">backgroundEndColor</span><span class="sxs-lookup"><span data-stu-id="75001-117">backgroundEndColor</span></span>](slider-backgroundendcolor.md)       | <span data-ttu-id="75001-118">指定或抓取滑杆控制項的背景結束色彩。</span><span class="sxs-lookup"><span data-stu-id="75001-118">Specifies or retrieves the background ending color of the slider control.</span></span>                                         |
| [<span data-ttu-id="75001-119">backgroundHoverImage</span><span class="sxs-lookup"><span data-stu-id="75001-119">backgroundHoverImage</span></span>](slider-backgroundhoverimage.md)   | <span data-ttu-id="75001-120">指定或抓取將滑鼠停留在其上方時顯示之滑杆的背景影像。</span><span class="sxs-lookup"><span data-stu-id="75001-120">Specifies or retrieves the background image of the slider that appears when hovering over it with the mouse.</span></span>      |
| [<span data-ttu-id="75001-121">backgroundImage</span><span class="sxs-lookup"><span data-stu-id="75001-121">backgroundImage</span></span>](slider-backgroundimage.md)             | <span data-ttu-id="75001-122">指定或抓取滑杆的預設背景影像。</span><span class="sxs-lookup"><span data-stu-id="75001-122">Specifies or retrieves the default background image of the slider.</span></span>                                                |
| [<span data-ttu-id="75001-123">borderSize</span><span class="sxs-lookup"><span data-stu-id="75001-123">borderSize</span></span>](slider-bordersize.md)                       | <span data-ttu-id="75001-124">指定或抓取框線大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="75001-124">Specifies or retrieves the border size in pixels.</span></span>                                                                 |
| [<span data-ttu-id="75001-125">cursor</span><span class="sxs-lookup"><span data-stu-id="75001-125">cursor</span></span>](slider-cursor.md)                               | <span data-ttu-id="75001-126">指定或抓取值，指出當滑鼠停留在滑杆控制項上時，所顯示的游標類型。</span><span class="sxs-lookup"><span data-stu-id="75001-126">Specifies or retrieves a value indicating which type of cursor appears when the mouse is over the slider control.</span></span> |
| [<span data-ttu-id="75001-127">direction</span><span class="sxs-lookup"><span data-stu-id="75001-127">direction</span></span>](slider-direction.md)                         | <span data-ttu-id="75001-128">指定或抓取滑杆影像的配置方向。</span><span class="sxs-lookup"><span data-stu-id="75001-128">Specifies or retrieves the direction that slider images are laid out.</span></span>                                             |
| [<span data-ttu-id="75001-129">disabledColor</span><span class="sxs-lookup"><span data-stu-id="75001-129">disabledColor</span></span>](slider-disabledcolor.md)                 | <span data-ttu-id="75001-130">指定或抓取滑杆控制項的停用色彩。</span><span class="sxs-lookup"><span data-stu-id="75001-130">Specifies or retrieves the disabled color of the slider control.</span></span>                                                  |
| [<span data-ttu-id="75001-131">disabledImage</span><span class="sxs-lookup"><span data-stu-id="75001-131">disabledImage</span></span>](slider-disabledimage.md)                 | <span data-ttu-id="75001-132">指定或抓取停用控制項時所顯示之滑杆的影像。</span><span class="sxs-lookup"><span data-stu-id="75001-132">Specifies or retrieves the image of the slider that appears when the control is disabled.</span></span>                         |
| [<span data-ttu-id="75001-133">foregroundColor</span><span class="sxs-lookup"><span data-stu-id="75001-133">foregroundColor</span></span>](slider-foregroundcolor.md)             | <span data-ttu-id="75001-134">指定或抓取滑杆控制項的前景色彩。</span><span class="sxs-lookup"><span data-stu-id="75001-134">Specifies or retrieves the foreground color of the slider control.</span></span>                                                |
| [<span data-ttu-id="75001-135">foregroundEndColor</span><span class="sxs-lookup"><span data-stu-id="75001-135">foregroundEndColor</span></span>](slider-foregroundendcolor.md)       | <span data-ttu-id="75001-136">指定或抓取滑杆控制項的前景結束色彩。</span><span class="sxs-lookup"><span data-stu-id="75001-136">Specifies or retrieves the foreground ending color of the slider control.</span></span>                                         |
| [<span data-ttu-id="75001-137">foregroundHoverImage</span><span class="sxs-lookup"><span data-stu-id="75001-137">foregroundHoverImage</span></span>](slider-foregroundhoverimage.md)   | <span data-ttu-id="75001-138">指定或抓取將滑鼠停留在其上方時顯示之滑杆的前景影像。</span><span class="sxs-lookup"><span data-stu-id="75001-138">Specifies or retrieves the foreground image of the slider that appears when hovering over it with the mouse.</span></span>      |
| [<span data-ttu-id="75001-139">foregroundImage</span><span class="sxs-lookup"><span data-stu-id="75001-139">foregroundImage</span></span>](slider-foregroundimage.md)             | <span data-ttu-id="75001-140">指定或抓取滑杆的預設前景影像。</span><span class="sxs-lookup"><span data-stu-id="75001-140">Specifies or retrieves the default foreground image of the slider.</span></span>                                                |
| [<span data-ttu-id="75001-141">foregroundProgress</span><span class="sxs-lookup"><span data-stu-id="75001-141">foregroundProgress</span></span>](slider-foregroundprogress.md)       | <span data-ttu-id="75001-142">指定或抓取前景進度列的目前位置（以滑杆區域的百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="75001-142">Specifies or retrieves the current position of the foreground progress bar as a percentage of the slider area.</span></span>    |
| [<span data-ttu-id="75001-143">max</span><span class="sxs-lookup"><span data-stu-id="75001-143">max</span></span>](slider-max.md)                                     | <span data-ttu-id="75001-144">指定或抓取滑杆控制項所定義範圍的最大值。</span><span class="sxs-lookup"><span data-stu-id="75001-144">Specifies or retrieves the maximum value of the range defined by the slider control.</span></span>                              |
| [<span data-ttu-id="75001-145">min</span><span class="sxs-lookup"><span data-stu-id="75001-145">min</span></span>](slider-min.md)                                     | <span data-ttu-id="75001-146">指定或抓取滑杆控制項所定義範圍的最小值。</span><span class="sxs-lookup"><span data-stu-id="75001-146">Specifies or retrieves the minimum value of the range defined by the slider control.</span></span>                              |
| [<span data-ttu-id="75001-147">幻燈片</span><span class="sxs-lookup"><span data-stu-id="75001-147">slide</span></span>](slider-slide.md)                                 | <span data-ttu-id="75001-148">指定或抓取值，指出前景影像是否滑過背景影像。</span><span class="sxs-lookup"><span data-stu-id="75001-148">Specifies or retrieves a value indicating whether the foreground image slides over the background image.</span></span>          |
| [<span data-ttu-id="75001-149">thumbDisabledImage</span><span class="sxs-lookup"><span data-stu-id="75001-149">thumbDisabledImage</span></span>](slider-thumbdisabledimage.md)       | <span data-ttu-id="75001-150">指定或抓取滑杆控制項的停用捲動方塊影像。</span><span class="sxs-lookup"><span data-stu-id="75001-150">Specifies or retrieves the disabled thumb image of the slider control.</span></span>                                            |
| [<span data-ttu-id="75001-151">thumbDownImage</span><span class="sxs-lookup"><span data-stu-id="75001-151">thumbDownImage</span></span>](slider-thumbdownimage.md)               | <span data-ttu-id="75001-152">指定或抓取表示 thumb 關閉狀態的影像。</span><span class="sxs-lookup"><span data-stu-id="75001-152">Specifies or retrieves the image representing the down state of the thumb.</span></span>                                        |
| [<span data-ttu-id="75001-153">thumbHoverImage</span><span class="sxs-lookup"><span data-stu-id="75001-153">thumbHoverImage</span></span>](slider-thumbhoverimage.md)             | <span data-ttu-id="75001-154">指定或抓取將滑鼠停留在其上方時所顯示之捲動方塊的影像。</span><span class="sxs-lookup"><span data-stu-id="75001-154">Specifies or retrieves the image of the thumb that appears when hovering over it with the mouse.</span></span>                  |
| [<span data-ttu-id="75001-155">thumbImage</span><span class="sxs-lookup"><span data-stu-id="75001-155">thumbImage</span></span>](slider-thumbimage.md)                       | <span data-ttu-id="75001-156">指定或抓取將用來表示滑杆目前位置的影像。</span><span class="sxs-lookup"><span data-stu-id="75001-156">Specifies or retrieves the image that will be used to represent the current position of the slider.</span></span>               |
| [<span data-ttu-id="75001-157">平鋪</span><span class="sxs-lookup"><span data-stu-id="75001-157">tiled</span></span>](slider-tiled.md)                                 | <span data-ttu-id="75001-158">指定或抓取值，指出是否要將滑杆影像並排顯示。</span><span class="sxs-lookup"><span data-stu-id="75001-158">Specifies or retrieves a value indicating whether the slider images will be tiled.</span></span>                                |
| [<span data-ttu-id="75001-159">提示</span><span class="sxs-lookup"><span data-stu-id="75001-159">toolTip</span></span>](slider-tooltip.md)                             | <span data-ttu-id="75001-160">指定或抓取滑杆控制項的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="75001-160">Specifies or retrieves the ToolTip text for the slider control.</span></span>                                                   |
| [<span data-ttu-id="75001-161">transparencyColor</span><span class="sxs-lookup"><span data-stu-id="75001-161">transparencyColor</span></span>](slider-transparencycolor.md)         | <span data-ttu-id="75001-162">指定或抓取滑杆影像的透明色彩。</span><span class="sxs-lookup"><span data-stu-id="75001-162">Specifies or retrieves the transparent color of the slider images.</span></span>                                                |
| [<span data-ttu-id="75001-163">useForegroundProgress</span><span class="sxs-lookup"><span data-stu-id="75001-163">useForegroundProgress</span></span>](slider-useforegroundprogress.md) | <span data-ttu-id="75001-164">指定或抓取值，指出是否將使用前景進度列。</span><span class="sxs-lookup"><span data-stu-id="75001-164">Specifies or retrieves a value indicating whether the foreground progress bar will be used.</span></span>                       |
| [<span data-ttu-id="75001-165">value</span><span class="sxs-lookup"><span data-stu-id="75001-165">value</span></span>](slider-value.md)                                 | <span data-ttu-id="75001-166">指定並抓取滑杆的目前位置。</span><span class="sxs-lookup"><span data-stu-id="75001-166">Specifies and retrieves the current position of the slider.</span></span>                                                       |



 

<span data-ttu-id="75001-167">**滑杆** 元素可以執行下列事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="75001-167">The **SLIDER** element can implement the following event handlers.</span></span>



| <span data-ttu-id="75001-168">事件處理常式</span><span class="sxs-lookup"><span data-stu-id="75001-168">Event handler</span></span>                                   | <span data-ttu-id="75001-169">Description</span><span class="sxs-lookup"><span data-stu-id="75001-169">Description</span></span>                                                                                                          |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75001-170">onDragBegin</span><span class="sxs-lookup"><span data-stu-id="75001-170">onDragBegin</span></span>](slider-ondragbegin.md)           | <span data-ttu-id="75001-171">處理當使用者按一下並按住滑鼠左鍵並開始拖曳滑鼠時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="75001-171">Handles an event that occurs when the user clicks and holds the left mouse button down and begins to drag the mouse.</span></span> |
| [<span data-ttu-id="75001-172">onDragEnd</span><span class="sxs-lookup"><span data-stu-id="75001-172">onDragEnd</span></span>](slider-ondragend.md)               | <span data-ttu-id="75001-173">處理在拖曳作業之後放開滑鼠左鍵時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="75001-173">Handles an event that occurs when the left mouse button is released after a dragging operation.</span></span>                      |
| [<span data-ttu-id="75001-174">onPositionChange</span><span class="sxs-lookup"><span data-stu-id="75001-174">onPositionChange</span></span>](slider-onpositionchange.md) | <span data-ttu-id="75001-175">處理當滑杆的位置由於使用者按一下或拖曳而變更時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="75001-175">Handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>   |



 

<span data-ttu-id="75001-176">**滑杆** 元素支援環境屬性，並可執行環境事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="75001-176">The **SLIDER** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="75001-177">如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md) 和 [環境事件處理常式](ambient-event-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="75001-177">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

<span data-ttu-id="75001-178">預先定義的滑杆是標準 **滑杆** 元素，預設會指定各種不同的通用屬性設定。</span><span class="sxs-lookup"><span data-stu-id="75001-178">Predefined sliders are normal **SLIDER** elements with various common attribute settings specified by default.</span></span> <span data-ttu-id="75001-179">您可以使用下列預先定義的滑杆。</span><span class="sxs-lookup"><span data-stu-id="75001-179">The following predefined sliders are available.</span></span>



| <span data-ttu-id="75001-180">預先定義的滑杆</span><span class="sxs-lookup"><span data-stu-id="75001-180">Predefined SLIDER</span></span>                  | <span data-ttu-id="75001-181">Description</span><span class="sxs-lookup"><span data-stu-id="75001-181">Description</span></span>                                                    |
|------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="75001-182">BALANCESLIDER</span><span class="sxs-lookup"><span data-stu-id="75001-182">BALANCESLIDER</span></span>](balanceslider.md) | <span data-ttu-id="75001-183">用來設定音訊餘額的 **滑杆** 。</span><span class="sxs-lookup"><span data-stu-id="75001-183">A **SLIDER** used to set audio balance.</span></span>                        |
| [<span data-ttu-id="75001-184">SEEKSLIDER</span><span class="sxs-lookup"><span data-stu-id="75001-184">SEEKSLIDER</span></span>](seekslider.md)       | <span data-ttu-id="75001-185">用來搜尋媒體檔案內任何位置的 **滑杆** 。</span><span class="sxs-lookup"><span data-stu-id="75001-185">A **SLIDER** used to seek to any position within a media file.</span></span> |
| [<span data-ttu-id="75001-186">VOLUMESLIDER</span><span class="sxs-lookup"><span data-stu-id="75001-186">VOLUMESLIDER</span></span>](volumeslider.md)   | <span data-ttu-id="75001-187">用來設定音訊音量的 **滑杆** 。</span><span class="sxs-lookup"><span data-stu-id="75001-187">A **SLIDER** used to set audio volume.</span></span>                         |



 

## <a name="related-topics"></a><span data-ttu-id="75001-188">相關主題</span><span class="sxs-lookup"><span data-stu-id="75001-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75001-189">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="75001-189">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




