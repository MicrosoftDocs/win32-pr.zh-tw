---
title: " (設計基礎) 的錯誤訊息"
description: 錯誤訊息會警示使用者已發生的問題。
ms.assetid: b02110e9-985d-4448-9c95-eb958b0059b1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0a8ee17093618dc8a192cfad8ce962f7ed04fc76
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104562913"
---
# <a name="error-messages-design-basics"></a><span data-ttu-id="2e6c8-103"> (設計基礎) 的錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="2e6c8-103">Error Messages (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="2e6c8-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="2e6c8-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="2e6c8-106">錯誤訊息會警示使用者已發生的問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-106">An error message alerts users of a problem that has already occurred.</span></span> <span data-ttu-id="2e6c8-107">相反地，警告訊息會警示使用者可能會在未來發生問題的狀況。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-107">By contrast, a warning message alerts users of a condition that might cause a problem in the future.</span></span> <span data-ttu-id="2e6c8-108">您可以使用強制回應對話方塊、就地訊息、通知或氣球來顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-108">Error messages can be presented using modal dialog boxes, in-place messages, notifications, or balloons.</span></span>

![錯誤訊息的螢幕擷取畫面：無法重新命名](images/mess-error-image1.png)

<span data-ttu-id="2e6c8-110">一般的強制回應錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-110">A typical modal error message.</span></span>

<span data-ttu-id="2e6c8-111">有效的錯誤訊息會通知使用者發生問題、解釋發生問題的原因，並提供解決方案，讓使用者可以修正問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-111">Effective error messages inform users that a problem occurred, explain why it happened, and provide a solution so users can fix the problem.</span></span> <span data-ttu-id="2e6c8-112">使用者應執行動作，或將其行為變更為錯誤訊息的結果。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-112">Users should either perform an action or change their behavior as the result of an error message.</span></span>

<span data-ttu-id="2e6c8-113">妥善撰寫、實用的錯誤訊息對品質的使用者體驗很重要。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-113">Well-written, helpful error messages are crucial to a quality user experience.</span></span> <span data-ttu-id="2e6c8-114">撰寫不當的錯誤訊息會導致產品滿意度偏低，而且是肇因技術支援成本的首要原因。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-114">Poorly written error messages result in low product satisfaction, and are a leading cause of avoidable technical support costs.</span></span> <span data-ttu-id="2e6c8-115">不必要的錯誤訊息會中斷使用者的流程。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-115">Unnecessary error messages break users' flow.</span></span>

<span data-ttu-id="2e6c8-116">**注意：** 與 [對話方塊](win-dialog-box.md)、 [警告訊息](mess-warn.md)、 [確認](mess-confirm.md)、 [標準圖示](vis-std-icons.md)、 [通知](mess-notif.md)和 [版面](vis-layout.md) 配置相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-116">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [warning messages](mess-warn.md), [confirmations](mess-confirm.md), [standard icons](vis-std-icons.md), [notifications](mess-notif.md), and [layout](vis-layout.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="2e6c8-117">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-117">Is this the right user interface?</span></span>

<span data-ttu-id="2e6c8-118">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-118">To decide, consider these questions:</span></span>

- <span data-ttu-id="2e6c8-119">**使用者介面 (UI) 呈現已發生的問題嗎？**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-119">**Is the user interface (UI) presenting a problem that has already occurred?**</span></span> <span data-ttu-id="2e6c8-120">如果沒有，則訊息不會是錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-120">If not, the message isn't an error.</span></span> <span data-ttu-id="2e6c8-121">如果使用者警示的情況可能會在未來發生問題，請使用警告訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-121">If the user being alerted of a condition that might cause a problem in the future, use a warning message.</span></span>
- <span data-ttu-id="2e6c8-122">**可以防止問題而不會造成混淆嗎？**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-122">**Can the problem be prevented without causing confusion?**</span></span> <span data-ttu-id="2e6c8-123">若是如此，請改為避免問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-123">If so, prevent the problem instead.</span></span> <span data-ttu-id="2e6c8-124">例如，使用受限制為有效值的控制項，而不是使用可能需要錯誤訊息的不受限制控制項。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-124">For example, use controls that are constrained to valid values instead of using unconstrained controls that may require error messages.</span></span> <span data-ttu-id="2e6c8-125">此外，當您按一下時，停用控制項會導致錯誤，只要它很明顯地停用控制項的原因。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-125">Also, disable controls when clicking would result in error, as long as it's obvious why the control is disabled.</span></span>
- <span data-ttu-id="2e6c8-126">**問題可以自動校正嗎？**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-126">**Can the problem be corrected automatically?**</span></span> <span data-ttu-id="2e6c8-127">如果是的話，請處理問題並隱藏錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-127">If so, handle the problem and suppress the error message.</span></span>
- <span data-ttu-id="2e6c8-128">**使用者是否有可能執行動作，或將其行為變更為訊息的結果？**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-128">**Are users likely to perform an action or change their behavior as the result of the message?**</span></span> <span data-ttu-id="2e6c8-129">如果沒有，則條件不會讓使用者中斷，因此最好是抑制錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-129">If not, the condition doesn't justify interrupting the user so it's better to suppress the error.</span></span>
- <span data-ttu-id="2e6c8-130">**當使用者主動使用其他程式時，是否有相關問題？**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-130">**Is the problem relevant when users are actively using other programs?**</span></span> <span data-ttu-id="2e6c8-131">如果是的話，請考慮使用 [通知區域圖標](winenv-notification.md)來顯示問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-131">If so, consider showing the problem using a [notification area icon](winenv-notification.md).</span></span>
- <span data-ttu-id="2e6c8-132">**問題與目前的使用者活動不相關，不需要立即的使用者動作，而且使用者可以自由地忽略它嗎？**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-132">**Is the problem not related to the current user activity, does it not require immediate user action, and can users freely ignore it?**</span></span> <span data-ttu-id="2e6c8-133">若是如此，請改用 [動作失敗通知](mess-notif.md) 。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-133">If so, use an [action failure notification](mess-notif.md) instead.</span></span>
- <span data-ttu-id="2e6c8-134">**問題是否與主視窗內的背景工作狀態有關？**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-134">**Does the problem relate to the status of a background task within a primary window?**</span></span> <span data-ttu-id="2e6c8-135">如果是的話，請考慮使用 [狀態列](ctrl-status-bars.md)來顯示問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-135">If so, consider showing the problem using a [status bars](ctrl-status-bars.md).</span></span>
- <span data-ttu-id="2e6c8-136">**主要目標使用者是 IT 專業人員嗎？**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-136">**Are the primary target users IT professionals?**</span></span> <span data-ttu-id="2e6c8-137">若是如此，請考慮使用替代的意見反應機制，例如 [記錄](glossary.md) 檔專案或電子郵件警示。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-137">If so, consider using an alternative feedback mechanism, such as [log file](glossary.md) entries or e-mail alerts.</span></span> <span data-ttu-id="2e6c8-138">IT 專業人員強烈偏好記錄檔，以取得非重要的資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-138">IT professionals strongly prefer log files for non-critical information.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="2e6c8-139">設計概念</span><span class="sxs-lookup"><span data-stu-id="2e6c8-139">Design concepts</span></span>

<span data-ttu-id="2e6c8-140">**不良錯誤訊息的特性**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-140">**The characteristics of poor error messages**</span></span>

<span data-ttu-id="2e6c8-141">如果有許多討厭、無用和寫入錯誤的錯誤訊息，就不會驚訝。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-141">It should be no surprise that there are many annoying, unhelpful, and poorly written error messages.</span></span> <span data-ttu-id="2e6c8-142">而且，由於錯誤訊息通常會使用強制回應對話方塊來呈現，因此它們會中斷使用者目前的活動，並在允許使用者繼續之前先確認要求。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-142">And because error messages are often presented using modal dialogs, they interrupt the user's current activity and demand to be acknowledged before allowing the user to continue.</span></span>

<span data-ttu-id="2e6c8-143">問題的部分在於有很多方法可以進行錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-143">Part of the problem is that there are so many ways to do it wrong.</span></span> <span data-ttu-id="2e6c8-144">請考慮下列太可惜的錯誤訊息廳範例：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-144">Consider these examples from the Error Message Hall of Shame:</span></span>

<span data-ttu-id="2e6c8-145">**不必要的錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-145">**Unnecessary error messages**</span></span>

<span data-ttu-id="2e6c8-146">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-146">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-147">錯誤訊息的螢幕擷取畫面：應用程式失敗</span><span class="sxs-lookup"><span data-stu-id="2e6c8-147">screen shot of error message: application failed</span></span> ](images/mess-error-image2.png)

<span data-ttu-id="2e6c8-148">從 Windows XP 的這個範例可能是最糟的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-148">This example from Windows XP might be the worst error message ever.</span></span> <span data-ttu-id="2e6c8-149">這表示程式無法啟動，因為 Windows 本身正在關機。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-149">It indicates that a program couldn't launch because Windows itself is in the process of shutting down.</span></span> <span data-ttu-id="2e6c8-150">使用者無法執行這項操作，甚至想要 (使用者選擇在所有) 之後關閉 Windows。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-150">There is nothing the user can do about this or even wants to do about this (the user chose to shut Windows down, after all).</span></span> <span data-ttu-id="2e6c8-151">而藉由顯示此錯誤訊息，Windows 會防止自己關機！</span><span class="sxs-lookup"><span data-stu-id="2e6c8-151">And by displaying this error message, Windows prevents itself from shutting down!</span></span>

<span data-ttu-id="2e6c8-152">**問題：** 錯誤訊息本身就是問題所在。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-152">**The problem:** The error message itself is the problem.</span></span> <span data-ttu-id="2e6c8-153">除了關閉錯誤訊息之外，使用者也不需要執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-153">Aside from dismissing the error message, there is nothing for users to do.</span></span>

<span data-ttu-id="2e6c8-154">**領先的原因：** 報告所有的錯誤案例，不論使用者的目標或觀點。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-154">**Leading cause:** Reporting all error cases, regardless of users' goals or point of view.</span></span>

<span data-ttu-id="2e6c8-155">**建議的替代方案：** 請勿報告使用者不在意的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-155">**Recommended alternative:** Don't report errors that users don't care about.</span></span>

<span data-ttu-id="2e6c8-156">**「成功」錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-156">**"Success" error messages**</span></span>

<span data-ttu-id="2e6c8-157">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-157">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-158">錯誤訊息的螢幕擷取畫面：移除失敗</span><span class="sxs-lookup"><span data-stu-id="2e6c8-158">screen shot of error message: removal failure</span></span> ](images/mess-error-image3.png)

<span data-ttu-id="2e6c8-159">此錯誤訊息是由使用者選擇不在程式移除之後立即重新開機 Windows 所造成。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-159">This error message resulted from the user choosing not to restart Windows immediately after program removal.</span></span> <span data-ttu-id="2e6c8-160">從使用者的觀點來看，移除程式成功。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-160">The program removal was successful from the user's point of view.</span></span>

<span data-ttu-id="2e6c8-161">**問題：** 從使用者的觀點來看，並不會發生任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-161">**The problem:** There's no error from the user's point of view.</span></span> <span data-ttu-id="2e6c8-162">除了關閉錯誤訊息之外，使用者也不需要執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-162">Aside from dismissing the error message, there is nothing for users to do.</span></span>

<span data-ttu-id="2e6c8-163">**領先的原因：** 從使用者的觀點來看，工作已順利完成，但無法從卸載程式的觀點來看。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-163">**Leading cause:** The task completed successfully from the user's point of view, but failed from the uninstall program's point of view.</span></span>

<span data-ttu-id="2e6c8-164">**建議的替代方案：** 請勿報告使用者認為可接受的條件錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-164">**Recommended alternative:** Don't report errors for conditions that users consider acceptable.</span></span>

<span data-ttu-id="2e6c8-165">**完全無用的錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-165">**Completely useless error messages**</span></span>

<span data-ttu-id="2e6c8-166">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-166">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-167">錯誤訊息的螢幕擷取畫面：未知的錯誤</span><span class="sxs-lookup"><span data-stu-id="2e6c8-167">screen shot of error message: unknown error</span></span> ](images/mess-error-image4.png)

<span data-ttu-id="2e6c8-168">使用者瞭解有錯誤，但不知道錯誤是什麼，或是該怎麼做。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-168">Users learn that there was an error, but have no idea what the error was or what to do about it.</span></span> <span data-ttu-id="2e6c8-169">沒關係，沒問題！</span><span class="sxs-lookup"><span data-stu-id="2e6c8-169">And no, it's not OK!</span></span>

<span data-ttu-id="2e6c8-170">**問題：** 錯誤訊息不會提供特定的問題，使用者也不能執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-170">**The problem:** The error message doesn't give a specific problem and there is nothing users can do about it.</span></span>

<span data-ttu-id="2e6c8-171">**領先的原因：** 最可能的情況是，程式的錯誤處理不佳。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-171">**Leading cause:** Most likely, the program has poor error handling.</span></span>

<span data-ttu-id="2e6c8-172">**建議的替代方案：** 設計正確的錯誤處理常式。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-172">**Recommended alternative:** Design good error handling into the program.</span></span>

<span data-ttu-id="2e6c8-173">**費解錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-173">**Incomprehensible error messages**</span></span>

<span data-ttu-id="2e6c8-174">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-174">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-175">錯誤訊息的螢幕擷取畫面：備份未完成</span><span class="sxs-lookup"><span data-stu-id="2e6c8-175">screen shot of error message: backup not complete</span></span> ](images/mess-error-image5.png)

<span data-ttu-id="2e6c8-176">在此範例中，問題陳述很清楚，但補充說明全然 baffling。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-176">In this example, the problem statement is clear, but the supplemental explanation is utterly baffling.</span></span>

<span data-ttu-id="2e6c8-177">**問題：** 問題陳述或解決方案費解。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-177">**The problem:** The problem statement or solution is incomprehensible.</span></span>

<span data-ttu-id="2e6c8-178">**領先的原因：** 從程式碼的觀點來解釋問題，而不是從使用者的觀點來說明。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-178">**Leading cause:** Explaining the problem from the code's point of view instead of the user's.</span></span>

<span data-ttu-id="2e6c8-179">**建議的替代方案：** 撰寫您的目標使用者可以輕鬆瞭解的錯誤訊息正文。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-179">**Recommended alternative:** Write error message text that your target users can easily understand.</span></span> <span data-ttu-id="2e6c8-180">提供使用者可實際執行的解決方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-180">Provide solutions that users can actually perform.</span></span> <span data-ttu-id="2e6c8-181">設計程式的錯誤訊息體驗沒有程式設計人員在該位置撰寫錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-181">Design your program's error message experience don't have programmers compose error messages on the spot.</span></span>

<span data-ttu-id="2e6c8-182">**Overcommunicate 的錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-182">**Error messages that overcommunicate**</span></span>

<span data-ttu-id="2e6c8-183">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-183">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-184">極詳細訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2e6c8-184">screen shot of extremely verbose message</span></span> ](images/mess-error-image6.png)

<span data-ttu-id="2e6c8-185">在此範例中，錯誤訊息顯然會嘗試說明每個疑難排解步驟。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-185">In this example, the error message apparently attempts to explain every troubleshooting step.</span></span>

