---
title: CUSTOMSLIDER 元素
description: CUSTOMSLIDER 元素
ms.assetid: 9cba9bdd-ea5b-4a4a-a61e-e6aff29fc3e0
keywords:
- Windows Media Player 的 CUSTOMSLIDER 元素
- 外觀，CUSTOMSLIDER 元素
- CUSTOMSLIDER 元素
- CUSTOMSLIDER 元素的外觀參考
- 元素，CUSTOMSLIDER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f49fc6260df295e3266ae9ddf7b5b3eceee43d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301316"
---
# <a name="customslider-element"></a><span data-ttu-id="065f3-108">CUSTOMSLIDER 元素</span><span class="sxs-lookup"><span data-stu-id="065f3-108">CUSTOMSLIDER Element</span></span>

<span data-ttu-id="065f3-109">**CUSTOMSLIDER** 元素提供一種方式來建立和操作任何形狀的滑杆控制項，例如圓形旋鈕。</span><span class="sxs-lookup"><span data-stu-id="065f3-109">The **CUSTOMSLIDER** element provides a way to create and manipulate a slider control of any shape, such as a circular knob.</span></span> <span data-ttu-id="065f3-110">下表列出此元素支援的屬性和事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="065f3-110">The following tables list the attributes and event handlers supported by this element.</span></span>

<span data-ttu-id="065f3-111">**CUSTOMSLIDER** 元素支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="065f3-111">The **CUSTOMSLIDER** element supports the following attributes.</span></span>



| <span data-ttu-id="065f3-112">屬性</span><span class="sxs-lookup"><span data-stu-id="065f3-112">Attribute</span></span>                                               | <span data-ttu-id="065f3-113">描述</span><span class="sxs-lookup"><span data-stu-id="065f3-113">Description</span></span>                                                                                                                 |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="065f3-114">cursor</span><span class="sxs-lookup"><span data-stu-id="065f3-114">cursor</span></span>](customslider-cursor.md)                       | <span data-ttu-id="065f3-115">指定或抓取當滑鼠停留在滑杆上時，所顯示之滑杆控制項游標的值。</span><span class="sxs-lookup"><span data-stu-id="065f3-115">Specifies or retrieves the value of the slider control cursor that appears when the mouse is over the slider.</span></span>               |
| [<span data-ttu-id="065f3-116">disabledImage</span><span class="sxs-lookup"><span data-stu-id="065f3-116">disabledImage</span></span>](customslider-disabledimage.md)         | <span data-ttu-id="065f3-117">指定或抓取滑杆停用時使用的滑杆影像。</span><span class="sxs-lookup"><span data-stu-id="065f3-117">Specifies or retrieves the image of the slider used when the slider is disabled.</span></span>                                            |
| [<span data-ttu-id="065f3-118">downImage</span><span class="sxs-lookup"><span data-stu-id="065f3-118">downImage</span></span>](customslider-downimage.md)                 | <span data-ttu-id="065f3-119">指定或抓取自訂滑杆的向下狀態影像。</span><span class="sxs-lookup"><span data-stu-id="065f3-119">Specifies or retrieves the down state image of the custom slider.</span></span>                                                           |
| [<span data-ttu-id="065f3-120">hoverImage</span><span class="sxs-lookup"><span data-stu-id="065f3-120">hoverImage</span></span>](customslider-hoverimage.md)               | <span data-ttu-id="065f3-121">指定或抓取當滑鼠停留在自訂滑杆上時所顯示的影像。</span><span class="sxs-lookup"><span data-stu-id="065f3-121">Specifies or retrieves the image that displays when the mouse is over the custom slider.</span></span>                                    |
| [<span data-ttu-id="065f3-122">image</span><span class="sxs-lookup"><span data-stu-id="065f3-122">image</span></span>](customslider-image.md)                         | <span data-ttu-id="065f3-123">指定或抓取檔案的名稱，該檔案包含對應至自訂滑杆之各種狀態的影像。</span><span class="sxs-lookup"><span data-stu-id="065f3-123">Specifies or retrieves the name of the file containing the images corresponding to the various states of the custom slider.</span></span> |
| [<span data-ttu-id="065f3-124">max</span><span class="sxs-lookup"><span data-stu-id="065f3-124">max</span></span>](customslider-max.md)                             | <span data-ttu-id="065f3-125">指定或抓取自訂滑杆所定義範圍的最大值。</span><span class="sxs-lookup"><span data-stu-id="065f3-125">Specifies or retrieves the maximum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="065f3-126">min</span><span class="sxs-lookup"><span data-stu-id="065f3-126">min</span></span>](customslider-min.md)                             | <span data-ttu-id="065f3-127">指定或抓取自訂滑杆所定義範圍的最小值。</span><span class="sxs-lookup"><span data-stu-id="065f3-127">Specifies or retrieves the minimum value of the range defined by the custom slider.</span></span>                                         |
| [<span data-ttu-id="065f3-128">positionImage</span><span class="sxs-lookup"><span data-stu-id="065f3-128">positionImage</span></span>](customslider-positionimage.md)         | <span data-ttu-id="065f3-129">指定或抓取用來決定要顯示之 **圖像** 檔案位置影像的影像地圖。</span><span class="sxs-lookup"><span data-stu-id="065f3-129">Specifies or retrieves the image map used to determine which position image from the **image** file to display.</span></span>             |
| [<span data-ttu-id="065f3-130">提示</span><span class="sxs-lookup"><span data-stu-id="065f3-130">toolTip</span></span>](customslider-tooltip.md)                     | <span data-ttu-id="065f3-131">指定或抓取滑杆的工具提示文字。</span><span class="sxs-lookup"><span data-stu-id="065f3-131">Specifies or retrieves the ToolTip text for the slider.</span></span>                                                                     |
| [<span data-ttu-id="065f3-132">transparencyColor</span><span class="sxs-lookup"><span data-stu-id="065f3-132">transparencyColor</span></span>](customslider-transparencycolor.md) | <span data-ttu-id="065f3-133">指定或抓取自訂滑杆影像的透明色彩。</span><span class="sxs-lookup"><span data-stu-id="065f3-133">Specifies or retrieves the transparency color of the custom slider images.</span></span>                                                  |
| [<span data-ttu-id="065f3-134">value</span><span class="sxs-lookup"><span data-stu-id="065f3-134">value</span></span>](customslider-value.md)                         | <span data-ttu-id="065f3-135">指定或抓取滑杆的目前位置。</span><span class="sxs-lookup"><span data-stu-id="065f3-135">Specifies or retrieves the current position of the slider.</span></span>                                                                  |



 

