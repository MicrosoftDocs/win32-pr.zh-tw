---
title: 文字方塊
description: 使用文字方塊時，使用者可以顯示、輸入或編輯文字或數值。
ms.assetid: fb8ed262-1451-496d-a3f4-a29af39763bb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 2b5257e9772465f26815abb0f6ecbe0ff357ba4b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104514284"
---
# <a name="text-boxes"></a><span data-ttu-id="66c7d-103">文字方塊</span><span class="sxs-lookup"><span data-stu-id="66c7d-103">Text Boxes</span></span>

> [!NOTE]
> <span data-ttu-id="66c7d-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="66c7d-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="66c7d-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="66c7d-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="66c7d-106">使用文字方塊時，使用者可以顯示、輸入或編輯文字或數值。</span><span class="sxs-lookup"><span data-stu-id="66c7d-106">With a text box, users can display, enter, or edit a text or numeric value.</span></span>

![<span data-ttu-id="66c7d-107">一般文字方塊和標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-107">screen shot of a typical text box and label</span></span> ](images/ctrl-text-boxes-image1.png)

<span data-ttu-id="66c7d-108">標準的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-108">A typical text box.</span></span>

> [!Note]  
> <span data-ttu-id="66c7d-109">與[版面](vis-layout.md)[配置、字型和](vis-fonts.md)[氣球](ctrl-balloons.md)相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="66c7d-109">Guidelines related to [layout](vis-layout.md), [fonts](vis-fonts.md), and [balloons](ctrl-balloons.md) are presented in separate articles.</span></span>

 

## <a name="is-this-the-right-control"></a><span data-ttu-id="66c7d-110">這是正確的控制項嗎？</span><span class="sxs-lookup"><span data-stu-id="66c7d-110">Is this the right control?</span></span>

<span data-ttu-id="66c7d-111">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="66c7d-111">To decide, consider these questions:</span></span>

-   <span data-ttu-id="66c7d-112">**有效列舉所有有效的值是否可行？**</span><span class="sxs-lookup"><span data-stu-id="66c7d-112">**Is it practical to enumerate all the valid values efficiently?**</span></span> <span data-ttu-id="66c7d-113">如果是的話，請考慮使用 [單一選取清單](ctrl-list-boxes.md)、 [清單視圖](ctrl-list-views.md)、 [下拉式清單](/windows/desktop/uxguide/ctrl-drop)、可編輯的下拉式清單或 [滑杆](ctrl-sliders.md) 。</span><span class="sxs-lookup"><span data-stu-id="66c7d-113">If so, consider a [single-selection list](ctrl-list-boxes.md), [list view](ctrl-list-views.md), [drop-down list](/windows/desktop/uxguide/ctrl-drop), editable drop-down list, or [slider](ctrl-sliders.md) instead.</span></span>
-   <span data-ttu-id="66c7d-114">**有效的資料是否完全不受限制？或者，有效的資料僅受限於)  (限制長度或字元類型的格式？**</span><span class="sxs-lookup"><span data-stu-id="66c7d-114">**Is the valid data completely unconstrained? Or is the valid data constrained only by format (constrained length or character types)?**</span></span> <span data-ttu-id="66c7d-115">如果是的話，請使用文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-115">If so, use a text box.</span></span>
-   <span data-ttu-id="66c7d-116">**該值代表的資料類型是否已經有特殊的通用控制項？**</span><span class="sxs-lookup"><span data-stu-id="66c7d-116">**Does the value represent a data type that has a specialized common control?**</span></span> <span data-ttu-id="66c7d-117">範例包括日期、時間或 IPv4 或 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="66c7d-117">Examples include date, time, or IPv4 or IPv6 address.</span></span> <span data-ttu-id="66c7d-118">如果是的話，請使用適當的控制項，例如日期控制項，而不是文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-118">If so, use the appropriate control, such as a date control rather than a text box.</span></span>
-   <span data-ttu-id="66c7d-119">如果資料為數值：</span><span class="sxs-lookup"><span data-stu-id="66c7d-119">If the data is numeric:</span></span>
    -   <span data-ttu-id="66c7d-120">**使用者是否會將設定視為相對數量？**</span><span class="sxs-lookup"><span data-stu-id="66c7d-120">**Do users perceive the setting as a relative quantity?**</span></span> <span data-ttu-id="66c7d-121">如果是，請使用滑桿。</span><span class="sxs-lookup"><span data-stu-id="66c7d-121">If so, use a slider.</span></span>
    -   <span data-ttu-id="66c7d-122">**在變更設定時，獲得即時回應的效果是否為使用者帶來益處？**</span><span class="sxs-lookup"><span data-stu-id="66c7d-122">**Would the user benefit from instant feedback on the effect of setting changes?**</span></span> <span data-ttu-id="66c7d-123">如果是的話，請使用滑杆，可能與文字方塊一起使用。</span><span class="sxs-lookup"><span data-stu-id="66c7d-123">If so, use a slider, possibly along with a text box.</span></span> <span data-ttu-id="66c7d-124">例如，使用者可以輕鬆地選擇使用滑杆的色彩，因為它們可以立即看到變更色調、飽和度或亮度值的效果。</span><span class="sxs-lookup"><span data-stu-id="66c7d-124">For example, users can easily choose a color using a slider because they can immediately see the effect of changes to hue, saturation, or luminosity values.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="66c7d-125">設計概念</span><span class="sxs-lookup"><span data-stu-id="66c7d-125">Design concepts</span></span>

<span data-ttu-id="66c7d-126">雖然文字方塊具有極具彈性的優點，但是具有最基本條件約束的缺點。</span><span class="sxs-lookup"><span data-stu-id="66c7d-126">While text boxes have the benefit of being very flexible, they have the drawback of having minimal constraints.</span></span> <span data-ttu-id="66c7d-127">可編輯文字方塊上的唯一條件約束為：</span><span class="sxs-lookup"><span data-stu-id="66c7d-127">The only constraints on an editable text box are:</span></span>

-   <span data-ttu-id="66c7d-128">您可以選擇性地設定最大字元數。</span><span class="sxs-lookup"><span data-stu-id="66c7d-128">You can optionally set the maximum number of characters.</span></span>
-   <span data-ttu-id="66c7d-129">您可以選擇性地將輸入限制為僅限 (0 9) 的數位字元。</span><span class="sxs-lookup"><span data-stu-id="66c7d-129">You can optionally restrict input to numeric characters (0   9) only.</span></span>
-   <span data-ttu-id="66c7d-130">如果您使用 [微調控制項](ctrl-spin-controls.md)，則可以將微調控制項選項限制為有效的值。</span><span class="sxs-lookup"><span data-stu-id="66c7d-130">If you use a [spin control](ctrl-spin-controls.md), you can limit spin control choices to valid values.</span></span>

<span data-ttu-id="66c7d-131">除了微調控制項的長度和選擇性的顯示內容之外，文字方塊沒有任何建議有效值或其格式的視覺線索。</span><span class="sxs-lookup"><span data-stu-id="66c7d-131">Aside from their length and the optional presence of a spin control, text boxes don't have any visual clues that suggest the valid values or their format.</span></span> <span data-ttu-id="66c7d-132">這表示要依賴標籤來將此資訊傳達給使用者。</span><span class="sxs-lookup"><span data-stu-id="66c7d-132">This means relying on labels to convey this information to users.</span></span> <span data-ttu-id="66c7d-133">如果使用者輸入不正確文字，您必須處理錯誤並顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="66c7d-133">If users enter text that's not valid, you must handle the error with an error message.</span></span>

<span data-ttu-id="66c7d-134">一般來說， **您應該使用您可以使用的最受限制的控制項**。</span><span class="sxs-lookup"><span data-stu-id="66c7d-134">As a general rule, **you should use the most constrained control that you can**.</span></span> <span data-ttu-id="66c7d-135">使用不受限制的控制項（例如文字方塊）做為最後的手段。</span><span class="sxs-lookup"><span data-stu-id="66c7d-135">Use unconstrained controls like text boxes as a last resort.</span></span> <span data-ttu-id="66c7d-136">也就是說，當您考慮條件約束時，請記住全域使用者的需求。</span><span class="sxs-lookup"><span data-stu-id="66c7d-136">That said, when you are considering constraints, bear in mind the needs of global users.</span></span> <span data-ttu-id="66c7d-137">例如，受限於「美國郵遞區號」的控制項不會進行全球化，但接受任何郵遞區號格式的未受限制的文字方塊則為。</span><span class="sxs-lookup"><span data-stu-id="66c7d-137">For example, a control that is constrained to United States ZIP Codes isn't globalized, but an unconstrained text box that accepts any postal code format is.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="66c7d-138">使用模式</span><span class="sxs-lookup"><span data-stu-id="66c7d-138">Usage patterns</span></span>

<span data-ttu-id="66c7d-139">文字方塊是具有許多可能用途的彈性控制項。</span><span class="sxs-lookup"><span data-stu-id="66c7d-139">A text box is a flexible control with several possible uses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66c7d-140"><strong>資料輸入</strong></span><span class="sxs-lookup"><span data-stu-id="66c7d-140"><strong>Data input</strong></span></span><br/> <span data-ttu-id="66c7d-141">單行、未受限制的文字方塊，用來輸入或編輯簡短字串。</span><span class="sxs-lookup"><span data-stu-id="66c7d-141">A single-line, unconstrained text box used to enter or edit short strings.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image2.png" alt="Screen shot of a text box with Display name label " /><br/> <span data-ttu-id="66c7d-142">單行、未受限制的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-142">A single-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66c7d-143"><strong>格式化的資料輸入</strong></span><span class="sxs-lookup"><span data-stu-id="66c7d-143"><strong>Formatted data input</strong></span></span><br/> <span data-ttu-id="66c7d-144">一組簡短、固定大小的單行文字方塊，可用來輸入具有特定格式的資料。</span><span class="sxs-lookup"><span data-stu-id="66c7d-144">A set of short, fixed-sized, single-line text boxes used to enter data with a specific format.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image3.png" alt="Screen shot of a Product key text box " /><br/> <span data-ttu-id="66c7d-145">用於格式化資料輸入的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-145">A text box used for formatted data input.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="66c7d-146"><a href="glossary.md">自動</a>結束功能會自動將輸入焦點從一個文字方塊往下移動。</span><span class="sxs-lookup"><span data-stu-id="66c7d-146">The <a href="glossary.md">auto-exit</a> feature automatically advances the input focus from one text box to the next.</span></span> <span data-ttu-id="66c7d-147">這種方法有一個缺點，就是無法以單一單位的形式複製或貼上資料。</span><span class="sxs-lookup"><span data-stu-id="66c7d-147">One disadvantage to this approach is that the data can't be copied or pasted as a single unit.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66c7d-148"><strong>輔助資料輸入</strong></span><span class="sxs-lookup"><span data-stu-id="66c7d-148"><strong>Assisted data input</strong></span></span><br/> <span data-ttu-id="66c7d-149">單行、未受限制的文字方塊，用來輸入或編輯字串，並結合可協助使用者選取有效值的命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="66c7d-149">A single-line, unconstrained text box used to enter or edit strings, combined with a command button that helps users select valid values.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image4.png" alt="Screen shot of text box with Browse button" /><br/> <span data-ttu-id="66c7d-150">在此範例中，Browse 命令可協助使用者選取有效的值。</span><span class="sxs-lookup"><span data-stu-id="66c7d-150">In this example, the Browse command helps users select valid values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66c7d-151"><strong>文字輸入</strong></span><span class="sxs-lookup"><span data-stu-id="66c7d-151"><strong>Textual input</strong></span></span><br/> <span data-ttu-id="66c7d-152">多行、未受限制的文字方塊，用來輸入或編輯長字串。</span><span class="sxs-lookup"><span data-stu-id="66c7d-152">A multi-line, unconstrained text box used to enter or edit long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image5.png" alt="Screen shot of an Address text box " /><br/> <span data-ttu-id="66c7d-153">多行、未受限制的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-153">A multi-line, unconstrained text box.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66c7d-154"><strong>數字輸入</strong></span><span class="sxs-lookup"><span data-stu-id="66c7d-154"><strong>Numeric input</strong></span></span><br/> <span data-ttu-id="66c7d-155">用來輸入或編輯數位的單行、僅限數位的文字方塊，以及選用的 <a href="ctrl-spin-controls.md">微調控制項</a> 來加速以滑鼠為基礎的輸入。</span><span class="sxs-lookup"><span data-stu-id="66c7d-155">A single-line, numeric-only text box used to enter or edit numbers, with an optional <a href="ctrl-spin-controls.md">spin control</a> to facilitate mouse-based input.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image6.png" alt="Screen shot of a text box for entering a wait time " /><br/> <span data-ttu-id="66c7d-156">用於數值輸入的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-156">A text box used for numeric input.</span></span><br/> <span data-ttu-id="66c7d-157">文字方塊的組合和其相關聯的微調控制項稱為 <a href="ctrl-spin-controls.md">微調</a>方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-157">The combination of a text box and its associated spin control is called a <a href="ctrl-spin-controls.md">spin box</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66c7d-158"><strong>密碼和 PIN 輸入</strong></span><span class="sxs-lookup"><span data-stu-id="66c7d-158"><strong>Password and PIN input</strong></span></span><br/> <span data-ttu-id="66c7d-159">單行、未受限制的文字方塊，用來安全地輸入密碼和 Pin。</span><span class="sxs-lookup"><span data-stu-id="66c7d-159">A single-line, unconstrained text box used to enter passwords and PINs securely.</span></span><br/></td>
<td><img src="images/ctrl-text-boxes-image7.png" alt="Screen shot of a Password text box " /><br/> <span data-ttu-id="66c7d-160">用來輸入密碼的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-160">A text box used to enter passwords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66c7d-161"><strong>資料輸出</strong></span><span class="sxs-lookup"><span data-stu-id="66c7d-161"><strong>Data output</strong></span></span><br/> <span data-ttu-id="66c7d-162">單行的唯讀文字方塊，一律會顯示而不含框線，用來顯示簡短字串。</span><span class="sxs-lookup"><span data-stu-id="66c7d-162">A single-line, read-only text box, always displayed without a border, used to display short strings.</span></span> <br/></td>
<td><span data-ttu-id="66c7d-163">與靜態文字不同的是，使用文字方塊所顯示的資料，可以在資料比) 、選取和複製的控制項更寬時，滾動 (有用。</span><span class="sxs-lookup"><span data-stu-id="66c7d-163">Unlike static text, data displayed using a text box can be scrolled (useful if the data is wider than the control), selected, and copied.</span></span><br/> <img src="images/ctrl-text-boxes-image8.png" alt="Screen shot of a text box showing path to a folder " /><br/> <span data-ttu-id="66c7d-164">用來顯示資料的單行、唯讀文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-164">A single-line, read-only text box used to display data.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66c7d-165"><strong>文字輸出</strong></span><span class="sxs-lookup"><span data-stu-id="66c7d-165"><strong>Textual output</strong></span></span><br/> <span data-ttu-id="66c7d-166">用來顯示長字串的多行、唯讀的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-166">A multi-line, read-only text box used to display long strings.</span></span> <br/></td>
<td><img src="images/ctrl-text-boxes-image9.png" alt="Screen shot of a Privacy information text box " /><br/> <span data-ttu-id="66c7d-167">用來顯示資料的唯讀文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-167">A read-only text box used to display data.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="66c7d-168">指導方針</span><span class="sxs-lookup"><span data-stu-id="66c7d-168">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="66c7d-169">一般</span><span class="sxs-lookup"><span data-stu-id="66c7d-169">General</span></span>

-   <span data-ttu-id="66c7d-170">**停用文字方塊時，也會停用任何相關聯的標籤、指令標籤、微調控制項和命令按鈕。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-170">**When disabling a text box, also disable any associated labels, instruction labels, spin controls, and command buttons.**</span></span>
-   <span data-ttu-id="66c7d-171">**使用自動完成可協助使用者輸入可能重複使用的資料**。</span><span class="sxs-lookup"><span data-stu-id="66c7d-171">**Use auto-complete to help users enter data that is likely to be used repeatedly**.</span></span> <span data-ttu-id="66c7d-172">範例包括使用者名稱、位址和檔案名。</span><span class="sxs-lookup"><span data-stu-id="66c7d-172">Examples include user names, addresses, and file names.</span></span> <span data-ttu-id="66c7d-173">不過，請勿針對可能包含機密資訊的文字方塊（例如密碼、Pin、信用卡號碼或醫療資訊）使用自動完成。</span><span class="sxs-lookup"><span data-stu-id="66c7d-173">However, don't use auto-complete for text boxes that may contain sensitive information, such as passwords, PINs, credit card numbers, or medical information.</span></span>
-   <span data-ttu-id="66c7d-174">**不要讓使用者不必要地滾動。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-174">**Don't make users scroll unnecessarily.**</span></span> <span data-ttu-id="66c7d-175">如果您預期資料會大於文字方塊，而您可以輕易地將文字方塊放大而不會損害配置，請調整方塊的大小以消除滾動的需求。</span><span class="sxs-lookup"><span data-stu-id="66c7d-175">If you expect data to be larger than the text box and you can readily make the text box larger without harming the layout, size the box to eliminate the need for scrolling.</span></span>

    <span data-ttu-id="66c7d-176">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-176">**Incorrect:**</span></span>

    ![<span data-ttu-id="66c7d-177">[電腦名稱稱] 文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-177">screen shot of a computer name text box</span></span> ](images/ctrl-text-boxes-image10.png)

    <span data-ttu-id="66c7d-178">在此範例中，文字方塊的處理方式應該要花更長的時間來處理其資料。</span><span class="sxs-lookup"><span data-stu-id="66c7d-178">In this example, the text box should be made much longer to handle its data.</span></span>

-   <span data-ttu-id="66c7d-179">捲軸：</span><span class="sxs-lookup"><span data-stu-id="66c7d-179">Scroll bars:</span></span>
    -   <span data-ttu-id="66c7d-180">**請勿將水準捲軸放在多行文字方塊上。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-180">**Don't put horizontal scroll bars on multi-line text boxes.**</span></span> <span data-ttu-id="66c7d-181">改為使用垂直捲動和換行。</span><span class="sxs-lookup"><span data-stu-id="66c7d-181">Use vertical scrolling and line wrapping instead.</span></span>
    -   <span data-ttu-id="66c7d-182">**請勿將任何捲軸放在單行文字方塊上。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-182">**Don't put any scroll bars on single-line text boxes.**</span></span>
-   <span data-ttu-id="66c7d-183">**針對數值輸入，您可以使用微調控制項。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-183">**For numeric input, you may use a spin control.**</span></span> <span data-ttu-id="66c7d-184">針對文字輸入，請改用下拉式清單或可編輯的下拉式清單。</span><span class="sxs-lookup"><span data-stu-id="66c7d-184">For textual input, use a drop-down list or editable drop-down list instead.</span></span>
-   <span data-ttu-id="66c7d-185">**請勿使用自動結束功能，除非格式化的資料輸入。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-185">**Don't use the auto-exit feature except for formatted data input.**</span></span> <span data-ttu-id="66c7d-186">自動轉移焦點可能會令人驚訝。</span><span class="sxs-lookup"><span data-stu-id="66c7d-186">The automatic shift of focus can surprise users.</span></span>

### <a name="editable-text-boxes"></a><span data-ttu-id="66c7d-187">可編輯的文字方塊</span><span class="sxs-lookup"><span data-stu-id="66c7d-187">Editable text boxes</span></span>

-   <span data-ttu-id="66c7d-188">**當您可以時，限制輸入文字的長度。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-188">**Limit the length of the input text when you can.**</span></span> <span data-ttu-id="66c7d-189">例如，如果有效的輸入是介於0和999之間的數位，請使用限制為三個字元的數值文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-189">For example, if the valid input is a number between 0 and 999, use a numeric text box that is limited to three characters.</span></span> <span data-ttu-id="66c7d-190">使用格式化資料輸入的所有文字方塊部分都必須有簡短的固定長度。</span><span class="sxs-lookup"><span data-stu-id="66c7d-190">All parts of text boxes that use formatted data input must have a short, fixed length.</span></span>
-   <span data-ttu-id="66c7d-191">**具有資料格式的彈性。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-191">**Be flexible with data formats.**</span></span> <span data-ttu-id="66c7d-192">如果使用者可能使用各種不同的格式來輸入文字，請嘗試處理所有最常見的樣式。</span><span class="sxs-lookup"><span data-stu-id="66c7d-192">If users are likely to enter text using a wide variety of formats, try to handle all the most common ones.</span></span> <span data-ttu-id="66c7d-193">例如，您可以使用選擇性的空格和標點符號輸入許多名稱、數位和識別碼，而且大小寫通常不重要。</span><span class="sxs-lookup"><span data-stu-id="66c7d-193">For example, many names, numbers, and identifiers can be entered with optional spaces and punctuation, and the capitalization often doesn't matter.</span></span>
-   <span data-ttu-id="66c7d-194">如果您無法處理可能的格式，請使用格式資料輸入來要求特定格式，或在標籤中指出有效的格式。</span><span class="sxs-lookup"><span data-stu-id="66c7d-194">If you can't handle the likely formats, require a specific format by using formatted data input or indicate the valid formats in the label.</span></span>

    <span data-ttu-id="66c7d-195">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-195">**Acceptable:**</span></span>

    ![<span data-ttu-id="66c7d-196">數值輸入文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-196">screen shot of a text box for numeric input</span></span> ](images/ctrl-text-boxes-image11.png)

    <span data-ttu-id="66c7d-197">在此範例中，文字方塊需要特定格式的輸入。</span><span class="sxs-lookup"><span data-stu-id="66c7d-197">In this example, a text box requires input in a specific format.</span></span>

    <span data-ttu-id="66c7d-198">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-198">**Better:**</span></span>

    ![<span data-ttu-id="66c7d-199">[格式化資料輸入] 文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-199">screen shot of formatted data input text box</span></span> ](images/ctrl-text-boxes-image12.png)

    <span data-ttu-id="66c7d-200">在此範例中，使用格式化的資料輸入模式來要求特定的格式。</span><span class="sxs-lookup"><span data-stu-id="66c7d-200">In this example, the formatted data input pattern is used to require a specific format.</span></span>

    <span data-ttu-id="66c7d-201">**最好：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-201">**Best:**</span></span>

    ![<span data-ttu-id="66c7d-202">未受限制文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-202">screen shot of an unconstrained text box</span></span> ](images/ctrl-text-boxes-image13.png)

    <span data-ttu-id="66c7d-203">在此範例中，文字方塊會處理所有可能的格式。</span><span class="sxs-lookup"><span data-stu-id="66c7d-203">In this example, a text box handles all likely formats.</span></span>

-   <span data-ttu-id="66c7d-204">選擇最大輸入長度時，請考慮格式化彈性。</span><span class="sxs-lookup"><span data-stu-id="66c7d-204">Consider format flexibility when choosing the maximum input length.</span></span> <span data-ttu-id="66c7d-205">例如，有效的信用卡號碼最多可使用19個字元，因此將長度限制為較短的長度，會讓您難以使用較長的格式輸入數位。</span><span class="sxs-lookup"><span data-stu-id="66c7d-205">For example, a valid credit card number can use up to 19 characters so limiting the length to anything shorter would make it difficult to enter numbers using the longer formats.</span></span>
-   <span data-ttu-id="66c7d-206">**如果使用者更有可能貼上長的複雜資料，請不要使用格式化的資料輸入模式。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-206">**Don't use the formatted data input pattern if users are more likely to paste in long, complex data.**</span></span> <span data-ttu-id="66c7d-207">相反地，請在使用者更可能輸入資料的情況下，保留格式化資料輸入模式。</span><span class="sxs-lookup"><span data-stu-id="66c7d-207">Rather, reserve the formatted data input pattern for situations where users are more likely to type the data.</span></span>

    ![<span data-ttu-id="66c7d-208">具有標籤： ipv6 位址之文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-208">screen shot of a text box with label: ipv6 address</span></span> ](images/ctrl-text-boxes-image14.png)

    <span data-ttu-id="66c7d-209">在此範例中，不會使用格式化的資料輸入模式，讓使用者可以貼上 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="66c7d-209">In this example, the formatted data input pattern isn't used, so that users can to paste IPv6 addresses.</span></span>

-   <span data-ttu-id="66c7d-210">**如果使用者更有可能重新輸入整個值，請選取輸入焦點上的所有文字。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-210">**If users are more likely going to reenter the entire value, select all the text on input focus.**</span></span> <span data-ttu-id="66c7d-211">如果使用者比較有可能進行編輯，請將插入號放在文字的結尾。</span><span class="sxs-lookup"><span data-stu-id="66c7d-211">If users are more likely to edit, place the caret at the end of the text.</span></span>

    ![<span data-ttu-id="66c7d-212">[密碼] 文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-212">screen shot of a password text box</span></span> ](images/ctrl-text-boxes-image15.png)

    <span data-ttu-id="66c7d-213">在此範例中，使用者比較有可能取代編輯，因此會在輸入焦點上選取整個值。</span><span class="sxs-lookup"><span data-stu-id="66c7d-213">In this example, users are more likely to replace than edit, so the entire value is selected on input focus.</span></span>

    ![<span data-ttu-id="66c7d-214">輸入關鍵字之文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-214">screen shot of a text box for entering keywords</span></span> ](images/ctrl-text-boxes-image16.png)

    <span data-ttu-id="66c7d-215">在此範例中，使用者比較有可能加入關鍵字，而不是取代文字，因此插入號會放置在文字的結尾。</span><span class="sxs-lookup"><span data-stu-id="66c7d-215">In this example, users are more likely to add keywords than replace the text, so the caret is placed at the end of the text.</span></span>

-   <span data-ttu-id="66c7d-216">**如果新行字元是有效的輸入，一律使用多行的文字方塊。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-216">**Always use a multi-line text box if new-line characters are valid input.**</span></span>
-   <span data-ttu-id="66c7d-217">**當文字方塊適用于檔案或路徑時，請一律提供 [流覽] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-217">**When the text box is for a file or path, always provide a Browse button.**</span></span>

### <a name="numeric-text-boxes"></a><span data-ttu-id="66c7d-218">數值文字方塊</span><span class="sxs-lookup"><span data-stu-id="66c7d-218">Numeric text boxes</span></span>

-   <span data-ttu-id="66c7d-219">**選擇最方便的單位，並為單元加上標籤。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-219">**Choose the most convenient unit and label the units.**</span></span> <span data-ttu-id="66c7d-220">例如，請考慮使用 milliliters 而非升 (或反之亦然) 、百分比，而不是直接值 (或反之亦然) 等等。</span><span class="sxs-lookup"><span data-stu-id="66c7d-220">For example, consider using milliliters instead of liters (or vice versa), percentages instead of direct values (or vice versa), and so on.</span></span>

    <span data-ttu-id="66c7d-221">**正確：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-221">**Correct:**</span></span>

    ![<span data-ttu-id="66c7d-222">以升為單位的文字方塊螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-222">screen shot of text box with liters as unit</span></span> ](images/ctrl-text-boxes-image17.png)

    <span data-ttu-id="66c7d-223">在此範例中，會標示單位，但需要使用者輸入小數位數。</span><span class="sxs-lookup"><span data-stu-id="66c7d-223">In this example, the unit is labeled, but it requires users to enter decimal numbers.</span></span>

    <span data-ttu-id="66c7d-224">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-224">**Better:**</span></span>

    ![<span data-ttu-id="66c7d-225">以 milliliters 為單位的文字方塊螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-225">screen shot of text box with milliliters as unit</span></span> ](images/ctrl-text-boxes-image18.png)

    <span data-ttu-id="66c7d-226">在此範例中，文字方塊使用較方便的單位。</span><span class="sxs-lookup"><span data-stu-id="66c7d-226">In this example, the text box uses a more convenient unit.</span></span>

-   <span data-ttu-id="66c7d-227">**如果有説明，請使用微調控制項。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-227">**Use a spin control whenever it is helpful.**</span></span> <span data-ttu-id="66c7d-228">不過，有時微調控制項並不實用，例如使用者需要輸入許多大型數位時。</span><span class="sxs-lookup"><span data-stu-id="66c7d-228">However, sometimes spin controls aren't practical, such as when users need to enter many large numbers.</span></span> <span data-ttu-id="66c7d-229">使用微調控制項的時機：</span><span class="sxs-lookup"><span data-stu-id="66c7d-229">Use spin controls when:</span></span>
    -   <span data-ttu-id="66c7d-230">輸入可能是較小的數位，通常低於100。</span><span class="sxs-lookup"><span data-stu-id="66c7d-230">The input is likely to be a small number, typically under 100.</span></span>
    -   <span data-ttu-id="66c7d-231">使用者可能會對現有的數位進行較小的變更。</span><span class="sxs-lookup"><span data-stu-id="66c7d-231">Users are likely to make a small change to an existing number.</span></span>
    -   <span data-ttu-id="66c7d-232">使用者比較可能會使用滑鼠，而不是鍵盤。</span><span class="sxs-lookup"><span data-stu-id="66c7d-232">Users are more likely to be using the mouse than the keyboard.</span></span>
-   <span data-ttu-id="66c7d-233">**每次將數位文字靠右對齊：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-233">**Right-align numeric text whenever:**</span></span>

    -   <span data-ttu-id="66c7d-234">有一個以上的數值文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-234">There is more than one numeric text box.</span></span>
    -   <span data-ttu-id="66c7d-235">文字方塊會垂直對齊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-235">The text boxes are vertically aligned.</span></span>
    -   <span data-ttu-id="66c7d-236">使用者很可能會新增或比較值。</span><span class="sxs-lookup"><span data-stu-id="66c7d-236">Users are likely to add or compare the values.</span></span>

    <span data-ttu-id="66c7d-237">**正確：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-237">**Correct:**</span></span>

    ![<span data-ttu-id="66c7d-238">[費用] 文字方塊的螢幕擷取畫面 (飯店等 ) </span><span class="sxs-lookup"><span data-stu-id="66c7d-238">screen shot of expenses text boxes (hotel, etc.)</span></span> ](images/ctrl-text-boxes-image19.png)

    <span data-ttu-id="66c7d-239">在此範例中，數值文字會靠右對齊，讓您輕鬆比較值。</span><span class="sxs-lookup"><span data-stu-id="66c7d-239">In this example, the numeric text is right-aligned to make it easy to compare values.</span></span>

    <span data-ttu-id="66c7d-240">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-240">**Incorrect:**</span></span>

    ![<span data-ttu-id="66c7d-241">rgb 值文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-241">screen shot of text boxes for rgb values</span></span> ](images/ctrl-text-boxes-image20.png)

    <span data-ttu-id="66c7d-242">在此範例中，數值文字的左對齊方式不正確。</span><span class="sxs-lookup"><span data-stu-id="66c7d-242">In this example, the numeric text is incorrectly left-aligned.</span></span>

-   <span data-ttu-id="66c7d-243">**一律將貨幣值靠右對齊。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-243">**Always right-align monetary values.**</span></span>
-   <span data-ttu-id="66c7d-244">**請勿將特殊意義指派給特定數值**，即使您的應用程式在內部使用這些特殊意義也是一樣。</span><span class="sxs-lookup"><span data-stu-id="66c7d-244">**Don't assign special meanings to specific numeric values**, even if those special meanings are used internally by your application.</span></span> <span data-ttu-id="66c7d-245">相反地，請使用核取方塊或選項按鈕來進行明確的使用者選取。</span><span class="sxs-lookup"><span data-stu-id="66c7d-245">Instead, use check boxes or radio buttons for an explicit user selection.</span></span>

    <span data-ttu-id="66c7d-246">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-246">**Incorrect:**</span></span>

    ![<span data-ttu-id="66c7d-247">標籤的螢幕擷取畫面：使用-1 可停用快取</span><span class="sxs-lookup"><span data-stu-id="66c7d-247">screen shot of label: use -1 to disable caching</span></span> ](images/ctrl-text-boxes-image21.png)

    <span data-ttu-id="66c7d-248">在此範例中，值-1 具有特殊意義。</span><span class="sxs-lookup"><span data-stu-id="66c7d-248">In this example, the value -1 has a special meaning.</span></span>

    <span data-ttu-id="66c7d-249">**正確：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-249">**Correct:**</span></span>

    ![<span data-ttu-id="66c7d-250">核取方塊標籤的螢幕擷取畫面：快取</span><span class="sxs-lookup"><span data-stu-id="66c7d-250">screen shot of check box label: caching</span></span> ](images/ctrl-text-boxes-image22.png)

    <span data-ttu-id="66c7d-251">在此範例中，核取方塊會讓選項明確。</span><span class="sxs-lookup"><span data-stu-id="66c7d-251">In this example, a check box makes the option explicit.</span></span>

### <a name="password-and-pin-input"></a><span data-ttu-id="66c7d-252">密碼和 PIN 輸入</span><span class="sxs-lookup"><span data-stu-id="66c7d-252">Password and PIN input</span></span>

-   <span data-ttu-id="66c7d-253">**一律使用密碼通用控制項，而不是建立您自己的控制項。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-253">**Always use the password common control instead of creating your own.**</span></span> <span data-ttu-id="66c7d-254">密碼和 Pin 需要以安全的方式處理特殊處理。</span><span class="sxs-lookup"><span data-stu-id="66c7d-254">Passwords and PINs require special treatment to be handled securely.</span></span>

<span data-ttu-id="66c7d-255">如需更多指導方針和範例，請參閱 [球標](ctrl-balloons.md)。</span><span class="sxs-lookup"><span data-stu-id="66c7d-255">For more guidelines and examples, see [Balloons](ctrl-balloons.md).</span></span>

### <a name="textual-output"></a><span data-ttu-id="66c7d-256">文字輸出</span><span class="sxs-lookup"><span data-stu-id="66c7d-256">Textual output</span></span>

-   <span data-ttu-id="66c7d-257">**針對大型、多行唯讀文字，請考慮使用白色背景系統色彩。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-257">**Consider using the white background system color for large, multi-line read-only text.**</span></span> <span data-ttu-id="66c7d-258">白色背景讓文字更容易閱讀。</span><span class="sxs-lookup"><span data-stu-id="66c7d-258">A white background makes the text easier to read.</span></span> <span data-ttu-id="66c7d-259">灰色背景上的許多文字都不會防止閱讀。</span><span class="sxs-lookup"><span data-stu-id="66c7d-259">Lots of text on a gray background discourages reading.</span></span>

<span data-ttu-id="66c7d-260">如需背景色彩的詳細資訊， [請參閱字型](vis-fonts.md)。</span><span class="sxs-lookup"><span data-stu-id="66c7d-260">For more information on background colors, see [Fonts](vis-fonts.md).</span></span>

### <a name="data-output"></a><span data-ttu-id="66c7d-261">資料輸出</span><span class="sxs-lookup"><span data-stu-id="66c7d-261">Data output</span></span>

-   <span data-ttu-id="66c7d-262">**請勿針對單行、唯讀文字方塊使用框線。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-262">**Don't use a border for single-line, read-only text boxes.**</span></span> <span data-ttu-id="66c7d-263">框線是可編輯文字的視覺線索。</span><span class="sxs-lookup"><span data-stu-id="66c7d-263">The border is a visual clue that the text is editable.</span></span>
-   <span data-ttu-id="66c7d-264">**請勿停用單行、唯讀的文字方塊。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-264">**Don't disable single-line, read-only text boxes.**</span></span> <span data-ttu-id="66c7d-265">這可防止使用者選取文字並將其複製到剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="66c7d-265">This prevents users from selecting and copying the text to the clipboard.</span></span> <span data-ttu-id="66c7d-266">它也可防止使用者在超過其界限大小的情況時，將資料滾動。</span><span class="sxs-lookup"><span data-stu-id="66c7d-266">It also prevents users from scrolling the data if it exceeds the size of its boundaries.</span></span>
-   <span data-ttu-id="66c7d-267">**除非使用者可能需要滾動或複製文字，否則請勿在單行、唯讀的文字方塊上設定制表位。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-267">**Don't set a tab stop on single-line, read-only text box unless the user is likely to need to scroll or copy the text.**</span></span>

## <a name="input-validation-and-error-handling"></a><span data-ttu-id="66c7d-268">輸入驗證和錯誤處理</span><span class="sxs-lookup"><span data-stu-id="66c7d-268">Input validation and error handling</span></span>

<span data-ttu-id="66c7d-269">由於文字方塊通常不會限制為只接受有效的輸入，因此您可能需要驗證輸入，並處理任何問題。</span><span class="sxs-lookup"><span data-stu-id="66c7d-269">Because text boxes are usually not constrained to accept only valid input, you may need to validate the input and handle any problems.</span></span> <span data-ttu-id="66c7d-270">驗證各種類型的輸入問題，如下所示：</span><span class="sxs-lookup"><span data-stu-id="66c7d-270">Validate the various types of input problems as follows:</span></span>

-   <span data-ttu-id="66c7d-271">如果使用者輸入不正確字元，請忽略字元，並顯示 [輸入問題氣球](ctrl-balloons.md) 來說明有效的字元。</span><span class="sxs-lookup"><span data-stu-id="66c7d-271">If the user enters a character that isn't valid, ignore the character and display an [input problem balloon](ctrl-balloons.md) that explains the valid characters.</span></span>

    ![[產品金鑰] 文字方塊的螢幕擷取畫面](images/ctrl-text-boxes-image23.png)

    <span data-ttu-id="66c7d-273">在此範例中，氣球會報告不正確的輸入字元。</span><span class="sxs-lookup"><span data-stu-id="66c7d-273">In this example, a balloon reports an incorrect input character.</span></span>

-   <span data-ttu-id="66c7d-274">如果輸入資料的值或格式無效，當文字方塊失去輸入焦點時，就會顯示輸入問題氣球。</span><span class="sxs-lookup"><span data-stu-id="66c7d-274">If the input data has a value or format that isn't valid, display an input problem balloon when the text box loses input focus.</span></span>
-   <span data-ttu-id="66c7d-275">如果輸入資料與視窗中的其他控制項不一致，請在整個輸入完成時提供錯誤訊息，例如當使用者按一下強制回應對話方塊的 [確定] 時。</span><span class="sxs-lookup"><span data-stu-id="66c7d-275">If the input data is inconsistent with other controls on the window, give an error message when the entire input is complete, such as when users click OK for a modal dialog box.</span></span>

<span data-ttu-id="66c7d-276">**除非使用者無法輕易更正錯誤，否則請不要清除不正確輸入資料。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-276">**Don't clear invalid input data unless users aren't able to correct errors easily.**</span></span> <span data-ttu-id="66c7d-277">這麼做可讓使用者在不需要重新開機的情況下更正錯誤。</span><span class="sxs-lookup"><span data-stu-id="66c7d-277">Doing so allows users to correct mistakes without starting over.</span></span> <span data-ttu-id="66c7d-278">例如，您應該清除不正確的密碼和 Pin 碼，因為使用者無法輕易地修正它們。</span><span class="sxs-lookup"><span data-stu-id="66c7d-278">For example, you should clear incorrect passwords and PINs because users can't correct them easily.</span></span>

<span data-ttu-id="66c7d-279">如需更多指導方針與範例，請參閱 [錯誤訊息](mess-error.md) 和 [批註](ctrl-balloons.md)提示。</span><span class="sxs-lookup"><span data-stu-id="66c7d-279">For more guidelines and examples, see [Error Messages](mess-error.md) and [Balloons](ctrl-balloons.md).</span></span>

## <a name="prompts"></a><span data-ttu-id="66c7d-280">提示</span><span class="sxs-lookup"><span data-stu-id="66c7d-280">Prompts</span></span>

<span data-ttu-id="66c7d-281">提示是放在文字方塊內的標籤或簡短指令，作為其預設值。</span><span class="sxs-lookup"><span data-stu-id="66c7d-281">A prompt is a label or short instruction placed inside a text box as its default value.</span></span> <span data-ttu-id="66c7d-282">與靜態文字不同的是，當使用者在文字方塊中輸入內容或取得輸入焦點時，會從畫面中消失。</span><span class="sxs-lookup"><span data-stu-id="66c7d-282">Unlike static text, prompts disappear from the screen once users type something into the text box or it gets input focus.</span></span>

![<span data-ttu-id="66c7d-283">具有標籤的提示文字方塊螢幕擷取畫面：搜尋</span><span class="sxs-lookup"><span data-stu-id="66c7d-283">screen shot of prompt text box with label: search</span></span> ](images/ctrl-text-boxes-image24.png)

<span data-ttu-id="66c7d-284">典型的提示。</span><span class="sxs-lookup"><span data-stu-id="66c7d-284">A typical prompt.</span></span>

<span data-ttu-id="66c7d-285">在下列情況下使用提示：</span><span class="sxs-lookup"><span data-stu-id="66c7d-285">Use a prompt when:</span></span>

-   <span data-ttu-id="66c7d-286">螢幕空間是在不需要使用標籤或指示的高階頁面上，例如工具列上。</span><span class="sxs-lookup"><span data-stu-id="66c7d-286">Screen space is at such a premium that using a label or instruction is undesirable, such as on a toolbar.</span></span>
-   <span data-ttu-id="66c7d-287">提示的主要目的是要以精簡的方式識別文字方塊的用途。</span><span class="sxs-lookup"><span data-stu-id="66c7d-287">The prompt is primarily for identifying the purpose of the text box in a compact way.</span></span> <span data-ttu-id="66c7d-288">當使用者使用文字方塊時，不一定要有重要的資訊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-288">It must not be crucial information that the user needs to see while using the text box.</span></span>

<span data-ttu-id="66c7d-289">請勿使用提示來指示使用者輸入內容，或按一下按鈕。</span><span class="sxs-lookup"><span data-stu-id="66c7d-289">Don't use prompts just to direct users to type something or to click buttons.</span></span> <span data-ttu-id="66c7d-290">例如，請勿寫入提示文字，指出輸入檔案名，然後按一下 [傳送]。</span><span class="sxs-lookup"><span data-stu-id="66c7d-290">For example, don't write prompt text that says Enter a filename and then click Send.</span></span>

<span data-ttu-id="66c7d-291">使用提示時：</span><span class="sxs-lookup"><span data-stu-id="66c7d-291">When using prompts:</span></span>

-   <span data-ttu-id="66c7d-292">以斜體灰色和實際的輸入文字（一般黑色）繪製提示文字。</span><span class="sxs-lookup"><span data-stu-id="66c7d-292">Draw the prompt text in italic gray and the actual input text in normal black.</span></span> <span data-ttu-id="66c7d-293">提示文字不能與真正的文字混淆。</span><span class="sxs-lookup"><span data-stu-id="66c7d-293">The prompt text must not be confused with real text.</span></span>
-   <span data-ttu-id="66c7d-294">將提示文字保持簡潔。</span><span class="sxs-lookup"><span data-stu-id="66c7d-294">Keep the prompt text concise.</span></span> <span data-ttu-id="66c7d-295">您可以使用片段，而不是完整的句子。</span><span class="sxs-lookup"><span data-stu-id="66c7d-295">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="66c7d-296">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="66c7d-296">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="66c7d-297">請勿使用結尾標點符號或省略號。</span><span class="sxs-lookup"><span data-stu-id="66c7d-297">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="66c7d-298">當使用者在文字方塊中按一下或 tab 鍵時，提示文字應該無法編輯，而且應該會消失。</span><span class="sxs-lookup"><span data-stu-id="66c7d-298">The prompt text should not be editable and should disappear once users click in or tab into the text box.</span></span>
    -   <span data-ttu-id="66c7d-299">**例外狀況：** 如果文字方塊具有預設輸入焦點，則會顯示提示，並在使用者開始鍵入之後消失。</span><span class="sxs-lookup"><span data-stu-id="66c7d-299">**Exception:** If the text box has default input focus, the prompt is displayed, and it disappears once the user starts typing.</span></span>
-   <span data-ttu-id="66c7d-300">如果文字方塊在遺失輸入焦點時仍為空白，則會還原提示文字。</span><span class="sxs-lookup"><span data-stu-id="66c7d-300">The prompt text is restored if the text box is still empty when it loses input focus.</span></span>

## <a name="recommended-sizing-and-spacing"></a><span data-ttu-id="66c7d-301">建議的大小和間距</span><span class="sxs-lookup"><span data-stu-id="66c7d-301">Recommended sizing and spacing</span></span>

![<span data-ttu-id="66c7d-302">單行和兩行文字方塊的圖表</span><span class="sxs-lookup"><span data-stu-id="66c7d-302">figure of one-line and two-line text boxes</span></span> ](images/ctrl-text-boxes-image25.png)

<span data-ttu-id="66c7d-303">文字方塊的建議大小和間距。</span><span class="sxs-lookup"><span data-stu-id="66c7d-303">Recommended sizing and spacing for text boxes.</span></span>

<span data-ttu-id="66c7d-304">文字方塊的寬度是預期輸入大小的視覺線索。</span><span class="sxs-lookup"><span data-stu-id="66c7d-304">The width of a text box is a visual clue of the expected input size.</span></span> <span data-ttu-id="66c7d-305">調整文字方塊大小時：</span><span class="sxs-lookup"><span data-stu-id="66c7d-305">When sizing text boxes:</span></span>

-   <span data-ttu-id="66c7d-306">**選擇適合最長有效資料的寬度。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-306">**Choose a width appropriate for the longest valid data.**</span></span> <span data-ttu-id="66c7d-307">在大部分的情況下，使用者不需要滾動所輸入或查看的最長可能字串。</span><span class="sxs-lookup"><span data-stu-id="66c7d-307">In most situations, users shouldn't have to scroll the longest likely string they'll enter or view.</span></span>
-   <span data-ttu-id="66c7d-308">**包含額外的 30%** (高達200% 的文字，以提供任何文字 (較短的文字) ，而不是) 將當地語系化的數位。</span><span class="sxs-lookup"><span data-stu-id="66c7d-308">**Include an additional 30 percent** (up to 200 percent for shorter text) for any text (but not numbers) that will be localized.</span></span>
-   <span data-ttu-id="66c7d-309">**如果預期的輸入沒有特定大小，請選擇與視窗中其他文字方塊或控制項一致的寬度。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-309">**If the expected input has no particular size, choose a width that is consistent with the other text boxes or controls on the window.**</span></span>
-   <span data-ttu-id="66c7d-310">**調整多行文字方塊的大小，以顯示整數行的文字數。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-310">**Size multi-line text boxes to display an integral number of lines of text.**</span></span>

## <a name="labels"></a><span data-ttu-id="66c7d-311">標籤</span><span class="sxs-lookup"><span data-stu-id="66c7d-311">Labels</span></span>

### <a name="text-box-labels"></a><span data-ttu-id="66c7d-312">文字方塊標籤</span><span class="sxs-lookup"><span data-stu-id="66c7d-312">Text box labels</span></span>

-   <span data-ttu-id="66c7d-313">所有文字方塊都需要標籤。</span><span class="sxs-lookup"><span data-stu-id="66c7d-313">All text boxes need labels.</span></span> <span data-ttu-id="66c7d-314">將標籤以單字或片語的形式寫入，而不是以句子（以冒號結尾）和使用 [靜態文字](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="66c7d-314">Write the label as a word or phrase, not as a sentence, ending with a colon, and using [static text](glossary.md).</span></span>

    <span data-ttu-id="66c7d-315">**異常：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-315">**Exceptions:**</span></span>

    -   <span data-ttu-id="66c7d-316">含有提示的文字方塊，其中的空間位於 premium。</span><span class="sxs-lookup"><span data-stu-id="66c7d-316">Text boxes with prompts located where space is at a premium.</span></span>
    -   <span data-ttu-id="66c7d-317">針對標記，用於 **格式化資料輸入** 的一組文字方塊應視為單一文字方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-317">For labeling, a group of text boxes used for **formatted data input** should be treated as a single text box.</span></span>
    -   <span data-ttu-id="66c7d-318">如果文字方塊是指向選項按鈕或核取方塊，並以冒號結尾的標籤來導入，請勿在文字方塊上放置額外的標籤。</span><span class="sxs-lookup"><span data-stu-id="66c7d-318">If a text box is subordinate to a radio button or check box, and is introduced by its label ending with a colon, don't put an additional label on the text box.</span></span>
    -   <span data-ttu-id="66c7d-319">**省略重新聲明主要指令的控制項標籤。**</span><span class="sxs-lookup"><span data-stu-id="66c7d-319">**Omit control labels that restate the main instruction.**</span></span> <span data-ttu-id="66c7d-320">在此情況下，主要指令會採用冒號 (，除非它是問題) 和存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="66c7d-320">In this case, the main instruction takes the colon (unless it's a question) and access key.</span></span>

        <span data-ttu-id="66c7d-321">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-321">**Acceptable:**</span></span>

        ![具有重複標籤之文字方塊的螢幕擷取畫面](images/ctrl-text-boxes-image26.png)

        <span data-ttu-id="66c7d-323">在此範例中，文字方塊標籤只是主要指令的重述。</span><span class="sxs-lookup"><span data-stu-id="66c7d-323">In this example, the text box label is just a restatement of the main instruction.</span></span>

        <span data-ttu-id="66c7d-324">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-324">**Better:**</span></span>

        ![<span data-ttu-id="66c7d-325">只有主要指示的文字方塊螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-325">screen shot of text box with main instruction only</span></span> ](images/ctrl-text-boxes-image27.png)

        <span data-ttu-id="66c7d-326">在此範例中，會移除多餘的標籤，所以主要指令會接受冒號和存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="66c7d-326">In this example, the redundant label is removed, so the main instruction takes the colon and access key.</span></span>

-   <span data-ttu-id="66c7d-327">指派唯一的存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="66c7d-327">Assign a unique access key.</span></span> <span data-ttu-id="66c7d-328">如需存取金鑰指派指導方針，請參閱 [鍵盤](inter-keyboard.md)。</span><span class="sxs-lookup"><span data-stu-id="66c7d-328">For access key assignment guidelines, see [Keyboard](inter-keyboard.md).</span></span>
-   <span data-ttu-id="66c7d-329">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="66c7d-329">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="66c7d-330">將標籤放在文字方塊的左邊或上方，然後將標籤與文字方塊的左邊緣對齊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-330">Position the label either to the left of or above the text box, and align the label with the left edge of the text box.</span></span> <span data-ttu-id="66c7d-331">如果標籤位於左邊，請垂直對齊標籤文字與文字方塊文字。</span><span class="sxs-lookup"><span data-stu-id="66c7d-331">If the label is on the left, vertically align the label text with the text box text.</span></span>

    <span data-ttu-id="66c7d-332">**正確：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-332">**Correct:**</span></span>

    ![<span data-ttu-id="66c7d-333">文字方塊上方靠左對齊標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-333">screen shot of left-aligned label above text box</span></span> ](images/ctrl-text-boxes-image28.png)

    ![<span data-ttu-id="66c7d-334">文字方塊左邊的文字對齊標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-334">screen shot of text-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image29.png)

    <span data-ttu-id="66c7d-335">在這些範例中，頂端的標籤會與文字方塊的左邊緣對齊，而左邊的標籤會與文字方塊中的文字對齊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-335">In these examples, the label on top aligns with the left edge of the text box, and the label on the left aligns with the text in the text box.</span></span>

    <span data-ttu-id="66c7d-336">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-336">**Incorrect:**</span></span>

    ![<span data-ttu-id="66c7d-337">文字方塊上方文字對齊標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-337">screen shot of text-aligned label above text box</span></span> ](images/ctrl-text-boxes-image30.png)

    ![<span data-ttu-id="66c7d-338">文字方塊左邊靠左對齊標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-338">screen shot of top-aligned label left of text box</span></span> ](images/ctrl-text-boxes-image31.png)

    <span data-ttu-id="66c7d-339">在這些不正確的範例中，頂端的標籤會與文字方塊中的文字對齊，而左邊的標籤會與文字方塊的頂端對齊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-339">In these incorrect examples, the label on top aligns with the text in the text box, and the label on the left aligns with the top of the text box.</span></span>

-   <span data-ttu-id="66c7d-340">您可以在標籤後面的括弧中指定單位 (例如，秒數或連接) 。</span><span class="sxs-lookup"><span data-stu-id="66c7d-340">You may specify units (for example, seconds or connections) in parentheses after the label.</span></span>
-   <span data-ttu-id="66c7d-341">如果文字方塊接受任意小的字元數上限，您可以在標籤中陳述最大輸入。</span><span class="sxs-lookup"><span data-stu-id="66c7d-341">If a text box accepts an arbitrarily small maximum number of characters, you can state the maximum input in the label.</span></span> <span data-ttu-id="66c7d-342">文字方塊寬度也應建議大小上限。</span><span class="sxs-lookup"><span data-stu-id="66c7d-342">The text box width should also suggest the maximum size.</span></span>

    ![<span data-ttu-id="66c7d-343">[密碼] 文字方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-343">screen shot of password text box</span></span> ](images/ctrl-text-boxes-image32.png)

    <span data-ttu-id="66c7d-344">在此範例中，標籤會提供最大字元數。</span><span class="sxs-lookup"><span data-stu-id="66c7d-344">In this example, the label gives the maximum number of characters.</span></span>

-   <span data-ttu-id="66c7d-345">請勿將文字方塊的內容 (或其單位標籤) 句子的一部分，因為這不是可當地語系化的。</span><span class="sxs-lookup"><span data-stu-id="66c7d-345">Don't make the content of the text box (or its units label) part of a sentence, because this is not localizable.</span></span>
-   <span data-ttu-id="66c7d-346">如果文字方塊可以用來輸入數個專案，請清楚說明如何分隔標籤中的專案。</span><span class="sxs-lookup"><span data-stu-id="66c7d-346">If the text box can be used to enter several items, make it clear how to separate the items in the label.</span></span>

    ![<span data-ttu-id="66c7d-347">以分號分隔標籤的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-347">screen shot of label separate names with semicolon</span></span> ](images/ctrl-text-boxes-image33.png)

    <span data-ttu-id="66c7d-348">在此範例中，標籤中會提供專案分隔符號。</span><span class="sxs-lookup"><span data-stu-id="66c7d-348">In this example, the item separator is given in the label.</span></span>

-   <span data-ttu-id="66c7d-349">如需指出必要輸入的指導方針，請參閱 [對話方塊](win-dialog-box.md)中的必要輸入。</span><span class="sxs-lookup"><span data-stu-id="66c7d-349">For guidelines on indicating required input, see Required input in [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="instruction-labels"></a><span data-ttu-id="66c7d-350">指令標籤</span><span class="sxs-lookup"><span data-stu-id="66c7d-350">Instruction labels</span></span>

-   <span data-ttu-id="66c7d-351">如果您需要新增有關文字方塊的解說文字，請將它加入標籤上方。</span><span class="sxs-lookup"><span data-stu-id="66c7d-351">If you need to add instructional text about a text box, add it above the label.</span></span> <span data-ttu-id="66c7d-352">使用結尾標點符號的完整句子。</span><span class="sxs-lookup"><span data-stu-id="66c7d-352">Use complete sentences with ending punctuation.</span></span>
-   <span data-ttu-id="66c7d-353">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="66c7d-353">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="66c7d-354">有説明但不需要的其他資訊應該保持簡短。</span><span class="sxs-lookup"><span data-stu-id="66c7d-354">Additional information that is helpful but not necessary should be kept short.</span></span> <span data-ttu-id="66c7d-355">請將這項資訊放在標籤和冒號之間的括弧內，或在文字方塊下方的括弧之外。</span><span class="sxs-lookup"><span data-stu-id="66c7d-355">Place this information either in parentheses between the label and colon, or without parentheses below the text box.</span></span>

    ![<span data-ttu-id="66c7d-356">[新增的資訊] 文字方塊中的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="66c7d-356">screen shot of added information below text box</span></span> ](images/ctrl-text-boxes-image34.png)

    <span data-ttu-id="66c7d-357">在此範例中，會將其他資訊放在文字方塊下方。</span><span class="sxs-lookup"><span data-stu-id="66c7d-357">In this example, additional information is placed below the text box.</span></span>

### <a name="prompt-labels"></a><span data-ttu-id="66c7d-358">提示標籤</span><span class="sxs-lookup"><span data-stu-id="66c7d-358">Prompt labels</span></span>

-   <span data-ttu-id="66c7d-359">將提示文字保持簡潔。</span><span class="sxs-lookup"><span data-stu-id="66c7d-359">Keep the prompt text concise.</span></span> <span data-ttu-id="66c7d-360">您可以使用片段，而不是完整的句子。</span><span class="sxs-lookup"><span data-stu-id="66c7d-360">You can use fragments instead of full sentences.</span></span>
-   <span data-ttu-id="66c7d-361">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="66c7d-361">Use sentence-style capitalization.</span></span>
-   <span data-ttu-id="66c7d-362">請勿使用結尾標點符號或省略號。</span><span class="sxs-lookup"><span data-stu-id="66c7d-362">Don't use ending punctuation or ellipsis.</span></span>
-   <span data-ttu-id="66c7d-363">如果提示使用者輸入的資訊將由文字方塊旁的按鈕所處理，只要將按鈕放在文字方塊旁邊即可。</span><span class="sxs-lookup"><span data-stu-id="66c7d-363">If the prompt directs users to enter information that will be acted upon by a button next to the text box, simply place the button next to the text box.</span></span> <span data-ttu-id="66c7d-364">請不要使用提示來指示使用者按一下按鈕 (例如，不要撰寫顯示的提示文字、拖曳檔案，然後按一下 [傳送) 。</span><span class="sxs-lookup"><span data-stu-id="66c7d-364">Don't use the prompt to direct users to click the button (for example, don't write prompt text that says, Drag a file and then click Send).</span></span>

## <a name="documentation"></a><span data-ttu-id="66c7d-365">文件</span><span class="sxs-lookup"><span data-stu-id="66c7d-365">Documentation</span></span>

<span data-ttu-id="66c7d-366">參考文字方塊時：</span><span class="sxs-lookup"><span data-stu-id="66c7d-366">When referring to text boxes:</span></span>

-   <span data-ttu-id="66c7d-367">使用類型可參考需要輸入或貼上的使用者互動;否則，若使用者可以使用其他方式將資訊放入文字方塊中，例如從清單中選取值或使用 [流覽] 按鈕，請使用 enter。</span><span class="sxs-lookup"><span data-stu-id="66c7d-367">Use type to refer to user interactions that require typing or pasting; otherwise use enter if users can put information into the text box using other means, such as selecting the value from a list or using a Browse button.</span></span>
-   <span data-ttu-id="66c7d-368">使用 [選取] 可參考唯讀文字方塊中的專案。</span><span class="sxs-lookup"><span data-stu-id="66c7d-368">Use select to refer to an entry in a read-only text box.</span></span>
-   <span data-ttu-id="66c7d-369">使用確切的標籤文字（包含其大小寫），並包含 [單字] 方塊。</span><span class="sxs-lookup"><span data-stu-id="66c7d-369">Use the exact label text, including its capitalization, and include the word box.</span></span> <span data-ttu-id="66c7d-370">請勿包含存取金鑰底線或冒號。</span><span class="sxs-lookup"><span data-stu-id="66c7d-370">Don't include the access key underscore or colon.</span></span> <span data-ttu-id="66c7d-371">請勿將文字方塊稱為文字方塊或欄位。</span><span class="sxs-lookup"><span data-stu-id="66c7d-371">Don't refer to a text box as a text box or a field.</span></span>
-   <span data-ttu-id="66c7d-372">可能的話，請使用粗體文字來格式化標籤。</span><span class="sxs-lookup"><span data-stu-id="66c7d-372">When possible, format the label using bold text.</span></span> <span data-ttu-id="66c7d-373">否則，請只在必要時才將標籤放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="66c7d-373">Otherwise, put the label in quotation marks only if required to prevent confusion.</span></span>

    <span data-ttu-id="66c7d-374">範例：在 [ **密碼** ] 方塊中輸入您的密碼，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="66c7d-374">Example: Type your password into the **Password** box, and then click **OK**.</span></span>

-   <span data-ttu-id="66c7d-375">如果文字方塊需要特定格式，請只記錄最常使用的可接受格式。</span><span class="sxs-lookup"><span data-stu-id="66c7d-375">If the text box requires a specific format, document only the most commonly used acceptable format.</span></span> <span data-ttu-id="66c7d-376">讓使用者自行探索任何其他格式。</span><span class="sxs-lookup"><span data-stu-id="66c7d-376">Let users discover any other formats on their own.</span></span> <span data-ttu-id="66c7d-377">您想要有資料格式的彈性，但是這樣做並不會產生複雜的檔。</span><span class="sxs-lookup"><span data-stu-id="66c7d-377">You want to be flexible with data formats, but doing so should not result in complex documentation.</span></span>

    <span data-ttu-id="66c7d-378">**正確：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-378">**Correct:**</span></span>

    <span data-ttu-id="66c7d-379">請使用1234-56-7890 格式輸入元件的序號。</span><span class="sxs-lookup"><span data-stu-id="66c7d-379">Enter the part's serial number using the 1234-56-7890 format.</span></span>

    <span data-ttu-id="66c7d-380">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="66c7d-380">**Incorrect:**</span></span>

    <span data-ttu-id="66c7d-381">使用下列任一種格式輸入元件的序號：</span><span class="sxs-lookup"><span data-stu-id="66c7d-381">Enter the part's serial number using any of the following formats:</span></span>

    <span data-ttu-id="66c7d-382">1234567890</span><span class="sxs-lookup"><span data-stu-id="66c7d-382">1234567890</span></span>

    <span data-ttu-id="66c7d-383">1234-56-7890</span><span class="sxs-lookup"><span data-stu-id="66c7d-383">1234-56-7890</span></span>

    <span data-ttu-id="66c7d-384">1234 56 7890</span><span class="sxs-lookup"><span data-stu-id="66c7d-384">1234 56 7890</span></span>

