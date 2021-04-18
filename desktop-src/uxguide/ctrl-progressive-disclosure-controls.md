---
title: 漸進式洩漏控制項
description: 透過漸進式洩漏控制項，使用者可以顯示或隱藏其他資訊，包括資料、選項或命令。
ms.assetid: 0ca00c49-f897-49a6-926a-cc65f3155c6c
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 22c74f60b3184f7fa7f7cdb2b4f2e9d9f64995ea
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321419"
---
# <a name="progressive-disclosure-controls"></a><span data-ttu-id="dee42-103">漸進式洩漏控制項</span><span class="sxs-lookup"><span data-stu-id="dee42-103">Progressive Disclosure Controls</span></span>

> [!NOTE]
> <span data-ttu-id="dee42-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="dee42-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="dee42-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="dee42-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="dee42-106">透過漸進式洩漏控制項，使用者可以顯示或隱藏其他資訊，包括資料、選項或命令。</span><span class="sxs-lookup"><span data-stu-id="dee42-106">With a progressive disclosure control, users can show or hide additional information including data, options, or commands.</span></span> <span data-ttu-id="dee42-107">漸進式洩漏透過將焦點放在必要的情況下提高簡易性，但視需要洩漏其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dee42-107">Progressive disclosure promotes simplicity by focusing on the essential, yet revealing additional detail as needed.</span></span>

![漸進式洩漏控制項的螢幕擷取畫面](images/progressive-disclosure-controls-image1.png)

<span data-ttu-id="dee42-109">漸進式洩漏控制項的範例。</span><span class="sxs-lookup"><span data-stu-id="dee42-109">Examples of progressive disclosure controls.</span></span>

