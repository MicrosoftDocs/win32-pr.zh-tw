---
title: 定位點
description: 索引標籤可讓您在個別標記的頁面上顯示相關的資訊。
ms.assetid: d90228ce-aa95-4359-be8e-ea2014d71ae6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b2649862885e55bdfe10fdca7f34b7618d976a38
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104560555"
---
# <a name="tabs"></a><span data-ttu-id="50a75-103">定位點</span><span class="sxs-lookup"><span data-stu-id="50a75-103">Tabs</span></span>

> [!NOTE]
> <span data-ttu-id="50a75-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="50a75-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="50a75-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="50a75-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="50a75-106">索引標籤可讓您在個別標記的頁面上顯示相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="50a75-106">Tabs provide a way to present related information on separate labeled pages.</span></span>

![<span data-ttu-id="50a75-107">五個索引標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-107">screen shot of five tabs</span></span> ](images/ctrl-tabs-image1.png)

<span data-ttu-id="50a75-108">一組一般的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-108">A typical set of tabs.</span></span>

<span data-ttu-id="50a75-109">索引標籤通常會與屬性視窗 (相關聯，反之亦然) ，不過，您可以在任何類型的視窗中使用 tab 鍵。</span><span class="sxs-lookup"><span data-stu-id="50a75-109">Tabs are usually associated with property windows (and vice versa), but tabs can be used in any type of window.</span></span>

<span data-ttu-id="50a75-110">索引標籤控制項代表索引標籤式馬尼拉資料夾，用來組織通常位於美國的檔櫃中的資訊。</span><span class="sxs-lookup"><span data-stu-id="50a75-110">Tab controls represent the tabbed manila folders used to organize information in filing cabinets commonly found in the United States.</span></span> <span data-ttu-id="50a75-111"> (不會在全球使用的馬尼拉資料夾。 ) </span><span class="sxs-lookup"><span data-stu-id="50a75-111">(Manila folders aren't used worldwide.)</span></span>

> [!Note]  
> <span data-ttu-id="50a75-112">與 [版面](vis-layout.md)配置、索引標籤 [功能表](cmd-menus.md)、 [對話方塊](win-dialog-box.md)和 [屬性視窗](win-property-win.md) 相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="50a75-112">Guidelines related to [layout](vis-layout.md), [tab menus](cmd-menus.md), [dialog boxes](win-dialog-box.md), and [property windows](win-property-win.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="50a75-113">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="50a75-113">Is this the right control?</span></span>

<span data-ttu-id="50a75-114">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="50a75-114">To decide, consider these questions:</span></span>

-   <span data-ttu-id="50a75-115">**控制項可以在單一、合理大小的頁面上輕鬆容納嗎？**</span><span class="sxs-lookup"><span data-stu-id="50a75-115">**Can the controls comfortably fit on a single, reasonably sized page?**</span></span> <span data-ttu-id="50a75-116">若是如此，請使用單一頁面。</span><span class="sxs-lookup"><span data-stu-id="50a75-116">If so, use a single page.</span></span>
-   <span data-ttu-id="50a75-117">**是否只有一個索引標籤？**</span><span class="sxs-lookup"><span data-stu-id="50a75-117">**Is there only one tab?**</span></span> <span data-ttu-id="50a75-118">若是如此，請使用單一頁面。</span><span class="sxs-lookup"><span data-stu-id="50a75-118">If so, use a single page.</span></span>
-   <span data-ttu-id="50a75-119">**這些索引標籤是否以某種方式彼此相關？**</span><span class="sxs-lookup"><span data-stu-id="50a75-119">**Are the tabs related to each other in some obvious way?**</span></span> <span data-ttu-id="50a75-120">如果沒有，請考慮將資訊分割成個別的相關資訊視窗。</span><span class="sxs-lookup"><span data-stu-id="50a75-120">If not, consider splitting the information into separate windows of related information.</span></span>
-   <span data-ttu-id="50a75-121">**如果用於設定，不同頁面上的設定是否完全獨立？**</span><span class="sxs-lookup"><span data-stu-id="50a75-121">**If used for settings, are settings on different pages completely independent?**</span></span> <span data-ttu-id="50a75-122">變更一個頁面上的設定會影響其他頁面上的設定嗎？</span><span class="sxs-lookup"><span data-stu-id="50a75-122">Will changing a setting on one page affect settings on other pages?</span></span> <span data-ttu-id="50a75-123">如果它們不是獨立的，請改用工作頁面或 [wizard](win-wizards.md) 。</span><span class="sxs-lookup"><span data-stu-id="50a75-123">If they're not independent, use task pages or a [wizard](win-wizards.md) instead.</span></span>
-   <span data-ttu-id="50a75-124">**索引標籤大多對等，還是有階層式關聯性？**</span><span class="sxs-lookup"><span data-stu-id="50a75-124">**Are the tabs mostly peers of each other, or is there a hierarchical relationship?**</span></span> <span data-ttu-id="50a75-125">如果有階層，請考慮使用漸進式洩漏或子 [對話方塊](win-dialog-box.md) 來顯示相關資訊。</span><span class="sxs-lookup"><span data-stu-id="50a75-125">If hierarchical, consider using progressive disclosure or child [dialog boxes](win-dialog-box.md) to show related information.</span></span>
-   <span data-ttu-id="50a75-126">**索引標籤是用來顯示工作內的步驟嗎？**</span><span class="sxs-lookup"><span data-stu-id="50a75-126">**Are the tabs used to display steps within a task?**</span></span> <span data-ttu-id="50a75-127">您可以使用「索引標籤」來顯示工作中的步驟（如果這些步驟的外觀類似步驟），而且有明顯的替代方式可進入文字步驟，例如 [下一步] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="50a75-127">You can use "tabs" to display steps within a task only if they are presented to look like steps, and there is an obvious, alternative way to get to the text step, such as a Next button.</span></span> <span data-ttu-id="50a75-128">否則，如果需要這些步驟，請使用頁面流程或 [wizard](win-wizards.md)中的頁面。</span><span class="sxs-lookup"><span data-stu-id="50a75-128">Otherwise, if the steps are required, use pages in a page flow or a [wizard](win-wizards.md).</span></span> <span data-ttu-id="50a75-129">如果步驟是選擇性的，請改為使用模式 [對話方塊](win-dialog-box.md) 來顯示選擇性的步驟。</span><span class="sxs-lookup"><span data-stu-id="50a75-129">If the steps are optional, display the optional steps using modal [dialog boxes](win-dialog-box.md) instead.</span></span>
-   <span data-ttu-id="50a75-130">**索引標籤是否會有相同資料的不同觀點？**</span><span class="sxs-lookup"><span data-stu-id="50a75-130">**Are the tabs different views of the same data?**</span></span> <span data-ttu-id="50a75-131">如果是的話，請考慮使用 [分割按鈕](ctrl-command-buttons.md) 或 [下拉式清單](/windows/desktop/uxguide/ctrl-drop) 來變更 views。</span><span class="sxs-lookup"><span data-stu-id="50a75-131">If so, consider using a [split button](ctrl-command-buttons.md) or [drop-down list](/windows/desktop/uxguide/ctrl-drop) to change views.</span></span> <span data-ttu-id="50a75-132">雖然您可以有效地使用索引標籤來變更視圖，但替代方案更輕量。</span><span class="sxs-lookup"><span data-stu-id="50a75-132">While tabs can be used effectively for changing views, the alternatives are more lightweight.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="50a75-133">使用模式</span><span class="sxs-lookup"><span data-stu-id="50a75-133">Usage patterns</span></span>

<span data-ttu-id="50a75-134">索引標籤有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="50a75-134">Tabs have several usage patterns:</span></span>



|                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50a75-135">**動態視窗介面**</span><span class="sxs-lookup"><span data-stu-id="50a75-135">**Dynamic window surface**</span></span><br/> <span data-ttu-id="50a75-136">和捲軸一樣，索引標籤可以用來增加視窗介面區，以顯示相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="50a75-136">like scroll bars, tabs can be used to increase the window surface area to show related information.</span></span><br/>                                                    | <span data-ttu-id="50a75-137">使用這個模式時，使用索引標籤的概念類似于在單一可滾動表面上以線性方式將所有資訊放在索引標籤上，並以索引標籤標籤作為標題。</span><span class="sxs-lookup"><span data-stu-id="50a75-137">With this pattern, using tabs is conceptually similar to placing all the information on the tabs linearly on a single scrollable surface, with the tab labels as headings.</span></span> <br/> ![<span data-ttu-id="50a75-138">五個索引標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-138">screen shot of five tabs</span></span> ](images/ctrl-tabs-image1.png)<br/> <span data-ttu-id="50a75-139">在此範例中，索引標籤會有效地增加視窗介面區域。</span><span class="sxs-lookup"><span data-stu-id="50a75-139">In this example, tabs effectively increase the window surface area.</span></span><br/>                          |
| <span data-ttu-id="50a75-140">**多重檢視**</span><span class="sxs-lookup"><span data-stu-id="50a75-140">**Multiple views**</span></span><br/> <span data-ttu-id="50a75-141">就像分割按鈕或下拉式清單一樣，索引標籤可用來顯示相同或相關資訊的不同視圖。</span><span class="sxs-lookup"><span data-stu-id="50a75-141">like split buttons or drop-down lists, tabs can be used to show different views of the same or related information.</span></span> <br/>                                           | ![<span data-ttu-id="50a75-142">[設計]、[分割] 和 [預覽] 索引標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-142">screen shot of design, split, and preview tabs</span></span> ](images/ctrl-tabs-image2.png)<br/> <span data-ttu-id="50a75-143">在此範例中，索引標籤會變更檔內的視圖。</span><span class="sxs-lookup"><span data-stu-id="50a75-143">In this example, tabs change views within a document.</span></span><br/>                                                                                                                                                                                                         |
| <span data-ttu-id="50a75-144">**多份檔**</span><span class="sxs-lookup"><span data-stu-id="50a75-144">**Multiple documents**</span></span><br/> <span data-ttu-id="50a75-145">索引標籤和多個視窗一樣，可以用來在單一視窗中顯示不同的檔。</span><span class="sxs-lookup"><span data-stu-id="50a75-145">like multiple windows, tabs can be used to show different documents in a single window.</span></span> <br/>                                                                   | ![<span data-ttu-id="50a75-146">不同檔的三個索引標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-146">screen shot of three tabs for different documents</span></span> ](images/ctrl-tabs-image3.png)<br/> ![<span data-ttu-id="50a75-147">不同月份的索引標籤圖</span><span class="sxs-lookup"><span data-stu-id="50a75-147">figure of tabs for different months</span></span> ](images/ctrl-tabs-image4.png)<br/> <span data-ttu-id="50a75-148">在這些範例中，索引標籤會在單一應用程式視窗中顯示不同的檔。</span><span class="sxs-lookup"><span data-stu-id="50a75-148">In these examples, tabs show different documents within a single application window.</span></span><br/>                                                                                       |
| <span data-ttu-id="50a75-149">**專屬選項**</span><span class="sxs-lookup"><span data-stu-id="50a75-149">**Exclusive options**</span></span><br/> <span data-ttu-id="50a75-150">索引標籤和選項按鈕一樣，可以用來呈現多個專屬選項。</span><span class="sxs-lookup"><span data-stu-id="50a75-150">like radio buttons, tabs can be used to present multiple exclusive choices.</span></span> <span data-ttu-id="50a75-151">在此模式中，只會套用選取的索引標籤，並忽略所有其他索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-151">in this pattern, only the selected tab applies and all other tabs are ignored.</span></span> <br/> | <span data-ttu-id="50a75-152">![[位置]、[資料] 和 [訊息] 索引標籤的螢幕擷取畫面 ](images/ctrl-tabs-image5.png)</span><span class="sxs-lookup"><span data-stu-id="50a75-152">![screen shot of location, data, and messages tabs ](images/ctrl-tabs-image5.png)</span></span><br/> <span data-ttu-id="50a75-153">在此範例中，會使用索引標籤 (錯誤地) 做為換用的選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="50a75-153">In this example, tabs are used (incorrectly) as a substitute for radio buttons.</span></span><br/> <span data-ttu-id="50a75-154">**不建議使用此模式，** 因為它使用非標準行為。</span><span class="sxs-lookup"><span data-stu-id="50a75-154">**This pattern is not recommended** because it uses a nonstandard behavior.</span></span> <span data-ttu-id="50a75-155">索引標籤的行為就像是一個設定，而不是單純地在視窗內流覽的方法。</span><span class="sxs-lookup"><span data-stu-id="50a75-155">The tabs behave as a setting instead of purely a way to navigate within the window.</span></span> <br/> |



 

<span data-ttu-id="50a75-156">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="50a75-156">**If you do only one thing...**</span></span>

<span data-ttu-id="50a75-157">請確定索引標籤上的資訊是相關的，但不同頁面上的設定都是獨立的。</span><span class="sxs-lookup"><span data-stu-id="50a75-157">Make sure the information on the tabs is related, yet settings on different pages are independent.</span></span> <span data-ttu-id="50a75-158">選取的最後一個索引標籤應該沒有特殊意義。</span><span class="sxs-lookup"><span data-stu-id="50a75-158">The last tab selected should have no special meaning.</span></span>

## <a name="guidelines"></a><span data-ttu-id="50a75-159">指導方針</span><span class="sxs-lookup"><span data-stu-id="50a75-159">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="50a75-160">一般</span><span class="sxs-lookup"><span data-stu-id="50a75-160">General</span></span>

-   <span data-ttu-id="50a75-161">**使用水準索引標籤的情況：**</span><span class="sxs-lookup"><span data-stu-id="50a75-161">**Use horizontal tabs if:**</span></span>
    -   <span data-ttu-id="50a75-162">此視窗有七個或更少的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-162">The window has seven or fewer tabs.</span></span>
    -   <span data-ttu-id="50a75-163">**所有索引標籤都能容納在一個資料列上，即使使用者介面 (UI) 已當地語系化也是一樣。**</span><span class="sxs-lookup"><span data-stu-id="50a75-163">**All the tabs fit on one row, even when the user interface (UI) is localized.**</span></span>
-   <span data-ttu-id="50a75-164">**使用垂直索引標籤的情況：**</span><span class="sxs-lookup"><span data-stu-id="50a75-164">**Use vertical tabs if:**</span></span>
    -   <span data-ttu-id="50a75-165">屬性視窗有八個以上的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-165">The property window has eight or more tabs.</span></span>
    -   <span data-ttu-id="50a75-166">**使用水準索引標籤需要一個以上的資料列。**</span><span class="sxs-lookup"><span data-stu-id="50a75-166">**Using horizontal tabs would require more than one row.**</span></span>

        ![<span data-ttu-id="50a75-167">具有11個選項之屬性視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-167">screen shot of property window with eleven options</span></span> ](images/ctrl-tabs-image6.png)

        <span data-ttu-id="50a75-168">在此範例中，垂直索引標籤能容納八個以上的索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-168">In this example, vertical tabs accommodate eight or more tabs.</span></span>

-   <span data-ttu-id="50a75-169">**請勿使用垂直索引標籤來嵌套索引標籤或合併水準索引標籤。**</span><span class="sxs-lookup"><span data-stu-id="50a75-169">**Don't nest tabs or combine horizontal tabs with vertical tabs.**</span></span> <span data-ttu-id="50a75-170">相反地，請減少索引標籤數目、僅使用垂直索引標籤，或使用另一個控制項（例如下拉式清單）。</span><span class="sxs-lookup"><span data-stu-id="50a75-170">Instead, reduce the number of tabs, use only vertical tabs, or use another control such as a drop-down list.</span></span>
-   <span data-ttu-id="50a75-171">**不要滾動水準索引標籤。**</span><span class="sxs-lookup"><span data-stu-id="50a75-171">**Don't scroll horizontal tabs.**</span></span> <span data-ttu-id="50a75-172">無法立即探索水準滾動。</span><span class="sxs-lookup"><span data-stu-id="50a75-172">Horizontal scrolling isn't readily discoverable.</span></span> <span data-ttu-id="50a75-173">不過，您可以滾動垂直索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-173">You may scroll vertical tabs, however.</span></span>

    <span data-ttu-id="50a75-174">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="50a75-174">**Incorrect:**</span></span>

    ![<span data-ttu-id="50a75-175">截斷的水準索引標籤標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-175">screen shot of truncated horizontal tab label</span></span> ](images/ctrl-tabs-image7.png)

    <span data-ttu-id="50a75-176">在此範例中，會滾動水準索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-176">In this example, the horizontal tabs are scrolled.</span></span>

-   <span data-ttu-id="50a75-177">針對可調整大小的視窗或窗格上的索引標籤，視需要在頁面上（而非視窗或窗格）放置捲軸。</span><span class="sxs-lookup"><span data-stu-id="50a75-177">For tabs on a resizable window or pane, put a scrollbar, when needed, on the page, not the window or pane.</span></span> <span data-ttu-id="50a75-178">索引標籤應該一律是可見的，而不是從視野中取出。</span><span class="sxs-lookup"><span data-stu-id="50a75-178">The tabs should always be visible and not scroll out of view.</span></span>

    ![<span data-ttu-id="50a75-179">具有捲軸之垂直索引標籤頁面的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-179">screen shot of vertical tab page with scroll bar</span></span> ](images/ctrl-tabs-image8.png)

    <span data-ttu-id="50a75-180">在此範例中，索引標籤頁面具有捲軸，而非窗格。</span><span class="sxs-lookup"><span data-stu-id="50a75-180">In this example, the tab page has the scrollbar, not the pane.</span></span>

-   <span data-ttu-id="50a75-181">**確認索引標籤看起來像是索引標籤，而不是另一種類型的控制項。**</span><span class="sxs-lookup"><span data-stu-id="50a75-181">**Make sure the tabs look like tabs and not another type of control.**</span></span>

    <span data-ttu-id="50a75-182">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="50a75-182">**Incorrect:**</span></span>

    ![<span data-ttu-id="50a75-183">具有索引標籤按鈕之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-183">screen shot of window with buttons for tabs</span></span> ](images/ctrl-tabs-image9.png)

    <span data-ttu-id="50a75-184">在此範例中，這些索引標籤看起來像命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="50a75-184">In this example, these tabs look like command buttons.</span></span>

### <a name="interaction"></a><span data-ttu-id="50a75-185">互動</span><span class="sxs-lookup"><span data-stu-id="50a75-185">Interaction</span></span>

-   <span data-ttu-id="50a75-186">**當控制項只套用至頁面時，請將它們放在索引標籤式頁面的框線內。**</span><span class="sxs-lookup"><span data-stu-id="50a75-186">**When controls apply only to a page, place them within the border of the tabbed page.**</span></span>
-   <span data-ttu-id="50a75-187">**當控制項套用至整個視窗時，請將它們放在索引標籤式頁面之外。**</span><span class="sxs-lookup"><span data-stu-id="50a75-187">**When controls apply to the entire window, place them outside the tabbed page.**</span></span>
-   <span data-ttu-id="50a75-188">**請勿指派變更索引標籤的效果。**</span><span class="sxs-lookup"><span data-stu-id="50a75-188">**Don't assign effects to changing tabs.**</span></span> <span data-ttu-id="50a75-189">您必須以任何順序存取索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-189">Tabs must be accessible in any order.</span></span> <span data-ttu-id="50a75-190">變更目前的索引標籤絕不會有副作用、套用設定或產生錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="50a75-190">Changing the current tab should never have side effects, apply settings, or result in an error message.</span></span>
-   <span data-ttu-id="50a75-191">**請勿在選取的最後一個索引標籤上指派特殊意義。**</span><span class="sxs-lookup"><span data-stu-id="50a75-191">**Don't assign a special meaning to the last tab selected.**</span></span> <span data-ttu-id="50a75-192">索引標籤選取用於流覽使用者的最後一個索引標籤選取專案不是設定。</span><span class="sxs-lookup"><span data-stu-id="50a75-192">Tab selection is for navigation the user's last tab selection isn't a setting.</span></span>
-   <span data-ttu-id="50a75-193">**請勿讓頁面上的設定相依于其他頁面上的設定。**</span><span class="sxs-lookup"><span data-stu-id="50a75-193">**Don't make the settings on a page dependent on settings on other pages.**</span></span> <span data-ttu-id="50a75-194">請改為將任何相依的設定放在相同的頁面上。</span><span class="sxs-lookup"><span data-stu-id="50a75-194">Put any dependent settings on the same page instead.</span></span>
-   <span data-ttu-id="50a75-195">**如果使用者可能會從顯示的最後一個索引標籤開始，請讓索引標籤保持不變，並依預設選取它。**</span><span class="sxs-lookup"><span data-stu-id="50a75-195">**If users are likely to start with the last tab displayed, make the tab persist and select it by default.**</span></span> <span data-ttu-id="50a75-196">讓設定以每個視窗、每個使用者為基礎來保存。</span><span class="sxs-lookup"><span data-stu-id="50a75-196">Make the settings persist on a per-window, per-user basis.</span></span> <span data-ttu-id="50a75-197">否則，預設會選取第一個頁面。</span><span class="sxs-lookup"><span data-stu-id="50a75-197">Otherwise, select the first page by default.</span></span>

### <a name="icons"></a><span data-ttu-id="50a75-198">圖示</span><span class="sxs-lookup"><span data-stu-id="50a75-198">Icons</span></span>

-   <span data-ttu-id="50a75-199">**請勿將圖示放在索引標籤上。**</span><span class="sxs-lookup"><span data-stu-id="50a75-199">**Don't put icons on tabs.**</span></span> <span data-ttu-id="50a75-200">圖示通常會加入不必要的視覺效果雜亂、取用螢幕空間，而且通常不會改善使用者理解。</span><span class="sxs-lookup"><span data-stu-id="50a75-200">Icons usually add unnecessary visual clutter, consume screen space, and often don't improve user comprehension.</span></span> <span data-ttu-id="50a75-201">只新增可協助理解的圖示，例如標準符號。</span><span class="sxs-lookup"><span data-stu-id="50a75-201">Only add icons that aid in comprehension, such as standard symbols.</span></span>

    <span data-ttu-id="50a75-202">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="50a75-202">**Incorrect:**</span></span>

    ![<span data-ttu-id="50a75-203">索引標籤上有圖示之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-203">screen shot of window with icons on tabs</span></span> ](images/ctrl-tabs-image10.png)

    <span data-ttu-id="50a75-204">在此範例中，圖示會新增視覺效果，而不會大幅改善使用者理解。</span><span class="sxs-lookup"><span data-stu-id="50a75-204">In this example, the icons add visual clutter and do little to improve user comprehension.</span></span>

    <span data-ttu-id="50a75-205">**例外狀況：** 如果沒有足夠的空間可顯示有意義的標籤，您可以使用明顯可辨識的圖示：</span><span class="sxs-lookup"><span data-stu-id="50a75-205">**Exception:** You can use clearly recognizable icons if there might be insufficient space to display meaningful labels:</span></span>

    <span data-ttu-id="50a75-206">**正確：**</span><span class="sxs-lookup"><span data-stu-id="50a75-206">**Correct:**</span></span>

    ![<span data-ttu-id="50a75-207">具有圖示和縮減標籤之索引標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-207">screen shot of tabs with icons and abridged labels</span></span> ](images/ctrl-tabs-image11.png)

    <span data-ttu-id="50a75-208">在此範例中，視窗很窄，因此圖示會比標籤更妥善地傳達索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-208">In this example, the window is so narrow that icons better communicate the tabs than the labels.</span></span>

-   <span data-ttu-id="50a75-209">**請勿使用標籤圖形的產品標誌。**</span><span class="sxs-lookup"><span data-stu-id="50a75-209">**Don't use product logos for tab graphics.**</span></span> <span data-ttu-id="50a75-210">索引標籤不適用於 [商標](exper-branding.md)。</span><span class="sxs-lookup"><span data-stu-id="50a75-210">Tabs aren't for [branding](exper-branding.md).</span></span>

### <a name="dynamic-window-surface-pattern"></a><span data-ttu-id="50a75-211">動態視窗介面模式</span><span class="sxs-lookup"><span data-stu-id="50a75-211">Dynamic window surface pattern</span></span>

-   <span data-ttu-id="50a75-212">**請勿在索引標籤頁上使用捲軸。**</span><span class="sxs-lookup"><span data-stu-id="50a75-212">**Don't use scroll bars on tab pages.**</span></span> <span data-ttu-id="50a75-213">索引標籤的功能類似于捲軸，以增加視窗的有效區域。</span><span class="sxs-lookup"><span data-stu-id="50a75-213">Tabs function similarly to scroll bars to increase the effective area of a window.</span></span> <span data-ttu-id="50a75-214">其中一個機制應該就已足夠。</span><span class="sxs-lookup"><span data-stu-id="50a75-214">One mechanism should be sufficient.</span></span>
-   <span data-ttu-id="50a75-215">**使用簡潔的索引標籤標籤。**</span><span class="sxs-lookup"><span data-stu-id="50a75-215">**Use concise tab labels.**</span></span> <span data-ttu-id="50a75-216">使用可清楚描述頁面內容的一或兩個字組。</span><span class="sxs-lookup"><span data-stu-id="50a75-216">Use one or two words that clearly describe the content of the page.</span></span> <span data-ttu-id="50a75-217">較長的標籤會耗用螢幕空間，特別是當標籤已當地語系化時。</span><span class="sxs-lookup"><span data-stu-id="50a75-217">Longer labels consume screen space, especially when the labels are localized.</span></span>
-   <span data-ttu-id="50a75-218">**使用有意義的特定索引標籤標籤。**</span><span class="sxs-lookup"><span data-stu-id="50a75-218">**Use specific, meaningful tab labels.**</span></span> <span data-ttu-id="50a75-219">避免可套用至任何索引標籤的一般索引標籤標籤，例如 [一般]、[Advanced] 或 [設定]。</span><span class="sxs-lookup"><span data-stu-id="50a75-219">Avoid generic tab labels that could apply to any tab, such as General, Advanced, or Settings.</span></span>
-   <span data-ttu-id="50a75-220">**如果索引標籤不會套用至目前的內容，而且使用者不會預期它，請將它移除。**</span><span class="sxs-lookup"><span data-stu-id="50a75-220">**If a tab doesn't apply to the current context and users don't expect it to, remove it.**</span></span> <span data-ttu-id="50a75-221">這麼做可簡化 UI，且使用者不會錯過。</span><span class="sxs-lookup"><span data-stu-id="50a75-221">Doing so simplifies the UI and users won't miss it.</span></span>

    <span data-ttu-id="50a75-222">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="50a75-222">**Incorrect:**</span></span>

    ![<span data-ttu-id="50a75-223">選項視窗的螢幕擷取畫面，索引標籤名稱為暗灰色</span><span class="sxs-lookup"><span data-stu-id="50a75-223">screen shot of options window with tab name dimmed</span></span> ](images/ctrl-tabs-image12.png)

    <span data-ttu-id="50a75-224">在此範例中，使用 Microsoft Word 作為電子郵件編輯器時，會不正確地停用 [檔案位置] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-224">In this example, the File Locations tab is incorrectly disabled when Microsoft Word is used as an e-mail editor.</span></span> <span data-ttu-id="50a75-225">由於使用者不會預期會在此內容中查看或變更檔案位置，而不是停用此索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-225">Rather than disabling this tab, it should be removed because users wouldn't expect to view or change file locations in this context.</span></span>

-   <span data-ttu-id="50a75-226">**如果索引標籤不適用於目前的內容，使用者可能會預期：**</span><span class="sxs-lookup"><span data-stu-id="50a75-226">**If a tab doesn't apply to the current context and users might expect it to:**</span></span>

    -   <span data-ttu-id="50a75-227">顯示索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-227">Display the tab.</span></span>
    -   <span data-ttu-id="50a75-228">停用頁面上的控制項。</span><span class="sxs-lookup"><span data-stu-id="50a75-228">Disable the controls on the page.</span></span>
    -   <span data-ttu-id="50a75-229">包含說明控制項停用原因的文字。</span><span class="sxs-lookup"><span data-stu-id="50a75-229">Include text explaining why the controls are disabled.</span></span>

    <span data-ttu-id="50a75-230">請勿停用此索引標籤，因為這樣做並不容易理解，且禁止探索。</span><span class="sxs-lookup"><span data-stu-id="50a75-230">Don't disable the tab, because doing so isn't self-explanatory and prohibits exploration.</span></span> <span data-ttu-id="50a75-231">尋找特定值的使用者會被迫查看所有其他索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-231">Users looking for a specific value would be forced to look on all other tabs.</span></span>

    ![<span data-ttu-id="50a75-232">視窗的螢幕擷取畫面，其中的 [視圖] 索引標籤選項為暗灰色</span><span class="sxs-lookup"><span data-stu-id="50a75-232">screen shot of window with view tab options dimmed</span></span> ](images/ctrl-tabs-image13.png)

    <span data-ttu-id="50a75-233">在此範例中，沒有任何 View 選項適用于讀取配置。</span><span class="sxs-lookup"><span data-stu-id="50a75-233">In this example, none of the View options apply in Reading Layout.</span></span> <span data-ttu-id="50a75-234">不過，使用者可能會預期他們會根據索引標籤標籤來套用，因此會顯示頁面，但選項會停用。</span><span class="sxs-lookup"><span data-stu-id="50a75-234">However, users might expect them to apply based on the tab label, so the page is displayed but the options are disabled.</span></span>

### <a name="multiple-views-and-documents-patterns"></a><span data-ttu-id="50a75-235">多個視圖和檔案模式</span><span class="sxs-lookup"><span data-stu-id="50a75-235">Multiple views and documents patterns</span></span>

-   <span data-ttu-id="50a75-236">**使用索引標籤標籤上的視圖或檔案名稱。**</span><span class="sxs-lookup"><span data-stu-id="50a75-236">**Use the view or document names on tab labels.**</span></span>
-   <span data-ttu-id="50a75-237">**避免索引標籤名稱過長。**</span><span class="sxs-lookup"><span data-stu-id="50a75-237">**Avoid excessively long tab names.**</span></span> <span data-ttu-id="50a75-238">如有必要，請使用省略號來取得最大名稱大小或截斷顯示的索引標籤標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-238">If necessary, either have a maximum name size or truncate the displayed tab label using ellipses.</span></span> <span data-ttu-id="50a75-239">較長的標籤會耗用螢幕空間，特別是當標籤已當地語系化時。</span><span class="sxs-lookup"><span data-stu-id="50a75-239">Longer labels consume screen space, especially when the labels are localized.</span></span>
-   <span data-ttu-id="50a75-240">**如果索引標籤不適用於目前的內容，請移除索引標籤。**</span><span class="sxs-lookup"><span data-stu-id="50a75-240">**If a tab doesn't apply to the current context, remove the tab.**</span></span>

### <a name="exclusive-options-pattern"></a><span data-ttu-id="50a75-241">專屬選項模式</span><span class="sxs-lookup"><span data-stu-id="50a75-241">Exclusive options pattern</span></span>

-   <span data-ttu-id="50a75-242">**請勿使用此模式！**</span><span class="sxs-lookup"><span data-stu-id="50a75-242">**Don't use this pattern!**</span></span> <span data-ttu-id="50a75-243">改為使用選項按鈕或下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="50a75-243">Use radio buttons or a drop-down list instead.</span></span>

    <span data-ttu-id="50a75-244">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="50a75-244">**Incorrect:**</span></span>

    ![<span data-ttu-id="50a75-245">具有兩個 [建立] 索引標籤之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-245">screen shot of window with two 'create' tabs</span></span> ](images/ctrl-tabs-image14.png)

    <span data-ttu-id="50a75-246">在此範例中，索引標籤不正確地用來取代選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="50a75-246">In this example, tabs are incorrectly used as a substitute for radio buttons.</span></span>

    <span data-ttu-id="50a75-247">**正確：**</span><span class="sxs-lookup"><span data-stu-id="50a75-247">**Correct:**</span></span>

    ![<span data-ttu-id="50a75-248">有兩個選項按鈕之視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="50a75-248">screen shot of window with two radio buttons</span></span> ](images/ctrl-tabs-image15.png)

    <span data-ttu-id="50a75-249">在此範例中，會正確地使用選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="50a75-249">In this example, radio buttons are correctly used instead.</span></span>

## <a name="labels"></a><span data-ttu-id="50a75-250">標籤</span><span class="sxs-lookup"><span data-stu-id="50a75-250">Labels</span></span>

-   <span data-ttu-id="50a75-251">根據其模式來標籤索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-251">Label tabs based on their pattern.</span></span> <span data-ttu-id="50a75-252">使用名詞而不是動詞，而不需要結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="50a75-252">Use nouns rather than verbs, without ending punctuation.</span></span> <span data-ttu-id="50a75-253">如需詳細資訊，請參閱上述模式指導方針。</span><span class="sxs-lookup"><span data-stu-id="50a75-253">See the preceding pattern guidelines for more information.</span></span>
-   <span data-ttu-id="50a75-254">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="50a75-254">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="50a75-255">請勿指派存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="50a75-255">Don't assign an access key.</span></span> <span data-ttu-id="50a75-256">索引標籤可透過其快速鍵存取 (Ctrl + Tab、Ctrl + Shift + Tab、Ctrl + PgUp、Ctrl + >pgdn) 。</span><span class="sxs-lookup"><span data-stu-id="50a75-256">Tabs are accessible through their shortcut keys (Ctrl+Tab, Ctrl+Shift+Tab, Ctrl+PgUp, Ctrl+PgDn).</span></span> <span data-ttu-id="50a75-257">有個很好的存取金鑰選擇，因此不會將存取金鑰指派給索引標籤，可讓您更輕鬆地將它們指派給其他控制項。</span><span class="sxs-lookup"><span data-stu-id="50a75-257">There is a shortage of good access key choices, so not assigning access keys to tabs makes it easier to assign them to other controls.</span></span>

## <a name="documentation"></a><span data-ttu-id="50a75-258">文件</span><span class="sxs-lookup"><span data-stu-id="50a75-258">Documentation</span></span>

<span data-ttu-id="50a75-259">參考索引標籤時：</span><span class="sxs-lookup"><span data-stu-id="50a75-259">When referring to tabs:</span></span>

-   <span data-ttu-id="50a75-260">使用確切的標籤文字（包含其大小寫），並包含 [文字] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-260">Use the exact label text, including its capitalization, and include the word tab.</span></span>
-   <span data-ttu-id="50a75-261">若要描述使用者互動，請使用按一下。</span><span class="sxs-lookup"><span data-stu-id="50a75-261">To describe user interaction, use click.</span></span>
-   <span data-ttu-id="50a75-262">可能的話，請使用粗體文字來格式化標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-262">When possible, format the label using bold text.</span></span> <span data-ttu-id="50a75-263">否則，請只在必要時才將標籤放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="50a75-263">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>
-   <span data-ttu-id="50a75-264">由於多個用途可能不明確，特別是針對全球的物件，請單獨使用名詞索引標籤來參考索引標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="50a75-264">Because multiple uses can be ambiguous, especially for a worldwide audience, use the noun tab alone to refer only to a tab control.</span></span> <span data-ttu-id="50a75-265">若為其他用途，請使用描述項來明確說明意義： Tab 鍵、索引標籤停止或尺規上的定位字元標記。</span><span class="sxs-lookup"><span data-stu-id="50a75-265">For other uses, clarify the meaning with a descriptor: the Tab key, a tab stop, or a tab mark on the ruler.</span></span>

<span data-ttu-id="50a75-266">範例：在 [ **工具** ] 功能表上，按一下 [ **選項**]，然後按一下 [ **流覽** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="50a75-266">Example: On the **Tools** menu, click **Options**, and then click the **View** tab.</span></span>

