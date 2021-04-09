---
title: BUTTONGROUP 元素
description: BUTTONGROUP 元素
ms.assetid: 4756c016-3347-4129-be5e-e822270a24de
keywords:
- Windows Media Player 的 BUTTONGROUP 元素
- 外觀，BUTTONGROUP 元素
- BUTTONGROUP 元素
- BUTTONGROUP 元素的外觀參考
- 元素，BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4de489e779b5e20214778b56fd8d19c7627e444
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092307"
---
# <a name="buttongroup-element"></a><span data-ttu-id="3d768-108">BUTTONGROUP 元素</span><span class="sxs-lookup"><span data-stu-id="3d768-108">BUTTONGROUP Element</span></span>

<span data-ttu-id="3d768-109">**BUTTONGROUP** 元素提供將面板中的數個按鈕分組的方式。</span><span class="sxs-lookup"><span data-stu-id="3d768-109">The **BUTTONGROUP** element provides a way to group several buttons within a skin.</span></span> <span data-ttu-id="3d768-110">您可以使用 **BUTTONELEMENT** 專案做為 **BUTTONGROUP** 元素的子系，以指定這些按鈕。</span><span class="sxs-lookup"><span data-stu-id="3d768-110">These buttons can be specified by using **BUTTONELEMENT** elements as children of the **BUTTONGROUP** element.</span></span>

<span data-ttu-id="3d768-111">**BUTTONGROUP** 元素支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="3d768-111">The **BUTTONGROUP** element supports the following attributes.</span></span>



| <span data-ttu-id="3d768-112">屬性</span><span class="sxs-lookup"><span data-stu-id="3d768-112">Attribute</span></span>                                              | <span data-ttu-id="3d768-113">描述</span><span class="sxs-lookup"><span data-stu-id="3d768-113">Description</span></span>                                                                                                                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d768-114">buttonCount</span><span class="sxs-lookup"><span data-stu-id="3d768-114">buttonCount</span></span>](buttongroup-buttoncount.md)             | <span data-ttu-id="3d768-115">捕獲 **BUTTONGROUP** 中的按鈕數目。</span><span class="sxs-lookup"><span data-stu-id="3d768-115">Retrieves the number of buttons in the **BUTTONGROUP**.</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="3d768-116">cursor</span><span class="sxs-lookup"><span data-stu-id="3d768-116">cursor</span></span>](buttongroup-cursor.md)                       | <span data-ttu-id="3d768-117">指定或抓取當滑鼠停留在 **BUTTONGROUP** 中的按鈕上時，所顯示的游標類型。</span><span class="sxs-lookup"><span data-stu-id="3d768-117">Specifies or retrieves the type of cursor that appears when the mouse is over a button in the **BUTTONGROUP**.</span></span>                                                                                                                  |
| [<span data-ttu-id="3d768-118">disabledImage</span><span class="sxs-lookup"><span data-stu-id="3d768-118">disabledImage</span></span>](buttongroup-disabledimage.md)         | <span data-ttu-id="3d768-119">指定或抓取表示 **BUTTONGROUP** 中按鈕已停用狀態之影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d768-119">Specifies or retrieves the name of the image representing the disabled state of the buttons in the **BUTTONGROUP**.</span></span>                                                                                                             |
| [<span data-ttu-id="3d768-120">downImage</span><span class="sxs-lookup"><span data-stu-id="3d768-120">downImage</span></span>](buttongroup-downimage.md)                 | <span data-ttu-id="3d768-121">指定或抓取表示 **BUTTONGROUP** 關閉狀態之影像的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d768-121">Specifies or retrieves the name of the image representing the down state of the **BUTTONGROUP**.</span></span>                                                                                                                                |
| [<span data-ttu-id="3d768-122">hoverDownImage</span><span class="sxs-lookup"><span data-stu-id="3d768-122">hoverDownImage</span></span>](buttongroup-hoverdownimage.md)       | <span data-ttu-id="3d768-123">指定或抓取影像的名稱，代表 **BUTTONGROUP** 中按鈕的暫止狀態。</span><span class="sxs-lookup"><span data-stu-id="3d768-123">Specifies or retrieves the name of the image representing the hover-down state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="3d768-124">當按鈕處於關閉狀態，且使用者將滑鼠停留在該按鈕上方時，就會出現暫止狀態。</span><span class="sxs-lookup"><span data-stu-id="3d768-124">The hover-down state occurs when the button is in the down state and the user hovers over it with the mouse.</span></span> |
| [<span data-ttu-id="3d768-125">hoverImage</span><span class="sxs-lookup"><span data-stu-id="3d768-125">hoverImage</span></span>](buttongroup-hoverimage.md)               | <span data-ttu-id="3d768-126">指定或抓取影像的名稱，代表 **BUTTONGROUP** 中按鈕的暫留狀態。</span><span class="sxs-lookup"><span data-stu-id="3d768-126">Specifies or retrieves the name of the image representing the hover state of a button in the **BUTTONGROUP**.</span></span> <span data-ttu-id="3d768-127">當按鈕處於 [已啟動] 狀態，且使用者將滑鼠停留在該按鈕上方時，就會發生停留狀態。</span><span class="sxs-lookup"><span data-stu-id="3d768-127">The hover state occurs when the button is in the up state and the user hovers over it with the mouse.</span></span>             |
| [<span data-ttu-id="3d768-128">hueShift</span><span class="sxs-lookup"><span data-stu-id="3d768-128">hueShift</span></span>](buttongroup-hueshift.md)                   | <span data-ttu-id="3d768-129">指定或抓取 **BUTTONGROUP** 影像色調的位移量。</span><span class="sxs-lookup"><span data-stu-id="3d768-129">Specifies or retrieves the amount by which the hue of the **BUTTONGROUP** images is shifted.</span></span>                                                                                                                                    |
| [<span data-ttu-id="3d768-130">image</span><span class="sxs-lookup"><span data-stu-id="3d768-130">image</span></span>](buttongroup-image.md)                         | <span data-ttu-id="3d768-131">指定或抓取表示 **BUTTONGROUP** 按鈕的影像名稱。</span><span class="sxs-lookup"><span data-stu-id="3d768-131">Specifies or retrieves the name of the image representing the buttons of a **BUTTONGROUP**.</span></span>                                                                                                                                     |
| [<span data-ttu-id="3d768-132">mappingImage</span><span class="sxs-lookup"><span data-stu-id="3d768-132">mappingImage</span></span>](buttongroup-mappingimage.md)           | <span data-ttu-id="3d768-133">指定或抓取表示 **BUTTONGROUP** 按鈕對應的影像名稱。</span><span class="sxs-lookup"><span data-stu-id="3d768-133">Specifies or retrieves the name of the image representing the button map of the **BUTTONGROUP**.</span></span>                                                                                                                                |
| [<span data-ttu-id="3d768-134">radio</span><span class="sxs-lookup"><span data-stu-id="3d768-134">radio</span></span>](buttongroup-radio.md)                         | <span data-ttu-id="3d768-135">指定或抓取值，指出 **BUTTONGROUP** 是否包含選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="3d768-135">Specifies or retrieves a value indicating whether the **BUTTONGROUP** is composed of radio buttons.</span></span>                                                                                                                             |
| [<span data-ttu-id="3d768-136">飽和</span><span class="sxs-lookup"><span data-stu-id="3d768-136">saturation</span></span>](buttongroup-saturation.md)               | <span data-ttu-id="3d768-137">指定或抓取 **BUTTONGROUP** 影像的飽和度值。</span><span class="sxs-lookup"><span data-stu-id="3d768-137">Specifies or retrieves the saturation value of the **BUTTONGROUP** images.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="3d768-138">showBackground</span><span class="sxs-lookup"><span data-stu-id="3d768-138">showBackground</span></span>](buttongroup-showbackground.md)       | <span data-ttu-id="3d768-139">指定或抓取值，指出 **BUTTONGROUP** 是否只會顯示按鈕，或顯示 **影像** 屬性中指定的完整點陣圖。</span><span class="sxs-lookup"><span data-stu-id="3d768-139">Specifies or retrieves a value indicating whether the **BUTTONGROUP** displays only the buttons, or displays the full bitmap specified in the **image** attribute.</span></span>                                                              |
| [<span data-ttu-id="3d768-140">transparencyColor</span><span class="sxs-lookup"><span data-stu-id="3d768-140">transparencyColor</span></span>](buttongroup-transparencycolor.md) | <span data-ttu-id="3d768-141">指定或抓取 **BUTTONGROUP** 影像的透明色彩。</span><span class="sxs-lookup"><span data-stu-id="3d768-141">Specifies or retrieves the transparent color of the **BUTTONGROUP** images.</span></span>                                                                                                                                                     |



 