<span data-ttu-id="065f3-136">**CUSTOMSLIDER** 元素可以執行下列事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="065f3-136">The **CUSTOMSLIDER** element can implement the following event handlers.</span></span>



| <span data-ttu-id="065f3-137">事件處理常式</span><span class="sxs-lookup"><span data-stu-id="065f3-137">Event handler</span></span>                                         | <span data-ttu-id="065f3-138">Description</span><span class="sxs-lookup"><span data-stu-id="065f3-138">Description</span></span>                                                                                                          |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="065f3-139">onDragBegin</span><span class="sxs-lookup"><span data-stu-id="065f3-139">onDragBegin</span></span>](customslider-ondragbegin.md)           | <span data-ttu-id="065f3-140">處理當使用者按一下並按住滑鼠左鍵並開始拖曳滑鼠時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="065f3-140">Handles an event that occurs when the user clicks and holds the left mouse button down and begins to drag the mouse.</span></span> |
| [<span data-ttu-id="065f3-141">onDragEnd</span><span class="sxs-lookup"><span data-stu-id="065f3-141">onDragEnd</span></span>](customslider-ondragend.md)               | <span data-ttu-id="065f3-142">處理在拖曳作業之後放開滑鼠左鍵時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="065f3-142">Handles an event that occurs when the left mouse button is released after a dragging operation.</span></span>                      |
| [<span data-ttu-id="065f3-143">onPositionChange</span><span class="sxs-lookup"><span data-stu-id="065f3-143">onPositionChange</span></span>](customslider-onpositionchange.md) | <span data-ttu-id="065f3-144">處理當滑杆的位置由於使用者按一下或拖曳而變更時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="065f3-144">Handles an event that occurs when the position of the slider changes as a result of the user clicking or dragging.</span></span>   |



 

<span data-ttu-id="065f3-145">**CUSTOMSLIDER** 元素支援環境屬性，並可執行環境事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="065f3-145">The **CUSTOMSLIDER** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="065f3-146">如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md) 和 [環境事件處理常式](ambient-event-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="065f3-146">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="065f3-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="065f3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="065f3-148">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="065f3-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




