---
title: LISTBOX 元素
description: LISTBOX 元素
ms.assetid: b83ba0cb-1838-494d-b4cb-55b4da18a038
keywords:
- Windows Media Player 的外觀、LISTBOX 元素
- 外觀，LISTBOX 元素
- LISTBOX 元素
- 外觀、LISTBOX 元素的參考
- 元素，LISTBOX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d9566d11586e995b289a0048dacb29a91921b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021235"
---
# <a name="listbox-element"></a><span data-ttu-id="5e340-108">LISTBOX 元素</span><span class="sxs-lookup"><span data-stu-id="5e340-108">LISTBOX Element</span></span>

<span data-ttu-id="5e340-109">**LISTBOX** 元素提供一種方式，讓使用者從清單中選取專案。</span><span class="sxs-lookup"><span data-stu-id="5e340-109">The **LISTBOX** element provides a way for users to select items from a list.</span></span> <span data-ttu-id="5e340-110">您可以使用 **ITEM 專案** 做為 **LISTBOX** 專案的子系，以指定這些專案。</span><span class="sxs-lookup"><span data-stu-id="5e340-110">These items can be specified by using **ITEM** elements as children of the **LISTBOX** element.</span></span> <span data-ttu-id="5e340-111">如果您需要只在需要時才顯示的清單方塊控制項，請使用 **popup** 元素，這與 **LISTBOX** 元素相同，但 **popup** 屬性的預設值除外，後者會指定其顯示行為。</span><span class="sxs-lookup"><span data-stu-id="5e340-111">If you need a list box control that is displayed only when needed, use the **POPUP** element, which is identical to the **LISTBOX** element except for the default value of the **popUp** attribute, which dictates its display behavior.</span></span>

<span data-ttu-id="5e340-112">**LISTBOX** 元素支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="5e340-112">The **LISTBOX** element supports the following attributes.</span></span>



