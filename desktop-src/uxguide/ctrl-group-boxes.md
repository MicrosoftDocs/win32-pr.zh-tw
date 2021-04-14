---
title: 群組方塊
description: 群組方塊是圍繞一組相關控制項的標記矩形框架。 群組方塊是以視覺化方式顯示關聯性的方式;除了可能提供一組控制項的存取金鑰外，它還不提供任何功能。
ms.assetid: 5b5ffb36-3ed1-44cd-af87-5cddf46c56a6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 67f930383f2d4412d30027971c6cab2bd3edcccd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104564819"
---
# <a name="group-boxes"></a><span data-ttu-id="3574e-104">群組方塊</span><span class="sxs-lookup"><span data-stu-id="3574e-104">Group Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="3574e-105">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="3574e-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="3574e-106">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="3574e-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="3574e-107">群組方塊是圍繞一組相關控制項的標記矩形框架。</span><span class="sxs-lookup"><span data-stu-id="3574e-107">A group box is a labeled rectangular frame that surrounds a set of related controls.</span></span> <span data-ttu-id="3574e-108">群組方塊是以視覺化方式顯示關聯性的方式;除了可能提供一組控制項的存取金鑰外，它還不提供任何功能。</span><span class="sxs-lookup"><span data-stu-id="3574e-108">A group box is a way to show relationships visually; aside from possibly providing an access key for a group of controls, it provides no functionality.</span></span>

![<span data-ttu-id="3574e-109">包含核取方塊之群組方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="3574e-109">screen shot of group box containing check boxes</span></span> ](images/ctrl-group-boxes-image1.png)

<span data-ttu-id="3574e-110">典型的群組方塊。</span><span class="sxs-lookup"><span data-stu-id="3574e-110">A typical group box.</span></span>

> [!Note]  
> <span data-ttu-id="3574e-111">與 [版面](vis-layout.md) 配置相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="3574e-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="3574e-112">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="3574e-112">Is this the right control?</span></span>

<span data-ttu-id="3574e-113">雖然群組方塊是表示關聯性的強大視覺方式，過度使用它們會新增視覺效果，並大幅減少介面上的可用空間。</span><span class="sxs-lookup"><span data-stu-id="3574e-113">While group boxes are a strong visual means of indicating relationships, overusing them adds visual clutter and greatly reduces the space available on a surface.</span></span> <span data-ttu-id="3574e-114">它們在視覺上很繁重，而且應該謹慎使用，只有在沒有更好的解決方案時才需要使用。</span><span class="sxs-lookup"><span data-stu-id="3574e-114">They are visually heavy and should be used sparingly—only when there isn't a better solution.</span></span>

<span data-ttu-id="3574e-115">Windows 的設計趨勢是消除不必要的程式碼，以簡化更清楚的外觀。</span><span class="sxs-lookup"><span data-stu-id="3574e-115">A design trend in Windows is a simpler, cleaner appearance by eliminating unnecessary lines.</span></span>

<span data-ttu-id="3574e-116">若要決定是否需要群組方塊，請考慮下列問題：</span><span class="sxs-lookup"><span data-stu-id="3574e-116">To decide whether a group box is necessary, consider these questions:</span></span>

-   <span data-ttu-id="3574e-117">**群組中是否有一個以上的控制項？**</span><span class="sxs-lookup"><span data-stu-id="3574e-117">**Is there more than one control in the group?**</span></span> <span data-ttu-id="3574e-118">如果沒有，請改用純文字標籤。</span><span class="sxs-lookup"><span data-stu-id="3574e-118">If not, use a plain text label instead.</span></span> <span data-ttu-id="3574e-119">常見的例外狀況是使用具有單一控制項的群組方塊，以維持與相同介面上其他群組方塊的一致性。</span><span class="sxs-lookup"><span data-stu-id="3574e-119">A rare exception is to use a group box with a single control to maintain consistency with other group boxes on the same surface.</span></span>

