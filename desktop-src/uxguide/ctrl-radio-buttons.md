---
title: 選項按鈕
description: 使用選項按鈕時，使用者可以在一組互斥、相關的選項之間做選擇。
ms.assetid: f9af0a8a-d4a1-464c-a967-bab88ae0726b
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 00495695753506702015431c889e74d5a7effe9a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195690"
---
# <a name="radio-buttons"></a><span data-ttu-id="b1cc9-103">選項按鈕</span><span class="sxs-lookup"><span data-stu-id="b1cc9-103">Radio Buttons</span></span>

> [!NOTE]
> <span data-ttu-id="b1cc9-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="b1cc9-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="b1cc9-106">使用選項按鈕時，使用者可以在一組互斥、相關的選項之間做選擇。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-106">With a radio button, users make a choice among a set of mutually exclusive, related options.</span></span> <span data-ttu-id="b1cc9-107">使用者只能選擇一個選項。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-107">Users can choose one and only one option.</span></span> <span data-ttu-id="b1cc9-108">因為選項按鈕的運作方式就像是無線電上的通道預設，所以會呼叫它們。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-108">Radio buttons are so called because they function like the channel presets on radios.</span></span>

![<span data-ttu-id="b1cc9-109">三個選項按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-109">screen shot of three radio buttons</span></span> ](images/radio-buttons-image1.png)

<span data-ttu-id="b1cc9-110">選項按鈕的一般群組。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-110">A typical group of radio buttons.</span></span>

<span data-ttu-id="b1cc9-111">一組選項按鈕的行為就像單一控制項一樣。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-111">A group of radio buttons behaves like a single control.</span></span> <span data-ttu-id="b1cc9-112">使用 Tab 鍵只能存取選取的選項，但是使用者可以使用方向鍵來迴圈流覽群組。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-112">Only the selected choice is accessible using the Tab key, but users can cycle through the group using the arrow keys.</span></span>

> [!Note]  
> <span data-ttu-id="b1cc9-113">與 [版面](vis-layout.md) 配置和 [鍵盤導覽](inter-keyboard.md) 相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-113">Guidelines related to [layout](vis-layout.md) and [keyboard navigation](inter-keyboard.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="b1cc9-114">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="b1cc9-114">Is this the right control?</span></span>

<span data-ttu-id="b1cc9-115">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="b1cc9-115">To decide, consider these questions:</span></span>

-   <span data-ttu-id="b1cc9-116">**控制項是否可用來從一組互斥的選項中選擇一個選項？**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-116">**Is the control used to choose one option from a set of mutually exclusive choices?**</span></span> <span data-ttu-id="b1cc9-117">如果不是，請使用其他控制項。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-117">If not, use another control.</span></span> <span data-ttu-id="b1cc9-118">若要選擇多個選項，請改用 [核取方塊](ctrl-check-boxes.md)、 [多重選取清單](ctrl-list-boxes.md) 或核取方塊清單。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-118">To choose multiple options, use [check boxes](ctrl-check-boxes.md), a [multiple-selection list](ctrl-list-boxes.md) or a check box list instead.</span></span>
-   <span data-ttu-id="b1cc9-119">**選項的數目是介於2到7之間？**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-119">**Is the number of options between two and seven?**</span></span> <span data-ttu-id="b1cc9-120">由於所使用的螢幕空間與選項數目成正比，因此請將群組中的選項數目維持在二到七的群組中。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-120">Since the screen space used is proportional to the number of options, keep the number of options in a group between two and seven.</span></span> <span data-ttu-id="b1cc9-121">若有八個以上的選項，請使用 [下拉式清單](/windows/desktop/uxguide/ctrl-drop) 或 [單一選取清單](ctrl-list-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-121">For eight or more options, use a [drop-down list](/windows/desktop/uxguide/ctrl-drop) or [single-selection list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="b1cc9-122">**核取方塊是較佳的選擇嗎？**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-122">**Would a check box be a better choice?**</span></span> <span data-ttu-id="b1cc9-123">如果只有兩個選項，您可以改為使用單一 [核取方塊](ctrl-check-boxes.md) 。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-123">If there are only two options, you could use a single [check box](ctrl-check-boxes.md) instead.</span></span> <span data-ttu-id="b1cc9-124">不過，核取方塊僅適用于開啟或關閉單一選項，而選項按鈕可用於完全不同的替代方案。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-124">However, check boxes are suitable only for turning a single option on or off, whereas radio buttons can be used for completely different alternatives.</span></span> <span data-ttu-id="b1cc9-125">如果這兩種解決方案都可行：</span><span class="sxs-lookup"><span data-stu-id="b1cc9-125">If both solutions are possible:</span></span>
    -   <span data-ttu-id="b1cc9-126">如果已清除核取方塊的意義不完全明顯，請使用選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-126">Use radio buttons if the meaning of the cleared check box isn't completely obvious.</span></span>

        <span data-ttu-id="b1cc9-127">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-127">**Incorrect:**</span></span>

        ![<span data-ttu-id="b1cc9-128">[橫向] 核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-128">screen shot of landscape check box</span></span> ](images/radio-buttons-image2.png)

        <span data-ttu-id="b1cc9-129">**正確：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-129">**Correct:**</span></span>

        ![<span data-ttu-id="b1cc9-130">橫向/縱向選項按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-130">screen shot of landscape/portrait radio buttons</span></span> ](images/radio-buttons-image3.png)

        <span data-ttu-id="b1cc9-131">在正確的範例中，不會相反選項，因此選項按鈕是較佳的選擇。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-131">In the correct example, the choices are not opposites so radio buttons are the better choice.</span></span>

    -   <span data-ttu-id="b1cc9-132">在 [wizard] 頁面上使用選項按鈕，讓替代方案更清楚，即使核取方塊是可接受的。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-132">Use radio buttons on wizard pages to make the alternatives clear, even if a check box is otherwise acceptable.</span></span>
    -   <span data-ttu-id="b1cc9-133">如果您有足夠的螢幕空間，而且選項很重要，足以充分利用該螢幕空間，請使用選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-133">Use radio buttons if you have enough screen space and the options are important enough to be a good use of that screen space.</span></span> <span data-ttu-id="b1cc9-134">否則，請使用核取方塊或下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-134">Otherwise, use a check box or drop-down list.</span></span>

        <span data-ttu-id="b1cc9-135">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-135">**Incorrect:**</span></span>

        ![<span data-ttu-id="b1cc9-136">顯示/不顯示選項按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-136">screen shot of show/don't show radio buttons</span></span> ](images/radio-buttons-image4.png)

        <span data-ttu-id="b1cc9-137">在此範例中，選項的重要性不足以使用選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-137">In this example, the options aren't important enough to use radio buttons.</span></span>

        <span data-ttu-id="b1cc9-138">**正確：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-138">**Correct:**</span></span>

        ![<span data-ttu-id="b1cc9-139">[不要顯示此訊息] 核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-139">screen shot of don't show this message check box</span></span> ](images/radio-buttons-image5.png)

        <span data-ttu-id="b1cc9-140">在此範例中，核取方塊是此周邊選項的螢幕空間有效率的使用方式。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-140">In this example, a check box is an efficient use of screen space for this peripheral option.</span></span>

    -   <span data-ttu-id="b1cc9-141">如果頁面上有其他核取方塊，請使用核取方塊。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-141">Use a check box if there other check boxes on the page.</span></span>

-   <span data-ttu-id="b1cc9-142">**下拉式清單是較佳的選擇嗎？**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-142">**Would a drop-down list be a better choice?**</span></span> <span data-ttu-id="b1cc9-143">如果大部分的使用者建議使用預設選項，在大部分情況下，選項按鈕可能會比所需更多的選項。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-143">If the default option is recommended for most users in most situations, radio buttons might draw more attention to the options than necessary.</span></span>
    -   <span data-ttu-id="b1cc9-144">如果您不想要特別注意選項，或不想要鼓勵使用者進行變更，請考慮使用下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-144">Consider using a drop-down list if you don't want to draw attention to the options, or you don't want to encourage users to make changes.</span></span> <span data-ttu-id="b1cc9-145">下拉式清單會將焦點放在目前的選取範圍，而選項按鈕則會平均強調所有選項。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-145">A drop-down list focuses on the current selection, whereas radio buttons emphasize all options equally.</span></span>

        ![<span data-ttu-id="b1cc9-146">最高品質作為預設按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-146">screen shot of highest quality as default button</span></span> ](images/radio-buttons-image6.png)

        <span data-ttu-id="b1cc9-147">在此範例中，下拉式清單將焦點放在目前的選取範圍，並防止使用者進行變更。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-147">In this example, a drop-down list focuses on the current selection and discourages users from making changes.</span></span>

    -   <span data-ttu-id="b1cc9-148">如果頁面上有其他下拉式清單，請考慮使用下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-148">Consider a drop-down list if there are other drop-down lists on the page.</span></span>

-   <span data-ttu-id="b1cc9-149">**一組命令按鈕、命令連結或分割按鈕是否是較佳的選擇？**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-149">**Would a set of command buttons, command links, or a split button be a better choice?**</span></span> <span data-ttu-id="b1cc9-150">如果只使用選項按鈕來影響命令的執行方式，則改為顯示命令變化通常會比較好。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-150">If the radio buttons are used only to affect how a command is performed, it is often better to present the command variations instead.</span></span> <span data-ttu-id="b1cc9-151">這麼做可讓使用者選擇具有單一互動的正確命令。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-151">Doing so allows users to choose the right command with a single interaction.</span></span>
-   <span data-ttu-id="b1cc9-152">**選項是否存在方案選項，而不是資料？**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-152">**Do the options present program options, rather than data?**</span></span> <span data-ttu-id="b1cc9-153">選項的值不應以內容或其他資料為基礎。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-153">The options' values shouldn't be based on context or other data.</span></span> <span data-ttu-id="b1cc9-154">針對資料，請使用下拉式清單或單一選取清單。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-154">For data, use a drop-down list or single-selection list.</span></span>
-   <span data-ttu-id="b1cc9-155">如果您在嚮導頁面或控制台上使用控制項，則 **控制項是否會回應主要指令，而使用者是否可以在稍後變更選擇？**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-155">If the control is used on a wizard page or control panel, **is the control a response to the main instruction and can users later change the choice?**</span></span> <span data-ttu-id="b1cc9-156">如果是的話，請考慮使用命令連結，而不是使用選項按鈕，讓互動更有效率。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-156">If so, consider using command links instead of radio buttons to make the interaction more efficient.</span></span>
-   <span data-ttu-id="b1cc9-157">**這些值是否為非數值？**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-157">**Are the values non-numeric?**</span></span> <span data-ttu-id="b1cc9-158">若為數值資料，請使用 [文字方塊](ctrl-text-boxes.md)、 [下拉式清單](/windows/desktop/uxguide/ctrl-drop)或 [滑杆](ctrl-sliders.md)。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-158">For numeric data, use [text boxes](ctrl-text-boxes.md), [drop-down lists](/windows/desktop/uxguide/ctrl-drop), or [sliders](ctrl-sliders.md).</span></span>

## <a name="guidelines"></a><span data-ttu-id="b1cc9-159">指導方針</span><span class="sxs-lookup"><span data-stu-id="b1cc9-159">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="b1cc9-160">一般</span><span class="sxs-lookup"><span data-stu-id="b1cc9-160">General</span></span>

-   <span data-ttu-id="b1cc9-161">**以邏輯順序列出選項，** 例如最可能選取到最少、最簡單的作業（最複雜）或最小的風險。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-161">**List the options in a logical order,** such as most likely to be selected to least, simplest operation to most complex, or least risk to most.</span></span> <span data-ttu-id="b1cc9-162">不建議依字母順序排序，因為它是語言相依，因此不可當地語系化。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-162">Alphabetical ordering is not recommended because it is language dependent and therefore not localizable.</span></span>
-   <span data-ttu-id="b1cc9-163">**如果沒有任何選項是有效的選項，請新增另一個選項來反映此選項，** 例如 [無] 或 [不適用]。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-163">**If none of the options is a valid choice, add another option to reflect this choice,** such as None or Does not apply.</span></span>
-   <span data-ttu-id="b1cc9-164">**偏好垂直對齊選項按鈕，而非水準對齊。**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-164">**Prefer to align radio buttons vertically instead of horizontally.**</span></span> <span data-ttu-id="b1cc9-165">水準對齊較難讀取和當地語系化。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-165">Horizontal alignment is harder to read and localize.</span></span>

    <span data-ttu-id="b1cc9-166">**正確：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-166">**Correct:**</span></span>

    ![<span data-ttu-id="b1cc9-167">垂直選項按鈕對齊方式的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-167">screen shot of vertical radio-button alignment</span></span> ](images/radio-buttons-image7.png)

    <span data-ttu-id="b1cc9-168">在此範例中，選項按鈕會垂直對齊。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-168">In this example, the radio buttons are aligned vertically.</span></span>

    <span data-ttu-id="b1cc9-169">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-169">**Incorrect:**</span></span>

    ![<span data-ttu-id="b1cc9-170">水準選項按鈕對齊方式的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-170">screen shot of horizontal radio-button alignment</span></span> ](images/radio-buttons-image8.png)

    <span data-ttu-id="b1cc9-171">在此範例中，水準對齊較難閱讀。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-171">In this example, the horizontal alignment is harder to read.</span></span>

-   <span data-ttu-id="b1cc9-172">重新 **考慮使用群組方塊來組織選項按鈕群組**，這通常會造成不必要的螢幕混亂。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-172">**Reconsider using group boxes to organize groups of radio buttons**—this often results in unnecessary screen clutter.</span></span>
-   <span data-ttu-id="b1cc9-173">**請勿使用選項按鈕標籤作為群組箱標籤。**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-173">**Don't use radio button labels as group box labels.**</span></span>
-   <span data-ttu-id="b1cc9-174">**請勿使用選項按鈕的選項來：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-174">**Don't use the selection of a radio button to:**</span></span>
    -   <span data-ttu-id="b1cc9-175">執行命令。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-175">Perform commands.</span></span>
    -   <span data-ttu-id="b1cc9-176">顯示其他視窗，例如用來收集更多輸入的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-176">Display other windows, such as a dialog box to gather more input.</span></span>
    -   <span data-ttu-id="b1cc9-177">以動態方式顯示或隱藏與選取之控制項相關的其他控制項 (畫面讀取器無法偵測到這類事件) 。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-177">Dynamically show or hide other controls related to the selected control (screen readers cannot detect such events).</span></span> <span data-ttu-id="b1cc9-178">不過，您可以根據選取範圍動態變更文字。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-178">However, you can change text dynamically based on the selection.</span></span>

### <a name="subordinate-controls"></a><span data-ttu-id="b1cc9-179">次級控制項</span><span class="sxs-lookup"><span data-stu-id="b1cc9-179">Subordinate controls</span></span>

-   <span data-ttu-id="b1cc9-180">將從屬控制項放在或下方 (縮排，並使用選項按鈕標籤) 選項按鈕和其標籤。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-180">Place subordinate controls to the right of or below (indented, flush with the radio button label) the radio button and its label.</span></span> <span data-ttu-id="b1cc9-181">以冒號結束選項按鈕標籤。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-181">End the radio button label with a colon.</span></span>

    ![<span data-ttu-id="b1cc9-182">控制項在其標籤右邊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-182">screen shot of control to the right of its label</span></span> ](images/radio-buttons-image9.png)

    <span data-ttu-id="b1cc9-183">在此範例中，選項按鈕與其從屬控制項共用選項按鈕標籤及其存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-183">In this example, the radio button and its subordinate control share the radio button label and its access key.</span></span> <span data-ttu-id="b1cc9-184">在此情況下，方向鍵會將焦點從選項按鈕移至其附屬文字方塊。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-184">In this case, the arrow keys move focus from the radio button to its subordinate text box.</span></span>

-   <span data-ttu-id="b1cc9-185">**如果相依的可編輯文字方塊和下拉式清單共用選項按鈕的標籤，則保持啟用狀態。**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-185">**Leave dependent editable text boxes and drop-down lists enabled if they share the radio button's label.**</span></span> <span data-ttu-id="b1cc9-186">當使用者在方塊中輸入或貼上任何文字時，請自動選取對應的選項。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-186">When users type or paste anything into the box, select the corresponding option automatically.</span></span> <span data-ttu-id="b1cc9-187">這麼做可簡化互動。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-187">Doing so simplifies the interaction.</span></span>

    ![<span data-ttu-id="b1cc9-188">包含文字方塊之頁面範圍對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-188">screen shot of page range dialog box with text box</span></span> ](images/radio-buttons-image10.png)

    <span data-ttu-id="b1cc9-189">在此範例中，輸入頁碼會自動選取頁面。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-189">In this example, entering a page number automatically selects Pages.</span></span>

-   <span data-ttu-id="b1cc9-190">**避免使用其他選項按鈕或核取方塊來嵌套選項按鈕。**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-190">**Avoid nesting radio buttons with other radio buttons or check boxes.**</span></span> <span data-ttu-id="b1cc9-191">可能的話，請將所有選項保留在相同的層級。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-191">If possible, keep all the options at the same level.</span></span>

    <span data-ttu-id="b1cc9-192">**正確：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-192">**Correct:**</span></span>

    ![<span data-ttu-id="b1cc9-193">靠左對齊之選項按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-193">screen shot of left-aligned radio buttons</span></span> ](images/radio-buttons-image11.png)

    <span data-ttu-id="b1cc9-194">在此範例中，選項的等級相同。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-194">In this example, the options are at the same level.</span></span>

    <span data-ttu-id="b1cc9-195">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-195">**Incorrect:**</span></span>

    ![<span data-ttu-id="b1cc9-196">嵌套選項按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-196">screen shot of nested radio buttons</span></span> ](images/radio-buttons-image12.png)

    <span data-ttu-id="b1cc9-197">在此範例中，使用嵌套選項會增加不必要的複雜性。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-197">In this example, using nested options adds unnecessary complexity.</span></span>

-   <span data-ttu-id="b1cc9-198">如果您使用其他選項按鈕或核取方塊來嵌入選項按鈕，請 **停用這些附屬控制項，直到選取高階選項為止。**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-198">If you do nest radio buttons with other radio buttons or check boxes, **disable these subordinate controls until the high-level option is selected.**</span></span> <span data-ttu-id="b1cc9-199">這樣做可避免與從屬控制項的意義混淆。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-199">Doing so avoids confusion about the meaning of the subordinate controls.</span></span>

### <a name="default-values"></a><span data-ttu-id="b1cc9-200">預設值</span><span class="sxs-lookup"><span data-stu-id="b1cc9-200">Default values</span></span>

-   <span data-ttu-id="b1cc9-201">因為一組選項按鈕代表一組互斥的選項，所以 **預設一律會選取一個選項按鈕。選取最安全的 (，以避免資料遺失或系統存取) ，以及最安全且私用的選項。**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-201">Because a group of radio buttons represents a set of mutually exclusive choices, **always have one radio button selected by default. Select the safest (to prevent loss of data or system access) and most secure and private option.**</span></span> <span data-ttu-id="b1cc9-202">如果安全性和安全性不是因素，請選取最有可能或方便的選項。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-202">If safety and security aren't factors, select the most likely or convenient option.</span></span>
-   <span data-ttu-id="b1cc9-203">**例外狀況：** 如果有下列情況，則沒有預設選項：</span><span class="sxs-lookup"><span data-stu-id="b1cc9-203">**Exceptions:** Don't have a default selection if:</span></span>
    -   <span data-ttu-id="b1cc9-204">**基於安全、安全性或法律考慮，沒有可接受的預設選項，因此使用者必須做出明確的選擇。**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-204">**There is no acceptable default option for safety, security, or legal reasons and therefore the user must make an explicit choice.**</span></span> <span data-ttu-id="b1cc9-205">如果使用者未進行選取，則會顯示錯誤訊息來強制執行。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-205">If the user doesn't make a selection, display an error message to force one.</span></span>
    -   <span data-ttu-id="b1cc9-206">**使用者介面 (UI) 必須反映目前的狀態，而且尚未設定該選項。**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-206">**The user interface (UI) must reflect the current state and the option hasn't been set yet.**</span></span> <span data-ttu-id="b1cc9-207">預設值會不正確地表示使用者不需要進行選取。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-207">A default value would incorrectly imply that the user doesn't need to make a selection.</span></span>
    -   <span data-ttu-id="b1cc9-208">**目標是要收集非偏誤的資料。**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-208">**The goal is to collect unbiased data.**</span></span> <span data-ttu-id="b1cc9-209">預設值會偏差資料收集。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-209">Default values would bias data collection.</span></span>
    -   <span data-ttu-id="b1cc9-210">**選項按鈕群組代表混合狀態中的屬性**，當顯示多個沒有相同設定之物件的屬性時，就會發生此情況。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-210">**The group of radio buttons represents a property in a mixed state**, which happens when displaying a property for multiple objects that don't have the same setting.</span></span> <span data-ttu-id="b1cc9-211">在此情況下不會顯示錯誤訊息，因為每個物件都有有效的狀態。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-211">Don't display an error message in this case since each object has a valid state.</span></span>
-   <span data-ttu-id="b1cc9-212">**請將第一個選項設為預設選項**，因為使用者通常會預期這一點，除非該順序不是邏輯的。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-212">**Make the first option the default option**, since users often expect that—unless that order isn't logical.</span></span> <span data-ttu-id="b1cc9-213">若要這樣做，您可能需要變更選項標籤。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-213">To do this, you might need to change the option labels.</span></span>

    <span data-ttu-id="b1cc9-214">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-214">**Incorrect:**</span></span>

    ![<span data-ttu-id="b1cc9-215">最後一個選項按鈕的螢幕擷取畫面作為預設選項</span><span class="sxs-lookup"><span data-stu-id="b1cc9-215">screen shot of last radio button as default option</span></span> ](images/radio-buttons-image13.png)

    <span data-ttu-id="b1cc9-216">在此範例中，預設選項不是第一個選項。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-216">In this example, the default option isn't the first option.</span></span>

    <span data-ttu-id="b1cc9-217">**正確：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-217">**Correct:**</span></span>

    ![<span data-ttu-id="b1cc9-218">第一個選項按鈕的螢幕擷取畫面（預設值）</span><span class="sxs-lookup"><span data-stu-id="b1cc9-218">screen shot of first radio button as default</span></span> ](images/radio-buttons-image14.png)

    <span data-ttu-id="b1cc9-219">在此範例中，會改寫選項標籤，讓第一個選項成為預設選項。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-219">In this example, the option labels are reworded to make the first option the default option.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="b1cc9-220">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="b1cc9-220">Recommended sizing and spacing</span></span>

![<span data-ttu-id="b1cc9-221">選項按鈕調整大小和間距的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-221">screen shot of radio button sizing and spacing</span></span> ](images/radio-buttons-image15.png)

<span data-ttu-id="b1cc9-222">選項按鈕的建議大小和間距。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-222">Recommended sizing and spacing for radio buttons.</span></span>

## <a name="labels"></a><span data-ttu-id="b1cc9-223">標籤</span><span class="sxs-lookup"><span data-stu-id="b1cc9-223">Labels</span></span>

### <a name="radio-button-labels"></a><span data-ttu-id="b1cc9-224">選項按鈕標籤</span><span class="sxs-lookup"><span data-stu-id="b1cc9-224">Radio button labels</span></span>

-   <span data-ttu-id="b1cc9-225">為每個選項按鈕加上標籤。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-225">Label every radio button.</span></span>

<!-- -->

-   <span data-ttu-id="b1cc9-226">將唯一的 [存取金鑰](glossary.md) 指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-226">Assign a unique [access key](glossary.md) to each label.</span></span> <span data-ttu-id="b1cc9-227">如需指導方針，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-227">For guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="b1cc9-228">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-228">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="b1cc9-229">以片語的形式寫入標籤，而不是以句子撰寫，且不使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-229">Write the label as a phrase, not as a sentence, and use no ending punctuation.</span></span>
    -   <span data-ttu-id="b1cc9-230">**例外狀況：** 如果選項按鈕標籤也會標記其後的從屬控制項，請以冒號結束標籤。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-230">**Exception:** If a radio button label also labels a subordinate control that follows it, end the label with a colon.</span></span>
-   <span data-ttu-id="b1cc9-231">使用平行片語，並嘗試保留所有標籤的相同長度。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-231">Use parallel phrasing, and try to keep the length about the same for all labels.</span></span>
-   <span data-ttu-id="b1cc9-232">將標籤文字的焦點放在選項之間的差異。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-232">Focus the label text on the differences among the options.</span></span> <span data-ttu-id="b1cc9-233">如果所有選項都有相同的簡介文字，請將該文字移至群組標籤。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-233">If all the options have the same introductory text, move that text to the group label.</span></span>
-   <span data-ttu-id="b1cc9-234">使用正片語。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-234">Use positive phrasing.</span></span> <span data-ttu-id="b1cc9-235">例如，使用 do 而非 [否]，並使用 [列印] 而非 [列印]。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-235">For example, use do instead of do not, and print instead of do not print.</span></span>
-   <span data-ttu-id="b1cc9-236">只描述標籤的選項。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-236">Describe just the option with the label.</span></span> <span data-ttu-id="b1cc9-237">將標籤保持簡短，讓您可以輕鬆地在訊息和檔中參考它們。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-237">Keep labels brief so it's easy to refer to them in messages and documentation.</span></span> <span data-ttu-id="b1cc9-238">如果選項需要進一步說明，請使用完整的句子和結束標點符號在 [靜態文字](glossary.md) 控制項中提供說明。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-238">If the option requires further explanation, provide the explanation in a [static text](glossary.md) control using complete sentences and ending punctuation.</span></span>

    ![具有解說文字之選項按鈕的螢幕擷取畫面](images/radio-buttons-image16.png)

    <span data-ttu-id="b1cc9-240">在此範例中，會使用個別的靜態文字控制項來說明這些選項。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-240">In this example, the options are explained using separate static text controls.</span></span>

    > [!Note]  
    > <span data-ttu-id="b1cc9-241">將說明新增至一個選項按鈕，並不表示您必須提供所有選項按鈕的說明。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-241">Adding an explanation to one radio button doesn't mean that you have to provide explanations for all the radio buttons.</span></span> <span data-ttu-id="b1cc9-242">如果您可以的話，請在標籤中提供相關資訊，並且只在必要時使用說明。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-242">Provide the relevant information in the label if you can, and use explanations only when necessary.</span></span> <span data-ttu-id="b1cc9-243">請勿只重新聲明標籤以保持一致性。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-243">Don't merely restate the label for consistency.</span></span>

     

-   <span data-ttu-id="b1cc9-244">**如果強烈建議選項，請將「 (建議的) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-244">**If an option is strongly recommended, add "(recommended)" to the label.**</span></span> <span data-ttu-id="b1cc9-245">請務必新增至控制項標籤，而不是增補附注。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-245">Be sure to add to the control label, not the supplemental notes.</span></span>
-   <span data-ttu-id="b1cc9-246">**如果選項僅供 advanced 使用者使用，請將「 (advanced) 」新增至標籤。**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-246">**If an option is intended only for advanced users, add "(advanced)" to the label.**</span></span> <span data-ttu-id="b1cc9-247">請務必新增至控制項標籤，而不是增補附注。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-247">Be sure to add to the control label, not the supplemental notes.</span></span>
-   <span data-ttu-id="b1cc9-248">如果您必須使用多行標籤，請將標籤的頂端與選項按鈕對齊。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-248">If you must use multi-line labels, align the top of the label with the radio button.</span></span>
-   <span data-ttu-id="b1cc9-249">請勿使用從屬控制項、它所包含的值，或其單位標籤來建立句子或片語。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-249">Don't use a subordinate control, the values it contains, or its units label to create a sentence or phrase.</span></span> <span data-ttu-id="b1cc9-250">這類設計無法當地語系化，因為句子結構會隨著語言而有所不同。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-250">Such a design isn't localizable because sentence structure varies with language.</span></span>

### <a name="radio-button-group-labels"></a><span data-ttu-id="b1cc9-251">選項按鈕群組標籤</span><span class="sxs-lookup"><span data-stu-id="b1cc9-251">Radio button group labels</span></span>

-   <span data-ttu-id="b1cc9-252">使用群組標籤來說明群組的用途，而不是如何進行選取。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-252">Use the group label to explain the purpose of the group, not how to make the selection.</span></span> <span data-ttu-id="b1cc9-253">假設使用者知道如何使用選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-253">Assume that users know how to use radio buttons.</span></span> <span data-ttu-id="b1cc9-254">例如，不要說「選取下列其中一個選項」。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-254">For example, don't say "Select one of the following choices".</span></span>
-   <span data-ttu-id="b1cc9-255">所有的選項按鈕群組都需要標籤。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-255">All radio button groups need labels.</span></span> <span data-ttu-id="b1cc9-256">以單字或片語（而非句子）的形式寫入標籤，並使用靜態文字或群組方塊以冒號結尾。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-256">Write the label as a word or phrase, not as a sentence, ending with a colon using static text or a group box.</span></span>

    <span data-ttu-id="b1cc9-257">**例外狀況：** 如果標籤只是對話方塊 [主要指示](glossary.md)的重述，請省略標籤。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-257">**Exception:** Omit the label if it is merely a restatement of a dialog box's [main instruction](glossary.md).</span></span> <span data-ttu-id="b1cc9-258">在此情況下，除非有一個) ，否則 main 指令會接受冒號 (，除非它是問題) 和存取金鑰 (。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-258">In this case, the main instruction takes the colon (unless it's a question) and access key (if there is one).</span></span>

    <span data-ttu-id="b1cc9-259">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-259">**Acceptable:**</span></span>

    ![<span data-ttu-id="b1cc9-260">重複選項按鈕群組標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-260">screen shot of redundant radio-button group label</span></span> ](images/radio-buttons-image17.png)

    <span data-ttu-id="b1cc9-261">在此範例中，選項按鈕群組標籤只是主要指令的重述。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-261">In this example, the radio button group label is just a restatement of the main instruction.</span></span>

    <span data-ttu-id="b1cc9-262">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="b1cc9-262">**Better:**</span></span>

    ![<span data-ttu-id="b1cc9-263">選項按鈕主要指示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="b1cc9-263">screen shot of radio button main instruction only</span></span> ](images/radio-buttons-image18.png)

    <span data-ttu-id="b1cc9-264">在此範例中，會移除多餘的標籤，所以主要指令會接受冒號。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-264">In this example, the redundant label is removed, so the main instruction takes the colon.</span></span>

-   <span data-ttu-id="b1cc9-265">請勿指派標籤的存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-265">Don't assign an access key to the label.</span></span> <span data-ttu-id="b1cc9-266">這並不是必要的，而是讓其他存取金鑰更難指派。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-266">Doing so isn't necessary and it makes the other access keys harder to assign.</span></span>
    -   <span data-ttu-id="b1cc9-267">**例外狀況：** 如果並非所有控制項都可以有唯一的存取金鑰，您可以將存取金鑰指派給標籤，而不是個別控制項。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-267">**Exception:** If not all controls can have unique access keys, you can assign an access key to the label instead of the individual controls.</span></span> <span data-ttu-id="b1cc9-268">如需詳細資訊，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-268">For more information, see [Keyboard](inter-keyboard.md).</span></span>

## <a name="documentation"></a><span data-ttu-id="b1cc9-269">文件</span><span class="sxs-lookup"><span data-stu-id="b1cc9-269">Documentation</span></span>

<span data-ttu-id="b1cc9-270">參考選項按鈕時：</span><span class="sxs-lookup"><span data-stu-id="b1cc9-270">When referring to radio buttons:</span></span>

-   <span data-ttu-id="b1cc9-271">使用確切的標籤文字，包括其大小寫，但不包含存取金鑰底線或冒號。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-271">Use the exact label text, including its capitalization, but don't include the access key underscore or colon.</span></span>
-   <span data-ttu-id="b1cc9-272">在程式設計和其他技術檔中，請將選項按鈕稱為選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-272">In programming and other technical documentation, refer to radio buttons as radio buttons.</span></span> <span data-ttu-id="b1cc9-273">其他地方使用選項按鈕，尤其是在使用者檔中。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-273">Everywhere else use option buttons, especially in user documentation.</span></span>
-   <span data-ttu-id="b1cc9-274">若要描述使用者互動，請使用按一下。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-274">To describe user interaction, use click.</span></span>
-   <span data-ttu-id="b1cc9-275">可能的話，請使用粗體文字來格式化標籤。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-275">When possible, format the label using bold text.</span></span> <span data-ttu-id="b1cc9-276">否則，請只在必要時才將標籤放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-276">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="b1cc9-277">範例：按一下 [ **目前的頁面**]，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="b1cc9-277">Example: Click **Current page**, and then click **OK**.</span></span>

 

 