<span data-ttu-id="2e6c8-186">**問題：** 太多資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-186">**The problem:** Too much information.</span></span>

<span data-ttu-id="2e6c8-187">**領先的原因：** 提供太多詳細資料，或嘗試在錯誤訊息中說明複雜的疑難排解程式。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-187">**Leading cause:** Giving too many details or trying to explain a complicated troubleshooting process within an error message.</span></span>

<span data-ttu-id="2e6c8-188">**建議的替代方案：** 避免不必要的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-188">**Recommended alternative:** Avoid unnecessary details.</span></span> <span data-ttu-id="2e6c8-189">此外，請避免疑難排解員。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-189">Also, avoid troubleshooters.</span></span> <span data-ttu-id="2e6c8-190">如果您需要疑難排解員，請將焦點放在最有可能的解決方案，並藉由連結至 [說明] 中的適當主題來說明其餘部分。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-190">If a troubleshooter is necessary, focus on the most likely solutions and explain the remainder by linking to the appropriate topic in Help.</span></span>

<span data-ttu-id="2e6c8-191">**不必要的錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-191">**Unnecessarily harsh error messages**</span></span>

<span data-ttu-id="2e6c8-192">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-192">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-193">訊息的螢幕擷取畫面：找不到物件</span><span class="sxs-lookup"><span data-stu-id="2e6c8-193">screen shot of message: can't find object</span></span> ](images/mess-error-image7.png)

<span data-ttu-id="2e6c8-194">程式找不到物件幾乎聽起來很嚴重。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-194">The program's inability to find an object hardly sounds catastrophic.</span></span> <span data-ttu-id="2e6c8-195">並假設它是災難性的，為什麼會有回應？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-195">And assuming it is catastrophic, why is OK the response?</span></span>

<span data-ttu-id="2e6c8-196">**問題：** 程式的語氣不必要，也不太明顯。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-196">**The problem:** The program's tone is unnecessarily harsh or dramatic.</span></span>

<span data-ttu-id="2e6c8-197">**領先的原因：** 問題的原因是從程式的觀點來看，出現了嚴重的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-197">**Leading cause:** The problem is due to a bug that appears catastrophic from the program's point of view.</span></span>

<span data-ttu-id="2e6c8-198">**建議的替代方案：** 根據使用者的觀點，仔細選擇語言。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-198">**Recommended alternative:** Choose language carefully based on the user's point of view.</span></span>

<span data-ttu-id="2e6c8-199">**使用者的錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-199">**Error messages that blame users**</span></span>

<span data-ttu-id="2e6c8-200">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-200">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-201">訊息的螢幕擷取畫面：不合法的字元</span><span class="sxs-lookup"><span data-stu-id="2e6c8-201">screen shot of message: illegal character</span></span> ](images/mess-error-image8.png)

<span data-ttu-id="2e6c8-202">為何讓使用者感覺像是犯罪？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-202">Why make users feel like a criminal?</span></span>

<span data-ttu-id="2e6c8-203">**問題：** 錯誤訊息會以 accuses 使用者提出錯誤的方式片語。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-203">**The problem:** The error message is phrased in a way that accuses the user of making an error.</span></span>

<span data-ttu-id="2e6c8-204">**領先的原因：** 著重于使用者行為而非問題的不區分片語。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-204">**Leading cause:** Insensitive phrasing that focuses on the user's behavior instead of the problem.</span></span>

<span data-ttu-id="2e6c8-205">**建議的替代方案：** 將焦點放在問題上，而不是因需要而導致問題的使用者動作。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-205">**Recommended alternative:** Focus on the problem, not the user action that led to the problem, using the passive voice as necessary.</span></span>

<span data-ttu-id="2e6c8-206">**更愚蠢的錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-206">**Silly error messages**</span></span>

<span data-ttu-id="2e6c8-207">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-207">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-208">訊息的螢幕擷取畫面：錯誤報表中的錯誤</span><span class="sxs-lookup"><span data-stu-id="2e6c8-208">screen shot of message: error in error report</span></span> ](images/mess-error-image9.png)

<span data-ttu-id="2e6c8-209">在此範例中，問題陳述很諷刺，而且不提供任何解決方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-209">In this example, the problem statement is quite ironic and no solutions are provided.</span></span>

<span data-ttu-id="2e6c8-210">**問題：** 更愚蠢或非 sequitors 的錯誤訊息語句。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-210">**The problem:** Error message statements that are silly or non-sequitors.</span></span>

<span data-ttu-id="2e6c8-211">**領先的原因：** 建立錯誤訊息，而不需要注意其內容。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-211">**Leading cause:** Creating error messages without paying attention to their context.</span></span>

<span data-ttu-id="2e6c8-212">**建議的替代方案：** 由寫入器製作和審核您的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-212">**Recommended alternative:** Have your error messages crafted and reviewed by a writer.</span></span> <span data-ttu-id="2e6c8-213">查看錯誤時，請考慮內容和使用者的想法狀態。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-213">Consider the context and the user's state of mind when reviewing the errors.</span></span>

<span data-ttu-id="2e6c8-214">**程式設計人員錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-214">**Programmer error messages**</span></span>

<span data-ttu-id="2e6c8-215">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-215">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-216">訊息的螢幕擷取畫面：存取違規位址</span><span class="sxs-lookup"><span data-stu-id="2e6c8-216">screen shot of message: access violation address</span></span> ](images/mess-error-image10.png)

<span data-ttu-id="2e6c8-217">在此範例中，錯誤訊息指出程式中有錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-217">In this example, the error message indicates that there is a bug in the program.</span></span> <span data-ttu-id="2e6c8-218">此錯誤訊息只有程式設計師才有意義。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-218">This error message has meaning only to the programmer.</span></span>

<span data-ttu-id="2e6c8-219">**問題：** 旨在協助程式開發人員尋找 bug 的訊息會保留在程式的發行版本中。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-219">**The problem:** Messages intended to help the program's developers find bugs are left in the release version of the program.</span></span> <span data-ttu-id="2e6c8-220">這些錯誤訊息沒有使用者的意義或值。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-220">These error messages have no meaning or value to users.</span></span>

<span data-ttu-id="2e6c8-221">**領先的原因：** 使用一般 UI 的程式設計人員將訊息傳送給自己。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-221">**Leading cause:** Programmers using normal UI to make messages to themselves.</span></span>

<span data-ttu-id="2e6c8-222">**建議的替代方案：** 開發人員必須有條件地編譯所有這類訊息，使其自動從產品的發行版本中移除。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-222">**Recommended alternative:** Developers must conditionally compile all such messages so that they are automatically removed from the release version of a product.</span></span> <span data-ttu-id="2e6c8-223">請勿浪費時間來嘗試對使用者發出像是這理解的錯誤，因為他們唯一的物件是程式設計人員。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-223">Don't waste time trying to make errors like this comprehensible to users because their only audience is the programmers.</span></span>

<span data-ttu-id="2e6c8-224">**呈現不良的錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-224">**Poorly presented error messages**</span></span>

<span data-ttu-id="2e6c8-225">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-225">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-226">訊息的螢幕擷取畫面：非預期的失敗</span><span class="sxs-lookup"><span data-stu-id="2e6c8-226">screen shot of message: unexpected failure</span></span> ](images/mess-error-image11.png)

<span data-ttu-id="2e6c8-227">這個範例有許多常見的呈現錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-227">This example has many common presentation mistakes.</span></span>

<span data-ttu-id="2e6c8-228">**問題：** 取得錯誤訊息簡報中錯誤的所有詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-228">**The problem:** Getting all the details wrong in the error message presentation.</span></span>

<span data-ttu-id="2e6c8-229">**領先的原因：** 不知道並套用錯誤訊息指導方針。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-229">**Leading cause:** Not knowing and applying the error message guidelines.</span></span> <span data-ttu-id="2e6c8-230">請勿使用寫入器和編輯器來建立和檢查錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-230">Not using writers and editors to create and review the error messages.</span></span>

<span data-ttu-id="2e6c8-231">錯誤處理的本質是很容易就能進行這些錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-231">The nature of error handling is such that many of these mistakes are very easy to make.</span></span> <span data-ttu-id="2e6c8-232">要注意的是，大部分的錯誤訊息都可以針對太可惜的廳被提名人。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-232">It's disturbing to realize that most error messages could be nominees for the Hall of Shame.</span></span>

<span data-ttu-id="2e6c8-233">**良好錯誤訊息的特性**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-233">**The characteristics of good error messages**</span></span>

<span data-ttu-id="2e6c8-234">相對於先前的錯誤範例，良好的錯誤訊息有：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-234">In contrast to the previous bad examples, good error messages have:</span></span>

- <span data-ttu-id="2e6c8-235">**問題。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-235">**A problem.**</span></span> <span data-ttu-id="2e6c8-236">指出發生問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-236">States that a problem occurred.</span></span>
- <span data-ttu-id="2e6c8-237">**原因。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-237">**A cause.**</span></span> <span data-ttu-id="2e6c8-238">說明發生問題的原因。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-238">Explains why the problem occurred.</span></span>
- <span data-ttu-id="2e6c8-239">**方案。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-239">**A solution.**</span></span> <span data-ttu-id="2e6c8-240">提供解決方案，讓使用者可以修正問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-240">Provides a solution so that users can fix the problem.</span></span>

<span data-ttu-id="2e6c8-241">此外，良好的錯誤訊息會以下列方式呈現：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-241">Additionally, good error messages are presented in a way that is:</span></span>

- <span data-ttu-id="2e6c8-242">**相關。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-242">**Relevant.**</span></span> <span data-ttu-id="2e6c8-243">這則訊息會顯示使用者在意的問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-243">The message presents a problem that users care about.</span></span>
- <span data-ttu-id="2e6c8-244">**可行。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-244">**Actionable.**</span></span> <span data-ttu-id="2e6c8-245">使用者應執行動作，或將其行為變更為訊息的結果。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-245">Users should either perform an action or change their behavior as the result of the message.</span></span>
- <span data-ttu-id="2e6c8-246">**以使用者為中心。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-246">**User-centered.**</span></span> <span data-ttu-id="2e6c8-247">此訊息會根據目標使用者動作或目標來描述問題，而不是程式碼不滿意的情況。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-247">The message describes the problem in terms of target user actions or goals, not in terms of what the code is unhappy with.</span></span>
- <span data-ttu-id="2e6c8-248">**簡短。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-248">**Brief.**</span></span> <span data-ttu-id="2e6c8-249">訊息越短越好，但也不會縮短。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-249">The message is as short as possible, but no shorter.</span></span>
- <span data-ttu-id="2e6c8-250">**清楚。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-250">**Clear.**</span></span> <span data-ttu-id="2e6c8-251">此訊息使用一般語言，讓目標使用者可以輕鬆地瞭解問題和解決方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-251">The message uses plain language so that the target users can easily understand problem and solution.</span></span>
- <span data-ttu-id="2e6c8-252">**特定。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-252">**Specific.**</span></span> <span data-ttu-id="2e6c8-253">此訊息會使用特定語言來描述問題，並提供相關物件的特定名稱、位置和值。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-253">The message describes the problem using specific language, giving specific names, locations, and values of the objects involved.</span></span>
- <span data-ttu-id="2e6c8-254">**禮貌。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-254">**Courteous.**</span></span> <span data-ttu-id="2e6c8-255">使用者不應該應該過度或感到愚蠢。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-255">Users shouldn't be blamed or made to feel stupid.</span></span>
- <span data-ttu-id="2e6c8-256">**罕見。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-256">**Rare.**</span></span> <span data-ttu-id="2e6c8-257">不常顯示。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-257">Displayed infrequently.</span></span> <span data-ttu-id="2e6c8-258">經常顯示的錯誤訊息是不良設計的徵兆。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-258">Frequently displayed error messages are a sign of bad design.</span></span>

<span data-ttu-id="2e6c8-259">藉由設計您的錯誤處理經驗來取得這些特性，您就可以將程式的錯誤訊息從太可惜的錯誤訊息大廳中排除。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-259">By designing your error handling experience to have these characteristics, you can keep your program's error messages out of the Error Message Hall of Shame.</span></span>

<span data-ttu-id="2e6c8-260">**避免不必要的錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-260">**Avoiding unnecessary error messages**</span></span>

<span data-ttu-id="2e6c8-261">通常，最佳的錯誤訊息不會有錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-261">Often the best error message is no error message.</span></span> <span data-ttu-id="2e6c8-262">您可以透過更好的設計來避免許多錯誤，而且通常會有更好的錯誤訊息替代方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-262">Many errors can be avoided through better design, and there are often better alternatives to error messages.</span></span> <span data-ttu-id="2e6c8-263">通常最好避免發生錯誤，而不是報告一個錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-263">It's usually better to prevent an error than to report one.</span></span>

<span data-ttu-id="2e6c8-264">要避免的最明顯錯誤訊息是無法操作的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-264">The most obvious error messages to avoid are those that aren't actionable.</span></span> <span data-ttu-id="2e6c8-265">如果使用者可能會在未進行任何變更的情況下關閉訊息，請省略錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-265">If users are likely to dismiss the message without doing or changing anything, omit the error message.</span></span>

<span data-ttu-id="2e6c8-266">某些錯誤訊息可能會被排除，因為它們不會造成使用者的觀點。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-266">Some error messages can be eliminated because they aren't problems from the user's point of view.</span></span> <span data-ttu-id="2e6c8-267">例如，假設使用者嘗試刪除已經在刪除中的檔案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-267">For example, suppose the user tried to delete a file that is already in the process of being deleted.</span></span> <span data-ttu-id="2e6c8-268">從程式碼的觀點來看，這可能是未預期的情況，因此使用者不會將其視為錯誤，因為他們想要的結果。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-268">While this might be an unexpected case from the code's point of view, users don't consider this an error because their desired outcome is achieved.</span></span>

<span data-ttu-id="2e6c8-269">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-269">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-270">message：無法刪除檔案的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2e6c8-270">screen shot of message: can't delete file</span></span> ](images/mess-error-image12.png)

<span data-ttu-id="2e6c8-271">此錯誤訊息應該會被排除，因為動作是從使用者的觀點來看成功。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-271">This error message should be eliminated because the action was successful from the user's point of view.</span></span>

<span data-ttu-id="2e6c8-272">另一個範例是，假設使用者明確地取消工作。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-272">For another example, suppose the user explicitly cancels a task.</span></span> <span data-ttu-id="2e6c8-273">針對使用者的觀點，下列條件不是錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-273">For the user's point of view, the following condition isn't an error.</span></span>

<span data-ttu-id="2e6c8-274">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-274">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-275">訊息的螢幕擷取畫面：無法完成備份</span><span class="sxs-lookup"><span data-stu-id="2e6c8-275">screen shot of message: can't complete backup</span></span> ](images/mess-error-image13.png)

<span data-ttu-id="2e6c8-276">此錯誤訊息也應消除，因為動作是從使用者的觀點來看成功。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-276">This error message should also be eliminated because the action was successful from the user's point of view.</span></span>

