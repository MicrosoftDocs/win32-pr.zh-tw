---
title: 核取方塊
description: 使用核取方塊時，使用者會在兩個明顯相反的選擇之間做出決定。
ms.assetid: 7c39987d-807b-41c1-9788-65c3d468b976
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 20cf5bc4fd13b974f87fbb33a5fea9a365f99735
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524300"
---
# <a name="check-boxes"></a><span data-ttu-id="bbc62-103">核取方塊</span><span class="sxs-lookup"><span data-stu-id="bbc62-103">Check Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="bbc62-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="bbc62-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="bbc62-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="bbc62-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="bbc62-106">使用核取方塊時，使用者會在兩個明顯相反的選擇之間做出決定。</span><span class="sxs-lookup"><span data-stu-id="bbc62-106">With a check box, users make a decision between two clearly opposite choices.</span></span> <span data-ttu-id="bbc62-107">核取方塊標籤表示選取的狀態，而已清除狀態的意義必須與所選狀態的明確相反。</span><span class="sxs-lookup"><span data-stu-id="bbc62-107">The check box label indicates the selected state, whereas the meaning of the cleared state must be the unambiguous opposite of the selected state.</span></span> <span data-ttu-id="bbc62-108">因此， **核取方塊只能用來開啟或關閉選項，或選取或取消選取專案。**</span><span class="sxs-lookup"><span data-stu-id="bbc62-108">Consequently, **check boxes should be used only to toggle an option on or off or to select or deselect an item.**</span></span>

