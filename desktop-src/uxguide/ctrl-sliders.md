---
title: " (設計基本概念的滑杆) "
description: 使用滑杆時，使用者可以從連續的值範圍中選擇。
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ff9791ab49c338e4c11e014a3e996771571add9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104560792"
---
# <a name="sliders-design-basics"></a><span data-ttu-id="07c2f-103"> (設計基本概念的滑杆) </span><span class="sxs-lookup"><span data-stu-id="07c2f-103">Sliders (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="07c2f-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="07c2f-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="07c2f-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="07c2f-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="07c2f-106">使用滑杆時，使用者可以從連續的值範圍中選擇。</span><span class="sxs-lookup"><span data-stu-id="07c2f-106">With a slider, users can choose from a continuous range of values.</span></span> <span data-ttu-id="07c2f-107">滑杆具有顯示範圍的橫條，以及顯示目前值的指標。</span><span class="sxs-lookup"><span data-stu-id="07c2f-107">A slider has a bar that shows the range and an indicator that shows the current value.</span></span> <span data-ttu-id="07c2f-108">選擇性刻度會顯示值。</span><span class="sxs-lookup"><span data-stu-id="07c2f-108">Optional tick marks show values.</span></span>

![<span data-ttu-id="07c2f-109">顯示橫條圖、滑杆和刻度的圖表</span><span class="sxs-lookup"><span data-stu-id="07c2f-109">figure showing bar, slider, and tick marks</span></span> ](images/ctrl-sliders-image1.png)

<span data-ttu-id="07c2f-110">一般滑杆。</span><span class="sxs-lookup"><span data-stu-id="07c2f-110">A typical slider.</span></span>

> [!Note]  
> <span data-ttu-id="07c2f-111">與 [版面](vis-layout.md) 配置相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="07c2f-111">Guidelines related to [layout](vis-layout.md) are presented in a separate article.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="07c2f-112">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="07c2f-112">Is this the right control?</span></span>

<span data-ttu-id="07c2f-113">當您想要讓使用者能夠 **設定已定義、連續的值 (例如音量或亮度) 或某個範圍的離散值 (例如螢幕解析度設定) 時，** 請使用滑杆。</span><span class="sxs-lookup"><span data-stu-id="07c2f-113">Use a slider when you want your users to be able to **set defined, contiguous values (such as volume or brightness) or a range of discrete values (such as screen resolution settings).**</span></span>

<span data-ttu-id="07c2f-114">當您知道使用者將值視為相對數量而不是數字值時，滑桿是很好的選擇。</span><span class="sxs-lookup"><span data-stu-id="07c2f-114">A slider is a good choice when you know that users think of the value as a relative quantity, not a numeric value.</span></span> <span data-ttu-id="07c2f-115">例如，使用者想要將音訊音量設定為低或中，而不是設定值為 2 或 5。</span><span class="sxs-lookup"><span data-stu-id="07c2f-115">For example, users think about setting their audio volume to low or medium—not about setting the value to 2 or 5.</span></span>

<span data-ttu-id="07c2f-116">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="07c2f-116">To decide, consider these questions:</span></span>