| <span data-ttu-id="5e340-113">屬性</span><span class="sxs-lookup"><span data-stu-id="5e340-113">Attribute</span></span>                                        | <span data-ttu-id="5e340-114">描述</span><span class="sxs-lookup"><span data-stu-id="5e340-114">Description</span></span>                                                                                                           |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e340-115">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="5e340-115">backgroundColor</span></span>](listbox-backgroundcolor.md)   | <span data-ttu-id="5e340-116">指定或抓取清單方塊控制項中的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="5e340-116">Specifies or retrieves the background color in the list box control.</span></span>                                                  |
| [<span data-ttu-id="5e340-117">邊境</span><span class="sxs-lookup"><span data-stu-id="5e340-117">border</span></span>](listbox-border.md)                     | <span data-ttu-id="5e340-118">指定或抓取值，指出清單方塊控制項是否有框線。</span><span class="sxs-lookup"><span data-stu-id="5e340-118">Specifies or retrieves a value indicating whether the list box control has a border.</span></span> <span data-ttu-id="5e340-119">只能在設計階段設定。</span><span class="sxs-lookup"><span data-stu-id="5e340-119">Can only be set at design time.</span></span>  |
| [<span data-ttu-id="5e340-120">firstVisibleItem</span><span class="sxs-lookup"><span data-stu-id="5e340-120">firstVisibleItem</span></span>](listbox-firstvisibleitem.md) | <span data-ttu-id="5e340-121">指定或抓取清單方塊控制項中第一個可見行的索引。</span><span class="sxs-lookup"><span data-stu-id="5e340-121">Specifies or retrieves the index of the first visible line in the list box control.</span></span>                                   |
| [<span data-ttu-id="5e340-122">focusItem</span><span class="sxs-lookup"><span data-stu-id="5e340-122">focusItem</span></span>](listbox-focusitem.md)               | <span data-ttu-id="5e340-123">指定或抓取包含焦點的行。</span><span class="sxs-lookup"><span data-stu-id="5e340-123">Specifies or retrieves the line that contains focus.</span></span>                                                                  |
| [<span data-ttu-id="5e340-124">fontFace</span><span class="sxs-lookup"><span data-stu-id="5e340-124">fontFace</span></span>](listbox-fontface.md)                 | <span data-ttu-id="5e340-125">指定或抓取清單方塊控制項的字型。</span><span class="sxs-lookup"><span data-stu-id="5e340-125">Specifies or retrieves the font for the list box control.</span></span>                                                             |
| [<span data-ttu-id="5e340-126">fontSize</span><span class="sxs-lookup"><span data-stu-id="5e340-126">fontSize</span></span>](listbox-fontsize.md)                 | <span data-ttu-id="5e340-127">指定或抓取清單方塊控制項的字型大小。</span><span class="sxs-lookup"><span data-stu-id="5e340-127">Specifies or retrieves the font size for the list box control.</span></span>                                                        |
| [<span data-ttu-id="5e340-128">fontStyle</span><span class="sxs-lookup"><span data-stu-id="5e340-128">fontStyle</span></span>](listbox-fontstyle.md)               | <span data-ttu-id="5e340-129">指定或抓取清單方塊控制項的字型樣式。</span><span class="sxs-lookup"><span data-stu-id="5e340-129">Specifies or retrieves the font style for the list box control.</span></span>                                                       |
| [<span data-ttu-id="5e340-130">foregroundColor</span><span class="sxs-lookup"><span data-stu-id="5e340-130">foregroundColor</span></span>](listbox-foregroundcolor.md)   | <span data-ttu-id="5e340-131">指定或抓取清單方塊控制項中的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="5e340-131">Specifies or retrieves the text color in the list box control.</span></span>                                                        |
| [<span data-ttu-id="5e340-132">itemCount</span><span class="sxs-lookup"><span data-stu-id="5e340-132">itemCount</span></span>](listbox-itemcount.md)               | <span data-ttu-id="5e340-133">捕獲清單方塊控制項中的專案數。</span><span class="sxs-lookup"><span data-stu-id="5e340-133">Retrieves the number of items in the list box control.</span></span>                                                                |
| [<span data-ttu-id="5e340-134">多</span><span class="sxs-lookup"><span data-stu-id="5e340-134">multiSelect</span></span>](listbox-multiselect.md)           | <span data-ttu-id="5e340-135">指定或抓取值，指出使用者是否可以選取多行。</span><span class="sxs-lookup"><span data-stu-id="5e340-135">Specifies or retrieves a value indicating whether the user can select multiple lines.</span></span> <span data-ttu-id="5e340-136">只能在設計階段設定。</span><span class="sxs-lookup"><span data-stu-id="5e340-136">Can only be set at design time.</span></span> |
| [<span data-ttu-id="5e340-137">彈出</span><span class="sxs-lookup"><span data-stu-id="5e340-137">popUp</span></span>](listbox-popup.md)                       | <span data-ttu-id="5e340-138">指定值，這個值表示專案是否代表 popup 或清單方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="5e340-138">Specifies a value indicating whether the element represents a popup or list box control.</span></span>                              |
| [<span data-ttu-id="5e340-139">readOnly</span><span class="sxs-lookup"><span data-stu-id="5e340-139">readOnly</span></span>](listbox-readonly.md)                 | <span data-ttu-id="5e340-140">指定或抓取值，指出文字是否為唯讀或可由使用者選取的文字。</span><span class="sxs-lookup"><span data-stu-id="5e340-140">Specifies or retrieves a value indicating whether text is read-only or text can be selected by the user.</span></span>              |
| [<span data-ttu-id="5e340-141">selectedItem</span><span class="sxs-lookup"><span data-stu-id="5e340-141">selectedItem</span></span>](listbox-selecteditem.md)         | <span data-ttu-id="5e340-142">指定或抓取清單方塊控制項中所選取專案的索引。</span><span class="sxs-lookup"><span data-stu-id="5e340-142">Specifies or retrieves the index of the item selected in the list box control.</span></span>                                        |
| [<span data-ttu-id="5e340-143">排序</span><span class="sxs-lookup"><span data-stu-id="5e340-143">sorted</span></span>](listbox-sorted.md)                     | <span data-ttu-id="5e340-144">指定或抓取值，指出清單方塊控制項是否依照字母順序排序。</span><span class="sxs-lookup"><span data-stu-id="5e340-144">Specifies or retrieves a value indicating whether the list box control is sorted alphabetically.</span></span>                      |



 

<span data-ttu-id="5e340-145">**LISTBOX** 元素支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="5e340-145">The **LISTBOX** element supports the following methods.</span></span>