<span data-ttu-id="3574e-120">**不正確：** ![包含一個文字方塊的群組方塊螢幕擷取畫面 ](images/ctrl-group-boxes-image2.png)</span><span class="sxs-lookup"><span data-stu-id="3574e-120">**Incorrect:** ![screen shot of group box containing one text box ](images/ctrl-group-boxes-image2.png)</span></span>

<span data-ttu-id="3574e-121">在此範例中，[群組] 方塊只有一個控制項。</span><span class="sxs-lookup"><span data-stu-id="3574e-121">In this example, the group box has only a single control.</span></span>

-   <span data-ttu-id="3574e-122">**控制項是否相關？是否顯示關聯性增加了清晰度？**</span><span class="sxs-lookup"><span data-stu-id="3574e-122">**Are the controls related? Does showing the relationship add clarity?**</span></span> <span data-ttu-id="3574e-123">如果不是，則會在群組方塊以外的地方分別呈現控制項。</span><span class="sxs-lookup"><span data-stu-id="3574e-123">If not, present the controls separately outside of a group box.</span></span>
-   <span data-ttu-id="3574e-124">**群組內的所有控制項都是嗎？**</span><span class="sxs-lookup"><span data-stu-id="3574e-124">**Are all the controls inside the group?**</span></span> <span data-ttu-id="3574e-125">如果是的話，請在較大的介面上指出關聯性，例如父對話方塊或頁面。</span><span class="sxs-lookup"><span data-stu-id="3574e-125">If so, indicate the relationship on the larger surface, such as the parent dialog box or page.</span></span>

<span data-ttu-id="3574e-126">**不正確：** ![包含所有控制項之群組方塊的螢幕擷取畫面 ](images/ctrl-group-boxes-image3.png)</span><span class="sxs-lookup"><span data-stu-id="3574e-126">**Incorrect:** ![screen shot of group box containing all controls ](images/ctrl-group-boxes-image3.png)</span></span>

<span data-ttu-id="3574e-127">在此範例中，所有控制項 (在對話方塊的 [認可] 按鈕) 中。</span><span class="sxs-lookup"><span data-stu-id="3574e-127">In this example, all the controls (aside from the commit buttons) in the dialog box are within the group box.</span></span>

-   <span data-ttu-id="3574e-128">**您可以使用單獨的版面配置來有效地傳達關聯性嗎？**</span><span class="sxs-lookup"><span data-stu-id="3574e-128">**Can you effectively communicate the relationships using layout alone?**</span></span> <span data-ttu-id="3574e-129">若是如此，請改用 [layout](vis-layout.md) 。</span><span class="sxs-lookup"><span data-stu-id="3574e-129">If so, use [layout](vis-layout.md) instead.</span></span> <span data-ttu-id="3574e-130">您可以將相關的控制項彼此相鄰，並在不相關的控制項之間放置額外的間距。</span><span class="sxs-lookup"><span data-stu-id="3574e-130">You can place related controls next to each other and put extra spacing between unrelated controls.</span></span> <span data-ttu-id="3574e-131">您也可以使用標題和縮排來顯示階層式關聯性。</span><span class="sxs-lookup"><span data-stu-id="3574e-131">You can also use headings and indenting to show hierarchical relationships.</span></span>

![<span data-ttu-id="3574e-132">四個圖示的圖，其中顯示四個工作群組</span><span class="sxs-lookup"><span data-stu-id="3574e-132">figure of four icons showing four groups of tasks</span></span> ](images/ctrl-group-boxes-image4.png)

<span data-ttu-id="3574e-133">在此範例中，只會使用版面配置來顯示控制項關聯性。</span><span class="sxs-lookup"><span data-stu-id="3574e-133">In this example, layout alone is used to show control relationships.</span></span>

