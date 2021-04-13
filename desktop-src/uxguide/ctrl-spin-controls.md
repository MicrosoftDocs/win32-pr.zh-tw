---
title: 微調控制項
description: 使用微調控制項時，使用者可以按一下箭號按鈕，以累加方式變更其相關數值文字方塊中的值。
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 54ce622983e52d65fa58ef05aca783ff67ebce66
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321416"
---
# <a name="spin-controls"></a><span data-ttu-id="328e1-103">微調控制項</span><span class="sxs-lookup"><span data-stu-id="328e1-103">Spin Controls</span></span>

> [!NOTE]
> <span data-ttu-id="328e1-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="328e1-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="328e1-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="328e1-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="328e1-106">使用微調控制項時，使用者可以按一下箭號按鈕，以累加方式變更其相關 [數值文字方塊](ctrl-text-boxes.md)中的值。</span><span class="sxs-lookup"><span data-stu-id="328e1-106">With a spin control, users can click arrow buttons to change incrementally the value within its associated [numeric text box](ctrl-text-boxes.md).</span></span> <span data-ttu-id="328e1-107">「微調」一詞是指文字方塊及其關聯之微調控制項的組合。</span><span class="sxs-lookup"><span data-stu-id="328e1-107">The term spin box refers to the combination of a text box and its associated spin control.</span></span>

![<span data-ttu-id="328e1-108">微調控制項和文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="328e1-108">screen shot of spin control and text box</span></span> ](images/ctrl-spin-controls-image1.png)

<span data-ttu-id="328e1-109">典型的微調方塊。</span><span class="sxs-lookup"><span data-stu-id="328e1-109">A typical spin box.</span></span>

<span data-ttu-id="328e1-110">使用者通常會偏好微調控制項，因為他們可以進行變更，而不需要從滑鼠移動手。</span><span class="sxs-lookup"><span data-stu-id="328e1-110">Users often prefer spin controls because they can make changes without moving their hands from the mouse.</span></span> <span data-ttu-id="328e1-111">當微調控制項與文字方塊配對時，使用者可以直接在文字方塊中輸入或貼上輸入，因此微調控制項的使用是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="328e1-111">When the spin control is paired with a text box, users can type or paste input directly in the text box, so use of the spin control is optional.</span></span>

<span data-ttu-id="328e1-112">當微調控制項用於數值輸入時，輸入不一定是純整數。</span><span class="sxs-lookup"><span data-stu-id="328e1-112">While spin controls are used for numeric input, the input doesn't have to be a pure whole number.</span></span> <span data-ttu-id="328e1-113">輸入可以是十進位數，而且可以有負號、分隔符號 (例如冒號或連字號) 和單位修飾詞。</span><span class="sxs-lookup"><span data-stu-id="328e1-113">The input can be decimal numbers and it can have negative signs, delimiters (such as colons or hyphens), and unit modifiers.</span></span>