<span data-ttu-id="2e6c8-277">有時您可以藉由專注于使用者的目標而非技術來消除錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-277">Sometimes error messages can be eliminated by focusing on users' goals instead of the technology.</span></span> <span data-ttu-id="2e6c8-278">在這麼做時，請重新考慮什麼是錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-278">In doing so, reconsider what an error really is.</span></span> <span data-ttu-id="2e6c8-279">使用者的目標是否有問題，或您的程式滿足這些問題的能力？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-279">Is the problem with the user's goals, or with your program's ability to satisfy them?</span></span> <span data-ttu-id="2e6c8-280">如果使用者的動作在真實世界中有意義，也應該對軟體有意義。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-280">If the user's action makes sense in the real world, it should make sense in software too.</span></span>

<span data-ttu-id="2e6c8-281">例如，假設在電子商務程式中，使用者嘗試使用搜尋來尋找產品，但常值搜尋查詢沒有相符專案，而且所需的產品不存在。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-281">For example, suppose within an e-commerce program a user tries to find a product using search, but the literal search query has no matches and the desired product is out of stock.</span></span> <span data-ttu-id="2e6c8-282">技術上來說，這是一項錯誤，但是不會提供錯誤訊息，程式可以：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-282">Technically, this is an error, but instead of giving an error message, the program could:</span></span>

- <span data-ttu-id="2e6c8-283">繼續搜尋最符合查詢的產品。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-283">Continue to search for products that most closely match the query.</span></span>
- <span data-ttu-id="2e6c8-284">如果搜尋有明顯的錯誤，則會自動建議已更正的查詢。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-284">If the search has obvious mistakes, automatically recommend a corrected query.</span></span>
- <span data-ttu-id="2e6c8-285">自動處理常見的問題，例如拼錯、替代拼寫，以及不相符的複數表示和動詞案例。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-285">Automatically handle common problems such as misspellings, alternative spellings, and mismatching pluralization and verb cases.</span></span>
- <span data-ttu-id="2e6c8-286">指出產品的存貨。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-286">Indicate when the product will be in stock.</span></span>

<span data-ttu-id="2e6c8-287">只要使用者的要求合理，設計完善的電子商務程式應該會傳回合理的結果，而不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-287">As long as the user's request is reasonable, a well designed e-commerce program should return reasonable results not errors.</span></span>

<span data-ttu-id="2e6c8-288">避免錯誤訊息的另一種好方法是先防止發生問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-288">Another great way to avoid error messages is by preventing problems in the first place.</span></span> <span data-ttu-id="2e6c8-289">您可以透過下列方式防止錯誤：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-289">You can prevent errors by:</span></span>

- <span data-ttu-id="2e6c8-290">**使用受限制的控制項。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-290">**Using constrained controls.**</span></span> <span data-ttu-id="2e6c8-291">使用受限制為有效值的控制項。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-291">Use controls that are constrained to valid values.</span></span> <span data-ttu-id="2e6c8-292">清單、滑杆、核取方塊、選項按鈕和日期和時間選擇器等控制項都限制為有效值，而文字方塊通常不是，而且可能需要錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-292">Controls like lists, sliders, check boxes, radio buttons, and date and time pickers are constrained to valid values, whereas text boxes are often not and may require error messages.</span></span> <span data-ttu-id="2e6c8-293">不過，您可以限制文字方塊僅接受特定字元，並接受最大字元數。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-293">However, you can constrain text boxes to accept only certain characters and accept a maximum number of characters.</span></span>
- <span data-ttu-id="2e6c8-294">**使用受限制的互動。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-294">**Using constrained interactions.**</span></span> <span data-ttu-id="2e6c8-295">若為拖曳作業，則只允許使用者在有效的目標上放置。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-295">For drag operations, allow users to drop only on valid targets.</span></span>
- <span data-ttu-id="2e6c8-296">**使用停用的控制項和功能表項目。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-296">**Using disabled controls and menu items.**</span></span> <span data-ttu-id="2e6c8-297">當使用者可以輕鬆推算控制項或功能表項目停用的原因時，請停用控制項和功能表項目。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-297">Disable controls and menu items when users can easily deduce why the control or menu item is disabled.</span></span>
- <span data-ttu-id="2e6c8-298">**提供良好的預設值。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-298">**Providing good default values.**</span></span> <span data-ttu-id="2e6c8-299">如果使用者可以接受預設值，就不太可能產生輸入錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-299">Users are less likely to make input errors if they can accept the default values.</span></span> <span data-ttu-id="2e6c8-300">即使使用者決定變更值，預設值仍能讓使用者知道預期的輸入格式。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-300">Even if users decide to change the value, the default value lets users know the expected input format.</span></span>
- <span data-ttu-id="2e6c8-301">**讓事情正常運作。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-301">**Making things just work.**</span></span> <span data-ttu-id="2e6c8-302">如果不必要或自動執行工作，使用者就比較不可能發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-302">Users are less likely to make mistakes if the tasks are unnecessary or performed automatically for them.</span></span> <span data-ttu-id="2e6c8-303">或者，如果使用者犯了很小的錯誤，但其意圖很清楚，則會自動修正此問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-303">Or if users make small mistakes but their intention is clear, the problem is fixed automatically.</span></span> <span data-ttu-id="2e6c8-304">例如，您可以自動校正次要格式問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-304">For example, you can automatically correct minor formatting problems.</span></span>

<span data-ttu-id="2e6c8-305">**提供必要的錯誤訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-305">**Providing necessary error messages**</span></span>

<span data-ttu-id="2e6c8-306">有時候您真的需要提供錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-306">Sometimes you really do need to provide an error message.</span></span> <span data-ttu-id="2e6c8-307">使用者犯了錯誤、網路和裝置停止運作、找不到物件或修改物件、無法完成工作，以及程式有錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-307">Users make mistakes, networks and devices stop working, objects can't be found or modified, tasks can't be completed, and programs have bugs.</span></span> <span data-ttu-id="2e6c8-308">在理想情況下，這些問題會較不常發生，例如，我們可以設計我們的軟體來防止許多類型的使用者錯誤，但這並不是實際的問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-308">Ideally, these problems would happen less often for example, we can design our software to prevent many types of user mistakes but it isn't realistic to prevent all of these problems.</span></span> <span data-ttu-id="2e6c8-309">當這些問題發生時，有一個實用的錯誤訊息就能快速回到他們的腳。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-309">And when one of these problems does happen, a helpful error message gets users back on their feet quickly.</span></span>

<span data-ttu-id="2e6c8-310">常見的想法是，錯誤訊息是最糟的使用者體驗，而且應該盡可能避免，但是更精確的說，就是使用者混淆是最糟的體驗，因此應該盡可能避免所有成本。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-310">A common belief is that error messages are the worst user experience and should be avoided at all costs, but it is more accurate to say that user confusion is the worst experience and should be avoided at all costs.</span></span> <span data-ttu-id="2e6c8-311">有時候成本會是很有用的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-311">Sometimes that cost is a helpful error message.</span></span>

<span data-ttu-id="2e6c8-312">請考慮停用的控制項。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-312">Consider disabled controls.</span></span> <span data-ttu-id="2e6c8-313">大部分的情況下，控制項停用的原因很明顯，因此停用控制項是避免錯誤訊息的絕佳方法。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-313">Most of the time, it is obvious why a control is disabled, so disabling the control is a great way to avoid an error message.</span></span> <span data-ttu-id="2e6c8-314">但是，如果停用控制項的原因不明顯，該怎麼辦？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-314">However, what if the reason a control is disabled isn't obvious?</span></span> <span data-ttu-id="2e6c8-315">使用者無法繼續，而且沒有任何意見反應可判斷問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-315">The user can't proceed and there is no feedback to determine the problem.</span></span> <span data-ttu-id="2e6c8-316">現在使用者停滯，必須推算問題或獲得技術支援。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-316">Now the user is stuck and either has to deduce the problem or get technical support.</span></span> <span data-ttu-id="2e6c8-317">在這種情況下，最好是讓控制項保持啟用狀態，並改為提供實用的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-317">In such cases, it's much better to leave the control enabled and give a helpful error message instead.</span></span>

<span data-ttu-id="2e6c8-318">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-318">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-319">訊息的螢幕擷取畫面：儲存備份的位置？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-319">screen shot of message: where save backup?</span></span> ](images/mess-error-image14.png)

<span data-ttu-id="2e6c8-320">為什麼在這裡停用 [下一步] 按鈕？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-320">Why is the Next button disabled here?</span></span> <span data-ttu-id="2e6c8-321">最好讓它保持啟用狀態，並提供實用的錯誤訊息，以避免使用者混淆。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-321">Better to leave it enabled and avoid user confusion by giving a helpful error message.</span></span>

<span data-ttu-id="2e6c8-322">如果您不確定是否應該提供錯誤訊息，請從撰寫您可能提供的錯誤訊息開始。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-322">If you aren't sure whether you should give an error message, start by composing the error message that you might give.</span></span> <span data-ttu-id="2e6c8-323">如果使用者可能會執行動作或變更其行為，請提供錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-323">If users are likely either to perform an action or to change their behavior as a result, provide the error message.</span></span> <span data-ttu-id="2e6c8-324">相反地，如果使用者可能會在未進行任何變更的情況下關閉訊息，請省略錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-324">By contrast, if users are likely to dismiss the message without doing or changing anything, omit the error message.</span></span>

<span data-ttu-id="2e6c8-325">**設計正確的錯誤處理**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-325">**Designing for good error handling**</span></span>

<span data-ttu-id="2e6c8-326">雖然製作良好的錯誤訊息正文可能是一項挑戰，但有時候程式可能不會有良好的錯誤處理支援。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-326">While crafting good error message text can be challenging, sometimes it is impossible without good error handling support from the program.</span></span> <span data-ttu-id="2e6c8-327">請考慮下列錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-327">Consider this error message:</span></span>

<span data-ttu-id="2e6c8-328">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-328">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-329">訊息的螢幕擷取畫面：未知的錯誤</span><span class="sxs-lookup"><span data-stu-id="2e6c8-329">screen shot of message: unknown error</span></span> ](images/mess-error-image15.png)

<span data-ttu-id="2e6c8-330">問題其實是未知的，因為缺少程式的錯誤處理支援。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-330">Chances are, the problem really is unknown because the program's error handling support is lacking.</span></span>

<span data-ttu-id="2e6c8-331">雖然這是很不好的寫入錯誤訊息，但更可能的原因是，基礎程式碼沒有已知的良好錯誤處理，因此沒有已知問題的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-331">While it's possible that this is a very poorly written error message, it more likely reflects the lack of good error handling by the underlying code there is no specific information known about the problem.</span></span>

<span data-ttu-id="2e6c8-332">為了建立特定、可操作、以使用者為中心的錯誤訊息，程式的錯誤處理常式代碼必須提供特定的高階錯誤資訊：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-332">In order to create specific, actionable, user-centered error messages, your program's error handling code must provide specific, high-level error information:</span></span>

- <span data-ttu-id="2e6c8-333">每個問題都應指派唯一的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-333">Each problem should have a unique error code assigned.</span></span>
- <span data-ttu-id="2e6c8-334">如果問題有幾個原因，程式應該盡可能判斷特定的原因。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-334">If a problem has several causes, the program should determine the specific cause whenever possible.</span></span>
- <span data-ttu-id="2e6c8-335">如果問題有參數，則必須維持參數。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-335">If the problem has parameters, the parameters must be maintained.</span></span>
- <span data-ttu-id="2e6c8-336">低層級的問題必須以夠高的層級處理，以便從使用者的觀點來呈現錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-336">Low-level problems must be handled at a sufficiently high level so that the error message can be presented from the user's point of view.</span></span>

<span data-ttu-id="2e6c8-337">良好的錯誤訊息不只是 UI 問題，而是軟體設計的問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-337">Good error messages aren't just a UI problem, they are a software design problem.</span></span> <span data-ttu-id="2e6c8-338">好的錯誤訊息體驗並不是可以在稍後附加的。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-338">A good error message experience isn't something that can be tacked on later.</span></span>

<span data-ttu-id="2e6c8-339">**疑難排解 (以及如何避免)**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-339">**Troubleshooting (and how to avoid it)**</span></span>

<span data-ttu-id="2e6c8-340">如果有數個不同的原因發生問題，則會回報單一錯誤訊息的疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-340">Troubleshooting results when a problem with several different causes is reported with a single error message.</span></span>

<span data-ttu-id="2e6c8-341">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-341">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-342">指出三個原因的一則訊息的圖表</span><span class="sxs-lookup"><span data-stu-id="2e6c8-342">diagram of one message stating three causes</span></span> ](images/mess-error-image16.png)

<span data-ttu-id="2e6c8-343">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-343">**Correct:**</span></span>

![三個訊息的圖表，指出每個訊息的原因](images/mess-error-image17.png)

<span data-ttu-id="2e6c8-345">使用單一錯誤訊息報告多個問題時的疑難排解結果。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-345">Troubleshooting results when several problems are reported with a single error message.</span></span>

<span data-ttu-id="2e6c8-346">在下列範例中，無法移動專案，因為它已經移動或刪除，或存取被拒。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-346">In the following example, an item couldn't be moved because it was already moved or deleted, or access was denied.</span></span> <span data-ttu-id="2e6c8-347">如果程式很容易判斷出原因，為什麼要讓使用者負擔來判斷特定的原因？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-347">If the program can easily determine the cause, why put the burden on the user to determine the specific cause?</span></span>

<span data-ttu-id="2e6c8-348">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-348">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-349">訊息的螢幕擷取畫面，說明兩個原因</span><span class="sxs-lookup"><span data-stu-id="2e6c8-349">screen shot of message stating two causes</span></span> ](images/mess-error-image18.png)

<span data-ttu-id="2e6c8-350">沒錯，這是什麼？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-350">Well, which is it?</span></span> <span data-ttu-id="2e6c8-351">現在使用者必須進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-351">Now the user has to troubleshoot.</span></span>

<span data-ttu-id="2e6c8-352">此程式可判斷是否拒絕存取，因此應回報此問題，並顯示特定的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-352">The program can determine if access was denied, so this problem should be reported with a specific error message.</span></span>

<span data-ttu-id="2e6c8-353">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-353">**Correct:**</span></span>

![<span data-ttu-id="2e6c8-354">訊息的螢幕擷取畫面，指出其中一個原因</span><span class="sxs-lookup"><span data-stu-id="2e6c8-354">screen shot of message stating one cause</span></span> ](images/mess-error-image19.png)

<span data-ttu-id="2e6c8-355">因為有特定的原因，所以不需要進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-355">With a specific cause, no troubleshooting is required.</span></span>

<span data-ttu-id="2e6c8-356">只有在無法判斷特定原因時，才使用具有多個原因的訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-356">Use messages with multiple causes only when the specific cause cannot be determined.</span></span> <span data-ttu-id="2e6c8-357">在此範例中，程式很難判斷專案是否已移動或刪除，因此可能會在這裡使用具有多個原因的單一錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-357">In this example, it would be difficult for the program to determine if the item was moved or deleted, so a single error message with multiple causes might be used here.</span></span> <span data-ttu-id="2e6c8-358">不過，使用者不太可能會在意，例如，他們無法移動已刪除的檔案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-358">However, it's unlikely that users are going to care if, for example, they couldn't move a deleted file.</span></span> <span data-ttu-id="2e6c8-359">基於這些原因，錯誤訊息甚至不是必要的。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-359">For these causes, the error message isn't even necessary.</span></span>

