---
title: 環境事件屬性
description: 環境事件屬性
ms.assetid: 56cd2701-53b3-4456-8fcd-d65f8a6aefd7
keywords:
- Windows Media Player 的外觀、環境事件屬性
- 外觀，環境事件屬性
- 外觀、環境事件屬性的參考
- 環境事件屬性
- 屬性，環境事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40522a741509e56d2e4c9201c305126067a0fe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672023"
---
# <a name="ambient-event-attributes"></a><span data-ttu-id="346b8-108">環境事件屬性</span><span class="sxs-lookup"><span data-stu-id="346b8-108">Ambient Event Attributes</span></span>

<span data-ttu-id="346b8-109">下列屬性通用於所有的外觀事件。</span><span class="sxs-lookup"><span data-stu-id="346b8-109">The following attributes are common to all skin events.</span></span> <span data-ttu-id="346b8-110">您可以使用專案的事件處理常式內的 **事件** 關鍵字來存取它們。</span><span class="sxs-lookup"><span data-stu-id="346b8-110">They are accessed with the **event** keyword within an event handler for the element.</span></span>



| <span data-ttu-id="346b8-111">屬性</span><span class="sxs-lookup"><span data-stu-id="346b8-111">Attribute</span></span>                              | <span data-ttu-id="346b8-112">描述</span><span class="sxs-lookup"><span data-stu-id="346b8-112">Description</span></span>                                                                                                  |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="346b8-113">altKey</span><span class="sxs-lookup"><span data-stu-id="346b8-113">altKey</span></span>](event-altkey.md)             | <span data-ttu-id="346b8-114">抓取值，指出在事件發生時，ALT 鍵是否已關閉。</span><span class="sxs-lookup"><span data-stu-id="346b8-114">Retrieves a value indicating whether the ALT key was down when the event occurred.</span></span>                           |
| [<span data-ttu-id="346b8-115">按鈕</span><span class="sxs-lookup"><span data-stu-id="346b8-115">button</span></span>](event-button.md)             | <span data-ttu-id="346b8-116">抓取值，指出在事件發生時哪一個滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="346b8-116">Retrieves a value indicating which mouse buttons were down when the event occurred.</span></span>                          |
| [<span data-ttu-id="346b8-117">clientX</span><span class="sxs-lookup"><span data-stu-id="346b8-117">clientX</span></span>](event-clientx.md)           | <span data-ttu-id="346b8-118">針對應用程式視窗的用戶端區域，抓取滑鼠指標的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="346b8-118">Retrieves the x-coordinate of the mouse pointer with respect to the client region of the application window.</span></span> |
| [<span data-ttu-id="346b8-119">clientY</span><span class="sxs-lookup"><span data-stu-id="346b8-119">clientY</span></span>](event-clienty.md)           | <span data-ttu-id="346b8-120">根據應用程式視窗的用戶端區域，抓取滑鼠指標的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="346b8-120">Retrieves the y-coordinate of the mouse pointer with respect to the client region of the application window.</span></span> |
| [<span data-ttu-id="346b8-121">ctrlKey</span><span class="sxs-lookup"><span data-stu-id="346b8-121">ctrlKey</span></span>](event-ctrlkey.md)           | <span data-ttu-id="346b8-122">抓取值，指出在事件發生時，CTRL 鍵是否已關閉。</span><span class="sxs-lookup"><span data-stu-id="346b8-122">Retrieves a value indicating whether the CTRL key was down when the event occurred.</span></span>                          |
| [<span data-ttu-id="346b8-123">fromElement</span><span class="sxs-lookup"><span data-stu-id="346b8-123">fromElement</span></span>](event-fromelement.md)   | <span data-ttu-id="346b8-124">抓取事件來自的元素。</span><span class="sxs-lookup"><span data-stu-id="346b8-124">Retrieves the element the event came from.</span></span>                                                                   |
| [<span data-ttu-id="346b8-125">keyCode</span><span class="sxs-lookup"><span data-stu-id="346b8-125">keyCode</span></span>](event-keycode.md)           | <span data-ttu-id="346b8-126">當事件發生時，如果按鍵已按下，則抓取 ASCII 按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="346b8-126">Retrieves the ASCII key code if a key was pressed when the event occurred.</span></span>                                   |
| [<span data-ttu-id="346b8-127">offsetX</span><span class="sxs-lookup"><span data-stu-id="346b8-127">offsetX</span></span>](event-offsetx.md)           | <span data-ttu-id="346b8-128">抓取滑鼠指標的 x 座標（相對於引發事件的元素）。</span><span class="sxs-lookup"><span data-stu-id="346b8-128">Retrieves the x-coordinate of the mouse pointer with respect to the element firing the event.</span></span>                |
| [<span data-ttu-id="346b8-129">offsetY</span><span class="sxs-lookup"><span data-stu-id="346b8-129">offsetY</span></span>](event-offsety.md)           | <span data-ttu-id="346b8-130">抓取滑鼠指標相對於引發事件之元素的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="346b8-130">Retrieves the y-coordinate of the mouse pointer with respect to the element firing the event.</span></span>                |
| [<span data-ttu-id="346b8-131">screenHeight</span><span class="sxs-lookup"><span data-stu-id="346b8-131">screenHeight</span></span>](event-screenheight.md) | <span data-ttu-id="346b8-132">抓取可用螢幕大小的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="346b8-132">Retrieves the height of the available screen size in pixels.</span></span>                                                 |
| [<span data-ttu-id="346b8-133">screenWidth</span><span class="sxs-lookup"><span data-stu-id="346b8-133">screenWidth</span></span>](event-screenwidth.md)   | <span data-ttu-id="346b8-134">抓取可用螢幕大小的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="346b8-134">Retrieves the width of the available screen size in pixels.</span></span>                                                  |
| [<span data-ttu-id="346b8-135">screenX</span><span class="sxs-lookup"><span data-stu-id="346b8-135">screenX</span></span>](event-screenx.md)           | <span data-ttu-id="346b8-136">抓取滑鼠指標相對於螢幕的絕對 x 座標。</span><span class="sxs-lookup"><span data-stu-id="346b8-136">Retrieves the absolute x-coordinate of the mouse pointer with respect to the screen.</span></span>                         |
| [<span data-ttu-id="346b8-137">screenY</span><span class="sxs-lookup"><span data-stu-id="346b8-137">screenY</span></span>](event-screeny.md)           | <span data-ttu-id="346b8-138">抓取滑鼠指標相對於螢幕的絕對 y 座標。</span><span class="sxs-lookup"><span data-stu-id="346b8-138">Retrieves the absolute y-coordinate of the mouse pointer with respect to the screen.</span></span>                         |
| [<span data-ttu-id="346b8-139">shiftKey</span><span class="sxs-lookup"><span data-stu-id="346b8-139">shiftKey</span></span>](event-shiftkey.md)         | <span data-ttu-id="346b8-140">抓取值，指出在事件發生時，SHIFT 鍵是否已關閉。</span><span class="sxs-lookup"><span data-stu-id="346b8-140">Retrieves a value indicating whether the SHIFT key was down when the event occurred.</span></span>                         |
| [<span data-ttu-id="346b8-141">srcElement</span><span class="sxs-lookup"><span data-stu-id="346b8-141">srcElement</span></span>](event-srcelement.md)     | <span data-ttu-id="346b8-142">捕獲引發事件的元素。</span><span class="sxs-lookup"><span data-stu-id="346b8-142">Retrieves the element that fired the event.</span></span>                                                                  |
| [<span data-ttu-id="346b8-143">toElement</span><span class="sxs-lookup"><span data-stu-id="346b8-143">toElement</span></span>](event-toelement.md)       | <span data-ttu-id="346b8-144">抓取鍵盤焦點移至的元素。</span><span class="sxs-lookup"><span data-stu-id="346b8-144">Retrieves the element the keyboard focus moved to.</span></span>                                                           |
| [<span data-ttu-id="346b8-145">x</span><span class="sxs-lookup"><span data-stu-id="346b8-145">x</span></span>](event-x.md)                       | <span data-ttu-id="346b8-146">抓取與應用程式視窗相關之滑鼠指標的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="346b8-146">Retrieves the x-coordinate of the mouse pointer with respect to the application window.</span></span>                      |
| [<span data-ttu-id="346b8-147">y</span><span class="sxs-lookup"><span data-stu-id="346b8-147">y</span></span>](event-y.md)                       | <span data-ttu-id="346b8-148">抓取滑鼠指標相對於應用程式視窗的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="346b8-148">Retrieves the y-coordinate of the mouse pointer with respect to the application window.</span></span>                      |



 

## <a name="related-topics"></a><span data-ttu-id="346b8-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="346b8-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="346b8-150">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="346b8-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




