---
title: 下拉式清單方塊
description: 在下拉式清單或下拉式方塊中，使用者可以在互斥值清單中進行選擇。
ms.assetid: dbe88cf1-7946-4343-bc16-ce12be7ce205
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ce9cbcac3495022edbb398bcbd78b35ac5265150
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524572"
---
# <a name="drop-down-lists--combo-boxes"></a><span data-ttu-id="061f1-103">下拉式方塊 & 下拉式清單</span><span class="sxs-lookup"><span data-stu-id="061f1-103">Drop-down Lists & Combo Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="061f1-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="061f1-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="061f1-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="061f1-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="061f1-106">在下拉式清單或下拉式方塊中，使用者可以在互斥值清單中進行選擇。</span><span class="sxs-lookup"><span data-stu-id="061f1-106">With a drop-down list or combo box, users make a choice among a list of mutually exclusive values.</span></span> <span data-ttu-id="061f1-107">使用者只能選擇一個選項。</span><span class="sxs-lookup"><span data-stu-id="061f1-107">Users can choose one and only one option.</span></span> <span data-ttu-id="061f1-108">使用標準下拉式清單時，使用者只能使用清單中的選項，但是您可以使用下拉式方塊來輸入不在清單中的選項。</span><span class="sxs-lookup"><span data-stu-id="061f1-108">With a standard drop-down list, users are limited to choices in the list, but with a combo box they can enter a choice that isn't in the list.</span></span>

