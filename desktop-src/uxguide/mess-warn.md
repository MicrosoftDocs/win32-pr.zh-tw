---
title: 警告訊息
description: 警告訊息是強制回應對話方塊、就地訊息、通知或氣球，會警示使用者可能會在未來發生問題的狀況。
ms.assetid: 4a2c3be9-9dc6-4d62-bd3d-72a2e5b621f4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: d704890b2471e205b933e2995950716c269488e8
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321411"
---
# <a name="warning-messages"></a><span data-ttu-id="41c43-103">警告訊息</span><span class="sxs-lookup"><span data-stu-id="41c43-103">Warning Messages</span></span>

> [!NOTE]
> <span data-ttu-id="41c43-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="41c43-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="41c43-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="41c43-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="41c43-106">警告訊息是強制回應對話方塊、就地訊息、通知或氣球，會警示使用者可能會在未來發生問題的狀況。</span><span class="sxs-lookup"><span data-stu-id="41c43-106">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span>

![一般警告訊息的螢幕擷取畫面](images/mess-warn-image1.png)

<span data-ttu-id="41c43-108">一般的強制回應警告訊息。</span><span class="sxs-lookup"><span data-stu-id="41c43-108">A typical modal warning message.</span></span>

<span data-ttu-id="41c43-109">警告的基本特性是，它們牽涉到遺失下列一或多項的風險：</span><span class="sxs-lookup"><span data-stu-id="41c43-109">The fundamental characteristic of warnings is that they involve the risk of losing one or more of the following:</span></span>

-   <span data-ttu-id="41c43-110">重要的資產，例如重要的財務或其他資料。</span><span class="sxs-lookup"><span data-stu-id="41c43-110">A valuable asset, such as important financial or other data.</span></span>
-   <span data-ttu-id="41c43-111">系統存取或完整性。</span><span class="sxs-lookup"><span data-stu-id="41c43-111">System access or integrity.</span></span>
-   <span data-ttu-id="41c43-112">隱私權或對機密資訊的控制。</span><span class="sxs-lookup"><span data-stu-id="41c43-112">Privacy or control over confidential information.</span></span>
-   <span data-ttu-id="41c43-113">使用者的時間 (大量的時間，例如30秒或更多的) 。</span><span class="sxs-lookup"><span data-stu-id="41c43-113">User's time (a significant amount, such as 30 seconds or more).</span></span>

<span data-ttu-id="41c43-114">相反地，確認是一個強制回應對話方塊，會詢問使用者是否要繼續執行動作。</span><span class="sxs-lookup"><span data-stu-id="41c43-114">By contrast, a confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span> <span data-ttu-id="41c43-115">某些類型的警告會顯示為確認，若是如此，則也適用確認方針。</span><span class="sxs-lookup"><span data-stu-id="41c43-115">Some types of warnings are presented as confirmations, and if so, the confirmation guidelines also apply.</span></span>