-   <span data-ttu-id="07c2f-117">**設定看起來是否像相對數量？**</span><span class="sxs-lookup"><span data-stu-id="07c2f-117">**Does the setting seem like a relative quantity?**</span></span> <span data-ttu-id="07c2f-118">如果沒有，請使用[選項按鈕](ctrl-radio-buttons.md)，或[下拉式](/windows/desktop/uxguide/ctrl-drop)[清單或單一選取清單](ctrl-list-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="07c2f-118">If not, use [radio buttons](ctrl-radio-buttons.md), or a [drop-down](/windows/desktop/uxguide/ctrl-drop) or [single-selection list](ctrl-list-boxes.md).</span></span>
-   <span data-ttu-id="07c2f-119">**該設定是否為已知的確切數值？**</span><span class="sxs-lookup"><span data-stu-id="07c2f-119">**Is the setting an exact, known numeric value?**</span></span> <span data-ttu-id="07c2f-120">如果是的話，請使用 [數值文字方塊](ctrl-text-boxes.md)。</span><span class="sxs-lookup"><span data-stu-id="07c2f-120">If so, use a [numeric text boxes](ctrl-text-boxes.md).</span></span>
-   <span data-ttu-id="07c2f-121">**在變更設定時，獲得即時回應的效果是否為使用者帶來益處？**</span><span class="sxs-lookup"><span data-stu-id="07c2f-121">**Would a user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="07c2f-122">如果是，請使用滑桿。</span><span class="sxs-lookup"><span data-stu-id="07c2f-122">If so, use a slider.</span></span> <span data-ttu-id="07c2f-123">例如，藉由立即看到色調、飽和或光度值變更後的效果，能讓使用者更易於選擇色彩。</span><span class="sxs-lookup"><span data-stu-id="07c2f-123">For example, users can choose a color more easily by immediately seeing the effect of changes to hue, saturation, or luminosity values.</span></span>
-   <span data-ttu-id="07c2f-124">**設定的範圍是否包含四個或更多值？**</span><span class="sxs-lookup"><span data-stu-id="07c2f-124">**Does the setting have a range of four or more values?**</span></span> <span data-ttu-id="07c2f-125">如果不是，請使用選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="07c2f-125">If not, use radio buttons.</span></span>
-   <span data-ttu-id="07c2f-126">**使用者是否能變更該值？**</span><span class="sxs-lookup"><span data-stu-id="07c2f-126">**Can the user change the value?**</span></span> <span data-ttu-id="07c2f-127">滑桿的用意是提供使用者互動。</span><span class="sxs-lookup"><span data-stu-id="07c2f-127">Sliders are for user interaction.</span></span> <span data-ttu-id="07c2f-128">如果使用者無法變更該值，請改用唯讀 [文字方塊](ctrl-text-boxes.md) 。</span><span class="sxs-lookup"><span data-stu-id="07c2f-128">If a user can't ever change the value, use a read-only [text box](ctrl-text-boxes.md) instead.</span></span>

<span data-ttu-id="07c2f-129">如果可以有滑杆或數值文字方塊，請在下列情況下使用數值文字方塊：</span><span class="sxs-lookup"><span data-stu-id="07c2f-129">If a slider or a numeric text box is possible, use a numeric text box if:</span></span>

-   <span data-ttu-id="07c2f-130">螢幕空間很小。</span><span class="sxs-lookup"><span data-stu-id="07c2f-130">Screen space is tight.</span></span>
-   <span data-ttu-id="07c2f-131">使用者很可能會偏好使用鍵盤。</span><span class="sxs-lookup"><span data-stu-id="07c2f-131">A user is likely to prefer using the keyboard.</span></span>

<span data-ttu-id="07c2f-132">如果是下列情況，請使用滑桿：</span><span class="sxs-lookup"><span data-stu-id="07c2f-132">Use a slider if:</span></span>

-   <span data-ttu-id="07c2f-133">使用者可受益於立即回應。</span><span class="sxs-lookup"><span data-stu-id="07c2f-133">Users will benefit from instant feedback.</span></span>

## <a name="guidelines"></a><span data-ttu-id="07c2f-134">指導方針</span><span class="sxs-lookup"><span data-stu-id="07c2f-134">Guidelines</span></span>

-   <span data-ttu-id="07c2f-135">**使用原有的方向。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-135">**Use a natural orientation.**</span></span> <span data-ttu-id="07c2f-136">例如，如果滑桿表示真實世界中通常會垂直顯示的值 (例如溫度)，請使用垂直方向。</span><span class="sxs-lookup"><span data-stu-id="07c2f-136">For example, if the slider represents a real-world value that is normally shown vertically (such as temperature), use a vertical orientation.</span></span>
-   <span data-ttu-id="07c2f-137">**引導滑杆以反映使用者的文化特性。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-137">**Orient the slider to reflect the culture of your users.**</span></span> <span data-ttu-id="07c2f-138">例如，從左至右讀取的西方文化特性，因此針對水準滑杆，將範圍的下限放在左側，並將右端放置於右邊。</span><span class="sxs-lookup"><span data-stu-id="07c2f-138">For example, Western cultures read from left to right, so for horizontal sliders, put the low end of the range on the left and the high end on the right.</span></span> <span data-ttu-id="07c2f-139">針對從右至左讀取的文化特性，請反向操作。</span><span class="sxs-lookup"><span data-stu-id="07c2f-139">For cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="07c2f-140">**調整控制項的大小，讓使用者可以輕鬆地設定所需的值。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-140">**Size the control so that a user can easily set the desired value.**</span></span> <span data-ttu-id="07c2f-141">設定分散值時，確定使用者可輕鬆地使用滑鼠選取任何值。</span><span class="sxs-lookup"><span data-stu-id="07c2f-141">For settings with discrete values, make sure the user can easily select any value using the mouse.</span></span>
-   <span data-ttu-id="07c2f-142">**如果值範圍很大，而且使用者可能會在範圍的一端選取值，請考慮使用非線性尺規。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-142">**Consider using a non-linear scale if the range of values is large and users will likely select values at one end of the range.**</span></span> <span data-ttu-id="07c2f-143">例如，時間值可能是1分鐘、1小時、1天或1個月。</span><span class="sxs-lookup"><span data-stu-id="07c2f-143">For example, time value might be 1 minute, 1 hour, 1 day, or 1 month.</span></span>
-   <span data-ttu-id="07c2f-144">**只要可行，就能在使用者進行選取時，立即提供意見反應。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-144">**Whenever practical, give immediate feedback while or after a user makes a selection.**</span></span> <span data-ttu-id="07c2f-145">例如，Microsoft Windows volume control 會發出嗶聲，以表示產生的音訊音量。</span><span class="sxs-lookup"><span data-stu-id="07c2f-145">For example, the Microsoft Windows volume control beeps to indicate the resulting audio volume.</span></span>
-   <span data-ttu-id="07c2f-146">**使用標籤顯示值的範圍。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-146">**Use labels to show the range of values.**</span></span>

    <span data-ttu-id="07c2f-147">**例外狀況：** 如果滑杆是垂直方向，而且頂端標籤是 [最大值]、[高]、[更多] 或 [相等]，您可以省略其他標籤，因為意義是明確的。</span><span class="sxs-lookup"><span data-stu-id="07c2f-147">**Exception:** If the slider is vertically oriented and the top label is Maximum, High, More, or equivalent, you can omit the other labels since the meaning is clear.</span></span>

    ![<span data-ttu-id="07c2f-148">垂直滑杆的圖</span><span class="sxs-lookup"><span data-stu-id="07c2f-148">figure of a vertical slider</span></span> ](images/ctrl-sliders-image2.png)

    <span data-ttu-id="07c2f-149">在此範例中，滑杆的垂直方向會讓範圍標籤不需要。</span><span class="sxs-lookup"><span data-stu-id="07c2f-149">In this example, the slider's vertical orientation makes the range labels unnecessary.</span></span>

-   <span data-ttu-id="07c2f-150">**當使用者需要知道設定的近似值時，請使用刻度標記。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-150">**Use tick marks when users need to know the approximate value of the setting.**</span></span>
-   <span data-ttu-id="07c2f-151">**當使用者需要知道他們所選擇之設定的確切值時，請使用刻度和值標籤。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-151">**Use tick marks and a value label when users need to know the exact value of the setting they choose.**</span></span> <span data-ttu-id="07c2f-152">如果使用者需要知道要設定的單位，請一律使用值標籤。</span><span class="sxs-lookup"><span data-stu-id="07c2f-152">Always use a value label if a user needs to know the units to make sense of the setting.</span></span>

    ![<span data-ttu-id="07c2f-153">顯示所選圖元數的滑杆圖</span><span class="sxs-lookup"><span data-stu-id="07c2f-153">figure of slider showing number of pixels selected</span></span> ](images/ctrl-sliders-image3.png)

    <span data-ttu-id="07c2f-154">在此範例中，標籤是用來清楚指出選取的值。</span><span class="sxs-lookup"><span data-stu-id="07c2f-154">In this example, a label is used to clearly indicate the selected value.</span></span>

-   <span data-ttu-id="07c2f-155">**若為水準方向的滑杆，請將刻度標記放在滑杆下方。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-155">**For horizontally-oriented sliders, place tick marks under the slider.**</span></span> <span data-ttu-id="07c2f-156">如果是垂直方向的滑杆，請將右上角的刻度放置於西方文化特性的右邊;針對從右至左讀取的文化特性，請反向操作。</span><span class="sxs-lookup"><span data-stu-id="07c2f-156">For vertically-oriented sliders, place tick marks to the right for Western cultures; for cultures that read from right to left, do the opposite.</span></span>
-   <span data-ttu-id="07c2f-157">**將 [值] 標籤完全放在滑杆控制項底下，以便清楚關聯性。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-157">**Place the value label completely under the slider control so that the relationship is clear.**</span></span>

    <span data-ttu-id="07c2f-158">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="07c2f-158">**Incorrect:**</span></span>

    ![<span data-ttu-id="07c2f-159">長度超過其滑杆的標籤圖</span><span class="sxs-lookup"><span data-stu-id="07c2f-159">figure of a label that is longer than its slider</span></span> ](images/ctrl-sliders-image4.png)

    <span data-ttu-id="07c2f-160">在此範例中，[值] 標籤不會對齊滑杆下方。</span><span class="sxs-lookup"><span data-stu-id="07c2f-160">In this example, the value label isn't aligned under the slider.</span></span>

-   <span data-ttu-id="07c2f-161">**停用滑杆時，也會停用任何相關聯的標籤。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-161">**When disabling a slider, also disable any associated labels.**</span></span>
-   <span data-ttu-id="07c2f-162">**針對相同的設定，請勿同時使用滑杆和數值文字方塊。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-162">**Don't use both a slider and a numeric text box for the same setting.**</span></span> <span data-ttu-id="07c2f-163">只使用更適當的控制項。</span><span class="sxs-lookup"><span data-stu-id="07c2f-163">Use only the more appropriate control.</span></span>

    <span data-ttu-id="07c2f-164">**例外狀況：** 當使用者同時需要立即意見反應和設定確切數值的能力時，請使用這兩個控制項。</span><span class="sxs-lookup"><span data-stu-id="07c2f-164">**Exception:** Use both controls when the user needs both immediate feedback and the ability to set an exact numeric value.</span></span>

-   <span data-ttu-id="07c2f-165">**不要使用滑桿做為進度指示器。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-165">**Don't use a slider as a progress indicator.**</span></span>
-   <span data-ttu-id="07c2f-166">**請勿從預設大小變更滑杆指標的大小。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-166">**Don't change the size of the slider indicator from the default size.**</span></span>

    <span data-ttu-id="07c2f-167">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="07c2f-167">**Incorrect:**</span></span>

    ![<span data-ttu-id="07c2f-168">小於預設值的滑杆圖</span><span class="sxs-lookup"><span data-stu-id="07c2f-168">figure of slider that is smaller than the default</span></span> ](images/ctrl-sliders-image5.png)

    <span data-ttu-id="07c2f-169">在此範例中，會使用小於預設值的大小。</span><span class="sxs-lookup"><span data-stu-id="07c2f-169">In this example, a size smaller than the default is used.</span></span>

    <span data-ttu-id="07c2f-170">**正確：**</span><span class="sxs-lookup"><span data-stu-id="07c2f-170">**Correct:**</span></span>

    ![<span data-ttu-id="07c2f-171">顯示預設滑杆的圖</span><span class="sxs-lookup"><span data-stu-id="07c2f-171">figure showing the default slider</span></span> ](images/ctrl-sliders-image6.png)

    <span data-ttu-id="07c2f-172">在此範例中，會使用預設大小。</span><span class="sxs-lookup"><span data-stu-id="07c2f-172">In this example, the default size is used.</span></span>

-   <span data-ttu-id="07c2f-173">**請勿標記每個刻度。**</span><span class="sxs-lookup"><span data-stu-id="07c2f-173">**Don't label every tick mark.**</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="07c2f-174">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="07c2f-174">Recommended sizing and spacing</span></span>

![<span data-ttu-id="07c2f-175">建議的滑杆調整大小和間距圖</span><span class="sxs-lookup"><span data-stu-id="07c2f-175">figure of recommended slider sizing and spacing</span></span> ](images/ctrl-sliders-image7.png)

<span data-ttu-id="07c2f-176">建議的調整大小和滑杆間距。</span><span class="sxs-lookup"><span data-stu-id="07c2f-176">Recommended sizing and spacing for sliders.</span></span>

## <a name="labels"></a><span data-ttu-id="07c2f-177">標籤</span><span class="sxs-lookup"><span data-stu-id="07c2f-177">Labels</span></span>

### <a name="slider-labels"></a><span data-ttu-id="07c2f-178">滑桿標籤</span><span class="sxs-lookup"><span data-stu-id="07c2f-178">Slider labels</span></span>

-   <span data-ttu-id="07c2f-179">使用以冒號結尾的靜態文字標籤，或不含結尾標點符號的群組方塊標籤。</span><span class="sxs-lookup"><span data-stu-id="07c2f-179">Use a static text label ending with a colon, or a group box label with no ending punctuation.</span></span>
-   <span data-ttu-id="07c2f-180">將唯一的存取金鑰指派給每個標籤。</span><span class="sxs-lookup"><span data-stu-id="07c2f-180">Assign a unique access key to each label.</span></span> <span data-ttu-id="07c2f-181">如需指派指導方針，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="07c2f-181">For assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="07c2f-182">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="07c2f-182">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="07c2f-183">將滑杆標籤放在滑動軸的左邊，或對齊滑杆的左邊緣 (或左邊的範圍識別碼（如果有) 的話）。</span><span class="sxs-lookup"><span data-stu-id="07c2f-183">Position the slider label either to the left of the slider, or above and aligned with the left edge of the slider (or its left range identifier, if present).</span></span>

### <a name="range-labels"></a><span data-ttu-id="07c2f-184">範圍標籤</span><span class="sxs-lookup"><span data-stu-id="07c2f-184">Range labels</span></span>

-   <span data-ttu-id="07c2f-185">在滑桿範圍的兩端建立標籤，如果是垂直方向，則不需要建立標籤。</span><span class="sxs-lookup"><span data-stu-id="07c2f-185">Label the two ends of the slider range, unless a vertical orientation makes this unnecessary.</span></span>
-   <span data-ttu-id="07c2f-186">針對每個標籤僅使用單字（如果可能的話）。</span><span class="sxs-lookup"><span data-stu-id="07c2f-186">Use only word, if possible, for each label.</span></span>
-   <span data-ttu-id="07c2f-187">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="07c2f-187">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="07c2f-188">確定這些標籤為描述性文字，而且平行放置。</span><span class="sxs-lookup"><span data-stu-id="07c2f-188">Make sure these labels are descriptive and parallel.</span></span> <span data-ttu-id="07c2f-189">範例：最大/最小、多/少、低/高、小聲/大聲。</span><span class="sxs-lookup"><span data-stu-id="07c2f-189">Examples: Maximum/Minimum, More/Less, Low/High, Soft/Loud.</span></span>
-   <span data-ttu-id="07c2f-190">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="07c2f-190">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="07c2f-191">請勿指派存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="07c2f-191">Don't assign access keys.</span></span>

### <a name="value-labels"></a><span data-ttu-id="07c2f-192">值標籤</span><span class="sxs-lookup"><span data-stu-id="07c2f-192">Value labels</span></span>

-   <span data-ttu-id="07c2f-193">如果您需要值標籤，請將它顯示在滑桿下方。</span><span class="sxs-lookup"><span data-stu-id="07c2f-193">If you need a value label, display it below the slider.</span></span>
-   <span data-ttu-id="07c2f-194">把文字放在與控制項相對的位置中間並包括單位 (例如像素)。</span><span class="sxs-lookup"><span data-stu-id="07c2f-194">Center the text relative to the control and include the units (such as pixels).</span></span>

    ![<span data-ttu-id="07c2f-195">位於滑杆下方的標籤圖</span><span class="sxs-lookup"><span data-stu-id="07c2f-195">figure of label centered under the slider</span></span> ](images/ctrl-sliders-image8.png)

    <span data-ttu-id="07c2f-196">在此範例中，[值] 標籤位於滑杆的中央，並包含單位。</span><span class="sxs-lookup"><span data-stu-id="07c2f-196">In this example, the value label is centered under the slider and includes the units.</span></span>

## <a name="documentation"></a><span data-ttu-id="07c2f-197">文件</span><span class="sxs-lookup"><span data-stu-id="07c2f-197">Documentation</span></span>

<span data-ttu-id="07c2f-198">參考滑杆時：</span><span class="sxs-lookup"><span data-stu-id="07c2f-198">When referring to sliders:</span></span>

-   <span data-ttu-id="07c2f-199">使用確切的標籤文字（包含其大小寫），並包含文字滑杆。</span><span class="sxs-lookup"><span data-stu-id="07c2f-199">Use the exact label text, including its capitalization, and include the word slider.</span></span> <span data-ttu-id="07c2f-200">請勿包含存取金鑰底線或冒號。</span><span class="sxs-lookup"><span data-stu-id="07c2f-200">Don't include the access key underscore or colon.</span></span>
-   <span data-ttu-id="07c2f-201">若要描述使用者互動，請使用 move。</span><span class="sxs-lookup"><span data-stu-id="07c2f-201">To describe user interaction, use move.</span></span>
-   <span data-ttu-id="07c2f-202">可能的話，請使用粗體文字來格式化標籤。</span><span class="sxs-lookup"><span data-stu-id="07c2f-202">When possible, format the label using bold text.</span></span> <span data-ttu-id="07c2f-203">否則，請只在必要時才將標籤放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="07c2f-203">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="07c2f-204">範例：若要增加螢幕解析度，請將 **螢幕解析度** 滑杆向右移動。</span><span class="sxs-lookup"><span data-stu-id="07c2f-204">Example: To increase your screen resolution, move the **Screen resolution** slider to the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07c2f-205">相關主題</span><span class="sxs-lookup"><span data-stu-id="07c2f-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07c2f-206">詞彙</span><span class="sxs-lookup"><span data-stu-id="07c2f-206">Glossary</span></span>](glossary.md)
</dt> </dl>

 

 