![<span data-ttu-id="061f1-109">[提醒時間] 下拉式方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-109">screen shot of reminder time combo box</span></span> ](images/ctrl-drop-image1.png)

<span data-ttu-id="061f1-110">典型的下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-110">A typical combo box.</span></span>

<span data-ttu-id="061f1-111">當您閱讀這篇文章時，請務必瞭解下列詞彙：</span><span class="sxs-lookup"><span data-stu-id="061f1-111">The following terms are important to understand as you read this article:</span></span>

-   <span data-ttu-id="061f1-112">標準清單方塊是一個方塊，其中包含多個專案的清單，並顯示多個專案。</span><span class="sxs-lookup"><span data-stu-id="061f1-112">A standard list box is a box containing a list of multiple items, with multiple items visible.</span></span>
-   <span data-ttu-id="061f1-113">下拉式清單是一份清單，其中一律會顯示選取的專案，而其他專案則會按下下拉式按鈕，視需要顯示。</span><span class="sxs-lookup"><span data-stu-id="061f1-113">A drop-down list is a list in which the selected item is always visible, and the others are visible on demand by clicking a drop-down button.</span></span>
-   <span data-ttu-id="061f1-114">下拉式方塊是標準清單方塊或下拉式清單和可編輯 [文字方塊](ctrl-text-boxes.md)的組合，因此可讓使用者輸入不在清單中的值。</span><span class="sxs-lookup"><span data-stu-id="061f1-114">A combo box is a combination of a standard list box or a drop-down list and an editable [text box](ctrl-text-boxes.md), thus allowing users to enter a value that isn't in the list.</span></span>
    -   <span data-ttu-id="061f1-115">可編輯的下拉式清單是下拉式清單和可編輯文字方塊的組合。</span><span class="sxs-lookup"><span data-stu-id="061f1-115">An editable drop-down list is a combination of a drop-down list and an editable text box.</span></span>
    -   <span data-ttu-id="061f1-116">可編輯的清單方塊是標準清單方塊和可編輯文字方塊的組合。</span><span class="sxs-lookup"><span data-stu-id="061f1-116">An editable list box is a combination of a standard list box and an editable text box.</span></span>

> [!Note]  
> <span data-ttu-id="061f1-117">與 [版面](vis-layout.md) 配置相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="061f1-117">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="061f1-118">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="061f1-118">Is this the right control?</span></span>

<span data-ttu-id="061f1-119">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="061f1-119">To decide, consider these questions:</span></span>

-   <span data-ttu-id="061f1-120">**控制項是否可用來從互斥值清單中選擇一個選項？**</span><span class="sxs-lookup"><span data-stu-id="061f1-120">**Is the control used to choose one option from a list of mutually exclusive values?**</span></span> <span data-ttu-id="061f1-121">如果不是，請使用其他控制項。</span><span class="sxs-lookup"><span data-stu-id="061f1-121">If not, use another control.</span></span> <span data-ttu-id="061f1-122">若要選擇多個選項，請改為使用 [標準的多重選取清單](ctrl-list-boxes.md)、核取方塊清單、清單產生器或新增/移除清單。</span><span class="sxs-lookup"><span data-stu-id="061f1-122">To choose multiple options, use a [standard multiple-selection list](ctrl-list-boxes.md), check box list, list builder, or add/remove list instead.</span></span>
-   <span data-ttu-id="061f1-123">**選項是命令嗎？**</span><span class="sxs-lookup"><span data-stu-id="061f1-123">**Are the options commands?**</span></span> <span data-ttu-id="061f1-124">若是如此，請改用 [功能表按鈕](ctrl-command-buttons.md) 或分割按鈕。</span><span class="sxs-lookup"><span data-stu-id="061f1-124">If so, use a [menu button](ctrl-command-buttons.md) or split button instead.</span></span> <span data-ttu-id="061f1-125">針對 (名詞) 或屬性 (形容詞) ，而不是 (動詞命令) 命令的物件，請使用下拉式清單與下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-125">Use drop-down lists and combo boxes for objects (nouns) or attributes (adjectives), but not commands (verbs).</span></span>
-   <span data-ttu-id="061f1-126">**清單是否會顯示資料，而不是程式選項？**</span><span class="sxs-lookup"><span data-stu-id="061f1-126">**Does the list present data, rather than program options?**</span></span> <span data-ttu-id="061f1-127">無論何種方式，下拉式清單或下拉式方塊都是適合的選擇。</span><span class="sxs-lookup"><span data-stu-id="061f1-127">Either way, a drop-down list or combo box is a suitable choice.</span></span> <span data-ttu-id="061f1-128">相較之下， [選項按鈕](ctrl-radio-buttons.md) 只適用于少數的程式選項。</span><span class="sxs-lookup"><span data-stu-id="061f1-128">By contrast, [radio buttons](ctrl-radio-buttons.md) are suitable only for a small number of program options.</span></span>

<span data-ttu-id="061f1-129">**下拉式清單**</span><span class="sxs-lookup"><span data-stu-id="061f1-129">**Drop-down lists**</span></span>

-   <span data-ttu-id="061f1-130">**大部分的使用者在大多數情況下，是否有建議使用的預設選項？**</span><span class="sxs-lookup"><span data-stu-id="061f1-130">**Is there a default option that is recommended for most users in most situations?**</span></span> <span data-ttu-id="061f1-131">看到選取的選項遠比看到替代方案更重要嗎？</span><span class="sxs-lookup"><span data-stu-id="061f1-131">Is seeing the selected option far more important than seeing the alternatives?</span></span> <span data-ttu-id="061f1-132">如果您不想要鼓勵使用者藉由隱藏替代方案來進行變更，請考慮使用下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="061f1-132">Consider using a drop-down list if you don't want to encourage users to make changes by hiding the alternatives.</span></span> <span data-ttu-id="061f1-133">如果沒有，請考慮使用選項按鈕、單選清單，或可編輯的清單方塊，以提供更多強調替代選項。</span><span class="sxs-lookup"><span data-stu-id="061f1-133">If not, consider radio buttons, a single-selection list, or an editable list box, which give more emphasis to the alternative choices.</span></span>

    ![<span data-ttu-id="061f1-134">最高品質作為預設按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-134">screen shot of highest quality as default button</span></span> ](images/ctrl-drop-image2.png)

    <span data-ttu-id="061f1-135">在此範例中，最高的色彩品質是大部分使用者的最佳選擇，因此下拉式清單是把替代方案的理想選擇。</span><span class="sxs-lookup"><span data-stu-id="061f1-135">In this example, the highest color quality is the best choice for most users, so a drop-down list is a good choice to downplay the alternatives.</span></span>

-   <span data-ttu-id="061f1-136">**您是否想要強調選項？**</span><span class="sxs-lookup"><span data-stu-id="061f1-136">**Do you want to draw attention to the option?**</span></span> <span data-ttu-id="061f1-137">如果是，請考慮使用選項按鈕、單選清單，或可編輯的清單方塊，這通常會以更多的螢幕空間來繪製更多的注意力。</span><span class="sxs-lookup"><span data-stu-id="061f1-137">If so, consider radio buttons, a single-selection list, or an editable list box, which tend to draw more attention by taking more screen space.</span></span> <span data-ttu-id="061f1-138">因為下拉式清單是 compact，所以它們是您想要 underemphasize 之選項的理想選擇。</span><span class="sxs-lookup"><span data-stu-id="061f1-138">Because drop-down lists are compact, they are good choices for options that you want to underemphasize.</span></span>
-   <span data-ttu-id="061f1-139">**螢幕空間是否在 premium？**</span><span class="sxs-lookup"><span data-stu-id="061f1-139">**Is screen space at a premium?**</span></span> <span data-ttu-id="061f1-140">如果是的話，請使用下拉式清單，因為所使用的螢幕空間是固定的，而且與選擇的數目無關。</span><span class="sxs-lookup"><span data-stu-id="061f1-140">If so, use a drop-down list because the screen space used is fixed and independent of the number of choices.</span></span>
-   <span data-ttu-id="061f1-141">**視窗上是否有其他下拉式清單？**</span><span class="sxs-lookup"><span data-stu-id="061f1-141">**Are there other drop-down lists on the window?**</span></span> <span data-ttu-id="061f1-142">如果是的話，請考慮使用下拉式清單來保持一致性。</span><span class="sxs-lookup"><span data-stu-id="061f1-142">If so, consider using a drop-down list for consistency.</span></span>

<span data-ttu-id="061f1-143">**可編輯的下拉式清單**</span><span class="sxs-lookup"><span data-stu-id="061f1-143">**Editable drop-down lists**</span></span>

<span data-ttu-id="061f1-144">除了針對下拉式清單所提供的準則之外，下列也適用：</span><span class="sxs-lookup"><span data-stu-id="061f1-144">In addition to the principles just provided for drop-down lists, the following also apply:</span></span>

-   <span data-ttu-id="061f1-145">**是否有可能的選項受限制？**</span><span class="sxs-lookup"><span data-stu-id="061f1-145">**Are the possible choices constrained?**</span></span> <span data-ttu-id="061f1-146">如果是的話，請改用一般下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="061f1-146">If so, use a normal drop-down list instead.</span></span> <span data-ttu-id="061f1-147">下拉式方塊適用于未受限制的輸入，其中使用者可能需要輸入目前不在清單中的值。</span><span class="sxs-lookup"><span data-stu-id="061f1-147">Combo boxes are for unconstrained input, in which users may need to enter a value not currently in the list.</span></span> <span data-ttu-id="061f1-148">因為輸入不受限制，所以如果使用者輸入不正確文字，您必須處理錯誤並顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="061f1-148">Because the input is unconstrained, if users enter text that isn't valid you must handle the error with an error message.</span></span>
-   <span data-ttu-id="061f1-149">**您可以事先列舉最有可能的選擇** 嗎？</span><span class="sxs-lookup"><span data-stu-id="061f1-149">**Can you enumerate the most likely choices in advance**?</span></span> <span data-ttu-id="061f1-150">如果沒有，請改用文字方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-150">If not, use a text box instead.</span></span>
-   <span data-ttu-id="061f1-151">**下拉式清單是用來列出先前的使用者輸入嗎？**</span><span class="sxs-lookup"><span data-stu-id="061f1-151">**Is the drop-down list being used to list previous user input?**</span></span> <span data-ttu-id="061f1-152">除非使用者需要檢查先前輸入的完整清單，否則請改用具有自動完成選項的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-152">Unless users need to review the complete list of previous input, use a text box with the auto-complete option instead.</span></span>

    ![<span data-ttu-id="061f1-153">具有下拉式清單的 [執行] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-153">screen shot of run dialog box with drop-down list</span></span> ](images/ctrl-drop-image3.png)

    <span data-ttu-id="061f1-154">在此範例中，使用者可能需要檢查先前的輸入，因此可編輯的下拉式清單是不錯的選擇。</span><span class="sxs-lookup"><span data-stu-id="061f1-154">In this example, users may need to review their previous input, so an editable drop-down list is a good choice.</span></span>

    ![<span data-ttu-id="061f1-155">outlook 至折線圖和自動完成的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-155">screen shot of outlook to line and auto-complete</span></span> ](images/ctrl-drop-image4.png)

    <span data-ttu-id="061f1-156">在此範例中，具有自動完成的文字方塊是不錯的選擇。</span><span class="sxs-lookup"><span data-stu-id="061f1-156">In this example, a text box with auto-complete is a good choice.</span></span>

-   <span data-ttu-id="061f1-157">**使用者是否需要協助來選取有效的值？**</span><span class="sxs-lookup"><span data-stu-id="061f1-157">**Will users need assistance in selecting valid values?**</span></span> <span data-ttu-id="061f1-158">如果是的話，請改用具有 [瀏覽按鈕](ctrl-command-buttons.md) 的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-158">If so, use a text box with a [Browse button](ctrl-command-buttons.md) instead.</span></span>

    ![<span data-ttu-id="061f1-159">outlook 至折線圖和瀏覽按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-159">screen shot of outlook to line and browse button</span></span> ](images/ctrl-drop-image5.png)

    <span data-ttu-id="061f1-160">在此範例中，使用者可以按一下 [到] 以協助他們選取有效的值。</span><span class="sxs-lookup"><span data-stu-id="061f1-160">In this example, users can click "To" to help them select valid values.</span></span>

-   <span data-ttu-id="061f1-161">**建議使用者查看替代選項或邀請變更是否很重要？**</span><span class="sxs-lookup"><span data-stu-id="061f1-161">**Is it important to encourage users to review the alternative choices or invite change?**</span></span> <span data-ttu-id="061f1-162">如果是的話，請考慮改用可編輯的清單方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-162">If so, consider using an editable list box instead.</span></span> <span data-ttu-id="061f1-163">使用可編輯的下拉式清單時，使用者將不會察覺到此清單中的替代方案。</span><span class="sxs-lookup"><span data-stu-id="061f1-163">With an editable drop-down list, users aren't going to be aware of the alternatives until the list is dropped.</span></span>
-   <span data-ttu-id="061f1-164">**使用者是否需要在大型清單中快速找出專案？**</span><span class="sxs-lookup"><span data-stu-id="061f1-164">**Do users need to locate an item rapidly in a large list?**</span></span> <span data-ttu-id="061f1-165"> (Win32 僅) 如果有，請使用下拉式方塊，因為使用者可以輸入其完整名稱來選取專案。</span><span class="sxs-lookup"><span data-stu-id="061f1-165">(Win32 only) If so, use a combo box because users can select an item by typing its full name.</span></span> <span data-ttu-id="061f1-166">相較之下，Win32 下拉式清單只會根據輸入的最後一個字元來選取專案 (因此，在月份清單中輸入「六月」將符合11月，而不是6月) 。</span><span class="sxs-lookup"><span data-stu-id="061f1-166">By contrast, the Win32 drop-down list selects items based only by the last character typed (so typing "Jun" into a list of months would match November, not June).</span></span> <span data-ttu-id="061f1-167">在此情況下，即使可能的選項受到限制，也請使用下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-167">In this case, use a combo box even if the possible choices are constrained.</span></span>

<span data-ttu-id="061f1-168">**可編輯的清單方塊**</span><span class="sxs-lookup"><span data-stu-id="061f1-168">**Editable list boxes**</span></span>

-   <span data-ttu-id="061f1-169">**是否有可能的選項受限制？**</span><span class="sxs-lookup"><span data-stu-id="061f1-169">**Are the possible choices constrained?**</span></span> <span data-ttu-id="061f1-170">如果是的話，請改為使用單一選取清單或一般下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="061f1-170">If so, use a single-selection list or normal drop-down list instead.</span></span> <span data-ttu-id="061f1-171">下拉式方塊適用于未受限制的輸入，其中使用者可能需要輸入目前不在清單中的值。</span><span class="sxs-lookup"><span data-stu-id="061f1-171">Combo boxes are for unconstrained input, where users may need to enter a value not currently in the list.</span></span> <span data-ttu-id="061f1-172">因為輸入不受限制，所以如果使用者輸入不正確文字，您必須處理錯誤並顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="061f1-172">Because the input is unconstrained, if users enter text that is not valid you must handle the error with an error message.</span></span>
-   <span data-ttu-id="061f1-173">**您可以事先列舉最有可能的選擇嗎？**</span><span class="sxs-lookup"><span data-stu-id="061f1-173">**Can you enumerate the most likely choices in advance?**</span></span> <span data-ttu-id="061f1-174">如果沒有，請改用文字方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-174">If not, use a text box instead.</span></span>
-   <span data-ttu-id="061f1-175">**建議使用者查看替代選項或邀請變更是否很重要？**</span><span class="sxs-lookup"><span data-stu-id="061f1-175">**Is it important to encourage users to review the alternative choices or invite change?**</span></span> <span data-ttu-id="061f1-176">如果沒有，請考慮改用可編輯的下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="061f1-176">If not, consider an editable drop-down list instead.</span></span>
-   <span data-ttu-id="061f1-177">**您是否想要強調選項？**</span><span class="sxs-lookup"><span data-stu-id="061f1-177">**Do you want to draw attention to the option?**</span></span> <span data-ttu-id="061f1-178">如果沒有，請考慮改用可編輯的下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="061f1-178">If not, consider an editable drop-down list instead.</span></span> <span data-ttu-id="061f1-179">因為下拉式清單是 compact，所以它們是您想要 underemphasize 之選項的理想選擇。</span><span class="sxs-lookup"><span data-stu-id="061f1-179">Because drop-down lists are compact, they are good choices for options that you want to underemphasize.</span></span>
-   <span data-ttu-id="061f1-180">**螢幕空間是否在 premium？**</span><span class="sxs-lookup"><span data-stu-id="061f1-180">**Is screen space at a premium?**</span></span> <span data-ttu-id="061f1-181">如果是的話，請使用可編輯的下拉式清單，因為所使用的螢幕空間是固定的，而且與選擇的數目無關。</span><span class="sxs-lookup"><span data-stu-id="061f1-181">If so, use an editable drop-down list because the screen space used is fixed and independent of the number of choices.</span></span>

<span data-ttu-id="061f1-182">如果是下拉式清單， **清單中的專案數目不是選擇控制項的因素** ，因為它們的範圍從上千個專案到一。</span><span class="sxs-lookup"><span data-stu-id="061f1-182">For drop-down lists, **the number of items in the list isn't a factor in choosing the control** because they scale from thousands of items all the way down to one.</span></span> <span data-ttu-id="061f1-183">可編輯的下拉式清單會從上千個專案縮小為無，因為使用者可以輸入不在清單中的值。</span><span class="sxs-lookup"><span data-stu-id="061f1-183">Editable drop-down lists scale from thousands of items down to none, because users can enter a value that isn't in the list.</span></span> <span data-ttu-id="061f1-184">因為下拉式清單可用於資料，所以可能事先不知道專案的數量，而且可能無法保證。</span><span class="sxs-lookup"><span data-stu-id="061f1-184">Because drop-down lists can be used for data, the number of items might not be known in advance and perhaps cannot be guaranteed.</span></span> <span data-ttu-id="061f1-185">**在可編輯的清單方塊中一律包含至少三個專案，以證明額外的螢幕空間。**</span><span class="sxs-lookup"><span data-stu-id="061f1-185">**Always include at least three items in editable list boxes to justify the additional screen space.**</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="061f1-186">使用模式</span><span class="sxs-lookup"><span data-stu-id="061f1-186">Usage patterns</span></span>

<span data-ttu-id="061f1-187">下拉式清單和下拉式方塊有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="061f1-187">Drop-down lists and combo boxes have several usage patterns:</span></span>



|   <span data-ttu-id="061f1-188">使用狀況</span><span class="sxs-lookup"><span data-stu-id="061f1-188">Usage</span></span>     |    <span data-ttu-id="061f1-189">範例</span><span class="sxs-lookup"><span data-stu-id="061f1-189">Example</span></span>   |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="061f1-190">**下拉式** 清單：標準下拉式清單，其中包含一組固定的預先決定值。</span><span class="sxs-lookup"><span data-stu-id="061f1-190">**Drop-down list** a standard drop-down list, with a fixed set of predetermined values.</span></span> <br/>                                 | <span data-ttu-id="061f1-191">當關閉時，只會顯示選取的專案。</span><span class="sxs-lookup"><span data-stu-id="061f1-191">when closed, only the selected item is visible.</span></span> <span data-ttu-id="061f1-192">當使用者按一下下拉式按鈕時，所有選項都會變成可見。</span><span class="sxs-lookup"><span data-stu-id="061f1-192">when users click the drop-down button, all the options become visible.</span></span> <span data-ttu-id="061f1-193">若要變更此值，使用者可以開啟清單，然後按一下另一個值。</span><span class="sxs-lookup"><span data-stu-id="061f1-193">to change the value, users open the list and click another value.</span></span><br/> ![<span data-ttu-id="061f1-194">下拉式清單的螢幕擷取畫面，隱藏的選項</span><span class="sxs-lookup"><span data-stu-id="061f1-194">screen shot of drop-down list, options hidden</span></span> ](images/ctrl-drop-image6.png)<br/> <span data-ttu-id="061f1-195">在此範例中，清單處於正常狀態。</span><span class="sxs-lookup"><span data-stu-id="061f1-195">in this example, the list is in its normal state.</span></span><br/> ![<span data-ttu-id="061f1-196">下拉式清單的螢幕擷取畫面，顯示選項</span><span class="sxs-lookup"><span data-stu-id="061f1-196">screen shot of drop-down list, options displayed</span></span> ](images/ctrl-drop-image7.png)<br/> <span data-ttu-id="061f1-197">在此範例中，清單已中斷。</span><span class="sxs-lookup"><span data-stu-id="061f1-197">In this example, the list has been dropped down.</span></span><br/> |
| <span data-ttu-id="061f1-198">[**預覽] 下拉式** 清單，其中有一個下拉式清單，可預覽選取專案的結果以協助使用者選擇。</span><span class="sxs-lookup"><span data-stu-id="061f1-198">**Preview drop-down list** a drop-down list that previews the results of the selection to help users choose.</span></span><br/>             | ![<span data-ttu-id="061f1-199">色彩和文字選項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-199">screen shot of color and text options</span></span> ](images/ctrl-drop-image8.png)<br/> <span data-ttu-id="061f1-200">在這些範例中，下拉式清單會預覽選取專案的結果。</span><span class="sxs-lookup"><span data-stu-id="061f1-200">In these examples, the drop-down lists preview the results of the selection.</span></span><br/>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="061f1-201">**可編輯的下拉式清單** 下拉式方塊，可讓使用者輸入不在下拉式清單中的值。</span><span class="sxs-lookup"><span data-stu-id="061f1-201">**Editable drop-down list** a drop-down combo box, which allows users to enter a value that isn't in the drop-down list.</span></span><br/> | ![aa511458. dropdownlists27 (en-us，msdn. 10) .png](images/ctrl-drop-image9.png)![<span data-ttu-id="061f1-203">可編輯的字型大小下拉式方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-203">screen shot of editable font-size combo box</span></span> ](images/ctrl-drop-image10.png)<br/> <span data-ttu-id="061f1-204">編輯和卸載模式中可編輯的下拉式清單範例。</span><span class="sxs-lookup"><span data-stu-id="061f1-204">Examples of an editable drop-down list in edit and dropped-down modes.</span></span><br/> <span data-ttu-id="061f1-205">當您想要提供文字方塊的彈性，但想要提供方便的選項清單來協助使用者時，請使用這個控制項。</span><span class="sxs-lookup"><span data-stu-id="061f1-205">Use this control when you want to give the flexibility of a text box, yet want to assist users by providing a convenient list of likely choices.</span></span><br/>                                                                                                   |
| <span data-ttu-id="061f1-206">**可編輯的清單方塊** ：一般下拉式方塊，可讓使用者輸入不在 [永遠可見] 清單中的值。</span><span class="sxs-lookup"><span data-stu-id="061f1-206">**Editable list boxes** a regular combo box, which allows users to enter a value that isn't in the always visible list.</span></span> <br/> | ![<span data-ttu-id="061f1-207">字型選項下拉式清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-207">screen shot of drop-down list of font options</span></span> ](images/ctrl-drop-image11.png)<br/> <span data-ttu-id="061f1-208">在這些範例中，一律會顯示可編輯的清單方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-208">In these examples, the editable list boxes are always displayed.</span></span><br/> <span data-ttu-id="061f1-209">當建議使用者檢查替代選項或邀請變更時，此控制項是比可編輯的下拉式清單更好的選擇。</span><span class="sxs-lookup"><span data-stu-id="061f1-209">This control is a better choice than the editable drop-down list when it is important to encourage users to review the alternative choices or invite change.</span></span><br/>                                                                                                                                                                      |



 

## <a name="guidelines"></a><span data-ttu-id="061f1-210">指導方針</span><span class="sxs-lookup"><span data-stu-id="061f1-210">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="061f1-211">一般</span><span class="sxs-lookup"><span data-stu-id="061f1-211">General</span></span>

-   <span data-ttu-id="061f1-212">**請勿使用下拉式清單或下拉式方塊的變更來**：</span><span class="sxs-lookup"><span data-stu-id="061f1-212">**Don't use the change of a drop-down list or combo box to**:</span></span>
    -   <span data-ttu-id="061f1-213">執行命令。</span><span class="sxs-lookup"><span data-stu-id="061f1-213">Perform commands.</span></span>
    -   <span data-ttu-id="061f1-214">顯示其他視窗，例如用來收集更多輸入的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-214">Display other windows, such as a dialog box to gather more input.</span></span>
    -   <span data-ttu-id="061f1-215">以動態方式顯示與所選取控制項相關的其他控制項 ([畫面讀取器](inter-accessibility.md) 無法偵測到這類事件) 。</span><span class="sxs-lookup"><span data-stu-id="061f1-215">Dynamically display other controls related to the selected control ([screen readers](inter-accessibility.md) cannot detect such events).</span></span>

### <a name="presentation"></a><span data-ttu-id="061f1-216">簡報</span><span class="sxs-lookup"><span data-stu-id="061f1-216">Presentation</span></span>

-   <span data-ttu-id="061f1-217">**以邏輯順序排序清單專案**，例如將高度相關的選項群組在一起，並優先放置最常見的選項，或使用依字母順序排列的選項。</span><span class="sxs-lookup"><span data-stu-id="061f1-217">**Sort list items in a logical order**, such as grouping highly related options together, placing most common options first, or using alphabetical order.</span></span> <span data-ttu-id="061f1-218">依字母順序排序名稱、依數位順序排序數位和日期（以時間順序排列）。</span><span class="sxs-lookup"><span data-stu-id="061f1-218">Sort names in alphabetical order, numbers in numeric order, and dates in chronological order.</span></span> <span data-ttu-id="061f1-219">具有12個以上專案的清單應依字母順序排序，讓專案更容易尋找。</span><span class="sxs-lookup"><span data-stu-id="061f1-219">Lists with 12 or more items should be sorted alphabetically to make items easier to find.</span></span>

    <span data-ttu-id="061f1-220">**正確：** ![邏輯下拉式清單的螢幕擷取畫面 ](images/ctrl-drop-image12.png)</span><span class="sxs-lookup"><span data-stu-id="061f1-220">**Correct:** ![screen shot of logical drop-down list ](images/ctrl-drop-image12.png)</span></span>

    <span data-ttu-id="061f1-221">在此範例中，清單專案依其空間關聯性排序。</span><span class="sxs-lookup"><span data-stu-id="061f1-221">In this example, the list items are sorted by their spatial relationship.</span></span>

    <span data-ttu-id="061f1-222">**不正確：** ![[雜亂無章] 下拉式清單的螢幕擷取畫面 ](images/ctrl-drop-image13.png)</span><span class="sxs-lookup"><span data-stu-id="061f1-222">**Incorrect:** ![screen shot of disorganized drop-down list ](images/ctrl-drop-image13.png)</span></span>

    <span data-ttu-id="061f1-223">在此範例中，有很多清單專案需要依字母順序排序。</span><span class="sxs-lookup"><span data-stu-id="061f1-223">In this example, there are so many list items that they need to be sorted in alphabetical order.</span></span>

    <span data-ttu-id="061f1-224">**正確：** ![依字母順序排列下拉式清單的螢幕擷取畫面 ](images/ctrl-drop-image14.png)</span><span class="sxs-lookup"><span data-stu-id="061f1-224">**Correct:** ![screen shot of alphabetized drop-down list ](images/ctrl-drop-image14.png)</span></span>

    <span data-ttu-id="061f1-225">在此範例中，清單專案會依字母順序排序，但代表所有專案的選項除外。</span><span class="sxs-lookup"><span data-stu-id="061f1-225">In this example, the list items are sorted in alphabetical order except for the option that represents all items.</span></span>

-   <span data-ttu-id="061f1-226">**無論其餘專案的排序次序為何，都可在清單的開頭放置代表 All 或 None 的選項。**</span><span class="sxs-lookup"><span data-stu-id="061f1-226">**Place options that represent All or None at the beginning of the list, regardless of the sort order of the remaining items.**</span></span>
-   <span data-ttu-id="061f1-227">**以括弧括住中繼選項。**</span><span class="sxs-lookup"><span data-stu-id="061f1-227">**Enclose meta-options in parentheses.**</span></span>

    ![顯示已選取 [無 () ] 之下拉式清單的螢幕擷取畫面。](images/ctrl-drop-image15.png)

    <span data-ttu-id="061f1-229">在此範例中，「 (無) 」是中繼選項，因為它不是有效的選項值，而是描述該選項本身未使用。</span><span class="sxs-lookup"><span data-stu-id="061f1-229">In this example, "(None)" is a meta-option because it is not a valid value for the choice rather it describes that the option itself isn't being used.</span></span>

-   <span data-ttu-id="061f1-230">**停用下拉式清單或下拉式方塊時，也會停用任何相關聯的標籤和命令按鈕。**</span><span class="sxs-lookup"><span data-stu-id="061f1-230">**When disabling a drop-down list or combo box, also disable any associated labels and command buttons.**</span></span>

### <a name="drop-down-lists"></a><span data-ttu-id="061f1-231">下拉式清單</span><span class="sxs-lookup"><span data-stu-id="061f1-231">Drop-down lists</span></span>

-   <span data-ttu-id="061f1-232">當您使用單一下拉式清單來變更相關聯控制項的視圖時，請 **在選取時立即變更視圖，而不需要個別的命令按鈕。**</span><span class="sxs-lookup"><span data-stu-id="061f1-232">When a single drop-down list is used to change the view of an associated control, **change the view immediately on selection instead of requiring a separate command button.**</span></span> <span data-ttu-id="061f1-233">只有在清單需要很長的時間才能轉譯時，才使用個別的命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="061f1-233">Use a separate command button only if the list takes a significant amount of time to render.</span></span> <span data-ttu-id="061f1-234">不過，清單標頭和 [功能表按鈕](ctrl-command-buttons.md) 是此用途的慣用控制項。</span><span class="sxs-lookup"><span data-stu-id="061f1-234">However, list headers and [menu buttons](ctrl-command-buttons.md) are the preferred controls for this purpose.</span></span>
-   <span data-ttu-id="061f1-235">**不要有空白清單專案** 改用 **中繼選項**。</span><span class="sxs-lookup"><span data-stu-id="061f1-235">**Don't have blank list items** **use meta-options instead**.</span></span> <span data-ttu-id="061f1-236">使用者不知道如何解讀空白專案，而中繼選項的意義是明確的。</span><span class="sxs-lookup"><span data-stu-id="061f1-236">Users don't know how to interpret blank items, whereas the meaning of meta-options is explicit.</span></span>

    <span data-ttu-id="061f1-237">**正確：** ![下拉式清單的螢幕擷取畫面，其中已選取 [無] ](images/ctrl-drop-image16.png)</span><span class="sxs-lookup"><span data-stu-id="061f1-237">**Correct:** ![screen shot of drop-down list with none selected ](images/ctrl-drop-image16.png)</span></span>

    <span data-ttu-id="061f1-238">**不正確：** ![已選取空白的下拉式清單螢幕擷取畫面 ](images/ctrl-drop-image17.png)</span><span class="sxs-lookup"><span data-stu-id="061f1-238">**Incorrect:** ![screen shot of drop-down list with blank selected ](images/ctrl-drop-image17.png)</span></span>

    <span data-ttu-id="061f1-239">在不正確的範例中，空白選項的意義不清楚。</span><span class="sxs-lookup"><span data-stu-id="061f1-239">In the incorrect example, the meaning of the blank option is unclear.</span></span>

### <a name="preview-drop-down-lists"></a><span data-ttu-id="061f1-240">預覽下拉式清單</span><span class="sxs-lookup"><span data-stu-id="061f1-240">Preview drop-down lists</span></span>

-   <span data-ttu-id="061f1-241">**在清單專案中使用 [預覽]，比使用單獨描述的影像更清楚地顯示。**</span><span class="sxs-lookup"><span data-stu-id="061f1-241">**Use previews in the list items when it is better to show with images than describe using text alone.**</span></span>

    ![<span data-ttu-id="061f1-242">預覽字體下拉式清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-242">screen shot of drop-down list of fonts previewed</span></span> ](images/ctrl-drop-image18.png)

    <span data-ttu-id="061f1-243">在此範例中，預覽會解釋比單獨文字更好的選項。</span><span class="sxs-lookup"><span data-stu-id="061f1-243">In this example, the preview explains the options far better than text alone.</span></span>

-   <span data-ttu-id="061f1-244">**請勿在預覽中使用不必要的無用圖示**。</span><span class="sxs-lookup"><span data-stu-id="061f1-244">**Don't use unnecessary, unhelpful icons in previews**.</span></span>

    <span data-ttu-id="061f1-245">**不正確：** ![具有圖示之標籤下拉式清單的螢幕擷取畫面 ](images/ctrl-drop-image19.png)</span><span class="sxs-lookup"><span data-stu-id="061f1-245">**Incorrect:** ![screen shot of drop-down list of labels with icons ](images/ctrl-drop-image19.png)</span></span>

    <span data-ttu-id="061f1-246">在此範例中，預覽圖示是不必要的，因為它們不會傳達任何資訊。</span><span class="sxs-lookup"><span data-stu-id="061f1-246">In this example, the preview icons are unnecessary because they don't communicate any information.</span></span>

### <a name="combo-boxes"></a><span data-ttu-id="061f1-247">下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="061f1-247">Combo boxes</span></span>

-   <span data-ttu-id="061f1-248">**當您可以時，限制輸入文字的長度。**</span><span class="sxs-lookup"><span data-stu-id="061f1-248">**Limit the length of the input text when you can.**</span></span> <span data-ttu-id="061f1-249">例如，如果有效的輸入是介於0和999之間的數位，請使用限制為三個字元的下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-249">For example, if the valid input is a number between 0 and 999, use a combo box that is limited to three characters.</span></span>
-   <span data-ttu-id="061f1-250">**如果有許多可能的選項，請將清單內容放在最有可能的選項上**。</span><span class="sxs-lookup"><span data-stu-id="061f1-250">**If there are many possible options, focus the list contents on the most likely options**.</span></span> <span data-ttu-id="061f1-251">由於使用者可以輸入不在清單中的值，因此下拉式方塊不需要列出所有選項，只要是可能的選擇或代表性範例。</span><span class="sxs-lookup"><span data-stu-id="061f1-251">Because users can enter values that aren't in the list, combo boxes don't have to list all choices, just the likely choices or a representative sample.</span></span>

    ![<span data-ttu-id="061f1-252">字型大小下拉式清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-252">screen shot of drop-down list of font sizes</span></span> ](images/ctrl-drop-image10.png)

    <span data-ttu-id="061f1-253">在此範例中，不會列出許多有效的選項，例如15或一半大小的字型，例如9.5。</span><span class="sxs-lookup"><span data-stu-id="061f1-253">In this example, many valid choices aren't listed, such as 15, or half-size fonts such as 9.5.</span></span>

### <a name="default-values"></a><span data-ttu-id="061f1-254">預設值</span><span class="sxs-lookup"><span data-stu-id="061f1-254">Default values</span></span>

-   <span data-ttu-id="061f1-255">**依預設，請選取最安全的 (，以防止遺失資料或系統存取) 和最安全的選項。**</span><span class="sxs-lookup"><span data-stu-id="061f1-255">**Select the safest (to prevent loss of data or system access) and most secure option by default.**</span></span> <span data-ttu-id="061f1-256">如果安全性和安全性不是因素，請選取最有可能或方便的選項。</span><span class="sxs-lookup"><span data-stu-id="061f1-256">If safety and security aren't factors, select the most likely or convenient option.</span></span>
    -   <span data-ttu-id="061f1-257">**例外狀況：** 如果控制項代表 [混合狀態](glossary.md)中的屬性，則顯示空白的預設值，這會在顯示多個沒有相同設定之物件的屬性時發生。</span><span class="sxs-lookup"><span data-stu-id="061f1-257">**Exception:** Display a blank default value if the control represents a property in a [mixed state](glossary.md), which happens when displaying a property for multiple objects that don't have the same setting.</span></span>

## <a name="prompts"></a><span data-ttu-id="061f1-258">提示</span><span class="sxs-lookup"><span data-stu-id="061f1-258">Prompts</span></span>

<span data-ttu-id="061f1-259">提示是在可編輯的下拉式清單內放置的標籤或簡短指令，作為其預設值。</span><span class="sxs-lookup"><span data-stu-id="061f1-259">A prompt is a label or short instruction placed inside an editable drop-down list as its default value.</span></span> <span data-ttu-id="061f1-260">與靜態文字不同的是，當使用者在下拉式方塊中輸入某個內容或取得輸入焦點時，會從畫面中消失。</span><span class="sxs-lookup"><span data-stu-id="061f1-260">Unlike static text, prompts disappear from the screen once users type something into the combo box or it gets input focus.</span></span>

![<span data-ttu-id="061f1-261">搜尋方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-261">screen shot of a search box</span></span> ](images/ctrl-drop-image20.png)

<span data-ttu-id="061f1-262">典型的提示。</span><span class="sxs-lookup"><span data-stu-id="061f1-262">A typical prompt.</span></span>

<span data-ttu-id="061f1-263">在下列情況下使用提示：</span><span class="sxs-lookup"><span data-stu-id="061f1-263">Use a prompt when:</span></span>

-   <span data-ttu-id="061f1-264">螢幕空間是在不需要使用標籤或指示的高階頁面上，例如工具列上。</span><span class="sxs-lookup"><span data-stu-id="061f1-264">Screen space is at such a premium that using a label or instruction is undesirable, such as on a toolbar.</span></span>
-   <span data-ttu-id="061f1-265">提示的主要目的是要以精簡的方式來識別清單的用途。</span><span class="sxs-lookup"><span data-stu-id="061f1-265">The prompt is primarily for identifying the purpose of the list in a compact way.</span></span> <span data-ttu-id="061f1-266">當使用者使用下拉式方塊時，它不一定是使用者需要看到的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="061f1-266">It must not be crucial information that users need to see while using the combo box.</span></span>

<span data-ttu-id="061f1-267">請不要使用提示來指示使用者從清單中選取某個內容，或按一下按鈕。</span><span class="sxs-lookup"><span data-stu-id="061f1-267">Don't use prompts just to direct users to select something from the list or to click buttons.</span></span> <span data-ttu-id="061f1-268">例如，像是選取選項或輸入檔案名，然後按一下 [傳送] 是不必要的提示。</span><span class="sxs-lookup"><span data-stu-id="061f1-268">For example, prompts like Select an option or Enter a filename and then click Send are unnecessary.</span></span>

<span data-ttu-id="061f1-269">使用提示時：</span><span class="sxs-lookup"><span data-stu-id="061f1-269">When using prompts:</span></span>

-   <span data-ttu-id="061f1-270">以斜體灰色和純文字的一般黑色繪製提示文字。</span><span class="sxs-lookup"><span data-stu-id="061f1-270">Draw the prompt text in italic gray and real text in normal black.</span></span> <span data-ttu-id="061f1-271">提示文字不能與真正的文字混淆。</span><span class="sxs-lookup"><span data-stu-id="061f1-271">The prompt text must not be confused with real text.</span></span>
-   <span data-ttu-id="061f1-272">將提示文字保持簡潔。</span><span class="sxs-lookup"><span data-stu-id="061f1-272">Keep the prompt text concise.</span></span> <span data-ttu-id="061f1-273">您可以使用片段，而不是完整的句子。</span><span class="sxs-lookup"><span data-stu-id="061f1-273">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="061f1-274">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="061f1-274">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="061f1-275">請勿使用結尾標點符號或省略號。</span><span class="sxs-lookup"><span data-stu-id="061f1-275">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="061f1-276">提示文字不能是可編輯的，且應該在使用者按一下或 tab 進入文字方塊後消失。</span><span class="sxs-lookup"><span data-stu-id="061f1-276">The prompt text should not be editable, and should disappear once users click in or tab into the text box.</span></span>
    -   <span data-ttu-id="061f1-277">**例外狀況：** 如果文字方塊具有預設輸入焦點，而且只有在使用者開始鍵入後才會消失，則會顯示提示。</span><span class="sxs-lookup"><span data-stu-id="061f1-277">**Exception:** The prompt is displayed if the text box has default input focus, and only disappears once the user starts typing.</span></span>
-   <span data-ttu-id="061f1-278">如果文字方塊在遺失輸入焦點時仍為空白，則會還原提示文字。</span><span class="sxs-lookup"><span data-stu-id="061f1-278">The prompt text is restored if the text box is still empty when it loses input focus.</span></span>

<span data-ttu-id="061f1-279">**不正確：** ![六個可編輯下拉式清單的螢幕擷取畫面](images/ctrl-drop-image21.png)</span><span class="sxs-lookup"><span data-stu-id="061f1-279">**Incorrect:**![screen shot of six editable drop-down lists ](images/ctrl-drop-image21.png)</span></span>

<span data-ttu-id="061f1-280">在此範例中，螢幕空間不是 premium;填妥可編輯的下拉式清單之後，使用者很難記住其用途;提示文字是可編輯的，並以與實際文字相同的方式繪製。</span><span class="sxs-lookup"><span data-stu-id="061f1-280">In this example, screen space is not at a premium; once an editable drop-down list is filled out, it is difficult for users to remember what it is for; and the prompt text is editable and drawn the same way as real text.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="061f1-281">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="061f1-281">Recommended sizing and spacing</span></span>

![<span data-ttu-id="061f1-282">下拉式清單和規格的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-282">screen shot of drop-down list and specifications</span></span> ](images/ctrl-drop-image22.png)

<span data-ttu-id="061f1-283">下拉式清單和下拉式方塊的建議調整大小和間距。</span><span class="sxs-lookup"><span data-stu-id="061f1-283">Recommended sizing and spacing for drop-down lists and combo boxes.</span></span>

-   <span data-ttu-id="061f1-284">**選擇適合最長有效資料的寬度。**</span><span class="sxs-lookup"><span data-stu-id="061f1-284">**Choose a width appropriate for the longest valid data.**</span></span> <span data-ttu-id="061f1-285">下拉式清單無法水準滾動，因此使用者只能看到控制項中可見的內容。</span><span class="sxs-lookup"><span data-stu-id="061f1-285">Drop-down lists cannot be scrolled horizontally, so users can see only what is visible in the control.</span></span> <span data-ttu-id="061f1-286">但 (請注意，該下拉式方塊可以啟用 AutoScroll 功能。 ) </span><span class="sxs-lookup"><span data-stu-id="061f1-286">(Note, however, that combo boxes can have AutoScroll functionality enabled.)</span></span>
-   <span data-ttu-id="061f1-287">**包含額外的 30%** (高達200% 的文字，以提供任何文字 (較短的文字) ，而不是) 將當地語系化的數位。</span><span class="sxs-lookup"><span data-stu-id="061f1-287">**Include an additional 30 percent** (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span>
-   <span data-ttu-id="061f1-288">**選擇可消除不必要垂直捲動的清單長度。**</span><span class="sxs-lookup"><span data-stu-id="061f1-288">**Choose a list length that eliminates unnecessary vertical scrolling.**</span></span> <span data-ttu-id="061f1-289">因為下拉式清單會隨選顯示，所以其清單最多可顯示30個專案。</span><span class="sxs-lookup"><span data-stu-id="061f1-289">Because drop-down lists are displayed on demand, their lists should show up to 30 items.</span></span> <span data-ttu-id="061f1-290">可編輯的清單方塊 (沒有下拉式按鈕的) 應該會顯示3到12個專案。</span><span class="sxs-lookup"><span data-stu-id="061f1-290">Editable list boxes (those that don't have a drop-down button) should show between 3 and 12 items.</span></span>

## <a name="labels"></a><span data-ttu-id="061f1-291">標籤</span><span class="sxs-lookup"><span data-stu-id="061f1-291">Labels</span></span>

<span data-ttu-id="061f1-292">**控制項標籤**</span><span class="sxs-lookup"><span data-stu-id="061f1-292">**Control labels**</span></span>

-   <span data-ttu-id="061f1-293">將標籤以單字或片語的形式寫入，而不是句子，並以冒號結尾。</span><span class="sxs-lookup"><span data-stu-id="061f1-293">Write the label as a word or phrase, not as a sentence, and end it with a colon.</span></span> <span data-ttu-id="061f1-294">**異常：**</span><span class="sxs-lookup"><span data-stu-id="061f1-294">**Exceptions:**</span></span>
    -   <span data-ttu-id="061f1-295">可編輯的下拉式清單，其中包含空間位於 premium 的提示。</span><span class="sxs-lookup"><span data-stu-id="061f1-295">Editable drop-down lists with prompts located where space is at a premium.</span></span>
    -   <span data-ttu-id="061f1-296">如果下拉式清單或下拉式方塊附屬於選項按鈕或核取方塊，且其標籤以冒號結尾，則請勿在控制項上放置額外的標籤。</span><span class="sxs-lookup"><span data-stu-id="061f1-296">If a drop-down list or combo box is subordinate to a radio button or check box and is introduced by its label ending with a colon, don't put an additional label on the control.</span></span>
-   <span data-ttu-id="061f1-297">為每個標籤指派唯一的 [存取金鑰](glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="061f1-297">Assign a unique [access key](glossary.md) for each label.</span></span> <span data-ttu-id="061f1-298">如需指導方針，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="061f1-298">For guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="061f1-299">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="061f1-299">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="061f1-300">將標籤置於控制項的左邊或上方，然後將標籤與控制項的左邊緣對齊。</span><span class="sxs-lookup"><span data-stu-id="061f1-300">Position the label either to the left of or above the control, and align the label with the left edge of the control.</span></span> <span data-ttu-id="061f1-301">如果標籤位於左邊，請垂直對齊標籤文字與控制項文字。</span><span class="sxs-lookup"><span data-stu-id="061f1-301">If label is on the left, vertically align the label text with the control text.</span></span>

    <span data-ttu-id="061f1-302">**正確：** ![下拉式清單標籤對齊方式的螢幕擷取畫面 ](images/ctrl-drop-image23.png)</span><span class="sxs-lookup"><span data-stu-id="061f1-302">**Correct:** ![screen shot of drop-down list label alignment ](images/ctrl-drop-image23.png)</span></span>

    <span data-ttu-id="061f1-303">在此範例中，標籤會與控制項文字正確對齊。</span><span class="sxs-lookup"><span data-stu-id="061f1-303">In this example, the label is correctly aligned with the control text.</span></span>

    <span data-ttu-id="061f1-304">**不正確：** ![下拉式清單的螢幕擷取畫面未正確對齊 ](images/ctrl-drop-image24.png)</span><span class="sxs-lookup"><span data-stu-id="061f1-304">**Incorrect:** ![screen shot of drop-down list incorrectly aligned ](images/ctrl-drop-image24.png)</span></span>

    <span data-ttu-id="061f1-305">在此範例中，標籤與控制項文字的對齊方式不正確。</span><span class="sxs-lookup"><span data-stu-id="061f1-305">In this example, the label is incorrectly aligned with the control text.</span></span>

-   <span data-ttu-id="061f1-306">您可以在標籤後面的括弧中，指定單位 (秒、連接等) 。</span><span class="sxs-lookup"><span data-stu-id="061f1-306">You may specify units (seconds, connections, and so on) in parentheses after the label.</span></span>
-   <span data-ttu-id="061f1-307">請勿讓下拉式清單或下拉式方塊的內容 (或其單位標籤) 句子的一部分，因為這不是可當地語系化的。</span><span class="sxs-lookup"><span data-stu-id="061f1-307">Don't make the content of the drop-down list or combo box (or its units label) part of a sentence, because this is not localizable.</span></span>

<span data-ttu-id="061f1-308">**選項文字**</span><span class="sxs-lookup"><span data-stu-id="061f1-308">**Option text**</span></span>

-   <span data-ttu-id="061f1-309">將唯一名稱指派給每個選項。</span><span class="sxs-lookup"><span data-stu-id="061f1-309">Assign a unique name to each option.</span></span>
-   <span data-ttu-id="061f1-310">除非專案是適當的名詞，否則請使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="061f1-310">Use [sentence-style capitalization](glossary.md), unless an item is a proper noun.</span></span>
-   <span data-ttu-id="061f1-311">將標籤以單字或片語的形式寫入，而不是以句子形式寫入，而且不使用結尾標點符號。</span><span class="sxs-lookup"><span data-stu-id="061f1-311">Write the label as a word or phrase, not as a sentence, and use no ending punctuation.</span></span>
-   <span data-ttu-id="061f1-312">使用平行片語，並嘗試保留所有選項的相同長度。</span><span class="sxs-lookup"><span data-stu-id="061f1-312">Use parallel phrasing, and try to keep the length about the same for all options.</span></span>

<span data-ttu-id="061f1-313">**教學文字**</span><span class="sxs-lookup"><span data-stu-id="061f1-313">**Instructional text**</span></span>

-   <span data-ttu-id="061f1-314">如果您需要加入下拉式清單或下拉式方塊的解說文字，請將它加入至標籤上方。</span><span class="sxs-lookup"><span data-stu-id="061f1-314">If you need to add instructional text about a drop-down list or combo box, add it above the label.</span></span> <span data-ttu-id="061f1-315">使用結尾標點符號的完整句子。</span><span class="sxs-lookup"><span data-stu-id="061f1-315">Use complete sentences with ending punctuation.</span></span>
-   <span data-ttu-id="061f1-316">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="061f1-316">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="061f1-317">有説明但不需要的其他資訊應該保持簡短。</span><span class="sxs-lookup"><span data-stu-id="061f1-317">Additional information that is helpful but not necessary should be kept short.</span></span> <span data-ttu-id="061f1-318">請將這項資訊放在標籤和冒號之間的括弧中，或是在控制項下方的括弧內。</span><span class="sxs-lookup"><span data-stu-id="061f1-318">Place this information either in parentheses between the label and colon, or without parentheses below the control.</span></span>

    ![<span data-ttu-id="061f1-319">已新增資料之下拉式清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="061f1-319">screen shot of drop-down list with added data</span></span> ](images/ctrl-drop-image25.png)

    <span data-ttu-id="061f1-320">此範例會顯示位於控制項下方的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="061f1-320">This example shows additional information placed below the control.</span></span>

## <a name="documentation"></a><span data-ttu-id="061f1-321">文件</span><span class="sxs-lookup"><span data-stu-id="061f1-321">Documentation</span></span>

<span data-ttu-id="061f1-322">參考下拉式清單時：</span><span class="sxs-lookup"><span data-stu-id="061f1-322">When referring to drop-down lists:</span></span>

-   <span data-ttu-id="061f1-323">使用確切的標籤文字，包括其大小寫，但不包含存取金鑰底線或冒號;包含其中一個清單或方塊，以較清楚的方式進行。</span><span class="sxs-lookup"><span data-stu-id="061f1-323">Use the exact label text, including its capitalization, but don't include the access key underscore or colon; include either list or box, whichever is clearer.</span></span>
-   <span data-ttu-id="061f1-324">針對清單選項，請使用確切的選項文字，包括其大小寫。</span><span class="sxs-lookup"><span data-stu-id="061f1-324">For list options, use the exact option text, including its capitalization.</span></span>
-   <span data-ttu-id="061f1-325">在程式設計和其他技術檔中，請將下拉式清單視為下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="061f1-325">In programming and other technical documentation, refer to drop-down lists as drop-down lists.</span></span> <span data-ttu-id="061f1-326">在其他地方，使用 [清單] 或 [box]，以較清楚的方式。</span><span class="sxs-lookup"><span data-stu-id="061f1-326">Everywhere else, use either list or box, whichever is clearer.</span></span>
-   <span data-ttu-id="061f1-327">若要描述使用者互動，請使用按一下。</span><span class="sxs-lookup"><span data-stu-id="061f1-327">To describe user interaction, use click.</span></span>
-   <span data-ttu-id="061f1-328">可能的話，請使用粗體文字來格式化標籤和清單選項。</span><span class="sxs-lookup"><span data-stu-id="061f1-328">When possible, format the label and list options using bold text.</span></span> <span data-ttu-id="061f1-329">否則，請只在必要時才將標籤和選項放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="061f1-329">Otherwise, put the label and options in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="061f1-330">範例：在 [ **大小** ] 清單中，按一下 [ **大型** 字型]。</span><span class="sxs-lookup"><span data-stu-id="061f1-330">Example: In the **Font size** list, click **Large fonts**.</span></span>

<span data-ttu-id="061f1-331">參考下拉式方塊時：</span><span class="sxs-lookup"><span data-stu-id="061f1-331">When referring to combo boxes:</span></span>

-   <span data-ttu-id="061f1-332">使用確切的標籤文字，包括其大小寫，但不包含存取金鑰底線或冒號;包含 [單字] 方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-332">Use the exact label text, including its capitalization, but don't include the access key underscore or colon; include the word box.</span></span>
-   <span data-ttu-id="061f1-333">針對清單選項，請使用確切的選項文字，包括其大小寫。</span><span class="sxs-lookup"><span data-stu-id="061f1-333">For list options, use the exact option text including its capitalization.</span></span>
-   <span data-ttu-id="061f1-334">在程式設計和其他技術檔中，請將下拉式方塊稱為下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="061f1-334">In programming and other technical documentation, refer to combo boxes as combo boxes.</span></span> <span data-ttu-id="061f1-335">在其他地方使用 box。</span><span class="sxs-lookup"><span data-stu-id="061f1-335">Everywhere else, use box.</span></span>
-   <span data-ttu-id="061f1-336">若要描述使用者互動，請使用 enter。</span><span class="sxs-lookup"><span data-stu-id="061f1-336">To describe user interaction, use enter.</span></span>
-   <span data-ttu-id="061f1-337">可能的話，請使用粗體文字來格式化標籤和清單選項。</span><span class="sxs-lookup"><span data-stu-id="061f1-337">When possible, format the label and list options using bold text.</span></span> <span data-ttu-id="061f1-338">否則，請只在必要時才將標籤和選項放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="061f1-338">Otherwise, put the label and options in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="061f1-339">範例：在 [ **字型** ] 方塊中，輸入您要使用的字型。</span><span class="sxs-lookup"><span data-stu-id="061f1-339">Example: In the **Font** box, enter the font you want to use.</span></span>

 

