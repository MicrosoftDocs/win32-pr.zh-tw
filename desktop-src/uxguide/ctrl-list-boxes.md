---
title: 清單方塊
description: 使用清單方塊時，使用者可以從一律可見清單中顯示的一組值中進行選取。
ms.assetid: 620e9ff9-b367-446b-9e97-9c9d6d14f4bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 3db0bbb07ed6cea18b7d8fb29fd4e329840590d5
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321420"
---
# <a name="list-boxes"></a><span data-ttu-id="f8e6c-103">清單方塊</span><span class="sxs-lookup"><span data-stu-id="f8e6c-103">List Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="f8e6c-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="f8e6c-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="f8e6c-106">使用清單方塊時，使用者可以從一律可見清單中顯示的一組值中進行選取。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-106">With a list box, users can select from a set of values presented in a list that is always visible.</span></span> <span data-ttu-id="f8e6c-107">使用單一選取清單方塊時，使用者會從互斥值清單中選取一個專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-107">With a single-selection list box, users select one item from a list of mutually exclusive values.</span></span> <span data-ttu-id="f8e6c-108">使用多重選取清單方塊時，使用者會從值清單中選取零個以上的專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-108">With a multiple-selection list box, users select zero or more items from a list of values.</span></span>

![<span data-ttu-id="f8e6c-109">單一選取清單方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f8e6c-109">screen shot of single-selection list box</span></span> ](images/ctrl-list-boxes-image1.png)

<span data-ttu-id="f8e6c-110">典型的單一選取清單方塊。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-110">A typical single-selection list box.</span></span>

> [!Note]  
> <span data-ttu-id="f8e6c-111">與 [版面](vis-layout.md) 配置和 [清單視圖](ctrl-list-views.md) 相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-111">Guidelines related to [layout](vis-layout.md) and [list views](ctrl-list-views.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="f8e6c-112">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="f8e6c-112">Is this the right control?</span></span>

<span data-ttu-id="f8e6c-113">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="f8e6c-113">To decide, consider these questions:</span></span>

-   <span data-ttu-id="f8e6c-114">**清單是否會顯示資料，而不是程式選項？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-114">**Does the list present data, rather than program options?**</span></span> <span data-ttu-id="f8e6c-115">無論是哪一種方式，清單方塊都是合適的選擇，無論專案數為何。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-115">Either way, a list box is a suitable choice regardless of the number of items.</span></span> <span data-ttu-id="f8e6c-116">相較之下， [選項按鈕](ctrl-radio-buttons.md) 或 [核取方塊](ctrl-check-boxes.md) 僅適用于少數的程式選項。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-116">By contrast, [radio buttons](ctrl-radio-buttons.md) or [check boxes](ctrl-check-boxes.md) are suitable only for a small number of program options.</span></span>
-   <span data-ttu-id="f8e6c-117">**使用者是否需要變更視圖、群組、依資料行排序，或變更資料行的寬度和順序？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-117">**Do users need to change views, group, sort by columns, or change column widths and order?**</span></span> <span data-ttu-id="f8e6c-118">若是如此，請改用 [清單視圖](ctrl-list-views.md) 。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-118">If so, use a [list view](ctrl-list-views.md) instead.</span></span>
-   <span data-ttu-id="f8e6c-119">**控制項必須是拖曳來源或放置目標？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-119">**Does the control need to be a drag source or a drop target?**</span></span> <span data-ttu-id="f8e6c-120">若是如此，請改用清單視圖。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-120">If so, use a list view instead.</span></span>
-   <span data-ttu-id="f8e6c-121">**是否需要將清單專案複製到剪貼簿或從剪貼簿貼上？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-121">**Do the list items need to be copied to or pasted from the clipboard?**</span></span> <span data-ttu-id="f8e6c-122">若是如此，請改用清單視圖。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-122">If so, use a list view instead.</span></span>

<span data-ttu-id="f8e6c-123">**單一選取清單**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-123">**Single-selection lists**</span></span>

-   <span data-ttu-id="f8e6c-124">**控制項是否可用來從互斥值清單中選擇一個選項？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-124">**Is the control used to choose one option from a list of mutually exclusive values?**</span></span> <span data-ttu-id="f8e6c-125">如果不是，請使用其他控制項。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-125">If not, use another control.</span></span> <span data-ttu-id="f8e6c-126">若要選擇多個選項，請改為使用標準的多重選取清單、核取方塊清單、清單產生器或新增/移除清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-126">To choose multiple options, use a standard multiple-selection list, check box list, list builder, or add/remove list instead.</span></span>
-   <span data-ttu-id="f8e6c-127">**大部分的使用者在大多數情況下，是否有建議使用的預設選項？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-127">**Is there a default option that is recommended for most users in most situations?**</span></span> <span data-ttu-id="f8e6c-128">看到選取的選項遠比看到替代方案更重要嗎？</span><span class="sxs-lookup"><span data-stu-id="f8e6c-128">Is seeing the selected option far more important than seeing the alternatives?</span></span> <span data-ttu-id="f8e6c-129">如果是的話，請考慮使用下拉式清單，如果您不想要讓使用者藉由隱藏替代方案來進行變更，請考慮使用 [下拉式清單](/windows/desktop/uxguide/ctrl-drop) 。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-129">If so, consider using a [drop-down list](/windows/desktop/uxguide/ctrl-drop) if you don't want to encourage users to make changes by hiding the alternatives.</span></span>

![<span data-ttu-id="f8e6c-130">最高品質作為預設按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f8e6c-130">screen shot of highest quality as default button</span></span> ](images/ctrl-list-boxes-image2.png)

<span data-ttu-id="f8e6c-131">在此範例中，最高的色彩品質是大部分使用者的最佳選擇，因此下拉式清單是把替代方案的理想選擇。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-131">In this example, the highest color quality is the best choice for most users, so a drop-down list is a good choice to downplay the alternatives.</span></span>

-   <span data-ttu-id="f8e6c-132">**清單需要持續互動嗎？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-132">**Does the list require constant interaction?**</span></span> <span data-ttu-id="f8e6c-133">若是如此，請使用單一選取清單來簡化互動。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-133">If so, use a single-selection list to simplify the interaction.</span></span>

![<span data-ttu-id="f8e6c-134">選項清單的螢幕擷取畫面，例如純文字</span><span class="sxs-lookup"><span data-stu-id="f8e6c-134">screen shot of list of options such as plain text</span></span> ](images/ctrl-list-boxes-image3.png)

<span data-ttu-id="f8e6c-135">在此範例中，使用者會不斷地變更 [顯示專案] 清單中選取的專案，以設定前景和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-135">In this example, users are constantly changing the selected item in the Display items list to set the foreground and background colors.</span></span> <span data-ttu-id="f8e6c-136">在此情況下，使用下拉式清單相當繁瑣。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-136">Using a drop-down list in this case would be very tedious.</span></span>

-   <span data-ttu-id="f8e6c-137">**設定看起來像相對數量嗎？使用者是否能從立即的意見反應中獲益** 于設定變更的影響？</span><span class="sxs-lookup"><span data-stu-id="f8e6c-137">**Does the setting seem like a relative quantity?Would users benefit from instant feedback** on the effect of setting changes?</span></span> <span data-ttu-id="f8e6c-138">如果是的話，請考慮改用 [滑杆](ctrl-sliders.md) 。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-138">If so, consider using a [slider](ctrl-sliders.md) instead.</span></span>
-   <span data-ttu-id="f8e6c-139">**清單專案之間是否有重要的階層式關聯性？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-139">**Is there a significant hierarchical relationship between the list items?**</span></span> <span data-ttu-id="f8e6c-140">如果是的話，請改用 [樹狀檢視](ctrl-tree-views.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-140">If so, use a [tree view](ctrl-tree-views.md) control instead.</span></span>
-   <span data-ttu-id="f8e6c-141">**螢幕空間是否在 premium？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-141">**Is screen space at a premium?**</span></span> <span data-ttu-id="f8e6c-142">如果是的話，請改用下拉式清單，因為使用的螢幕空間是固定的，而且與清單專案的數目無關。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-142">If so, use a drop-down list instead because the screen space used is fixed and independent of the number of list items.</span></span>

<span data-ttu-id="f8e6c-143">**標準多重選取清單和核取方塊清單**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-143">**Standard multiple-selection lists and check box lists**</span></span>

-   <span data-ttu-id="f8e6c-144">**這項工作或通常使用的是多重選取專案嗎？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-144">**Is multiple selection essential to the task or commonly used?**</span></span> <span data-ttu-id="f8e6c-145">如果是的話，請使用核取方塊清單讓多個選取明顯，尤其是當您的目標使用者不是 advanced。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-145">If so, use a check box list to make multiple selection obvious, especially if your target users aren't advanced.</span></span> <span data-ttu-id="f8e6c-146">許多使用者都不知道標準的多重選取清單支援多重選取。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-146">Many users won't realize that a standard multiple-selection list supports multiple selection.</span></span> <span data-ttu-id="f8e6c-147">如果核取方塊會對多個選取專案造成太多的注意，或造成太多螢幕雜亂，請使用標準的多重選取清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-147">Use a standard multiple-selection list if the check boxes would draw too much attention to multiple selection or result in too much screen clutter.</span></span>
-   <span data-ttu-id="f8e6c-148">**多重選取專案的穩定性是否重要？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-148">**Is the stability of the multiple selection important?**</span></span> <span data-ttu-id="f8e6c-149">如果是的話，請使用核取方塊清單、清單產生器或新增/移除清單，因為按一下一次只變更一個專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-149">If so, use a check box list, list builder, or add/remove list because clicking changes only a single item at a time.</span></span> <span data-ttu-id="f8e6c-150">使用標準的多重選取清單時，很容易就能清除所有選取專案，即使是意外的。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-150">With a standard multiple selection list, it's very easy to clear all the selections even by accident.</span></span>
-   <span data-ttu-id="f8e6c-151">**控制項是否可用來從值清單中選擇零個以上的專案？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-151">**Is the control used to choose zero or more items from a list of values?**</span></span> <span data-ttu-id="f8e6c-152">如果不是，請使用其他控制項。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-152">If not, use another control.</span></span> <span data-ttu-id="f8e6c-153">若要選擇一個專案，請改為使用單一選取清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-153">For choosing one item, use a single-selection list instead.</span></span>

<span data-ttu-id="f8e6c-154">**預覽清單**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-154">**Preview lists**</span></span>

-   <span data-ttu-id="f8e6c-155">**使用影像選取的選項是否比單獨使用文字更容易？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-155">**Are the options easier to select with images than with text alone?**</span></span> <span data-ttu-id="f8e6c-156">若是如此，請使用預覽清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-156">If so, use a preview list.</span></span>

<span data-ttu-id="f8e6c-157">**列出產生器和新增/移除清單**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-157">**List builders and add/remove lists**</span></span>

-   <span data-ttu-id="f8e6c-158">**控制項是否可用來從值清單中選擇零個以上的專案？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-158">**Is the control used to choose zero or more items from a list of values?**</span></span> <span data-ttu-id="f8e6c-159">如果不是，請使用其他控制項。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-159">If not, use another control.</span></span> <span data-ttu-id="f8e6c-160">若要選擇一個專案，請改為使用單一選取清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-160">For choosing one item, use a single-selection list instead.</span></span>
-   <span data-ttu-id="f8e6c-161">**選取專案的順序是否重要？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-161">**Does the order of the selected items matter?**</span></span> <span data-ttu-id="f8e6c-162">如果是，則清單產生器和新增/移除清單模式支援順序，而其他多重選取模式則不支援。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-162">If so, the list builder and add/remove list patterns support order, whereas the other multiple-selection patterns do not.</span></span>
-   <span data-ttu-id="f8e6c-163">**使用者是否要查看所有選取專案的摘要？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-163">**Is it important for users to see a summary of all the selected items?**</span></span> <span data-ttu-id="f8e6c-164">如果是，清單產生器和新增/移除清單模式只會顯示選取的專案，而其他多重選取模式則不會顯示。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-164">If so, the list builder and add/remove list patterns display only the selected items, whereas the other multiple-selection patterns do not.</span></span>
-   <span data-ttu-id="f8e6c-165">**可能的選擇是否受限制？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-165">**Are the possible choices unconstrained?**</span></span> <span data-ttu-id="f8e6c-166">如果是，請使用 [新增/移除] 清單，讓使用者可以選擇目前不在清單中的值。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-166">If so, use an add/remove list so that users can choose values not currently in the list.</span></span>
-   <span data-ttu-id="f8e6c-167">**將值新增至清單時需要特殊的對話方塊來選擇物件嗎？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-167">**Does adding a value to the list require a specialized dialog box for choosing objects?**</span></span> <span data-ttu-id="f8e6c-168">如果是，請使用 [新增/移除] 清單，並在使用者按一下 [新增] 時顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-168">If so, use an add/remove list and display the dialog box when users click Add.</span></span>
-   <span data-ttu-id="f8e6c-169">**螢幕空間是否在 premium？**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-169">**Is screen space at a premium?**</span></span> <span data-ttu-id="f8e6c-170">若是如此，請改用 [新增/移除] 清單，因為它不一定會顯示一組選項，因此使用較少的螢幕空間。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-170">If so, use an add/remove list instead because it uses less screen space by not always showing the set of options.</span></span>

<span data-ttu-id="f8e6c-171">針對清單方塊， **清單中的專案數目不是選擇控制項的因素** ，因為它們會從上千個專案一直到一個選取清單 (，而不是多重選取清單) 。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-171">For list boxes, **the number of items in the list isn't a factor in choosing the control** because they scale from thousands of items all the way down to one for single-selection lists (and none for multiple-selection lists).</span></span> <span data-ttu-id="f8e6c-172">由於清單方塊可用於資料，因此可能事先不知道專案的數目。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-172">Because list boxes can be used for data, the number of items might not be known in advance.</span></span>

<span data-ttu-id="f8e6c-173">**注意：** 有時候看起來像清單方塊的控制項是使用清單視圖來執行，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-173">**Note:** Sometimes a control that looks like a list box is implemented using a list view and vice versa.</span></span> <span data-ttu-id="f8e6c-174">在這種情況下，請根據使用方式套用指導方針，而不是執行。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-174">In such cases, apply the guidelines based on usage, not implementation.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="f8e6c-175">使用模式</span><span class="sxs-lookup"><span data-stu-id="f8e6c-175">Usage patterns</span></span>

<span data-ttu-id="f8e6c-176">清單方塊有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="f8e6c-176">List boxes have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f8e6c-177"><strong>單一選取清單</strong> 允許使用者一次選取一個專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-177"><strong>Single-selection lists</strong> Allow users to select one item at a time.</span></span> <br/></td>
<td><img src="images/ctrl-list-boxes-image4.png" alt="Screen shot of list box with one item selected " /><br/> <span data-ttu-id="f8e6c-178">在此範例中，使用者只能選取一個顯示專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-178">In this example, users can select only one display item.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8e6c-179"><strong>標準多重選取清單</strong> 允許使用者選取任意數目的專案，包括 [無]。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-179"><strong>Standard multiple-selection lists</strong> Allow users to select any number of items, including none.</span></span><br/></td>
<td><span data-ttu-id="f8e6c-180">標準多重選取清單的外觀與單一選取清單完全相同，因此沒有清單方塊支援多重選取的視覺線索。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-180">Standard multiple-selection lists have exactly the same appearance as single-selection lists, so there is no visual clue that a list box supports multiple selection.</span></span> <span data-ttu-id="f8e6c-181">由於使用者必須探索這項功能，因此這份清單模式最適合用於多個選取專案並不重要的工作，而且很少使用。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-181">Because users have to discover this ability, this list pattern is best used for tasks where multiple selection isn't essential and is rarely used.</span></span> <br/> <span data-ttu-id="f8e6c-182">有兩種不同的多重選取模式： <a href="glossary.md">多個</a> 和 <a href="glossary.md">延伸</a>。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-182">There are two different multiple-selection modes: <a href="glossary.md">multiple</a> and <a href="glossary.md">extended</a>.</span></span> <span data-ttu-id="f8e6c-183"><strong>擴充選取模式</strong> 是最常見的，也就是藉由拖曳或使用 Shift + Click 和 Ctrl + 按一下來分別選取連續和非相鄰值的群組，來擴充選取範圍。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-183"><strong>Extended selection mode</strong> is by far the more common, where the selection can be extended by dragging or with Shift+click and Ctrl+click to select groups of contiguous and non-adjacent values, respectively.</span></span> <span data-ttu-id="f8e6c-184">在 <strong>多重選取模式</strong>中，不論 Shift 和 Ctrl 鍵為何，按一下任何專案都會切換其選取狀態。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-184">In the <strong>multiple-selection mode</strong>, clicking any item toggles its selection state regardless of the Shift and Ctrl keys.</span></span> <span data-ttu-id="f8e6c-185">由於這種不尋常的行為，多重選取模式已被取代，因此您應該改為使用核取方塊清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-185">Given this unusual behavior, multiple-selection mode is deprecated and you should use check box lists instead.</span></span><br/> <img src="images/ctrl-list-boxes-image5.png" alt="Screen shot of list box with several items selected " /><br/> <span data-ttu-id="f8e6c-186">在此範例中，使用者可以使用多重選取模式來選取任意數目的專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-186">In this example, users can select any number of items using the multiple-selection mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8e6c-187"><strong>核取方塊清單</strong> 如同標準的多重選取清單方塊，核取方塊清單可讓使用者選取任意數目的專案，包括 [無]。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-187"><strong>Check box lists</strong> Like standard multiple-selection list boxes, check box lists allow users to select any number of items, including none.</span></span><br/></td>
<td><span data-ttu-id="f8e6c-188">不同于標準的多重選取清單，核取方塊會清楚指出可能會有多個選取專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-188">Unlike standard multiple-selection lists, the check boxes clearly indicate that multiple selection is possible.</span></span> <span data-ttu-id="f8e6c-189">針對需要多重選取的工作，請使用此清單模式。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-189">Use this list pattern for tasks where multiple selection is essential or commonly used.</span></span> <br/> <img src="images/ctrl-list-boxes-image6.png" alt="Screen shot of Toolbars check-box list " /><br/> <span data-ttu-id="f8e6c-190">在此範例中，使用者通常會選取一個以上的專案，因此會使用核取方塊清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-190">In this example, users typically select more than one item so a check box list is used.</span></span><br/> <span data-ttu-id="f8e6c-191">假設有多個選取專案，您可能會假設核取方塊清單最好是標準的多重選取清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-191">Given this clear indication of multiple selection, you might assume that check box lists are preferable to standard multiple-selection lists.</span></span> <span data-ttu-id="f8e6c-192">在實務上，少數工作需要多個選取或大量使用;在這種情況下，使用核取方塊清單會將太多注意力放在選取範圍內。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-192">In practice, few tasks require multiple selection or use it heavily; using a check box list in such cases draws too much attention to selection.</span></span> <span data-ttu-id="f8e6c-193">因此， <strong>標準的多重選取清單更為普遍。</strong></span><span class="sxs-lookup"><span data-stu-id="f8e6c-193">Consequently, <strong>standard multiple-selection lists are far more common.</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8e6c-194"><strong>預覽清單</strong> 可以是單一或多個選取專案，但是會顯示選取範圍（而不只是文字）的預覽效果。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-194"><strong>Preview lists</strong> Can be single or multiple selection, but they show a preview of the effect of the selection rather than just text.</span></span><br/></td>
<td><img src="images/ctrl-list-boxes-image7.png" alt="Screen shot of Window Color options preview " /><br/> <span data-ttu-id="f8e6c-195">在此範例中，每個選項的預覽清楚地顯示選項的效果，這比單獨使用文字更有效率。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-195">In this example, a preview of each option clearly shows the effect of the choice, which is more effective than using text alone.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f8e6c-196"><strong>清單</strong> 產生器允許使用者一次新增一個專案，並選擇性地設定清單順序，以建立選項的清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-196"><strong>List builders</strong> Allow users to create a list of choices by adding one item at a time, and optionally setting the list order.</span></span><br/></td>
<td><span data-ttu-id="f8e6c-197">清單產生器是由兩個單一選取清單所組成：左邊的清單是一組固定的選項，右側的清單是所建立的清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-197">A list builder consists of two single-selection lists: the list on the left is a fixed set of options and the list on the right is the list being built.</span></span> <span data-ttu-id="f8e6c-198">清單之間有兩個命令按鈕：</span><span class="sxs-lookup"><span data-stu-id="f8e6c-198">There are two command buttons between the lists:</span></span> <br/>
<ul>
<li><span data-ttu-id="f8e6c-199">[ <strong>加入</strong> ] 按鈕，會將目前選取的選項移至所要建立的清單，然後插入選取的專案之前。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-199">An <strong>Add</strong> button that moves the currently selected option to the list being built, inserted before the selected item.</span></span> <span data-ttu-id="f8e6c-200"> (按兩下選項專案的效果相同。 ) </span><span class="sxs-lookup"><span data-stu-id="f8e6c-200">(Double-clicking on an option item has the same effect.)</span></span></li>
<li><span data-ttu-id="f8e6c-201">從建立的清單中移除選取的專案，並將其傳回選項清單的 [ <strong>移除</strong> ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-201">A <strong>Remove</strong> button that removes the selected item from the built list and returns it to the option list.</span></span> <span data-ttu-id="f8e6c-202"> (按兩下內建清單中的專案具有相同的效果。 ) 建立清單可能會選擇性地使用 [ <strong>上移</strong> <strong>] 和 [下移]</strong> 命令來排列清單專案的順序。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-202">(Double-clicking on an item in the built list has the same effect.) The built list may optionally have <strong>Move Up</strong> and <strong>Move Down</strong> commands to order the list items.</span></span></li>
</ul>
<img src="images/ctrl-list-boxes-image8.png" alt="Screen shot of Toolbar buttons list builder " /><br/> <span data-ttu-id="f8e6c-203">在此範例中，清單產生器是用來建立工具列，方法是從一組可用選項中選取專案，並設定其順序。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-203">In this example, a list builder is used to create a toolbar by selecting items from a set of available options and setting their order.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f8e6c-204"><strong>新增/移除清單</strong> 允許使用者一次新增一個或多個專案，並選擇性地設定清單 (（例如清單產生器) ）來建立選項的清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-204"><strong>Add/remove lists</strong> Allow users to create a list of choices by adding one or more items at a time, and optionally setting the list order (like list builders).</span></span><br/></td>
<td><span data-ttu-id="f8e6c-205">不同于清單產生器，按一下 [ <strong>新增</strong> ] 會顯示一個對話方塊，以選取要加入至清單的專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-205">Unlike a list builder, clicking <strong>Add</strong> displays a dialog box to select items to add to the list.</span></span> <span data-ttu-id="f8e6c-206">使用個別的對話方塊可讓您在選擇專案時有很大的彈性，您可以使用特殊的物件選擇器或甚至一般的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-206">Using a separate dialog box allows for significant flexibility in choosing items you can use a specialized object picker or even a common dialog.</span></span> <span data-ttu-id="f8e6c-207">相較于清單產生器，此變化較精簡，但需要稍微多一點的時間來加入專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-207">Compared to the list builder, this variation is more compact but requires slightly more effort to add items.</span></span> <br/> <img src="images/ctrl-list-boxes-image9.png" alt="Screen shot of Menu contents list " /><br/> <span data-ttu-id="f8e6c-208">在此範例中，使用者可以從功能表新增或移除工具，以及設定順序。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-208">In this example, users can add or remove tools from a menu, as well as set order.</span></span><br/> <span data-ttu-id="f8e6c-209">雖然 [清單產生器] 和 [新增/移除] 清單模式明顯比其他多重選取清單更大，但它們提供兩個獨特的優點：</span><span class="sxs-lookup"><span data-stu-id="f8e6c-209">While the list builder and add/remove list patterns are significantly heavier than the other multiple-selection lists, they offer two unique advantages:</span></span><br/>
<ul>
<li><span data-ttu-id="f8e6c-210">在建立清單和之後，使用者都可以掌控清單順序。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-210">Users have control over the list order, both while building the list and after.</span></span></li>
<li><span data-ttu-id="f8e6c-211">使用者可以查看所選項目的摘要，如果選擇的數目很大，這可能會有很大的好處。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-211">Users can review a summary of the selected items, which can be a significant benefit if the number of choices is large.</span></span></li>
</ul>
<span data-ttu-id="f8e6c-212">缺點是它們需要更多的螢幕空間，而且可能很難在從頭建立大型專案清單時使用。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-212">Their disadvantages are that they require much more screen space and can be difficult to use when creating a large list of items from scratch.</span></span> <span data-ttu-id="f8e6c-213">因此，最適合用來建立簡短的清單，或修改已經存在的清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-213">Consequently, they are best used to create short lists or modify lists that already exist.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="f8e6c-214">指導方針</span><span class="sxs-lookup"><span data-stu-id="f8e6c-214">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="f8e6c-215">簡報</span><span class="sxs-lookup"><span data-stu-id="f8e6c-215">Presentation</span></span>

-   <span data-ttu-id="f8e6c-216">**以邏輯順序排序清單專案，例如將** 相關選項群組在一起，並先放置最常使用的專案，或使用字母順序。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-216">**Sort list items in a logical order,** such as grouping related options together, placing most frequently used items first, or using alphabetical order.</span></span> <span data-ttu-id="f8e6c-217">依字母順序排序名稱、依數位順序排序數位和日期（以時間順序排列）。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-217">Sort names in alphabetical order, numbers in numeric order, and dates in chronological order.</span></span> <span data-ttu-id="f8e6c-218">具有12個以上專案的清單應依字母順序排序，讓專案更容易尋找。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-218">Lists with 12 or more items should be sorted alphabetically to make items easier to find.</span></span>

<span data-ttu-id="f8e6c-219">**正確：** ![對齊 (左、置中、右) 的螢幕擷取畫面 ](images/ctrl-list-boxes-image10.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-219">**Correct:** ![screen shot of alignment (left, center, right) ](images/ctrl-list-boxes-image10.png)</span></span>

<span data-ttu-id="f8e6c-220">在此範例中，清單方塊專案依其空間關聯性排序。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-220">In this example, the list box items are sorted by their spatial relationship.</span></span>

<span data-ttu-id="f8e6c-221">**不正確：** ![雜亂無章清單的螢幕擷取畫面 ](images/ctrl-list-boxes-image11.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-221">**Incorrect:** ![screen shot of disorganized list ](images/ctrl-list-boxes-image11.png)</span></span>

<span data-ttu-id="f8e6c-222">在此範例中，有很多清單專案應依字母順序排序。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-222">In this example, there are so many list items that they should be sorted in alphabetical order.</span></span>

<span data-ttu-id="f8e6c-223">**正確：** ![依字母順序排列清單的螢幕擷取畫面 ](images/ctrl-list-boxes-image12.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-223">**Correct:** ![screen shot of alphabetized list ](images/ctrl-list-boxes-image12.png)</span></span>

<span data-ttu-id="f8e6c-224">在此範例中，清單專案比較容易尋找，因為它們會依字母順序排序。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-224">In this example, the list items are easier to find because they are sorted in alphabetical order.</span></span> <span data-ttu-id="f8e6c-225">不過，「所有 Windows 產品」專案都是在清單的開頭，而不是它的排序次序。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-225">However, the item "All Windows products" is at the beginning of the list, regardless of its sort order.</span></span>

-   <span data-ttu-id="f8e6c-226">無論其餘專案的排序次序為何，都 **可在清單的開頭放置代表 All 或 None 的選項**。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-226">**Place options that represent All or None at the beginning of the list**, regardless of sort order of the remaining items.</span></span>
-   <span data-ttu-id="f8e6c-227">**以括弧括住中繼選項。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-227">**Enclose meta-options in parentheses.**</span></span>

![<span data-ttu-id="f8e6c-228">下拉式清單的螢幕擷取畫面，其中已選取 [無]</span><span class="sxs-lookup"><span data-stu-id="f8e6c-228">screen shot of drop-down list with none selected</span></span> ](images/ctrl-list-boxes-image13.png)

<span data-ttu-id="f8e6c-229">在此範例中，「 (無) 」是中繼選項，因為它不是有效的選項值，而是表示選項本身未使用。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-229">In this example, "(none)" is a meta-option because it is not a valid value for the choice rather it indicates that the option itself isn't being used.</span></span>

-   <span data-ttu-id="f8e6c-230">**不要有空白清單專案改用中繼選項。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-230">**Don't have blank list items use meta-options instead.**</span></span> <span data-ttu-id="f8e6c-231">使用者不知道如何解讀空白專案，而中繼選項的意義是明確的。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-231">Users don't know how to interpret blank items, whereas the meaning of meta-options is explicit.</span></span>

<span data-ttu-id="f8e6c-232">**不正確：** ![已選取空白的下拉式清單螢幕擷取畫面 ](images/ctrl-list-boxes-image14.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-232">**Incorrect:** ![screen shot of drop-down list with blank selected ](images/ctrl-list-boxes-image14.png)</span></span>

<span data-ttu-id="f8e6c-233">在此範例中，空白專案的意義不清楚。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-233">In this example, the meaning of the blank item is unclear.</span></span>

<span data-ttu-id="f8e6c-234">**正確：** ![下拉式清單的螢幕擷取畫面，其中已選取 [無] ](images/ctrl-list-boxes-image13.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-234">**Correct:** ![screen shot of drop-down list with none selected ](images/ctrl-list-boxes-image13.png)</span></span>

<span data-ttu-id="f8e6c-235">在此範例中，會改為使用「 (無) 」中繼選項。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-235">In this example, the "(none)" meta-option is used instead.</span></span>

### <a name="interaction"></a><span data-ttu-id="f8e6c-236">互動</span><span class="sxs-lookup"><span data-stu-id="f8e6c-236">Interaction</span></span>

-   <span data-ttu-id="f8e6c-237">**請考慮提供按兩下行為。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-237">**Consider providing double-click behavior.**</span></span> <span data-ttu-id="f8e6c-238">按兩下應該與選取專案並執行其預設命令的效果相同。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-238">Double-clicking should have the same effect as selecting an item and performing its default command.</span></span>
-   <span data-ttu-id="f8e6c-239">**讓按兩下行為重複。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-239">**Make double-click behavior redundant.**</span></span> <span data-ttu-id="f8e6c-240">應該一律會有相同效果的命令按鈕或內容功能表命令。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-240">There should always be a command button or context menu command that has the same effect.</span></span>
-   <span data-ttu-id="f8e6c-241">**如果使用者無法對選取的專案進行任何動作，則不允許選取。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-241">**If users can't do anything with the selected items, don't allow selection.**</span></span>

<span data-ttu-id="f8e6c-242">**正確：** ![已完成的 wizard 變更清單螢幕擷取畫面 ](images/ctrl-list-boxes-image15.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-242">**Correct:** ![screen shot of list of wizard changes completed ](images/ctrl-list-boxes-image15.png)</span></span>

<span data-ttu-id="f8e6c-243">此清單方塊會顯示變更的唯讀清單;不需要選擇。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-243">This list box displays a read-only list of changes; there is no need for selection.</span></span>

-   <span data-ttu-id="f8e6c-244">**停用清單方塊時，也會停用任何相關聯的標籤和命令按鈕。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-244">**When disabling a list box, also disable any associated labels and command buttons.**</span></span>
-   <span data-ttu-id="f8e6c-245">**請勿在清單方塊中使用所選取專案的變更來：**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-245">**Don't use the change of the selected item in a list box to:**</span></span>
    -   <span data-ttu-id="f8e6c-246">執行命令。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-246">Perform commands.</span></span>
    -   <span data-ttu-id="f8e6c-247">顯示其他視窗，例如用來收集更多輸入的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-247">Display other windows, such as a dialog box to gather more input.</span></span>
    -   <span data-ttu-id="f8e6c-248">以動態方式顯示與所選取控制項相關的其他控制項 (畫面讀取器無法偵測到這類事件) 。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-248">Dynamically display other controls related to the selected control (screen readers cannot detect such events).</span></span> <span data-ttu-id="f8e6c-249">**例外狀況：** 您可以動態變更用來描述所選取專案的靜態文字。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-249">**Exception:** You can dynamically change static text used to describe the selected item.</span></span>

<span data-ttu-id="f8e6c-250">**可接受：** ![選取清單專案詳細資料的螢幕擷取畫面 ](images/ctrl-list-boxes-image16.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-250">**Acceptable:** ![screen shot of details of list item selected ](images/ctrl-list-boxes-image16.png)</span></span>

<span data-ttu-id="f8e6c-251">在此範例中，變更選取的專案會變更描述。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-251">In this example, changing the selected item changes the description.</span></span>

-   <span data-ttu-id="f8e6c-252">**避免水準滾動。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-252">**Avoid horizontal scrolling.**</span></span> <span data-ttu-id="f8e6c-253">多行清單依賴水準滾動，通常比垂直捲動更難使用。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-253">Multicolumn lists rely on horizontal scrolling, which is generally harder to use than vertical scrolling.</span></span> <span data-ttu-id="f8e6c-254">當您有許多字母順序的專案，且有足夠的螢幕空間可供寬控制項使用時，可能會使用需要水準滾動的多行清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-254">Multicolumn lists that require horizontal scrolling may be used when you have many alphabetically sorted items and sufficient screen space for a wide control.</span></span>

<span data-ttu-id="f8e6c-255">**可接受：** ![windows explorer 中的資料夾清單螢幕擷取畫面 ](images/ctrl-list-boxes-image17.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-255">**Acceptable:** ![screen shot of list of folders in windows explorer ](images/ctrl-list-boxes-image17.png)</span></span>

<span data-ttu-id="f8e6c-256">在此範例中，會使用多個需要水準滾動的資料行，因為有許多專案和大量的可用螢幕空間可供廣泛的控制項使用。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-256">In this example, multiple columns that require horizontal scrolling are used because there are many items and plenty of available screen space for a wide control.</span></span>

### <a name="multiple-selection-lists"></a><span data-ttu-id="f8e6c-257">多重選取清單</span><span class="sxs-lookup"><span data-stu-id="f8e6c-257">Multiple-selection lists</span></span>

-   <span data-ttu-id="f8e6c-258">**請考慮在清單下方顯示選取的專案數目，** 特別是當使用者可能選取數個專案時。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-258">**Consider displaying the number of selected items below the list,** especially if users are likely to select several items.</span></span> <span data-ttu-id="f8e6c-259">這項資訊不僅能提供有用的意見反應，也清楚指出清單方塊支援多重選取。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-259">This information not only gives useful feedback, but it also clearly indicates that the list box supports multiple selection.</span></span>

![<span data-ttu-id="f8e6c-260">已選取四個專案的清單方塊螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f8e6c-260">screen shot of list box with four items selected</span></span> ](images/ctrl-list-boxes-image5.png)

<span data-ttu-id="f8e6c-261">在此範例中，選取的專案數目會顯示在清單下方。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-261">In this example, the number of selected items is displayed below the list.</span></span>

-   <span data-ttu-id="f8e6c-262">您可以提供可能更有意義的其他選取範圍計量，例如選取專案所需的資源。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-262">You can provide other selection metrics that might be more meaningful, such as the resources required for the selections.</span></span>

![<span data-ttu-id="f8e6c-263">windows 功能的核取方塊清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f8e6c-263">screen shot of check-box list of windows features</span></span> ](images/ctrl-list-boxes-image18.png)

<span data-ttu-id="f8e6c-264">在此範例中，安裝元件所需的磁碟空間比選取的專案數目更有意義。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-264">In this example, the disk space required to install the components is more meaningful than the number of items selected.</span></span>

-   <span data-ttu-id="f8e6c-265">如果有可能有許多清單專案，並選取或清除所有的專案，請加入 [全選] 和 [全部清除] 命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-265">If there are potentially many list items and selecting or clearing all of them is likely, add Select all and Clear all command buttons.</span></span>
-   <span data-ttu-id="f8e6c-266">針對標準的多重選取清單，請勿使用多重選取模式，因為此選取模式已被取代。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-266">For standard multiple-selection lists, don't use multiple-selection mode because this selection mode has been deprecated.</span></span> <span data-ttu-id="f8e6c-267">針對相等的行為，請改用核取方塊清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-267">For equivalent behavior, use a check box list instead.</span></span>

### <a name="default-values"></a><span data-ttu-id="f8e6c-268">預設值</span><span class="sxs-lookup"><span data-stu-id="f8e6c-268">Default values</span></span>

-   <span data-ttu-id="f8e6c-269">**依預設，請選取最安全的 (，以防止遺失資料或系統存取) 和最安全的選項。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-269">**Select the safest (to prevent loss of data or system access) and most secure option by default.**</span></span> <span data-ttu-id="f8e6c-270">如果安全性和安全性不是因素，請選取最有可能或方便的選項。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-270">If safety and security aren't factors, select the most likely or convenient option.</span></span>

<span data-ttu-id="f8e6c-271">**例外狀況：** 如果控制項代表 [混合狀態](glossary.md)中的屬性，則不選取任何專案，這會在顯示多個沒有相同設定之物件的屬性時發生。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-271">**Exception:** Don't select any items if the control represents a property in a [mixed state](glossary.md), which happens when displaying a property for multiple objects that don't have the same setting.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="f8e6c-272">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="f8e6c-272">Recommended sizing and spacing</span></span>

![<span data-ttu-id="f8e6c-273">清單方塊調整大小和間距的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f8e6c-273">screen shot of list-box sizing and spacing</span></span> ](images/ctrl-list-boxes-image19.png)

<span data-ttu-id="f8e6c-274">清單方塊的建議大小和間距。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-274">Recommended sizing and spacing for list boxes.</span></span>

-   <span data-ttu-id="f8e6c-275">**選擇適合最長有效資料的清單方塊寬度。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-275">**Choose a list box width appropriate for the longest valid data.**</span></span> <span data-ttu-id="f8e6c-276">標準清單方塊無法水準滾動，因此使用者只能看到控制項中顯示的內容。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-276">Standard list boxes cannot be scrolled horizontally, so users can see only what is visible in the control.</span></span>
-   <span data-ttu-id="f8e6c-277">**包含額外的 30%** (高達200% 的文字，以提供任何文字 (較短的文字) ，而不是) 將當地語系化的數位。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-277">**Include an additional 30 percent** (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span>
-   <span data-ttu-id="f8e6c-278">**選擇顯示整數專案數目的清單方塊高度。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-278">**Choose a list box height that displays an integral number of items.**</span></span> <span data-ttu-id="f8e6c-279">避免垂直截斷專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-279">Avoid truncating items vertically.</span></span>
-   <span data-ttu-id="f8e6c-280">**選擇可消除不必要垂直捲動的清單方塊高度。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-280">**Choose a list box height that eliminates unnecessary vertical scrolling.**</span></span> <span data-ttu-id="f8e6c-281">清單方塊應該會顯示3到20個專案，而不需要滾動。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-281">List boxes should display between 3 and 20 items without the need for scrolling.</span></span> <span data-ttu-id="f8e6c-282">如果這樣做會消除垂直捲動條，請考慮讓清單方塊稍微長一點。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-282">Consider making a list box slightly longer if doing so eliminates the vertical scroll bar.</span></span> <span data-ttu-id="f8e6c-283">可能有多個專案的清單應該會顯示至少五個專案，藉由一次顯示更多專案，並讓捲軸更容易放置，來加速滾動。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-283">Lists with potentially many items should display at least five items to facilitate scrolling by showing more items at a time and making the scroll bar easier to position.</span></span>
-   <span data-ttu-id="f8e6c-284">**如果使用者受益于使清單方塊變得更大，請讓清單方塊和其父視窗可調整大小。**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-284">**If users benefit from making the list box larger, make the list box and its parent window resizable.**</span></span> <span data-ttu-id="f8e6c-285">這麼做可讓使用者視需要調整清單方塊的大小。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-285">Doing so allows users to adjust the list box size as needed.</span></span> <span data-ttu-id="f8e6c-286">不過，可調整大小的清單方塊應該不會顯示三個以上的專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-286">However, resizable list boxes should display no fewer than three items.</span></span>

## <a name="labels"></a><span data-ttu-id="f8e6c-287">標籤</span><span class="sxs-lookup"><span data-stu-id="f8e6c-287">Labels</span></span>

<span data-ttu-id="f8e6c-288">**控制項標籤**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-288">**Control labels**</span></span>

-   <span data-ttu-id="f8e6c-289">所有清單方塊都需要標籤。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-289">All list boxes need labels.</span></span> <span data-ttu-id="f8e6c-290">將標籤以單字或片語的形式寫入，而不是以句子撰寫;使用標籤結尾的冒號。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-290">Write the label as a word or phrase, not as a sentence; use a colon at the end of the label.</span></span>

<span data-ttu-id="f8e6c-291">**例外狀況：** 如果標籤只是對話方塊 [主要指示](glossary.md)的重述，請省略標籤。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-291">**Exception:** Omit the label if it is merely a restatement of a dialog box's [main instruction](glossary.md).</span></span> <span data-ttu-id="f8e6c-292">在此情況下，主要指令會採用冒號 (，除非它是問題) 和存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-292">In this case, the main instruction takes the colon (unless it's a question) and access key.</span></span>

<span data-ttu-id="f8e6c-293">**可接受：** ![具有重複標籤清單的螢幕擷取畫面 ](images/ctrl-list-boxes-image20.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-293">**Acceptable:** ![screen shot of list with redundant label ](images/ctrl-list-boxes-image20.png)</span></span>

<span data-ttu-id="f8e6c-294">在此範例中，清單方塊標籤只會下方重述主要指令。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-294">In this example, the list box label just restates the main instruction.</span></span>

<span data-ttu-id="f8e6c-295">**更好：** ![沒有重複標籤清單的螢幕擷取畫面 ](images/ctrl-list-boxes-image21.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-295">**Better:** ![screen shot of list of without redundant label ](images/ctrl-list-boxes-image21.png)</span></span>

<span data-ttu-id="f8e6c-296">在此範例中，會移除多餘的標籤，所以主要指令會接受冒號和存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-296">In this example, the redundant label is removed, so the main instruction takes the colon and access key.</span></span>

-   <span data-ttu-id="f8e6c-297">如果清單方塊是指向選項按鈕或核取方塊，且該控制項的標籤以冒號結尾，請勿在清單方塊控制項上放置額外的標籤。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-297">If a list box is subordinate to a radio button or check box and is introduced by that control's label ending with a colon, don't put an additional label on the list box control.</span></span>

![<span data-ttu-id="f8e6c-298">使用相同標籤的按鈕和清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f8e6c-298">screen shot of button and list using same label</span></span> ](images/ctrl-list-boxes-image22.png)

<span data-ttu-id="f8e6c-299">在此範例中，清單方塊是一個選項按鈕，並共用其標籤。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-299">In this example, the list box is subordinate to a radio button and shares its label.</span></span>

-   <span data-ttu-id="f8e6c-300">指派唯一的 [存取金鑰](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-300">Assign a unique [access key](glossary.md).</span></span> <span data-ttu-id="f8e6c-301">如需指導方針，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-301">For guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="f8e6c-302">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-302">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="f8e6c-303">將標籤置於控制項的左邊或上方，然後將標籤與控制項的左邊緣對齊。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-303">Position the label either to the left of or above the control, and align the label with the left edge of the control.</span></span>
    -   <span data-ttu-id="f8e6c-304">如果標籤位於左邊，則垂直對齊標籤文字與控制項中的第一行文字。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-304">If label is on the left, vertically align the label text with the first line of text in the control.</span></span>

<span data-ttu-id="f8e6c-305">**正確：** ![清單中具有靠左對齊標籤且靠左對齊標籤的清單螢幕擷取畫面 ](images/ctrl-list-boxes-image23.png)![](images/ctrl-list-boxes-image24.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-305">**Correct:** ![screen shot of list with left-aligned label above ](images/ctrl-list-boxes-image23.png)![screen shot of list with text-aligned label to left ](images/ctrl-list-boxes-image24.png)</span></span>

<span data-ttu-id="f8e6c-306">在這些範例中，頂端的標籤會與清單方塊的左邊緣對齊，而左邊的標籤會與清單方塊中的文字對齊。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-306">In these examples, the label on top aligns with the left edge of the list box and the label on the left aligns with the text in the list box.</span></span>

<span data-ttu-id="f8e6c-307">**不正確：** ![左邊對齊標籤的清單螢幕擷取畫面上方清單中的螢幕擷取畫面 ](images/ctrl-list-boxes-image25.png)![](images/ctrl-list-boxes-image26.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-307">**Incorrect:** ![screen shot of list with text-aligned label above ](images/ctrl-list-boxes-image25.png)![screen shot of list with top-aligned label on left ](images/ctrl-list-boxes-image26.png)</span></span>

<span data-ttu-id="f8e6c-308">在這些不正確的範例中，頂端的標籤會與清單方塊中的文字對齊，而左邊的標籤會與清單方塊的頂端對齊。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-308">In these incorrect examples, the label on top aligns with the text in the list box and the label on the left aligns with the top of the list box.</span></span>

-   <span data-ttu-id="f8e6c-309">若為多重選取清單方塊，請使用可清楚指出可能有多重選取的標籤。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-309">For multiple-selection list boxes, use a label that clearly indicates multiple selection is possible.</span></span> <span data-ttu-id="f8e6c-310">核取方塊清單標籤可能較不明確。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-310">Check box list labels can be less explicit.</span></span>

<span data-ttu-id="f8e6c-311">**正確：** ![[選取一或多個標籤] 清單的螢幕擷取畫面 ](images/ctrl-list-boxes-image27.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-311">**Correct:** ![screen shot of list with select one or more label ](images/ctrl-list-boxes-image27.png)</span></span>

<span data-ttu-id="f8e6c-312">在此範例中，標籤會清楚指出可能會有多個選取專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-312">In this example, the label clearly indicates that multiple selection is possible.</span></span>

<span data-ttu-id="f8e6c-313">**不正確：** ![具有附加元件標籤之清單方塊的螢幕擷取畫面 ](images/ctrl-list-boxes-image28.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-313">**Incorrect:** ![screen shot of list box with add-ons label ](images/ctrl-list-boxes-image28.png)</span></span>

<span data-ttu-id="f8e6c-314">在此範例中，標籤不會提供關於多重選取的明顯資訊。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-314">In this example, the label provides no obvious information about multiple selection.</span></span>

<span data-ttu-id="f8e6c-315">**最佳：** ![包含附加元件標籤的核取方塊清單螢幕擷取畫面 ](images/ctrl-list-boxes-image29.png)</span><span class="sxs-lookup"><span data-stu-id="f8e6c-315">**Best:** ![screen shot of check-box list with add-ons label ](images/ctrl-list-boxes-image29.png)</span></span>

<span data-ttu-id="f8e6c-316">在此範例中，核取方塊會清楚指出可能有多重選取，因此標籤不需要明確。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-316">In this example, the check boxes clearly indicate that multiple selection is possible, so the label doesn't have to be explicit.</span></span>

-   <span data-ttu-id="f8e6c-317">您可以在標籤後面的括弧中，指定單位 (秒、連接等) 。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-317">You may specify units (seconds, connections, and so on) in parentheses after the label.</span></span>

<span data-ttu-id="f8e6c-318">**選項文字**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-318">**Option text**</span></span>

-   <span data-ttu-id="f8e6c-319">將唯一名稱指派給每個選項。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-319">Assign a unique name to each option.</span></span>
-   <span data-ttu-id="f8e6c-320">除非專案是適當的名詞，否則請使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-320">Use [sentence-style capitalization](glossary.md), unless an item is a proper noun.</span></span>
-   <span data-ttu-id="f8e6c-321">將標籤以單字或片語的形式寫入，而不是以句子形式寫入，而且不使用結尾標點符號。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-321">Write the label as a word or phrase, not as a sentence, and use no ending punctuation.</span></span>
-   <span data-ttu-id="f8e6c-322">使用平行片語，並嘗試保留所有選項的相同長度。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-322">Use parallel phrasing, and try to keep the length about the same for all options.</span></span>

<span data-ttu-id="f8e6c-323">**教學和補充文字**</span><span class="sxs-lookup"><span data-stu-id="f8e6c-323">**Instructional and supplemental text**</span></span>

-   <span data-ttu-id="f8e6c-324">如果您需要新增有關清單方塊的解說文字，請將它加入標籤上方。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-324">If you need to add instructional text about a list box, add it above the label.</span></span> <span data-ttu-id="f8e6c-325">使用結尾標點符號的完整句子。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-325">Use complete sentences with ending punctuation.</span></span>
-   <span data-ttu-id="f8e6c-326">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-326">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="f8e6c-327">有説明但不需要的其他資訊應該保持簡短。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-327">Additional information that is helpful but not necessary should be kept short.</span></span> <span data-ttu-id="f8e6c-328">將此文字放在標籤和冒號之間的括弧中，或是在控制項下方的括弧內。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-328">Place this text either in parentheses between the label and colon, or without parentheses below the control.</span></span>

![<span data-ttu-id="f8e6c-329">核取方塊清單和描述性文字的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="f8e6c-329">screen shot of check-box list and descriptive text</span></span> ](images/ctrl-list-boxes-image30.png)

<span data-ttu-id="f8e6c-330">在此範例中，補充文字會放置在清單下方。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-330">In this example, supplemental text is placed below the list.</span></span>

## <a name="documentation"></a><span data-ttu-id="f8e6c-331">文件</span><span class="sxs-lookup"><span data-stu-id="f8e6c-331">Documentation</span></span>

<span data-ttu-id="f8e6c-332">參考清單方塊時：</span><span class="sxs-lookup"><span data-stu-id="f8e6c-332">When referring to list boxes:</span></span>

-   <span data-ttu-id="f8e6c-333">使用確切的標籤文字，包括其大小寫，但不包含存取金鑰底線或冒號。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-333">Use the exact label text, including its capitalization, but don't include the access key underscore or colon.</span></span> <span data-ttu-id="f8e6c-334">包含字組清單。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-334">Include the word list.</span></span> <span data-ttu-id="f8e6c-335">請勿以清單方塊或欄位形式來參考清單方塊。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-335">Don't refer to a list box as a list box or a field.</span></span>
-   <span data-ttu-id="f8e6c-336">針對清單專案，使用確切的專案文字，包括其大小寫。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-336">For list items, use the exact item text, including its capitalization.</span></span>
-   <span data-ttu-id="f8e6c-337">在程式設計和其他技術檔中，請以清單方塊的形式來參考清單方塊。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-337">In programming and other technical documentation, refer to list boxes as list boxes.</span></span> <span data-ttu-id="f8e6c-338">在其他地方，使用 list。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-338">Everywhere else, use list.</span></span>
-   <span data-ttu-id="f8e6c-339">若要描述使用者互動，請使用 select。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-339">To describe user interaction, use select.</span></span>
-   <span data-ttu-id="f8e6c-340">可能的話，請使用粗體文字來格式化標籤和清單專案。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-340">When possible, format the label and list items using bold text.</span></span> <span data-ttu-id="f8e6c-341">否則，請只在必要時才將標籤和專案放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-341">Otherwise, put the label and items in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="f8e6c-342">範例：在 [ **移至目標** ] 清單中選取 [ **書簽**]。</span><span class="sxs-lookup"><span data-stu-id="f8e6c-342">Example: In the **Go to what** list, select **Bookmark**.</span></span>