-   <span data-ttu-id="3574e-134">**您可以使用分隔符號有效地傳達關聯性嗎？**</span><span class="sxs-lookup"><span data-stu-id="3574e-134">**Can you effectively communicate the relationships using a separator?**</span></span> <span data-ttu-id="3574e-135">如果是的話，請改用分隔符號。</span><span class="sxs-lookup"><span data-stu-id="3574e-135">If so, use a separator instead.</span></span> <span data-ttu-id="3574e-136">分隔符號是一條可將其下的控制項統一的水平線。</span><span class="sxs-lookup"><span data-stu-id="3574e-136">A separator is a horizontal line that unifies the controls below it.</span></span> <span data-ttu-id="3574e-137">分隔符號提供更簡單、更清楚的外觀。</span><span class="sxs-lookup"><span data-stu-id="3574e-137">Separators provide a simpler, cleaner look.</span></span> <span data-ttu-id="3574e-138">但是，與群組方塊不同的是，當它們跨越表面的全形時，效果最好。</span><span class="sxs-lookup"><span data-stu-id="3574e-138">However, unlike group boxes, they work best when they span the full width of the surface.</span></span>
    -   <span data-ttu-id="3574e-139">**開發人員：** 您可以使用具有蝕刻矩形且高度為一的分隔符號來執行分隔符號。</span><span class="sxs-lookup"><span data-stu-id="3574e-139">**Developers:** You can implement a separator with an etched rectangle with a height of one.</span></span>

![顯示以蝕刻矩形分隔符號分隔之電子郵件控制項的螢幕擷取畫面。](images/ctrl-group-boxes-image5.png)

<span data-ttu-id="3574e-141">在此範例中，標示的分隔符號會用來顯示控制項關聯性。</span><span class="sxs-lookup"><span data-stu-id="3574e-141">In this example, labeled separators are used to show control relationships.</span></span>

![<span data-ttu-id="3574e-142">以分隔符號分隔之控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="3574e-142">screen shot of controls set apart by separators</span></span> ](images/ctrl-group-boxes-image6.png)

<span data-ttu-id="3574e-143">在此範例中，未標記的分隔符號會用來顯示控制項關聯性。</span><span class="sxs-lookup"><span data-stu-id="3574e-143">In this example, unlabeled separators are used to show control relationships.</span></span>

-   <span data-ttu-id="3574e-144">**您是否可以有效地傳達沒有文字的關聯性？**</span><span class="sxs-lookup"><span data-stu-id="3574e-144">**Can you effectively communicate the relationships without text?**</span></span> <span data-ttu-id="3574e-145">如果是的話，請考慮使用圖形元素，例如 [背景](vis-graphic.md) 或匯總工具。</span><span class="sxs-lookup"><span data-stu-id="3574e-145">If so, consider using graphic elements such as [backgrounds](vis-graphic.md) or aggregators.</span></span>

## <a name="guidelines"></a><span data-ttu-id="3574e-146">指導方針</span><span class="sxs-lookup"><span data-stu-id="3574e-146">Guidelines</span></span>

-   <span data-ttu-id="3574e-147">**不要嵌套群組方塊。**</span><span class="sxs-lookup"><span data-stu-id="3574e-147">**Don't nest group boxes.**</span></span> <span data-ttu-id="3574e-148">使用版面配置來顯示群組方塊內的關聯性。</span><span class="sxs-lookup"><span data-stu-id="3574e-148">Use layout to show relationships within a group box.</span></span>

<span data-ttu-id="3574e-149">**不正確：** ![群組方塊內群組方塊的螢幕擷取畫面 ](images/ctrl-group-boxes-image7.png)</span><span class="sxs-lookup"><span data-stu-id="3574e-149">**Incorrect:** ![screen shot of a group box within a group box ](images/ctrl-group-boxes-image7.png)</span></span>

<span data-ttu-id="3574e-150">在此範例中，嵌套群組方塊會產生不必要的視覺雜亂。</span><span class="sxs-lookup"><span data-stu-id="3574e-150">In this example, the nested group boxes result in unnecessary visual clutter.</span></span>

<span data-ttu-id="3574e-151">**正確：** ![一個群組方塊中相同控制項的螢幕擷取畫面 ](images/ctrl-group-boxes-image8.png)</span><span class="sxs-lookup"><span data-stu-id="3574e-151">**Correct:** ![screen shot of same controls within one group box ](images/ctrl-group-boxes-image8.png)</span></span>