> [!Note]  
> <span data-ttu-id="dee42-110">與 [版面](vis-layout.md)配置、 [功能表](cmd-menus.md)和 [工具列](cmd-toolbars.md) 相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="dee42-110">Guidelines related to [layout](vis-layout.md), [menus](cmd-menus.md), and [toolbars](cmd-toolbars.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="dee42-111">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="dee42-111">Is this the right control?</span></span>

<span data-ttu-id="dee42-112">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="dee42-112">To decide, consider these questions:</span></span>

-   <span data-ttu-id="dee42-113">**使用者是否需要在部分（而非全部）的情況下查看資訊，或是部分但不是所有的時間？**</span><span class="sxs-lookup"><span data-stu-id="dee42-113">**Do users need to see the information in some but not all scenarios, or some but not all of the time?**</span></span> <span data-ttu-id="dee42-114">如果是，使用漸進式洩漏來顯示資訊會簡化基準體驗，但可讓使用者輕鬆地存取訊號。</span><span class="sxs-lookup"><span data-stu-id="dee42-114">If so, displaying the information using progressive disclosure simplifies the baseline experience, yet allows users to access the information easily.</span></span>

    ![顯示 [安全性中心] 狀態顯示的螢幕擷取畫面。](images/progressive-disclosure-controls-image2.png)

    <span data-ttu-id="dee42-116">在此範例中，資訊安全中心會隨時顯示重要的安全性狀態，但會使用漸進式洩漏來顯示隨選的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dee42-116">In this example, Security Center displays the important security status all the time, but uses progressive disclosure to display details on demand.</span></span>

-   <span data-ttu-id="dee42-117">**如果預設會顯示資訊，使用者是否有可能選擇隱藏該資訊？**</span><span class="sxs-lookup"><span data-stu-id="dee42-117">**If the information is displayed by default, are users ever likely to choose to hide it?**</span></span> <span data-ttu-id="dee42-118">是否有使用者需要更多空間的情況？</span><span class="sxs-lookup"><span data-stu-id="dee42-118">Are there scenarios where users will need more space?</span></span> <span data-ttu-id="dee42-119">使用者是否有充分的動機可以自訂使用者介面 (UI) ？</span><span class="sxs-lookup"><span data-stu-id="dee42-119">Are users sufficiently motivated to customize the user interface (UI)?</span></span> <span data-ttu-id="dee42-120">如果沒有，請在不使用漸進式洩漏的情況下顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="dee42-120">If not, display the information without using progressive disclosure.</span></span>

    <span data-ttu-id="dee42-121">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-121">**Incorrect:**</span></span>

    ![<span data-ttu-id="dee42-122">預設顯示的資料選項螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-122">screen shot of data choices displayed by default</span></span> ](images/progressive-disclosure-controls-image3.png)

    <span data-ttu-id="dee42-123">在此範例中，使用者不會想要隱藏資訊。</span><span class="sxs-lookup"><span data-stu-id="dee42-123">In this example, users won't be motivated to hide the information.</span></span>

-   <span data-ttu-id="dee42-124">**額外的資訊是 advanced、重大、複雜，還是與獨立子工作相關的？**</span><span class="sxs-lookup"><span data-stu-id="dee42-124">**Is the additional information advanced, substantial, complex, or related to an independent subtask?**</span></span> <span data-ttu-id="dee42-125">如果是的話，請考慮使用 [命令按鈕](ctrl-command-buttons.md) 或 [連結](ctrl-command-links.md) ，將資訊顯示在另一個視窗中，而不是使用漸進式洩漏控制項。</span><span class="sxs-lookup"><span data-stu-id="dee42-125">If so, consider displaying the information in a separate window using [command buttons](ctrl-command-buttons.md) or [links](ctrl-command-links.md) instead of using a progressive disclosure control.</span></span> <span data-ttu-id="dee42-126">如果適用于 advanced users， (其他資訊為 advanced。</span><span class="sxs-lookup"><span data-stu-id="dee42-126">(Additional information is advanced if it is intended for advanced users.</span></span> <span data-ttu-id="dee42-127">如果它讓其他資訊難以閱讀或配置，則會很複雜。 ) </span><span class="sxs-lookup"><span data-stu-id="dee42-127">It's complex if it makes other information hard to read or lay out.)</span></span>

    ![<span data-ttu-id="dee42-128">您要執行這個檔案的螢幕擷取畫面嗎？</span><span class="sxs-lookup"><span data-stu-id="dee42-128">screen shot of do you want to run this file?</span></span> ](images/progressive-disclosure-controls-image4.png)

    <span data-ttu-id="dee42-129">在此範例中，軟體名稱和發行者的相關資訊主要對 advanced users 有意義，因此會使用不同視窗的連結。</span><span class="sxs-lookup"><span data-stu-id="dee42-129">In this example, information about the software's name and publisher is meaningful primarily to advanced users, so links to separate windows are used.</span></span>

-   <span data-ttu-id="dee42-130">**其他資訊是句子或句子片段的詳細資訊，可描述專案的用途或使用方式？**</span><span class="sxs-lookup"><span data-stu-id="dee42-130">**Is the additional information a sentence or sentence fragment that describes what an item does or how it can be used?**</span></span> <span data-ttu-id="dee42-131">如果是的話，請考慮使用 [工具提示或提示](ctrl-tooltips-and-infotips.md) 。</span><span class="sxs-lookup"><span data-stu-id="dee42-131">If so, consider using a [tooltip](ctrl-tooltips-and-infotips.md) or infotip.</span></span>
-   <span data-ttu-id="dee42-132">**這是與目前工作相關的其他資訊，但與目前顯示的資訊無關嗎？**</span><span class="sxs-lookup"><span data-stu-id="dee42-132">**Is the additional information related to the current task, but independent of the currently displayed information?**</span></span> <span data-ttu-id="dee42-133">如果是的話，請考慮改用 [tab 鍵](ctrl-tabs.md) 。</span><span class="sxs-lookup"><span data-stu-id="dee42-133">If so, consider using [tabs](ctrl-tabs.md) instead.</span></span> <span data-ttu-id="dee42-134">不過，可折迭清單通常偏好用於索引標籤，因為它們較具彈性且可擴充。</span><span class="sxs-lookup"><span data-stu-id="dee42-134">However, collapsible lists are often preferable to tabs because they are more flexible and scalable.</span></span>
-   <span data-ttu-id="dee42-135">**顯示或隱藏其他資訊基本上是資料篩選器？**</span><span class="sxs-lookup"><span data-stu-id="dee42-135">**Is showing or hiding the additional information essentially a data filter?**</span></span> <span data-ttu-id="dee42-136">如果是的話，請考慮使用 [下拉式清單](/windows/desktop/uxguide/ctrl-drop) 或 [核取方塊](ctrl-check-boxes.md) ，將篩選套用至整個清單。</span><span class="sxs-lookup"><span data-stu-id="dee42-136">If so, consider using a [drop-down list](/windows/desktop/uxguide/ctrl-drop) or [check boxes](ctrl-check-boxes.md) instead to apply the filter to the entire list.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="dee42-137">設計概念</span><span class="sxs-lookup"><span data-stu-id="dee42-137">Design concepts</span></span>

<span data-ttu-id="dee42-138">漸進式洩漏的目標是：</span><span class="sxs-lookup"><span data-stu-id="dee42-138">The goals of progressive disclosure are to:</span></span>

-   <span data-ttu-id="dee42-139">將焦點放在必要時 **簡化 UI** ，但視需要洩漏其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dee42-139">**Simplify a UI** by focusing on the essential, yet revealing additional detail as needed.</span></span>
-   <span data-ttu-id="dee42-140">藉由減少雜亂的認知，**簡化 UI 的外觀**。</span><span class="sxs-lookup"><span data-stu-id="dee42-140">**Simplify a UI's appearance** by reducing the perception of clutter.</span></span>

<span data-ttu-id="dee42-141">您可以使用漸進式洩漏控制項來達成兩個目標，讓使用者按一下以查看更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dee42-141">Both goals can be achieved by using progressive disclosure controls, where users click to see more detail.</span></span> <span data-ttu-id="dee42-142">不過，您可以透過下列方式，達到簡化外觀的第二個目標，而不需要使用明確的漸進式洩漏控制項：</span><span class="sxs-lookup"><span data-stu-id="dee42-142">However, you can achieve the second goal of simplifying the appearance without using explicit progressive disclosure controls by:</span></span>

-   <span data-ttu-id="dee42-143">**僅顯示內容中的內容詳細資料。**</span><span class="sxs-lookup"><span data-stu-id="dee42-143">**Showing contextual detail only in context.**</span></span> <span data-ttu-id="dee42-144">例如，您可以在與所選物件或模式相關的情況下，自動顯示內容相關的命令或工具列。</span><span class="sxs-lookup"><span data-stu-id="dee42-144">For example, you can show contextual commands or toolbars automatically when relevant to the selected object or mode.</span></span>
-   <span data-ttu-id="dee42-145">**減少次要 UI 的 affordances 權數。**[Affordances](glossary.md) 是視覺屬性，建議使用物件的方式。</span><span class="sxs-lookup"><span data-stu-id="dee42-145">**Reducing the weight of affordances for secondary UI.**[Affordances](glossary.md) are visual properties that suggest how objects are used.</span></span> <span data-ttu-id="dee42-146">趨勢是讓使用者可以就地進行互動，但讓所有的這類 UI 都繪製成 scream 「按我！」</span><span class="sxs-lookup"><span data-stu-id="dee42-146">The trend is to have UI that users can interact with in place, but to have all such UI drawn to scream "click me!"</span></span> <span data-ttu-id="dee42-147">導致太多視覺效果雜亂。</span><span class="sxs-lookup"><span data-stu-id="dee42-147">leads to too much visual clutter.</span></span> <span data-ttu-id="dee42-148">針對次要 UI，通常最好使用微妙的 affordances，並在滑鼠上方提供完整的效果。</span><span class="sxs-lookup"><span data-stu-id="dee42-148">For secondary UI, it is often better to use subtle affordances and give the full effects on mouse over.</span></span>

    ![<span data-ttu-id="dee42-149">用來分級相片的星星圖示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-149">screen shot of star icons used to rate photos</span></span> ](images/progressive-disclosure-controls-image5.png)

    <span data-ttu-id="dee42-150">在此範例中，[分級] 欄位是互動式的，但在滑鼠停留之前不會出現。</span><span class="sxs-lookup"><span data-stu-id="dee42-150">In this example, the Rating field is interactive, but doesn't appear so until mouse hover.</span></span>

-   <span data-ttu-id="dee42-151">**只有在必要條件完成後才顯示後續步驟。**</span><span class="sxs-lookup"><span data-stu-id="dee42-151">**Showing follow-up steps only after prerequisites are done.**</span></span> <span data-ttu-id="dee42-152">這種方法最適用于熟悉的工作，使用者可以放心採取第一步。</span><span class="sxs-lookup"><span data-stu-id="dee42-152">This approach is best used with familiar tasks where users can confidently take the first steps.</span></span>

    ![<span data-ttu-id="dee42-153">[使用者名稱] 和 [密碼] 文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-153">screen shot of user-name and password text boxes</span></span> ](images/progressive-disclosure-controls-image6.png)

    <span data-ttu-id="dee42-154">在此範例中，[使用者名稱] 和 [密碼] 頁面一開始只會顯示 [使用者名稱] 和 [選用密碼] 方塊。</span><span class="sxs-lookup"><span data-stu-id="dee42-154">In this example, the user name and password page initially shows only the user name and optional password boxes.</span></span> <span data-ttu-id="dee42-155">確認和提示方塊會在使用者輸入密碼之後顯示。</span><span class="sxs-lookup"><span data-stu-id="dee42-155">The confirmation and hint boxes are displayed after the user enters a password.</span></span>

<span data-ttu-id="dee42-156">雖然漸進式洩漏是簡化 Ui 的絕佳方法，但是有下列風險：</span><span class="sxs-lookup"><span data-stu-id="dee42-156">While progressive disclosure is a great way to simplify UIs, it has these risks:</span></span>

-   <span data-ttu-id="dee42-157">**缺乏可探索性。**</span><span class="sxs-lookup"><span data-stu-id="dee42-157">**Lack of discoverability.**</span></span> <span data-ttu-id="dee42-158">使用者可能會假設，如果看不到任何東西，就不會存在。</span><span class="sxs-lookup"><span data-stu-id="dee42-158">Users may assume that if they can't see something, it doesn't exist.</span></span> <span data-ttu-id="dee42-159">如果使用者沒有看到他們要尋找的內容，則可能不會停留或按一下。</span><span class="sxs-lookup"><span data-stu-id="dee42-159">Users may not hover or click if they don't see what they are looking for.</span></span> <span data-ttu-id="dee42-160">有時候使用者可能不會按到更多選項。</span><span class="sxs-lookup"><span data-stu-id="dee42-160">There is always a chance that users might not click things like More options.</span></span>
-   <span data-ttu-id="dee42-161">**缺乏穩定性。**</span><span class="sxs-lookup"><span data-stu-id="dee42-161">**Lack of stability.**</span></span> <span data-ttu-id="dee42-162">漸進式洩漏應預期或至少是自然的。</span><span class="sxs-lookup"><span data-stu-id="dee42-162">Progressive disclosure should be expected or at least feel natural.</span></span> <span data-ttu-id="dee42-163">如果控制項意外出現並消失，則產生的 UI 可能會覺得不穩定。</span><span class="sxs-lookup"><span data-stu-id="dee42-163">If controls unexpectedly appear and disappear, the resulting UI can feel unstable.</span></span>

### <a name="progressive-disclosure-controls"></a><span data-ttu-id="dee42-164">漸進式洩漏控制項</span><span class="sxs-lookup"><span data-stu-id="dee42-164">Progressive disclosure controls</span></span>

<span data-ttu-id="dee42-165">漸進式洩漏控制項通常會在沒有描述其行為的直接標籤的情況下顯示，因此使用者必須能夠根據控制項的視覺外觀，來執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="dee42-165">Progressive disclosure controls are usually displayed without direct labels that describe their behavior, so users must be able to do the following based on the control's visual appearance alone:</span></span>

-   <span data-ttu-id="dee42-166">辨識控制項可提供漸進式的洩漏。</span><span class="sxs-lookup"><span data-stu-id="dee42-166">Recognize that the control provides progressive disclosure.</span></span>
-   <span data-ttu-id="dee42-167">判斷目前的狀態為展開或折迭。</span><span class="sxs-lookup"><span data-stu-id="dee42-167">Determine if the current state is expanded or collapsed.</span></span>
-   <span data-ttu-id="dee42-168">判斷是否需要額外的資訊、選項或命令來執行工作。</span><span class="sxs-lookup"><span data-stu-id="dee42-168">Determine if additional information, options, or commands are needed to perform the task.</span></span>
-   <span data-ttu-id="dee42-169">判斷如何還原原始狀態（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="dee42-169">Determine how to restore the original state, if desired.</span></span>

<span data-ttu-id="dee42-170">雖然使用者可以根據試用和錯誤來判斷上述情況，但您應該嘗試進行這類實驗。</span><span class="sxs-lookup"><span data-stu-id="dee42-170">While users can determine the above by trial and error, you should try to make such experimentation unnecessary.</span></span>

<span data-ttu-id="dee42-171">漸進式洩漏控制項有相當弱的 [affordances](glossary.md)，這表示其視覺效果屬性會建議其使用方式，雖然弱。</span><span class="sxs-lookup"><span data-stu-id="dee42-171">Progressive disclosure controls have a fairly weak [affordances](glossary.md), which means their visual properties suggest how they are used, albeit weakly.</span></span> <span data-ttu-id="dee42-172">下表比較常見漸進式洩漏控制項的外觀：</span><span class="sxs-lookup"><span data-stu-id="dee42-172">The following table compares the appearance of the common progressive disclosure controls:</span></span>



|                                                                                                                                                          |                                                                                                                                                                                                             |                                                                                                                                |                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span data-ttu-id="dee42-173">**控制**</span><span class="sxs-lookup"><span data-stu-id="dee42-173">**Control**</span></span><br/>                                                                                                                                   | <span data-ttu-id="dee42-174">**目的**</span><span class="sxs-lookup"><span data-stu-id="dee42-174">**Purpose**</span></span><br/>                                                                                                                                                                                      | <span data-ttu-id="dee42-175">**外觀**</span><span class="sxs-lookup"><span data-stu-id="dee42-175">**Appearance**</span></span><br/>                                                                                                      | <span data-ttu-id="dee42-176">**符號表示**</span><span class="sxs-lookup"><span data-stu-id="dee42-176">**Glyph indicates**</span></span><br/> |
| <span data-ttu-id="dee42-177">**角括弧**</span><span class="sxs-lookup"><span data-stu-id="dee42-177">**Chevrons**</span></span><br/> <span data-ttu-id="dee42-178">![left/right 和向上/向下燕的螢幕擷取畫面 ](images/progressive-disclosure-controls-image7.png)</span><span class="sxs-lookup"><span data-stu-id="dee42-178">![screen shot of left/right and up/down chevrons ](images/progressive-disclosure-controls-image7.png)</span></span><br/>                 | <span data-ttu-id="dee42-179">**全部顯示：** 顯示或隱藏完整或部分隱藏內容中的其餘專案。</span><span class="sxs-lookup"><span data-stu-id="dee42-179">**Show all:** Show or hide the remaining items in completely or partially hidden content.</span></span> <span data-ttu-id="dee42-180">專案會 (使用單一的燕形形) 或在快顯功能表 (使用雙箭號) 來顯示。</span><span class="sxs-lookup"><span data-stu-id="dee42-180">Items are either shown in place (using a single chevron) or in a pop-up menu (using a double chevron).</span></span><br/> | <span data-ttu-id="dee42-181">動作將會出現在方向的燕點。</span><span class="sxs-lookup"><span data-stu-id="dee42-181">Chevrons point in the direction where the action will occur.</span></span><br/>                                                        | <span data-ttu-id="dee42-182">未來的狀態</span><span class="sxs-lookup"><span data-stu-id="dee42-182">Future state</span></span><br/>        |
| <span data-ttu-id="dee42-183">**箭頭**</span><span class="sxs-lookup"><span data-stu-id="dee42-183">**Arrows**</span></span><br/> <span data-ttu-id="dee42-184">![left/right 和向上/向下箭號的螢幕擷取畫面 ](images/progressive-disclosure-controls-image8.png)</span><span class="sxs-lookup"><span data-stu-id="dee42-184">![screen shot of left/right and up/down arrows ](images/progressive-disclosure-controls-image8.png)</span></span><br/>                     | <span data-ttu-id="dee42-185">**顯示選項：** 顯示快顯命令功能表。</span><span class="sxs-lookup"><span data-stu-id="dee42-185">**Show options:** Show a pop-up command menu.</span></span><br/>                                                                                                                                                    | <span data-ttu-id="dee42-186">箭號指向動作將會發生的方向。</span><span class="sxs-lookup"><span data-stu-id="dee42-186">Arrows point in the direction where the action will occur.</span></span><br/>                                                          | <span data-ttu-id="dee42-187">未來的狀態</span><span class="sxs-lookup"><span data-stu-id="dee42-187">Future state</span></span><br/>        |
| <span data-ttu-id="dee42-188">**加號和減號控制項**</span><span class="sxs-lookup"><span data-stu-id="dee42-188">**Plus and minus controls**</span></span><br/> <span data-ttu-id="dee42-189">![兩個小加號和減號按鈕的螢幕擷取畫面 ](images/progressive-disclosure-controls-image9.png)</span><span class="sxs-lookup"><span data-stu-id="dee42-189">![screen shot of two small plus and minus buttons ](images/progressive-disclosure-controls-image9.png)</span></span><br/> | <span data-ttu-id="dee42-190">**展開 [容器]：** 流覽階層時，就地展開或折迭容器內容。</span><span class="sxs-lookup"><span data-stu-id="dee42-190">**Expand containers:** Expand or collapse container content in place when navigating through a hierarchy.</span></span><br/>                                                                                        | <span data-ttu-id="dee42-191">加上和減號符號不會指向，但動作一律會在其右側發生。</span><span class="sxs-lookup"><span data-stu-id="dee42-191">Plus and minus symbols don't point, but the action always occurs to their right.</span></span><br/>                                    | <span data-ttu-id="dee42-192">未來的狀態</span><span class="sxs-lookup"><span data-stu-id="dee42-192">Future state</span></span><br/>        |
| <span data-ttu-id="dee42-193">**旋轉三角形**</span><span class="sxs-lookup"><span data-stu-id="dee42-193">**Rotating triangles**</span></span><br/> <span data-ttu-id="dee42-194">![兩個小型三角形的螢幕擷取畫面 ](images/progressive-disclosure-controls-image10.png)</span><span class="sxs-lookup"><span data-stu-id="dee42-194">![screen shot of two small triangles ](images/progressive-disclosure-controls-image10.png)</span></span><br/>                  | <span data-ttu-id="dee42-195">**顯示詳細資料：** 顯示或隱藏個別專案的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="dee42-195">**Show details:** Show or hide additional information in place for an individual item.</span></span> <span data-ttu-id="dee42-196">它們也可用來展開容器。</span><span class="sxs-lookup"><span data-stu-id="dee42-196">They are also used to expand containers.</span></span><br/>                                                                  | <span data-ttu-id="dee42-197">旋轉三角形有點類似旋轉杆，因此會指向動作發生的方向。</span><span class="sxs-lookup"><span data-stu-id="dee42-197">Rotating triangles somewhat resemble rotating levers, so they point in the direction where the action has occurred.</span></span><br/> | <span data-ttu-id="dee42-198">目前狀態</span><span class="sxs-lookup"><span data-stu-id="dee42-198">Present state</span></span><br/>       |



 

<span data-ttu-id="dee42-199">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="dee42-199">**If you do only one thing...**</span></span>

<span data-ttu-id="dee42-200">使用者應該能夠單獨檢查，以正確地預測漸進式洩漏控制項的行為。</span><span class="sxs-lookup"><span data-stu-id="dee42-200">Users should be able to predict a progressive disclosure control's behavior correctly by inspection alone.</span></span> <span data-ttu-id="dee42-201">若要達成此目的，請選取適當的使用模式，並以一致的方式套用其外觀、位置和行為。</span><span class="sxs-lookup"><span data-stu-id="dee42-201">To achieve this, select the appropriate usage patterns and apply their appearance, location, and behavior consistently.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="dee42-202">使用模式</span><span class="sxs-lookup"><span data-stu-id="dee42-202">Usage patterns</span></span>

<span data-ttu-id="dee42-203">漸進式洩漏控制項有數種使用模式。</span><span class="sxs-lookup"><span data-stu-id="dee42-203">Progressive disclosure controls have several usage patterns.</span></span> <span data-ttu-id="dee42-204">其中一些內建于通用控制項中。</span><span class="sxs-lookup"><span data-stu-id="dee42-204">Some of them are built into common controls.</span></span>

### <a name="chevrons"></a><span data-ttu-id="dee42-205">角括弧</span><span class="sxs-lookup"><span data-stu-id="dee42-205">Chevrons</span></span>

<span data-ttu-id="dee42-206">燕尾顯示或隱藏完整或部分隱藏內容中的其餘專案。</span><span class="sxs-lookup"><span data-stu-id="dee42-206">Chevrons show or hide the remaining items in completely or partially hidden content.</span></span> <span data-ttu-id="dee42-207">通常會顯示專案，但是也可以在快顯功能表中顯示這些專案。</span><span class="sxs-lookup"><span data-stu-id="dee42-207">Usually the items are shown in place, but they can also be shown in a pop-up menu.</span></span> <span data-ttu-id="dee42-208">當您準備好時，專案會一直展開，直到使用者折迭為止。</span><span class="sxs-lookup"><span data-stu-id="dee42-208">When in place, the item stays expanded until the user collapses it.</span></span>

<span data-ttu-id="dee42-209">以下列方式使用燕：</span><span class="sxs-lookup"><span data-stu-id="dee42-209">Chevrons are used in the following ways:</span></span>



|                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee42-210">**就地 UI**</span><span class="sxs-lookup"><span data-stu-id="dee42-210">**In-place UI**</span></span><br/> <span data-ttu-id="dee42-211">相關聯的物件會收到輸入焦點，而且會使用空格鍵來啟用單一燕號。</span><span class="sxs-lookup"><span data-stu-id="dee42-211">the associated object receives input focus and the single chevron is activated with the space bar.</span></span><br/>                       | ![<span data-ttu-id="dee42-212">[安全性中心] 狀態顯示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-212">screen shot of security center status display</span></span> ](images/progressive-disclosure-controls-image11.png)<br/> <span data-ttu-id="dee42-213">在這些範例中，就地單一燕點位於其相關聯控制項的右邊。</span><span class="sxs-lookup"><span data-stu-id="dee42-213">In these examples, the in-place single chevrons are positioned to the right of their associated control.</span></span><br/>                                                                            |
| <span data-ttu-id="dee42-214">**具有外部標籤的命令按鈕**</span><span class="sxs-lookup"><span data-stu-id="dee42-214">**Command buttons with external labels**</span></span><br/> <span data-ttu-id="dee42-215">[命令] 按鈕會接收輸入焦點，而且會使用空格鍵來啟用單一的燕號線。</span><span class="sxs-lookup"><span data-stu-id="dee42-215">the command button receives input focus and the single chevron is activated with the space bar.</span></span><br/> | ![<span data-ttu-id="dee42-216">具有 [更多選項] 標籤的燕號螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-216">screen shot of chevron with 'more options' label</span></span> ](images/progressive-disclosure-controls-image12.png)<br/> <span data-ttu-id="dee42-217">在此範例中，會將單一的燕形按鈕標示，並放在標籤的左邊。</span><span class="sxs-lookup"><span data-stu-id="dee42-217">In this example, the single chevron button is labeled and positioned to the left of the label.</span></span> <span data-ttu-id="dee42-218">使用這個模式時，在沒有標籤的情況下，按鈕會很難瞭解。</span><span class="sxs-lookup"><span data-stu-id="dee42-218">With this pattern, the button would be difficult to understand without its label.</span></span><br/> |
| <span data-ttu-id="dee42-219">**具有內部標籤的命令按鈕**</span><span class="sxs-lookup"><span data-stu-id="dee42-219">**Command buttons with internal labels**</span></span><br/> <span data-ttu-id="dee42-220">命令按鈕會接收輸入焦點，並以空格鍵啟用。</span><span class="sxs-lookup"><span data-stu-id="dee42-220">the command button receives input focus and is activated with the space bar.</span></span><br/>                    | ![<span data-ttu-id="dee42-221">[更多] 和 [less] 命令按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-221">screen shot of 'more' and 'less' command buttons</span></span> ](images/progressive-disclosure-controls-image13.png)<br/> <span data-ttu-id="dee42-222">在這些範例中，一般的命令按鈕會有雙箭號，以建議其意義。</span><span class="sxs-lookup"><span data-stu-id="dee42-222">In these examples, regular command buttons have the double chevron positioned to suggest their meaning.</span></span><br/>                                                                          |



 

### <a name="arrows"></a><span data-ttu-id="dee42-223">箭頭</span><span class="sxs-lookup"><span data-stu-id="dee42-223">Arrows</span></span>

<span data-ttu-id="dee42-224">箭號會顯示快顯命令功能表。</span><span class="sxs-lookup"><span data-stu-id="dee42-224">Arrows show a pop-up command menu.</span></span> <span data-ttu-id="dee42-225">專案會一直展開，直到使用者選擇或按一下任何位置為止。</span><span class="sxs-lookup"><span data-stu-id="dee42-225">The item stays expanded until the user makes a selection or clicks anywhere.</span></span>

<span data-ttu-id="dee42-226">如果箭號按鈕是獨立的控制項，則會收到輸入焦點，並以空格鍵啟用。</span><span class="sxs-lookup"><span data-stu-id="dee42-226">If the arrow button is an independent control, it receives input focus and is activated with the space bar.</span></span> <span data-ttu-id="dee42-227">如果箭號按鈕具有父控制項，父控制項就會收到輸入焦點，而且會使用 Alt + 向下鍵和 Alt + 向上鍵和 Alt + 向上鍵來啟用箭號，如同下拉式清單控制項一樣。</span><span class="sxs-lookup"><span data-stu-id="dee42-227">If the arrow button has a parent control, the parent receives input focus and the arrow is activated with Alt+down arrow and Alt+up arrow keys, as with the drop-down list control.</span></span>

<span data-ttu-id="dee42-228">箭號會以下列方式使用：</span><span class="sxs-lookup"><span data-stu-id="dee42-228">Arrows are used in the following ways:</span></span>



|                                                                                       |                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee42-229">**分隔按鈕**</span><span class="sxs-lookup"><span data-stu-id="dee42-229">**Separate buttons**</span></span><br/> <span data-ttu-id="dee42-230">箭號位於個別的按鈕控制項中。</span><span class="sxs-lookup"><span data-stu-id="dee42-230">the arrow is in a separate button control.</span></span><br/> | ![<span data-ttu-id="dee42-231">控制項右邊箭號的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-231">screen shot of arrows to the right of controls</span></span> ](images/progressive-disclosure-controls-image14.png)<br/> <span data-ttu-id="dee42-232">在這些範例中，位於右邊的不同箭號按鈕表示命令功能表。</span><span class="sxs-lookup"><span data-stu-id="dee42-232">In these examples, separate arrow buttons positioned to the right indicate a command menu.</span></span><br/>               |
| <span data-ttu-id="dee42-233">**命令按鈕**</span><span class="sxs-lookup"><span data-stu-id="dee42-233">**Command buttons**</span></span><br/> <span data-ttu-id="dee42-234">箭號是命令按鈕的一部分。</span><span class="sxs-lookup"><span data-stu-id="dee42-234">the arrow is part of a command button.</span></span><br/>      | ![<span data-ttu-id="dee42-235">命令按鈕上標籤和箭號的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-235">screen shot of label and arrow on command button</span></span> ](images/progressive-disclosure-controls-image15.png)<br/> <span data-ttu-id="dee42-236">在這些範例中，功能表按鈕和分割按鈕的箭號位於文字的右邊。</span><span class="sxs-lookup"><span data-stu-id="dee42-236">In these examples, menu buttons and split buttons have the arrows positioned to the right of the text.</span></span><br/> |



 

### <a name="plus-and-minus-controls"></a><span data-ttu-id="dee42-237">加號和減號控制項</span><span class="sxs-lookup"><span data-stu-id="dee42-237">Plus and minus controls</span></span>

<span data-ttu-id="dee42-238">加號和減號控制項會展開或折迭，以在流覽階層時，就地顯示容器內容。</span><span class="sxs-lookup"><span data-stu-id="dee42-238">Plus and minus controls expand or collapse to show container content in place when navigating through a hierarchy.</span></span> <span data-ttu-id="dee42-239">專案會一直擴充，直到使用者折迭為止。</span><span class="sxs-lookup"><span data-stu-id="dee42-239">The item stays expanded until the user collapses it.</span></span> <span data-ttu-id="dee42-240">雖然它們看起來像按鈕，但它們的行為是就地的。</span><span class="sxs-lookup"><span data-stu-id="dee42-240">Although these look like buttons, their behavior is in-place.</span></span>

<span data-ttu-id="dee42-241">相關聯的物件會收到輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="dee42-241">The associated object receives input focus.</span></span> <span data-ttu-id="dee42-242">加號會以向右箭號來啟動，並以向左箭號鍵來啟用。</span><span class="sxs-lookup"><span data-stu-id="dee42-242">The plus is activated with the right arrow key, and the minus with the left arrow key.</span></span>

<span data-ttu-id="dee42-243">加號和減號控制項的使用方式如下：</span><span class="sxs-lookup"><span data-stu-id="dee42-243">Plus and minus controls are used in the following ways:</span></span>



|                                                                                                |                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee42-244">**可折迭的樹狀結構**</span><span class="sxs-lookup"><span data-stu-id="dee42-244">**Collapsible trees**</span></span><br/> <span data-ttu-id="dee42-245">顯示容器內容的多層級階層。</span><span class="sxs-lookup"><span data-stu-id="dee42-245">a multi-level hierarchy to show container content.</span></span><br/> | ![顯示已選取 [行為] Windows 檔案總管資料夾樹狀結構的螢幕擷取畫面。](images/progressive-disclosure-controls-image16.png)<br/> <span data-ttu-id="dee42-247">在此範例中，加號和減號控制項位於相關容器的左邊。</span><span class="sxs-lookup"><span data-stu-id="dee42-247">In this example, the plus and minus controls are positioned to the left of the associated container.</span></span><br/>       |
| <span data-ttu-id="dee42-248">**可折迭清單**</span><span class="sxs-lookup"><span data-stu-id="dee42-248">**Collapsible lists**</span></span><br/> <span data-ttu-id="dee42-249">顯示容器內容的兩層階層。</span><span class="sxs-lookup"><span data-stu-id="dee42-249">a two-level hierarchy to show container content.</span></span><br/>   | ![<span data-ttu-id="dee42-250">展開清單以顯示兩個層級的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-250">screen shot of list expanded to show two levels</span></span> ](images/progressive-disclosure-controls-image17.png)<br/> <span data-ttu-id="dee42-251">在此範例中，加號和減號控制項位於相關清單標題的左邊。</span><span class="sxs-lookup"><span data-stu-id="dee42-251">In this example, the plus and minus controls are positioned to the left of the associated list header.</span></span><br/> |



 

### <a name="rotating-triangles"></a><span data-ttu-id="dee42-252">旋轉三角形</span><span class="sxs-lookup"><span data-stu-id="dee42-252">Rotating triangles</span></span>

<span data-ttu-id="dee42-253">旋轉三角形會顯示或隱藏個別專案的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="dee42-253">Rotating triangles show or hide additional information in place for an individual item.</span></span> <span data-ttu-id="dee42-254">它們也可用來展開容器。</span><span class="sxs-lookup"><span data-stu-id="dee42-254">They are also used to expand containers.</span></span> <span data-ttu-id="dee42-255">專案會一直擴充，直到使用者折迭為止。</span><span class="sxs-lookup"><span data-stu-id="dee42-255">The item stays expanded until the user collapses it.</span></span>

<span data-ttu-id="dee42-256">相關聯的物件會收到輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="dee42-256">The associated object receives input focus.</span></span> <span data-ttu-id="dee42-257">折迭的 (右) 三角形會以向右箭號來啟動，並以向左方向鍵展開 (向下定位) 三角形。</span><span class="sxs-lookup"><span data-stu-id="dee42-257">The collapsed (right-pointing) triangle is activated with the right arrow key, and the expanded (downward-pointing) triangle with the left arrow key.</span></span>

<span data-ttu-id="dee42-258">旋轉三角形的使用方式如下：</span><span class="sxs-lookup"><span data-stu-id="dee42-258">Rotating triangles are used in the following ways:</span></span>



|                                                                                                            |                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee42-259">**可折迭的樹狀結構**</span><span class="sxs-lookup"><span data-stu-id="dee42-259">**Collapsible trees**</span></span><br/> <span data-ttu-id="dee42-260">顯示容器內容的多層級階層。</span><span class="sxs-lookup"><span data-stu-id="dee42-260">a multi-level hierarchy to show container content.</span></span><br/>             | ![<span data-ttu-id="dee42-261">windows explorer 資料夾樹狀結構的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-261">screen shot of windows explorer folder tree</span></span> ](images/progressive-disclosure-controls-image18.png)<br/> <span data-ttu-id="dee42-262">在此範例中，旋轉三角形位於相關容器的左邊。</span><span class="sxs-lookup"><span data-stu-id="dee42-262">In this example, the rotating triangles are positioned to the left of the associated container.</span></span><br/>       |
| <span data-ttu-id="dee42-263">**可折迭清單**</span><span class="sxs-lookup"><span data-stu-id="dee42-263">**Collapsible lists**</span></span><br/> <span data-ttu-id="dee42-264">用來顯示其他資訊的二級階層。</span><span class="sxs-lookup"><span data-stu-id="dee42-264">a two-level hierarchy to show additional information in place.</span></span><br/> | ![<span data-ttu-id="dee42-265">顯示其他資料的清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-265">screen shot of list displaying additional data</span></span> ](images/progressive-disclosure-controls-image19.png)<br/> <span data-ttu-id="dee42-266">在此範例中，旋轉三角形位於其相關清單專案的左邊。</span><span class="sxs-lookup"><span data-stu-id="dee42-266">In this example, the rotating triangles are positioned to the left of their associated list items.</span></span><br/> |



 

### <a name="preview-arrows"></a><span data-ttu-id="dee42-267">預覽箭號</span><span class="sxs-lookup"><span data-stu-id="dee42-267">Preview arrows</span></span>

<span data-ttu-id="dee42-268">如同燕尾，會顯示或隱藏其他資訊。</span><span class="sxs-lookup"><span data-stu-id="dee42-268">Like chevrons, additional information is shown or hidden in place.</span></span> <span data-ttu-id="dee42-269">專案會一直擴充，直到使用者折迭為止。</span><span class="sxs-lookup"><span data-stu-id="dee42-269">The item stays expanded until the user collapses it.</span></span> <span data-ttu-id="dee42-270">和燕號不同的是，圖像以圖形表示動作，通常是以箭號指出將會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="dee42-270">Unlike chevrons, the glyphs have a graphical representation of the action, typically with an arrow indicating what will happen.</span></span>

![<span data-ttu-id="dee42-271">指向對角線的箭號字元螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-271">screen shot of arrow glyphs pointing diagonally</span></span> ](images/progressive-disclosure-controls-image20.png)

<span data-ttu-id="dee42-272">在這些來自 Microsoft Windows Media Player 的範例中，圖像會有箭號來建議將會發生的動作。</span><span class="sxs-lookup"><span data-stu-id="dee42-272">In these examples from Microsoft Windows Media Player, the glyphs have arrows that suggest the action that will happen.</span></span>

<span data-ttu-id="dee42-273">預覽箭號最適合用於標準箭號未充分傳達控制項行為的情況，例如，當洩漏很複雜或有多種類型的洩漏時。</span><span class="sxs-lookup"><span data-stu-id="dee42-273">Preview arrows are best reserved for situations where a standard chevron doesn't adequately communicate the control's behavior, such as when the disclosure is complex or there is more than one type of disclosure.</span></span>

## <a name="guidelines"></a><span data-ttu-id="dee42-274">指導方針</span><span class="sxs-lookup"><span data-stu-id="dee42-274">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="dee42-275">一般</span><span class="sxs-lookup"><span data-stu-id="dee42-275">General</span></span>

-   <span data-ttu-id="dee42-276">**根據其使用方式選取漸進式洩漏模式。**</span><span class="sxs-lookup"><span data-stu-id="dee42-276">**Select the progressive disclosure pattern based on its usage.**</span></span> <span data-ttu-id="dee42-277">如需每個使用模式的說明，請參閱上一個表格。</span><span class="sxs-lookup"><span data-stu-id="dee42-277">For a description of each usage pattern, see the previous table.</span></span>
-   <span data-ttu-id="dee42-278">**請勿使用漸進式洩漏控制項的連結。**</span><span class="sxs-lookup"><span data-stu-id="dee42-278">**Don't use links for progressive disclosure controls.**</span></span> <span data-ttu-id="dee42-279">使用 [使用模式] 區段中顯示的漸進式控制項。</span><span class="sxs-lookup"><span data-stu-id="dee42-279">Use only the progressive disclosure controls presented in the Usage patterns section.</span></span> <span data-ttu-id="dee42-280">不過，請使用連結來流覽至 [說明主題](winenv-help.md)。</span><span class="sxs-lookup"><span data-stu-id="dee42-280">However, do use links to navigate to [Help topics](winenv-help.md).</span></span>

    <span data-ttu-id="dee42-281">**正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-281">**Correct:**</span></span>

    ![<span data-ttu-id="dee42-282">具有「顯示混音器」標籤的燕號螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-282">screen shot of chevron with 'show mixer' label</span></span> ](images/progressive-disclosure-controls-image21.png)

    <span data-ttu-id="dee42-283">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-283">**Incorrect:**</span></span>

    ![<span data-ttu-id="dee42-284">[顯示混音器] 連結文字的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-284">screen shot of 'show mixer' link text</span></span> ](images/progressive-disclosure-controls-image22.png)

    <span data-ttu-id="dee42-285">在不正確的範例中，會使用連結來就地顯示更多選項。</span><span class="sxs-lookup"><span data-stu-id="dee42-285">In the incorrect example, a link is used to show more options in place.</span></span> <span data-ttu-id="dee42-286">如果流覽至另一個頁面或對話方塊，或顯示說明主題，此使用方式會是正確的。</span><span class="sxs-lookup"><span data-stu-id="dee42-286">This usage would be correct if the link navigated to another page or dialog box, or displayed a Help topic.</span></span>

### <a name="interaction"></a><span data-ttu-id="dee42-287">互動</span><span class="sxs-lookup"><span data-stu-id="dee42-287">Interaction</span></span>

-   <span data-ttu-id="dee42-288">**針對未直接標記的燕號和箭號，請使用工具提示來描述其功能。**</span><span class="sxs-lookup"><span data-stu-id="dee42-288">**For chevrons and arrows that aren't directly labeled, use tooltips to describe what they do.**</span></span>

    ![<span data-ttu-id="dee42-289">[展開查詢產生器] 工具提示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-289">screen shot of 'expand the query builder' tooltip</span></span> ](images/progressive-disclosure-controls-image23.png)

    <span data-ttu-id="dee42-290">在此範例中，工具提示指出未標記的燕號控制項效果。</span><span class="sxs-lookup"><span data-stu-id="dee42-290">In this example, the tooltip indicates the effect of an unlabeled chevron control.</span></span>

-   <span data-ttu-id="dee42-291">**如果使用者展開或折迭專案，請讓狀態保持不變，以便在下一次顯示視窗時生效**，除非使用者可能偏好以預設狀態啟動。</span><span class="sxs-lookup"><span data-stu-id="dee42-291">**If a user expands or collapses an item, make the state persist so it takes effect the next time the window is displayed**, unless users are likely to prefer starting in the default state.</span></span> <span data-ttu-id="dee42-292">將狀態保持在每個視窗、每位使用者的基礎上。</span><span class="sxs-lookup"><span data-stu-id="dee42-292">Make the state persist on a per-window, per-user basis.</span></span>
-   <span data-ttu-id="dee42-293">**請確定所有展開的內容都可以折迭，反之亦然，相反的作業很明顯。**</span><span class="sxs-lookup"><span data-stu-id="dee42-293">**Make sure that all expanded content can be collapsed and vice versa, and that the inverse operation is obvious.**</span></span> <span data-ttu-id="dee42-294">這樣做會促進探索並減少挫折。</span><span class="sxs-lookup"><span data-stu-id="dee42-294">Doing so encourages exploration and reduces frustration.</span></span> <span data-ttu-id="dee42-295">使反向操作變得顯而易見的最佳方式，是將控制項保持在相同的固定位置。</span><span class="sxs-lookup"><span data-stu-id="dee42-295">The best way to make the inverse operation obvious is to keep the control in the same fixed location.</span></span> <span data-ttu-id="dee42-296">如果您需要移動控制項，請將它保留在視覺上不同區域內的相同相對位置。</span><span class="sxs-lookup"><span data-stu-id="dee42-296">If you need to move the control, keep it in the same relative location within a visually distinct area.</span></span>

    <span data-ttu-id="dee42-297">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-297">**Incorrect:**</span></span>

    ![<span data-ttu-id="dee42-298">[取代] 按鈕的螢幕擷取畫面（具有燕號）</span><span class="sxs-lookup"><span data-stu-id="dee42-298">screen shot of 'replace' button with chevron</span></span> ](images/progressive-disclosure-controls-image24.png)

    ![<span data-ttu-id="dee42-299">[取代] 按鈕的螢幕擷取畫面（沒有箭號）</span><span class="sxs-lookup"><span data-stu-id="dee42-299">screen shot of 'replace' button without chevron</span></span> ](images/progressive-disclosure-controls-image25.png)

    <span data-ttu-id="dee42-300">在此範例中，按一下 [取代] 按鈕時，會顯示 [ **取代成** ] 文字方塊。</span><span class="sxs-lookup"><span data-stu-id="dee42-300">In this example, clicking the Replace button with the chevron reveals the **Replace with** text box.</span></span> <span data-ttu-id="dee42-301">完成這項操作之後，Replace 擴充器會變成 Replace 命令，所以沒有辦法還原原始狀態。</span><span class="sxs-lookup"><span data-stu-id="dee42-301">Once this is done, the Replace expander becomes the Replace command, so there is no way to restore the original state.</span></span>

-   <span data-ttu-id="dee42-302">請 **僅使用適用于漸進式洩漏模式的存取金鑰**，如使用模式一節中所列。</span><span class="sxs-lookup"><span data-stu-id="dee42-302">**Use only the access keys appropriate for the progressive disclosure pattern**, as listed in the Usage patterns section.</span></span> <span data-ttu-id="dee42-303">請勿使用 Enter 來啟用漸進式洩漏。</span><span class="sxs-lookup"><span data-stu-id="dee42-303">Don't use Enter to activate progressive disclosure.</span></span>

### <a name="presentation"></a><span data-ttu-id="dee42-304">簡報</span><span class="sxs-lookup"><span data-stu-id="dee42-304">Presentation</span></span>

-   <span data-ttu-id="dee42-305">**請勿針對漸進式洩漏以外的目的使用三角形形狀的箭頭。**</span><span class="sxs-lookup"><span data-stu-id="dee42-305">**Don't use triangular-shaped arrowheads for a purpose other than progressive disclosure.**</span></span>

    <span data-ttu-id="dee42-306">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-306">**Incorrect:**</span></span>

    ![<span data-ttu-id="dee42-307">具有右手三角形的標籤螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-307">screen shot of label with right-pointing triangle</span></span> ](images/progressive-disclosure-controls-image26.png)

    <span data-ttu-id="dee42-308">雖然此範例不是漸進式的洩漏模式，但是使用箭號表示命令會顯示在快顯視窗中。</span><span class="sxs-lookup"><span data-stu-id="dee42-308">Although this example isn't a progressive disclosure pattern, using an arrow here suggests that commands will be shown in a popup window.</span></span>

    <span data-ttu-id="dee42-309">**正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-309">**Correct:**</span></span>

    ![<span data-ttu-id="dee42-310">標籤的螢幕擷取畫面，包含文字的專案符號左方</span><span class="sxs-lookup"><span data-stu-id="dee42-310">screen shot of label with bullet left of the text</span></span> ](images/progressive-disclosure-controls-image27.png)

    <span data-ttu-id="dee42-311">在此範例中，會正確地使用專案符號。</span><span class="sxs-lookup"><span data-stu-id="dee42-311">In this example, a bullet is correctly used instead.</span></span>

-   <span data-ttu-id="dee42-312">**移除 (不會停用未在目前內容中套用) 累進洩漏控制項。**</span><span class="sxs-lookup"><span data-stu-id="dee42-312">**Remove (don't disable) progressive disclosure controls that don't apply in the current context.**</span></span> <span data-ttu-id="dee42-313">漸進式洩漏控制項應一律提供其承諾，因此當沒有其他資訊可提供時，請將其移除。</span><span class="sxs-lookup"><span data-stu-id="dee42-313">Progressive disclosure controls should always deliver on their promise, so remove them when there isn't more information to give.</span></span>

    <span data-ttu-id="dee42-314">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-314">**Incorrect:**</span></span>

    ![<span data-ttu-id="dee42-315">暗灰色 [更多選項] 控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-315">screen shot of a dimmed 'more options' control</span></span> ](images/progressive-disclosure-controls-image28.png)

    <span data-ttu-id="dee42-316">在此範例中，不會套用的漸進式洩漏控制項會不正確地停用。</span><span class="sxs-lookup"><span data-stu-id="dee42-316">In this example, a progressive disclosure control that doesn't apply is incorrectly disabled.</span></span>

### <a name="chevrons"></a><span data-ttu-id="dee42-317">角括弧</span><span class="sxs-lookup"><span data-stu-id="dee42-317">Chevrons</span></span>

-   <span data-ttu-id="dee42-318">**使用單一燕尾顯示或隱藏位置。使用雙燕尾顯示或隱藏使用快顯功能表。**</span><span class="sxs-lookup"><span data-stu-id="dee42-318">**Use single chevrons to show or hide in place. Use double chevrons to show or hide using a pop-up menu.**</span></span> <span data-ttu-id="dee42-319">不過，您應該一律將雙燕浮點數用於具有內部標籤的命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="dee42-319">You should always use double chevrons for command buttons with internal labels, however.</span></span>

    <span data-ttu-id="dee42-320">**正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-320">**Correct:**</span></span>

    ![<span data-ttu-id="dee42-321">單一箭號更多選項控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-321">screen shot of single-chevron more options control</span></span> ](images/progressive-disclosure-controls-image29.png)

    <span data-ttu-id="dee42-322">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-322">**Incorrect:**</span></span>

    ![<span data-ttu-id="dee42-323">雙箭號更多選項控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-323">screen shot of double-chevron more options control</span></span> ](images/progressive-disclosure-controls-image30.png)

    <span data-ttu-id="dee42-324">在不正確的範例中，會使用雙燕浮點數來進行就地漸進式洩漏。</span><span class="sxs-lookup"><span data-stu-id="dee42-324">In the incorrect example, a double chevron is used for in-place progressive disclosure.</span></span>

    <span data-ttu-id="dee42-325">**正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-325">**Correct:**</span></span>

    ![<span data-ttu-id="dee42-326">雙箭號更多命令按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-326">screen shot of double-chevron more command button</span></span> ](images/progressive-disclosure-controls-image31.png)

    <span data-ttu-id="dee42-327">在此範例中，會使用雙箭號來進行就地漸進式洩漏，因為它是具有內部標籤的命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="dee42-327">In this example, a double chevron is used for in-place progressive disclosure because it is a command button with an internal label.</span></span>

-   <span data-ttu-id="dee42-328">**提供箭號與其相關聯控制項之間的視覺化關聯性。**</span><span class="sxs-lookup"><span data-stu-id="dee42-328">**Provide a visual relationship between the chevron and its associated control.**</span></span> <span data-ttu-id="dee42-329">因為就地的燕號放在其相關聯 UI 的右邊，且靠右對齊，所以在箭號與其相關聯的控制項之間可能會有相當大的距離。</span><span class="sxs-lookup"><span data-stu-id="dee42-329">Because in-place chevrons are placed to the right of their associated UI and right aligned, there can be quite a distance between a chevron and its associated control.</span></span>

    <span data-ttu-id="dee42-330">**正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-330">**Correct:**</span></span>

    ![<span data-ttu-id="dee42-331">在控制項後面顯示漸進網底的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-331">screen shot of graduated shading behind controls</span></span> ](images/progressive-disclosure-controls-image32.png)

    <span data-ttu-id="dee42-332">在此範例中，就地箭號與其相關聯的 UI 之間有清楚的關聯性。</span><span class="sxs-lookup"><span data-stu-id="dee42-332">In this example, there is a clear relationship between the in-place chevron and its associated UI.</span></span>

    <span data-ttu-id="dee42-333">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-333">**Incorrect:**</span></span>

    ![<span data-ttu-id="dee42-334">控制項的立體白色背景螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-334">screen shot of solid-white background for controls</span></span> ](images/progressive-disclosure-controls-image33.png)

    <span data-ttu-id="dee42-335">在此範例中，就地箭號與其相關聯的 UI 之間沒有明確的視覺關聯性，因此它在空間中似乎是浮動的。</span><span class="sxs-lookup"><span data-stu-id="dee42-335">In this example, there is no clear visual relationship between the in-place chevron and its associated UI, so it seems to be floating in space.</span></span>

### <a name="arrows"></a><span data-ttu-id="dee42-336">箭頭</span><span class="sxs-lookup"><span data-stu-id="dee42-336">Arrows</span></span>

-   <span data-ttu-id="dee42-337">**請勿使用可能與上一頁、轉寄、Go 或 Play 混淆的箭號圖形。**</span><span class="sxs-lookup"><span data-stu-id="dee42-337">**Don't use arrow graphics that could be confused with Back, Forward, Go, or Play.**</span></span> <span data-ttu-id="dee42-338">使用簡單的三角形形箭號 (箭號，而不會在中性背景) 。</span><span class="sxs-lookup"><span data-stu-id="dee42-338">Use simple triangular-shaped arrowheads (arrows without stems) on neutral backgrounds.</span></span>

    <span data-ttu-id="dee42-339">**正確：**</span><span class="sxs-lookup"><span data-stu-id="dee42-339">**Correct:**</span></span>

    ![<span data-ttu-id="dee42-340">兩個小型黑色三角形的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-340">screen shot of two small black triangles</span></span> ](images/progressive-disclosure-controls-image34.png)

    <span data-ttu-id="dee42-341">這些箭號顯然是漸進式的公開控制項。</span><span class="sxs-lookup"><span data-stu-id="dee42-341">These arrows are clearly progressive disclosure controls.</span></span>

    <span data-ttu-id="dee42-342">**漸進式洩漏) 不正確的 (：**</span><span class="sxs-lookup"><span data-stu-id="dee42-342">**Incorrect (for progressive disclosure):**</span></span>

    ![<span data-ttu-id="dee42-343">兩個小綠色箭號的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-343">screen shot of two small green arrows</span></span> ](images/progressive-disclosure-controls-image35.png)

    <span data-ttu-id="dee42-344">這些箭號看起來不像漸進式的洩漏控制項。</span><span class="sxs-lookup"><span data-stu-id="dee42-344">These arrows don't look like progressive disclosure controls.</span></span>

    <span data-ttu-id="dee42-345">**反向 (不正確，向前) ：**</span><span class="sxs-lookup"><span data-stu-id="dee42-345">**Incorrect (for Back, Forward):**</span></span>

    ![<span data-ttu-id="dee42-346">具有黑色三角形的兩個按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-346">screen shot of two buttons with black triangles</span></span> ](images/progressive-disclosure-controls-image36.png)

    <span data-ttu-id="dee42-347">這些箭號看起來像漸進式洩漏控制項，但它們並不是。</span><span class="sxs-lookup"><span data-stu-id="dee42-347">These arrows look like progressive disclosure controls, but they are not.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="dee42-348">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="dee42-348">Recommended sizing and spacing</span></span>

![<span data-ttu-id="dee42-349">建議大小和間距的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="dee42-349">screen shot of recommended sizing and spacing</span></span> ](images/progressive-disclosure-controls-image37.png)

<span data-ttu-id="dee42-350">漸進式洩漏控制項的建議大小和間距。</span><span class="sxs-lookup"><span data-stu-id="dee42-350">Recommended sizing and spacing for progressive disclosure controls.</span></span>

## <a name="labels"></a><span data-ttu-id="dee42-351">標籤</span><span class="sxs-lookup"><span data-stu-id="dee42-351">Labels</span></span>

-   <span data-ttu-id="dee42-352">針對具有外部標籤的命令按鈕上的燕形：</span><span class="sxs-lookup"><span data-stu-id="dee42-352">For chevrons on a command button with an external label:</span></span>
    -   <span data-ttu-id="dee42-353">指派唯一的 [存取金鑰](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="dee42-353">Assign a unique [access key](glossary.md).</span></span> <span data-ttu-id="dee42-354">如需指導方針，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="dee42-354">For guidelines, see [Keyboard](inter-keyboard.md).</span></span>
    -   <span data-ttu-id="dee42-355">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="dee42-355">Use [sentence-style capitalization](glossary.md).</span></span>
    -   <span data-ttu-id="dee42-356">以片語的形式寫入標籤，並不使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="dee42-356">Write the label as a phrase and use no ending punctuation.</span></span>
    -   <span data-ttu-id="dee42-357">寫入標籤，讓它描述按一下按鈕的效果，並在狀態變更時變更標籤。</span><span class="sxs-lookup"><span data-stu-id="dee42-357">Write the label so that it describes the effect of clicking the button, and change the label when the state changes.</span></span>
    -   <span data-ttu-id="dee42-358">如果介面一律顯示一些選項、命令或詳細資料，請使用下列標籤配對：</span><span class="sxs-lookup"><span data-stu-id="dee42-358">If the surface always displays some options, commands, or details, use the following label pairs:</span></span>
        -   <span data-ttu-id="dee42-359">**更多/較少的選項。**</span><span class="sxs-lookup"><span data-stu-id="dee42-359">**More/Fewer options.**</span></span> <span data-ttu-id="dee42-360">用於選項或混合使用選項、命令和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dee42-360">Use for options or a mixture of options, commands, and details.</span></span>
        -   <span data-ttu-id="dee42-361">**更多/較少的命令。**</span><span class="sxs-lookup"><span data-stu-id="dee42-361">**More/Fewer commands.**</span></span> <span data-ttu-id="dee42-362">僅用於命令。</span><span class="sxs-lookup"><span data-stu-id="dee42-362">Use for commands only.</span></span>
        -   <span data-ttu-id="dee42-363">**更多/較少的詳細資料。**</span><span class="sxs-lookup"><span data-stu-id="dee42-363">**More/Fewer details.**</span></span> <span data-ttu-id="dee42-364">僅供資訊使用。</span><span class="sxs-lookup"><span data-stu-id="dee42-364">Use for information only.</span></span>
        -   <span data-ttu-id="dee42-365">**更多/較少 <object name> 。**</span><span class="sxs-lookup"><span data-stu-id="dee42-365">**More/Fewer <object name>.**</span></span> <span data-ttu-id="dee42-366">針對其他物件類型（例如資料夾）使用。</span><span class="sxs-lookup"><span data-stu-id="dee42-366">Use for other object types, such as folders.</span></span>
    -   <span data-ttu-id="dee42-367">否則：</span><span class="sxs-lookup"><span data-stu-id="dee42-367">Otherwise:</span></span>
        -   <span data-ttu-id="dee42-368">**顯示/隱藏選項。**</span><span class="sxs-lookup"><span data-stu-id="dee42-368">**Show/Hide options.**</span></span> <span data-ttu-id="dee42-369">用於選項或混合使用選項、命令和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dee42-369">Use for options or a mixture of options, commands, and details.</span></span>
        -   <span data-ttu-id="dee42-370">**顯示/隱藏命令。**</span><span class="sxs-lookup"><span data-stu-id="dee42-370">**Show/Hide commands.**</span></span> <span data-ttu-id="dee42-371">僅用於命令。</span><span class="sxs-lookup"><span data-stu-id="dee42-371">Use for commands only.</span></span>
        -   <span data-ttu-id="dee42-372">**顯示/隱藏詳細資料。**</span><span class="sxs-lookup"><span data-stu-id="dee42-372">**Show/Hide details.**</span></span> <span data-ttu-id="dee42-373">僅供資訊使用。</span><span class="sxs-lookup"><span data-stu-id="dee42-373">Use for information only.</span></span>
        -   <span data-ttu-id="dee42-374">**顯示/隱藏 <object name> 。**</span><span class="sxs-lookup"><span data-stu-id="dee42-374">**Show/Hide <object name>.**</span></span> <span data-ttu-id="dee42-375">針對其他物件類型（例如資料夾）使用。</span><span class="sxs-lookup"><span data-stu-id="dee42-375">Use for other object types, such as folders.</span></span>
-   <span data-ttu-id="dee42-376">若為具有內部標籤之命令按鈕上的燕，請遵循標準 [命令按鈕](ctrl-command-buttons.md) 指導方針。</span><span class="sxs-lookup"><span data-stu-id="dee42-376">For chevrons on a command button with an internal label, follow the standard [command button](ctrl-command-buttons.md) guidelines.</span></span>

## <a name="documentation"></a><span data-ttu-id="dee42-377">文件</span><span class="sxs-lookup"><span data-stu-id="dee42-377">Documentation</span></span>

<span data-ttu-id="dee42-378">參考漸進式洩漏控制項時：</span><span class="sxs-lookup"><span data-stu-id="dee42-378">When referring to progressive disclosure controls:</span></span>

-   <span data-ttu-id="dee42-379">如果控制項有固定標籤，請只依其標籤參考控制項;請勿嘗試描述控制項。</span><span class="sxs-lookup"><span data-stu-id="dee42-379">If the control has a fixed label, refer to the control by its label only; don't try to describe the control.</span></span> <span data-ttu-id="dee42-380">使用確切的標籤文字，包括其大小寫，但不包含存取金鑰底線。</span><span class="sxs-lookup"><span data-stu-id="dee42-380">Use the exact label text, including its capitalization, but don't include the access key underscore.</span></span>
-   <span data-ttu-id="dee42-381">如果控制項沒有標籤或未固定，請使用控制項的類型來參考控制項：箭號、箭號、三角形或加號/減號按鈕。</span><span class="sxs-lookup"><span data-stu-id="dee42-381">If the control has no label or it isn't fixed, refer to the control by its type: chevron, arrow, triangle, or plus/minus button.</span></span> <span data-ttu-id="dee42-382">如有必要，也請描述控制項的位置。</span><span class="sxs-lookup"><span data-stu-id="dee42-382">If necessary, also describe the control's location.</span></span> <span data-ttu-id="dee42-383">如果控制項以動態方式出現（例如 [頁面空間](glossary.md) 控制項），請藉由描述如何顯示控制項來開始參考。</span><span class="sxs-lookup"><span data-stu-id="dee42-383">If the control appears dynamically, such as the [page space](glossary.md) control, start the reference by describing how to make the control appear.</span></span>

    <span data-ttu-id="dee42-384">**範例：** 若要顯示資料夾內的檔案，請將指標移到資料夾名稱的開頭，然後按一下資料夾旁的三角形。</span><span class="sxs-lookup"><span data-stu-id="dee42-384">**Example:** To display the files within a folder, move the pointer to the start of the folder name, and then click the triangle next to the folder.</span></span>

-   <span data-ttu-id="dee42-385">請勿將控制項參考為按鈕，除非與其他不是按鈕的漸進式控制項相較之下。</span><span class="sxs-lookup"><span data-stu-id="dee42-385">Don't refer to the control as a button, unless to contrast with other progressive disclosure controls that aren't buttons.</span></span>
-   <span data-ttu-id="dee42-386">若要描述使用者互動，請使用按一下。</span><span class="sxs-lookup"><span data-stu-id="dee42-386">To describe user interaction, use click.</span></span> <span data-ttu-id="dee42-387">如果需要清楚起見，請使用按一下 .。。以展開或折迭。</span><span class="sxs-lookup"><span data-stu-id="dee42-387">If needed for clarity, use click...to expand or collapse.</span></span>
-   <span data-ttu-id="dee42-388">可能的話，請使用粗體文字來格式化標籤。</span><span class="sxs-lookup"><span data-stu-id="dee42-388">When possible, format the label using bold text.</span></span> <span data-ttu-id="dee42-389">否則，請只在必要時才將標籤放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="dee42-389">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="dee42-390">範例：</span><span class="sxs-lookup"><span data-stu-id="dee42-390">Examples:</span></span>

-   <span data-ttu-id="dee42-391"> (箭號) 來判斷檔案大小，請按一下 [ **詳細資料**]。</span><span class="sxs-lookup"><span data-stu-id="dee42-391">(For a chevron) To determine the file size, click **Details**.</span></span>
-   <span data-ttu-id="dee42-392"> (箭號) 若要查看所有選項，請按一下 [ **搜尋** ] 方塊旁邊的箭號。</span><span class="sxs-lookup"><span data-stu-id="dee42-392">(For an arrow) To see all the options, click the arrow next to the **Search** box.</span></span>
-   <span data-ttu-id="dee42-393"> (針對加號/減號) 若要查看您的圖片，請按一下 [ **圖片**]。</span><span class="sxs-lookup"><span data-stu-id="dee42-393">(For plus/minus) To view your picture, click **Pictures**.</span></span>

