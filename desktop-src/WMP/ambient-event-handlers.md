---
title: 環境事件處理常式
description: 環境事件處理常式
ms.assetid: ec806b92-a66d-499d-9bb3-cea7e82676bb
keywords:
- Windows Media Player 的外觀、環境事件處理常式
- 外觀，環境事件處理常式
- 外觀、環境事件處理常式的參考
- 環境事件處理常式
- 事件，環境
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc05cf90956464afbb030f3cd5dc4af194b0da2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371967"
---
# <a name="ambient-event-handlers"></a><span data-ttu-id="c041c-108">環境事件處理常式</span><span class="sxs-lookup"><span data-stu-id="c041c-108">Ambient Event Handlers</span></span>

<span data-ttu-id="c041c-109">下列事件處理常式可以針對大部分的外觀元素來執行。</span><span class="sxs-lookup"><span data-stu-id="c041c-109">The following event handlers can be implemented for most skin elements.</span></span> <span data-ttu-id="c041c-110">使用 **事件** 關鍵字存取的環境事件屬性，可以在事件處理常式中使用，以判斷在事件發生時的鍵盤和滑鼠狀態。</span><span class="sxs-lookup"><span data-stu-id="c041c-110">The ambient event attributes accessed with the **event** keyword can be used within an event handler to determine the state of the keyboard and mouse at the time of the event.</span></span>



| <span data-ttu-id="c041c-111">事件處理常式</span><span class="sxs-lookup"><span data-stu-id="c041c-111">Event handler</span></span>                                   | <span data-ttu-id="c041c-112">Description</span><span class="sxs-lookup"><span data-stu-id="c041c-112">Description</span></span>                                                                                                                                                                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c041c-113">*屬性* \_onchange</span><span class="sxs-lookup"><span data-stu-id="c041c-113">*attribute*\_onchange</span></span>](attribute-onchange.md) | <span data-ttu-id="c041c-114">當外觀屬性變更值時，就會發生事件處理常式可以處理的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-114">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="c041c-115">事件處理常式的名稱是屬性的名稱，後面接著底線和 "onchange"，例如「值 \_ onchange」。</span><span class="sxs-lookup"><span data-stu-id="c041c-115">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span> |
| [<span data-ttu-id="c041c-116">onblur</span><span class="sxs-lookup"><span data-stu-id="c041c-116">onblur</span></span>](onblur.md)                            | <span data-ttu-id="c041c-117">處理當元素失去鍵盤焦點時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-117">Handles an event that occurs when the element loses the keyboard focus.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="c041c-118">onclick</span><span class="sxs-lookup"><span data-stu-id="c041c-118">onclick</span></span>](onclick.md)                          | <span data-ttu-id="c041c-119">處理當使用者按一下專案時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-119">Handles an event that occurs when the user clicks the element.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="c041c-120">ondblclick</span><span class="sxs-lookup"><span data-stu-id="c041c-120">ondblclick</span></span>](ondblclick.md)                    | <span data-ttu-id="c041c-121">處理使用者按兩下元素時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-121">Handles an event that occurs when the user double-clicks the element.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="c041c-122">onendAlphablend</span><span class="sxs-lookup"><span data-stu-id="c041c-122">onendalphablend</span></span>](onendalphablend.md)          | <span data-ttu-id="c041c-123">處理元素完成 **AlphaBlendTo** 作業時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-123">Handles an event that occurs when an element completes an **alphaBlendTo** operation.</span></span>                                                                                                                                         |
| [<span data-ttu-id="c041c-124">onendmove</span><span class="sxs-lookup"><span data-stu-id="c041c-124">onendmove</span></span>](onendmove.md)                      | <span data-ttu-id="c041c-125">處理元素完成 **moveTo** 作業時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-125">Handles an event that occurs when an element completes a **moveTo** operation.</span></span>                                                                                                                                                |
| [<span data-ttu-id="c041c-126">onfocus</span><span class="sxs-lookup"><span data-stu-id="c041c-126">onfocus</span></span>](onfocus.md)                          | <span data-ttu-id="c041c-127">處理當元素收到鍵盤焦點時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-127">Handles an event that occurs when the element receives the keyboard focus.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="c041c-128">onkeydown</span><span class="sxs-lookup"><span data-stu-id="c041c-128">onkeydown</span></span>](onkeydown.md)                      | <span data-ttu-id="c041c-129">處理按下按鍵時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-129">Handles an event that occurs when a key is pressed.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="c041c-130">onkeypress</span><span class="sxs-lookup"><span data-stu-id="c041c-130">onkeypress</span></span>](onkeypress.md)                    | <span data-ttu-id="c041c-131">處理使用者按下英數位鍵時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-131">Handles an event that occurs when the user presses an alphanumeric key.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="c041c-132">onkeyup</span><span class="sxs-lookup"><span data-stu-id="c041c-132">onkeyup</span></span>](onkeyup.md)                          | <span data-ttu-id="c041c-133">處理釋放金鑰時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-133">Handles an event that occurs when a key is released.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="c041c-134">onmousedown</span><span class="sxs-lookup"><span data-stu-id="c041c-134">onmousedown</span></span>](onmousedown.md)                  | <span data-ttu-id="c041c-135">處理當使用者按一下滑鼠按鍵時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-135">Handles an event that occurs when the user clicks a mouse button.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="c041c-136"></span><span class="sxs-lookup"><span data-stu-id="c041c-136">onmousemove</span></span>](onmousemove.md)                  | <span data-ttu-id="c041c-137">處理當使用者在專案上方移動滑鼠指標時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-137">Handles an event that occurs when the user moves the mouse pointer while it is over an element.</span></span>                                                                                                                               |
| [<span data-ttu-id="c041c-138">onmouseout</span><span class="sxs-lookup"><span data-stu-id="c041c-138">onmouseout</span></span>](onmouseout.md)                    | <span data-ttu-id="c041c-139">處理當使用者將指標移出元素時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-139">Handles an event that occurs when the user moves the pointer off the element.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="c041c-140">onmouseover</span><span class="sxs-lookup"><span data-stu-id="c041c-140">onmouseover</span></span>](onmouseover.md)                  | <span data-ttu-id="c041c-141">處理使用者第一次將指標放在元素上時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-141">Handles an event that occurs when the user first places the pointer over the element.</span></span>                                                                                                                                         |
| [<span data-ttu-id="c041c-142">onmouseup</span><span class="sxs-lookup"><span data-stu-id="c041c-142">onmouseup</span></span>](onmouseup.md)                      | <span data-ttu-id="c041c-143">處理當滑鼠指標在專案上方時，當使用者放開滑鼠按鍵時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-143">Handles an event that occurs when the user releases a mouse button while the pointer is over the element.</span></span>                                                                                                                     |
| [<span data-ttu-id="c041c-144">onresize</span><span class="sxs-lookup"><span data-stu-id="c041c-144">onresize</span></span>](onresize.md)                        | <span data-ttu-id="c041c-145">處理控制項調整時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c041c-145">Handles an event that occurs when a control resizes.</span></span>                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="c041c-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="c041c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c041c-147">**環境事件屬性**</span><span class="sxs-lookup"><span data-stu-id="c041c-147">**Ambient Event Attributes**</span></span>](ambient-event-attributes.md)
</dt> <dt>

[<span data-ttu-id="c041c-148">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="c041c-148">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