<span data-ttu-id="3574e-152">在此範例中，會改為使用版面配置來顯示相同的控制項關聯性。</span><span class="sxs-lookup"><span data-stu-id="3574e-152">In this example, the same control relationship is shown using layout instead.</span></span>

-   <span data-ttu-id="3574e-153">不要將控制項放在群組方塊標籤中。</span><span class="sxs-lookup"><span data-stu-id="3574e-153">Don't put controls in group box labels.</span></span>
    -   <span data-ttu-id="3574e-154">**例外狀況：** 如果方塊內的所有控制項都已由核取方塊啟用和停用，您可以使用核取方塊作為群組框標籤。</span><span class="sxs-lookup"><span data-stu-id="3574e-154">**Exception:** You can use a check box as a group box label if all of the controls inside the box are enabled and disabled by the check box.</span></span>

<span data-ttu-id="3574e-155">**不正確：** ![群組方塊標籤上下拉式清單的螢幕擷取畫面 ](images/ctrl-group-boxes-image9.png)</span><span class="sxs-lookup"><span data-stu-id="3574e-155">**Incorrect:** ![screen shot of drop-down list on a group-box label ](images/ctrl-group-boxes-image9.png)</span></span>

<span data-ttu-id="3574e-156">在此範例中，下拉式清單不正確地放在群組方塊上。</span><span class="sxs-lookup"><span data-stu-id="3574e-156">In this example, a drop-down list is incorrectly placed on a group box.</span></span> <span data-ttu-id="3574e-157">此範例應改為使用 [tab 鍵](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="3574e-157">This example should use [tabs](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) instead.</span></span>

-   <span data-ttu-id="3574e-158">**不要停用群組方塊。**</span><span class="sxs-lookup"><span data-stu-id="3574e-158">**Don't disable group boxes.**</span></span> <span data-ttu-id="3574e-159">若要指出目前未套用控制項群組，請停用 [群組] 方塊內的所有控制項，而不是 [群組] 方塊本身。</span><span class="sxs-lookup"><span data-stu-id="3574e-159">To indicate that a group of controls doesn't currently apply, disable all the controls within the group box, but not the group box itself.</span></span> <span data-ttu-id="3574e-160">這種方法更容易存取，而且所有 UI 架構都可以一致地支援。</span><span class="sxs-lookup"><span data-stu-id="3574e-160">This approach is more accessible and can be supported consistently by all UI frameworks.</span></span>

## <a name="labels"></a><span data-ttu-id="3574e-161">標籤</span><span class="sxs-lookup"><span data-stu-id="3574e-161">Labels</span></span>

-   <span data-ttu-id="3574e-162">標示所有群組方塊。</span><span class="sxs-lookup"><span data-stu-id="3574e-162">Label all group boxes.</span></span>
-   <span data-ttu-id="3574e-163">請勿指派標籤的存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="3574e-163">Don't assign an access key to the label.</span></span> <span data-ttu-id="3574e-164">這是不必要的，而且會讓其他存取金鑰更難指派。</span><span class="sxs-lookup"><span data-stu-id="3574e-164">Doing so is unnecessary and makes the other access keys harder to assign.</span></span> <span data-ttu-id="3574e-165">相反地，請將便捷鍵指派給 [群組] 方塊內的控制項。</span><span class="sxs-lookup"><span data-stu-id="3574e-165">Instead, assign access keys to the controls within the group box.</span></span>
    -   <span data-ttu-id="3574e-166">**例外狀況：** 如果表面有許多控制項，則可能沒有足夠的可用存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="3574e-166">**Exception:** If a surface has many controls, there may not be enough access keys available.</span></span> <span data-ttu-id="3574e-167">若是如此，請將存取金鑰指派給群組方塊，而不是群組方塊內的控制項，藉以減少存取金鑰的數目。</span><span class="sxs-lookup"><span data-stu-id="3574e-167">If so, reduce the number of access keys by assigning them to group boxes instead of the controls within the group boxes.</span></span>
-   <span data-ttu-id="3574e-168">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="3574e-168">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="3574e-169">使用名詞或名詞片語（而不是句子）來撰寫標籤，並且不使用結尾標點符號，包括冒號。</span><span class="sxs-lookup"><span data-stu-id="3574e-169">Write the label using a noun or a noun phrase, not as a sentence, and use no ending punctuation, including colons.</span></span>
-   <span data-ttu-id="3574e-170">針對相同介面中的群組方塊標籤使用平行片語。</span><span class="sxs-lookup"><span data-stu-id="3574e-170">Use parallel phrasing for group box labels within the same surface.</span></span>
-   <span data-ttu-id="3574e-171">將群組箱標籤保持簡潔。</span><span class="sxs-lookup"><span data-stu-id="3574e-171">Keep group box labels concise.</span></span> <span data-ttu-id="3574e-172">請勿使用解說文字作為標籤。</span><span class="sxs-lookup"><span data-stu-id="3574e-172">Don't use instructional text as the label.</span></span> <span data-ttu-id="3574e-173">不過，您可以在 [群組] 方塊中有解說文字。</span><span class="sxs-lookup"><span data-stu-id="3574e-173">You can have instructional text within the group box, however.</span></span>
-   <span data-ttu-id="3574e-174">請勿在方塊內的控制項標籤中重複群組框標籤。</span><span class="sxs-lookup"><span data-stu-id="3574e-174">Don't repeat the group box label in control labels within the box.</span></span> <span data-ttu-id="3574e-175">例如，如果群組方塊的標籤為 [對齊]，請將選項按鈕靠左、靠右或靠右對齊來標記。</span><span class="sxs-lookup"><span data-stu-id="3574e-175">For example, if the group box is labeled Alignment, label the option buttons Left, Right, and so on, not Left alignment or Right alignment.</span></span>
-   <span data-ttu-id="3574e-176">請勿在使用者介面文字中參考群組方塊。</span><span class="sxs-lookup"><span data-stu-id="3574e-176">Don't refer to group boxes in user interface text.</span></span>

## <a name="documentation"></a><span data-ttu-id="3574e-177">文件</span><span class="sxs-lookup"><span data-stu-id="3574e-177">Documentation</span></span>

<span data-ttu-id="3574e-178">參考群組方塊時：</span><span class="sxs-lookup"><span data-stu-id="3574e-178">When referring to group boxes:</span></span>

-   <span data-ttu-id="3574e-179">請僅在程式設計人員和其他技術檔中參考群組方塊。</span><span class="sxs-lookup"><span data-stu-id="3574e-179">Refer to group boxes only in programmer and other technical documentation.</span></span> <span data-ttu-id="3574e-180">針對 [群組] 方塊，請使用兩個小寫字。</span><span class="sxs-lookup"><span data-stu-id="3574e-180">For group box, use two lowercase words.</span></span>
-   <span data-ttu-id="3574e-181">在其他地方，除非對話方塊中包含一個以上具有相同名稱的選項，否則不需要在程式中包含群組方塊的名稱。</span><span class="sxs-lookup"><span data-stu-id="3574e-181">Everywhere else, it is unnecessary to include the name of the group box in a procedure unless a dialog box contains more than one option with the same name.</span></span> <span data-ttu-id="3574e-182">在這種情況下，請使用與群組箱名稱搭配的。</span><span class="sxs-lookup"><span data-stu-id="3574e-182">In such cases, use under with the group box name.</span></span>
-   <span data-ttu-id="3574e-183">可能的話，請使用粗體文字來格式化標籤。</span><span class="sxs-lookup"><span data-stu-id="3574e-183">When possible, format the label using bold text.</span></span> <span data-ttu-id="3574e-184">否則，請只在必要時才將標籤放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="3574e-184">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="3574e-185">範例：在 [ **效果**] 底下，選取 [ **隱藏**]。</span><span class="sxs-lookup"><span data-stu-id="3574e-185">Example: Under **Effects**, select **Hidden**.</span></span>

 

 