<span data-ttu-id="2e6c8-360">**處理未知的錯誤**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-360">**Handling unknown errors**</span></span>

<span data-ttu-id="2e6c8-361">在某些情況下，您的真的不會知道問題、原因或解決方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-361">In some cases, you genuinely won't know the problem, cause, or the solution.</span></span> <span data-ttu-id="2e6c8-362">如果要造成來抑制錯誤，最好事先瞭解缺少的資訊，而不是呈現問題、原因或可能不正確的解決方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-362">If it would be unwise to suppress the error, it is better to be up front about the lack of information than to present problems, causes, or solutions that might not be right.</span></span>

<span data-ttu-id="2e6c8-363">例如，如果您的程式有未處理的例外狀況，則下列錯誤訊息適用：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-363">For example, if your program has an unhandled exception, the following error message is suitable:</span></span>

![<span data-ttu-id="2e6c8-364">訊息的螢幕擷取畫面：發生未知的錯誤</span><span class="sxs-lookup"><span data-stu-id="2e6c8-364">screen shot of message: unknown error occurred</span></span> ](images/mess-error-image20.png)

<span data-ttu-id="2e6c8-365">如果您無法隱藏未知的錯誤，最好先事先瞭解缺少的資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-365">If you can't suppress an unknown error, it is better to be up front about the lack of information.</span></span>

<span data-ttu-id="2e6c8-366">另一方面，如果在大部分的情況下可能很有説明，請確實提供特定、可採取動作的資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-366">On the other hand, do provide specific, actionable information if it is likely to be helpful most of the time.</span></span>