<span data-ttu-id="3d768-142">**BUTTONGROUP** 元素支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="3d768-142">The **BUTTONGROUP** element supports the following methods.</span></span>



| <span data-ttu-id="3d768-143">方法</span><span class="sxs-lookup"><span data-stu-id="3d768-143">Method</span></span>                                 | <span data-ttu-id="3d768-144">描述</span><span class="sxs-lookup"><span data-stu-id="3d768-144">Description</span></span>                                                                                     |
|----------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3d768-145">點擊</span><span class="sxs-lookup"><span data-stu-id="3d768-145">click</span></span>](buttongroup-click.md)         | <span data-ttu-id="3d768-146">使用指定的索引，呼叫針對 **BUTTONELEMENT** 所定義的 **onclick** 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="3d768-146">Calls the **onclick** event handler defined for the **BUTTONELEMENT** with the specified index.</span></span> |
| [<span data-ttu-id="3d768-147">getButton</span><span class="sxs-lookup"><span data-stu-id="3d768-147">getButton</span></span>](buttongroup-getbutton.md) | <span data-ttu-id="3d768-148">使用指定的索引來抓取 **BUTTONELEMENT** 。</span><span class="sxs-lookup"><span data-stu-id="3d768-148">Retrieves the **BUTTONELEMENT** with the specified index.</span></span>                                       |



 

<span data-ttu-id="3d768-149">**BUTTONGROUP** 元素支援環境屬性，並可執行環境事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="3d768-149">The **BUTTONGROUP** element supports the ambient attributes and can implement the ambient event handlers.</span></span> <span data-ttu-id="3d768-150">如需詳細資訊，請參閱 [環境屬性](ambient-attributes.md) 和 [環境事件處理常式](ambient-event-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="3d768-150">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d768-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="3d768-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d768-152">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="3d768-152">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




