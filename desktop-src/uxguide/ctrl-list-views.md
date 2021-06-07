---
title: 列出視圖
description: 使用清單視圖時，使用者可以使用單一選取或多重選取專案來查看資料物件的集合，並與之互動。
ms.assetid: 62a7bfc8-96a9-450d-9db9-ec9dab6687b7
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 13847e484ccaa78fd08ac9fe60b1432d272b9efa
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524562"
---
# <a name="list-views"></a><span data-ttu-id="72c3a-103">列出視圖</span><span class="sxs-lookup"><span data-stu-id="72c3a-103">List Views</span></span>

> [!NOTE]
> <span data-ttu-id="72c3a-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="72c3a-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="72c3a-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="72c3a-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="72c3a-106">使用清單視圖時，使用者可以使用單一選取或多重選取專案來查看資料物件的集合，並與之互動。</span><span class="sxs-lookup"><span data-stu-id="72c3a-106">With a list view, users can view and interact with a collection of data objects, using either single selection or multiple selection.</span></span>

![<span data-ttu-id="72c3a-107">清單視圖與資料行標頭的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-107">screen shot of list view with column headers</span></span> ](images/ctrl-list-views-image1.png)

<span data-ttu-id="72c3a-108">一般清單視圖。</span><span class="sxs-lookup"><span data-stu-id="72c3a-108">A typical list view.</span></span>

<span data-ttu-id="72c3a-109">清單視圖比清單方塊具有更大的彈性和功能。</span><span class="sxs-lookup"><span data-stu-id="72c3a-109">List views have more flexibility and functionality than list boxes.</span></span> <span data-ttu-id="72c3a-110">不同于清單方塊，它們支援變更視圖、群組、具有標題的多個資料行、依資料行排序、變更資料行寬度和順序、拖曳來源或放置目標，以及將資料複製到剪貼簿，以及將資料複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="72c3a-110">Unlike list boxes, they support changing views, grouping, multiple columns with headings, sorting by columns, changing column widths and order, being a drag source or a drop target, and copying data to and from the clipboard.</span></span>

> [!Note]  
> <span data-ttu-id="72c3a-111">與 [版面](vis-layout.md) 配置和 [清單方塊](ctrl-list-boxes.md) 相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="72c3a-111">Guidelines related to [layout](vis-layout.md) and [list boxes](ctrl-list-boxes.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="72c3a-112">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="72c3a-112">Is this the right control?</span></span>

<span data-ttu-id="72c3a-113">清單視圖不只是更有彈性且功能更高的清單方塊：它的額外功能會導致不同的使用方式。</span><span class="sxs-lookup"><span data-stu-id="72c3a-113">A list view is more than just a more flexible and functional list box: its extra functionality results in different usage.</span></span> <span data-ttu-id="72c3a-114">下表顯示比較。</span><span class="sxs-lookup"><span data-stu-id="72c3a-114">The following table shows the comparison.</span></span>



|   <span data-ttu-id="72c3a-115">使用方式</span><span class="sxs-lookup"><span data-stu-id="72c3a-115">Usage</span></span>                          | <span data-ttu-id="72c3a-116">清單方塊</span><span class="sxs-lookup"><span data-stu-id="72c3a-116">List boxes</span></span>                 | <span data-ttu-id="72c3a-117">清單檢視</span><span class="sxs-lookup"><span data-stu-id="72c3a-117">List views</span></span>               |
|-----------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72c3a-118">**Data type**</span><span class="sxs-lookup"><span data-stu-id="72c3a-118">**Data type**</span></span><br/>    | <span data-ttu-id="72c3a-119">資料和程式選項。</span><span class="sxs-lookup"><span data-stu-id="72c3a-119">Both data and program options.</span></span><br/> | <span data-ttu-id="72c3a-120">僅限資料。</span><span class="sxs-lookup"><span data-stu-id="72c3a-120">Data only.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="72c3a-121">**Contents**</span><span class="sxs-lookup"><span data-stu-id="72c3a-121">**Contents**</span></span><br/>     | <span data-ttu-id="72c3a-122">僅限標籤。</span><span class="sxs-lookup"><span data-stu-id="72c3a-122">Labels only.</span></span><br/>                   | <span data-ttu-id="72c3a-123">標籤和輔助資料，可能在多個資料行中。</span><span class="sxs-lookup"><span data-stu-id="72c3a-123">Labels and auxiliary data, possibly in multiple columns.</span></span><br/>                                                                           |
| <span data-ttu-id="72c3a-124">**互動**</span><span class="sxs-lookup"><span data-stu-id="72c3a-124">**Interaction**</span></span><br/>  | <span data-ttu-id="72c3a-125">用於進行選取。</span><span class="sxs-lookup"><span data-stu-id="72c3a-125">Used for making selections.</span></span><br/>    | <span data-ttu-id="72c3a-126">可以用來進行選擇，但通常用於顯示資料和與資料互動。</span><span class="sxs-lookup"><span data-stu-id="72c3a-126">Can be used for making selections, but often used for displaying and interacting with data.</span></span> <span data-ttu-id="72c3a-127">可以是拖曳來源或放置目標。</span><span class="sxs-lookup"><span data-stu-id="72c3a-127">Can be a drag source or a drop target.</span></span><br/> |
| <span data-ttu-id="72c3a-128">**展示**</span><span class="sxs-lookup"><span data-stu-id="72c3a-128">**Presentation**</span></span><br/> | <span data-ttu-id="72c3a-129">固定。</span><span class="sxs-lookup"><span data-stu-id="72c3a-129">Fixed.</span></span><br/>                         | <span data-ttu-id="72c3a-130">使用者可以變更視圖、群組、依資料行排序，以及變更資料行的寬度和順序。</span><span class="sxs-lookup"><span data-stu-id="72c3a-130">Users can change views, group, sort by columns, and change column widths and order.</span></span><br/>                                                |



 

<span data-ttu-id="72c3a-131">若要判斷這是否為正確的控制項，請考慮下列問題：</span><span class="sxs-lookup"><span data-stu-id="72c3a-131">To decide if this is the right control, consider these questions:</span></span>

-   <span data-ttu-id="72c3a-132">**清單是否會顯示資料，而不是程式選項？**</span><span class="sxs-lookup"><span data-stu-id="72c3a-132">**Does the list present data, rather than program options?**</span></span> <span data-ttu-id="72c3a-133">如果沒有，請考慮改為使用清單方塊。</span><span class="sxs-lookup"><span data-stu-id="72c3a-133">If not, consider using a list box instead.</span></span>
-   <span data-ttu-id="72c3a-134">**使用者是否需要變更視圖、群組、依資料行排序，或變更資料行的寬度和順序？**</span><span class="sxs-lookup"><span data-stu-id="72c3a-134">**Do users need to change views, group, sort by columns, or change column widths and order?**</span></span> <span data-ttu-id="72c3a-135">如果沒有，請改為使用清單方塊。</span><span class="sxs-lookup"><span data-stu-id="72c3a-135">If not, use a list box instead.</span></span>
-   <span data-ttu-id="72c3a-136">**控制項必須是拖曳來源或放置目標？**</span><span class="sxs-lookup"><span data-stu-id="72c3a-136">**Does the control need to be a drag source or a drop target?**</span></span> <span data-ttu-id="72c3a-137">如果是的話，請使用清單視圖。</span><span class="sxs-lookup"><span data-stu-id="72c3a-137">If so, use a list view.</span></span>
-   <span data-ttu-id="72c3a-138">**是否需要將清單專案複製到剪貼簿或從剪貼簿貼上？**</span><span class="sxs-lookup"><span data-stu-id="72c3a-138">**Do the list items need to be copied to or pasted from the clipboard?**</span></span> <span data-ttu-id="72c3a-139">如果是的話，請使用清單視圖。</span><span class="sxs-lookup"><span data-stu-id="72c3a-139">If so, use a list view.</span></span>

### <a name="check-box-list-views"></a><span data-ttu-id="72c3a-140">核取方塊清單視圖</span><span class="sxs-lookup"><span data-stu-id="72c3a-140">Check box list views</span></span>

-   <span data-ttu-id="72c3a-141">**控制項是否可用來從資料清單中選擇零個以上的專案？**</span><span class="sxs-lookup"><span data-stu-id="72c3a-141">**Is the control used to choose zero or more items from a list of data?**</span></span> <span data-ttu-id="72c3a-142">若要選擇一個專案，請改為使用單一選項。</span><span class="sxs-lookup"><span data-stu-id="72c3a-142">To choose one item, use single selection instead.</span></span>
-   <span data-ttu-id="72c3a-143">**這項工作或通常使用的是多重選取專案嗎？**</span><span class="sxs-lookup"><span data-stu-id="72c3a-143">**Is multiple selection essential to the task or commonly used?**</span></span> <span data-ttu-id="72c3a-144">如果是的話，請使用核取方塊清單視圖讓多個選取明顯，尤其是當您的目標使用者不是 advanced。</span><span class="sxs-lookup"><span data-stu-id="72c3a-144">If so, use a check box list view to make multiple selection obvious, especially if your target users aren't advanced.</span></span> <span data-ttu-id="72c3a-145">如果沒有，請使用標準的多重選取清單查看，如果核取方塊會對多個選取專案造成太多的注意，或造成太多螢幕雜亂。</span><span class="sxs-lookup"><span data-stu-id="72c3a-145">If not, use a standard multiple-selection list view if the check boxes would draw too much attention to multiple selection or result in too much screen clutter.</span></span>
-   <span data-ttu-id="72c3a-146">**多重選取專案的穩定性是否重要？**</span><span class="sxs-lookup"><span data-stu-id="72c3a-146">**Is the stability of the multiple selection important?**</span></span> <span data-ttu-id="72c3a-147">如果是的話，請使用 [核取方塊清單](ctrl-list-boxes.md)、清單產生器或新增/移除清單，因為按一下一次只變更一個專案。</span><span class="sxs-lookup"><span data-stu-id="72c3a-147">If so, use a [check box list](ctrl-list-boxes.md), list builder, or add/remove list because clicking changes only a single item at a time.</span></span> <span data-ttu-id="72c3a-148">使用標準的多重選取清單時，很容易就能清除所有選取專案，即使是意外的。</span><span class="sxs-lookup"><span data-stu-id="72c3a-148">With a standard multiple selection list, it's very easy to clear all the selections even by accident.</span></span>

> [!Note]  
> <span data-ttu-id="72c3a-149">有時候看起來像清單視圖的控制項是使用清單方塊來執行，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="72c3a-149">Sometimes a control that looks like a list view is implemented using a list box, and vice versa.</span></span> <span data-ttu-id="72c3a-150">在這種情況下，請根據使用方式套用指導方針，而不是在執行時套用。</span><span class="sxs-lookup"><span data-stu-id="72c3a-150">In such cases, apply the guidelines based on the usage, not on the implementation.</span></span>

 

## <a name="usage-patterns"></a><span data-ttu-id="72c3a-151">使用模式</span><span class="sxs-lookup"><span data-stu-id="72c3a-151">Usage patterns</span></span>

<span data-ttu-id="72c3a-152">所有視圖都支援單一選取，其中使用者一次只能選取一個專案，而多個選項可讓使用者選取任意數目的專案，包括 none。</span><span class="sxs-lookup"><span data-stu-id="72c3a-152">All views support single selection, where users can select only one item at a time, and multiple selection, where users can select any number of items, including none.</span></span> <span data-ttu-id="72c3a-153">清單視圖支援 [延伸選取模式](glossary.md)，也就是透過拖曳或使用 Shift + Click 或 Ctrl + 按一下來選取連續或非相鄰值的群組，來擴充選取範圍。</span><span class="sxs-lookup"><span data-stu-id="72c3a-153">List views support [extended selection mode](glossary.md), where the selection can be extended by dragging or with Shift+click or Ctrl+click to select groups of contiguous or non-adjacent values, respectively.</span></span> <span data-ttu-id="72c3a-154">與清單方塊不同的是，它們不支援 [多重選取模式](glossary.md)，因為不論 Shift 和 Ctrl 鍵為何，按一下任何專案都會切換其選取狀態。</span><span class="sxs-lookup"><span data-stu-id="72c3a-154">Unlike list boxes, they don't support [multiple selection mode](glossary.md), where clicking any item toggles its selection state regardless of the Shift and Ctrl keys.</span></span>

### <a name="standard-list-view"></a><span data-ttu-id="72c3a-155">標準清單視圖</span><span class="sxs-lookup"><span data-stu-id="72c3a-155">Standard list view</span></span>

<span data-ttu-id="72c3a-156">清單視圖控制項支援五個標準視圖：</span><span class="sxs-lookup"><span data-stu-id="72c3a-156">The list view control supports five standard views:</span></span>



|    <span data-ttu-id="72c3a-157">使用狀況</span><span class="sxs-lookup"><span data-stu-id="72c3a-157">Usage</span></span>    |   <span data-ttu-id="72c3a-158">範例</span><span class="sxs-lookup"><span data-stu-id="72c3a-158">Example</span></span>        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72c3a-159">**磚**</span><span class="sxs-lookup"><span data-stu-id="72c3a-159">**Tile**</span></span><br/> <span data-ttu-id="72c3a-160">每個專案都會顯示為中圖示，右邊有標籤和選擇性的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="72c3a-160">each item appears as a medium icon, with a label and optional details to the right.</span></span> <br/>                                                                                                                         | ![<span data-ttu-id="72c3a-161">具有標題和詳細資料的縮圖螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-161">screen shot of thumbnails with titles and details</span></span> ](images/ctrl-list-views-image2.png)<br/> <span data-ttu-id="72c3a-162">磚視圖會顯示具有標籤的中等圖示和右邊的選擇性詳細資料。</span><span class="sxs-lookup"><span data-stu-id="72c3a-162">Tile view shows medium icons with labels and optional details on the right.</span></span><br/>                                                                                                                                                                |
| <span data-ttu-id="72c3a-163">**大型圖示**</span><span class="sxs-lookup"><span data-stu-id="72c3a-163">**Large icon**</span></span><br/> <span data-ttu-id="72c3a-164">每個專案都會顯示為額外的大型、大型或中圖示，並在其下方加上標籤。</span><span class="sxs-lookup"><span data-stu-id="72c3a-164">each item appears as an extra large, large, or medium icon with a label below it.</span></span><br/>                                                                                                                      | ![<span data-ttu-id="72c3a-165">大型縮圖清單視圖的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-165">screen shot of large thumbnail list view</span></span> ](images/ctrl-list-views-image3.png)<br/> <span data-ttu-id="72c3a-166">大型圖示視圖會將每個專案顯示為大型圖示，並在其下方加上標籤。</span><span class="sxs-lookup"><span data-stu-id="72c3a-166">Large Icon view shows each item as a large icon with a label below it.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="72c3a-167">**小圖示**</span><span class="sxs-lookup"><span data-stu-id="72c3a-167">**Small icon**</span></span><br/> <span data-ttu-id="72c3a-168">每個專案都會顯示為具有右邊標籤的小圖示。</span><span class="sxs-lookup"><span data-stu-id="72c3a-168">each item appears as a small icon with a label to the right.</span></span><br/>                                                                                                                                           | ![<span data-ttu-id="72c3a-169">小縮圖清單視圖的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-169">screen shot of small thumbnail list view</span></span> ](images/ctrl-list-views-image4.png)<br/> <span data-ttu-id="72c3a-170">小圖示視圖會將每個專案顯示為小圖示，並在右側顯示其標籤。</span><span class="sxs-lookup"><span data-stu-id="72c3a-170">Small Icon view shows each item as a small icon with its label on the right.</span></span><br/>                                                                                                                                                                        |
| <span data-ttu-id="72c3a-171">**清單**</span><span class="sxs-lookup"><span data-stu-id="72c3a-171">**List**</span></span><br/> <span data-ttu-id="72c3a-172">每個專案都會顯示為具有右邊標籤的小圖示。</span><span class="sxs-lookup"><span data-stu-id="72c3a-172">each item appears as a small icon with a label to the right.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="72c3a-173">在清單模式中，這個視圖會排列資料行中的專案，並使用水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="72c3a-173">in list mode, this view orders items in columns and uses a horizontal scrollbar.</span></span> <span data-ttu-id="72c3a-174">相反地，圖示視圖模式會排列資料列中的專案，並使用垂直捲動條。</span><span class="sxs-lookup"><span data-stu-id="72c3a-174">by contrast, the icon view modes order items in rows and use a vertical scrollbar.</span></span> <br/> ![<span data-ttu-id="72c3a-175">清單模式中清單視圖的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-175">screen shot of list view in list mode</span></span> ](images/ctrl-list-views-image5.png)<br/> <span data-ttu-id="72c3a-176">清單模式會將每個專案顯示為小圖示，並在右側顯示其標籤。</span><span class="sxs-lookup"><span data-stu-id="72c3a-176">List mode shows each item as a small icon with its label on the right.</span></span><br/> |
| <span data-ttu-id="72c3a-177">**詳細資料**</span><span class="sxs-lookup"><span data-stu-id="72c3a-177">**Details**</span></span><br/> <span data-ttu-id="72c3a-178">每個專案都會以表格格式顯示為數據列。</span><span class="sxs-lookup"><span data-stu-id="72c3a-178">each item appears as a row in a tabular format.</span></span> <span data-ttu-id="72c3a-179">最左邊的資料行包含專案的選擇性圖示和標籤，而後續的資料行則包含其他資訊，例如專案屬性。</span><span class="sxs-lookup"><span data-stu-id="72c3a-179">the leftmost column contains both the item's optional icon and label, and the subsequent columns contain additional information, such as item properties.</span></span><br/> | <span data-ttu-id="72c3a-180">此外，您可以新增或移除資料行，並重新排序和調整大小。</span><span class="sxs-lookup"><span data-stu-id="72c3a-180">additionally, columns can be added or removed, and reordered and resized.</span></span> <span data-ttu-id="72c3a-181">資料列可以分組，並依資料行排序。</span><span class="sxs-lookup"><span data-stu-id="72c3a-181">rows can be grouped, sorted by column.</span></span> <br/> ![<span data-ttu-id="72c3a-182">詳細資料模式中清單視圖的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-182">screen shot of list view in details mode</span></span> ](images/ctrl-list-views-image6.png)<br/> <span data-ttu-id="72c3a-183">詳細資料檢視會將每個專案顯示為表格格式的行。</span><span class="sxs-lookup"><span data-stu-id="72c3a-183">Details view shows each item as a line in a table format.</span></span><br/>                                                              |



 

### <a name="list-view-variations"></a><span data-ttu-id="72c3a-184">清單視圖變化</span><span class="sxs-lookup"><span data-stu-id="72c3a-184">List view variations</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="72c3a-185"><strong>資料行選擇器</strong></span><span class="sxs-lookup"><span data-stu-id="72c3a-185"><strong>Column chooser</strong></span></span><br/> <span data-ttu-id="72c3a-186">清單視圖有時候會有這麼多的資料行，而不會顯示所有資料行。</span><span class="sxs-lookup"><span data-stu-id="72c3a-186">List views sometimes have so many columns that it isn't practical to show them all.</span></span> <span data-ttu-id="72c3a-187">在此情況下，最佳方法是依預設顯示最有用的資料行，並允許使用者視需要新增或移除資料行。</span><span class="sxs-lookup"><span data-stu-id="72c3a-187">In this case, the best approach is to display the most useful columns by default and allow users to add or remove columns as needed.</span></span> <br/></td>
<td><img src="images/ctrl-list-views-image7.png" alt="Screen shot of list view with Column Chooser menu " /><br/> <span data-ttu-id="72c3a-188">以滑鼠右鍵按一下資料行標題，就會顯示可讓使用者新增或移除資料行的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="72c3a-188">Right-clicking the column heading displays a context menu that allows users to add or remove columns.</span></span><br/> <img src="images/ctrl-list-views-image8.png" alt="Screen shot of Choose Details dialog box " /><br/> <span data-ttu-id="72c3a-189">在資料行標頭操作功能表中按一下 [更多]，會顯示 [選擇資料行] 對話方塊，讓使用者可以新增或移除資料行，以及重新排列資料行。</span><span class="sxs-lookup"><span data-stu-id="72c3a-189">Clicking More in the column header context menu displays the Choose Columns dialog box, which allows users to add or remove columns as well as reorder them.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72c3a-190"><strong>核取方塊清單視圖</strong></span><span class="sxs-lookup"><span data-stu-id="72c3a-190"><strong>Check box list view</strong></span></span><br/> <span data-ttu-id="72c3a-191">允許使用者選取多個專案。</span><span class="sxs-lookup"><span data-stu-id="72c3a-191">Allow users to select multiple items.</span></span><br/></td>
<td><span data-ttu-id="72c3a-192">多重選取清單視圖與單一選取清單視圖的外觀完全相同，因此沒有視覺提示可支援多重選取。</span><span class="sxs-lookup"><span data-stu-id="72c3a-192">Multiple-selection list views have exactly the same appearance as single-selection list views, so there is no visual clue that they support multiple selection.</span></span> <span data-ttu-id="72c3a-193">您可以使用核取方塊清單視圖，清楚地指出可能會有多個選取專案。</span><span class="sxs-lookup"><span data-stu-id="72c3a-193">A check box list view can be used to clearly indicate that multiple selection is possible.</span></span> <span data-ttu-id="72c3a-194">因此，您應該將此模式用於多個選取專案很重要或經常使用的工作。</span><span class="sxs-lookup"><span data-stu-id="72c3a-194">Consequently, this pattern should be used for tasks where multiple selection is essential or commonly used.</span></span><br/> <img src="images/ctrl-list-views-image9.png" alt="Screen shot of dialog box with several check boxes " /><br/> <span data-ttu-id="72c3a-195">在此範例中，小圖示視圖會使用核取方塊，因為多個選項對工作而言是不可或缺的。</span><span class="sxs-lookup"><span data-stu-id="72c3a-195">In this example, a Small Icon view uses check boxes because multiple selection is essential to the task.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72c3a-196"><strong>列出具有群組的視圖</strong></span><span class="sxs-lookup"><span data-stu-id="72c3a-196"><strong>List views with groups</strong></span></span><br/> <span data-ttu-id="72c3a-197">將資料組織成群組。</span><span class="sxs-lookup"><span data-stu-id="72c3a-197">Organize the data into groups.</span></span><br/></td>
<td><span data-ttu-id="72c3a-198">雖然詳細資料檢視通常支援依任何資料行排序資料，但清單視圖還可讓使用者將專案組織成群組。</span><span class="sxs-lookup"><span data-stu-id="72c3a-198">While Details views often support sorting the data by any of the columns, list views further allow users to organize the items into groups.</span></span> <span data-ttu-id="72c3a-199">群組的一些優點如下：</span><span class="sxs-lookup"><span data-stu-id="72c3a-199">Some benefits of grouping are:</span></span><br/>
<ul>
<li><span data-ttu-id="72c3a-200">群組會在 (清單) 以外的所有視圖中運作，因此，例如，使用者可以依演出者群組專輯的額外大型圖示觀點。</span><span class="sxs-lookup"><span data-stu-id="72c3a-200">Groups works in all views (except list), so, for example, users could group an extra large icons view of albums by artist.</span></span></li>
<li><span data-ttu-id="72c3a-201">群組可以是高層級的集合，這通常比直接從資料群組更有意義。</span><span class="sxs-lookup"><span data-stu-id="72c3a-201">Groups can be high-level collections, which are often more meaningful than grouping directly off the data.</span></span> <span data-ttu-id="72c3a-202">例如，Windows 檔案總管將日期組成今天、昨天、去年、去年和很長一段時間。</span><span class="sxs-lookup"><span data-stu-id="72c3a-202">For example, Windows Explorer groups dates into Today, Yesterday, Last week, Earlier this year, and A long time ago.</span></span></li>
</ul>
<img src="images/ctrl-list-views-image10.png" alt="Screen shot of list view with several data groups " /><br/> <span data-ttu-id="72c3a-203">在此範例中，Windows 歡迎中心會在清單視圖中顯示群組專案。</span><span class="sxs-lookup"><span data-stu-id="72c3a-203">In this example, the Windows Welcome Center shows grouped items in a list view.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="72c3a-204">指導方針</span><span class="sxs-lookup"><span data-stu-id="72c3a-204">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="72c3a-205">簡報</span><span class="sxs-lookup"><span data-stu-id="72c3a-205">Presentation</span></span>

-   <span data-ttu-id="72c3a-206">**依邏輯順序排序清單專案。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-206">**Sort list items in a logical order.**</span></span> <span data-ttu-id="72c3a-207">依字母順序排序名稱、依數位順序排序數位和日期（以時間順序排列）。</span><span class="sxs-lookup"><span data-stu-id="72c3a-207">Sort names in alphabetical order, numbers in numeric order, and dates in chronological order.</span></span>
-   <span data-ttu-id="72c3a-208">**如果有的話，可讓使用者變更排序次序。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-208">**If appropriate, allow users to change the sort order.**</span></span> <span data-ttu-id="72c3a-209">如果清單中有許多專案，或如果有使用預設值以外的排序次序更有效地找到專案，則使用者排序會很重要。</span><span class="sxs-lookup"><span data-stu-id="72c3a-209">User sorting is important if the list has many items or if there are scenarios where items are found more effectively using a sort order other than the default.</span></span>
-   <span data-ttu-id="72c3a-210">**使用 [永遠顯示選取範圍] 屬性** ，讓使用者可以輕鬆地判斷選取的專案，即使控制項沒有焦點也一樣。</span><span class="sxs-lookup"><span data-stu-id="72c3a-210">**Use the Always Show Selection attribute** so that users can readily determine the selected item, even when the control doesn't have focus.</span></span>
-   <span data-ttu-id="72c3a-211">**避免呈現空白的清單視圖。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-211">**Avoid presenting empty list views.**</span></span> <span data-ttu-id="72c3a-212">如果使用者建立清單，請使用使用者可能需要的指示或範例專案來初始化清單。</span><span class="sxs-lookup"><span data-stu-id="72c3a-212">If users create a list, initialize the list with instructions or example items that users might need.</span></span>

    ![<span data-ttu-id="72c3a-213">[搜尋] 對話方塊的螢幕擷取畫面，包含指示</span><span class="sxs-lookup"><span data-stu-id="72c3a-213">screen shot of search dialog box with instructions</span></span> ](images/ctrl-list-views-image11.png)

    <span data-ttu-id="72c3a-214">在此範例中，搜尋清單視圖一開始會顯示指示。</span><span class="sxs-lookup"><span data-stu-id="72c3a-214">In this example, the Search list view initially presents instructions.</span></span>

-   <span data-ttu-id="72c3a-215">**如果使用者可以變更視圖、群組、依資料行排序，或變更資料行及其寬度和順序，請讓這些設定持續存在，使其在下次顯示清單視圖時生效。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-215">**If users can change views, group, sort by columns, or change columns and their widths and order, make those settings persist so they take effect the next time the list view is displayed.**</span></span> <span data-ttu-id="72c3a-216">將它們保存在個別清單視圖上（每個使用者為基礎）。</span><span class="sxs-lookup"><span data-stu-id="72c3a-216">Make them persist on a per-list view, per-user basis.</span></span>

### <a name="interaction"></a><span data-ttu-id="72c3a-217">互動</span><span class="sxs-lookup"><span data-stu-id="72c3a-217">Interaction</span></span>

-   <span data-ttu-id="72c3a-218">**使用按一下滑鼠來選取使用者指向的清單專案。例外狀況：** 在 [命令連結清單] 模式中，按一下 [選取專案]，然後關閉視窗或流覽至下一個頁面。</span><span class="sxs-lookup"><span data-stu-id="72c3a-218">**Use single-click to select the list item the user is pointing to.Exception:** For the command link list pattern, single-click selects the item and either closes the window or navigates to the next page.</span></span>
-   <span data-ttu-id="72c3a-219">**請考慮提供按兩下行為。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-219">**Consider providing double-click behavior.**</span></span> <span data-ttu-id="72c3a-220">按兩下應該與選取專案並執行其預設命令的效果相同。</span><span class="sxs-lookup"><span data-stu-id="72c3a-220">Double clicking should have the same effect as selecting an item and performing its default command.</span></span>
-   <span data-ttu-id="72c3a-221">**讓按兩下行為重複。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-221">**Make double-click behavior redundant.**</span></span> <span data-ttu-id="72c3a-222">應該一律會有相同效果的命令按鈕或內容功能表命令。</span><span class="sxs-lookup"><span data-stu-id="72c3a-222">There should always be a command button or context menu command that has the same effect.</span></span>
-   <span data-ttu-id="72c3a-223">如果清單專案需要進一步說明，請 **在提示中提供說明** [。](ctrl-tooltips-and-infotips.md)</span><span class="sxs-lookup"><span data-stu-id="72c3a-223">If a list item requires further explanation, **provide the explanation in an** [infotip](ctrl-tooltips-and-infotips.md).</span></span> <span data-ttu-id="72c3a-224">使用完整的句子和結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="72c3a-224">Use complete sentences and ending punctuation.</span></span>

    ![<span data-ttu-id="72c3a-225">使用鍵盤提示顯示清單視圖的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-225">screen shot of list view with keyboard infotip</span></span> ](images/ctrl-list-views-image12.png)

    <span data-ttu-id="72c3a-226">在此範例中，會使用資訊提示來提供進一步的資訊。</span><span class="sxs-lookup"><span data-stu-id="72c3a-226">In this example, an infotip is used to provide further information.</span></span>

-   <span data-ttu-id="72c3a-227">**提供相關命令的內容功能表。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-227">**Provide context menus of relevant commands.**</span></span> <span data-ttu-id="72c3a-228">這類命令包括剪下、複製、貼上、移除或刪除、重新命名和屬性。</span><span class="sxs-lookup"><span data-stu-id="72c3a-228">Such commands include Cut, Copy, Paste, Remove or Delete, Rename, and Properties.</span></span>
-   <span data-ttu-id="72c3a-229">**如果使用者可以變更排序次序和群組，請依內容功能表提供 [排序依據] 和 [群組]。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-229">**If users can change the sort order and grouping, provide Sort By and Group By context menus.**</span></span> <span data-ttu-id="72c3a-230">第一次按一下資料行名稱，會依該資料行的遞增順序來排序或群組清單，第二次按一下會依遞減順序排序或群組。</span><span class="sxs-lookup"><span data-stu-id="72c3a-230">The first click on a column name sorts or groups the list in the ascending order for that column, the second click sorts or groups in descending order.</span></span> <span data-ttu-id="72c3a-231">使用先前的 order (從另一個資料行) 作為次要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="72c3a-231">Use the previous order (from another column) as the secondary key.</span></span>

    ![<span data-ttu-id="72c3a-232">具有 [排序依據] 功能表的清單視圖螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-232">screen shot of list view with 'sort-by' menu</span></span> ](images/ctrl-list-views-image13.png)

    <span data-ttu-id="72c3a-233">在此範例中，[排序依據] 內容功能表會變更排序次序。</span><span class="sxs-lookup"><span data-stu-id="72c3a-233">In this example, the Sort By context menu changes the sort order.</span></span> <span data-ttu-id="72c3a-234">按一下 [名稱一次]，依名稱以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="72c3a-234">Clicking Name once sorts by name in ascending order.</span></span> <span data-ttu-id="72c3a-235">再按一次 [名稱] 會以遞減順序排序。</span><span class="sxs-lookup"><span data-stu-id="72c3a-235">Clicking Name again sorts by name in descending order.</span></span>

-   <span data-ttu-id="72c3a-236">**使用鍵盤讓清單檢視列標題可供存取。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-236">**Make the list view column header accessible using the keyboard.**</span></span>
    -   <span data-ttu-id="72c3a-237">**開發人員：** 您可以藉由設定資料行標頭控制項的焦點來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="72c3a-237">**Developers:** You can do this by setting focus on the column header control.</span></span> <span data-ttu-id="72c3a-238">這項功能是 Windows Vista 的新功能。</span><span class="sxs-lookup"><span data-stu-id="72c3a-238">This capability is new to Windows Vista.</span></span>
-   <span data-ttu-id="72c3a-239">**停用清單視圖時，也會停用任何相關聯的標籤和命令按鈕。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-239">**When disabling a list view, also disable any associated labels and command buttons.**</span></span>
-   <span data-ttu-id="72c3a-240">**避免水準滾動。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-240">**Avoid horizontal scrolling.**</span></span> <span data-ttu-id="72c3a-241">清單模式使用水準滾動。</span><span class="sxs-lookup"><span data-stu-id="72c3a-241">The List mode uses horizontal scrolling.</span></span> <span data-ttu-id="72c3a-242">此模式通常是最精簡的，但水準滾動通常比垂直捲動更難使用。</span><span class="sxs-lookup"><span data-stu-id="72c3a-242">This mode is usually the most compact, but horizontal scrolling is generally harder to use than vertical scrolling.</span></span> <span data-ttu-id="72c3a-243">如果壓縮度並不重要，請考慮使用小圖示視圖。</span><span class="sxs-lookup"><span data-stu-id="72c3a-243">Consider using the Small Icon view instead if compactness isn't important.</span></span> <span data-ttu-id="72c3a-244">但是，如果有許多字母順序的專案，且有足夠的螢幕空間可供廣泛的控制項使用，則清單模式是不錯的選擇。</span><span class="sxs-lookup"><span data-stu-id="72c3a-244">However, List mode is a good choice when there are many alphabetically sorted items and sufficient screen space for a wide control.</span></span>

    <span data-ttu-id="72c3a-245">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="72c3a-245">**Acceptable:**</span></span>

    ![<span data-ttu-id="72c3a-246">寬清單模式控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-246">screen shot of a wide list-mode control</span></span> ](images/ctrl-list-views-image14.png)

    <span data-ttu-id="72c3a-247">在此範例中，會使用清單模式，因為廣泛控制項有許多專案和大量可用的螢幕空間。</span><span class="sxs-lookup"><span data-stu-id="72c3a-247">In this example, List mode is used because there are many items and plenty of available screen space for a wide control.</span></span>

### <a name="multiple-selection-lists"></a><span data-ttu-id="72c3a-248">多重選取清單</span><span class="sxs-lookup"><span data-stu-id="72c3a-248">Multiple-selection lists</span></span>

-   <span data-ttu-id="72c3a-249">**請考慮在清單下方顯示選取的專案數目**，特別是當使用者可能選取數個專案時。</span><span class="sxs-lookup"><span data-stu-id="72c3a-249">**Consider displaying the number of selected items below the list**, especially if users are likely to select several items.</span></span> <span data-ttu-id="72c3a-250">這項資訊不僅能提供有用的意見反應，也清楚指出清單視圖支援多重選取。</span><span class="sxs-lookup"><span data-stu-id="72c3a-250">This information not only gives useful feedback, but it also clearly indicates that the list view supports multiple selection.</span></span>

    ![<span data-ttu-id="72c3a-251">五個所選縮圖清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-251">screen shot of list of five selected thumbnails</span></span> ](images/ctrl-list-views-image15.png)

    <span data-ttu-id="72c3a-252">在此範例中，選取的專案數目會顯示在清單下方。</span><span class="sxs-lookup"><span data-stu-id="72c3a-252">In this example, the number of selected items is displayed below the list.</span></span>

-   <span data-ttu-id="72c3a-253">或者，您可以提供可能更有意義的其他選取範圍計量，例如選取專案所需的資源，而不是選取的專案數目。</span><span class="sxs-lookup"><span data-stu-id="72c3a-253">Alternatively instead of the number of selected items, you can give other selection metrics that might be more meaningful, such as the resources required for the selections.</span></span>

    ![<span data-ttu-id="72c3a-254">顯示磁碟空間之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-254">screen shot of dialog box showing disk space</span></span> ](images/ctrl-list-views-image16.png)

    <span data-ttu-id="72c3a-255">在此範例中，安裝元件所需的磁碟空間比選取的元件數目更有意義。</span><span class="sxs-lookup"><span data-stu-id="72c3a-255">In this example, the disk space required to install the components is more meaningful than the number of components selected.</span></span>

-   <span data-ttu-id="72c3a-256">針對核取方塊清單視圖，如果有可能有許多專案，以及選取或清除所有的專案，請加入 [全選] 和 [全部清除] 命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="72c3a-256">For check box list views, if there are potentially many items and selecting or clearing all of them is likely, add Select all and Clear all command buttons.</span></span>
-   <span data-ttu-id="72c3a-257">**使用混合狀態核取方塊來指出部分在容器中選取專案。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-257">**Use mixed-state check boxes to indicate partial selection of the items in a container.**</span></span> <span data-ttu-id="72c3a-258">混合狀態不會當做個別專案的第三個狀態使用。</span><span class="sxs-lookup"><span data-stu-id="72c3a-258">The mixed state is not used as a third state for an individual item.</span></span>

### <a name="changing-views"></a><span data-ttu-id="72c3a-259">變更視圖</span><span class="sxs-lookup"><span data-stu-id="72c3a-259">Changing views</span></span>

<span data-ttu-id="72c3a-260">如果使用者可以變更 views：</span><span class="sxs-lookup"><span data-stu-id="72c3a-260">If users can change views:</span></span>

-   <span data-ttu-id="72c3a-261">**依預設，選擇最方便的視圖。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-261">**Choose the most convenient view by default.**</span></span> <span data-ttu-id="72c3a-262">使用者所做的任何變更，都應該以每個清單的每個使用者為基礎來持續保存。</span><span class="sxs-lookup"><span data-stu-id="72c3a-262">Any changes users make should be made persistent on a per-list view, per-user basis.</span></span>
-   <span data-ttu-id="72c3a-263">**使用分割按鈕、功能表按鈕或下拉式清單來變更視圖。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-263">**Change the view using a split button, menu button, or drop-down list.**</span></span> <span data-ttu-id="72c3a-264">只要可行，請使用工具列上的 [ [分割] 按鈕](ctrl-command-buttons.md) ，然後變更按鈕標籤以反映目前的視圖。</span><span class="sxs-lookup"><span data-stu-id="72c3a-264">Whenever practical, use a [split button](ctrl-command-buttons.md) on the toolbar and change the button label to reflect the current view.</span></span>

    ![<span data-ttu-id="72c3a-265">具有分割 [views] 按鈕的清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-265">screen shot of list with split 'views' button</span></span> ](images/ctrl-list-views-image17.png)

    <span data-ttu-id="72c3a-266">在此範例中，工具列上的 [分割] 按鈕可用來變更視圖。</span><span class="sxs-lookup"><span data-stu-id="72c3a-266">In this example, a split button on the toolbar is used to change views.</span></span>

-   <span data-ttu-id="72c3a-267">**提供 View 內容功能表。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-267">**Provide a View context menu.**</span></span>

    ![<span data-ttu-id="72c3a-268">具有 [view] 內容功能表的 [清單] 螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-268">screen shot of list with 'view' context menu</span></span> ](images/ctrl-list-views-image18.png)

<span data-ttu-id="72c3a-269">在此範例中，會使用視圖內容功能表來變更視圖。</span><span class="sxs-lookup"><span data-stu-id="72c3a-269">In this example, a View context menu is used to change views.</span></span>

### <a name="details-views"></a><span data-ttu-id="72c3a-270">詳細資料檢視</span><span class="sxs-lookup"><span data-stu-id="72c3a-270">Details views</span></span>

-   <span data-ttu-id="72c3a-271">**請考慮使用圖格視圖來改善可讀性。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-271">**Consider using tiles view to improve readability.**</span></span>

    <span data-ttu-id="72c3a-272">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="72c3a-272">**Acceptable:**</span></span>

    ![<span data-ttu-id="72c3a-273">具有窄欄的詳細資料清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-273">screen shot of details list with narrow columns</span></span> ](images/ctrl-list-views-image19.png)

    <span data-ttu-id="72c3a-274">在此範例中，有太多資料，且視窗、清單和資料行太小，使得清單專案難以讀取。</span><span class="sxs-lookup"><span data-stu-id="72c3a-274">In this example, there is too much data and the window, list, and columns are too small, making the list items hard to read.</span></span>

    <span data-ttu-id="72c3a-275">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="72c3a-275">**Better:**</span></span>

    ![<span data-ttu-id="72c3a-276">群組中資料的詳細資料清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-276">screen shot of details list with data in groups</span></span> ](images/ctrl-list-views-image20.png)

    <span data-ttu-id="72c3a-277">在此範例中，磚視圖會顯示資料，而不進行截斷。</span><span class="sxs-lookup"><span data-stu-id="72c3a-277">In this example, Tile view displays the data without truncation.</span></span>

-   <span data-ttu-id="72c3a-278">**選擇最長資料適用的預設資料行寬度。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-278">**Choose default column widths appropriate for the longest data.**</span></span> <span data-ttu-id="72c3a-279">清單視圖會自動以省略號截斷長資料，因此，如果預設顯示一些省略號，則資料行寬度是適當的。</span><span class="sxs-lookup"><span data-stu-id="72c3a-279">List views automatically truncate long data with ellipses, so the column widths are appropriate if few ellipses are displayed by default.</span></span> <span data-ttu-id="72c3a-280">雖然使用者可以調整資料行的大小，但偏好使用其他方案：</span><span class="sxs-lookup"><span data-stu-id="72c3a-280">While users can resize columns, prefer other solutions:</span></span>

    -   <span data-ttu-id="72c3a-281">調整每個資料行寬度以容納其資料。</span><span class="sxs-lookup"><span data-stu-id="72c3a-281">Size each column width to fit its data.</span></span>
    -   <span data-ttu-id="72c3a-282">調整控制項寬度以容納其資料行，再加上任何可能的捲軸。</span><span class="sxs-lookup"><span data-stu-id="72c3a-282">Size the control width to fit its columns plus any likely scrollbars.</span></span>
    -   <span data-ttu-id="72c3a-283">如有必要，請使用水準滾動。</span><span class="sxs-lookup"><span data-stu-id="72c3a-283">If necessary, use horizontal scrolling.</span></span>
    -   <span data-ttu-id="72c3a-284">只有奇數個專案或最後手段有截斷的資料。</span><span class="sxs-lookup"><span data-stu-id="72c3a-284">Have truncated data only for odd-sized items or as a last resort.</span></span>

    <span data-ttu-id="72c3a-285">如果預設的一般大小資料必須截斷，請讓視窗和清單視圖變成可調整大小。</span><span class="sxs-lookup"><span data-stu-id="72c3a-285">If normal-sized data must be truncated by default, make the window and list view resizable.</span></span> <span data-ttu-id="72c3a-286">包含額外的 30% (高達200% 的文字，以提供任何文字 (較短的文字) ，而不是) 將當地語系化的數位。</span><span class="sxs-lookup"><span data-stu-id="72c3a-286">Include an additional 30 percent (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span>

    <span data-ttu-id="72c3a-287">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="72c3a-287">**Incorrect:**</span></span>

    ![<span data-ttu-id="72c3a-288">清單資料行的螢幕擷取畫面，其中包含截斷的資料</span><span class="sxs-lookup"><span data-stu-id="72c3a-288">screen shot of list columns with truncated data</span></span> ](images/ctrl-list-views-image21.png)

    <span data-ttu-id="72c3a-289">在此範例中，大部分的資料會被截斷。</span><span class="sxs-lookup"><span data-stu-id="72c3a-289">In this example, most data is truncated.</span></span> <span data-ttu-id="72c3a-290">許多橢圓形顯然指出控制項和資料行寬度對資料而言太小。</span><span class="sxs-lookup"><span data-stu-id="72c3a-290">The many ellipses clearly indicate that the control and column widths are too small for the data.</span></span>

    <span data-ttu-id="72c3a-291">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="72c3a-291">**Incorrect:**</span></span>

    ![<span data-ttu-id="72c3a-292">具有截斷資料的單一資料行清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-292">screen shot of one-column list with truncated data</span></span> ](images/ctrl-list-views-image22.png)

    <span data-ttu-id="72c3a-293">在此範例中，資料會被截斷而沒有原因。</span><span class="sxs-lookup"><span data-stu-id="72c3a-293">In this example, data is truncated without reason.</span></span>

-   <span data-ttu-id="72c3a-294">**選擇適當的預設資料行順序。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-294">**Choose an appropriate default column order.**</span></span> <span data-ttu-id="72c3a-295">一般而言，依照下列方式排序資料行：</span><span class="sxs-lookup"><span data-stu-id="72c3a-295">Generally, order the columns as follows:</span></span>

    -   <span data-ttu-id="72c3a-296">首先，專案名稱或識別資料。</span><span class="sxs-lookup"><span data-stu-id="72c3a-296">First, the item name or identifying data.</span></span>
    -   <span data-ttu-id="72c3a-297">接下來，其他資料在區分清單專案時很有説明。</span><span class="sxs-lookup"><span data-stu-id="72c3a-297">Next, other data useful in differentiating the list items.</span></span>
    -   <span data-ttu-id="72c3a-298">接下來，最有用的 (最好的簡短或固定長度) 資料。</span><span class="sxs-lookup"><span data-stu-id="72c3a-298">Next, the most useful (preferably short or fixed length) data.</span></span>
    -   <span data-ttu-id="72c3a-299">接下來， (慣用的簡短或固定長度) 資料較不實用。</span><span class="sxs-lookup"><span data-stu-id="72c3a-299">Next, less useful (preferable short or fixed length) data.</span></span>
    -   <span data-ttu-id="72c3a-300">Last、long、可變長度的資料。</span><span class="sxs-lookup"><span data-stu-id="72c3a-300">Last, long, variable-length data.</span></span>

    <span data-ttu-id="72c3a-301">Long、variable 長度-資料會放在最後一個資料行中，以減少水準滾動的需求。</span><span class="sxs-lookup"><span data-stu-id="72c3a-301">Long, variable length-data is placed in the last columns to reduce the need for horizontal scrolling.</span></span> <span data-ttu-id="72c3a-302">在這些類別中，將相關的資訊放在邏輯順序中。</span><span class="sxs-lookup"><span data-stu-id="72c3a-302">Within these categories, place related information together in a logical sequence.</span></span>

-   <span data-ttu-id="72c3a-303">**適當時，允許使用者新增和移除資料行，以及變更順序。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-303">**When appropriate, allow users to add and remove columns, as well as change the order.**</span></span> <span data-ttu-id="72c3a-304">預設會顯示最有用的資料行。</span><span class="sxs-lookup"><span data-stu-id="72c3a-304">Display the most useful columns by default.</span></span> <span data-ttu-id="72c3a-305">這可透過標頭拖放屬性來達成。</span><span class="sxs-lookup"><span data-stu-id="72c3a-305">This is achieved with the Header Drag Drop attribute.</span></span>
-   <span data-ttu-id="72c3a-306">選擇適合資料的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="72c3a-306">Choose an alignment appropriate for the data.</span></span> <span data-ttu-id="72c3a-307">使用下列規則：</span><span class="sxs-lookup"><span data-stu-id="72c3a-307">Use the following rules:</span></span>
    -   <span data-ttu-id="72c3a-308">靠右對齊數位、貨幣和時間。</span><span class="sxs-lookup"><span data-stu-id="72c3a-308">Right-align numbers, currencies, and times.</span></span>
    -   <span data-ttu-id="72c3a-309">將文字、識別碼靠左對齊，即使數值) 和日期也 (。</span><span class="sxs-lookup"><span data-stu-id="72c3a-309">Left-align text, IDs (even if numeric), and dates.</span></span>
-   <span data-ttu-id="72c3a-310">針對可排序的資料行標題， **第一次按一下標題會以遞增順序排序資料行的清單，第二次按一下則會以遞減順序排序。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-310">For sortable column headings, **the first click on a heading sorts the list in ascending order for the column, the second click sorts in descending order.**</span></span> <span data-ttu-id="72c3a-311">使用先前的排序次序 (從另一個資料行) 做為次要排序索引鍵。</span><span class="sxs-lookup"><span data-stu-id="72c3a-311">Use the previous sort order (from another column) as the secondary sort key.</span></span>

    ![<span data-ttu-id="72c3a-312">已排序資料的詳細資料清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-312">screen shot of details list with sorted data</span></span> ](images/ctrl-list-views-image23.png)

    <span data-ttu-id="72c3a-313">在此範例中，先按一下 [名稱] 資料行，然後按一下 [類型] 資料行。</span><span class="sxs-lookup"><span data-stu-id="72c3a-313">In this example, the Name column was clicked first, then the Type column.</span></span> <span data-ttu-id="72c3a-314">因此，以遞增順序輸入的是主要排序索引鍵，而名稱的遞增順序則是次要。</span><span class="sxs-lookup"><span data-stu-id="72c3a-314">As a result, Type in ascending order is the primary sort key, and Name in ascending order is the secondary.</span></span>

-   <span data-ttu-id="72c3a-315">**使用 Full Row Select 屬性** ，讓使用者可以輕鬆地判斷所有資料行中選取的專案。</span><span class="sxs-lookup"><span data-stu-id="72c3a-315">**Use the Full Row Select attribute** so that users can readily determine the selected items in all columns.</span></span>
-   <span data-ttu-id="72c3a-316">**除非資料可以排序，否則請勿使用可排序的資料行標題。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-316">**Don't use a sortable column header unless the data can be sorted.**</span></span>
-   <span data-ttu-id="72c3a-317">**如果只有一個資料行，而且不需要反向排序，請不要使用資料行標頭。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-317">**Don't use a column header if there is only one column and there is no need to reverse sort.**</span></span> <span data-ttu-id="72c3a-318">請改用標籤來識別資料。</span><span class="sxs-lookup"><span data-stu-id="72c3a-318">Use a label instead to identify the data.</span></span>

    <span data-ttu-id="72c3a-319">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="72c3a-319">**Incorrect:**</span></span>

    ![<span data-ttu-id="72c3a-320">欄標題中具有標籤的清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-320">screen shot of list with label in column header</span></span> ](images/ctrl-list-views-image24.png)

    <span data-ttu-id="72c3a-321">**正確：**</span><span class="sxs-lookup"><span data-stu-id="72c3a-321">**Correct:**</span></span>

    ![<span data-ttu-id="72c3a-322">控制項上方具有標籤清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-322">screen shot of list with label above the control</span></span> ](images/ctrl-list-views-image25.png)

    <span data-ttu-id="72c3a-323">在正確的範例中，會使用標籤，而不是資料行標頭。</span><span class="sxs-lookup"><span data-stu-id="72c3a-323">In the correct example, a label is used instead of a column header.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="72c3a-324">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="72c3a-324">Recommended sizing and spacing</span></span>

![<span data-ttu-id="72c3a-325">清單大小和間距的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-325">screen shot of list sizing and spacing</span></span> ](images/ctrl-list-views-image26.png)

<span data-ttu-id="72c3a-326">清單視圖的建議大小和間距。</span><span class="sxs-lookup"><span data-stu-id="72c3a-326">Recommended sizing and spacing for list views.</span></span>

-   <span data-ttu-id="72c3a-327">**選擇顯示整數專案數目的清單視圖高度。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-327">**Choose a list view height that displays an integral number of items.**</span></span> <span data-ttu-id="72c3a-328">避免垂直截斷專案。</span><span class="sxs-lookup"><span data-stu-id="72c3a-328">Avoid truncating items vertically.</span></span>
-   <span data-ttu-id="72c3a-329">**選擇可在所有支援的視圖中消除不必要垂直和水準滾動的清單視圖大小。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-329">**Choose a list view size that eliminates unnecessary vertical and horizontal scrolling in all supported views.**</span></span> <span data-ttu-id="72c3a-330">清單視圖應顯示3到20個專案。</span><span class="sxs-lookup"><span data-stu-id="72c3a-330">List views should display between 3 and 20 items.</span></span> <span data-ttu-id="72c3a-331">如果這樣做會消除捲軸，請考慮讓清單視圖稍微放大。</span><span class="sxs-lookup"><span data-stu-id="72c3a-331">Consider making a list view slightly larger if doing so eliminates a scroll bar.</span></span> <span data-ttu-id="72c3a-332">可能有多個專案的清單應該會顯示至少五個專案，藉由一次顯示更多專案，並讓捲軸更容易放置，來加速滾動。</span><span class="sxs-lookup"><span data-stu-id="72c3a-332">Lists with potentially many items should display at least five items to facilitate scrolling by showing more items at a time and making the scroll bar easier to position.</span></span>
-   <span data-ttu-id="72c3a-333">**如果使用者受益于使清單視圖更大，請讓清單視圖和其父視窗可調整大小。**</span><span class="sxs-lookup"><span data-stu-id="72c3a-333">**If users benefit from making the list view larger, make the list view and its parent window resizable.**</span></span> <span data-ttu-id="72c3a-334">這麼做可讓使用者視需要調整清單視圖大小。</span><span class="sxs-lookup"><span data-stu-id="72c3a-334">Doing so allows users to adjust the list view size as needed.</span></span> <span data-ttu-id="72c3a-335">不過，可調整大小的清單視圖應該只顯示三個以上的專案。</span><span class="sxs-lookup"><span data-stu-id="72c3a-335">However, resizable list views should display no fewer than three items.</span></span>

## <a name="labels"></a><span data-ttu-id="72c3a-336">標籤</span><span class="sxs-lookup"><span data-stu-id="72c3a-336">Labels</span></span>

### <a name="control-labels"></a><span data-ttu-id="72c3a-337">控制項標籤</span><span class="sxs-lookup"><span data-stu-id="72c3a-337">Control labels</span></span>

-   <span data-ttu-id="72c3a-338">所有清單視圖都需要標籤。</span><span class="sxs-lookup"><span data-stu-id="72c3a-338">All list views need labels.</span></span> <span data-ttu-id="72c3a-339">以單字或片語撰寫標籤，而非句子，以使用靜態文字的冒號結尾。</span><span class="sxs-lookup"><span data-stu-id="72c3a-339">Write the label as a word or phrase, not as a sentence, ending with a colon using static text.</span></span>
-   <span data-ttu-id="72c3a-340">為每個標籤指派唯一的 [存取金鑰](glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="72c3a-340">Assign a unique [access key](glossary.md) for each label.</span></span> <span data-ttu-id="72c3a-341">如需指導方針，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="72c3a-341">For guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="72c3a-342">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="72c3a-342">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="72c3a-343">將標籤置於控制項上方，並將標籤與控制項的左邊緣對齊。</span><span class="sxs-lookup"><span data-stu-id="72c3a-343">Position the label above the control and align the label with the left edge of the control.</span></span>
-   <span data-ttu-id="72c3a-344">若為多重選取清單視圖，請撰寫明確指出可能有多重選取的標籤。</span><span class="sxs-lookup"><span data-stu-id="72c3a-344">For multiple-selection list views, write the label that clearly indicates multiple selection is possible.</span></span> <span data-ttu-id="72c3a-345">核取方塊清單視圖標籤可能較不明確。</span><span class="sxs-lookup"><span data-stu-id="72c3a-345">Check box list view labels can be less explicit.</span></span>

    <span data-ttu-id="72c3a-346">**正確：**</span><span class="sxs-lookup"><span data-stu-id="72c3a-346">**Correct:**</span></span>

    ![<span data-ttu-id="72c3a-347">標籤的螢幕擷取畫面：選取一或多個附加元件</span><span class="sxs-lookup"><span data-stu-id="72c3a-347">screen shot of label: select one or more add-ons</span></span> ](images/ctrl-list-views-image27.png)

    <span data-ttu-id="72c3a-348">在此範例中，標籤會清楚指出可能會有多個選取專案。</span><span class="sxs-lookup"><span data-stu-id="72c3a-348">In this example, the label clearly indicates that multiple selection is possible.</span></span>

    <span data-ttu-id="72c3a-349">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="72c3a-349">**Incorrect:**</span></span>

    ![<span data-ttu-id="72c3a-350">標籤：附加元件的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="72c3a-350">screen shot of label: add-ons</span></span> ](images/ctrl-list-views-image28.png)

    <span data-ttu-id="72c3a-351">在此範例中，標籤不會提供多個選取專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="72c3a-351">In this example, the label provides no information about multiple selection.</span></span>

    <span data-ttu-id="72c3a-352">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="72c3a-352">**Acceptable:**</span></span>

    ![<span data-ttu-id="72c3a-353">核取方塊清單標籤的螢幕擷取畫面：附加元件</span><span class="sxs-lookup"><span data-stu-id="72c3a-353">screen shot of check-box list label: add-ons</span></span> ](images/ctrl-list-views-image29.png)

    <span data-ttu-id="72c3a-354">在此範例中，核取方塊會清楚指出可能有多重選取，因此標籤不需要明確。</span><span class="sxs-lookup"><span data-stu-id="72c3a-354">In this example, the check boxes clearly indicate that multiple selection is possible, so the label doesn't have to be explicit.</span></span>

-   <span data-ttu-id="72c3a-355">您可以在標籤後面的括弧中，指定單位 (秒、連接等) 。</span><span class="sxs-lookup"><span data-stu-id="72c3a-355">You may specify units (seconds, connections, and so on) in parentheses after the label.</span></span>

### <a name="heading-labels"></a><span data-ttu-id="72c3a-356">標題標籤</span><span class="sxs-lookup"><span data-stu-id="72c3a-356">Heading labels</span></span>

-   <span data-ttu-id="72c3a-357">讓標題標籤簡短 (三個單字或較少的) 。</span><span class="sxs-lookup"><span data-stu-id="72c3a-357">Keep the heading labels brief (three words or fewer).</span></span>
-   <span data-ttu-id="72c3a-358">使用不含結束標點符號的單一名詞或名詞片語。</span><span class="sxs-lookup"><span data-stu-id="72c3a-358">Use a single noun or noun phrase with no ending punctuation.</span></span>
-   <span data-ttu-id="72c3a-359">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="72c3a-359">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="72c3a-360">讓標題的對齊方式與資料相同。</span><span class="sxs-lookup"><span data-stu-id="72c3a-360">Align the heading the same way as the data.</span></span>

### <a name="group-labels"></a><span data-ttu-id="72c3a-361">群組標籤</span><span class="sxs-lookup"><span data-stu-id="72c3a-361">Group labels</span></span>

-   <span data-ttu-id="72c3a-362">針對高層級的集合，請使用下列群組標籤：</span><span class="sxs-lookup"><span data-stu-id="72c3a-362">Use the following group labels for high-level collections:</span></span>
    -   <span data-ttu-id="72c3a-363">名稱：使用名字或字母範圍的第一個字母。</span><span class="sxs-lookup"><span data-stu-id="72c3a-363">Names: Use first letter of name or letter ranges.</span></span>
    -   <span data-ttu-id="72c3a-364">大小：未指定、0 KB、0-10 KB、10-100 KB、100 KB-1 MB、1-16 MB、16-128 MB</span><span class="sxs-lookup"><span data-stu-id="72c3a-364">Sizes: Unspecified, 0 KB, 0-10 KB, 10-100 KB, 100 KB - 1 MB, 1-16 MB, 16-128 MB</span></span>
    -   <span data-ttu-id="72c3a-365">日期：今天、昨天、過去一周、今年之前和很長一段時間。</span><span class="sxs-lookup"><span data-stu-id="72c3a-365">Dates: Today, Yesterday, Last week, Earlier this year, and A long time ago.</span></span>
-   <span data-ttu-id="72c3a-366">否則，群組標籤會使用要分組之資料的確切文字，包括大小寫和標點符號。</span><span class="sxs-lookup"><span data-stu-id="72c3a-366">Otherwise, group labels use the exact text of the data being grouped, including capitalization and punctuation.</span></span>

### <a name="data-text"></a><span data-ttu-id="72c3a-367">資料文字</span><span class="sxs-lookup"><span data-stu-id="72c3a-367">Data text</span></span>

-   <span data-ttu-id="72c3a-368">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="72c3a-368">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="instructional-text"></a><span data-ttu-id="72c3a-369">教學文字</span><span class="sxs-lookup"><span data-stu-id="72c3a-369">Instructional text</span></span>

-   <span data-ttu-id="72c3a-370">如果您需要新增有關清單視圖的解說文字，請將它加入標籤上方。</span><span class="sxs-lookup"><span data-stu-id="72c3a-370">If you need to add instructional text about a list view, add it above the label.</span></span> <span data-ttu-id="72c3a-371">使用結尾標點符號的完整句子。</span><span class="sxs-lookup"><span data-stu-id="72c3a-371">Use complete sentences with ending punctuation.</span></span>
-   <span data-ttu-id="72c3a-372">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="72c3a-372">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="72c3a-373">有説明但不需要的其他資訊應該保持簡短。</span><span class="sxs-lookup"><span data-stu-id="72c3a-373">Additional information that is helpful but not necessary should be kept short.</span></span> <span data-ttu-id="72c3a-374">請將這項資訊放在標籤和冒號之間的括弧內，或在控制項下方的括弧之外。</span><span class="sxs-lookup"><span data-stu-id="72c3a-374">Place this information either in parentheses between the label and colon or without parentheses below the control.</span></span>

## <a name="documentation"></a><span data-ttu-id="72c3a-375">文件</span><span class="sxs-lookup"><span data-stu-id="72c3a-375">Documentation</span></span>

<span data-ttu-id="72c3a-376">參考清單視圖時：</span><span class="sxs-lookup"><span data-stu-id="72c3a-376">When referring to list views:</span></span>

-   <span data-ttu-id="72c3a-377">使用確切的標籤文字（包含其大小寫，但不包含存取金鑰底線或冒號），並包含字組清單。</span><span class="sxs-lookup"><span data-stu-id="72c3a-377">Use the exact label text including its capitalization but don't include the access key underscore or colon, and include the word list.</span></span> <span data-ttu-id="72c3a-378">請勿以清單方塊、清單視圖或欄位形式來參考清單方塊。</span><span class="sxs-lookup"><span data-stu-id="72c3a-378">Don't refer to a list box as a list box, list view, or field.</span></span>
-   <span data-ttu-id="72c3a-379">針對清單資料，請使用確切的資料文字，包括其大小寫。</span><span class="sxs-lookup"><span data-stu-id="72c3a-379">For list data, use the exact data text including its capitalization.</span></span>
-   <span data-ttu-id="72c3a-380">在程式設計和其他技術檔中，請將清單視圖稱為清單視圖。</span><span class="sxs-lookup"><span data-stu-id="72c3a-380">Refer to list views as list views only in programming and other technical documentation.</span></span> <span data-ttu-id="72c3a-381">其他地方使用 list。</span><span class="sxs-lookup"><span data-stu-id="72c3a-381">Everywhere else use list.</span></span>
-   <span data-ttu-id="72c3a-382">若要描述使用者互動，請針對資料使用 [選取]，然後按一下以取得標題。</span><span class="sxs-lookup"><span data-stu-id="72c3a-382">To describe user interaction, use select for the data, and click for the headings.</span></span>
-   <span data-ttu-id="72c3a-383">可能的話，請使用粗體文字來格式化標籤和清單選項。</span><span class="sxs-lookup"><span data-stu-id="72c3a-383">When possible, format the label and list options using bold text.</span></span> <span data-ttu-id="72c3a-384">否則，請只在必要時才將標籤和選項放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="72c3a-384">Otherwise, put the label and options in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="72c3a-385">範例：在 [ **程式和服務** ] 清單中，選取 [檔案 **和印表機共用**]。</span><span class="sxs-lookup"><span data-stu-id="72c3a-385">Example: In the **Programs and services** list, select **File and printer sharing**.</span></span>

<span data-ttu-id="72c3a-386">在清單視圖中參考核取方塊時：</span><span class="sxs-lookup"><span data-stu-id="72c3a-386">When referring to check boxes in a list view:</span></span>

-   <span data-ttu-id="72c3a-387">使用確切的標籤文字（包含其大小寫），並包含 [單字] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="72c3a-387">Use the exact label text including its capitalization, and include the word check box.</span></span> <span data-ttu-id="72c3a-388">請勿包含存取金鑰底線。</span><span class="sxs-lookup"><span data-stu-id="72c3a-388">Don't include the access key underscore.</span></span>
-   <span data-ttu-id="72c3a-389">若要描述使用者互動，請使用選取和清除。</span><span class="sxs-lookup"><span data-stu-id="72c3a-389">To describe user interaction, use select and clear.</span></span>
-   <span data-ttu-id="72c3a-390">可能的話，請使用粗體文字來格式化標籤。</span><span class="sxs-lookup"><span data-stu-id="72c3a-390">When possible, format the label using bold text.</span></span> <span data-ttu-id="72c3a-391">否則，請只在必要時才將標籤放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="72c3a-391">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="72c3a-392">範例： **選取 [底線** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="72c3a-392">Example: Select the **Underline** check box.</span></span>

 