![<span data-ttu-id="2e6c8-367">顯示 Office Communicator 「伺服器無法使用」訊息的螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-367">Screenshot that shows an Office Communicator 'server unavailable' message.</span></span> ](images/mess-error-image21.png)

<span data-ttu-id="2e6c8-368">如果網路連線通常是問題，則此錯誤訊息適用于未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-368">This error message is suitable for an unknown error if network connectivity is usually the problem.</span></span>

<span data-ttu-id="2e6c8-369">**判斷適當的訊息類型**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-369">**Determine the appropriate message type**</span></span>

<span data-ttu-id="2e6c8-370">根據強調和措辭，某些問題可能會顯示為錯誤、警告或資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-370">Some issues can be presented as an error, warning, or information, depending on the emphasis and phrasing.</span></span> <span data-ttu-id="2e6c8-371">例如，假設網頁無法根據目前的 Windows Internet Explorer 設定載入未簽署的 ActiveX 控制項：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-371">For example, suppose a Web page cannot load an unsigned ActiveX control based on the current Windows Internet Explorer configuration:</span></span>

- <span data-ttu-id="2e6c8-372">**錯誤。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-372">**Error.**</span></span> <span data-ttu-id="2e6c8-373">「此頁面無法載入未簽署的 ActiveX 控制項。」</span><span class="sxs-lookup"><span data-stu-id="2e6c8-373">"This page cannot load an unsigned ActiveX control."</span></span> <span data-ttu-id="2e6c8-374"> (片語做為現有的問題。 ) </span><span class="sxs-lookup"><span data-stu-id="2e6c8-374">(Phrased as an existing problem.)</span></span>
- <span data-ttu-id="2e6c8-375">**警告。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-375">**Warning.**</span></span> <span data-ttu-id="2e6c8-376">「此頁面可能無法如預期般運作，因為 Windows Internet Explorer 未設定為載入未簽署的 ActiveX 控制項。」</span><span class="sxs-lookup"><span data-stu-id="2e6c8-376">"This page might not behave as expected because Windows Internet Explorer isn't configured to load unsigned ActiveX controls."</span></span> <span data-ttu-id="2e6c8-377">或「允許此頁面安裝未簽署的 ActiveX 控制項？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-377">or "Allow this page to install an unsigned ActiveX Control?</span></span> <span data-ttu-id="2e6c8-378">從不受信任的來源執行此動作可能會危害您的電腦。」</span><span class="sxs-lookup"><span data-stu-id="2e6c8-378">Doing so from untrusted sources may harm your computer."</span></span> <span data-ttu-id="2e6c8-379"> (這兩個片語為可能會導致未來問題的狀況。 ) </span><span class="sxs-lookup"><span data-stu-id="2e6c8-379">(Both phrased as conditions that may cause future problems.)</span></span>
- <span data-ttu-id="2e6c8-380">**資訊。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-380">**Information.**</span></span> <span data-ttu-id="2e6c8-381">「您已設定 Windows Internet Explorer 封鎖未簽署的 ActiveX 控制項。」</span><span class="sxs-lookup"><span data-stu-id="2e6c8-381">"You have configured Windows Internet Explorer to block unsigned ActiveX controls."</span></span> <span data-ttu-id="2e6c8-382"> (片語作為事實的陳述。 ) </span><span class="sxs-lookup"><span data-stu-id="2e6c8-382">(Phrased as a statement of fact.)</span></span>

<span data-ttu-id="2e6c8-383">**若要判斷適當的訊息類型，請將焦點放在使用者需要知道或採取行動之問題的最重要層面。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-383">**To determine the appropriate message type, focus on the most important aspect of the issue that users need to know or act upon.**</span></span> <span data-ttu-id="2e6c8-384">一般來說，如果問題封鎖使用者繼續進行，您應該將它顯示為錯誤;如果使用者可以繼續，請將它顯示為警告。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-384">Typically, if an issue blocks the user from proceeding, you should present it as an error; if the user can proceed, present it as a warning.</span></span> <span data-ttu-id="2e6c8-385">根據焦點製作 [主要指示](text-ui.md) 或其他對應的文字，然後選擇符合文字的圖示 ([標準](vis-std-icons.md) 或) 。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-385">Craft the [main instruction](text-ui.md) or other corresponding text based on that focus, then choose an icon ([standard](vis-std-icons.md) or otherwise) that matches the text.</span></span> <span data-ttu-id="2e6c8-386">主要的指令文字和圖示應該一律相符。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-386">The main instruction text and icons should always match.</span></span>

<span data-ttu-id="2e6c8-387">**錯誤訊息展示**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-387">**Error message presentation**</span></span>

<span data-ttu-id="2e6c8-388">Windows 程式中大部分的錯誤訊息都是使用強制回應對話方塊來呈現， (是本文中大部分的範例) ，但是還有其他選項：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-388">Most error messages in Windows programs are presented using modal dialog boxes (as are most examples in this article), but there are other options:</span></span>

- <span data-ttu-id="2e6c8-389">就地</span><span class="sxs-lookup"><span data-stu-id="2e6c8-389">In-place</span></span>
- <span data-ttu-id="2e6c8-390">汽球</span><span class="sxs-lookup"><span data-stu-id="2e6c8-390">Balloons</span></span>
- <span data-ttu-id="2e6c8-391">通知</span><span class="sxs-lookup"><span data-stu-id="2e6c8-391">Notifications</span></span>
- <span data-ttu-id="2e6c8-392">通知區域圖示</span><span class="sxs-lookup"><span data-stu-id="2e6c8-392">Notification area icons</span></span>
- <span data-ttu-id="2e6c8-393">狀態列</span><span class="sxs-lookup"><span data-stu-id="2e6c8-393">Status bars</span></span>
- <span data-ttu-id="2e6c8-394">記錄檔 (針對以 IT 專業人員為目標的錯誤) </span><span class="sxs-lookup"><span data-stu-id="2e6c8-394">Log files (for errors targeted at IT professionals)</span></span>

<span data-ttu-id="2e6c8-395">在強制回應對話方塊中放入錯誤訊息，具有要求使用者立即關注和通知的優點。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-395">Putting error messages in modal dialog boxes has the benefit of demanding the user's immediate attention and acknowledgement.</span></span> <span data-ttu-id="2e6c8-396">但是，如果不需要注意，這也是其主要缺點。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-396">However, this is also their primary drawback if that attention isn't necessary.</span></span>

![<span data-ttu-id="2e6c8-397">訊息的螢幕擷取畫面：停止您正在執行的工作</span><span class="sxs-lookup"><span data-stu-id="2e6c8-397">screen shot of message: stop what you are doing</span></span> ](images/mess-error-image22.png)

<span data-ttu-id="2e6c8-398">您真的需要中斷使用者，讓他們可以按一下 [關閉] 按鈕嗎？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-398">Do you really need to interrupt users so that they can click the Close button?</span></span> <span data-ttu-id="2e6c8-399">如果沒有，請考慮使用強制回應對話方塊的替代方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-399">If not, consider alternatives to using a modal dialog box.</span></span>

<span data-ttu-id="2e6c8-400">當使用者在繼續進行之前必須立即確認問題，但通常是不佳的選擇時，強制回應對話方塊是很好的選擇。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-400">Modal dialogs are a great choice when the user must acknowledge the problem immediately before continuing, but often a poor choice otherwise.</span></span> <span data-ttu-id="2e6c8-401">一般而言，您應該偏好使用可執行工作的最輕量呈現方式。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-401">Generally, you should prefer to use the lightest weight presentation that does the job well.</span></span>

<span data-ttu-id="2e6c8-402">**避免 overcommunicating**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-402">**Avoid overcommunicating**</span></span>

<span data-ttu-id="2e6c8-403">一般情況下， [使用者不會進行掃描](vis-layout.md)。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-403">Generally, [users don't read, they scan](vis-layout.md).</span></span> <span data-ttu-id="2e6c8-404">文字越多，就越難掃描文字，而使用者越可能完全不會讀懂文字。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-404">The more text there is, the harder the text is to scan, and the more likely users won't read the text at all.</span></span> <span data-ttu-id="2e6c8-405">因此，請務必將文字縮小至其基本資訊，並在需要時使用漸進式洩漏和說明連結以提供其他資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-405">As a result, it is important to reduce the text down to its essentials, and use progressive disclosure and Help links when necessary to provide additional information.</span></span>

<span data-ttu-id="2e6c8-406">有許多極端範例，但讓我們來看一個更常見的例子。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-406">There are many extreme examples, but let's look at one more typical.</span></span> <span data-ttu-id="2e6c8-407">下列範例中的大部分屬性都有良好的錯誤訊息，但其文字並不精確，而且需要動機才能讀取。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-407">The following example has most of the attributes of a good error message, but its text isn't concise and requires motivation to read.</span></span>

<span data-ttu-id="2e6c8-408">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-408">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-409">詳細資訊訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2e6c8-409">screen shot of verbose message</span></span> ](images/mess-error-image23.png)

<span data-ttu-id="2e6c8-410">這個範例是很好的錯誤訊息，但 overcommunicates。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-410">This example is a good error message, but it overcommunicates.</span></span>

<span data-ttu-id="2e6c8-411">這項文字真正說什麼？</span><span class="sxs-lookup"><span data-stu-id="2e6c8-411">What is all this text really saying?</span></span> <span data-ttu-id="2e6c8-412">就像這樣：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-412">Something like this:</span></span>

<span data-ttu-id="2e6c8-413">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-413">**Correct:**</span></span>

![<span data-ttu-id="2e6c8-414">訊息的螢幕擷取畫面：未偵測到 cd 錄製器</span><span class="sxs-lookup"><span data-stu-id="2e6c8-414">screen shot of message: cd recorder not detected</span></span> ](images/mess-error-image24.png)

<span data-ttu-id="2e6c8-415">這項錯誤訊息基本上都有相同的資訊，但是更簡潔。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-415">This error message has essentially the same information, but is far more concise.</span></span>

<span data-ttu-id="2e6c8-416">藉由使用 [說明] 來提供詳細資料，此錯誤訊息會有 [反向金字塔樣式](text-ui.md) 的簡報。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-416">By using Help to provide the details, this error message has an [inverted pyramid style](text-ui.md) of presentation.</span></span>

<span data-ttu-id="2e6c8-417">如需 overcommunicating 的詳細指導方針和範例，請參閱 [消費者介面文字](text-ui.md)。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-417">For more guidelines and examples on overcommunicating, see [User Interface Text](text-ui.md).</span></span>

<span data-ttu-id="2e6c8-418">**如果您只進行八件事**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-418">**If you do only eight things**</span></span>

1. <span data-ttu-id="2e6c8-419">設計程式以進行錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-419">Design your program for error handling.</span></span>
2. <span data-ttu-id="2e6c8-420">不要提供不必要的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-420">Don't give unnecessary error messages.</span></span>
3. <span data-ttu-id="2e6c8-421">提供必要的錯誤訊息，以避免使用者混淆。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-421">Avoid user confusion by giving necessary error messages.</span></span>
4. <span data-ttu-id="2e6c8-422">請確定錯誤訊息提供問題、原因和解決方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-422">Make sure the error message gives a problem, cause, and solution.</span></span>
5. <span data-ttu-id="2e6c8-423">請確定錯誤訊息是相關、可採取動作、簡短、明確、明確、不致和罕見的。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-423">Make sure the error message is relevant, actionable, brief, clear, specific, courteous, and rare.</span></span>
6. <span data-ttu-id="2e6c8-424">從使用者的觀點來設計錯誤訊息，而不是程式的觀點。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-424">Design error messages from the user's point of view, not the program's point of view.</span></span>
7. <span data-ttu-id="2e6c8-425">避免使用者進行疑難排解時，請針對每個可偵測的原因使用不同的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-425">Avoid involving the user in troubleshooting use a different error message for each detectable cause.</span></span>
8. <span data-ttu-id="2e6c8-426">使用可執行工作的最輕量呈現方法。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-426">Use the lightest weight presentation method that does the job well.</span></span>

<span data-ttu-id="2e6c8-427">**使用模式**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-427">**Usage patterns**</span></span>

<span data-ttu-id="2e6c8-428">錯誤訊息有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-428">Error messages have several usage patterns:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2e6c8-429"><strong>系統問題</strong></span><span class="sxs-lookup"><span data-stu-id="2e6c8-429"><strong>System problems</strong></span></span><br/> <span data-ttu-id="2e6c8-430">作業系統、硬體裝置、網路或程式失敗，或未處於執行工作所需的狀態。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-430">The operating system, hardware device, network, or program has failed or is not in the state required to perform a task.</span></span> <br/></td>
<td><span data-ttu-id="2e6c8-431">使用者可以解決許多系統問題：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-431">Many system problems can be solved by the user:</span></span> <br/>
<ul>
<li><span data-ttu-id="2e6c8-432">裝置問題可以藉由開啟裝置、重新連接裝置，以及插入媒體來解決。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-432">Device problems can be solved by turning the device on, reconnecting the device, and inserting media.</span></span></li>
<li><span data-ttu-id="2e6c8-433">您可以藉由檢查實體網路連線，以及執行 <strong>網路診斷和修復</strong>，來解決網路問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-433">Network problems can be solved by checking the physical network connect, and running <strong>Network diagnose and repair</strong>.</span></span></li>
<li><span data-ttu-id="2e6c8-434">您可以藉由變更程式選項或重新開機程式來解決程式問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-434">Program problems can be solved by changing program options or restarting the program.</span></span></li>
</ul>
<img src="images/mess-error-image25.png" alt="Screen shot of message: Can&#39;t find a camera " /><br/> <span data-ttu-id="2e6c8-435">在此範例中，程式找不到可執行使用者工作的相機。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-435">In this example, the program can't find a camera to perform a user task.</span></span><br/> <img src="images/mess-error-image26.png" alt="Screen shot of message Network discovery off " /><br/> <span data-ttu-id="2e6c8-436">在此範例中，必須開啟執行工作所需的功能。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-436">In this example, a feature required to perform a task needs to be turned on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e6c8-437"><strong>檔案問題</strong></span><span class="sxs-lookup"><span data-stu-id="2e6c8-437"><strong>File problems</strong></span></span><br/> <span data-ttu-id="2e6c8-438">找不到使用者起始的工作所需的檔案或資料夾、已在使用中，或其格式不正確。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-438">A file or folder required for a task initiated by the user was not found, is already in use, or doesn't have the expected format.</span></span> <br/></td>
<td><img src="images/mess-error-image27.png" alt="Screen shot of message: Can&#39;t delete file " /><br/> <span data-ttu-id="2e6c8-439">在此範例中，因為找不到檔案或資料夾，所以無法予以刪除。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-439">In this example, the file or folder can't be deleted because it wasn't found.</span></span><br/> <img src="images/mess-error-image28.png" alt="Screen shot of message: Can&#39;t play this file " /><br/> <span data-ttu-id="2e6c8-440">在此範例中，程式不支援指定的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-440">In this example, the program doesn't support the given file format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e6c8-441"><strong>安全性問題</strong></span><span class="sxs-lookup"><span data-stu-id="2e6c8-441"><strong>Security problems</strong></span></span><br/> <span data-ttu-id="2e6c8-442">使用者無權存取資源，或有足夠的許可權來執行使用者所起始的工作。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-442">The user doesn't have permission to access a resource, or sufficient privilege to perform a task initiated by the user.</span></span> <br/></td>
<td><img src="images/mess-error-image29.png" alt="Screen shot of message: You don&#39;t have permission " /><br/> <span data-ttu-id="2e6c8-443">在此範例中，使用者沒有存取資源的許可權。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-443">In this example, the user doesn't have permission to access a resource.</span></span><br/> <img src="images/mess-error-image30.png" alt="Screen shot of message: You don&#39;t have privilege " /><br/> <span data-ttu-id="2e6c8-444">在此範例中，使用者沒有執行工作的許可權。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-444">In this example, the user doesn't have the privilege to perform a task.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e6c8-445"><strong>工作問題</strong></span><span class="sxs-lookup"><span data-stu-id="2e6c8-445"><strong>Task problems</strong></span></span><br/> <span data-ttu-id="2e6c8-446">執行使用者所起始的工作 (不是系統、找不到檔案、檔案格式或安全性問題) 的特定問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-446">There is a specific problem performing a task initiated by the user (other than a system, file not found, file format, or security problem).</span></span> <br/></td>
<td><img src="images/mess-error-image31.png" alt="Screen shot of message: Data can&#39;t be pasted " /><br/> <span data-ttu-id="2e6c8-447">在此範例中，剪貼簿資料無法貼入繪圖中。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-447">In this example, the Clipboard data can't be pasted into Paint.</span></span><br/> <img src="images/mess-error-image32.png" alt="Screen shot of message: Upgrade can&#39;t be installed " /><br/> <span data-ttu-id="2e6c8-448">在此範例中，使用者無法安裝軟體升級。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-448">In this example, the user can't install a software upgrade.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2e6c8-449"><strong>使用者輸入問題</strong></span><span class="sxs-lookup"><span data-stu-id="2e6c8-449"><strong>User input problems</strong></span></span><br/> <span data-ttu-id="2e6c8-450">使用者輸入的值與其他使用者輸入不正確或不一致。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-450">The user entered a value that is incorrect or inconsistent with other user input.</span></span> <br/></td>
<td><img src="images/mess-error-image33.png" alt="Screen shot of message: Incorrect time value " /><br/> <span data-ttu-id="2e6c8-451">在此範例中，使用者輸入的時間值不正確。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-451">In this example, the user entered an incorrect time value.</span></span><br/> <img src="images/mess-error-image34.png" alt="Screen shot of message: Incorrect input format " /><br/> <span data-ttu-id="2e6c8-452">在此範例中，使用者輸入的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-452">In this example, user input is not in the correct format.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="guidelines"></a><span data-ttu-id="2e6c8-453">指導方針</span><span class="sxs-lookup"><span data-stu-id="2e6c8-453">Guidelines</span></span>

### <a name="presentation"></a><span data-ttu-id="2e6c8-454">簡報</span><span class="sxs-lookup"><span data-stu-id="2e6c8-454">Presentation</span></span>

- <span data-ttu-id="2e6c8-455">在 **適當時使用工作對話方塊**，以達成一致的外觀和配置。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-455">**Use task dialogs whenever appropriate** to achieve a consistent look and layout.</span></span> <span data-ttu-id="2e6c8-456">工作對話方塊需要 Windows Vista 或更新版本，因此不適用於舊版 Windows。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-456">Task dialogs require Windows Vista or later, so they aren't suitable for earlier versions of Windows.</span></span> <span data-ttu-id="2e6c8-457">如果您必須使用訊息方塊，請使用兩個分行符號分隔出補充指令中的主要指令。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-457">If you must use a message box, separate the main instruction from the supplemental instruction with two line breaks.</span></span>

### <a name="user-input-errors"></a><span data-ttu-id="2e6c8-458">使用者輸入錯誤</span><span class="sxs-lookup"><span data-stu-id="2e6c8-458">User input errors</span></span>

- <span data-ttu-id="2e6c8-459">**可能的話，請避免或減少使用者輸入錯誤：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-459">**Whenever possible, prevent or reduce user input errors by:**</span></span>
  - <span data-ttu-id="2e6c8-460">使用受限於有效值的控制項。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-460">Using controls that are constrained to valid values.</span></span>
  - <span data-ttu-id="2e6c8-461">當您按一下時停用控制項和功能表項目，就會導致錯誤，只要它很明顯地停用控制項或功能表項目。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-461">Disabling controls and menu items when clicking would result in error, as long as it's obvious why the control or menu item is disabled.</span></span>
  - <span data-ttu-id="2e6c8-462">提供良好的預設值。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-462">Providing good default values.</span></span>

<span data-ttu-id="2e6c8-463">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-463">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-464">具有喇叭音量標籤的文字方塊螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2e6c8-464">screen shot of text box with speaker volume label</span></span> ](images/mess-error-image35.png)

<span data-ttu-id="2e6c8-465">在此範例中，限制的輸入會使用未受限制的文字方塊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-465">In this example, an unconstrained text box is used for constrained input.</span></span> <span data-ttu-id="2e6c8-466">請改用滑杆。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-466">Use a slider instead.</span></span>

- <span data-ttu-id="2e6c8-467">**針對內容使用者輸入問題，使用非強制回應錯誤處理 (就地錯誤或氣球) 。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-467">**Use modeless error handling (in-place errors or balloons) for contextual user input problems.**</span></span>
- <span data-ttu-id="2e6c8-468">**在文字方塊中或在文字方塊失去焦點之後，于文字方塊中偵測到非關鍵性、單一點使用者輸入問題時，請使用球標。**[氣球](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) 不需要可用的螢幕空間或顯示就地訊息所需的動態配置。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-468">**Use balloons for non-critical, single-point user input problems detected while in a text box or immediately after a text box loses focus.**[Balloons](https://msdn.microsoft.com/library/windows/desktop/aa511451.aspx) don't require available screen space or the dynamic layout that is required to display in-place messages.</span></span> <span data-ttu-id="2e6c8-469">一次只顯示一個氣球。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-469">Display only a single balloon at a time.</span></span> <span data-ttu-id="2e6c8-470">因為此問題並不重要，所以不需要任何錯誤圖示。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-470">Because the problem isn't critical, no error icon is necessary.</span></span> <span data-ttu-id="2e6c8-471">當您按下、解決問題或在超時後，就會離開氣球。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-471">Balloons go away when clicked, when the problem is resolved, or after a timeout.</span></span>

![<span data-ttu-id="2e6c8-472">訊息的螢幕擷取畫面：不正確的字元</span><span class="sxs-lookup"><span data-stu-id="2e6c8-472">screen shot of message: incorrect character</span></span> ](images/mess-error-image36.png)

<span data-ttu-id="2e6c8-473">在此範例中，氣球表示輸入問題仍然存在於控制項中。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-473">In this example, a balloon indicates an input problem while still in the control.</span></span>

- <span data-ttu-id="2e6c8-474">**使用就地錯誤偵測延遲的錯誤偵測，** 通常是按一下 [認可] 按鈕找到的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-474">**Use in-place errors for delayed error detection,** usually errors found by clicking a commit button.</span></span> <span data-ttu-id="2e6c8-475"> (不會 [在](glossary.md) 立即認可的設定中使用就地錯誤。 ) 一次可能會有多個就地錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-475">(Don't use [in-place errors](glossary.md) for settings that are immediately committed.) There can be multiple in-place errors at a time.</span></span> <span data-ttu-id="2e6c8-476">使用一般文字和16x16 圖元錯誤圖示，盡可能將它們直接放在問題旁。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-476">Use normal text and a 16x16 pixel error icon, placing them directly next to the problem whenever possible.</span></span> <span data-ttu-id="2e6c8-477">除非使用者認可，且找不到任何其他錯誤，否則就地錯誤不會消失。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-477">In-place errors don't go away unless the user commits and no other errors are found.</span></span>

![<span data-ttu-id="2e6c8-478">訊息的螢幕擷取畫面：不正確的電子郵件地址</span><span class="sxs-lookup"><span data-stu-id="2e6c8-478">screen shot of message: incorrect e-mail address</span></span> ](images/mess-error-image37.png)

<span data-ttu-id="2e6c8-479">在此範例中，按一下 [認可] 按鈕時，會使用就地錯誤來進行找到。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-479">In this example, an in-place error is used for an error found by clicking the commit button.</span></span>

- <span data-ttu-id="2e6c8-480">**針對所有其他問題，使用強制回應錯誤處理 (工作對話方塊或訊息方塊) ，** 包括牽涉到多個控制項的錯誤，或是按一下 [認可] 按鈕時發現非內容相關或非輸入的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-480">**Use modal error handling (task dialogs or message boxes) for all other problems,** including errors that involve multiple controls or are non-contextual or non-input errors found by clicking a commit button.</span></span>
- <span data-ttu-id="2e6c8-481">**當回報使用者輸入問題時，請將輸入焦點設定為具有不正確資料的第一個控制項。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-481">**When a user input problem is reported, set input focus to the first control with the incorrect data.**</span></span> <span data-ttu-id="2e6c8-482">必要時，將控制項滾動至 view。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-482">Scroll the control into view if necessary.</span></span> <span data-ttu-id="2e6c8-483">如果控制項是文字方塊，請選取 [完整內容]。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-483">If the control is a text box, select the entire contents.</span></span> <span data-ttu-id="2e6c8-484">這應該一律是錯誤訊息所參考的內容。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-484">It should always be obvious what the error message is referring to.</span></span>
- <span data-ttu-id="2e6c8-485">**請勿清除不正確的輸入。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-485">**Don't clear incorrect input.**</span></span> <span data-ttu-id="2e6c8-486">相反地，請將它保留，讓使用者可以看到並修正問題，而不需要從頭開始。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-486">Instead, leave it so that the user can see and correct the problem without starting over.</span></span>
  - <span data-ttu-id="2e6c8-487">**例外狀況：** 清除不正確的密碼和 PIN 文字方塊，因為使用者無法有效更正遮罩輸入。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-487">**Exception:** Clear incorrect password and PIN text boxes because users can't correct masked input effectively.</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="2e6c8-488">疑難排解</span><span class="sxs-lookup"><span data-stu-id="2e6c8-488">Troubleshooting</span></span>

- <span data-ttu-id="2e6c8-489">**避免建立疑難排解問題。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-489">**Avoid creating troubleshooting problems.**</span></span> <span data-ttu-id="2e6c8-490">請勿依賴單一錯誤訊息來回報有幾個不同可偵測原因的問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-490">Don't rely on a single error message to report a problem with several different detectable causes.</span></span>
- <span data-ttu-id="2e6c8-491">**使用不同的錯誤訊息 (針對每個可偵測的原因，通常會有不同的補充指令) 。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-491">**Use a different error message (typically a different supplemental instruction) for each detectable cause.**</span></span> <span data-ttu-id="2e6c8-492">例如，如果檔案因為許多原因而無法開啟，請針對每個原因提供個別的補充指令。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-492">For example, if a file cannot be opened for several reasons, provide a separate supplemental instruction for each reason.</span></span>
- <span data-ttu-id="2e6c8-493">**只有在無法判斷特定原因時，才使用具有多個原因的訊息。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-493">**Use a message with multiple causes only when the specific cause can't be determined.**</span></span> <span data-ttu-id="2e6c8-494">在此情況下，請依解決問題的可能性來呈現解決方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-494">In this case, present the solutions in order of likelihood of fixing the problem.</span></span> <span data-ttu-id="2e6c8-495">這麼做可協助使用者更有效率地解決問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-495">Doing so helps users solve the problem more efficiently.</span></span>

### <a name="icons"></a><span data-ttu-id="2e6c8-496">圖示</span><span class="sxs-lookup"><span data-stu-id="2e6c8-496">Icons</span></span>

- <span data-ttu-id="2e6c8-497">**強制回應錯誤訊息對話方塊沒有標題列圖示。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-497">**Modal error message dialogs don't have title bar icons.**</span></span> <span data-ttu-id="2e6c8-498">標題列圖示會用來做為主視窗與次要視窗之間的視覺差異。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-498">Title bar icons are used as a visual distinction between primary windows and secondary windows.</span></span>
- <span data-ttu-id="2e6c8-499">**使用錯誤圖示。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-499">**Use an error icon.**</span></span> <span data-ttu-id="2e6c8-500">例外狀況：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-500">Exceptions:</span></span>
  - <span data-ttu-id="2e6c8-501">如果錯誤是使用強制回應對話方塊或氣球顯示的使用者輸入問題，請不要使用圖示。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-501">If the error is a user input problem displayed using a modal dialog box or balloon, don't use an icon.</span></span> <span data-ttu-id="2e6c8-502">這麼做是 Windows 的鼓勵語氣的計數器。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-502">Doing so is counter to the encouraging tone of Windows.</span></span> <span data-ttu-id="2e6c8-503">不過，就地錯誤訊息應該使用較小的錯誤圖示 (16x16 圖元) 來清楚地將它們識別為錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-503">However, in-place error messages should use a small error icon (16x16 pixel) to clearly identify them as error messages.</span></span>

     ![郵件的螢幕擷取畫面不正確的郵遞區號格式](images/mess-error-image38.png)

     ![郵件電腦名稱稱太長的螢幕擷取畫面](images/mess-error-image39.png)

     <span data-ttu-id="2e6c8-506">在這些範例中，使用者輸入問題不需要錯誤圖示。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-506">In these examples, user input problems don't need error icons.</span></span>

     ![郵件電話號碼格式錯誤的螢幕擷取畫面](images/mess-error-image40.png)

     <span data-ttu-id="2e6c8-508">在此範例中，就地錯誤訊息需要較小的錯誤圖示，以明確地將其識別為錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-508">In this example, an in-place error message needs a small error icon to clearly identify it as an error message.</span></span>

- <span data-ttu-id="2e6c8-509">如果問題是因為有圖示 (而不是使用者輸入問題的功能) ，您可以使用功能圖示搭配錯誤重迭。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-509">If the problem is for a feature that has an icon (and not a user input problem), you can use the feature icon with an error overlay.</span></span> <span data-ttu-id="2e6c8-510">如果您這麼做，也請使用功能名稱做為錯誤的主旨。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-510">If you do this, also use the feature name as the error's subject.</span></span>

    ![<span data-ttu-id="2e6c8-511">螢幕擷取畫面訊息媒體播放機無法播放檔案</span><span class="sxs-lookup"><span data-stu-id="2e6c8-511">screen shot message media player can't play file</span></span> ](images/mess-error-image41.png)

    <span data-ttu-id="2e6c8-512">在此範例中，功能圖示有錯誤重迭，而此功能是錯誤的主旨。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-512">In this example, the feature icon has an error overlay, and the feature is the subject of the error.</span></span>

- <span data-ttu-id="2e6c8-513">**請勿使用警告圖示來發生錯誤。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-513">**Don't use warning icons for errors.**</span></span> <span data-ttu-id="2e6c8-514">這麼做通常是為了讓簡報感覺更不嚴重。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-514">This is often done to make the presentation feel less severe.</span></span> <span data-ttu-id="2e6c8-515">錯誤不是警告。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-515">Errors aren't warnings.</span></span>

    <span data-ttu-id="2e6c8-516">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-516">**Incorrect:**</span></span>

    ![<span data-ttu-id="2e6c8-517">未啟用 [訊息快速切換] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2e6c8-517">screen shot of message fast switching not enabled</span></span> ](images/mess-error-image42.png)

    <span data-ttu-id="2e6c8-518">在此範例中，會不正確地使用警告圖示來使錯誤感到較不嚴重。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-518">In this example, a warning icon is incorrectly used to make the error feel less severe.</span></span>

<span data-ttu-id="2e6c8-519">如需更多指導方針和範例，請參閱 [標準圖示](vis-std-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-519">For more guidelines and examples, see [Standard Icons](vis-std-icons.md).</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="2e6c8-520">漸進式揭露</span><span class="sxs-lookup"><span data-stu-id="2e6c8-520">Progressive disclosure</span></span>

- <span data-ttu-id="2e6c8-521">**使用 [顯示/隱藏詳細資料的漸進式洩漏] 按鈕，即可在錯誤訊息中隱藏高階或詳細的資訊。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-521">**Use a Show/Hide details progressive disclosure button to hide advanced or detailed information in an error message.**</span></span> <span data-ttu-id="2e6c8-522">這麼做可簡化一般使用的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-522">Doing so simplifies the error message for typical usage.</span></span> <span data-ttu-id="2e6c8-523">請勿隱藏需要的資訊，因為使用者可能找不到它。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-523">Don't hide needed information, because users might not find it.</span></span>

![<span data-ttu-id="2e6c8-524">訊息的螢幕擷取畫面： activesync 無法登入</span><span class="sxs-lookup"><span data-stu-id="2e6c8-524">screen shot of message: activesync can't log on</span></span> ](images/mess-error-image43.png)

<span data-ttu-id="2e6c8-525">在此範例中，[漸進式洩漏] 按鈕可協助使用者視需要向下切入至更多詳細資料，或在不需要時簡化 UI。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-525">In this example, the progressive disclosure button helps users drill down to more detail if they want it, or simplify the UI if they don't.</span></span>

- <span data-ttu-id="2e6c8-526">**除非真的有更多詳細資料，否則請勿使用顯示/隱藏詳細資料。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-526">**Don't use Show/Hide details unless there really is more detail.**</span></span> <span data-ttu-id="2e6c8-527">請勿只以更詳細的格式重新聲明現有的資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-527">Don't just restate the existing information in a more verbose format.</span></span>
- <span data-ttu-id="2e6c8-528">**請勿使用顯示/隱藏詳細資料來顯示說明資訊。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-528">**Don't use Show/Hide details to show Help information.**</span></span> <span data-ttu-id="2e6c8-529">請改用說明連結。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-529">Use Help links instead.</span></span>

<span data-ttu-id="2e6c8-530">如需標籤指導方針，請參閱 [漸進式洩漏控制項](ctrl-progressive-disclosure-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-530">For labeling guidelines, see [Progressive Disclosure Controls](ctrl-progressive-disclosure-controls.md).</span></span>

<span data-ttu-id="2e6c8-531">**不要再顯示此訊息**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-531">**Don't show this message again**</span></span>

- <span data-ttu-id="2e6c8-532">**如果錯誤訊息需要此選項，請重新考慮錯誤和其頻率。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-532">**If an error message needs this option, reconsider the error and its frequency.**</span></span> <span data-ttu-id="2e6c8-533">如果它有良好錯誤的所有特性 (相關、可採取動作且不頻繁的) ，使用者就不應該將它隱藏起來。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-533">If it has all the characteristics of a good error (relevant, actionable, and infrequent), it shouldn't make sense for users to suppress it.</span></span>

<span data-ttu-id="2e6c8-534">如需詳細指導方針，請參閱 [對話方塊](win-dialog-box.md)。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-534">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="2e6c8-535">預設值</span><span class="sxs-lookup"><span data-stu-id="2e6c8-535">Default values</span></span>

- <span data-ttu-id="2e6c8-536">**選取最安全、最不具破壞性或最安全的回應作為預設值。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-536">**Select the safest, least destructive, or most secure response to be the default.**</span></span> <span data-ttu-id="2e6c8-537">如果安全性不是因素，請選取最有可能或方便的命令。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-537">If safety isn't a factor, select the most likely or convenient command.</span></span>

### <a name="help"></a><span data-ttu-id="2e6c8-538">Help</span><span class="sxs-lookup"><span data-stu-id="2e6c8-538">Help</span></span>

- <span data-ttu-id="2e6c8-539">**設計錯誤訊息，以避免需要協助。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-539">**Design error messages to avoid the need for Help.**</span></span> <span data-ttu-id="2e6c8-540">除非解決方案需要執行幾個步驟，否則使用者通常不需要讀取外部文字來瞭解並解決問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-540">Ordinarily users shouldn't have to read external text to understand and solve the problem, unless the solution requires several steps.</span></span>
- <span data-ttu-id="2e6c8-541">**請確定說明內容相關且實用。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-541">**Make sure the Help content is relevant and helpful.**</span></span> <span data-ttu-id="2e6c8-542">它不應該是錯誤訊息的詳細重述，而是應該包含超出錯誤訊息範圍的有用資訊，例如避免未來發生問題的方法。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-542">It shouldn't be a verbose restatement of the error message rather, it should contain useful information that is beyond the scope of the error message, such as ways to avoid the problem in the future.</span></span> <span data-ttu-id="2e6c8-543">請不要提供說明連結，因為您可以。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-543">Don't provide a Help link just because you can.</span></span>
- <span data-ttu-id="2e6c8-544">**使用特定、簡潔、相關的說明連結來存取說明內容。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-544">**Use specific, concise, relevant Help links to access Help content.**</span></span> <span data-ttu-id="2e6c8-545">請勿針對此用途使用命令按鈕或漸進式洩漏。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-545">Don't use command buttons or progressive disclosure for this purpose.</span></span>
- <span data-ttu-id="2e6c8-546">**對於您無法進行特定和可採取動作的錯誤訊息，請考慮提供線上說明內容的連結。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-546">**For error messages that you can't make specific and actionable, consider providing links to online Help content.**</span></span> <span data-ttu-id="2e6c8-547">如此一來，您就可以為使用者提供您在程式發行後可以更新的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-547">By doing so, you can provide users with additional information that you can update after the program is released.</span></span>

<span data-ttu-id="2e6c8-548">如需詳細指導方針， [請參閱說明](winenv-help.md)。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-548">For more guidelines, see [Help](winenv-help.md).</span></span>

### <a name="error-codes"></a><span data-ttu-id="2e6c8-549">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="2e6c8-549">Error codes</span></span>

- <span data-ttu-id="2e6c8-550">**針對您無法進行特定且可採取動作的錯誤訊息，或從 [說明] 獲益的錯誤訊息，請考慮同時提供錯誤碼。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-550">**For error messages that you can't make specific and actionable or they benefit from Help, consider also providing error codes.**</span></span> <span data-ttu-id="2e6c8-551">使用者通常會使用這些錯誤碼來搜尋網際網路，以取得其他資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-551">Users often use these error codes to search the Internet for additional information.</span></span>
- <span data-ttu-id="2e6c8-552">**一律提供問題和解決方案的文字描述。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-552">**Always provide a text description of the problem and solution.**</span></span> <span data-ttu-id="2e6c8-553">請勿依賴此用途的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-553">Don't depend just on the error code for this purpose.</span></span>

<span data-ttu-id="2e6c8-554">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-554">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-555">訊息的螢幕擷取畫面：無法開啟檔案</span><span class="sxs-lookup"><span data-stu-id="2e6c8-555">screen shot of message: unable to open file</span></span> ](images/mess-error-image44.png)

<span data-ttu-id="2e6c8-556">在此範例中，會使用錯誤碼作為解決方案文字的替代方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-556">In this example, an error code is used as a substitute for a solution text.</span></span>

- <span data-ttu-id="2e6c8-557">**為每個不同的原因指派一個唯一的錯誤碼。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-557">**Assign a unique error code for each different cause.**</span></span> <span data-ttu-id="2e6c8-558">這樣做可避免疑難排解問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-558">Doing so avoids troubleshooting.</span></span>
- <span data-ttu-id="2e6c8-559">**選擇可在網際網路上輕鬆搜尋的錯誤碼。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-559">**Choose error codes that are easily searchable on the Internet.**</span></span> <span data-ttu-id="2e6c8-560">如果您使用32位的代碼，請使用十六進位標記法搭配前置的 "0x" 和大寫字元。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-560">If you use 32-bit codes, use a hexadecimal representation with a leading "0x" and uppercase characters.</span></span>

<span data-ttu-id="2e6c8-561">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-561">**Correct:**</span></span>

<span data-ttu-id="2e6c8-562">1234</span><span class="sxs-lookup"><span data-stu-id="2e6c8-562">1234</span></span>

<span data-ttu-id="2e6c8-563">0xC0001234</span><span class="sxs-lookup"><span data-stu-id="2e6c8-563">0xC0001234</span></span>

<span data-ttu-id="2e6c8-564">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-564">**Incorrect:**</span></span>

<span data-ttu-id="2e6c8-565">-1</span><span class="sxs-lookup"><span data-stu-id="2e6c8-565">-1</span></span>

<span data-ttu-id="2e6c8-566">-67113524</span><span class="sxs-lookup"><span data-stu-id="2e6c8-566">-67113524</span></span>

- <span data-ttu-id="2e6c8-567">**使用 [顯示/隱藏詳細資料] 顯示錯誤碼。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-567">**Use Show/Hide details to display error codes.**</span></span> <span data-ttu-id="2e6c8-568">片語為錯誤碼： <error code> 。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-568">Phrase as Error code: <error code>.</span></span>

![<span data-ttu-id="2e6c8-569">訊息的螢幕擷取畫面：程式未初始化</span><span class="sxs-lookup"><span data-stu-id="2e6c8-569">screen shot of message: program didn't initialize</span></span> ](images/mess-error-image45.png)

<span data-ttu-id="2e6c8-570">在此範例中，會使用錯誤碼來補充可受益于進一步資訊的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-570">In this example, an error code is used to supplement an error message that can benefit from further information.</span></span>

### <a name="sound"></a><span data-ttu-id="2e6c8-571">音效</span><span class="sxs-lookup"><span data-stu-id="2e6c8-571">Sound</span></span>

- <span data-ttu-id="2e6c8-572">**不要伴隨著有音效效果或嗶聲的錯誤訊息。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-572">**Don't accompany error messages with a sound effect or beep.**</span></span> <span data-ttu-id="2e6c8-573">這麼做是 jarring 且不必要的。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-573">Doing so is jarring and unnecessary.</span></span>
  - <span data-ttu-id="2e6c8-574">**例外狀況：** 如果問題對電腦操作很重要，請播放重大的停止音效，而使用者必須立即採取行動以防止嚴重的後果。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-574">**Exception:** Play the Critical Stop sound effect if the problem is critical to the operation of the computer, and the user must take immediate action to prevent serious consequences.</span></span>

## <a name="text"></a><span data-ttu-id="2e6c8-575">Text</span><span class="sxs-lookup"><span data-stu-id="2e6c8-575">Text</span></span>

<span data-ttu-id="2e6c8-576">**一般**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-576">**General**</span></span>

- <span data-ttu-id="2e6c8-577">**移除多餘的文字。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-577">**Remove redundant text.**</span></span> <span data-ttu-id="2e6c8-578">在標題、主要指示、補充指示、命令連結和認可按鈕中尋找。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-578">Look for it in titles, main instructions, supplemental instructions, command links, and commit buttons.</span></span> <span data-ttu-id="2e6c8-579">一般而言，請在指示和互動式控制項中保留完整文字，然後從其他位置移除任何多餘的。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-579">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
- <span data-ttu-id="2e6c8-580">**使用以使用者為主的說明。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-580">**Use user-centered explanations.**</span></span> <span data-ttu-id="2e6c8-581">根據使用者動作或目標來描述問題，而不是在軟體不滿意的方面描述。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-581">Describe the problem in terms of user actions or goals, not in terms of what the software is unhappy with.</span></span> <span data-ttu-id="2e6c8-582">使用目標使用者瞭解並使用的語言。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-582">Use language that the target users understand and use.</span></span> <span data-ttu-id="2e6c8-583">避免技術術語。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-583">Avoid technical jargon.</span></span>

<span data-ttu-id="2e6c8-584">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-584">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-585">訊息的螢幕擷取畫面：輸入-同步呼叫</span><span class="sxs-lookup"><span data-stu-id="2e6c8-585">screen shot of message: input-synchronous call</span></span> ](images/mess-error-image46.png)

<span data-ttu-id="2e6c8-586">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-586">**Correct:**</span></span>

![<span data-ttu-id="2e6c8-587">訊息的螢幕擷取畫面：忙碌接收來電</span><span class="sxs-lookup"><span data-stu-id="2e6c8-587">screen shot of message: busy receiving a call</span></span> ](images/mess-error-image47.png)

<span data-ttu-id="2e6c8-588">在這些範例中，正確的版本會說出使用者的語言，而不正確的版本則會過於技術性。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-588">In these examples, the correct version speaks the user's language whereas the incorrect version is overly technical.</span></span>

- <span data-ttu-id="2e6c8-589">**請勿使用下列文字：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-589">**Don't use the following words:**</span></span>
  - <span data-ttu-id="2e6c8-590">錯誤，失敗 (改為使用問題) </span><span class="sxs-lookup"><span data-stu-id="2e6c8-590">Error, failure (use problem instead)</span></span>
  - <span data-ttu-id="2e6c8-591">無法 (使用無法改為) </span><span class="sxs-lookup"><span data-stu-id="2e6c8-591">Failed to (use unable to instead)</span></span>
  - <span data-ttu-id="2e6c8-592">不合法、無效、錯誤 (請改用不正確的) </span><span class="sxs-lookup"><span data-stu-id="2e6c8-592">Illegal, invalid, bad (use incorrect instead)</span></span>
  - <span data-ttu-id="2e6c8-593">Abort、kill、terminate (使用 stop 改) </span><span class="sxs-lookup"><span data-stu-id="2e6c8-593">Abort, kill, terminate (use stop instead)</span></span>
  - <span data-ttu-id="2e6c8-594">嚴重的嚴重 (請改用嚴重的) </span><span class="sxs-lookup"><span data-stu-id="2e6c8-594">Catastrophic, fatal (use serious instead)</span></span>

<span data-ttu-id="2e6c8-595">這些條款是不必要的，與 Windows 的鼓勵語氣相反。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-595">These terms are unnecessary and contrary to the encouraging tone of Windows.</span></span> <span data-ttu-id="2e6c8-596">[正確使用](vis-std-icons.md)時，錯誤圖示可充分傳達發生問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-596">When [used correctly](vis-std-icons.md), the error icon sufficiently communicates that there is a problem.</span></span>

<span data-ttu-id="2e6c8-597">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-597">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-598">訊息的螢幕擷取畫面：嚴重失敗！</span><span class="sxs-lookup"><span data-stu-id="2e6c8-598">screen shot of message: catastrophic failure!</span></span> ](images/mess-error-image48.png)

<span data-ttu-id="2e6c8-599">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-599">**Correct:**</span></span>

![<span data-ttu-id="2e6c8-600">訊息的螢幕擷取畫面：備份必須一次關閉</span><span class="sxs-lookup"><span data-stu-id="2e6c8-600">screen shot of message: backup must close at once</span></span> ](images/mess-error-image49.png)

<span data-ttu-id="2e6c8-601">在不正確的範例中，不需要「嚴重」和「失敗」詞彙。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-601">In the incorrect example, the terms "catastrophic" and "failure" are unnecessary.</span></span>

- <span data-ttu-id="2e6c8-602">請勿使用意思暗示指責使用者或隱含使用者錯誤的片語。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-602">Don't use phrasing that blames the user or implies user error.</span></span> <span data-ttu-id="2e6c8-603">避免在片語中使用您和。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-603">Avoid using you and your in the phrasing.</span></span> <span data-ttu-id="2e6c8-604">當使用中的語音通常是慣用的時候，請在使用者為主旨時使用被動聲音，如果使用的是使用中的聲音，可能會覺得應該過度錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-604">While the active voice is generally preferred, use the passive voice when the user is the subject and might feel blamed for the error if the active voice were used.</span></span>

<span data-ttu-id="2e6c8-605">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-605">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-606">您輸入不正確登入之訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2e6c8-606">screen shot of message you entered incorrect logon</span></span> ](images/mess-error-image50.png)

<span data-ttu-id="2e6c8-607">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-607">**Correct:**</span></span>

![<span data-ttu-id="2e6c8-608">訊息的螢幕擷取畫面：密碼不正確</span><span class="sxs-lookup"><span data-stu-id="2e6c8-608">screen shot of message: incorrect password</span></span> ](images/mess-error-image51.png)

<span data-ttu-id="2e6c8-609">不正確的範例會使用主動式聲音意思暗示指責使用者。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-609">The incorrect example blames the user by using the active voice.</span></span>

- <span data-ttu-id="2e6c8-610">**是特定的。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-610">**Be specific.**</span></span> <span data-ttu-id="2e6c8-611">避免模糊的用語，例如語法錯誤和不合法的作業。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-611">Avoid vague wording, such as syntax error and illegal operation.</span></span> <span data-ttu-id="2e6c8-612">提供相關物件的特定名稱、位置和值。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-612">Provide specific names, locations, and values of the objects involved.</span></span>

<span data-ttu-id="2e6c8-613">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-613">**Incorrect:**</span></span>

<span data-ttu-id="2e6c8-614">找不到檔案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-614">File not found.</span></span>

<span data-ttu-id="2e6c8-615">磁碟已滿。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-615">Disk is full.</span></span>

<span data-ttu-id="2e6c8-616">值超出範圍。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-616">Value out of range.</span></span>

<span data-ttu-id="2e6c8-617">字元無效。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-617">Character is invalid.</span></span>

<span data-ttu-id="2e6c8-618">裝置無法使用。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-618">Device not available.</span></span>

<span data-ttu-id="2e6c8-619">使用特定的名稱、位置和值，可以更輕鬆地解決這些問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-619">These problems would be much easier to solve with specific names, locations, and values.</span></span>

- <span data-ttu-id="2e6c8-620">**請勿在嘗試特定的情況下，提供可能不太可能的問題、原因或解決方案。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-620">**Don't give possibly unlikely problems, causes, or solutions in an attempt to be specific.**</span></span> <span data-ttu-id="2e6c8-621">請勿提供問題、原因或解決方案，除非它可能是正確的。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-621">Don't provide a problem, cause, or solution unless it is likely to be right.</span></span> <span data-ttu-id="2e6c8-622">例如，比起可能不正確的錯誤，最好是說發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-622">For example, it is better to say An unknown error occurred than something that is likely to be inaccurate.</span></span>
- <span data-ttu-id="2e6c8-623">除了在要求使用者進行不方便的 (例如等待) 或軟體是面臨這種情況時，**請避免出現「請」這個字**。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-623">**Avoid the word "please,"** except in situations in which the user is asked to do something inconvenient (such as waiting) or the software is to blame for the situation.</span></span>

<span data-ttu-id="2e6c8-624">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-624">**Correct:**</span></span>

<span data-ttu-id="2e6c8-625">請稍候，Windows 正在將檔案複製到您的電腦。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-625">Please wait while Windows copies the files to your computer.</span></span>

- <span data-ttu-id="2e6c8-626">請 **只在錯誤訊息中使用 "抱歉" 這個字，這會導致使用者的嚴重問題** (例如，資料遺失或無法使用電腦) 。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-626">**Use the word "sorry" only in error messages that result in serious problems for the user** (for example, data loss or inability to use the computer).</span></span> <span data-ttu-id="2e6c8-627">如果程式正常運作期間發生此問題，請不要深感抱歉 (例如，如果使用者需要等候) 的網路連接。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-627">Don't apologize if the issue occurred during the normal functioning of the program (for example, if the user needs to wait for a network connection to be found).</span></span>

<span data-ttu-id="2e6c8-628">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-628">**Correct:**</span></span>

<span data-ttu-id="2e6c8-629">很抱歉，Fabrikam 備份偵測到無法復原的問題，並已關閉以保護您電腦上的檔案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-629">We're sorry, but Fabrikam Backup detected an unrecoverable problem and was shut down to protect files on your computer.</span></span>

- <span data-ttu-id="2e6c8-630">**請使用其簡短名稱來參考產品。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-630">**Refer to products using their short names.**</span></span> <span data-ttu-id="2e6c8-631">請勿使用完整的產品名稱或商標符號。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-631">Don't use full product names or trademark symbols.</span></span> <span data-ttu-id="2e6c8-632">請勿包含公司名稱，除非使用者將公司名稱與產品建立關聯。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-632">Don't include the company name unless users associate the company name with the product.</span></span> <span data-ttu-id="2e6c8-633">請勿包含程式版本號碼。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-633">Don't include program version numbers.</span></span>

<span data-ttu-id="2e6c8-634">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-634">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-635">顯示 Microsoft Office Outlook 無法開啟此專案] 訊息的螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-635">Screenshot that shows a Microsoft Office Outlook 'Can't open this item' message.</span></span> ](images/mess-error-image52.png)

<span data-ttu-id="2e6c8-636">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-636">**Correct:**</span></span>

![<span data-ttu-id="2e6c8-637">訊息的螢幕擷取畫面：無法開啟此專案</span><span class="sxs-lookup"><span data-stu-id="2e6c8-637">screen shot of message: can't open this item</span></span> ](images/mess-error-image53.png)

<span data-ttu-id="2e6c8-638">在不正確的範例中，會使用完整的產品名稱和商標符號。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-638">In the incorrect example, full product names and trademark symbols are used.</span></span>

- <span data-ttu-id="2e6c8-639">**請在物件名稱前後加上雙引號。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-639">**Use double quotation marks around object names.**</span></span> <span data-ttu-id="2e6c8-640">這樣做可讓您更輕鬆地剖析文字，並避免可能的尷尬語句。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-640">Doing so makes the text easier to parse and avoids potentially embarrassing statements.</span></span>
  - <span data-ttu-id="2e6c8-641">**例外狀況：** 完整檔案路徑、Url 和功能變數名稱不需要用雙引號括住。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-641">**Exception:** Fully qualified file paths, URLs, and domain names don't need to be in double quotation marks.</span></span>

<span data-ttu-id="2e6c8-642">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-642">**Correct:**</span></span>

![<span data-ttu-id="2e6c8-643">訊息的螢幕擷取畫面：「我的房子」無法使用</span><span class="sxs-lookup"><span data-stu-id="2e6c8-643">screen shot of message: 'my house' is unavailable</span></span> ](images/mess-error-image54.png)

<span data-ttu-id="2e6c8-644">在此範例中，如果物件名稱不在引號中，則錯誤訊息會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-644">In this example, the error message would be confusing if the object name weren't in quotation marks.</span></span>

- <span data-ttu-id="2e6c8-645">**避免使用物件名稱來起始句子。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-645">**Avoid starting sentences with object names.**</span></span> <span data-ttu-id="2e6c8-646">這麼做通常很難剖析。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-646">Doing so is often difficult to parse.</span></span>
- <span data-ttu-id="2e6c8-647">**請勿使用加上雙引號或全大寫字母的單字。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-647">**Don't use exclamation marks or words with all capital letters.**</span></span> <span data-ttu-id="2e6c8-648">驚嘆號和大寫字母讓您覺得 shouting 是使用者。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-648">Exclamation marks and capital letters make it feel like you are shouting at the user.</span></span>

<span data-ttu-id="2e6c8-649">如需詳細的指導方針和範例，請參閱 [樣式和語氣](text-style-tone.md)。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-649">For more guidelines and examples, see [Style and Tone](text-style-tone.md).</span></span>

<span data-ttu-id="2e6c8-650">**標題**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-650">**Titles**</span></span>

- <span data-ttu-id="2e6c8-651">**使用標題來識別產生錯誤的命令或功能。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-651">**Use the title to identify the command or feature from which the error originated.**</span></span> <span data-ttu-id="2e6c8-652">例外狀況：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-652">Exceptions:</span></span>
  - <span data-ttu-id="2e6c8-653">如果有許多不同的命令顯示錯誤，請考慮改為使用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-653">If an error is displayed by many different commands, consider using the program name instead.</span></span>
  - <span data-ttu-id="2e6c8-654">如果該標題是多餘的，或與主要指示混淆，請改用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-654">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>
- <span data-ttu-id="2e6c8-655">**請勿使用標題來說明或摘要** 說明主要指令用途的問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-655">**Don't use the title to explain or summarize the problem** that's the purpose of the main instruction.</span></span>

<span data-ttu-id="2e6c8-656">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-656">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-657">顯示「無法重新命名新資料夾」訊息的螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-657">Screenshot that shows a 'Can't rename new folder' message.</span></span> ](images/mess-error-image55.png)

<span data-ttu-id="2e6c8-658">在此範例中，標題未正確地用來說明問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-658">In this example, the title is being incorrectly used to explain the problem.</span></span>

- <span data-ttu-id="2e6c8-659">使用標題樣式的大小寫，但不含結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-659">Use title-style capitalization, without ending punctuation.</span></span>

<span data-ttu-id="2e6c8-660">**主要指示**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-660">**Main instructions**</span></span>

- <span data-ttu-id="2e6c8-661">**您可以使用主要指示，以純文字明確的語言描述問題。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-661">**Use the main instruction to describe the problem in clear, plain, specific language.**</span></span>
- <span data-ttu-id="2e6c8-662">**請務必只使用單一的完整句子。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-662">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="2e6c8-663">削減主要指示以瞭解基本資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-663">Pare the main instruction down to the essential information.</span></span> <span data-ttu-id="2e6c8-664">如果您的程式或使用者是您的程式，則可以將主體保持隱含。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-664">You can leave the subject implicit if it is your program or the user.</span></span> <span data-ttu-id="2e6c8-665">如果您可以很簡潔，請包含問題的原因。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-665">Include the reason for the problem if you can do so concisely.</span></span> <span data-ttu-id="2e6c8-666">如果您必須進一步說明，請使用補充指示。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-666">If you must explain anything more, use a supplemental instruction.</span></span>

<span data-ttu-id="2e6c8-667">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-667">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-668">訊息的螢幕擷取畫面：無法安裝升級</span><span class="sxs-lookup"><span data-stu-id="2e6c8-668">screen shot of message: upgrade can't be installed</span></span> ](images/mess-error-image56.png)

<span data-ttu-id="2e6c8-669">在此範例中，完整的錯誤訊息會放在主要指令中，因此難以閱讀。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-669">In this example, the entire error message is put in the main instruction, making it hard to read.</span></span>

- <span data-ttu-id="2e6c8-670">**如果有相關的物件，請指定其名稱，並指定其名稱。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-670">**Be specific if there are objects involved, give their names.**</span></span>
- <span data-ttu-id="2e6c8-671">**避免將完整檔案路徑和 Url 放在主要指令中。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-671">**Avoid putting full file paths and URLs in the main instruction.**</span></span> <span data-ttu-id="2e6c8-672">相反地，請使用簡短名稱 (例如檔案名) 並將完整名稱 (例如在補充指令中) 的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-672">Rather, use a short name (such as the file name) and put the full name (such as the file path) in the supplemental instruction.</span></span> <span data-ttu-id="2e6c8-673">但是，如果錯誤訊息不需要補充指令，您可以在主要指令中放入單一完整檔案路徑或 URL。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-673">However, you can put a single full file path or URL in the main instruction if the error message doesn't otherwise need a supplemental instruction.</span></span>

![<span data-ttu-id="2e6c8-674">message：無法刪除 fabrikam 檔案的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="2e6c8-674">screen shot of message: can't delete fabrikam file</span></span> ](images/mess-error-image57.png)

<span data-ttu-id="2e6c8-675">在此範例中，只會在主要指令中有檔案名。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-675">In this example, only the file name is in the main instruction.</span></span> <span data-ttu-id="2e6c8-676">完整路徑是在補充指令中。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-676">The full path is in the supplemental instruction.</span></span>

- <span data-ttu-id="2e6c8-677">**如果內容很明顯，請不要提供完整的檔案路徑和 URL。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-677">**Don't give the full file path and URL at all if it's obvious from the context.**</span></span>

![<span data-ttu-id="2e6c8-678">訊息的螢幕擷取畫面：無法重新命名新資料夾</span><span class="sxs-lookup"><span data-stu-id="2e6c8-678">screen shot of message: can't rename new folder</span></span> ](images/mess-error-image58.png)

<span data-ttu-id="2e6c8-679">在此範例中，使用者正在從 Windows 檔案總管重新命名檔案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-679">In this example, the user is renaming a file from Windows Explorer.</span></span> <span data-ttu-id="2e6c8-680">在此情況下，不需要完整的檔案路徑，因為它從內容中很明顯。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-680">In this case, the full file path isn't needed because it's obvious from the context.</span></span>

- <span data-ttu-id="2e6c8-681">盡可能使用目前的時態。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-681">Use present tense whenever possible.</span></span>
- <span data-ttu-id="2e6c8-682">使用句型大寫。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-682">Use sentence-style capitalization.</span></span>
- <span data-ttu-id="2e6c8-683">如果指令是語句，則不包含最後句號。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-683">Don't include final periods if the instruction is a statement.</span></span> <span data-ttu-id="2e6c8-684">如果指令是問題，請包含最後一個問號。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-684">If the instruction is a question, include a final question mark.</span></span>

<span data-ttu-id="2e6c8-685">**主要指令範本**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-685">**Main instruction templates**</span></span>

<span data-ttu-id="2e6c8-686">雖然片語沒有嚴格的規則，但請盡可能嘗試使用下列主要指令範本：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-686">While there are no strict rules for phrasing, try using the following main instruction templates whenever possible:</span></span>

- <span data-ttu-id="2e6c8-687">[選用主體名稱] 無法 [執行動作]</span><span class="sxs-lookup"><span data-stu-id="2e6c8-687">[optional subject name] can't [perform action]</span></span>
- <span data-ttu-id="2e6c8-688">[選用主體名稱] 無法 [執行動作]，因為 [原因]</span><span class="sxs-lookup"><span data-stu-id="2e6c8-688">[optional subject name] can't [perform action] because [reason]</span></span>
- <span data-ttu-id="2e6c8-689">[選用主體名稱] 無法 [執行動作] 至 "[物件名稱]"</span><span class="sxs-lookup"><span data-stu-id="2e6c8-689">[optional subject name] can't [perform action] to "[object name]"</span></span>
- <span data-ttu-id="2e6c8-690">[選用主體名稱] 無法 [執行動作] 至 "[物件名稱]"，因為 [原因]</span><span class="sxs-lookup"><span data-stu-id="2e6c8-690">[optional subject name] can't [perform action] to "[object name]" because [reason]</span></span>
- <span data-ttu-id="2e6c8-691">沒有足夠的 [資源] 可 [執行動作]</span><span class="sxs-lookup"><span data-stu-id="2e6c8-691">There is not enough [resource] to [perform action]</span></span>
- <span data-ttu-id="2e6c8-692">[主體名稱] 沒有 [用途] 所需的 [物件名稱]</span><span class="sxs-lookup"><span data-stu-id="2e6c8-692">[Subject name] doesn't have a [object name] required for [purpose]</span></span>
- <span data-ttu-id="2e6c8-693">[裝置或設定] 已關閉，因此 [不希望的結果]</span><span class="sxs-lookup"><span data-stu-id="2e6c8-693">[Device or setting] is turned off so that [undesired results]</span></span>
- <span data-ttu-id="2e6c8-694">[裝置或設定] 未 [ \| \| 已啟用可找到的開啟 \| ]</span><span class="sxs-lookup"><span data-stu-id="2e6c8-694">[Device or setting] isn't [available \| found \| turned on \| enabled]</span></span>
- <span data-ttu-id="2e6c8-695">"[物件名稱]" 目前無法使用</span><span class="sxs-lookup"><span data-stu-id="2e6c8-695">"[object name]" is currently unavailable</span></span>
- <span data-ttu-id="2e6c8-696">使用者名稱或密碼不正確</span><span class="sxs-lookup"><span data-stu-id="2e6c8-696">The user name or password is incorrect</span></span>
- <span data-ttu-id="2e6c8-697">您無權存取 "[object name]"</span><span class="sxs-lookup"><span data-stu-id="2e6c8-697">You don't have permission to access "[object name]"</span></span>
- <span data-ttu-id="2e6c8-698">您沒有 [執行動作] 的許可權</span><span class="sxs-lookup"><span data-stu-id="2e6c8-698">You don't have privilege to [perform action]</span></span>
- <span data-ttu-id="2e6c8-699">[程式名稱] 遇到嚴重的問題，必須立即關閉</span><span class="sxs-lookup"><span data-stu-id="2e6c8-699">[program name] has experienced a serious problem and must close immediately</span></span>

<span data-ttu-id="2e6c8-700">當然，請視需要變更主要指令的語法是否正確，並遵守主要指示指導方針。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-700">Of course, make changes as needed for the main instruction to be grammatically correct and comply with the main instruction guidelines.</span></span>

<span data-ttu-id="2e6c8-701">**補充指示**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-701">**Supplemental instructions**</span></span>

- <span data-ttu-id="2e6c8-702">使用補充指示：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-702">Use the supplemental instruction to:</span></span>
  - <span data-ttu-id="2e6c8-703">提供有關問題的其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-703">Give additional details about the problem.</span></span>
  - <span data-ttu-id="2e6c8-704">說明問題的原因。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-704">Explain the cause of the problem.</span></span>
  - <span data-ttu-id="2e6c8-705">列出使用者可採取的步驟來修正問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-705">List steps the user can take to fix the problem.</span></span>
  - <span data-ttu-id="2e6c8-706">提供量值以防止問題重複發生。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-706">Provide measures to prevent the problem from reoccurring.</span></span>
- <span data-ttu-id="2e6c8-707">**可能的話，請提出實用且有用的解決方案，讓使用者可以修正問題。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-707">**Whenever possible, propose a practical, helpful solution so users can fix the problem.**</span></span> <span data-ttu-id="2e6c8-708">不過，請確定建議的解決方案可能會解決此問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-708">However, make sure the proposed solution is likely to solve the problem.</span></span> <span data-ttu-id="2e6c8-709">不要藉由建議可能但未必的解決方案，來浪費使用者的時間。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-709">Don't waste users' time by suggesting possible, but improbable, solutions.</span></span>

<span data-ttu-id="2e6c8-710">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-710">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-711">訊息的螢幕擷取畫面：記憶體不足</span><span class="sxs-lookup"><span data-stu-id="2e6c8-711">screen shot of message: out of memory</span></span> ](images/mess-error-image59.png)

<span data-ttu-id="2e6c8-712">在此範例中，雖然問題及其建議的解決方案是可行的，但這不太可能發生。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-712">In this example, while the problem and its recommended solution are possible, they are very unlikely.</span></span>

- <span data-ttu-id="2e6c8-713">**如果問題是使用者輸入的不正確值，請使用補充指示來說明正確的值。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-713">**If the problem is an incorrect value that the user entered, use the supplemental instruction to explain the correct values.**</span></span> <span data-ttu-id="2e6c8-714">使用者不需要從另一個來源判斷這份資訊。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-714">Users shouldn't have to determine this information from another source.</span></span>
- <span data-ttu-id="2e6c8-715">**如果可以從問題陳述中完整，請不要提供解決方案。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-715">**Don't provide a solution if it can be trivially deduced from the problem statement.**</span></span>

![<span data-ttu-id="2e6c8-716">訊息的螢幕擷取畫面：時間值不正確</span><span class="sxs-lookup"><span data-stu-id="2e6c8-716">screen shot of message: incorrect time value</span></span> ](images/mess-error-image33.png)

<span data-ttu-id="2e6c8-717">在此範例中，不需要任何補充指示;您可以從問題陳述中完整的解決方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-717">In this example, no supplemental instruction is necessary; the solution can be trivially deduced from the problem statement.</span></span>

- <span data-ttu-id="2e6c8-718">**如果解決方案有多個步驟，請依應完成的順序來顯示這些步驟。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-718">**If the solution has multiple steps, present the steps in the order in which they should be completed.**</span></span> <span data-ttu-id="2e6c8-719">不過，請避免使用多步驟解決方案，因為使用者難以記住兩個或三個簡單的步驟。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-719">However, avoid multi-step solutions because users have difficulty remembering more than two or three simple steps.</span></span> <span data-ttu-id="2e6c8-720">如果需要更多步驟，請參閱適當的說明主題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-720">If more steps are required, refer to the appropriate Help topic.</span></span>
- <span data-ttu-id="2e6c8-721">**讓補充指示保持簡潔。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-721">**Keep supplemental instructions concise.**</span></span> <span data-ttu-id="2e6c8-722">僅提供使用者需要知道的事項。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-722">Provide only what users need to know.</span></span> <span data-ttu-id="2e6c8-723">省略不必要的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-723">Omit unnecessary details.</span></span> <span data-ttu-id="2e6c8-724">最多可為適中長度的三個句子。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-724">Aim for a maximum of three sentences of moderate length.</span></span>
- <span data-ttu-id="2e6c8-725">**為了避免使用者執行指令時發生錯誤，請將結果放在動作之前。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-725">**To avoid mistakes while users perform instructions, put the results before the action.**</span></span>

<span data-ttu-id="2e6c8-726">**正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-726">**Correct:**</span></span>

<span data-ttu-id="2e6c8-727">若要重新開機 Windows，請按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-727">To restart Windows, click OK.</span></span>

<span data-ttu-id="2e6c8-728">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-728">**Incorrect:**</span></span>

<span data-ttu-id="2e6c8-729">按一下 [確定] 以重新開機 Windows。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-729">Click OK to restart Windows.</span></span>

<span data-ttu-id="2e6c8-730">在不正確的範例中，使用者可能會意外按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-730">In the incorrect example, users are more likely to click OK by accident.</span></span>

- <span data-ttu-id="2e6c8-731">**不建議您聯繫系統管理員，除非這麼做是問題的最可能解決方案。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-731">**Don't recommend contacting an administrator unless doing so is among the most likely solutions to the problem.**</span></span> <span data-ttu-id="2e6c8-732">針對真正只能由系統管理員解決的問題，保留這類解決方案。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-732">Reserve such solutions for problems that really can only be solved by an administrator.</span></span>

<span data-ttu-id="2e6c8-733">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-733">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-734">訊息的螢幕擷取畫面：伺服器無法使用</span><span class="sxs-lookup"><span data-stu-id="2e6c8-734">screen shot of message: server unavailable</span></span> ](images/mess-error-image60.png)

<span data-ttu-id="2e6c8-735">在此範例中，最可能的問題是使用者的網路連線，因此不值得您聯絡系統管理員。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-735">In this example, most likely the problem is with the user's network connection, so it's not worth contacting an administrator.</span></span>

- <span data-ttu-id="2e6c8-736">**不建議您聯繫技術支援部門。**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-736">**Don't recommend contacting technical support.**</span></span> <span data-ttu-id="2e6c8-737">若要解決問題，您可以選擇使用技術支援來解決問題，而不需要透過錯誤訊息來升級。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-737">The option to contact technical support to solve a problem is always available, and doesn't need to be promoted through error messages.</span></span> <span data-ttu-id="2e6c8-738">相反地，請將焦點放在撰寫有用的錯誤訊息，讓使用者可以解決問題，而不需要聯繫技術支援。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-738">Instead, focus on writing helpful error messages so that users can solve problems without contacting technical support.</span></span>

<span data-ttu-id="2e6c8-739">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-739">**Incorrect:**</span></span>

![<span data-ttu-id="2e6c8-740">顯示「無法開啟此專案」訊息的螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-740">Screenshot that shows a 'Can't open this item' message.</span></span> ](images/mess-error-image61.png)

<span data-ttu-id="2e6c8-741">在此範例中，錯誤訊息會不正確地建議與技術支援聯絡。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-741">In this example, the error message incorrectly recommends contacting technical support.</span></span>

- <span data-ttu-id="2e6c8-742">使用完整句子、句子樣式的大小寫和結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-742">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

<span data-ttu-id="2e6c8-743">**認可按鈕**</span><span class="sxs-lookup"><span data-stu-id="2e6c8-743">**Commit buttons**</span></span>

- <span data-ttu-id="2e6c8-744">如果錯誤訊息提供可解決問題的命令按鈕或命令連結，請在 [對話方塊](win-dialog-box.md)中依照各自的指導方針。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-744">If the error message provides command buttons or command links that solve the problem, follow their respective guidelines in [Dialog Boxes](win-dialog-box.md).</span></span>
- <span data-ttu-id="2e6c8-745">如果程式因錯誤而必須終止，請提供 [結束程式] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-745">If the program must terminate as a result of the error, provide an Exit program button.</span></span> <span data-ttu-id="2e6c8-746">為了避免混淆，請不要針對此用途使用 Close。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-746">To avoid confusion, don't use Close for this purpose.</span></span>
- <span data-ttu-id="2e6c8-747">否則，請提供 [關閉] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-747">Otherwise, provide a Close button.</span></span> <span data-ttu-id="2e6c8-748">請勿將 [確定] 用於錯誤訊息，因為這種措辭表示問題沒問題。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-748">Don't use OK for error messages, because this wording implies that problems are OK.</span></span>
  - <span data-ttu-id="2e6c8-749">**例外狀況：** 如果您的錯誤報表機制具有固定標籤 (與 MessageBox API 相同，請使用 [確定]。 ) </span><span class="sxs-lookup"><span data-stu-id="2e6c8-749">**Exception:** Use OK if your error reporting mechanism has fixed labels (as with the MessageBox API.)</span></span>

## <a name="documentation"></a><span data-ttu-id="2e6c8-750">文件</span><span class="sxs-lookup"><span data-stu-id="2e6c8-750">Documentation</span></span>

<span data-ttu-id="2e6c8-751">參考錯誤時：</span><span class="sxs-lookup"><span data-stu-id="2e6c8-751">When referring to errors:</span></span>

- <span data-ttu-id="2e6c8-752">請依主要指示來參考錯誤。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-752">Refer to errors by their main instruction.</span></span> <span data-ttu-id="2e6c8-753">如果主要指令很長或更詳細，請將其摘要。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-753">If the main instruction is long or detailed, summarize it.</span></span>
- <span data-ttu-id="2e6c8-754">如有必要，您可以將 [錯誤訊息] 對話方塊參考為訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-754">If necessary, you may refer to an error message dialog box as a message.</span></span> <span data-ttu-id="2e6c8-755">請參閱僅在程式設計和其他技術檔中的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-755">Refer to as an error message only in programming and other technical documentation.</span></span>
- <span data-ttu-id="2e6c8-756">可能的話，請使用粗體格式化文字。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-756">When possible, format the text using bold.</span></span> <span data-ttu-id="2e6c8-757">否則，請只在必要時才將文字放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-757">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="2e6c8-758">**範例：** 如果您收到「 **磁片磁碟機中沒有光碟片** 」訊息，請在磁片磁碟機中插入新的光碟片，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="2e6c8-758">**Example:** If you receive a **There is no CD disc in the drive** message, insert a new CD disc in the drive and try again.</span></span>