![<span data-ttu-id="bbc62-109">選取四個核取方塊之一的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-109">screen shot of one of four check boxes selected</span></span> ](images/ctrl-check-boxes-image1.png)

<span data-ttu-id="bbc62-110">一般的核取方塊群組。</span><span class="sxs-lookup"><span data-stu-id="bbc62-110">A typical group of check boxes.</span></span>

> [!Note]  
> <span data-ttu-id="bbc62-111">與 [版面](vis-layout.md) 配置相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="bbc62-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="bbc62-112">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="bbc62-112">Is this the right control?</span></span>

<span data-ttu-id="bbc62-113">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="bbc62-113">To decide, consider these questions:</span></span>

-   <span data-ttu-id="bbc62-114">**這是用來切換選項或選取或取消選取專案的核取方塊？**</span><span class="sxs-lookup"><span data-stu-id="bbc62-114">**Is the check box used to toggle an option on or off or to select or deselect an item?**</span></span> <span data-ttu-id="bbc62-115">如果不是，請使用其他控制項。</span><span class="sxs-lookup"><span data-stu-id="bbc62-115">If not, use another control.</span></span>
-   <span data-ttu-id="bbc62-116">**選取和清除的狀態是清楚且明確的相反嗎？**</span><span class="sxs-lookup"><span data-stu-id="bbc62-116">**Are the selected and cleared states clear and unambiguous opposites?**</span></span> <span data-ttu-id="bbc62-117">如果沒有，請使用 [選項按鈕](ctrl-radio-buttons.md) 或 [下拉式清單](/windows/desktop/uxguide/ctrl-drop) ，讓您可以個別標記狀態。</span><span class="sxs-lookup"><span data-stu-id="bbc62-117">If not, use [radio buttons](ctrl-radio-buttons.md) or a [drop-down list](/windows/desktop/uxguide/ctrl-drop) so that you can label the states independently.</span></span>
-   <span data-ttu-id="bbc62-118">**在群組中使用時，群組是否會包含獨立的選項，讓使用者選擇零或更多？**</span><span class="sxs-lookup"><span data-stu-id="bbc62-118">**When used in a group, does the group comprise independent choices, from which users may choose zero or more?**</span></span> <span data-ttu-id="bbc62-119">如果沒有，請考慮相依選項的控制項，例如選項按鈕和 [核取方塊樹狀檢視](ctrl-tree-views.md)。</span><span class="sxs-lookup"><span data-stu-id="bbc62-119">If not, consider controls for dependent choices, such as radio buttons and [check box tree views](ctrl-tree-views.md).</span></span>
-   <span data-ttu-id="bbc62-120">**在群組中使用時，群組是否會組成相依選項，使用者必須從中選擇一或多個專案？**</span><span class="sxs-lookup"><span data-stu-id="bbc62-120">**When used in a group, does the group comprise dependent choices, from which users must choose one or more?**</span></span> <span data-ttu-id="bbc62-121">如果是的話，請在未選取任何選項時，使用一組核取方塊並處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="bbc62-121">If so, use a group of check boxes and handle the error when none of the options are selected.</span></span>
-   <span data-ttu-id="bbc62-122">**群組中的選項數目是否為10或更少？**</span><span class="sxs-lookup"><span data-stu-id="bbc62-122">**Is the number of options in a group 10 or fewer?**</span></span> <span data-ttu-id="bbc62-123">由於使用的螢幕空間與選項數目成正比，因此請將核取方塊的數目維持在10個以下。</span><span class="sxs-lookup"><span data-stu-id="bbc62-123">Since the screen space used is proportional to the number of options, keep the number of check boxes to 10 or fewer.</span></span> <span data-ttu-id="bbc62-124">如果有10個以上的選項，請使用 [核取方塊清單](ctrl-list-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="bbc62-124">For more than 10 options, use a [check box list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="bbc62-125">**選項按鈕是否是較佳的選擇？**</span><span class="sxs-lookup"><span data-stu-id="bbc62-125">**Would a radio button be a better choice?**</span></span> <span data-ttu-id="bbc62-126">如果核取方塊僅適用于開啟或關閉選項，選項按鈕可以用於完全不同的選項。</span><span class="sxs-lookup"><span data-stu-id="bbc62-126">Where check boxes are suitable only for turning an option on or off, radio buttons can be used for completely different options.</span></span> <span data-ttu-id="bbc62-127">如果這兩種解決方案都可行：</span><span class="sxs-lookup"><span data-stu-id="bbc62-127">If both solutions are possible:</span></span>
    -   <span data-ttu-id="bbc62-128">如果已清除核取方塊的意義不完全明顯，請使用選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="bbc62-128">Use radio buttons if the meaning of the cleared check box isn't completely obvious.</span></span>

        <span data-ttu-id="bbc62-129">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-129">**Incorrect:**</span></span>

        ![<span data-ttu-id="bbc62-130">一個標示為 [橫向] 核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-130">screen shot of one check box labeled landscape</span></span> ](images/ctrl-check-boxes-image2.png)

        <span data-ttu-id="bbc62-131">在此範例中，來自橫向的相反選擇並不清楚，因此核取方塊不是理想的選擇。</span><span class="sxs-lookup"><span data-stu-id="bbc62-131">In this example, the opposite choice from Landscape isn't clear, so the check box isn't a good choice.</span></span>

        <span data-ttu-id="bbc62-132">**正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-132">**Correct:**</span></span>

        ![<span data-ttu-id="bbc62-133">兩個選項按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-133">screen shot of two radio buttons</span></span> ](images/ctrl-check-boxes-image3.png)

        <span data-ttu-id="bbc62-134">在此範例中，不會相反選項，因此選項按鈕是較佳的選擇。</span><span class="sxs-lookup"><span data-stu-id="bbc62-134">In this example, the choices are not opposites so radio buttons are the better choice.</span></span>

    -   <span data-ttu-id="bbc62-135">在 [wizard] 頁面上使用選項按鈕，讓替代方案更清楚，即使核取方塊是可接受的。</span><span class="sxs-lookup"><span data-stu-id="bbc62-135">Use radio buttons on wizard pages to make the alternatives clear, even if a check box is otherwise acceptable.</span></span>
    -   <span data-ttu-id="bbc62-136">如果您有足夠的螢幕空間，而且選項很重要，足以充分利用該螢幕空間，請使用選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="bbc62-136">Use radio buttons if you have enough screen space and the options are important enough to be a good use of that screen space.</span></span> <span data-ttu-id="bbc62-137">否則，請使用核取方塊或下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="bbc62-137">Otherwise, use a check box or a drop-down list.</span></span>

        <span data-ttu-id="bbc62-138">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-138">**Incorrect:**</span></span>

        ![<span data-ttu-id="bbc62-139">顯示和不顯示比例按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-139">screen shot of show and don't show ratio buttons</span></span> ](images/ctrl-check-boxes-image4.png)

        <span data-ttu-id="bbc62-140">在此範例中，選項的重要性不足以使用選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="bbc62-140">In this example, the options aren't important enough to use radio buttons.</span></span>

        <span data-ttu-id="bbc62-141">**正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-141">**Correct:**</span></span>

        ![<span data-ttu-id="bbc62-142">[不顯示訊息] 核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-142">screen shot of check box with don't show message</span></span> ](images/ctrl-check-boxes-image5.png)

        <span data-ttu-id="bbc62-143">在此範例中，核取方塊是此周邊選項的螢幕空間有效率的使用方式。</span><span class="sxs-lookup"><span data-stu-id="bbc62-143">In this example, a check box is an efficient use of screen space for this peripheral option.</span></span>

-   <span data-ttu-id="bbc62-144">如果視窗有其他核取方塊，請使用核取方塊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-144">Use a check box if there other check boxes on the window.</span></span>
-   <span data-ttu-id="bbc62-145">**選項是否會顯示程式選項，而不是資料？**</span><span class="sxs-lookup"><span data-stu-id="bbc62-145">**Does the option present a program option, rather than data?**</span></span> <span data-ttu-id="bbc62-146">選項的值不應以內容或其他資料為基礎。</span><span class="sxs-lookup"><span data-stu-id="bbc62-146">The option's values shouldn't be based on context or other data.</span></span> <span data-ttu-id="bbc62-147">針對資料，請使用核取方塊清單或 [多重選取清單](ctrl-list-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="bbc62-147">For data, use a check box list or [multiple-selection list](ctrl-list-boxes.md).</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="bbc62-148">使用模式</span><span class="sxs-lookup"><span data-stu-id="bbc62-148">Usage patterns</span></span>

<span data-ttu-id="bbc62-149">核取方塊有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="bbc62-149">Check boxes have several usage patterns:</span></span>



|    <span data-ttu-id="bbc62-150">使用狀況</span><span class="sxs-lookup"><span data-stu-id="bbc62-150">Usage</span></span>                                                                          |         <span data-ttu-id="bbc62-151">範例</span><span class="sxs-lookup"><span data-stu-id="bbc62-151">Example</span></span>                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc62-152">**個別選擇** 單一核取方塊用來選取個別選項。</span><span class="sxs-lookup"><span data-stu-id="bbc62-152">**An individual choice** A single check box is used to select an individual choice.</span></span> <br/>                                                                                                             | ![<span data-ttu-id="bbc62-153">具有提醒我標籤的一個核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-153">screen shot of one check box with remind me label</span></span> ](images/ctrl-check-boxes-image6.png)<br/> <span data-ttu-id="bbc62-154">單一核取方塊用於個別選項。</span><span class="sxs-lookup"><span data-stu-id="bbc62-154">A single check box is used for an individual choice.</span></span><br/>                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="bbc62-155">**(零或多個) 的獨立選項** 一組核取方塊用來從一組零或多個選擇中選取。</span><span class="sxs-lookup"><span data-stu-id="bbc62-155">**Independent choices (zero or more)** A group of check boxes is used to select from a set of zero or more choices.</span></span><br/>                                                                              | <span data-ttu-id="bbc62-156">與 [選項按鈕（例如選項按鈕](ctrl-radio-buttons.md)）不同的是，使用者可以在一組核取方塊中選取任意組合的選項。</span><span class="sxs-lookup"><span data-stu-id="bbc62-156">unlike single-selection controls such as [radio buttons](ctrl-radio-buttons.md), users can select any combination of options in a group of check boxes.</span></span><br/> <span data-ttu-id="bbc62-157">![選取三個核取方塊中兩個核取方塊的螢幕擷取畫面 ](images/ctrl-check-boxes-image7.png)</span><span class="sxs-lookup"><span data-stu-id="bbc62-157">![screen shot of two of three check boxes selected ](images/ctrl-check-boxes-image7.png)</span></span><br/> <span data-ttu-id="bbc62-158">一組核取方塊用於獨立選擇。</span><span class="sxs-lookup"><span data-stu-id="bbc62-158">A group of check boxes is used for independent choices.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="bbc62-159">**(一或多個) 的相依選項** 一組核取方塊也可以用來從一組或多個選項中選取。</span><span class="sxs-lookup"><span data-stu-id="bbc62-159">**Dependent choices (one or more)** A group of check boxes can also be used to select from a set of one or more choices.</span></span><br/>                                                                         | <span data-ttu-id="bbc62-160">**您可能需要表示一或多個相依選項的選取專案**。</span><span class="sxs-lookup"><span data-stu-id="bbc62-160">**you may need to represent a selection of one or more dependent choices**.</span></span> <span data-ttu-id="bbc62-161">由於 microsoft 的 windows 沒有直接支援這種輸入類型的控制項，因此最好的解決方法是在未選取任何選項時，使用一組核取方塊並處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="bbc62-161">because microsoft?windows doesn't have a control that directly supports this type of input, the best solution is to use a group of check boxes and handle the error when none of the options are selected.</span></span><br/> <span data-ttu-id="bbc62-162">![已選取兩個核取方塊之一的螢幕擷取畫面 ](images/ctrl-check-boxes-image8.png)</span><span class="sxs-lookup"><span data-stu-id="bbc62-162">![screen shot of one of two check boxes selected ](images/ctrl-check-boxes-image8.png)</span></span><br/> <span data-ttu-id="bbc62-163">必須選取至少一個通訊協定的核取方塊群組。</span><span class="sxs-lookup"><span data-stu-id="bbc62-163">A group of check boxes is used where at least one protocol must be selected.</span></span><br/> |
| <span data-ttu-id="bbc62-164">**混合選擇** 除了選取和清除的狀態之外，核取方塊也會有多重選取的混合狀態，表示已針對部分（而非全部）物件設定該選項。</span><span class="sxs-lookup"><span data-stu-id="bbc62-164">**Mixed choice** In addition to their selected and cleared states, check boxes also have a mixed state for multiple selection to indicate that the option is set for some, but not all, objects.</span></span><br/> | ![<span data-ttu-id="bbc62-165">純藍色唯讀核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-165">screen shot of a solid blue read-only check box</span></span> ](images/ctrl-check-boxes-image9.png)<br/> <span data-ttu-id="bbc62-166">混合狀態的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-166">A mixed-state check box.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="guidelines"></a><span data-ttu-id="bbc62-167">指導方針</span><span class="sxs-lookup"><span data-stu-id="bbc62-167">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="bbc62-168">一般</span><span class="sxs-lookup"><span data-stu-id="bbc62-168">General</span></span>

-   <span data-ttu-id="bbc62-169">**群組相關的核取方塊**。</span><span class="sxs-lookup"><span data-stu-id="bbc62-169">**Group related check boxes**.</span></span> <span data-ttu-id="bbc62-170">如有必要，請使用多個群組，將相關選項和不相關的選項分開至10個或更少的群組。</span><span class="sxs-lookup"><span data-stu-id="bbc62-170">Combine related options and separate unrelated options into groups of 10 or fewer, using multiple groups if necessary.</span></span>

    ![<span data-ttu-id="bbc62-171">相關且不相關核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-171">screen shot of related and unrelated check boxes</span></span> ](images/ctrl-check-boxes-image10.png)

    <span data-ttu-id="bbc62-172">相關、獨立選項的群組範例。</span><span class="sxs-lookup"><span data-stu-id="bbc62-172">An example of groups of related, independent options.</span></span>

-   <span data-ttu-id="bbc62-173">重新 **考慮使用群組方塊來組織核取方塊的群組，** 這通常會造成不必要的螢幕雜亂。</span><span class="sxs-lookup"><span data-stu-id="bbc62-173">**Reconsider using group boxes to organize groups of check boxes** this often results in unnecessary screen clutter.</span></span>
-   <span data-ttu-id="bbc62-174">**以邏輯順序列出核取方塊**，例如將高度相關的選項群組在一起，或先放置最常見的選項，或遵循一些其他自然進展。</span><span class="sxs-lookup"><span data-stu-id="bbc62-174">**List check boxes in a logical order**, such as grouping highly related options together or placing most common options first, or following some other natural progression.</span></span> <span data-ttu-id="bbc62-175">不建議依字母順序排序，因為它是語言相依，因此不可當地語系化。</span><span class="sxs-lookup"><span data-stu-id="bbc62-175">Alphabetical ordering isn't recommended because it is language dependent, and therefore not localizable.</span></span>
-   <span data-ttu-id="bbc62-176">**垂直對齊核取方塊，而不是水準對齊**。</span><span class="sxs-lookup"><span data-stu-id="bbc62-176">**Align check boxes vertically, not horizontally**.</span></span> <span data-ttu-id="bbc62-177">水準對齊較難閱讀。</span><span class="sxs-lookup"><span data-stu-id="bbc62-177">Horizontal alignment is harder to read.</span></span>

    <span data-ttu-id="bbc62-178">**正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-178">**Correct:**</span></span>

    ![<span data-ttu-id="bbc62-179">垂直對齊之核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-179">screen shot of check boxes aligned vertically</span></span> ](images/ctrl-check-boxes-image11.png)

    <span data-ttu-id="bbc62-180">在此範例中，核取方塊已正確對齊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-180">In this example, the check boxes are correctly aligned.</span></span>

    <span data-ttu-id="bbc62-181">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-181">**Incorrect:**</span></span>

    ![<span data-ttu-id="bbc62-182">水準對齊之核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-182">screen shot of check boxes aligned horizontally</span></span> ](images/ctrl-check-boxes-image12.png)

    <span data-ttu-id="bbc62-183">在此範例中，水準對齊較難閱讀。</span><span class="sxs-lookup"><span data-stu-id="bbc62-183">In this example, the horizontal alignment is harder to read.</span></span>

-   <span data-ttu-id="bbc62-184">**請勿使用混合狀態來表示第三個狀態。**</span><span class="sxs-lookup"><span data-stu-id="bbc62-184">**Don't use the mixed state to represent a third state.**</span></span> <span data-ttu-id="bbc62-185">混合狀態用來指出某個選項是針對部分（而非全部）子物件所設定。</span><span class="sxs-lookup"><span data-stu-id="bbc62-185">The mixed state is used to indicate that an option is set for some, but not all, child objects.</span></span> <span data-ttu-id="bbc62-186">使用者應該無法直接設定混合狀態，而是混合狀態是子物件的反映。</span><span class="sxs-lookup"><span data-stu-id="bbc62-186">Users shouldn't be able to set a mixed state directly rather the mixed state is a reflection of the child objects.</span></span> <span data-ttu-id="bbc62-187">混合狀態不會當做個別專案的第三個狀態使用。</span><span class="sxs-lookup"><span data-stu-id="bbc62-187">The mixed state isn't used as a third state for an individual item.</span></span> <span data-ttu-id="bbc62-188">若要表示第三個狀態，請改用選項按鈕或下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="bbc62-188">To represent a third state, use radio buttons or a drop-down list instead.</span></span>

    <span data-ttu-id="bbc62-189">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-189">**Incorrect:**</span></span>

    ![<span data-ttu-id="bbc62-190">純色藍色主題服務核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-190">screen shot of solid blue theme service check box</span></span> ](images/ctrl-check-boxes-image13.png)

    <span data-ttu-id="bbc62-191">在此範例中，混合狀態應該指出未安裝主題服務。</span><span class="sxs-lookup"><span data-stu-id="bbc62-191">In this example, the mixed state is supposed to indicate that the Theme service isn't installed.</span></span>

    <span data-ttu-id="bbc62-192">**正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-192">**Correct:**</span></span>

    ![<span data-ttu-id="bbc62-193">包含三個選項之下拉式清單的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-193">screen shot of drop-down list with three options</span></span> ](images/ctrl-check-boxes-image14.png)

    <span data-ttu-id="bbc62-194">在此範例中，使用者可以從三個清楚的選項清單中選擇。</span><span class="sxs-lookup"><span data-stu-id="bbc62-194">In this example, users can choose from a list of three clear options.</span></span>

-   <span data-ttu-id="bbc62-195">**按一下 [混合狀態] 核取方塊，應該會迴圈顯示所有選取的、全部清除，以及原始的混合狀態。**</span><span class="sxs-lookup"><span data-stu-id="bbc62-195">**Clicking a mixed state check box should cycle through all selected, all cleared, and the original mixed states.**</span></span> <span data-ttu-id="bbc62-196">針對容許，請務必要能夠還原原始混合狀態，因為這些設定對使用者而言可能很複雜或未知。</span><span class="sxs-lookup"><span data-stu-id="bbc62-196">For forgiveness, it's important to be able to restore the original mixed state because the settings might be complex or unknown to the user.</span></span> <span data-ttu-id="bbc62-197">否則，若要放心還原混合狀態，唯一的方法就是取消工作並重新開始。</span><span class="sxs-lookup"><span data-stu-id="bbc62-197">Otherwise, the only way to restore the mixed state with confidence would be to cancel the task and start over.</span></span>
-   <span data-ttu-id="bbc62-198">**請勿使用核取方塊作為進度指標**。</span><span class="sxs-lookup"><span data-stu-id="bbc62-198">**Don't use check boxes as a progress indicator**.</span></span> <span data-ttu-id="bbc62-199">請改用 [進度指標](progress-bars.md) 控制項。</span><span class="sxs-lookup"><span data-stu-id="bbc62-199">Use a [progress indicator](progress-bars.md) control instead.</span></span>

    <span data-ttu-id="bbc62-200">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-200">**Incorrect:**</span></span>

    ![<span data-ttu-id="bbc62-201">顯示進度的四個核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-201">screen shot of four check boxes showing progress</span></span> ](images/ctrl-check-boxes-image15.png)

    <span data-ttu-id="bbc62-202">在此範例中，會使用不正確的核取方塊作為進度指標。</span><span class="sxs-lookup"><span data-stu-id="bbc62-202">In this example, check boxes are used incorrectly as a progress indicator.</span></span>

    <span data-ttu-id="bbc62-203">**正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-203">**Correct:**</span></span>

    ![<span data-ttu-id="bbc62-204">部分填滿進度列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-204">screen shot of a partially filled progress bar</span></span> ](images/ctrl-check-boxes-image16.png)

    <span data-ttu-id="bbc62-205">一般進度列的範例。</span><span class="sxs-lookup"><span data-stu-id="bbc62-205">Example of a typical progress bar.</span></span>

-   <span data-ttu-id="bbc62-206">**使用正確的選取狀態顯示已停用的核取方塊。**</span><span class="sxs-lookup"><span data-stu-id="bbc62-206">**Show disabled check boxes using the correct selection state.**</span></span> <span data-ttu-id="bbc62-207">雖然使用者無法變更它們，但停用的核取方塊會傳達資訊，以便與結果一致。</span><span class="sxs-lookup"><span data-stu-id="bbc62-207">Even though users can't change them, disabled check boxes convey information so they should be consistent with results.</span></span>

    <span data-ttu-id="bbc62-208">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-208">**Incorrect:**</span></span>

    ![<span data-ttu-id="bbc62-209">將兩個核取方塊的螢幕擷取畫面變成灰色</span><span class="sxs-lookup"><span data-stu-id="bbc62-209">screen shot of one of two check boxes dimmed</span></span> ](images/ctrl-check-boxes-image17.png)

    <span data-ttu-id="bbc62-210">在此範例中，應該清除 [永遠閱讀此區段] 選項，因為停用選項時不會讀取區段。</span><span class="sxs-lookup"><span data-stu-id="bbc62-210">In this example, the "Always read this section aloud" option should be cleared because the section isn't read when the option is disabled.</span></span>

-   <span data-ttu-id="bbc62-211">**請勿使用核取方塊的選取專案來**：</span><span class="sxs-lookup"><span data-stu-id="bbc62-211">**Don't use the selection of a check box to**:</span></span>
    -   <span data-ttu-id="bbc62-212">執行命令。</span><span class="sxs-lookup"><span data-stu-id="bbc62-212">Perform commands.</span></span>
    -   <span data-ttu-id="bbc62-213">顯示其他視窗，例如用來收集更多輸入的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-213">Display other windows, such as a dialog box to gather more input.</span></span>
    -   <span data-ttu-id="bbc62-214">以動態方式顯示與所選取控制項相關的其他控制項 (畫面讀取器無法偵測到這類事件) 。</span><span class="sxs-lookup"><span data-stu-id="bbc62-214">Dynamically display other controls related to the selected control (screen readers cannot detect such events).</span></span>

### <a name="dont-show-this-item-again"></a><span data-ttu-id="bbc62-215">不要顯示此</span><span class="sxs-lookup"><span data-stu-id="bbc62-215">Don't show this</span></span> <item> <span data-ttu-id="bbc62-216">再次</span><span class="sxs-lookup"><span data-stu-id="bbc62-216">again</span></span>

-   <span data-ttu-id="bbc62-217">**<item>如果沒有更好的替代方案，請考慮使用 [不要再顯示這個選項] 選項，讓使用者隱藏週期性對話方塊。**</span><span class="sxs-lookup"><span data-stu-id="bbc62-217">**Consider using a Don't show this <item> again option to allow users to suppress a recurring dialog box only if there isn't a better alternative.**</span></span> <span data-ttu-id="bbc62-218">如果使用者真的需要此對話方塊，請嘗試事先判斷：如果有，請一律顯示對話方塊，如果沒有，則刪除對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-218">Try to determine beforehand if users really need the dialog; if they do, always show the dialog, and if they don't, eliminate the dialog.</span></span>

<span data-ttu-id="bbc62-219">如需詳細的指導方針和範例，請參閱 [對話方塊](win-dialog-box.md)。</span><span class="sxs-lookup"><span data-stu-id="bbc62-219">For more guidelines and examples, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="subordinate-controls"></a><span data-ttu-id="bbc62-220">次級控制項</span><span class="sxs-lookup"><span data-stu-id="bbc62-220">Subordinate controls</span></span>

-   <span data-ttu-id="bbc62-221">將從屬控制項放在 (縮排的右方或下方，並將核取方塊標籤) 核取方塊和其標籤。</span><span class="sxs-lookup"><span data-stu-id="bbc62-221">Place subordinate controls to the right of or below (indented, flush with the check box label) the check box and its label.</span></span> <span data-ttu-id="bbc62-222">以冒號結束核取方塊標籤。</span><span class="sxs-lookup"><span data-stu-id="bbc62-222">End the check box label with a colon.</span></span>

    ![<span data-ttu-id="bbc62-223">下方核取方塊標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-223">screen shot of text box below check box label</span></span> ](images/ctrl-check-boxes-image18.png)

    <span data-ttu-id="bbc62-224">在此範例中，核取方塊和其從屬控制項共用核取方塊標籤及其存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="bbc62-224">In this example, the check box and its subordinate control share the check box label and its access key.</span></span>

-   <span data-ttu-id="bbc62-225">**如果相依的可編輯文字方塊和下拉式清單共用核取方塊的標籤，請將它保持啟用狀態。**</span><span class="sxs-lookup"><span data-stu-id="bbc62-225">**Leave dependent editable text boxes and drop-down lists enabled if they share the check box's label.**</span></span> <span data-ttu-id="bbc62-226">當使用者在方塊中輸入或貼上任何文字時，請自動選取對應的選項。</span><span class="sxs-lookup"><span data-stu-id="bbc62-226">When users type or paste anything into the box, select the corresponding option automatically.</span></span> <span data-ttu-id="bbc62-227">這麼做可簡化互動。</span><span class="sxs-lookup"><span data-stu-id="bbc62-227">Doing so simplifies the interaction.</span></span>

    ![<span data-ttu-id="bbc62-228">頁首和頁尾文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-228">screen shot of header and footer text boxes</span></span> ](images/ctrl-check-boxes-image19.png)

    <span data-ttu-id="bbc62-229">在此範例中，輸入頁首或頁尾會自動選取此選項。</span><span class="sxs-lookup"><span data-stu-id="bbc62-229">In this example, entering a header or footer automatically selects the option.</span></span>

-   <span data-ttu-id="bbc62-230">如果您使用選項按鈕或其他核取方塊來嵌套核取方塊，請 **停用這些次級控制項，直到選取高階選項為止**。</span><span class="sxs-lookup"><span data-stu-id="bbc62-230">If you nest check boxes with radio buttons or other check boxes, **disable these subordinate controls until the high-level option is selected**.</span></span> <span data-ttu-id="bbc62-231">這樣做可避免與從屬控制項的意義混淆。</span><span class="sxs-lookup"><span data-stu-id="bbc62-231">Doing so avoids confusion about the meaning of the subordinate controls.</span></span>
-   <span data-ttu-id="bbc62-232">使用定位順序中的核取方塊，將次級控制項設為連續的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-232">Make subordinate controls to a check box contiguous with the check box in the tab order.</span></span>
-   <span data-ttu-id="bbc62-233">**如果選取選項表示選取從屬核取方塊，請明確地選取這些核取方塊以使關聯性清楚。**</span><span class="sxs-lookup"><span data-stu-id="bbc62-233">**If selecting an option implies selecting subordinate check boxes, explicitly select those check boxes to make the relationship clear.**</span></span>

    <span data-ttu-id="bbc62-234">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-234">**Incorrect:**</span></span>

    ![<span data-ttu-id="bbc62-235">螢幕擷取畫面：選取的按鈕、已清除的核取方塊</span><span class="sxs-lookup"><span data-stu-id="bbc62-235">screen shot: selected button, cleared check boxes</span></span> ](images/ctrl-check-boxes-image20.png)

    <span data-ttu-id="bbc62-236">在此範例中，不會選取附屬核取方塊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-236">In this example, the subordinate check boxes aren't selected.</span></span>

    <span data-ttu-id="bbc62-237">**正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-237">**Correct:**</span></span>

    ![<span data-ttu-id="bbc62-238">螢幕擷取畫面：選取的按鈕，選取的核取方塊</span><span class="sxs-lookup"><span data-stu-id="bbc62-238">screen shot: selected button, selected check boxes</span></span> ](images/ctrl-check-boxes-image21.png)

    <span data-ttu-id="bbc62-239">在此範例中，會選取附屬核取方塊，使其與所選選項的關聯性為 clear。</span><span class="sxs-lookup"><span data-stu-id="bbc62-239">In this example, the subordinate check boxes are selected, making their relationship to the selected option clear.</span></span>

-   <span data-ttu-id="bbc62-240">**如果替代專案增加不必要的複雜性，請使用相依的核取方塊**。</span><span class="sxs-lookup"><span data-stu-id="bbc62-240">**Use dependent check boxes if the alternatives add unnecessary complexity**.</span></span> <span data-ttu-id="bbc62-241">雖然核取方塊應該是獨立的選項，有時其他的選項（例如選項按鈕）會增加不必要的複雜度。</span><span class="sxs-lookup"><span data-stu-id="bbc62-241">While check boxes should be independent options, sometimes alternatives such as radio buttons add unnecessary complexity.</span></span>

    <span data-ttu-id="bbc62-242">**正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-242">**Correct:**</span></span>

    ![<span data-ttu-id="bbc62-243">令人困惑的按鈕和核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-243">screen shot of confusing buttons and check boxes</span></span> ](images/ctrl-check-boxes-image22.png)

    <span data-ttu-id="bbc62-244">在此範例中，使用選項按鈕是正確的，但會產生不必要的複雜性。</span><span class="sxs-lookup"><span data-stu-id="bbc62-244">In this example, the use of radio buttons is accurate, but creates unnecessary complexity.</span></span>

    <span data-ttu-id="bbc62-245">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-245">**Better:**</span></span>

    ![<span data-ttu-id="bbc62-246">僅限核取方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-246">screen shot of check boxes only</span></span> ](images/ctrl-check-boxes-image23.png)

    <span data-ttu-id="bbc62-247">在此範例中，使用核取方塊比較簡單，而且可讓使用者專注于選取所需的選項，而不是其複雜的關聯性。</span><span class="sxs-lookup"><span data-stu-id="bbc62-247">In this example, the use of check boxes is simpler and allows users to focus on selecting the desired options instead of on their complex relationship.</span></span>

    <span data-ttu-id="bbc62-248">**重要事項：只有在極少數的情況下，才會在極罕見的情況下套用此指導** 方針。</span><span class="sxs-lookup"><span data-stu-id="bbc62-248">**Important: Apply this guideline only in extremely rare circumstances**, when showing the dependencies adds significant complexity without adding clarity.</span></span> <span data-ttu-id="bbc62-249">在上述範例中，使用者不太可能會嘗試選擇上標和注標，如果有的話，就很容易瞭解它們是專屬的選項。</span><span class="sxs-lookup"><span data-stu-id="bbc62-249">In the previous example, it is unlikely that users would attempt to choose both superscript and subscript, and if they did, it would be easy to understand that they were exclusive options.</span></span>

### <a name="default-values"></a><span data-ttu-id="bbc62-250">預設值</span><span class="sxs-lookup"><span data-stu-id="bbc62-250">Default values</span></span>

-   <span data-ttu-id="bbc62-251">如果核取方塊適用于使用者選項，請 **設定最安全的 (，以防止資料或系統存取) 、最安全和私用狀態的遺失。**</span><span class="sxs-lookup"><span data-stu-id="bbc62-251">If a check box is for a user option, **set the safest (to prevent loss of data or system access), most secure and private state by default.**</span></span> <span data-ttu-id="bbc62-252">如果安全性和安全性不是因素，請選取最有可能或方便的值。</span><span class="sxs-lookup"><span data-stu-id="bbc62-252">If safety and security aren't factors, select the most likely or convenient value.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="bbc62-253">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="bbc62-253">Recommended sizing and spacing</span></span>

![<span data-ttu-id="bbc62-254">建議的核取方塊調整大小和間距圖</span><span class="sxs-lookup"><span data-stu-id="bbc62-254">figure of suggested check box sizing and spacing</span></span> ](images/ctrl-check-boxes-image24.png)

<span data-ttu-id="bbc62-255">建議的核取方塊大小和間距。</span><span class="sxs-lookup"><span data-stu-id="bbc62-255">Recommended sizing and spacing for check boxes.</span></span>

## <a name="labels"></a><span data-ttu-id="bbc62-256">標籤</span><span class="sxs-lookup"><span data-stu-id="bbc62-256">Labels</span></span>

<span data-ttu-id="bbc62-257">**核取方塊標籤**</span><span class="sxs-lookup"><span data-stu-id="bbc62-257">**Check box labels**</span></span>

-   <span data-ttu-id="bbc62-258">標記每個核取方塊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-258">Label every check box.</span></span>
-   <span data-ttu-id="bbc62-259">將唯一的 [存取金鑰](glossary.md) 指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="bbc62-259">Assign a unique [access key](glossary.md) to each label.</span></span> <span data-ttu-id="bbc62-260">如需指導方針，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="bbc62-260">For guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="bbc62-261">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="bbc62-261">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="bbc62-262">以片語或命令式句子的形式寫入標籤，並不使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="bbc62-262">Write the label as a phrase or an imperative sentence, and use no ending punctuation.</span></span>
    -   <span data-ttu-id="bbc62-263">**例外狀況：** 如果核取方塊標籤也會標示其後的次級控制項，請以冒號結束標籤。</span><span class="sxs-lookup"><span data-stu-id="bbc62-263">**Exception:** If a check box label also labels a subordinate control that follows it, end the label with a colon.</span></span>
-   <span data-ttu-id="bbc62-264">寫入標籤，使其描述核取方塊的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="bbc62-264">Write the label so that it describes the selected state of the check box.</span></span>
-   <span data-ttu-id="bbc62-265">針對一組核取方塊，請使用平行片語，並嘗試保留所有標籤的相同長度。</span><span class="sxs-lookup"><span data-stu-id="bbc62-265">For a group of check boxes, use parallel phrasing and try to keep the length about the same for all labels.</span></span>
-   <span data-ttu-id="bbc62-266">針對一組核取方塊，請將標籤文字放在選項之間的差異。</span><span class="sxs-lookup"><span data-stu-id="bbc62-266">For a group of check boxes, focus the label text on the differences among the options.</span></span> <span data-ttu-id="bbc62-267">如果所有選項都有相同的簡介文字，請將該文字移至群組標籤。</span><span class="sxs-lookup"><span data-stu-id="bbc62-267">If all the options have the same introductory text, move that text to the group label.</span></span>
-   <span data-ttu-id="bbc62-268">使用正片語。</span><span class="sxs-lookup"><span data-stu-id="bbc62-268">Use positive phrasing.</span></span> <span data-ttu-id="bbc62-269">請勿將標籤加上標籤，以便選取核取方塊，表示不執行動作。</span><span class="sxs-lookup"><span data-stu-id="bbc62-269">Don't phrase a label so that selecting a check box means not to perform an action.</span></span>

    -   <span data-ttu-id="bbc62-270">**例外狀況：不要 <item> 再顯示** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-270">**Exception:Don't show this <item> again** check boxes.</span></span>

    <span data-ttu-id="bbc62-271">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-271">**Incorrect:**</span></span>

    ![負標籤 [關閉] 的螢幕擷取畫面](images/ctrl-check-boxes-image25.png)

    <span data-ttu-id="bbc62-273">在此範例中，選項不會使用正片語。</span><span class="sxs-lookup"><span data-stu-id="bbc62-273">In this example, the option doesn't use positive phrasing.</span></span>

-   <span data-ttu-id="bbc62-274">只描述標籤的選項。</span><span class="sxs-lookup"><span data-stu-id="bbc62-274">Describe just the option with the label.</span></span> <span data-ttu-id="bbc62-275">將標籤保持簡短，讓您可以輕鬆地在訊息和檔中參考它們。</span><span class="sxs-lookup"><span data-stu-id="bbc62-275">Keep labels brief so it's easy to refer to them in messages and documentation.</span></span> <span data-ttu-id="bbc62-276">如果選項需要進一步說明，請使用完整的句子和結束標點符號在 [靜態文字](./glossary.md) 控制項中提供說明。</span><span class="sxs-lookup"><span data-stu-id="bbc62-276">If the option requires further explanation, provide the explanation in a [static text](./glossary.md) control using complete sentences and ending punctuation.</span></span>

    > [!Note]
    >
    > <span data-ttu-id="bbc62-277">將說明新增至群組中的一個核取方塊，並不表示您必須為群組中的所有核取方塊提供說明。</span><span class="sxs-lookup"><span data-stu-id="bbc62-277">Adding an explanation to one check box in a group doesn't mean that you have to provide explanations for all check boxes in the group.</span></span> <span data-ttu-id="bbc62-278">如果您可以的話，請在標籤中提供相關資訊，並且只在必要時使用說明。</span><span class="sxs-lookup"><span data-stu-id="bbc62-278">Provide the relevant information in the label if you can, and use explanations only when necessary.</span></span> <span data-ttu-id="bbc62-279">請勿只重新聲明標籤以保持一致性。</span><span class="sxs-lookup"><span data-stu-id="bbc62-279">Don't merely restate the label for consistency.</span></span>

     

    ![<span data-ttu-id="bbc62-280">核取方塊、標籤和描述的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-280">screen shot of checkbox, label, and description</span></span> ](images/ctrl-check-boxes-image26.png)

    <span data-ttu-id="bbc62-281">在此範例中，核取方塊標籤底下會有其他的解說文字。</span><span class="sxs-lookup"><span data-stu-id="bbc62-281">In this example, a check box label has additional explanatory text beneath it.</span></span>

-   <span data-ttu-id="bbc62-282">如果強烈建議選項，請考慮將「 (建議的) 」新增至標籤。</span><span class="sxs-lookup"><span data-stu-id="bbc62-282">If an option is strongly recommended, consider adding "(recommended)" to the label.</span></span> <span data-ttu-id="bbc62-283">請務必新增至控制項標籤，而不是增補附注。</span><span class="sxs-lookup"><span data-stu-id="bbc62-283">Be sure to add to the control label, not the supplemental notes.</span></span>
-   <span data-ttu-id="bbc62-284">如果您必須使用多行標籤，請將標籤的頂端與核取方塊對齊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-284">If you must use multi-line labels, align the top of the label with the check box.</span></span>
-   <span data-ttu-id="bbc62-285">請勿使用從屬控制項、它所包含的值，或其單位標籤來建立句子或片語。</span><span class="sxs-lookup"><span data-stu-id="bbc62-285">Don't use a subordinate control, the values it contains, or its units label to create a sentence or phrase.</span></span> <span data-ttu-id="bbc62-286">這類設計無法當地語系化，因為句子結構會隨著語言而有所不同。</span><span class="sxs-lookup"><span data-stu-id="bbc62-286">Such a design isn't localizable because sentence structure varies with language.</span></span>

    <span data-ttu-id="bbc62-287">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-287">**Incorrect:**</span></span>

    ![<span data-ttu-id="bbc62-288">包含文字方塊之核取方塊標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="bbc62-288">screen shot of checkbox label with text box in it</span></span> ](images/ctrl-check-boxes-image27.png)

    <span data-ttu-id="bbc62-289">在此範例中，文字方塊不正確地放在核取方塊標籤內。</span><span class="sxs-lookup"><span data-stu-id="bbc62-289">In this example, the text box is incorrectly placed inside the check box label.</span></span>

<span data-ttu-id="bbc62-290">**核取方塊群組標籤**</span><span class="sxs-lookup"><span data-stu-id="bbc62-290">**Check box group labels**</span></span>

-   <span data-ttu-id="bbc62-291">使用群組標籤來說明群組的用途，而不是如何進行選取。</span><span class="sxs-lookup"><span data-stu-id="bbc62-291">Use the group label to explain the purpose of the group, not how to make the selection.</span></span> <span data-ttu-id="bbc62-292">假設使用者知道如何使用核取方塊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-292">Assume that users know how to use check boxes.</span></span> <span data-ttu-id="bbc62-293">例如，不要說「選取下列任何選項」。</span><span class="sxs-lookup"><span data-stu-id="bbc62-293">For example, don't say "Select any of the following choices".</span></span>
-   <span data-ttu-id="bbc62-294">以冒號結束每個標籤。</span><span class="sxs-lookup"><span data-stu-id="bbc62-294">End each label with a colon.</span></span>
-   <span data-ttu-id="bbc62-295">請勿指派標籤的存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="bbc62-295">Don't assign an access key to the label.</span></span> <span data-ttu-id="bbc62-296">這並不是必要的，而是讓其他存取金鑰更難指派。</span><span class="sxs-lookup"><span data-stu-id="bbc62-296">Doing so isn't necessary and it makes the other access keys harder to assign.</span></span>
-   <span data-ttu-id="bbc62-297">若要選取一或多個相依選項，請說明標籤上的需求。</span><span class="sxs-lookup"><span data-stu-id="bbc62-297">For a selection of one or more dependent choices, explain the requirement on the label.</span></span>

    <span data-ttu-id="bbc62-298">**正確：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-298">**Correct:**</span></span>

    ![<span data-ttu-id="bbc62-299">兩個控制項標籤的螢幕擷取畫面：通訊協定</span><span class="sxs-lookup"><span data-stu-id="bbc62-299">screen shot of label for two controls: protocols</span></span> ](images/ctrl-check-boxes-image28.png)

    <span data-ttu-id="bbc62-300">在此範例中，使用者可能會認為他們只能進行一個選取。</span><span class="sxs-lookup"><span data-stu-id="bbc62-300">In this example, users might think that they can only make one selection.</span></span>

    <span data-ttu-id="bbc62-301">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="bbc62-301">**Better:**</span></span>

    ![<span data-ttu-id="bbc62-302">標籤的螢幕擷取畫面：選取一或多個通訊協定</span><span class="sxs-lookup"><span data-stu-id="bbc62-302">screen shot of label: protocols select one or more</span></span> ](images/ctrl-check-boxes-image29.png)

    <span data-ttu-id="bbc62-303">在此範例中，使用者可以選擇是否要進行一個以上的選擇。</span><span class="sxs-lookup"><span data-stu-id="bbc62-303">In this example, it's clear that users can make more than one selection.</span></span>

## <a name="documentation"></a><span data-ttu-id="bbc62-304">文件</span><span class="sxs-lookup"><span data-stu-id="bbc62-304">Documentation</span></span>

<span data-ttu-id="bbc62-305">參考核取方塊時：</span><span class="sxs-lookup"><span data-stu-id="bbc62-305">When referring to check boxes:</span></span>

-   <span data-ttu-id="bbc62-306">使用確切的標籤文字，包括其大小寫，但不包含存取金鑰底線或冒號。</span><span class="sxs-lookup"><span data-stu-id="bbc62-306">Use the exact label text, including its capitalization, but don't include the access key underscore or colon.</span></span> <span data-ttu-id="bbc62-307">包含 [單字] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-307">Include the word check box.</span></span>
-   <span data-ttu-id="bbc62-308">請將核取方塊稱為核取方塊，而不是 [選項]、[核取方塊] 或 [僅限 box]，因為對於當地語系化人員來說，box 並不明確。</span><span class="sxs-lookup"><span data-stu-id="bbc62-308">Refer to a check box as a check box, not option, checkbox, or just box, because box alone is ambiguous for localizers.</span></span>
-   <span data-ttu-id="bbc62-309">若要描述使用者互動，請使用選取和清除。</span><span class="sxs-lookup"><span data-stu-id="bbc62-309">To describe user interaction, use select and clear.</span></span>
-   <span data-ttu-id="bbc62-310">可能的話，請使用粗體文字來格式化標籤。</span><span class="sxs-lookup"><span data-stu-id="bbc62-310">When possible, format the label using bold text.</span></span> <span data-ttu-id="bbc62-311">否則，請只在必要時才將標籤放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="bbc62-311">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="bbc62-312">範例： **選取 [底線** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="bbc62-312">Example: Select the **Underline** check box.</span></span>