| <span data-ttu-id="5e340-146">方法</span><span class="sxs-lookup"><span data-stu-id="5e340-146">Method</span></span>                                                 | <span data-ttu-id="5e340-147">描述</span><span class="sxs-lookup"><span data-stu-id="5e340-147">Description</span></span>                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e340-148">appendItem</span><span class="sxs-lookup"><span data-stu-id="5e340-148">appendItem</span></span>](listbox-appenditem.md)                   | <span data-ttu-id="5e340-149">在清單方塊控制項的結尾插入新的文字。</span><span class="sxs-lookup"><span data-stu-id="5e340-149">Inserts new text at the end of the list box control.</span></span>                                                                  |
| [<span data-ttu-id="5e340-150">deleteAll</span><span class="sxs-lookup"><span data-stu-id="5e340-150">deleteAll</span></span>](listbox-deleteall.md)                     | <span data-ttu-id="5e340-151">刪除清單方塊控制項中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="5e340-151">Deletes all items from the list box control.</span></span>                                                                          |
| [<span data-ttu-id="5e340-152">deleteItem</span><span class="sxs-lookup"><span data-stu-id="5e340-152">deleteItem</span></span>](listbox-deleteitem.md)                   | <span data-ttu-id="5e340-153">刪除指定索引處的清單方塊控制項專案。</span><span class="sxs-lookup"><span data-stu-id="5e340-153">Deletes the list box control item at the specified index.</span></span>                                                             |
| [<span data-ttu-id="5e340-154">解雇</span><span class="sxs-lookup"><span data-stu-id="5e340-154">dismiss</span></span>](listbox-dismiss.md)                         | <span data-ttu-id="5e340-155">隱藏控制項。</span><span class="sxs-lookup"><span data-stu-id="5e340-155">Hides the control.</span></span>                                                                                                    |
| [<span data-ttu-id="5e340-156">findItem</span><span class="sxs-lookup"><span data-stu-id="5e340-156">findItem</span></span>](listbox-finditem.md)                       | <span data-ttu-id="5e340-157">從指定的專案索引後面的專案開始搜尋指定的字串。</span><span class="sxs-lookup"><span data-stu-id="5e340-157">Searches for a given string starting with the item following the specified item index.</span></span>                                |
| [<span data-ttu-id="5e340-158">getItem</span><span class="sxs-lookup"><span data-stu-id="5e340-158">getItem</span></span>](listbox-getitem.md)                         | <span data-ttu-id="5e340-159">使用指定的索引，抓取專案的文字。</span><span class="sxs-lookup"><span data-stu-id="5e340-159">Retrieves the text for the item with the specified index.</span></span>                                                             |
| [<span data-ttu-id="5e340-160">getNextSelectedItem</span><span class="sxs-lookup"><span data-stu-id="5e340-160">getNextSelectedItem</span></span>](listbox-getnextselecteditem.md) | <span data-ttu-id="5e340-161">從具有指定索引之專案之後的專案開始，從清單方塊控制項中取出下一個選取的專案。</span><span class="sxs-lookup"><span data-stu-id="5e340-161">Retrieves the next selected item in the list box control starting at the item after the one with the specified index.</span></span> |
| [<span data-ttu-id="5e340-162">insertItem</span><span class="sxs-lookup"><span data-stu-id="5e340-162">insertItem</span></span>](listbox-insertitem.md)                   | <span data-ttu-id="5e340-163">將指定的文字插入清單方塊控制項中的指定索引處。</span><span class="sxs-lookup"><span data-stu-id="5e340-163">Inserts the specified text at the specified index in the list box control.</span></span>                                            |
| [<span data-ttu-id="5e340-164">replaceItem</span><span class="sxs-lookup"><span data-stu-id="5e340-164">replaceItem</span></span>](listbox-replaceitem.md)                 | <span data-ttu-id="5e340-165">以指定的文字取代指定索引處的文字。</span><span class="sxs-lookup"><span data-stu-id="5e340-165">Replaces the text at the specified index with the specified text.</span></span>                                                     |
| [<span data-ttu-id="5e340-166">setSelectedState</span><span class="sxs-lookup"><span data-stu-id="5e340-166">setSelectedState</span></span>](listbox-setselectedstate.md)       | <span data-ttu-id="5e340-167">選取或取消選取具有指定索引的專案。</span><span class="sxs-lookup"><span data-stu-id="5e340-167">Selects or unselects the item with the specified index.</span></span>                                                               |
| [<span data-ttu-id="5e340-168">show</span><span class="sxs-lookup"><span data-stu-id="5e340-168">show</span></span>](listbox-show.md)                               | <span data-ttu-id="5e340-169">顯示控制項。</span><span class="sxs-lookup"><span data-stu-id="5e340-169">Displays the control.</span></span>                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="5e340-170">此元素需要 Windows XP 或更新版本的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="5e340-170">This element requires Windows Media Player for Windows XP or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5e340-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="5e340-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e340-172">**POPUP 元素**</span><span class="sxs-lookup"><span data-stu-id="5e340-172">**POPUP Element**</span></span>](popup-element.md)
</dt> <dt>

[<span data-ttu-id="5e340-173">**外觀程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="5e340-173">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