> [!Note]  
> <span data-ttu-id="328e1-114">與 [文字方塊](ctrl-text-boxes.md) 和 [版面](vis-layout.md) 配置相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="328e1-114">Guidelines related to [text boxes](ctrl-text-boxes.md) and [layout](vis-layout.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="328e1-115">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="328e1-115">Is this the right control?</span></span>

<span data-ttu-id="328e1-116">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="328e1-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="328e1-117">**用於數值輸入的控制項？**</span><span class="sxs-lookup"><span data-stu-id="328e1-117">**Is the control used for numeric input?**</span></span> <span data-ttu-id="328e1-118">如果沒有，請使用另一個控制項（例如 [下拉式清單](/windows/desktop/uxguide/ctrl-drop) 或 [滑杆](ctrl-sliders.md)），從一組固定的值進行選取。</span><span class="sxs-lookup"><span data-stu-id="328e1-118">If not, use another control, such as a [drop-down list](/windows/desktop/uxguide/ctrl-drop) or [slider](ctrl-sliders.md), to select from a fixed set of values.</span></span> <span data-ttu-id="328e1-119">使用捲軸來進行滾動。</span><span class="sxs-lookup"><span data-stu-id="328e1-119">Use scroll bars for scrolling.</span></span>
-   <span data-ttu-id="328e1-120">**使用者是否將值視為相對數量，而不是數值？**</span><span class="sxs-lookup"><span data-stu-id="328e1-120">**Do users think of the value as a relative quantity, not a numeric value?**</span></span> <span data-ttu-id="328e1-121">如果是的話，請改用滑杆。</span><span class="sxs-lookup"><span data-stu-id="328e1-121">If so, use a slider instead.</span></span> <span data-ttu-id="328e1-122">只針對確切的已知數值使用微調方塊。</span><span class="sxs-lookup"><span data-stu-id="328e1-122">Use spin boxes only for exact, known numeric values.</span></span> <span data-ttu-id="328e1-123">例如，使用者想要將音訊音量設定為低或中，而不是設定值為 2 或 5。</span><span class="sxs-lookup"><span data-stu-id="328e1-123">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>
-   <span data-ttu-id="328e1-124">**控制項是否與文字方塊配對？**</span><span class="sxs-lookup"><span data-stu-id="328e1-124">**Is the control paired with a text box?**</span></span> <span data-ttu-id="328e1-125">如果沒有，請不要使用。</span><span class="sxs-lookup"><span data-stu-id="328e1-125">If not, don't use.</span></span> <span data-ttu-id="328e1-126">微調控制項不可以單獨使用，也不應該與文字方塊以外的其他控制項類型一起使用。</span><span class="sxs-lookup"><span data-stu-id="328e1-126">Spin controls shouldn't be used alone or with other types of controls besides a text box.</span></span>

    <span data-ttu-id="328e1-127">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="328e1-127">**Incorrect:**</span></span>

    ![<span data-ttu-id="328e1-128">微調控制項、圖形、無文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="328e1-128">screen shot of spin control, graphic, no text box</span></span> ](images/ctrl-spin-controls-image2.png)

    <span data-ttu-id="328e1-129">在此範例中，會使用微調控制項來控制動態圖形。</span><span class="sxs-lookup"><span data-stu-id="328e1-129">In this example, a spin control is used to control a dynamic graphic.</span></span>

-   <span data-ttu-id="328e1-130">**連續值範圍是否有效？**</span><span class="sxs-lookup"><span data-stu-id="328e1-130">**Are contiguous value ranges valid?**</span></span> <span data-ttu-id="328e1-131">如果沒有，請改用有效的值下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="328e1-131">If not, use a drop-down list of valid values instead.</span></span>

    ![<span data-ttu-id="328e1-132">下拉式清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="328e1-132">screen shot of drop-down list</span></span> ](images/ctrl-spin-controls-image3.png)

    <span data-ttu-id="328e1-133">在此範例中，並非所有磁片磁碟機號碼都有效，所以下拉式清單是較佳的選擇。</span><span class="sxs-lookup"><span data-stu-id="328e1-133">In this example, not all disk drive numbers are valid, so a drop-down list is a better choice.</span></span>

-   <span data-ttu-id="328e1-134">**使用微調控制項實用嗎？**</span><span class="sxs-lookup"><span data-stu-id="328e1-134">**Is using the spin control practical?**</span></span> <span data-ttu-id="328e1-135">針對下列情況，使用微調控制項非常實用：</span><span class="sxs-lookup"><span data-stu-id="328e1-135">Using a spin control is practical for:</span></span>

    -   <span data-ttu-id="328e1-136">輸入較小的數位，通常低於100。</span><span class="sxs-lookup"><span data-stu-id="328e1-136">Entering a small number, typically under 100.</span></span>
    -   <span data-ttu-id="328e1-137">對現有或預設值進行較小的變更。</span><span class="sxs-lookup"><span data-stu-id="328e1-137">Making small changes to an existing or default value.</span></span>

    <span data-ttu-id="328e1-138">雖然微調控制項可用於任何數值輸入，但在這些情況下，它們不會有效率。</span><span class="sxs-lookup"><span data-stu-id="328e1-138">While spin controls can be used for any numeric input, they are inefficient in situations other than these.</span></span>

-   <span data-ttu-id="328e1-139">**微調控制項有説明嗎？**</span><span class="sxs-lookup"><span data-stu-id="328e1-139">**Is the spin control helpful?**</span></span> <span data-ttu-id="328e1-140">控制項是在使用者可能使用其滑鼠的內容中使用嗎？</span><span class="sxs-lookup"><span data-stu-id="328e1-140">Is the control used in a context where users are likely to be using their mouse?</span></span> <span data-ttu-id="328e1-141">如果沒有，請考慮使用微調控制項。</span><span class="sxs-lookup"><span data-stu-id="328e1-141">If not, consider a spin control optional.</span></span>
-   <span data-ttu-id="328e1-142">**是否為 [同級控制項] 下拉式清單？**</span><span class="sxs-lookup"><span data-stu-id="328e1-142">**Are the sibling controls drop-down lists?**</span></span> <span data-ttu-id="328e1-143">如果有其他的下拉式清單，請考慮使用下拉式清單來保持一致性。</span><span class="sxs-lookup"><span data-stu-id="328e1-143">If there are other drop-down lists, consider using a drop-down list for consistency.</span></span>

    ![<span data-ttu-id="328e1-144">具有下拉式清單之對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="328e1-144">screen shot of dialog box with drop-down lists</span></span> ](images/ctrl-spin-controls-image4.png)

    <span data-ttu-id="328e1-145">在此範例中，可以使用微調方塊，但會使用下拉式清單來提供一致性。</span><span class="sxs-lookup"><span data-stu-id="328e1-145">In this example, a spin box could be used, but a drop-down list is used for consistency.</span></span>

-   <span data-ttu-id="328e1-146">**觸控或畫筆使用者是否為主要目標？**</span><span class="sxs-lookup"><span data-stu-id="328e1-146">**Are touch or pen users a primary target?**</span></span> <span data-ttu-id="328e1-147">如果是的話，請考慮改為使用下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="328e1-147">If so, consider using a drop-down list instead.</span></span> <span data-ttu-id="328e1-148">微調控制項中的箭號按鈕太小，無法使用觸控或畫筆有效率地使用。</span><span class="sxs-lookup"><span data-stu-id="328e1-148">The arrow buttons in a spin control are too small to be used efficiently with touch or a pen.</span></span>

<span data-ttu-id="328e1-149">如果有滑杆或微調方塊，請在下列情況下使用微調方塊：</span><span class="sxs-lookup"><span data-stu-id="328e1-149">If a slider or a spin box is possible, use a spin box if:</span></span>

-   <span data-ttu-id="328e1-150">螢幕空間很小。</span><span class="sxs-lookup"><span data-stu-id="328e1-150">Screen space is tight.</span></span>
-   <span data-ttu-id="328e1-151">使用者很可能會偏好使用鍵盤。</span><span class="sxs-lookup"><span data-stu-id="328e1-151">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="328e1-152">如果是下列情況，請使用滑桿：</span><span class="sxs-lookup"><span data-stu-id="328e1-152">Use a slider if:</span></span>

-   <span data-ttu-id="328e1-153">使用者可受益於立即回應。</span><span class="sxs-lookup"><span data-stu-id="328e1-153">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="328e1-154">指導方針</span><span class="sxs-lookup"><span data-stu-id="328e1-154">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="328e1-155">一般</span><span class="sxs-lookup"><span data-stu-id="328e1-155">General</span></span>

-   <span data-ttu-id="328e1-156">**使用微調控制項，只要它們是實用且有用的。**</span><span class="sxs-lookup"><span data-stu-id="328e1-156">**Use spin controls whenever they are practical and helpful.**</span></span> <span data-ttu-id="328e1-157">[這是正確的控制項嗎？](#is-this-the-right-control)</span><span class="sxs-lookup"><span data-stu-id="328e1-157">See [Is this the right control?](#is-this-the-right-control)</span></span>

    -   <span data-ttu-id="328e1-158">**例外狀況：** 若要與相同使用者介面上的其他文字方塊保持一致 (UI) ，請使用微調控制項，即使它們不一定可行也一樣。</span><span class="sxs-lookup"><span data-stu-id="328e1-158">**Exception:** To be consistent with other text boxes on the same user interface (UI), use spin controls even if they aren't always practical.</span></span>

    <span data-ttu-id="328e1-159">**正確：**</span><span class="sxs-lookup"><span data-stu-id="328e1-159">**Correct:**</span></span>

    ![<span data-ttu-id="328e1-160">月、日、年微調控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="328e1-160">screen shot of month, day, year spin controls</span></span> ](images/ctrl-spin-controls-image5.png)

    <span data-ttu-id="328e1-161">在此範例中，微調控制項會與 year 控制項搭配使用，以保持一致性，雖然它不一定是可行的。</span><span class="sxs-lookup"><span data-stu-id="328e1-161">In this example, a spin control is used with the year control for consistency, even though it isn't always practical.</span></span>

    <span data-ttu-id="328e1-162">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="328e1-162">**Incorrect:**</span></span>

    ![<span data-ttu-id="328e1-163">ip 位址微調控制的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="328e1-163">screen shot of ip address spin control</span></span> ](images/ctrl-spin-controls-image6.png)

    <span data-ttu-id="328e1-164">在此範例中，微調控制項是無法使用的。</span><span class="sxs-lookup"><span data-stu-id="328e1-164">In this example, the spin control is unusable.</span></span>

-   <span data-ttu-id="328e1-165">**一律讓微調控制項成為文字方塊的「合作者」。**</span><span class="sxs-lookup"><span data-stu-id="328e1-165">**Always make a spin control the "buddy" of the text box.**</span></span> <span data-ttu-id="328e1-166">這麼做會將微調控制項放在文字方塊內。</span><span class="sxs-lookup"><span data-stu-id="328e1-166">Doing so places the spin control inside the text box.</span></span>

    <span data-ttu-id="328e1-167">**正確：**</span><span class="sxs-lookup"><span data-stu-id="328e1-167">**Correct:**</span></span>

    ![<span data-ttu-id="328e1-168">在文字方塊內放置微調控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="328e1-168">screen shot of spin control placed inside text box</span></span> ](images/ctrl-spin-controls-image7.png)

    <span data-ttu-id="328e1-169">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="328e1-169">**Incorrect:**</span></span>

    ![<span data-ttu-id="328e1-170">在文字方塊外放置微調控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="328e1-170">screen shot of spin control placed outside text box</span></span> ](images/ctrl-spin-controls-image8.png)

    <span data-ttu-id="328e1-171">在正確的範例中，微調控制項放在其相關聯的文字方塊內。</span><span class="sxs-lookup"><span data-stu-id="328e1-171">In the correct example, the spin control is placed inside its associated text box.</span></span>

-   <span data-ttu-id="328e1-172">**停用微調控制項的相關聯文字方塊時，請將其停用。**</span><span class="sxs-lookup"><span data-stu-id="328e1-172">**Disable a spin control when its associated text box is disabled.**</span></span> <span data-ttu-id="328e1-173">微調控制項是一種補充的輸入方法，絕對不是唯一的輸入方法。</span><span class="sxs-lookup"><span data-stu-id="328e1-173">The spin control is a supplemental input method—never the only input method.</span></span>

### <a name="values"></a><span data-ttu-id="328e1-174">值</span><span class="sxs-lookup"><span data-stu-id="328e1-174">Values</span></span>

-   <span data-ttu-id="328e1-175">**定義上方按鈕，將值增加一個單位，並將底部按鈕減少一個單位。**</span><span class="sxs-lookup"><span data-stu-id="328e1-175">**Define the top button to increase the value by one unit and the bottom button to decrease by one unit.**</span></span> <span data-ttu-id="328e1-176">一般而言，此單位是一，但它應該是最小的價值變更。</span><span class="sxs-lookup"><span data-stu-id="328e1-176">Typically, the unit is one, but it should be the smallest common change in value.</span></span> <span data-ttu-id="328e1-177">在理想的情況下，微調控制項應該涵蓋所有有效值，而且比輸入文字更方便。</span><span class="sxs-lookup"><span data-stu-id="328e1-177">Ideally, the spin control should cover all valid values, and it should be more convenient than typing in the text.</span></span>

    ![<span data-ttu-id="328e1-178">[邊界] 微調控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="328e1-178">screen shot of 'margins' spin control</span></span> ](images/ctrl-spin-controls-image9.png)

    <span data-ttu-id="328e1-179">在此範例中，按一下微調控制項會將值變更為 .1，這是值中最小的一般變更。</span><span class="sxs-lookup"><span data-stu-id="328e1-179">In this example, clicking a spin control changes the values by .1, which is the smallest common change in value.</span></span> <span data-ttu-id="328e1-180">使用較小的單位會涵蓋有效值的範圍，但讓微調控制項無法使用。</span><span class="sxs-lookup"><span data-stu-id="328e1-180">Using a smaller unit would cover the range of valid values but make the spin controls unusable.</span></span>

-   <span data-ttu-id="328e1-181">**使用微調控制項可將輸入限制為有效的值。**</span><span class="sxs-lookup"><span data-stu-id="328e1-181">**Use the spin control to limit input to valid values.**</span></span> <span data-ttu-id="328e1-182">使用微調控制項絕不會導致不正確的值。</span><span class="sxs-lookup"><span data-stu-id="328e1-182">Using a spin control should never result in an incorrect value.</span></span>
-   <span data-ttu-id="328e1-183">**在有效值範圍的結尾，重新開機範圍。**</span><span class="sxs-lookup"><span data-stu-id="328e1-183">**At the end of a range of valid values, restart the range.**</span></span> <span data-ttu-id="328e1-184">微調控制項比喻是使用者正在旋轉值滾輪，因此是這類滾輪的行為。</span><span class="sxs-lookup"><span data-stu-id="328e1-184">The spin control metaphor is that the user is spinning a wheel of values, hence this wheel-like behavior.</span></span>
    -   <span data-ttu-id="328e1-185">**例外狀況：** 如果產生的值是不正確的，請勿重新開機範圍。</span><span class="sxs-lookup"><span data-stu-id="328e1-185">**Exception:** Don't restart the range if the resulting value is certain to be incorrect.</span></span>

        ![<span data-ttu-id="328e1-186">[份數] 微調控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="328e1-186">screen shot of 'number of copies' spin control</span></span> ](images/ctrl-spin-controls-image10.png)

        <span data-ttu-id="328e1-187">在此範例中，按一下向下箭號按鈕，並不會重新開機範圍 (，方法是前往最大值) ，因為該值一定不正確。</span><span class="sxs-lookup"><span data-stu-id="328e1-187">In this example, clicking the down arrow button doesn't restart the range (by going to the maximum value) because that value is certain to be incorrect.</span></span>

-   <span data-ttu-id="328e1-188">**使用文字，而非特殊數值。**</span><span class="sxs-lookup"><span data-stu-id="328e1-188">**Use text instead of special numeric values.**</span></span> <span data-ttu-id="328e1-189">允許使用者微調這些特殊值，而不需要知道這些特殊值並將其輸入。</span><span class="sxs-lookup"><span data-stu-id="328e1-189">Allow users to spin to these special values instead of having to know them and type them in.</span></span>

    ![<span data-ttu-id="328e1-190">[在 (永遠不) 時睡眠] 微調控制項的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="328e1-190">screen shot of 'sleep after (never)' spin control</span></span> ](images/ctrl-spin-controls-image11.png)

    <span data-ttu-id="328e1-191">在此範例中，絕對不是特殊值，但使用者可以微調。</span><span class="sxs-lookup"><span data-stu-id="328e1-191">In this example, Never is a special value but users can spin to it.</span></span>

-   <span data-ttu-id="328e1-192">**如果值具有分隔符號，則相關聯的文字方塊應該有多個輸入焦點點。**</span><span class="sxs-lookup"><span data-stu-id="328e1-192">**If the value has delimiters, the associated text box should have multiple input focus points.**</span></span> <span data-ttu-id="328e1-193">這麼做可讓您個別運算元值區段。</span><span class="sxs-lookup"><span data-stu-id="328e1-193">Doing so allows the numeric segments to be manipulated individually.</span></span>

    ![<span data-ttu-id="328e1-194">時間微調控制項的螢幕擷取畫面，選取的分鐘數</span><span class="sxs-lookup"><span data-stu-id="328e1-194">screen shot of time spin control, minutes selected</span></span> ](images/ctrl-spin-controls-image12.png)

    <span data-ttu-id="328e1-195">在此範例中，微調控制項會影響小時、分、秒和 am/P.M. 的值（以其焦點為准）。</span><span class="sxs-lookup"><span data-stu-id="328e1-195">In this example, the spin control affects the values for hours, minutes, seconds, and A.M./P.M.—whichever has the focus.</span></span>

-   <span data-ttu-id="328e1-196">**如果值具有單位，請使用微調控制項來變更這些單位。**</span><span class="sxs-lookup"><span data-stu-id="328e1-196">**If the value has units, use the spin control to change those units as well.**</span></span>

    ![<span data-ttu-id="328e1-197">時間微調控制項的螢幕擷取畫面，[a.m.]</span><span class="sxs-lookup"><span data-stu-id="328e1-197">screen shot of time spin control, 'a.m.'</span></span> <span data-ttu-id="328e1-198">已選取</span><span class="sxs-lookup"><span data-stu-id="328e1-198">selected</span></span> ](images/ctrl-spin-controls-image13.png)

    <span data-ttu-id="328e1-199">在此範例中，微調控制項可以用來變更單位。</span><span class="sxs-lookup"><span data-stu-id="328e1-199">In this example, the spin control can be used to change units.</span></span>

## <a name="labels"></a><span data-ttu-id="328e1-200">標籤</span><span class="sxs-lookup"><span data-stu-id="328e1-200">Labels</span></span>

-   <span data-ttu-id="328e1-201">套用 [文字方塊標籤](ctrl-text-boxes.md) 指導方針，以標示相關聯的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="328e1-201">Apply the [text box labeling](ctrl-text-boxes.md) guidelines to label the associated text box.</span></span> <span data-ttu-id="328e1-202">微調控制項絕不會直接標記。</span><span class="sxs-lookup"><span data-stu-id="328e1-202">Spin controls are never labeled directly.</span></span>

## <a name="documentation"></a><span data-ttu-id="328e1-203">文件</span><span class="sxs-lookup"><span data-stu-id="328e1-203">Documentation</span></span>

<span data-ttu-id="328e1-204">參考微調控制項時：</span><span class="sxs-lookup"><span data-stu-id="328e1-204">When referring to spin controls:</span></span>

-   <span data-ttu-id="328e1-205">請勿在使用者檔中參考微調控制項。</span><span class="sxs-lookup"><span data-stu-id="328e1-205">Don't refer to spin controls in user documentation.</span></span> <span data-ttu-id="328e1-206">相反地，請參閱相關聯文字方塊的標籤。</span><span class="sxs-lookup"><span data-stu-id="328e1-206">Instead, refer to the label of the associated text box.</span></span>
-   <span data-ttu-id="328e1-207">請只在程式設計和其他技術檔中參考微調控制項和微調方塊。</span><span class="sxs-lookup"><span data-stu-id="328e1-207">Refer to spin controls and spin boxes only in programming and other technical documentation.</span></span>

<span data-ttu-id="328e1-208">範例：在 [ **日期** ] 方塊中，輸入或選取您要變更的日期部分。</span><span class="sxs-lookup"><span data-stu-id="328e1-208">Example: In the **Date** box, type or select the part of the date you want to change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="328e1-209">相關主題</span><span class="sxs-lookup"><span data-stu-id="328e1-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="328e1-210">詞彙</span><span class="sxs-lookup"><span data-stu-id="328e1-210">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 