<span data-ttu-id="41c43-116">**注意：** 與 [對話方塊](win-dialog-box.md)、 [確認](mess-confirm.md)、 [錯誤訊息](mess-error.md)[標準圖示](vis-std-icons.md)、 [通知](mess-notif.md)和 [版面](vis-layout.md) 配置相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="41c43-116">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [confirmations](mess-confirm.md), [error messages](mess-error.md)[standard icons](vis-std-icons.md), [notifications](mess-notif.md), and [layout](vis-layout.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="41c43-117">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="41c43-117">Is this the right user interface?</span></span>

<span data-ttu-id="41c43-118">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="41c43-118">To decide, consider these questions:</span></span>

-   <span data-ttu-id="41c43-119">**使用者是否會收到警示，指出未來可能會造成問題的情況？**</span><span class="sxs-lookup"><span data-stu-id="41c43-119">**Is the user being alerted of a condition that might cause a problem in the future?**</span></span> <span data-ttu-id="41c43-120">如果沒有，訊息就不會是警告。</span><span class="sxs-lookup"><span data-stu-id="41c43-120">If not, the message isn't a warning.</span></span>
-   <span data-ttu-id="41c43-121">**UI 是否呈現已發生的錯誤或問題？**</span><span class="sxs-lookup"><span data-stu-id="41c43-121">**Is the UI presenting an error or problem that has already occurred?**</span></span> <span data-ttu-id="41c43-122">若是如此，請改用錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="41c43-122">If so, use an error message instead.</span></span>
-   <span data-ttu-id="41c43-123">**使用者是否有可能執行動作，或將其行為變更為訊息的結果？**</span><span class="sxs-lookup"><span data-stu-id="41c43-123">**Are users likely to perform an action or change their behavior as the result of the message?**</span></span> <span data-ttu-id="41c43-124">如果沒有，則條件不會讓使用者中斷，因此最好隱藏警告。</span><span class="sxs-lookup"><span data-stu-id="41c43-124">If not, the condition doesn't justify interrupting the user so it's better to suppress the warning.</span></span>
-   <span data-ttu-id="41c43-125">**條件是由使用者起始之動作的直接結果嗎？**</span><span class="sxs-lookup"><span data-stu-id="41c43-125">**Is the condition the direct result of an action initiated by the user?**</span></span> <span data-ttu-id="41c43-126">如果沒有，請考慮使用 [非重大的事件通知](mess-notif.md)。</span><span class="sxs-lookup"><span data-stu-id="41c43-126">If not, consider using a [non-critical event notifications](mess-notif.md).</span></span>
-   <span data-ttu-id="41c43-127">**條件是否為控制項中的特殊條件？**</span><span class="sxs-lookup"><span data-stu-id="41c43-127">**Is the condition a special condition in a control?**</span></span> <span data-ttu-id="41c43-128">如果是的話，請改用 [球形球形](ctrl-balloons.md) 。</span><span class="sxs-lookup"><span data-stu-id="41c43-128">If so, use a [balloon](ctrl-balloons.md) instead.</span></span>
-   <span data-ttu-id="41c43-129">**針對確認，使用者是否要執行具風險的動作？**</span><span class="sxs-lookup"><span data-stu-id="41c43-129">**For confirmations, is the user about to perform a risky action?**</span></span> <span data-ttu-id="41c43-130">如果是的話，如果動作有重大的後果或無法輕易復原，則會有適當的警告。</span><span class="sxs-lookup"><span data-stu-id="41c43-130">If so, a warning is appropriate if the action has significant consequences or cannot be easily undone.</span></span>
-   <span data-ttu-id="41c43-131">**針對其他類型的警告，使用者是否需要立即或立即行動？**</span><span class="sxs-lookup"><span data-stu-id="41c43-131">**For other types of warnings, does the user need to act now or in the immediate future?**</span></span> <span data-ttu-id="41c43-132">如果使用者可以在沒有立即發生問題的情況下持續運作，不顯示警告。</span><span class="sxs-lookup"><span data-stu-id="41c43-132">Don't display warnings if users can continue to work productively without immediate problems.</span></span> <span data-ttu-id="41c43-133">延後警告，直到條件更快速且相關。</span><span class="sxs-lookup"><span data-stu-id="41c43-133">Postpone the warning until the condition is more immediate and relevant.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="41c43-134">設計概念</span><span class="sxs-lookup"><span data-stu-id="41c43-134">Design concepts</span></span>

### <a name="avoid-overwarning"></a><span data-ttu-id="41c43-135">避免 overwarning</span><span class="sxs-lookup"><span data-stu-id="41c43-135">Avoid overwarning</span></span>

<span data-ttu-id="41c43-136">我們在 Microsoft Windows 程式中 overwarn。</span><span class="sxs-lookup"><span data-stu-id="41c43-136">We overwarn in Microsoft Windows programs.</span></span> <span data-ttu-id="41c43-137">一般的 Windows 程式在所有地方都有警告，有一點重要性的警告。</span><span class="sxs-lookup"><span data-stu-id="41c43-137">The typical Windows program has warnings seemingly everywhere, warning about things that have little significance.</span></span> <span data-ttu-id="41c43-138">在某些程式中，幾乎每個問題都會顯示為警告。</span><span class="sxs-lookup"><span data-stu-id="41c43-138">In some programs, nearly every question is presented as a warning.</span></span> <span data-ttu-id="41c43-139">Overwarning 讓程式感覺像是有害的活動，而且會使真正的重大問題。</span><span class="sxs-lookup"><span data-stu-id="41c43-139">Overwarning makes using a program feel like a hazardous activity, and it detracts from truly significant issues.</span></span>

<span data-ttu-id="41c43-140">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-140">**Incorrect:**</span></span>

![<span data-ttu-id="41c43-141">不必要警告訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-141">screen shot of an unnecessary warning message</span></span> ](images/mess-warn-image2.png)

<span data-ttu-id="41c43-142">Overwarning 讓您的程式感覺危險，並看起來像是由律師所設計。</span><span class="sxs-lookup"><span data-stu-id="41c43-142">Overwarning makes your program feel hazardous and look like it was designed by lawyers.</span></span>

<span data-ttu-id="41c43-143">單純的資料遺失或未來的問題可能就是呼叫警告的可能性不足。</span><span class="sxs-lookup"><span data-stu-id="41c43-143">The mere potential for data loss or a future problem alone is insufficient to call for a warning.</span></span> <span data-ttu-id="41c43-144">此外，任何非預期的結果都應該是非預期或非預期的結果，而且不容易更正。</span><span class="sxs-lookup"><span data-stu-id="41c43-144">Additionally, any undesirable results should be unexpected or unintended, and not easily corrected.</span></span> <span data-ttu-id="41c43-145">否則，您可以將任何使用者錯誤解釋為可能導致資料遺失或某個問題的潛在問題，並提供警告。</span><span class="sxs-lookup"><span data-stu-id="41c43-145">Otherwise, just about any user mistake could be construed to result in data loss or a potential problem of some kind and merit a warning.</span></span>

### <a name="characteristics-of-good-warnings"></a><span data-ttu-id="41c43-146">良好警告的特性</span><span class="sxs-lookup"><span data-stu-id="41c43-146">Characteristics of good warnings</span></span>

<span data-ttu-id="41c43-147">良好的警告：</span><span class="sxs-lookup"><span data-stu-id="41c43-147">Good warnings:</span></span>

-   <span data-ttu-id="41c43-148">**牽涉到風險。**</span><span class="sxs-lookup"><span data-stu-id="41c43-148">**Involve risk.**</span></span> <span data-ttu-id="41c43-149">良好的警告會警示使用者有重大問題。</span><span class="sxs-lookup"><span data-stu-id="41c43-149">Good warnings alert users of something significant.</span></span>

<span data-ttu-id="41c43-150">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-150">**Incorrect:**</span></span>

![<span data-ttu-id="41c43-151">[您要結束嗎？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-151">screen shot of 'do you want to exit?'</span></span> <span data-ttu-id="41c43-152">warning</span><span class="sxs-lookup"><span data-stu-id="41c43-152">warning</span></span> ](images/mess-warn-image3.png)

<span data-ttu-id="41c43-153">那又怎樣？</span><span class="sxs-lookup"><span data-stu-id="41c43-153">So what?</span></span> <span data-ttu-id="41c43-154">這項確認會假設使用者通常會意外離開程式。</span><span class="sxs-lookup"><span data-stu-id="41c43-154">This confirmation assumes that users often exit programs by accident.</span></span>

-   <span data-ttu-id="41c43-155">**具有立即相關性。**</span><span class="sxs-lookup"><span data-stu-id="41c43-155">**Have immediate relevance.**</span></span> <span data-ttu-id="41c43-156">使用者不但必須在意，他們現在必須在意。</span><span class="sxs-lookup"><span data-stu-id="41c43-156">Not only do users have to care, they have to care now.</span></span> <span data-ttu-id="41c43-157">使用者通常不會有興趣解決這些問題，因為他們現在可以進行工作。</span><span class="sxs-lookup"><span data-stu-id="41c43-157">Users typically aren't interested in problems they might have later as long as they can do their work now.</span></span>

<span data-ttu-id="41c43-158">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-158">**Incorrect:**</span></span>

![<span data-ttu-id="41c43-159">電池的螢幕擷取畫面-低-3 小時的警告</span><span class="sxs-lookup"><span data-stu-id="41c43-159">screen shot of battery-low-in-three-hours warning</span></span> ](images/mess-warn-image4.png)

<span data-ttu-id="41c43-160">在此情況下，最好是在三個小時內警告使用者。</span><span class="sxs-lookup"><span data-stu-id="41c43-160">In this case, it's better just to warn the user in three hours.</span></span>

-   <span data-ttu-id="41c43-161">**導致動作。**</span><span class="sxs-lookup"><span data-stu-id="41c43-161">**Lead to action.**</span></span> <span data-ttu-id="41c43-162">有一些使用者必須做的事，或是要注意的是警告的結果。</span><span class="sxs-lookup"><span data-stu-id="41c43-162">There is something users must do or be aware of as the result of the warning.</span></span> <span data-ttu-id="41c43-163">也許它們必須立即採取動作，或在未來的某個時間進行。</span><span class="sxs-lookup"><span data-stu-id="41c43-163">Perhaps they must take an action now or sometime in the immediate future.</span></span> <span data-ttu-id="41c43-164">可能會以不同的結果來執行工作。</span><span class="sxs-lookup"><span data-stu-id="41c43-164">Perhaps they will perform a task differently as a result.</span></span> <span data-ttu-id="41c43-165">忽略警告的結果應該是明確的。</span><span class="sxs-lookup"><span data-stu-id="41c43-165">The consequence of ignoring the warning should be clear.</span></span> <span data-ttu-id="41c43-166">沒有動作的警告只會讓使用者感覺擇善固執。</span><span class="sxs-lookup"><span data-stu-id="41c43-166">Warnings without actions just make users feel paranoid.</span></span>

<span data-ttu-id="41c43-167">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-167">**Incorrect:**</span></span>

![<span data-ttu-id="41c43-168">[即時 messenger 正在執行] 警告的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-168">screen shot of 'live messenger is running' warning</span></span> ](images/mess-warn-image5.png)

<span data-ttu-id="41c43-169">為什麼此通知會出現警告？</span><span class="sxs-lookup"><span data-stu-id="41c43-169">Why is this notification a warning?</span></span> <span data-ttu-id="41c43-170">使用者應該怎麼做 (在擔心) ？</span><span class="sxs-lookup"><span data-stu-id="41c43-170">What are users supposed to do (beside worry)?</span></span>

-   <span data-ttu-id="41c43-171">**不明顯。**</span><span class="sxs-lookup"><span data-stu-id="41c43-171">**Are not obvious.**</span></span> <span data-ttu-id="41c43-172">不要顯示警告來陳述動作的明顯結果。</span><span class="sxs-lookup"><span data-stu-id="41c43-172">Don't display a warning to state the obvious consequence of an action.</span></span> <span data-ttu-id="41c43-173">例如，假設使用者瞭解未完成工作的後果。</span><span class="sxs-lookup"><span data-stu-id="41c43-173">For example, assume users understand the consequences of not completing a task.</span></span>

<span data-ttu-id="41c43-174">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-174">**Incorrect:**</span></span>

![<span data-ttu-id="41c43-175">您要結束 wizard 的螢幕擷取畫面嗎？警告</span><span class="sxs-lookup"><span data-stu-id="41c43-175">screen shot of do you want to exit wizard? warning</span></span> ](images/mess-warn-image6.png)

<span data-ttu-id="41c43-176">取消不完整的 wizard 表示工作未完成 .。。誰知道？</span><span class="sxs-lookup"><span data-stu-id="41c43-176">Canceling an incomplete wizard means the task doesn't get done...who knew?</span></span>

-   <span data-ttu-id="41c43-177">**不常發生。**</span><span class="sxs-lookup"><span data-stu-id="41c43-177">**Occur infrequently.**</span></span> <span data-ttu-id="41c43-178">常數警告很快就會變得無效和討厭。</span><span class="sxs-lookup"><span data-stu-id="41c43-178">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="41c43-179">使用者通常會更專注于消除警告而非解決問題。</span><span class="sxs-lookup"><span data-stu-id="41c43-179">Users often become more focused on getting rid of the warning than addressing the problem.</span></span>

<span data-ttu-id="41c43-180">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-180">**Incorrect:**</span></span>

![<span data-ttu-id="41c43-181">[更新病毒碼標記] 警告的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-181">screen shot of 'update virus signatures' warning</span></span> ](images/mess-warn-image7.png)

<span data-ttu-id="41c43-182">使用者比較可能會專注于消除警告，而不是修正基礎問題。</span><span class="sxs-lookup"><span data-stu-id="41c43-182">Users are more likely to focus on getting rid of the warning than fixing the underlying problem.</span></span>

<span data-ttu-id="41c43-183">沒有這些特性的訊息可能仍然是很好的訊息，而不是好的警告。</span><span class="sxs-lookup"><span data-stu-id="41c43-183">A message that doesn't have these characteristics might still be a good message, just not a good warning.</span></span>

### <a name="determine-the-appropriate-message-type"></a><span data-ttu-id="41c43-184">判斷適當的訊息類型</span><span class="sxs-lookup"><span data-stu-id="41c43-184">Determine the appropriate message type</span></span>

<span data-ttu-id="41c43-185">根據強調和措辭，某些問題可能會顯示為錯誤、警告或資訊。</span><span class="sxs-lookup"><span data-stu-id="41c43-185">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="41c43-186">例如，假設網頁無法根據目前的 Windows Internet Explorer 設定載入未簽署的 ActiveX 控制項：</span><span class="sxs-lookup"><span data-stu-id="41c43-186">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

-   <span data-ttu-id="41c43-187">**錯誤。**</span><span class="sxs-lookup"><span data-stu-id="41c43-187">**Error.**</span></span> <span data-ttu-id="41c43-188">「此頁面無法載入未簽署的 ActiveX 控制項。」</span><span class="sxs-lookup"><span data-stu-id="41c43-188">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="41c43-189"> (片語做為現有的問題。 ) </span><span class="sxs-lookup"><span data-stu-id="41c43-189">(Phrased as an existing problem.)</span></span>
-   <span data-ttu-id="41c43-190">**警告。**</span><span class="sxs-lookup"><span data-stu-id="41c43-190">**Warning.**</span></span> <span data-ttu-id="41c43-191">「此頁面可能無法如預期般運作，因為 Windows Internet Explorer 未設定為載入未簽署的 ActiveX 控制項。」</span><span class="sxs-lookup"><span data-stu-id="41c43-191">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="41c43-192">或「允許此頁面安裝未簽署的 ActiveX 控制項？</span><span class="sxs-lookup"><span data-stu-id="41c43-192">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="41c43-193">從不受信任的來源執行此動作可能會危害您的電腦。」</span><span class="sxs-lookup"><span data-stu-id="41c43-193">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="41c43-194"> (這兩個片語為可能會導致未來問題的狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="41c43-194">(Both phrased as conditions that may cause future problems.)</span></span>
-   <span data-ttu-id="41c43-195">**資訊。**</span><span class="sxs-lookup"><span data-stu-id="41c43-195">**Information.**</span></span> <span data-ttu-id="41c43-196">「您已設定 Windows Internet Explorer 封鎖未簽署的 ActiveX 控制項。」</span><span class="sxs-lookup"><span data-stu-id="41c43-196">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="41c43-197"> (片語作為事實的陳述。 ) </span><span class="sxs-lookup"><span data-stu-id="41c43-197">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="41c43-198">**若要判斷適當的訊息類型，請將焦點放在使用者需要知道或採取行動之問題的最重要層面。**</span><span class="sxs-lookup"><span data-stu-id="41c43-198">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="41c43-199">一般來說，如果問題封鎖使用者繼續進行，您應該將它顯示為錯誤;如果使用者可以繼續，請將它顯示為警告。</span><span class="sxs-lookup"><span data-stu-id="41c43-199">Typically, if an issue blocks the user from proceeding, you should present it as an error; if the user can proceed, present it as a warning.</span></span> <span data-ttu-id="41c43-200">根據焦點製作 [主要指示](text-ui.md) 或其他對應的文字，然後選擇符合文字的圖示 ([標準](vis-std-icons.md) 或) 。</span><span class="sxs-lookup"><span data-stu-id="41c43-200">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, then choose an icon ([standard](vis-std-icons.md) or otherwise) that matches the text.</span></span> <span data-ttu-id="41c43-201">主要的指令文字和圖示應該一律相符。</span><span class="sxs-lookup"><span data-stu-id="41c43-201">The main instruction text and icons should always match.</span></span>

### <a name="be-specific"></a><span data-ttu-id="41c43-202">特定</span><span class="sxs-lookup"><span data-stu-id="41c43-202">Be specific</span></span>

<span data-ttu-id="41c43-203">當下列資訊是特定且明確的時，警告會更吸引人：</span><span class="sxs-lookup"><span data-stu-id="41c43-203">Warnings are more compelling when the following information is specific and clear:</span></span>

-   <span data-ttu-id="41c43-204">警告的來源。</span><span class="sxs-lookup"><span data-stu-id="41c43-204">The source of the warning.</span></span>
-   <span data-ttu-id="41c43-205">特定條件和潛在問題。</span><span class="sxs-lookup"><span data-stu-id="41c43-205">The specific condition and potential problem.</span></span>
-   <span data-ttu-id="41c43-206">使用者應怎麼做。</span><span class="sxs-lookup"><span data-stu-id="41c43-206">What the user should do about it.</span></span>
-   <span data-ttu-id="41c43-207">如果使用者沒有執行任何動作，會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="41c43-207">What happens if the user doesn't do anything.</span></span>

<span data-ttu-id="41c43-208">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-208">**Incorrect:**</span></span>

![<span data-ttu-id="41c43-209">明顯風險清楚警告的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-209">screen shot of vague warning of significant risk</span></span> ](images/mess-warn-image8.png)

<span data-ttu-id="41c43-210">在此範例中，可能發生的問題為何？</span><span class="sxs-lookup"><span data-stu-id="41c43-210">In this example, what is the potential problem?</span></span> <span data-ttu-id="41c43-211">除了無法透過網路使用投影機之外，使用者應做什麼？</span><span class="sxs-lookup"><span data-stu-id="41c43-211">What is the user supposed to do, aside from not using the projector over the network?</span></span> <span data-ttu-id="41c43-212">如果沒有更明確的資訊，使用者就無法繼續進行。</span><span class="sxs-lookup"><span data-stu-id="41c43-212">Without more specific information, all the user can do is feel bad about proceeding.</span></span>

<span data-ttu-id="41c43-213">**正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-213">**Correct:**</span></span>

![<span data-ttu-id="41c43-214">問題和結果警告的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-214">screen shot of warning of problem and consequences</span></span> ](images/mess-warn-image9.png)

<span data-ttu-id="41c43-215">在此範例中，問題和後果很清楚。</span><span class="sxs-lookup"><span data-stu-id="41c43-215">In this example, the problem and consequences are clear.</span></span>

<span data-ttu-id="41c43-216">有時候可能會有一個合法的潛在問題可告知使用者，但不知道解決方案和後果。</span><span class="sxs-lookup"><span data-stu-id="41c43-216">Sometimes there is a legitimate potential problem worthy of informing users about, but the solution and consequences aren't known for sure.</span></span> <span data-ttu-id="41c43-217">您可以提供最有可能的資訊或最常見的範例，而不是提供不明確的警告。</span><span class="sxs-lookup"><span data-stu-id="41c43-217">Rather than give a vague warning, be specific by giving the most likely information or the most common example.</span></span>

<span data-ttu-id="41c43-218">**正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-218">**Correct:**</span></span>

![<span data-ttu-id="41c43-219">網路錯誤警告和解決方案的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-219">screen shot of network error warning and solutions</span></span> ](images/mess-warn-image10.png)

<span data-ttu-id="41c43-220">在此範例中，提供最有可能的解決方案來使警告成為特定的。</span><span class="sxs-lookup"><span data-stu-id="41c43-220">In this example, the warning is made specific by providing the most likely solution.</span></span>

<span data-ttu-id="41c43-221">不過，在這種情況下，請使用表示其他可能性的用語。</span><span class="sxs-lookup"><span data-stu-id="41c43-221">However, in such cases, use wording that indicates that there are other possibilities.</span></span> <span data-ttu-id="41c43-222">否則，使用者可能會誤導。</span><span class="sxs-lookup"><span data-stu-id="41c43-222">Otherwise, users might be misled.</span></span>

<span data-ttu-id="41c43-223">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-223">**Incorrect:**</span></span>

![<span data-ttu-id="41c43-224">網路纜線已拔掉警告的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-224">screen shot of network cable unplugged warning</span></span> ](images/mess-warn-image11.png)

<span data-ttu-id="41c43-225">**正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-225">**Correct:**</span></span>

![<span data-ttu-id="41c43-226">纜線的螢幕擷取畫面可能已被拔掉警告</span><span class="sxs-lookup"><span data-stu-id="41c43-226">screen shot of cable might be unplugged warning</span></span> ](images/mess-warn-image12.png)

<span data-ttu-id="41c43-227">在不正確的範例中，如果已清楚地插入纜線，使用者將會混淆。</span><span class="sxs-lookup"><span data-stu-id="41c43-227">In the incorrect example, users will be confused if the cable is clearly plugged in.</span></span>

<span data-ttu-id="41c43-228">**如果您只進行兩件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="41c43-228">**If you do only two things...**</span></span>

1. <span data-ttu-id="41c43-229">不要 overwarn。</span><span class="sxs-lookup"><span data-stu-id="41c43-229">Don't overwarn.</span></span> <span data-ttu-id="41c43-230">將警告限制為牽涉到風險且立即相關、可採取動作、不明顯且不頻繁的狀況。</span><span class="sxs-lookup"><span data-stu-id="41c43-230">Limit warnings to conditions that involve risk and are immediately relevant, actionable, not obvious, and infrequent.</span></span> <span data-ttu-id="41c43-231">否則，請移除或改寫訊息。</span><span class="sxs-lookup"><span data-stu-id="41c43-231">Otherwise, remove or rephrase the message.</span></span>

2. <span data-ttu-id="41c43-232">提供特定且有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="41c43-232">Provide specific, useful information.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="41c43-233">使用模式</span><span class="sxs-lookup"><span data-stu-id="41c43-233">Usage patterns</span></span>

<span data-ttu-id="41c43-234">警告有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="41c43-234">Warnings have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="41c43-235"><strong>注意</strong></span><span class="sxs-lookup"><span data-stu-id="41c43-235"><strong>Awareness</strong></span></span><br/> <span data-ttu-id="41c43-236">讓使用者知道狀況或潛在的問題，但使用者可能不需要立即執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="41c43-236">Make user aware of a condition or potential problem, but user may not have to do anything now.</span></span> <br/></td>
<td><img src="images/mess-warn-image13.png" alt="Screen shot of warning of network problems " /><br/> <img src="images/mess-warn-image14.png" alt="Screen shot of low-battery warning " /><br/> <img src="images/mess-warn-image15.png" alt="Screen shot of &#39;caps-lock-is-on&#39; warning " /><br/> <img src="images/mess-warn-image16.png" alt="Screen shot of &#39;TPM-not-found&#39; warning " /><br/> <span data-ttu-id="41c43-237">認知警告的範例。</span><span class="sxs-lookup"><span data-stu-id="41c43-237">Examples of awareness warnings.</span></span><br/> <span data-ttu-id="41c43-238">認知警告有下列展示：</span><span class="sxs-lookup"><span data-stu-id="41c43-238">Awareness warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="41c43-239"><strong>主要指示：</strong> 描述條件或潛在問題。</span><span class="sxs-lookup"><span data-stu-id="41c43-239"><strong>Main instruction:</strong> Describe the condition or potential problem.</span></span></li>
<li><span data-ttu-id="41c43-240"><strong>補充指示：</strong> 解釋隱含意義，以及其重要性。</span><span class="sxs-lookup"><span data-stu-id="41c43-240"><strong>Supplemental instruction:</strong> Explain the implication and why it is important.</span></span></li>
<li><span data-ttu-id="41c43-241"><strong>認可按鈕：</strong> 關閉。</span><span class="sxs-lookup"><span data-stu-id="41c43-241"><strong>Commit buttons:</strong> Close.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c43-242"><strong>錯誤預防</strong></span><span class="sxs-lookup"><span data-stu-id="41c43-242"><strong>Error prevention</strong></span></span><br/> <span data-ttu-id="41c43-243">讓使用者知道可能會妨礙問題的資訊，特別是在進行選擇時。</span><span class="sxs-lookup"><span data-stu-id="41c43-243">Make user aware of information that might prevent a problem, especially when making choices.</span></span> <br/></td>
<td><span data-ttu-id="41c43-244">錯誤防護警告最適合使用就地警告圖示和解說文字來呈現。</span><span class="sxs-lookup"><span data-stu-id="41c43-244">Error prevention warnings are best presented using an in-place warning icon and explanatory text.</span></span> <br/> <img src="images/mess-warn-image17.png" alt="Screen shot of Not-enough-free-space warning " /><br/> <img src="images/mess-warn-image18.png" alt="Screen shot of Use-installation-CD warning " /><br/> <span data-ttu-id="41c43-245">錯誤預防警告的範例。</span><span class="sxs-lookup"><span data-stu-id="41c43-245">Examples of error prevention warnings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="41c43-246"><strong>即將發生問題</strong></span><span class="sxs-lookup"><span data-stu-id="41c43-246"><strong>Imminent problem</strong></span></span><br/> <span data-ttu-id="41c43-247">使用者現在需要進行一些動作，以防止發生問題。</span><span class="sxs-lookup"><span data-stu-id="41c43-247">The user needs to do something now to prevent an imminent problem.</span></span> <br/></td>
<td><img src="images/mess-warn-image19.png" alt="Screen shot of Close-programs warning " /><br/> <span data-ttu-id="41c43-248">即將發生的問題警告範例。</span><span class="sxs-lookup"><span data-stu-id="41c43-248">An example of an imminent problem warning.</span></span><br/> <span data-ttu-id="41c43-249">即將發生的問題警告有下列展示：</span><span class="sxs-lookup"><span data-stu-id="41c43-249">Imminent problem warnings have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="41c43-250"><strong>主要指示：</strong> 描述使用者現在需要做什麼。</span><span class="sxs-lookup"><span data-stu-id="41c43-250"><strong>Main instruction:</strong> Describe what the user needs to do now.</span></span></li>
<li><span data-ttu-id="41c43-251"><strong>補充指示：</strong> 說明條件以及其重要性。</span><span class="sxs-lookup"><span data-stu-id="41c43-251"><strong>Supplemental instruction:</strong> Explain the condition and why it is important.</span></span></li>
<li><span data-ttu-id="41c43-252"><strong>認可按鈕：</strong> 每個選項的命令按鈕或命令連結，如果動作發生在對話方塊外，則為 [確定]。</span><span class="sxs-lookup"><span data-stu-id="41c43-252"><strong>Commit buttons:</strong> A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="41c43-253"><strong>有風險的動作確認</strong></span><span class="sxs-lookup"><span data-stu-id="41c43-253"><strong>Risky action confirmation</strong></span></span><br/> <span data-ttu-id="41c43-254">確認使用者想要繼續進行有一些風險且無法輕易復原的動作。</span><span class="sxs-lookup"><span data-stu-id="41c43-254">Confirm that the user wants to proceed with an action that has some risk and can't be easily undone.</span></span> <br/></td>
<td><img src="images/mess-warn-image20.png" alt="Screen shot of Formatting-will-erase-data warning " /><br/> <span data-ttu-id="41c43-255">具風險動作確認的範例。</span><span class="sxs-lookup"><span data-stu-id="41c43-255">An example of risky action confirmation.</span></span><br/> <span data-ttu-id="41c43-256">具風險的動作確認有下列展示：</span><span class="sxs-lookup"><span data-stu-id="41c43-256">Risky action confirmations have the following presentation:</span></span> <br/>
<ul>
<li><span data-ttu-id="41c43-257"><strong>主要指示：</strong> 詢問問題，以判斷使用者是否想要繼續進行。</span><span class="sxs-lookup"><span data-stu-id="41c43-257"><strong>Main instruction:</strong> Ask a question to determine if the user wants to proceed.</span></span></li>
<li><span data-ttu-id="41c43-258"><strong>補充指示：</strong> 說明使用者可能不想繼續的任何非明顯原因。</span><span class="sxs-lookup"><span data-stu-id="41c43-258"><strong>Supplemental instruction:</strong> Explain any non-obvious reasons why the user might not want to proceed.</span></span></li>
<li><span data-ttu-id="41c43-259"><strong>認可按鈕：</strong> 是，否。</span><span class="sxs-lookup"><span data-stu-id="41c43-259"><strong>Commit buttons:</strong> Yes, No.</span></span></li>
</ul>
<span data-ttu-id="41c43-260">如需此模式的指導方針，請參閱 <a href="mess-confirm.md">確認</a>。</span><span class="sxs-lookup"><span data-stu-id="41c43-260">For guidelines on this pattern, see <a href="mess-confirm.md">Confirmations</a>.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="41c43-261">指導方針</span><span class="sxs-lookup"><span data-stu-id="41c43-261">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="41c43-262">簡報</span><span class="sxs-lookup"><span data-stu-id="41c43-262">Presentation</span></span>

-   <span data-ttu-id="41c43-263">**選擇以資訊類型為基礎的展示 UI：**</span><span class="sxs-lookup"><span data-stu-id="41c43-263">**Choose the presentation UI based on the type of information:**</span></span>



|                               |                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41c43-264">**User Interface** (使用者介面)</span><span class="sxs-lookup"><span data-stu-id="41c43-264">**User interface**</span></span><br/> | <span data-ttu-id="41c43-265">**最適合用於**</span><span class="sxs-lookup"><span data-stu-id="41c43-265">**Best used for**</span></span><br/>                                                                                                           |
| <span data-ttu-id="41c43-266">強制回應對話方塊</span><span class="sxs-lookup"><span data-stu-id="41c43-266">Modal dialog boxes</span></span><br/> | <span data-ttu-id="41c43-267">重大警告 (包括使用者必須立即回應的確認) 。</span><span class="sxs-lookup"><span data-stu-id="41c43-267">Critical warnings (including confirmations) that users must respond to now.</span></span><br/>                                                 |
| <span data-ttu-id="41c43-268">就地</span><span class="sxs-lookup"><span data-stu-id="41c43-268">In-place</span></span><br/>           | <span data-ttu-id="41c43-269">可能會妨礙問題的資訊，特別是當使用者進行選擇時。</span><span class="sxs-lookup"><span data-stu-id="41c43-269">Information that might prevent a problem, especially when users are making choices.</span></span><br/>                                         |
| <span data-ttu-id="41c43-270">橫幅</span><span class="sxs-lookup"><span data-stu-id="41c43-270">Banners</span></span><br/>            | <span data-ttu-id="41c43-271">可能會妨礙問題的資訊，特別是在完成工作的相關資訊時。</span><span class="sxs-lookup"><span data-stu-id="41c43-271">Information that might prevent a problem, especially when related to completing a task.</span></span><br/>                                     |
| <span data-ttu-id="41c43-272">通知</span><span class="sxs-lookup"><span data-stu-id="41c43-272">Notifications</span></span><br/>      | <span data-ttu-id="41c43-273">可放心忽略的重大事件或狀態（至少暫時）。</span><span class="sxs-lookup"><span data-stu-id="41c43-273">Significant events or status that can be safely ignored, at least temporarily.</span></span><br/>                                              |
| <span data-ttu-id="41c43-274">汽球</span><span class="sxs-lookup"><span data-stu-id="41c43-274">Balloons</span></span><br/>           | <span data-ttu-id="41c43-275">控制項處於影響輸入的狀態。</span><span class="sxs-lookup"><span data-stu-id="41c43-275">A control is in a state that affects input.</span></span> <span data-ttu-id="41c43-276">此狀態可能是非預期的，使用者可能不會察覺到輸入受到影響。</span><span class="sxs-lookup"><span data-stu-id="41c43-276">This state is likely unintended and the user may not realize input is affected.</span></span><br/> |



 

-   <span data-ttu-id="41c43-277">**針對強制回應對話方塊：**</span><span class="sxs-lookup"><span data-stu-id="41c43-277">**For modal dialog boxes:**</span></span>
    -   <span data-ttu-id="41c43-278">**在適當時使用工作對話方塊，以達成一致的外觀和配置。**</span><span class="sxs-lookup"><span data-stu-id="41c43-278">**Use task dialogs whenever appropriate to achieve a consistent look and layout.**</span></span> <span data-ttu-id="41c43-279">工作對話方塊需要 Windows Vista 或更新版本，因此不適用於舊版 Windows。</span><span class="sxs-lookup"><span data-stu-id="41c43-279">Task dialogs require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span>
    -   <span data-ttu-id="41c43-280">**每個條件只顯示一則警告訊息。**</span><span class="sxs-lookup"><span data-stu-id="41c43-280">**Display only one warning message per condition.**</span></span> <span data-ttu-id="41c43-281">例如，顯示單一警告以完整說明條件，而不是每個訊息一次描述一個詳細資料。</span><span class="sxs-lookup"><span data-stu-id="41c43-281">For example, display a single warning that completely explains a condition instead of describing it one detail at a time per message.</span></span> <span data-ttu-id="41c43-282">針對單一條件顯示一系列的警告對話方塊會造成混淆和討厭。</span><span class="sxs-lookup"><span data-stu-id="41c43-282">Displaying a sequence of warning dialogs for a single condition is confusing and annoying.</span></span>
    -   <span data-ttu-id="41c43-283">**請勿針對每個條件顯示一次以上的警告。**</span><span class="sxs-lookup"><span data-stu-id="41c43-283">**Don't display a warning more than once per condition.**</span></span> <span data-ttu-id="41c43-284">常數警告很快就會變得無效和討厭。</span><span class="sxs-lookup"><span data-stu-id="41c43-284">Constant warnings quickly become ineffective and annoying.</span></span> <span data-ttu-id="41c43-285">使用者通常會更專注于消除警告而非解決問題。</span><span class="sxs-lookup"><span data-stu-id="41c43-285">Users often become more focused on getting rid of the warning than addressing the problem.</span></span> <span data-ttu-id="41c43-286">如果您必須針對單一條件重複發出警告，請使用 [漸進式擴大](mess-notif.md)。</span><span class="sxs-lookup"><span data-stu-id="41c43-286">If you must warn repeatedly for a single condition, use [progressive escalation](mess-notif.md).</span></span>
-   <span data-ttu-id="41c43-287">**不要伴隨有音效效果或嗶聲的警告。**</span><span class="sxs-lookup"><span data-stu-id="41c43-287">**Don't accompany warnings with a sound effect or beep.**</span></span> <span data-ttu-id="41c43-288">這麼做是 jarring 且不必要的。</span><span class="sxs-lookup"><span data-stu-id="41c43-288">Doing so is jarring and unnecessary.</span></span>
    -   <span data-ttu-id="41c43-289">**例外狀況：** 如果使用者必須立即回應，您可以使用音效效果。</span><span class="sxs-lookup"><span data-stu-id="41c43-289">**Exception:** If the user must respond immediately, you can use a sound effect.</span></span>

### <a name="icons"></a><span data-ttu-id="41c43-290">圖示</span><span class="sxs-lookup"><span data-stu-id="41c43-290">Icons</span></span>

-   <span data-ttu-id="41c43-291">請勿在對話方塊的標題列中放置警告圖示。</span><span class="sxs-lookup"><span data-stu-id="41c43-291">Don't place a warning icon in the title bar of a dialog box.</span></span>
-   <span data-ttu-id="41c43-292">**使用警告圖示。**</span><span class="sxs-lookup"><span data-stu-id="41c43-292">**Use a warning icon.**</span></span> <span data-ttu-id="41c43-293">例外狀況：</span><span class="sxs-lookup"><span data-stu-id="41c43-293">Exceptions:</span></span>
    -   <span data-ttu-id="41c43-294">如果有圖示的功能出現警告，您可以使用功能圖示搭配警告重迭。</span><span class="sxs-lookup"><span data-stu-id="41c43-294">If the warning is for a feature that has an icon, you can use the feature icon with a warning overlay.</span></span>

        <span data-ttu-id="41c43-295">**正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-295">**Correct:**</span></span>

        ![<span data-ttu-id="41c43-296">具有警告圖示重迭的鎖定圖示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-296">screen shot of lock icon with warning icon overlay</span></span> ](images/mess-warn-image21.png)

        <span data-ttu-id="41c43-297">在此範例中，功能圖示會有警告重迭。</span><span class="sxs-lookup"><span data-stu-id="41c43-297">In this example, the feature icon has a warning overlay.</span></span>

-   <span data-ttu-id="41c43-298">針對具有警告註腳的強制回應對話方塊，請將警告圖示放在註腳而非內容區域中。</span><span class="sxs-lookup"><span data-stu-id="41c43-298">For modal dialog boxes with a warning footnote, put the warning icon in the footnote instead of the content area.</span></span>

    <span data-ttu-id="41c43-299">**正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-299">**Correct:**</span></span>

    ![<span data-ttu-id="41c43-300">對話方塊註腳中警告圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-300">screen shot of warning icon in dialog-box footnote</span></span> ](images/mess-warn-image22.png)

    <span data-ttu-id="41c43-301">在此範例中，註腳具有警告圖示。</span><span class="sxs-lookup"><span data-stu-id="41c43-301">In this example, the footnote has the warning icon.</span></span>

<span data-ttu-id="41c43-302">如需更多指導方針和範例，請參閱 [標準圖示](vis-std-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="41c43-302">For more guidelines and examples, see [Standard Icons](vis-std-icons.md).</span></span>

### <a name="dont-show-this-message-again"></a><span data-ttu-id="41c43-303">不要再顯示此訊息</span><span class="sxs-lookup"><span data-stu-id="41c43-303">Don't show this message again</span></span>

-   <span data-ttu-id="41c43-304">**如果警告對話方塊需要此選項，請重新考慮警告和其頻率。**</span><span class="sxs-lookup"><span data-stu-id="41c43-304">**If a warning dialog box needs this option, reconsider the warning and its frequency.**</span></span> <span data-ttu-id="41c43-305">如果它具有良好警告的所有特性 (牽涉到風險，而且立即相關、可採取動作、不明顯且不頻繁的) ，使用者就不能將它隱藏起來。</span><span class="sxs-lookup"><span data-stu-id="41c43-305">If it has all the characteristics of a good warning (involves risk, and is immediately relevant, actionable, not obvious, and infrequent), it shouldn't make sense for users to suppress it.</span></span>

<span data-ttu-id="41c43-306">如需詳細指導方針，請參閱 [對話方塊](win-dialog-box.md)。</span><span class="sxs-lookup"><span data-stu-id="41c43-306">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="41c43-307">漸進式揭露</span><span class="sxs-lookup"><span data-stu-id="41c43-307">Progressive disclosure</span></span>

-   <span data-ttu-id="41c43-308">**如果您必須在警告訊息中包含 advanced 資訊，請使用累進洩漏按鈕加以顯示** (例如「顯示詳細資料」 ) 。</span><span class="sxs-lookup"><span data-stu-id="41c43-308">**If you must include advanced information in a warning message, reveal it by using progressive disclosure buttons** (for example, "Show details").</span></span> <span data-ttu-id="41c43-309">這麼做可簡化一般使用方式的警告。</span><span class="sxs-lookup"><span data-stu-id="41c43-309">Doing so simplifies the warning for typical usage.</span></span> <span data-ttu-id="41c43-310">請勿隱藏所需的資訊，因為使用者可能找不到它。</span><span class="sxs-lookup"><span data-stu-id="41c43-310">Don't hide needed information because users might not find it.</span></span>
-   <span data-ttu-id="41c43-311">**除非真的有更多詳細資料，否則請不要使用 [顯示詳細資料]。**</span><span class="sxs-lookup"><span data-stu-id="41c43-311">**Don't use "Show details" unless there really is more detail.**</span></span> <span data-ttu-id="41c43-312">請勿只以不同的格式重新聲明現有的資訊。</span><span class="sxs-lookup"><span data-stu-id="41c43-312">Don't just restate the existing information in a different format.</span></span>

<span data-ttu-id="41c43-313">如需標籤指導方針，請參閱 [漸進式洩漏](ctrl-progressive-disclosure-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="41c43-313">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="41c43-314">預設值</span><span class="sxs-lookup"><span data-stu-id="41c43-314">Default values</span></span>

-   <span data-ttu-id="41c43-315">**選取最安全、最不具破壞性或最安全的回應作為預設值。**</span><span class="sxs-lookup"><span data-stu-id="41c43-315">**Select the safest, least destructive, or most secure response to be the default.**</span></span>

## <a name="text"></a><span data-ttu-id="41c43-316">Text</span><span class="sxs-lookup"><span data-stu-id="41c43-316">Text</span></span>

### <a name="general"></a><span data-ttu-id="41c43-317">一般</span><span class="sxs-lookup"><span data-stu-id="41c43-317">General</span></span>

-   <span data-ttu-id="41c43-318">**移除多餘的文字。**</span><span class="sxs-lookup"><span data-stu-id="41c43-318">**Remove redundant text.**</span></span> <span data-ttu-id="41c43-319">在標題、主要指示、補充指示、內容區域、命令連結和認可按鈕中尋找。</span><span class="sxs-lookup"><span data-stu-id="41c43-319">Look for it in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="41c43-320">一般而言，請在指示和互動式控制項中保留完整文字，然後從其他位置移除任何多餘的。</span><span class="sxs-lookup"><span data-stu-id="41c43-320">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="41c43-321">**請勿在文字中使用「警告」或「警告」字詞。**</span><span class="sxs-lookup"><span data-stu-id="41c43-321">**Don't use the terms "warning" or "caution" in the text.**</span></span> <span data-ttu-id="41c43-322">當 [正確使用](vis-std-icons.md)時，警告圖示可充分地傳達使用者必須謹慎地進行通訊。</span><span class="sxs-lookup"><span data-stu-id="41c43-322">When [used correctly](vis-std-icons.md), the warning icon sufficiently communicates that users must proceed with caution.</span></span>

<span data-ttu-id="41c43-323">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-323">**Incorrect:**</span></span>

![<span data-ttu-id="41c43-324">文字中不必要使用警告的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-324">screen shot of unnecessary use of warning in text</span></span> ](images/mess-warn-image23.png)

<span data-ttu-id="41c43-325">在此範例中，「警告」一詞是不必要的。</span><span class="sxs-lookup"><span data-stu-id="41c43-325">In this example, the term "warning" is unnecessary.</span></span>

### <a name="titles"></a><span data-ttu-id="41c43-326">標題</span><span class="sxs-lookup"><span data-stu-id="41c43-326">Titles</span></span>

-   <span data-ttu-id="41c43-327">**使用標題來識別警告來源的命令或功能。**</span><span class="sxs-lookup"><span data-stu-id="41c43-327">**Use the title to identify the command or feature where the warning came from.**</span></span> <span data-ttu-id="41c43-328">例外狀況：</span><span class="sxs-lookup"><span data-stu-id="41c43-328">Exceptions:</span></span>
    -   <span data-ttu-id="41c43-329">如果有許多不同的命令顯示警告，請考慮改為使用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="41c43-329">If a warning is displayed by many different commands, consider using the program name instead.</span></span>
    -   <span data-ttu-id="41c43-330">如果該標題是多餘的，或與主要指示混淆，請改用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="41c43-330">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>

<span data-ttu-id="41c43-331">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-331">**Incorrect:**</span></span>

![<span data-ttu-id="41c43-332">安全性警告對話方塊標題的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-332">screen shot of security warning dialog box title</span></span> ](images/mess-warn-image24.png)

<span data-ttu-id="41c43-333">在此範例中，「安全性警告」不會識別警告來源的命令或功能。</span><span class="sxs-lookup"><span data-stu-id="41c43-333">In this example, "Security Warning" doesn't identify the command or feature where the warning came from.</span></span>

-   <span data-ttu-id="41c43-334">**請勿使用標題來說明在主要指令用途的對話方塊中要執行** 的動作。</span><span class="sxs-lookup"><span data-stu-id="41c43-334">**Don't use the title to explain what to do in the dialog** that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="41c43-335">使用 [標題樣式的大小寫](glossary.md)，但不含結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="41c43-335">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="41c43-336">主要指示</span><span class="sxs-lookup"><span data-stu-id="41c43-336">Main instructions</span></span>

-   <span data-ttu-id="41c43-337">警告的主要指示是根據其設計模式：</span><span class="sxs-lookup"><span data-stu-id="41c43-337">The main instruction for a warning is based on its design pattern:</span></span>



|                                      |                                                                      |
|--------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="41c43-338">**模式**</span><span class="sxs-lookup"><span data-stu-id="41c43-338">**Pattern**</span></span><br/>               | <span data-ttu-id="41c43-339">**主要指示**</span><span class="sxs-lookup"><span data-stu-id="41c43-339">**Main instruction**</span></span><br/>                                      |
| <span data-ttu-id="41c43-340">感知</span><span class="sxs-lookup"><span data-stu-id="41c43-340">Awareness</span></span><br/>                 | <span data-ttu-id="41c43-341">描述條件或潛在問題。</span><span class="sxs-lookup"><span data-stu-id="41c43-341">Describe the condition or potential problem.</span></span><br/>              |
| <span data-ttu-id="41c43-342">即將發生問題</span><span class="sxs-lookup"><span data-stu-id="41c43-342">Imminent problem</span></span><br/>          | <span data-ttu-id="41c43-343">描述使用者現在需要做什麼。</span><span class="sxs-lookup"><span data-stu-id="41c43-343">Describe what the user needs to do now.</span></span><br/>                   |
| <span data-ttu-id="41c43-344">有風險的動作確認</span><span class="sxs-lookup"><span data-stu-id="41c43-344">Risky action confirmation</span></span><br/> | <span data-ttu-id="41c43-345">詢問問題，以判斷使用者是否想要繼續進行。</span><span class="sxs-lookup"><span data-stu-id="41c43-345">Ask a question to determine if the user wants to proceed.</span></span><br/> |



 

-   ![<span data-ttu-id="41c43-346">電力偏低通知的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-346">screen shot of a low-battery notification</span></span> ](images/mess-warn-image25.png)
-   <span data-ttu-id="41c43-347">在此範例中，電力偏低通知是感知警告，因此主要指示會說明此狀況。</span><span class="sxs-lookup"><span data-stu-id="41c43-347">In this example, the low battery notification is an awareness warning, so the main instruction describes the condition.</span></span>
-   ![<span data-ttu-id="41c43-348">立即變更電池警告的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-348">screen shot of change battery immediately warning</span></span> ](images/mess-warn-image1.png)
-   <span data-ttu-id="41c43-349">在此範例中，[低電池] 對話方塊是即將發生的問題，因此主要指示描述使用者現在需要做什麼。</span><span class="sxs-lookup"><span data-stu-id="41c43-349">In this example, the low battery dialog box is an imminent problem, so the main instruction describes what the user needs to do now.</span></span>
-   <span data-ttu-id="41c43-350">**請務必只使用單一的完整句子。**</span><span class="sxs-lookup"><span data-stu-id="41c43-350">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="41c43-351">將主要指示帶到基本資訊。</span><span class="sxs-lookup"><span data-stu-id="41c43-351">Strip the main instruction down to the essential information.</span></span> <span data-ttu-id="41c43-352">如果您必須進一步說明，請使用補充指示。</span><span class="sxs-lookup"><span data-stu-id="41c43-352">If you must explain anything more, use a supplemental instruction.</span></span>
-   <span data-ttu-id="41c43-353">**如果使用者必須立即採取行動，請使用「立即」和「立即」等字。**</span><span class="sxs-lookup"><span data-stu-id="41c43-353">**Use words like "now" and "immediately" if the user must act immediately.**</span></span> <span data-ttu-id="41c43-354">如果沒有緊急，請不要使用這些字組。</span><span class="sxs-lookup"><span data-stu-id="41c43-354">Don't use these words if there is no urgency.</span></span>
-   <span data-ttu-id="41c43-355">**如果有相關的物件，請特別提供其完整名稱。**</span><span class="sxs-lookup"><span data-stu-id="41c43-355">**Be specific if there are objects involved, give their full names.**</span></span>
-   <span data-ttu-id="41c43-356">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="41c43-356">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="41c43-357">補充指示</span><span class="sxs-lookup"><span data-stu-id="41c43-357">Supplemental instructions</span></span>

-   <span data-ttu-id="41c43-358">警告的補充指示是根據其設計模式：</span><span class="sxs-lookup"><span data-stu-id="41c43-358">The supplemental instruction for a warning is based on its design pattern:</span></span>



|                                      |                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="41c43-359">**模式**</span><span class="sxs-lookup"><span data-stu-id="41c43-359">**Pattern**</span></span><br/>               | <span data-ttu-id="41c43-360">**補充指示**</span><span class="sxs-lookup"><span data-stu-id="41c43-360">**Supplemental instruction**</span></span><br/>                                            |
| <span data-ttu-id="41c43-361">感知</span><span class="sxs-lookup"><span data-stu-id="41c43-361">Awareness</span></span><br/>                 | <span data-ttu-id="41c43-362">解釋隱含意義，以及其重要性。</span><span class="sxs-lookup"><span data-stu-id="41c43-362">Explain the implication and why it is important.</span></span><br/>                        |
| <span data-ttu-id="41c43-363">即將發生問題</span><span class="sxs-lookup"><span data-stu-id="41c43-363">Imminent problem</span></span><br/>          | <span data-ttu-id="41c43-364">說明條件以及其重要性。</span><span class="sxs-lookup"><span data-stu-id="41c43-364">Explain the condition and why it is important.</span></span><br/>                          |
| <span data-ttu-id="41c43-365">有風險的動作確認</span><span class="sxs-lookup"><span data-stu-id="41c43-365">Risky action confirmation</span></span><br/> | <span data-ttu-id="41c43-366">說明使用者可能不想繼續的任何非明顯原因。</span><span class="sxs-lookup"><span data-stu-id="41c43-366">Explain any non-obvious reasons why the user might not want to proceed.</span></span><br/> |



 

-   <span data-ttu-id="41c43-367">**請勿以稍微不同的用語重複主要指令。**</span><span class="sxs-lookup"><span data-stu-id="41c43-367">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="41c43-368">相反地，如果沒有其他要新增的指令，請省略補充指令。</span><span class="sxs-lookup"><span data-stu-id="41c43-368">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="41c43-369">使用完整句子、句子樣式的大小寫和結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="41c43-369">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="41c43-370">認可按鈕</span><span class="sxs-lookup"><span data-stu-id="41c43-370">Commit buttons</span></span>

-   <span data-ttu-id="41c43-371">在警告對話方塊中，認可按鈕是根據其設計模式：</span><span class="sxs-lookup"><span data-stu-id="41c43-371">For warning dialog boxes, the commit buttons are based on its design pattern:</span></span>



|                                      |                                                                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41c43-372">**模式**</span><span class="sxs-lookup"><span data-stu-id="41c43-372">**Pattern**</span></span><br/>               | <span data-ttu-id="41c43-373">**認可按鈕**</span><span class="sxs-lookup"><span data-stu-id="41c43-373">**Commit buttons**</span></span><br/>                                                                                   |
| <span data-ttu-id="41c43-374">感知</span><span class="sxs-lookup"><span data-stu-id="41c43-374">Awareness</span></span><br/>                 | <span data-ttu-id="41c43-375">很接近了。</span><span class="sxs-lookup"><span data-stu-id="41c43-375">Close.</span></span> <span data-ttu-id="41c43-376">請勿使用 [確定]，因為它會建議可能的問題是正常的。</span><span class="sxs-lookup"><span data-stu-id="41c43-376">Don't use OK because it suggests that potential problems are OK.</span></span><br/>                              |
| <span data-ttu-id="41c43-377">即將發生問題</span><span class="sxs-lookup"><span data-stu-id="41c43-377">Imminent problem</span></span><br/>          | <span data-ttu-id="41c43-378">每個選項的命令按鈕或命令連結，如果動作發生在對話方塊外，則為 [確定]。</span><span class="sxs-lookup"><span data-stu-id="41c43-378">A command button or command link for each option, or OK if the action occurs outside the dialog box.</span></span><br/> |
| <span data-ttu-id="41c43-379">有風險的動作確認</span><span class="sxs-lookup"><span data-stu-id="41c43-379">Risky action confirmation</span></span><br/> | <span data-ttu-id="41c43-380">是，否。</span><span class="sxs-lookup"><span data-stu-id="41c43-380">Yes, No.</span></span><br/>                                                                                             |



 

-   <span data-ttu-id="41c43-381">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="41c43-381">**Incorrect:**</span></span>
-   ![<span data-ttu-id="41c43-382">具有 [確定] 按鈕之警告對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="41c43-382">screen shot of warning dialog box with ok button</span></span> ](images/mess-warn-image26.png)
-   <span data-ttu-id="41c43-383">問題不正常，請改用 Close。</span><span class="sxs-lookup"><span data-stu-id="41c43-383">Problems aren't OK, so use Close instead.</span></span>

## <a name="documentation"></a><span data-ttu-id="41c43-384">文件</span><span class="sxs-lookup"><span data-stu-id="41c43-384">Documentation</span></span>

<span data-ttu-id="41c43-385">參考警告時：</span><span class="sxs-lookup"><span data-stu-id="41c43-385">When referring to warnings:</span></span>

-   <span data-ttu-id="41c43-386">如果警告提出問題，請以其問題參考警告;否則，請使用 main 指令。</span><span class="sxs-lookup"><span data-stu-id="41c43-386">If the warning asks a question, refer to a warning by its question; otherwise, use the main instruction.</span></span> <span data-ttu-id="41c43-387">如果問題或主要指示很長或更詳細，請總結。</span><span class="sxs-lookup"><span data-stu-id="41c43-387">If the question or main instruction is long or detailed, summarize it.</span></span>
-   <span data-ttu-id="41c43-388">如有必要，您可以將警告對話方塊參考為訊息。</span><span class="sxs-lookup"><span data-stu-id="41c43-388">If necessary, you may refer to a warning dialog box as a message.</span></span>
-   <span data-ttu-id="41c43-389">可能的話，請使用粗體格式化文字。</span><span class="sxs-lookup"><span data-stu-id="41c43-389">When possible, format the text using bold.</span></span> <span data-ttu-id="41c43-390">否則，請只在必要時才將文字放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="41c43-390">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="41c43-391">範例：在 [ **您要顯示不安全的專案嗎？** ] 訊息中，按一下 [是]。</span><span class="sxs-lookup"><span data-stu-id="41c43-391">Example: In the **Do you want to display the nonsecure items?** message, click Yes.</span></span>

 

