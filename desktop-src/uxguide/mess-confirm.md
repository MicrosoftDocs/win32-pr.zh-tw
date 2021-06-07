---
title: 確認
description: 確認是一個強制回應對話方塊，會詢問使用者是否要繼續執行動作。
ms.assetid: 086302cd-c8a1-479c-87be-580945e5d3e6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 321cab040423df3a6dc0069d568d66c85e3aa8cc
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524522"
---
# <a name="confirmations"></a><span data-ttu-id="05fb3-103">確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-103">Confirmations</span></span>

> [!NOTE]
> <span data-ttu-id="05fb3-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="05fb3-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="05fb3-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="05fb3-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="05fb3-106">確認是一個強制回應對話方塊，會詢問使用者是否要繼續執行動作。</span><span class="sxs-lookup"><span data-stu-id="05fb3-106">A confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span>

![顯示 [您要儲存變更嗎？] 的 [記事本] 的螢幕擷取畫面](images/mess-confirm-image1.png)

<span data-ttu-id="05fb3-109">一般確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-109">A typical confirmation.</span></span>

<span data-ttu-id="05fb3-110">確認具有這些基本特性：</span><span class="sxs-lookup"><span data-stu-id="05fb3-110">Confirmations have these essential characteristics:</span></span>

-   <span data-ttu-id="05fb3-111">它們會顯示為使用者所起始之動作的直接結果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-111">They are displayed as the direct result of an action initiated by the user.</span></span>
-   <span data-ttu-id="05fb3-112">他們會確認使用者是否想要繼續執行動作。</span><span class="sxs-lookup"><span data-stu-id="05fb3-112">They verify that the user wants to proceed with the action.</span></span>
-   <span data-ttu-id="05fb3-113">它們包含一個簡單的問題，以及兩個或多個回應。</span><span class="sxs-lookup"><span data-stu-id="05fb3-113">They consist of a simple question and two or more responses.</span></span>

<span data-ttu-id="05fb3-114">當動作需要使用者進行相關且不同的選擇，但稍後無法進行時，確認最有用。</span><span class="sxs-lookup"><span data-stu-id="05fb3-114">Confirmations are most useful when the action requires the user to make a relevant and distinct choice that can't be made later.</span></span> <span data-ttu-id="05fb3-115">這項選擇通常牽涉到使用者不明顯的風險元素，但不一定要確認風險。</span><span class="sxs-lookup"><span data-stu-id="05fb3-115">That choice often involves some element of risk that isn't obvious to the user, but risk isn't essential to confirmations.</span></span> <span data-ttu-id="05fb3-116">需要這些元素，以證明回應強制回應對話方塊的中斷。</span><span class="sxs-lookup"><span data-stu-id="05fb3-116">These elements are necessary to justify the interruption of responding to a modal dialog.</span></span>

<span data-ttu-id="05fb3-117">相反地， [警告訊息](mess-warn.md) 會出現可能會在未來發生問題的狀況。</span><span class="sxs-lookup"><span data-stu-id="05fb3-117">By contrast, [warning messages](mess-warn.md) present a condition that might cause a problem in the future.</span></span> <span data-ttu-id="05fb3-118">其基本特性是它們牽涉到風險：</span><span class="sxs-lookup"><span data-stu-id="05fb3-118">Their fundamental characteristic is that they involve risk:</span></span>

-   <span data-ttu-id="05fb3-119">它們牽涉到可能遺失下列一或多項：</span><span class="sxs-lookup"><span data-stu-id="05fb3-119">They involve potential loss of one or more of the following:</span></span>
    -   <span data-ttu-id="05fb3-120">有價值的資產，例如資料遺失或財務損失。</span><span class="sxs-lookup"><span data-stu-id="05fb3-120">A valuable asset, such as data loss or financial loss.</span></span>
    -   <span data-ttu-id="05fb3-121">系統存取或完整性。</span><span class="sxs-lookup"><span data-stu-id="05fb3-121">System access or integrity.</span></span>
    -   <span data-ttu-id="05fb3-122">隱私權或對機密資訊的控制。</span><span class="sxs-lookup"><span data-stu-id="05fb3-122">Privacy or control over confidential information.</span></span>
    -   <span data-ttu-id="05fb3-123">使用者的時間 (大量的時間，例如30秒或更多的) 。</span><span class="sxs-lookup"><span data-stu-id="05fb3-123">User's time (a significant amount, such as 30 seconds or more).</span></span>
-   <span data-ttu-id="05fb3-124">它們有非預期或非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-124">They have unexpected or unintended consequences.</span></span>
-   <span data-ttu-id="05fb3-125">因為錯誤無法輕易地修正，甚至可能無法復原，因此現在它們需要正確的處理。</span><span class="sxs-lookup"><span data-stu-id="05fb3-125">They require correct handling now because mistakes can't be easily fixed, and may even be irreversible.</span></span>

<span data-ttu-id="05fb3-126">如果確認牽涉到風險，也可以將其視為警告。</span><span class="sxs-lookup"><span data-stu-id="05fb3-126">If a confirmation involves risk, it can be considered a warning as well.</span></span> <span data-ttu-id="05fb3-127">因此，也適用警告訊息指導方針。</span><span class="sxs-lookup"><span data-stu-id="05fb3-127">Consequently, the warning message guidelines also apply.</span></span>

<span data-ttu-id="05fb3-128">**注意：** 與 [對話方塊](win-dialog-box.md)、[錯誤訊息](mess-error.md) [、配置和](vis-layout.md)[警告訊息](mess-warn.md)相關的指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="05fb3-128">**Note:** Guidelines related to [dialog boxes](win-dialog-box.md), [error messages](mess-error.md), [layout](vis-layout.md), and [warning messages](mess-warn.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="05fb3-129">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="05fb3-129">Is this the right user interface?</span></span>

<span data-ttu-id="05fb3-130">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="05fb3-130">To decide, consider these questions:</span></span>

-   <span data-ttu-id="05fb3-131">**使用者是否有問題繼續進行有兩個或多個回應的動作？**</span><span class="sxs-lookup"><span data-stu-id="05fb3-131">**Is the user being asked a question to proceed with an action that has two or more responses?**</span></span> <span data-ttu-id="05fb3-132">如果沒有，則不會確認訊息。</span><span class="sxs-lookup"><span data-stu-id="05fb3-132">If not, the message isn't a confirmation.</span></span>
-   <span data-ttu-id="05fb3-133">**UI 是否呈現發生的錯誤或問題？**</span><span class="sxs-lookup"><span data-stu-id="05fb3-133">**Is the UI presenting an error or problem that has occurred?**</span></span> <span data-ttu-id="05fb3-134">若是如此，請改用 [錯誤訊息](mess-error.md) 。</span><span class="sxs-lookup"><span data-stu-id="05fb3-134">If so, use an [error message](mess-error.md) instead.</span></span>
-   <span data-ttu-id="05fb3-135">**繼續進行動作需要使用者選擇沒有適當的預設值？**</span><span class="sxs-lookup"><span data-stu-id="05fb3-135">**Does proceeding with the action require the user to make a choice that doesn't have a suitable default?**</span></span> <span data-ttu-id="05fb3-136">如果是的話，則可能會有適當的確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-136">If so, a confirmation may be appropriate.</span></span>
-   <span data-ttu-id="05fb3-137">**是否有替代的設計可避免確認的需求？**</span><span class="sxs-lookup"><span data-stu-id="05fb3-137">**Is there an alternative design that eliminates the need for the confirmation?**</span></span> <span data-ttu-id="05fb3-138">確認的需要有時表示設計瑕疵。</span><span class="sxs-lookup"><span data-stu-id="05fb3-138">The need for a confirmation sometimes indicates a design flaw.</span></span> <span data-ttu-id="05fb3-139">通常有更好的設計替代方案不需要確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-139">Often there is a better design alternative that doesn't need a confirmation.</span></span>
-   <span data-ttu-id="05fb3-140">**使用者是否要執行具風險的動作？**</span><span class="sxs-lookup"><span data-stu-id="05fb3-140">**Is the user about to perform a risky action?**</span></span> <span data-ttu-id="05fb3-141">如果是這樣，如果動作有重大的後果或無法輕易復原，則會有適當的確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-141">If so, a confirmation is appropriate if the action has significant consequences or cannot be easily undone.</span></span>
-   <span data-ttu-id="05fb3-142">**使用者是否要放棄工作？**</span><span class="sxs-lookup"><span data-stu-id="05fb3-142">**Is the user about to abandon a task?**</span></span> <span data-ttu-id="05fb3-143">若是如此，請不要確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-143">If so, don't confirm.</span></span> <span data-ttu-id="05fb3-144">假設使用者瞭解未完成工作的後果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-144">Assume users understand the consequences of not completing a task.</span></span>
-   <span data-ttu-id="05fb3-145">**動作是否會造成使用者可能不知道的後果？**</span><span class="sxs-lookup"><span data-stu-id="05fb3-145">**Does the action have consequences that users might not be aware of?**</span></span> <span data-ttu-id="05fb3-146">如果是的話，則可能會有適當的確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-146">If so, a confirmation may be appropriate.</span></span>
-   <span data-ttu-id="05fb3-147">**由於目前的內容，使用者是否有可能執行錯誤的動作？**</span><span class="sxs-lookup"><span data-stu-id="05fb3-147">**Given the current context, are users likely to be performing an action in error?**</span></span> <span data-ttu-id="05fb3-148">如果是的話，則可能會有適當的確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-148">If so, a confirmation may be appropriate.</span></span>
-   <span data-ttu-id="05fb3-149">**使用者是否經常執行動作？**</span><span class="sxs-lookup"><span data-stu-id="05fb3-149">**Do users perform the action frequently?**</span></span> <span data-ttu-id="05fb3-150">如果是，請考慮使用替代的設計。</span><span class="sxs-lookup"><span data-stu-id="05fb3-150">If so, consider an alternative design.</span></span> <span data-ttu-id="05fb3-151">頻繁的確認是討厭的，且有很少的價值，因為使用者會學習回應而不需要思考。</span><span class="sxs-lookup"><span data-stu-id="05fb3-151">Frequent confirmations are annoying and have little value because users learn to respond without thinking.</span></span>
-   <span data-ttu-id="05fb3-152">**動作是否有安全性含意？**</span><span class="sxs-lookup"><span data-stu-id="05fb3-152">**Does the action have security implications?**</span></span> <span data-ttu-id="05fb3-153">若是如此，即使先前的測試另有指示，也可能需要確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-153">If so, a confirmation may be required even if the previous tests indicate otherwise.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="05fb3-154">設計概念</span><span class="sxs-lookup"><span data-stu-id="05fb3-154">Design concepts</span></span>

### <a name="unnecessary-confirmations-are-annoying"></a><span data-ttu-id="05fb3-155">不必要的確認很討厭</span><span class="sxs-lookup"><span data-stu-id="05fb3-155">Unnecessary confirmations are annoying</span></span>

<span data-ttu-id="05fb3-156">第一次建立的 Windows 確認看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="05fb3-156">The first Windows confirmation ever created undoubtedly looked like this:</span></span>

![<span data-ttu-id="05fb3-157">[確定嗎？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-157">screen shot of 'are you sure?'</span></span> <span data-ttu-id="05fb3-158">確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-158">confirmation</span></span> ](images/mess-confirm-image2.png)

<span data-ttu-id="05fb3-159">原始討厭的確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-159">The original annoying confirmation.</span></span>

<span data-ttu-id="05fb3-160">這是非常糟糕的起點。</span><span class="sxs-lookup"><span data-stu-id="05fb3-160">This was a very bad start.</span></span> <span data-ttu-id="05fb3-161">如果您想要讓使用者討厭您的程式，只要在整個小量確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-161">If you want users to hate your program, just sprinkle confirmations like this throughout.</span></span> <span data-ttu-id="05fb3-162">若要瞭解原因，請考慮使用者的觀點。</span><span class="sxs-lookup"><span data-stu-id="05fb3-162">To understand why, consider the user's point of view.</span></span> <span data-ttu-id="05fb3-163">使用者只是要求由確認定義來執行動作，如此一來，使用者就會想要繼續進行。</span><span class="sxs-lookup"><span data-stu-id="05fb3-163">The user just asked to perform an action by the definition of a confirmation so unless something was somehow clicked or pressed accidentally, of course the user wants to proceed.</span></span>

<span data-ttu-id="05fb3-164">不只是不必要的確認，也不是保護使用者免于犯錯的效用。</span><span class="sxs-lookup"><span data-stu-id="05fb3-164">Not only are unnecessary confirmations annoying, but they aren't effective in protecting the user from mistakes.</span></span> <span data-ttu-id="05fb3-165">當程式有不必要的確認時，使用者很快就會發現，而其自然回應是盡可能快速地關閉（通常不會讀取）。</span><span class="sxs-lookup"><span data-stu-id="05fb3-165">Users quickly discover when a program has unnecessary confirmations and their natural response is to dismiss them as quickly as possible, often without reading.</span></span> <span data-ttu-id="05fb3-166">因此，這類確認只需要為這些工作新增額外的步驟。</span><span class="sxs-lookup"><span data-stu-id="05fb3-166">Consequently, such confirmations do little more than add an extra step to these tasks.</span></span>

<span data-ttu-id="05fb3-167">請不要使用確認，因為使用者可能會犯錯誤。</span><span class="sxs-lookup"><span data-stu-id="05fb3-167">Don't use confirmations just because there is the possibility of users making a mistake.</span></span> <span data-ttu-id="05fb3-168">**相反地，確認是在用來確認具有顯著或非預期結果的動作時最有效。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-168">**Rather, confirmations are most effective when used to confirm actions that have significant or unintended consequences.**</span></span> <span data-ttu-id="05fb3-169">良好確認永遠不會陳述明顯的;他們應該傳達使用者需要注意的事項，以找出不能繼續的好理由。</span><span class="sxs-lookup"><span data-stu-id="05fb3-169">Good confirmations never state the obvious; they should communicate something users need to be aware of a good reason not to continue.</span></span> <span data-ttu-id="05fb3-170">而且只有在動作真正需要時，才會使用它們，例如只有在有變更值得儲存的時候，才要求使用者儲存變更。</span><span class="sxs-lookup"><span data-stu-id="05fb3-170">And they are used only when they are really needed by an action, such as asking users to save changes only when there are changes worth saving.</span></span> <span data-ttu-id="05fb3-171">這麼做只會要求使用者在真正的保證時，才需要注意。</span><span class="sxs-lookup"><span data-stu-id="05fb3-171">Doing so demands the user's attention only when it is truly warranted.</span></span>

<span data-ttu-id="05fb3-172">針對其他類型的確認，通常會有比強制使用者回答問題更好的設計替代方案。</span><span class="sxs-lookup"><span data-stu-id="05fb3-172">For other types of confirmations, there is often a better design alternative than forcing users to answer a question.</span></span>

### <a name="consider-the-design-alternatives"></a><span data-ttu-id="05fb3-173">考慮設計替代方案</span><span class="sxs-lookup"><span data-stu-id="05fb3-173">Consider the design alternatives</span></span>

<span data-ttu-id="05fb3-174">以下是一些不再需要進行例行確認的設計替代方案：</span><span class="sxs-lookup"><span data-stu-id="05fb3-174">Here are some design alternatives that eliminate the need for routine confirmations:</span></span>

-   <span data-ttu-id="05fb3-175">**防止錯誤。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-175">**Prevent errors.**</span></span> <span data-ttu-id="05fb3-176">設計工作，讓嚴重錯誤難以意外地發生。</span><span class="sxs-lookup"><span data-stu-id="05fb3-176">Design tasks so that significant mistakes are difficult to do accidentally.</span></span> <span data-ttu-id="05fb3-177">例如，實際將破壞性命令與其他命令分開，並且需要多個動作才能完成。</span><span class="sxs-lookup"><span data-stu-id="05fb3-177">For example, physically separate destructive commands from other commands, and require multiple actions to complete.</span></span>
-   <span data-ttu-id="05fb3-178">**提供復原。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-178">**Provide undo.**</span></span> <span data-ttu-id="05fb3-179">提供還原動作的能力。</span><span class="sxs-lookup"><span data-stu-id="05fb3-179">Provide the ability to revert actions.</span></span> <span data-ttu-id="05fb3-180">例如，在 Microsoft Windows 中刪除檔案時，通常不需要確認，因為已刪除的檔案可以從資源回收筒復原。</span><span class="sxs-lookup"><span data-stu-id="05fb3-180">For example, deleting a file in Microsoft Windows usually doesn't require a confirmation because deleted files can be recovered from the Recycle Bin.</span></span> <span data-ttu-id="05fb3-181">請注意，如果動作很容易執行，則讓使用者重做動作可能就已足夠。</span><span class="sxs-lookup"><span data-stu-id="05fb3-181">Note that if an action is very easy to perform, just having users redo the action may be sufficient.</span></span>
-   <span data-ttu-id="05fb3-182">**提供意見反應。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-182">**Provide feedback.**</span></span> <span data-ttu-id="05fb3-183">明顯地產生不想要的結果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-183">Make undesirable outcomes obvious.</span></span> <span data-ttu-id="05fb3-184">如果使用者在發生錯誤時不知道，單獨提供復原並不足夠。</span><span class="sxs-lookup"><span data-stu-id="05fb3-184">Providing undo alone isn't sufficient if users don't realize when they make a mistake.</span></span> <span data-ttu-id="05fb3-185">例如，直接操作 (的效果（例如拖放作業) ）應該一律很明顯。</span><span class="sxs-lookup"><span data-stu-id="05fb3-185">For example, the effect of direct manipulation (such as a drag-and-drop operation) should always be obvious.</span></span>
-   <span data-ttu-id="05fb3-186">**假設可能的結果，但可讓您輕鬆地進行變更。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-186">**Assume the probable outcome, but make it easy to change.**</span></span> <span data-ttu-id="05fb3-187">如果您不確定使用者需要什麼，但是有很可能、安全且安全的選擇，請採用該選擇，讓它清楚瞭解發生什麼事，並使用操作功能表輕鬆地進行變更。</span><span class="sxs-lookup"><span data-stu-id="05fb3-187">If you aren't sure what users want but there is a likely, safe, and secure choice, assume that choice, make it clear what happened, and make it easy to change using a context menu.</span></span> <span data-ttu-id="05fb3-188">例如，Microsoft Word 假設使用者想要正確拼寫文字。</span><span class="sxs-lookup"><span data-stu-id="05fb3-188">For example, Microsoft Word assumes that users want to spell words correctly.</span></span> <span data-ttu-id="05fb3-189">如果它辨識拼錯的字，而且它知道可能正確的拼寫，Word 會自動進行更正，但允許使用者還原。</span><span class="sxs-lookup"><span data-stu-id="05fb3-189">If it recognizes a misspelled word and it knows the likely correct spelling, Word automatically makes the correction but allows users to revert.</span></span>
-   <span data-ttu-id="05fb3-190">**完全消除選擇。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-190">**Eliminate the choice completely.**</span></span> <span data-ttu-id="05fb3-191">如果選擇不重要，使用者就不會在意。</span><span class="sxs-lookup"><span data-stu-id="05fb3-191">If the choice isn't important, users just won't care.</span></span> <span data-ttu-id="05fb3-192">更妥善地 [簡化](/previous-versions//dn742474(v=vs.85)) 您的程式並排除選擇。</span><span class="sxs-lookup"><span data-stu-id="05fb3-192">Better to [simplify](/previous-versions//dn742474(v=vs.85)) your program and eliminate the choice.</span></span>

### <a name="make-confirmations-require-thought"></a><span data-ttu-id="05fb3-193">確認需要考慮</span><span class="sxs-lookup"><span data-stu-id="05fb3-193">Make confirmations require thought</span></span>

<span data-ttu-id="05fb3-194">為了確認有價值，使用者必須瞭解不會繼續的原因。</span><span class="sxs-lookup"><span data-stu-id="05fb3-194">For a confirmation to have value, users need to understand the reason not to proceed.</span></span> <span data-ttu-id="05fb3-195">有時候原因很明顯，因為當使用者以尚未儲存的變更來關閉檔時：</span><span class="sxs-lookup"><span data-stu-id="05fb3-195">Sometimes the reason is obvious, as when users are closing a document with changes that haven't been saved:</span></span>

![顯示「您要儲存變更嗎？」繪圖的螢幕擷取畫面](images/mess-confirm-image3.png)

<span data-ttu-id="05fb3-198">在此範例中，確認的原因很明顯。</span><span class="sxs-lookup"><span data-stu-id="05fb3-198">In this example, the reason for the confirmation is obvious.</span></span>

<span data-ttu-id="05fb3-199">在其他情況下，原因可能不明顯。</span><span class="sxs-lookup"><span data-stu-id="05fb3-199">In other situations, the reason might not be so obvious.</span></span>

<span data-ttu-id="05fb3-200">選擇對話方塊的 [認可按鈕標籤] 時， [一般的指導方針](win-dialog-box.md) 是選擇對主要指令有特定回應的標籤。</span><span class="sxs-lookup"><span data-stu-id="05fb3-200">When choosing commit button labels for dialog boxes, the [general guidelines](win-dialog-box.md) is to choose labels that are specific responses to the main instruction.</span></span> <span data-ttu-id="05fb3-201">這會導致有效的決策，因為使用者必須讀取最少量的文字才能繼續進行。</span><span class="sxs-lookup"><span data-stu-id="05fb3-201">This leads to efficient decision making because users have to read a minimum amount of text to proceed.</span></span> <span data-ttu-id="05fb3-202">不過，這種效率目標可這些確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-202">However, this efficiency goal can be counterproductive for confirmations.</span></span> <span data-ttu-id="05fb3-203">請考慮此範例：</span><span class="sxs-lookup"><span data-stu-id="05fb3-203">Consider this example:</span></span>

<span data-ttu-id="05fb3-204">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-204">**Incorrect:**</span></span>

![<span data-ttu-id="05fb3-205">使用 [卸載] 按鈕確認的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-205">screen shot of confirmation with uninstall button</span></span> ](images/mess-confirm-image4.png)

<span data-ttu-id="05fb3-206">在此範例中，需要考慮正確的回應。</span><span class="sxs-lookup"><span data-stu-id="05fb3-206">In this example, the correct response requires thought.</span></span>

<span data-ttu-id="05fb3-207">如果您在使用者提供卸載命令之後立即提出這項確認，使用者的回應可能會是「當然我要卸載！」</span><span class="sxs-lookup"><span data-stu-id="05fb3-207">If you present this confirmation immediately after the user gave the Uninstall command, the user's response is likely to be "Of course I want to uninstall!"</span></span> <span data-ttu-id="05fb3-208">使用者會按一下 [卸載]，而不需要再做一次考慮。</span><span class="sxs-lookup"><span data-stu-id="05fb3-208">The user will click Uninstall without giving it a second thought.</span></span>

<span data-ttu-id="05fb3-209">針對確認，我們不希望使用者做出惟恐、情緒決策。</span><span class="sxs-lookup"><span data-stu-id="05fb3-209">For confirmations, we don't want users making hasty, emotional decisions.</span></span> <span data-ttu-id="05fb3-210">為了鼓勵使用者思考其回應，我們需要提供小規模的決策加速。</span><span class="sxs-lookup"><span data-stu-id="05fb3-210">To encourage users to think about their response, we need to provide a small decision-making speed bump.</span></span> <span data-ttu-id="05fb3-211">在可行的情況下，最好是藉由仔細地措辭認可按鈕來完成這項作業。</span><span class="sxs-lookup"><span data-stu-id="05fb3-211">When practical, it's usually better to do this by carefully phrasing commit buttons.</span></span> <span data-ttu-id="05fb3-212">例如，我們可以使用其他語言來指出不會繼續的原因。</span><span class="sxs-lookup"><span data-stu-id="05fb3-212">For example, we can use additional language to indicate that there is a reason not to continue.</span></span>

<span data-ttu-id="05fb3-213">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-213">**Better:**</span></span>

![<span data-ttu-id="05fb3-214">[仍要卸載] 按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-214">screen shot of 'uninstall anyway' button</span></span> ](images/mess-confirm-image5.png)

<span data-ttu-id="05fb3-215">在此範例中，「仍」會新增至認可按鈕標籤，以指出確認提供的原因不會繼續。</span><span class="sxs-lookup"><span data-stu-id="05fb3-215">In this example, "anyway" is added to the commit button label to indicate that the confirmation gives a reason not to continue.</span></span>

<span data-ttu-id="05fb3-216">如果該方法不實用，我們可以使用 [是]/[否] 認可按鈕。</span><span class="sxs-lookup"><span data-stu-id="05fb3-216">If that approach isn't practical, we can use Yes/No commit buttons.</span></span>

<span data-ttu-id="05fb3-217">**還有更好的：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-217">**Also better:**</span></span>

![<span data-ttu-id="05fb3-218">確認具有 [是]/[否] 按鈕的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-218">screen shot of confirmation with yes/no buttons</span></span> ](images/mess-confirm-image6.png)

<span data-ttu-id="05fb3-219">在此範例中，使用 [是]/[否] 認可按鈕會強制使用者至少讀取主要指令。</span><span class="sxs-lookup"><span data-stu-id="05fb3-219">In this example, using Yes/No commit buttons forces users to at least read the main instruction.</span></span>

### <a name="provide-all-the-information"></a><span data-ttu-id="05fb3-220">提供所有資訊</span><span class="sxs-lookup"><span data-stu-id="05fb3-220">Provide all the information</span></span>

<span data-ttu-id="05fb3-221">如果您要詢問問題，您必須為使用者提供足夠的資訊，讓使用者以智慧方式回答該問題。</span><span class="sxs-lookup"><span data-stu-id="05fb3-221">If you are going to ask a question, you must provide sufficient information for users to answer that question intelligently.</span></span> <span data-ttu-id="05fb3-222">請考慮 Windows XP 中的 [確認檔案取代] 對話方塊：</span><span class="sxs-lookup"><span data-stu-id="05fb3-222">Consider the Confirm File Replace dialog from Windows XP:</span></span>

![<span data-ttu-id="05fb3-223">[確認檔案取代] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-223">screen shot of 'confirm file replace' dialog box</span></span> ](images/mess-confirm-image7.png)

<span data-ttu-id="05fb3-224">[Windows XP 確認檔案取代] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="05fb3-224">The Windows XP Confirm File Replace dialog box.</span></span>

<span data-ttu-id="05fb3-225">這種確認是否提供使用者可能需要的所有資訊來回答問題？</span><span class="sxs-lookup"><span data-stu-id="05fb3-225">Does this confirmation provide all the information users might need to answer the question?</span></span> <span data-ttu-id="05fb3-226">在您回答之前，請考慮最常見的使用者案例：</span><span class="sxs-lookup"><span data-stu-id="05fb3-226">Before you answer, consider the most common user scenarios:</span></span>

-   <span data-ttu-id="05fb3-227">複製 (或移動) 另一個檔案，取代現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="05fb3-227">Copy (or move) the other file, replacing the existing one.</span></span>
-   <span data-ttu-id="05fb3-228">保留現有的檔案，而不復制或移動其他檔案。</span><span class="sxs-lookup"><span data-stu-id="05fb3-228">Keep the existing file, without copying or moving the other file.</span></span>
-   <span data-ttu-id="05fb3-229">保留或複製較新的檔案 (主要案例) 。</span><span class="sxs-lookup"><span data-stu-id="05fb3-229">Keep or copy the newer file (top scenario).</span></span>
-   <span data-ttu-id="05fb3-230">您可以保留現有的檔案，或複製另一個檔案，視像是檔案內容和大小的準則而定。</span><span class="sxs-lookup"><span data-stu-id="05fb3-230">Either keep the existing file or copy the other file, depending on criteria such as file contents and size.</span></span>
-   <span data-ttu-id="05fb3-231">保留現有的檔案，並使用不同的名稱複製其他檔案。</span><span class="sxs-lookup"><span data-stu-id="05fb3-231">Keep the existing file and copy the other file using a different name.</span></span>
-   <span data-ttu-id="05fb3-232">如果發生錯誤或非預期的情況，請取消作業。</span><span class="sxs-lookup"><span data-stu-id="05fb3-232">Cancel the operation if something is wrong or unexpected.</span></span>

<span data-ttu-id="05fb3-233">使用者只要按一下 [是] 和 [案例 2]，就可以按一下 [否] 來達成案例1。</span><span class="sxs-lookup"><span data-stu-id="05fb3-233">Users can achieve scenario 1 by clicking Yes and scenario 2 by clicking No.</span></span> <span data-ttu-id="05fb3-234">他們可以藉由比較檔案日期和按一下適當的按鈕來達成案例3，但請注意，判斷較新的檔案需要多少想法，然後判斷出適合最常見案例的適當按鈕。</span><span class="sxs-lookup"><span data-stu-id="05fb3-234">They can achieve scenario 3 by comparing the file dates and clicking the appropriate button, but notice how much thought it takes to determine the newer file and then determine the appropriate button especially for what is likely to be the most common scenario.</span></span>

<span data-ttu-id="05fb3-235">案例4、5和6也很難。</span><span class="sxs-lookup"><span data-stu-id="05fb3-235">Scenarios 4, 5, and 6 are also surprisingly difficult.</span></span> <span data-ttu-id="05fb3-236">檔案大小會舍入，因此，舉例來說，您無法判斷這些檔案的大小是否相同，或即使它們是相同的檔案也是一樣。</span><span class="sxs-lookup"><span data-stu-id="05fb3-236">The file sizes are rounded off, so, for example, it is impossible to determine if these files have the same size or even if they are the same file.</span></span> <span data-ttu-id="05fb3-237">圖示適用于用來開啟檔案的應用程式，因此使用者必須開啟檔案，才能檢查並比較其內容。</span><span class="sxs-lookup"><span data-stu-id="05fb3-237">The icons are for the application used to open the file, so users would have to open the files to inspect and compare their content.</span></span> <span data-ttu-id="05fb3-238">有了檔案內容的縮圖，對回答問題而言會有更大的説明。</span><span class="sxs-lookup"><span data-stu-id="05fb3-238">Having thumbnails of the file content would be far more useful in answering the question.</span></span>

<span data-ttu-id="05fb3-239">從 Windows Vista 的複製檔案確認可提供詳細資訊，並新增保留這兩個檔案的選項，以更好的方式處理這些案例：</span><span class="sxs-lookup"><span data-stu-id="05fb3-239">The Copy File confirmation from Windows Vista does a much better job of handling these scenarios by providing more information and adding the option to keep both files:</span></span>

![<span data-ttu-id="05fb3-240">[複製檔案] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-240">screen shot of 'copy file' dialog box</span></span> ](images/mess-confirm-image8.png)

<span data-ttu-id="05fb3-241">Windows Vista 複製檔案確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-241">The Windows Vista Copy File confirmation.</span></span>

### <a name="provide-specific-useful-information"></a><span data-ttu-id="05fb3-242">提供特定的實用資訊</span><span class="sxs-lookup"><span data-stu-id="05fb3-242">Provide specific, useful information</span></span>

<span data-ttu-id="05fb3-243">如果您要詢問問題，請確定使用者瞭解問題以及替代回應的含意。</span><span class="sxs-lookup"><span data-stu-id="05fb3-243">If you are going to ask a question, ensure that users understand the question and the implications of the alternative responses.</span></span> <span data-ttu-id="05fb3-244">請考慮此 Windows Internet Explorer 安全性確認：</span><span class="sxs-lookup"><span data-stu-id="05fb3-244">Consider this Windows Internet Explorer security confirmation:</span></span>

![<span data-ttu-id="05fb3-245">確認有模糊問題的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-245">screen shot of confirmation with a vague question</span></span> ](images/mess-confirm-image9.png)

<span data-ttu-id="05fb3-246">模糊的安全性確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-246">A vague security confirmation.</span></span>

<span data-ttu-id="05fb3-247">此確認會詢問使用者無法智慧地回答的問題。</span><span class="sxs-lookup"><span data-stu-id="05fb3-247">This confirmation asks a question that users can't possibly answer intelligently.</span></span> <span data-ttu-id="05fb3-248">使用者已要求 Windows Internet Explorer 顯示頁面，而這則訊息會透過文字的用語以隱含的方式提供建議，並藉由反白顯示 [否] 作為預設選項。</span><span class="sxs-lookup"><span data-stu-id="05fb3-248">The user has requested that Windows Internet Explorer display a page, and this message advises against it implicitly through the wording of the text and by highlighting No as the default choice.</span></span>

<span data-ttu-id="05fb3-249">頁面所帶來的特定安全性問題並沒有充分的說明，所以繼續進行的風險並不明顯。</span><span class="sxs-lookup"><span data-stu-id="05fb3-249">The specific security issue that the page poses is not sufficiently explained, so the risk of continuing isn't clear.</span></span> <span data-ttu-id="05fb3-250">確認中的哪些資訊會導致使用者按 [否]？</span><span class="sxs-lookup"><span data-stu-id="05fb3-250">What information in the confirmation would cause the user ever to click No?</span></span> <span data-ttu-id="05fb3-251">由於訊息的 vagueness，確認不太可能會讓使用者無法繼續，但會讓他們感覺不到。</span><span class="sxs-lookup"><span data-stu-id="05fb3-251">Because of the vagueness of the message, the confirmation isn't likely to discourage users from continuing, but will make them feel bad about doing so.</span></span>

<span data-ttu-id="05fb3-252">若要確認這是很有用的功能，必須提供更詳細的資訊，這些資訊可能會導致使用者決定不繼續。</span><span class="sxs-lookup"><span data-stu-id="05fb3-252">For this confirmation to be useful, it must provide more information specific information that might cause the user to decide not to proceed.</span></span> <span data-ttu-id="05fb3-253">一般來說，對於確認中的每個回應，請考慮需要它的案例，並確定有足夠的資訊可供使用者選擇。</span><span class="sxs-lookup"><span data-stu-id="05fb3-253">In general, for each response in a confirmation, consider the scenarios that require it and make sure that there is sufficient information provided for users to want to choose it.</span></span> <span data-ttu-id="05fb3-254">提供選項，而非困境。</span><span class="sxs-lookup"><span data-stu-id="05fb3-254">Provide choices, not dilemmas.</span></span>

### <a name="how-to-determine-if-a-confirmation-is-necessary"></a><span data-ttu-id="05fb3-255">如何判斷是否需要確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-255">How to determine if a confirmation is necessary</span></span>

<span data-ttu-id="05fb3-256">思考案例，以及選擇每個回應的可能性，都建議以系統化的方式判斷是否需要確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-256">Thinking through the scenarios and the likelihood of choosing each response suggests a systematic way to determine if a confirmation is necessary.</span></span> <span data-ttu-id="05fb3-257">如果使用者可能會選取所有回應，則必須確認，而且很有用。</span><span class="sxs-lookup"><span data-stu-id="05fb3-257">If users are likely to select all of the responses, the confirmation is necessary and useful.</span></span> <span data-ttu-id="05fb3-258">但是，如果只有一個回應可能 (表示) 的時間是98%，則確實不需要確認，而且應該移除。</span><span class="sxs-lookup"><span data-stu-id="05fb3-258">However, if only one response is likely (say 98 percent of the time), the confirmation is clearly unnecessary and should be removed.</span></span> <span data-ttu-id="05fb3-259">請注意，與安全性、法律和安全性問題相關的確認是可能發生的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="05fb3-259">Note that confirmations related to security, legal, and safety issues are possible exceptions.</span></span>

![<span data-ttu-id="05fb3-260">[您要變更設定嗎？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-260">screen shot of 'do you want to change settings?'</span></span> ](images/mess-confirm-image10.png)

<span data-ttu-id="05fb3-261">這是必要確認嗎？</span><span class="sxs-lookup"><span data-stu-id="05fb3-261">Is this confirmation necessary?</span></span> <span data-ttu-id="05fb3-262">使用者是否會選取 [否]？</span><span class="sxs-lookup"><span data-stu-id="05fb3-262">Will users ever select No?</span></span> <span data-ttu-id="05fb3-263">有可能是很未必的。</span><span class="sxs-lookup"><span data-stu-id="05fb3-263">It's possible but very improbable.</span></span> <span data-ttu-id="05fb3-264">應移除此確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-264">This confirmation should be removed.</span></span>

<span data-ttu-id="05fb3-265">**如果您只進行三件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-265">**If you do only three things...**</span></span>

1. <span data-ttu-id="05fb3-266">確定確實需要您的確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-266">Make sure your confirmation is really necessary.</span></span> <span data-ttu-id="05fb3-267">應該有合理且明確的原因不會繼續進行，有時使用者可能不會這麼做。</span><span class="sxs-lookup"><span data-stu-id="05fb3-267">There should be a legitimate and clear reason not to proceed, and a chance that sometimes users won't.</span></span>

2. <span data-ttu-id="05fb3-268">如果確認的原因無法立即察覺，請選擇鼓勵使用者思考其回應的 [認可] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="05fb3-268">If the reason for the confirmation isn't immediately obvious, choose commit buttons that encourage users to think about their response.</span></span> <span data-ttu-id="05fb3-269">一般來說，這是藉由將確認視為「是」或「否」的問題，並提供完全易懂或「是/否」答案來完成。</span><span class="sxs-lookup"><span data-stu-id="05fb3-269">Typically, this is done by phrasing the confirmation as a yes or no question and providing completely self-explanatory or Yes/No answers.</span></span>

3. <span data-ttu-id="05fb3-270">請考慮所有案例，並提供以智慧方式回答問題所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="05fb3-270">Consider all the scenarios and provide the information required to answer the question intelligently.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="05fb3-271">使用模式</span><span class="sxs-lookup"><span data-stu-id="05fb3-271">Usage patterns</span></span>

<span data-ttu-id="05fb3-272">確認有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="05fb3-272">Confirmations have several usage patterns:</span></span>



|   <span data-ttu-id="05fb3-273">使用狀況</span><span class="sxs-lookup"><span data-stu-id="05fb3-273">Usage</span></span>                                                                                                                                                                    |    <span data-ttu-id="05fb3-274">範例</span><span class="sxs-lookup"><span data-stu-id="05fb3-274">Example</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05fb3-275">**例行確認**</span><span class="sxs-lookup"><span data-stu-id="05fb3-275">**Routine confirmations**</span></span><br/> <span data-ttu-id="05fb3-276">確認使用者想要繼續進行例行、低風險的動作。</span><span class="sxs-lookup"><span data-stu-id="05fb3-276">confirm that the user wants to proceed with a routine, low risk action.</span></span> <br/>                                              | <span data-ttu-id="05fb3-277">這些確認通常會片語「您確定 ...」</span><span class="sxs-lookup"><span data-stu-id="05fb3-277">These confirmations are usually phrased "are you sure...?"</span></span> <span data-ttu-id="05fb3-278">而且通常不會再顯示這個訊息核取方塊，將干擾降到最低。</span><span class="sxs-lookup"><span data-stu-id="05fb3-278">and often have a don't show this message again check box to minimize their annoyance.</span></span> <br/> <span data-ttu-id="05fb3-279">![[將資料夾移至回收站？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-279">![screen shot of 'move folder to recycle bin?'</span></span> ](images/mess-confirm-image11.png)<br/> <span data-ttu-id="05fb3-280">![[不要再顯示訊息] 的螢幕擷取畫面 ](images/mess-confirm-image12.png)</span><span class="sxs-lookup"><span data-stu-id="05fb3-280">![screen shot of 'don't show message again' ](images/mess-confirm-image12.png)</span></span><br/> <span data-ttu-id="05fb3-281">例行確認的範例。</span><span class="sxs-lookup"><span data-stu-id="05fb3-281">Examples of routine confirmations.</span></span><br/> <span data-ttu-id="05fb3-282">**注意：** 這種模式通常是不必要的，因此應予以避免。</span><span class="sxs-lookup"><span data-stu-id="05fb3-282">**Note:** This pattern is usually unnecessary and should be avoided.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="05fb3-283">**具風險的動作確認**</span><span class="sxs-lookup"><span data-stu-id="05fb3-283">**Risky action confirmations**</span></span><br/> <span data-ttu-id="05fb3-284">確認使用者想要繼續進行有一些風險且無法輕易復原的動作。</span><span class="sxs-lookup"><span data-stu-id="05fb3-284">confirm that the user wants to proceed with an action that has some risk and can't be easily undone.</span></span> <br/>            | <span data-ttu-id="05fb3-285">因為這些確認有風險，所以這些確認通常會出現警告圖示。</span><span class="sxs-lookup"><span data-stu-id="05fb3-285">Because they have risk, these confirmations usually have a warning icon.</span></span> <br/> ![顯示磁片區格式化確認範例的螢幕擷取畫面。](images/mess-confirm-image13.png)<br/> ![顯示永久刪除確認範例的螢幕擷取畫面。](images/mess-confirm-image14.png)<br/> <span data-ttu-id="05fb3-288">具風險動作確認的範例。</span><span class="sxs-lookup"><span data-stu-id="05fb3-288">Examples of risky action confirmations.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="05fb3-289">**非預期的結果確認**</span><span class="sxs-lookup"><span data-stu-id="05fb3-289">**Unintended consequence confirmations**</span></span><br/> <span data-ttu-id="05fb3-290">確認使用者想要繼續執行具有非預期或非預期結果的動作。</span><span class="sxs-lookup"><span data-stu-id="05fb3-290">confirm that the user wants to proceed with an action that has unexpected or unintended consequences.</span></span> <br/> | <span data-ttu-id="05fb3-291">除了提出問題之外，這些確認還指出了非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-291">In addition to asking a question, these confirmations point out the unintended consequences.</span></span> <span data-ttu-id="05fb3-292">因為它們有非預期的結果，所以這些確認通常會有警告圖示。</span><span class="sxs-lookup"><span data-stu-id="05fb3-292">because they have unintended consequences, these confirmations usually have a warning icon.</span></span> <br/> <span data-ttu-id="05fb3-293">![[關閉所有索引標籤？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-293">![screen shot of 'close all tabs?'</span></span> <span data-ttu-id="05fb3-294">確認 ](images/mess-confirm-image15.png)</span><span class="sxs-lookup"><span data-stu-id="05fb3-294">confirmation ](images/mess-confirm-image15.png)</span></span><br/> <span data-ttu-id="05fb3-295">![[取消安裝？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-295">![screen shot of 'cancel installation?'</span></span> <span data-ttu-id="05fb3-296">確認 ](images/mess-confirm-image16.png)</span><span class="sxs-lookup"><span data-stu-id="05fb3-296">confirmation ](images/mess-confirm-image16.png)</span></span><br/> <span data-ttu-id="05fb3-297">非預期結果確認的範例。</span><span class="sxs-lookup"><span data-stu-id="05fb3-297">examples of unintended consequence confirmations.</span></span><br/> <span data-ttu-id="05fb3-298">不過，此模式要求結果必須是真正的非預期的。</span><span class="sxs-lookup"><span data-stu-id="05fb3-298">however, this pattern requires that the consequences are truly unintended.</span></span> <br/> <span data-ttu-id="05fb3-299">**錯誤：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-299">**incorrect:**</span></span><br/> <span data-ttu-id="05fb3-300">![[關閉金鑰記錄器？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-300">![screen shot of 'turn off key logger?'</span></span> <span data-ttu-id="05fb3-301">確認 ](images/mess-confirm-image17.png)</span><span class="sxs-lookup"><span data-stu-id="05fb3-301">confirmation ](images/mess-confirm-image17.png)</span></span><br/> <span data-ttu-id="05fb3-302">結果是在這裡，因此這是例行的確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-302">The consequences are intended here, so this is a routine confirmation.</span></span><br/> |
| <span data-ttu-id="05fb3-303">**釐清內容**</span><span class="sxs-lookup"><span data-stu-id="05fb3-303">**Clarifications**</span></span><br/> <span data-ttu-id="05fb3-304">明確說明使用者要如何繼續進行可能不明確或非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-304">clarify how the user wants to proceed with an action that has potentially ambiguous or unexpected consequences.</span></span> <br/>             | <span data-ttu-id="05fb3-305">拖放作業可能會導致說明是否可以誤解作業的效果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-305">Drag-and-drop operations can result in clarifications if the effect of the operation can be misinterpreted.</span></span> <br/> <span data-ttu-id="05fb3-306">![[只變更這次出現嗎？] 的螢幕擷取畫面](images/mess-confirm-image18.png)</span><span class="sxs-lookup"><span data-stu-id="05fb3-306">![screen shot of 'change only this occurrence?'](images/mess-confirm-image18.png)</span></span><br/> <span data-ttu-id="05fb3-307">![[在結束時一律儲存] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-307">![screen shot of 'always save on exit?'</span></span> <span data-ttu-id="05fb3-308">確認 ](images/mess-confirm-image19.png)</span><span class="sxs-lookup"><span data-stu-id="05fb3-308">confirmation ](images/mess-confirm-image19.png)</span></span><br/> <span data-ttu-id="05fb3-309">說明的範例。</span><span class="sxs-lookup"><span data-stu-id="05fb3-309">Examples of clarifications.</span></span><br/> <span data-ttu-id="05fb3-310">**注意：** 應避免此模式，因為最好是設計動作，而不會有不明確的結果，並假設最可能的結果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-310">**Note:** This pattern should be avoided because it is better to design actions without ambiguous consequences and assume the most likely desired result.</span></span> <br/>                                                                                                                                                                                                                                     |
| <span data-ttu-id="05fb3-311">**安全性確認**</span><span class="sxs-lookup"><span data-stu-id="05fb3-311">**Security confirmations**</span></span><br/> <span data-ttu-id="05fb3-312">確認使用者想要繼續執行具有安全性後果的動作。</span><span class="sxs-lookup"><span data-stu-id="05fb3-312">confirm that the user wants to proceed with an action with security consequences.</span></span> <br/>                                   | ![<span data-ttu-id="05fb3-313">[您要執行此軟體嗎？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-313">screen shot of 'do you want to run this software?'</span></span> ](images/mess-confirm-image20.png)<br/> ![<span data-ttu-id="05fb3-314">[記住密碼？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-314">screen shot of 'remember password?'</span></span> <span data-ttu-id="05fb3-315">確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-315">confirmation</span></span> ](images/mess-confirm-image21.png)<br/> <span data-ttu-id="05fb3-316">安全性確認的範例。</span><span class="sxs-lookup"><span data-stu-id="05fb3-316">Examples of security confirmations.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="05fb3-317">**Ulterior 動機確認**</span><span class="sxs-lookup"><span data-stu-id="05fb3-317">**Ulterior motive confirmations**</span></span><br/> <span data-ttu-id="05fb3-318">提供動作的相關資訊，但將它呈現為確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-318">provide information about an action, but present it as a confirmation.</span></span> <br/>                                       | <span data-ttu-id="05fb3-319">雖然這些對話方塊會以確認的形式呈現，但其真實目標是使用者教育或功能公告。</span><span class="sxs-lookup"><span data-stu-id="05fb3-319">While these dialog boxes are presented as confirmations, their real goal is user education or advertisement of features.</span></span> <br/> <span data-ttu-id="05fb3-320">![希望工作列上有此工具列的螢幕擷取畫面嗎？</span><span class="sxs-lookup"><span data-stu-id="05fb3-320">![screen shot of want this toolbar on your taskbar?</span></span> ](images/mess-confirm-image22.png)<br/> <span data-ttu-id="05fb3-321">Ulterior 動機確認的範例。</span><span class="sxs-lookup"><span data-stu-id="05fb3-321">An example of an ulterior motive confirmation.</span></span><br/> <span data-ttu-id="05fb3-322">**注意：** 不建議使用此模式，因為通常會有更好的直接替代方法。</span><span class="sxs-lookup"><span data-stu-id="05fb3-322">**Note:** This pattern is not recommended because there is usually a better, more direct alternative.</span></span> <span data-ttu-id="05fb3-323">例如， [動畫](vis-animations.md) 是顯示原因和效果之間關聯性的較佳方式。</span><span class="sxs-lookup"><span data-stu-id="05fb3-323">For example, [animations](vis-animations.md) are a better way to show the relationship between cause and effect.</span></span> <br/>                                                                                                                                                                                                                                     |



 

## <a name="guidelines"></a><span data-ttu-id="05fb3-324">指導方針</span><span class="sxs-lookup"><span data-stu-id="05fb3-324">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="05fb3-325">一般</span><span class="sxs-lookup"><span data-stu-id="05fb3-325">General</span></span>

-   <span data-ttu-id="05fb3-326">**只有在有重大變更時，才使用 [儲存變更] 確認。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-326">**Use "Save changes" confirmations only when there are significant changes.**</span></span> <span data-ttu-id="05fb3-327">請勿確認使用者未直接進行的變更，例如自動格式化檔。</span><span class="sxs-lookup"><span data-stu-id="05fb3-327">Don't confirm changes that weren't directly made by the user, such as automatic document reformatting.</span></span>

<span data-ttu-id="05fb3-328">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-328">**Incorrect:**</span></span>

![顯示 Microsoft Office Outlook [您要儲存變更嗎？] 的螢幕擷取畫面](images/mess-confirm-image23.png)

<span data-ttu-id="05fb3-331">當使用者未變更空白電子郵件或檔時，此範例會不正確。</span><span class="sxs-lookup"><span data-stu-id="05fb3-331">This example is incorrect when used for an empty e-mail or document that wasn't changed by the user.</span></span>

### <a name="icons"></a><span data-ttu-id="05fb3-332">圖示</span><span class="sxs-lookup"><span data-stu-id="05fb3-332">Icons</span></span>

-   <span data-ttu-id="05fb3-333">確認不使用標題列圖示。</span><span class="sxs-lookup"><span data-stu-id="05fb3-333">Confirmations don't use title bar icons.</span></span>
-   <span data-ttu-id="05fb3-334">**確認的內容區域圖示是根據其設計模式：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-334">**The content area icon for a confirmation is based on its design pattern:**</span></span>



    | <span data-ttu-id="05fb3-335">模式</span><span class="sxs-lookup"><span data-stu-id="05fb3-335">Pattern</span></span>                                                | <span data-ttu-id="05fb3-336">圖示</span><span class="sxs-lookup"><span data-stu-id="05fb3-336">Icon</span></span>                                                                                                                                             |
    |--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="05fb3-337">例行確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-337">Routine confirmations</span></span> <br/>                | <span data-ttu-id="05fb3-338">無圖示。</span><span class="sxs-lookup"><span data-stu-id="05fb3-338">No icon.</span></span> <br/>                                                                                                                         |
    | <span data-ttu-id="05fb3-339">具風險的動作確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-339">Risky action confirmations</span></span> <br/>           | <span data-ttu-id="05fb3-340">警告圖示。</span><span class="sxs-lookup"><span data-stu-id="05fb3-340">Warning icon.</span></span> <br/>                                                                                                                    |
    | <span data-ttu-id="05fb3-341">非預期的結果確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-341">Unintended consequence confirmations</span></span> <br/> | <span data-ttu-id="05fb3-342">如果有風險，請使用警告圖示，如果有的話，則為功能圖示;否則，就不會有圖示。</span><span class="sxs-lookup"><span data-stu-id="05fb3-342">Use a warning icon if there is risk, the feature icon if available; otherwise, no icon.</span></span> <br/>                                          |
    | <span data-ttu-id="05fb3-343">釐清內容</span><span class="sxs-lookup"><span data-stu-id="05fb3-343">Clarifications</span></span> <br/>                       | <span data-ttu-id="05fb3-344">如果確認牽涉到檔，請使用檔的縮圖;否則，請使用功能圖示（如果有的話），或不使用圖示。</span><span class="sxs-lookup"><span data-stu-id="05fb3-344">If the confirmation involves a document, use the document's thumbnail; otherwise, use the feature icon if available, or no icon.</span></span> <br/> |
    | <span data-ttu-id="05fb3-345">安全性確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-345">Security confirmations</span></span> <br/>               | <span data-ttu-id="05fb3-346">警告圖示。</span><span class="sxs-lookup"><span data-stu-id="05fb3-346">Warning icon.</span></span> <br/>                                                                                                                    |
    | <span data-ttu-id="05fb3-347">Ulterior 動機確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-347">Ulterior motive confirmations</span></span> <br/>        | <span data-ttu-id="05fb3-348">無圖示。</span><span class="sxs-lookup"><span data-stu-id="05fb3-348">No icon.</span></span> <br/>                                                                                                                         |



 

-   <span data-ttu-id="05fb3-349">**請勿使用警告圖示進行例行問題。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-349">**Don't use warning icons for routine questions.**</span></span> <span data-ttu-id="05fb3-350">這麼做是 Windows 的鼓勵 [語氣](text-style-tone.md) 的計數器，讓您的程式感覺像是危險活動。</span><span class="sxs-lookup"><span data-stu-id="05fb3-350">Doing so is counter to the encouraging [tone of Windows](text-style-tone.md) and makes using your program feel like a hazardous activity.</span></span> <span data-ttu-id="05fb3-351">假設使用者瞭解在工作完成之前取消工作的後果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-351">Assume users understand the consequences of canceling a task before it is finished.</span></span>

<span data-ttu-id="05fb3-352">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-352">**Incorrect:**</span></span>

![<span data-ttu-id="05fb3-353">[您要結束本教學課程嗎？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-353">screen shot of 'do you want to end the tutorial?'</span></span> ](images/mess-confirm-image24.png)

<span data-ttu-id="05fb3-354">在此範例中，會使用警告圖示來詢問例行問題。</span><span class="sxs-lookup"><span data-stu-id="05fb3-354">In this example, a warning icon is used to ask a routine question.</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="05fb3-355">認可按鈕</span><span class="sxs-lookup"><span data-stu-id="05fb3-355">Commit buttons</span></span>

-   <span data-ttu-id="05fb3-356">**如果確認的原因很明顯，或可讓您一目了然，請使用主要指示的特定回應。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-356">**Use specific responses to the main instruction if the reason for the confirmation is obvious or can be made self explanatory.**</span></span>

![<span data-ttu-id="05fb3-357">[您要儲存變更嗎？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-357">screen shot of 'do you want to save changes?'</span></span> ](images/mess-confirm-image25.png)

<span data-ttu-id="05fb3-358">在此範例中，確認的原因很明顯，請儲存，並不要儲存工作正常。</span><span class="sxs-lookup"><span data-stu-id="05fb3-358">In this example, the reason for the confirmation is obvious, so Save and Don't save work well.</span></span>

-   <span data-ttu-id="05fb3-359">**否則，請使用 [是]，而且沒有任何按鈕可進行確認回應。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-359">**Otherwise, use Yes and No buttons for confirmation responses.**</span></span> <span data-ttu-id="05fb3-360">這麼做可讓使用者在回應之前，提供確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-360">Doing so makes users give the confirmation some thought before responding.</span></span> <span data-ttu-id="05fb3-361">請勿使用 [確定] 和 [取消] 進行確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-361">Never use OK and Cancel for confirmations.</span></span>

<span data-ttu-id="05fb3-362">**正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-362">**Correct:**</span></span>

![<span data-ttu-id="05fb3-363">[想要卸載支援檔案嗎？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-363">screen shot of 'want to uninstall support files?'</span></span> ](images/mess-confirm-image26.png)

<span data-ttu-id="05fb3-364">在此範例中，使用 [是]/[否] 認可按鈕會強制使用者至少讀取主要指令。</span><span class="sxs-lookup"><span data-stu-id="05fb3-364">In this example, using Yes/No commit buttons forces users to at least read the main instruction.</span></span>

<span data-ttu-id="05fb3-365">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-365">**Incorrect:**</span></span>

![<span data-ttu-id="05fb3-366">[取消您的保留？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-366">screen shot of 'cancel your reservation?'</span></span> ](images/mess-confirm-image27.png)

<span data-ttu-id="05fb3-367">在此範例中，使用 [確定]/[取消] 會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="05fb3-367">In this example, using OK/Cancel is confusing.</span></span>

-   <span data-ttu-id="05fb3-368">**若要關閉程式或重新開機 Windows，請使用主要指示的特定回應。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-368">**To close a program or restart Windows, use specific responses to the main instruction.**</span></span> <span data-ttu-id="05fb3-369">若要避免任何誤解，請勿使用 Close 或 Yes/No 來達成此目的。</span><span class="sxs-lookup"><span data-stu-id="05fb3-369">To prevent any misunderstanding, don't use Close or Yes/No for this purpose.</span></span>

<span data-ttu-id="05fb3-370">**正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-370">**Correct:**</span></span>

![[立即重新開機 windows] 按鈕的螢幕擷取畫面](images/mess-confirm-image28.png)

<span data-ttu-id="05fb3-372">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-372">**Incorrect:**</span></span>

![[是] 按鈕的螢幕擷取畫面](images/mess-confirm-image29.png)

<span data-ttu-id="05fb3-374">在不正確的範例中，[是] 會用來重新開機 Windows。</span><span class="sxs-lookup"><span data-stu-id="05fb3-374">In the incorrect example, Yes is used to restart Windows.</span></span>

### <a name="command-links"></a><span data-ttu-id="05fb3-375">命令連結</span><span class="sxs-lookup"><span data-stu-id="05fb3-375">Command links</span></span>

-   <span data-ttu-id="05fb3-376">**如需詳細的說明模式，請考慮使用命令連結，讓替代方案更清楚。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-376">**For the clarifications pattern, consider using command links to make the alternatives clear.**</span></span>

<span data-ttu-id="05fb3-377">**可以接受：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-377">**Acceptable:**</span></span>

![<span data-ttu-id="05fb3-378">[變更一或多個出現專案？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-378">screen shot of 'change one or all occurrences?'</span></span> ](images/mess-confirm-image30.png)

<span data-ttu-id="05fb3-379">**較佳：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-379">**Better:**</span></span>

![<span data-ttu-id="05fb3-380">使用命令連結的相同問題的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-380">screen shot of same question using command links</span></span> ](images/mess-confirm-image31.png)

<span data-ttu-id="05fb3-381">在更好的範例中，命令連結會讓替代專案變得清楚。</span><span class="sxs-lookup"><span data-stu-id="05fb3-381">In the better example, command links make the alternatives clear.</span></span>

-   <span data-ttu-id="05fb3-382">**先顯示最常使用的命令連結。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-382">**Present the most commonly used command links first.**</span></span> <span data-ttu-id="05fb3-383">產生的順序大致上應該遵循使用的可能性，但也有邏輯流程。</span><span class="sxs-lookup"><span data-stu-id="05fb3-383">The resulting order should roughly follow the likelihood of use, but also have a logical flow.</span></span>
-   <span data-ttu-id="05fb3-384">如果命令連結需要進一步的說明，請 **提供補充說明。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-384">If a command link requires further explanation, **provide a supplemental explanation.**</span></span> <span data-ttu-id="05fb3-385">補充說明說明為什麼使用者可能會想要選擇選項，或選擇選項時，會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="05fb3-385">Supplemental explanations describe why users might want to choose the option or what happens if the option is chosen.</span></span>

<span data-ttu-id="05fb3-386">如需詳細的指導方針與範例，請參閱 [命令連結](ctrl-command-links.md)。</span><span class="sxs-lookup"><span data-stu-id="05fb3-386">For more guidelines and examples, see [Command Links](ctrl-command-links.md).</span></span>

### <a name="default-values"></a><span data-ttu-id="05fb3-387">預設值</span><span class="sxs-lookup"><span data-stu-id="05fb3-387">Default values</span></span>

-   <span data-ttu-id="05fb3-388">**確認的預設回應是根據其設計模式：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-388">**The default response for a confirmation is based on its design pattern:**</span></span>



    | <span data-ttu-id="05fb3-389">模式</span><span class="sxs-lookup"><span data-stu-id="05fb3-389">Pattern</span></span>                                                 | <span data-ttu-id="05fb3-390">預設回應</span><span class="sxs-lookup"><span data-stu-id="05fb3-390">Default response</span></span>                                                                                |
    |--------------------------------------------------|---------------------------------------------------------------------------------|
    | <span data-ttu-id="05fb3-391">例行確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-391">Routine confirmations</span></span> <br/>                | <span data-ttu-id="05fb3-392">進行。</span><span class="sxs-lookup"><span data-stu-id="05fb3-392">Proceed.</span></span> <br/>                                                            |
    | <span data-ttu-id="05fb3-393">具風險的動作確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-393">Risky action confirmations</span></span> <br/>           | <span data-ttu-id="05fb3-394">請勿繼續 (或) 的安全選擇。</span><span class="sxs-lookup"><span data-stu-id="05fb3-394">Don't proceed (or the safe choice).</span></span> <br/>                                 |
    | <span data-ttu-id="05fb3-395">非預期的結果確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-395">Unintended consequence confirmations</span></span> <br/> | <span data-ttu-id="05fb3-396">如果結果很重要，請不要繼續;否則，請繼續進行。</span><span class="sxs-lookup"><span data-stu-id="05fb3-396">If consequences are significant, don't proceed; otherwise, proceed.</span></span> <br/> |
    | <span data-ttu-id="05fb3-397">釐清內容</span><span class="sxs-lookup"><span data-stu-id="05fb3-397">Clarifications</span></span> <br/>                       | <span data-ttu-id="05fb3-398">最可能的回應。</span><span class="sxs-lookup"><span data-stu-id="05fb3-398">The most likely response.</span></span> <br/>                                           |
    | <span data-ttu-id="05fb3-399">安全性確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-399">Security confirmations</span></span> <br/>               | <span data-ttu-id="05fb3-400">不要繼續。</span><span class="sxs-lookup"><span data-stu-id="05fb3-400">Don't proceed.</span></span> <br/>                                                      |
    | <span data-ttu-id="05fb3-401">Ulterior 動機確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-401">Ulterior motive confirmations</span></span> <br/>        | <span data-ttu-id="05fb3-402">進行。</span><span class="sxs-lookup"><span data-stu-id="05fb3-402">Proceed.</span></span> <br/>                                                            |



 

### <a name="dont-show-this-message-again"></a><span data-ttu-id="05fb3-403">不要再顯示此訊息</span><span class="sxs-lookup"><span data-stu-id="05fb3-403">Don't show this message again</span></span>

-   <span data-ttu-id="05fb3-404">**此選項只適用于例行和 ulterior 動機確認模式。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-404">**Use this option only for the routine and ulterior motive confirmation patterns.**</span></span> <span data-ttu-id="05fb3-405">針對其他模式，如果需要資訊，應該一律顯示該資訊。</span><span class="sxs-lookup"><span data-stu-id="05fb3-405">For the other patterns, if the information is necessary, it should always be displayed.</span></span>
-   <span data-ttu-id="05fb3-406">**請勿提供這個選項來顯示不必要的確認。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-406">**Don't provide this option to justify displaying an unnecessary confirmation.**</span></span> <span data-ttu-id="05fb3-407">請改為清除確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-407">Just get rid of the confirmation instead.</span></span>

<span data-ttu-id="05fb3-408">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-408">**Incorrect:**</span></span>

![<span data-ttu-id="05fb3-409">[關閉這些提醒嗎？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-409">screen shot of 'dismiss these reminders?'</span></span> ](images/mess-confirm-image32.png)

<span data-ttu-id="05fb3-410">**仍然不正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-410">**Still incorrect:**</span></span>

![[不要再顯示訊息] 的螢幕擷取畫面](images/mess-confirm-image33.png)

<span data-ttu-id="05fb3-412">在這些範例中，新增 [不要再顯示此訊息] 選項並不會修正不必要的確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-412">In these examples, adding a Don't show this message again option doesn't fix an unnecessary confirmation.</span></span>

<span data-ttu-id="05fb3-413">如需詳細指導方針，請參閱 [對話方塊](win-dialog-box.md)。</span><span class="sxs-lookup"><span data-stu-id="05fb3-413">For more guidelines, see [Dialog Boxes](win-dialog-box.md).</span></span>

### <a name="bulk-operations"></a><span data-ttu-id="05fb3-414">大量作業</span><span class="sxs-lookup"><span data-stu-id="05fb3-414">Bulk operations</span></span>

-   <span data-ttu-id="05fb3-415">針對適用于大量作業的確認，提供將確認套用至整個作業的選項。</span><span class="sxs-lookup"><span data-stu-id="05fb3-415">For confirmations that apply to bulk operations, provide an option to apply the confirmation to the entire operation.</span></span>

![<span data-ttu-id="05fb3-416">[對所有專案進行此動作嗎？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-416">screen shot of 'do this for all items?'</span></span> <span data-ttu-id="05fb3-417">核取方塊</span><span class="sxs-lookup"><span data-stu-id="05fb3-417">check box</span></span> ](images/mess-confirm-image34.png)

<span data-ttu-id="05fb3-418">這個範例有大量作業的選項。</span><span class="sxs-lookup"><span data-stu-id="05fb3-418">This example has an option for bulk operations.</span></span>

-   <span data-ttu-id="05fb3-419">在大量作業中刪除或延遲確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-419">Eliminate or postpone confirmations in a bulk operation.</span></span>

<span data-ttu-id="05fb3-420">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-420">**Incorrect:**</span></span>

![<span data-ttu-id="05fb3-421">[確認檔案刪除] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-421">screen shot of 'confirm file delete' dialog box</span></span> ](images/mess-confirm-image35.png)

<span data-ttu-id="05fb3-422">在此範例中，Windows XP 中的 Windows 檔案總管會在大量檔案移動期間確認每個唯讀檔案。</span><span class="sxs-lookup"><span data-stu-id="05fb3-422">In this example, Windows Explorer in Windows XP confirms each read-only file during a bulk file move.</span></span> <span data-ttu-id="05fb3-423">最好是複製唯讀檔案，而不要求或延後處理這些檔案，並在工作結束時提出確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-423">Better just to copy the read-only files without asking, or postpone handling these files and present the confirmation at the end of the task.</span></span>

### <a name="progressive-disclosure"></a><span data-ttu-id="05fb3-424">漸進式揭露</span><span class="sxs-lookup"><span data-stu-id="05fb3-424">Progressive disclosure</span></span>

-   <span data-ttu-id="05fb3-425">**如果您必須在確認訊息中包含 advanced 資訊，請使用累進洩漏按鈕加以顯示 (例如「顯示詳細資料」 ) 。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-425">**If you must include advanced information in a confirmation message, reveal it by using progressive disclosure buttons (for example, "Show details").**</span></span> <span data-ttu-id="05fb3-426">這麼做可簡化一般使用方式的確認。</span><span class="sxs-lookup"><span data-stu-id="05fb3-426">Doing so simplifies the confirmation for typical usage.</span></span> <span data-ttu-id="05fb3-427">請勿隱藏所需的資訊，因為使用者可能找不到它。</span><span class="sxs-lookup"><span data-stu-id="05fb3-427">Don't hide needed information because users might not find it.</span></span>
-   <span data-ttu-id="05fb3-428">**除非真的有更多詳細資料，否則請不要使用 [顯示詳細資料]。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-428">**Don't use "Show details" unless there really is more detail.**</span></span> <span data-ttu-id="05fb3-429">請勿只以不同的格式重新聲明現有的資訊。</span><span class="sxs-lookup"><span data-stu-id="05fb3-429">Don't just restate the existing information in a different format.</span></span>

<span data-ttu-id="05fb3-430">如需標籤指導方針，請參閱 [漸進式洩漏](ctrl-progressive-disclosure-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="05fb3-430">For labeling guidelines, see [Progressive Disclosure](ctrl-progressive-disclosure-controls.md).</span></span>

### <a name="user-account-control"></a><span data-ttu-id="05fb3-431">使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="05fb3-431">User Account Control</span></span>

-   <span data-ttu-id="05fb3-432">**請勿使用「使用者帳戶控制」 (UAC) 提高許可權的 UI 來取代確認。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-432">**Don't use the User Account Control (UAC) elevation UI as a substitute for a confirmation.**</span></span> <span data-ttu-id="05fb3-433">如果動作需要確認，請使用個別的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="05fb3-433">If an action needs a confirmation, use a separate dialog box.</span></span> <span data-ttu-id="05fb3-434">在提高 [許可權的 UI](winenv-uac.md)期間，使用者必須專注于他們是否已啟動工作，以及程式是否值得信任。</span><span class="sxs-lookup"><span data-stu-id="05fb3-434">During the [elevation UI](winenv-uac.md), users need to focus on whether they started task and if the program is trustworthy.</span></span>
-   <span data-ttu-id="05fb3-435">**在提高許可權的 UI 之前顯示確認。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-435">**Display the confirmation before the elevation UI.**</span></span> <span data-ttu-id="05fb3-436">這樣做會排除不必要的提升。</span><span class="sxs-lookup"><span data-stu-id="05fb3-436">Doing so eliminates unnecessary elevations.</span></span>

## <a name="text"></a><span data-ttu-id="05fb3-437">Text</span><span class="sxs-lookup"><span data-stu-id="05fb3-437">Text</span></span>

### <a name="general"></a><span data-ttu-id="05fb3-438">一般</span><span class="sxs-lookup"><span data-stu-id="05fb3-438">General</span></span>

-   <span data-ttu-id="05fb3-439">**移除多餘的文字。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-439">**Remove redundant text.**</span></span> <span data-ttu-id="05fb3-440">在標題、主要指示、補充指示、內容區域、命令連結和認可按鈕中尋找重複的文字。</span><span class="sxs-lookup"><span data-stu-id="05fb3-440">Look for redundant text in titles, main instructions, supplemental instructions, content areas, command links, and commit buttons.</span></span> <span data-ttu-id="05fb3-441">一般而言，請在指示和互動式控制項中保留完整文字，然後從其他位置移除任何多餘的。</span><span class="sxs-lookup"><span data-stu-id="05fb3-441">Generally, leave full text in instructions and interactive controls, and remove any redundancy from the other places.</span></span>
-   <span data-ttu-id="05fb3-442">**請勿在文字中使用「警告」或「警告」。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-442">**Don't use "warning" or "caution" in the text.**</span></span> <span data-ttu-id="05fb3-443">如果使用者需要特別小心，請改為使用警告圖示來表示。</span><span class="sxs-lookup"><span data-stu-id="05fb3-443">If users need to proceed with caution, indicate this using a warning icon instead.</span></span>

<span data-ttu-id="05fb3-444">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-444">**Incorrect:**</span></span>

![<span data-ttu-id="05fb3-445">磁片區格式化確認的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-445">screen shot of volume-formatting confirmation</span></span> ](images/mess-confirm-image36.png)

<span data-ttu-id="05fb3-446">在此範例中，「警告」一詞是不必要的。</span><span class="sxs-lookup"><span data-stu-id="05fb3-446">In this example, the term "warning" is unnecessary.</span></span>

### <a name="titles"></a><span data-ttu-id="05fb3-447">標題</span><span class="sxs-lookup"><span data-stu-id="05fb3-447">Titles</span></span>

-   <span data-ttu-id="05fb3-448">**使用標題來識別確認來自的命令或功能。異常：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-448">**Use the title to identify the command or feature where the confirmation came from. Exceptions:**</span></span>
    -   <span data-ttu-id="05fb3-449">如果有許多不同的命令顯示確認，請考慮改為使用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="05fb3-449">If a confirmation is displayed by many different commands, consider using the program name instead.</span></span>
    -   <span data-ttu-id="05fb3-450">如果該標題是多餘的，或與主要指示混淆，請改用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="05fb3-450">If that title would be redundant or confusing with the main instruction, use the program name instead.</span></span>

<span data-ttu-id="05fb3-451">但是，如果確認來自長時間執行的工作，且在工作開始之後可能會顯示正常，請一律使用命令或功能清楚地識別內容。</span><span class="sxs-lookup"><span data-stu-id="05fb3-451">However, if the confirmation is from a long-running task and may display well after the task started, always use the command or feature to clearly identify the context.</span></span>

-   <span data-ttu-id="05fb3-452">**請勿使用標題來說明在主要指令用途的對話方塊中要執行** 的動作。</span><span class="sxs-lookup"><span data-stu-id="05fb3-452">**Don't use the title to explain what to do in the dialog** that's the purpose of the main instruction.</span></span>
-   <span data-ttu-id="05fb3-453">如果新增了明確的文字，請使用 [確認] 來啟動標題。</span><span class="sxs-lookup"><span data-stu-id="05fb3-453">If it adds clarity, start the title with the word Confirm.</span></span>
-   <span data-ttu-id="05fb3-454">**針對具風險的動作確認，您可以新增涉及其他強調的物件名稱。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-454">**For risky action confirmations, you may add the name of the object involved for extra emphasis.**</span></span>

![<span data-ttu-id="05fb3-455">[格式化 f 磁片磁碟機] 對話方塊標題的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-455">screen shot of 'format f drive' dialog box title</span></span> ](images/mess-confirm-image13.png)

<span data-ttu-id="05fb3-456">在此範例中，標題中包含要格式化的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="05fb3-456">In this example, the drive to be formatted is included in the title.</span></span>

-   <span data-ttu-id="05fb3-457">使用 [標題樣式的大小寫](glossary.md)，但不含結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="05fb3-457">Use [title-style capitalization](glossary.md), without ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="05fb3-458">主要指示</span><span class="sxs-lookup"><span data-stu-id="05fb3-458">Main instructions</span></span>

-   <span data-ttu-id="05fb3-459">**確認的主要指示是根據其設計模式：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-459">**The main instruction for a confirmation is based on its design pattern:**</span></span>



    | <span data-ttu-id="05fb3-460">模式</span><span class="sxs-lookup"><span data-stu-id="05fb3-460">Pattern</span></span>                                                 | <span data-ttu-id="05fb3-461">主要指示</span><span class="sxs-lookup"><span data-stu-id="05fb3-461">Main instruction</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |
    |--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="05fb3-462">非預期的結果確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-462">Unintended consequence confirmations</span></span> <br/> | <span data-ttu-id="05fb3-463">陳述非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-463">state the unintended consequence.</span></span><br/> <span data-ttu-id="05fb3-464">**例外狀況：** 如果問題詢問使用者是否要繼續清楚暗示非預期的結果，請改為詢問問題。</span><span class="sxs-lookup"><span data-stu-id="05fb3-464">**exception:** if a question asking if the user wants to proceed clearly implies the unintended consequence, ask the question instead.</span></span> <br/> <span data-ttu-id="05fb3-465">![[關閉所有索引標籤？] 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-465">![screen shot of 'close all tabs?'</span></span> <span data-ttu-id="05fb3-466">確認 ](images/mess-confirm-image15.png)</span><span class="sxs-lookup"><span data-stu-id="05fb3-466">confirmation ](images/mess-confirm-image15.png)</span></span><br/> <span data-ttu-id="05fb3-467">在此範例中，要求使用者進行充分的傳達動作結果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-467">In this example, asking the user to proceed sufficiently conveys the consequences of the action.</span></span><br/> |
    | <span data-ttu-id="05fb3-468">All others</span><span class="sxs-lookup"><span data-stu-id="05fb3-468">All others</span></span> <br/>                           | <span data-ttu-id="05fb3-469">請詢問一個問題，以判斷使用者是否想要繼續進行。</span><span class="sxs-lookup"><span data-stu-id="05fb3-469">Ask a single question to determine if the user wants to proceed.</span></span> <br/>                                                                                                                                                                                                                                                                                                                              |



 

-   <span data-ttu-id="05fb3-470">**請務必只使用單一的完整句子。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-470">**Be concise use only a single, complete sentence.**</span></span> <span data-ttu-id="05fb3-471">將主要指示帶到基本資訊。</span><span class="sxs-lookup"><span data-stu-id="05fb3-471">Strip the main instruction down to the essential information.</span></span> <span data-ttu-id="05fb3-472">如果您必須進一步說明，請使用補充指示。</span><span class="sxs-lookup"><span data-stu-id="05fb3-472">If you must explain anything more, use a supplemental instruction.</span></span>
-   <span data-ttu-id="05fb3-473">**如果有相關的物件，請特別提供其完整名稱。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-473">**Be specific if there are objects involved, give their full names.**</span></span>
-   <span data-ttu-id="05fb3-474">**使用正片語。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-474">**Use positive phrasing.**</span></span> <span data-ttu-id="05fb3-475">對使用者來說，可以更輕鬆地理解正面片語。</span><span class="sxs-lookup"><span data-stu-id="05fb3-475">Positive phrasing is easier for users to understand.</span></span>

<span data-ttu-id="05fb3-476">**正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-476">**Correct:**</span></span>

<span data-ttu-id="05fb3-477">要啟用檔案和印表機共用嗎？</span><span class="sxs-lookup"><span data-stu-id="05fb3-477">Do you want to enable file and printer sharing?</span></span>

<span data-ttu-id="05fb3-478">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-478">**Incorrect:**</span></span>

<span data-ttu-id="05fb3-479">您要停用檔案和印表機共用嗎？</span><span class="sxs-lookup"><span data-stu-id="05fb3-479">Do you want to disable file and printer sharing?</span></span>

<span data-ttu-id="05fb3-480">不過，片語必須符合相關聯的命令，即使命令有負面片語;例如，使用 disable 來確認 Disable 命令。</span><span class="sxs-lookup"><span data-stu-id="05fb3-480">However, phrasing must match the associated command, even if the command is negatively phrased; so, for example, use disable to confirm a Disable command.</span></span>

-   <span data-ttu-id="05fb3-481">雖然片語沒有嚴格的規則，但 **這些常見的確認片語具有指出的含意：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-481">While there are no strict rules for phrasing, **these common confirmation phrases have the indicated connotation:**</span></span>



    | <span data-ttu-id="05fb3-482">片語</span><span class="sxs-lookup"><span data-stu-id="05fb3-482">Phrase</span></span>                                                            | <span data-ttu-id="05fb3-483">內涵</span><span class="sxs-lookup"><span data-stu-id="05fb3-483">Connotation</span></span>                                                            |
    |-------------------------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="05fb3-484">確定要 \[ 執行動作 \] 嗎？</span><span class="sxs-lookup"><span data-stu-id="05fb3-484">Are you sure you want to \[perform an action\]?</span></span> <br/> | <span data-ttu-id="05fb3-485">確認使用者要求的直接結果。</span><span class="sxs-lookup"><span data-stu-id="05fb3-485">Confirming the direct result of a user request.</span></span> <br/> |
    | <span data-ttu-id="05fb3-486">您要 \[ 執行動作 \] 嗎？</span><span class="sxs-lookup"><span data-stu-id="05fb3-486">Do you want to \[perform an action\]?</span></span> <br/>           | <span data-ttu-id="05fb3-487">確認使用者要求的副作用。</span><span class="sxs-lookup"><span data-stu-id="05fb3-487">Confirming a side effect of a user request.</span></span> <br/>     |
    | <span data-ttu-id="05fb3-488">您要 \[ 選取結果 \] 嗎？</span><span class="sxs-lookup"><span data-stu-id="05fb3-488">Would you like to \[select a result\]?</span></span> <br/>          | <span data-ttu-id="05fb3-489">需要澄清。</span><span class="sxs-lookup"><span data-stu-id="05fb3-489">Need a clarification.</span></span> <br/>                           |
    | <span data-ttu-id="05fb3-490">\[要執行動作 \] 嗎？</span><span class="sxs-lookup"><span data-stu-id="05fb3-490">\[Perform an action\]?</span></span> <br/>                          | <span data-ttu-id="05fb3-491">無含意。</span><span class="sxs-lookup"><span data-stu-id="05fb3-491">No connotation.</span></span> <br/>                                 |



 

-   <span data-ttu-id="05fb3-492">針對具風險的動作確認，請永久使用該詞彙來指出動作無法復原。</span><span class="sxs-lookup"><span data-stu-id="05fb3-492">For risky action confirmations, use the term permanently to indicate that an action can't be undone.</span></span>

![<span data-ttu-id="05fb3-493">永久刪除確認的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="05fb3-493">screen shot of permanent deletion confirmation</span></span> ](images/mess-confirm-image37.png)

<span data-ttu-id="05fb3-494">在此範例中，「永久」表示動作無法復原。</span><span class="sxs-lookup"><span data-stu-id="05fb3-494">In this example, "permanently" indicates that the action can't be undone.</span></span>

-   <span data-ttu-id="05fb3-495">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="05fb3-495">Use [sentence-style capitalization](glossary.md).</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="05fb3-496">補充指示</span><span class="sxs-lookup"><span data-stu-id="05fb3-496">Supplemental instructions</span></span>

-   <span data-ttu-id="05fb3-497">**確認的補充指示是根據其設計模式：**</span><span class="sxs-lookup"><span data-stu-id="05fb3-497">**The supplemental instruction for a confirmation is based on its design pattern:**</span></span>

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="05fb3-498"><strong>模式</strong></span><span class="sxs-lookup"><span data-stu-id="05fb3-498"><strong>Pattern</strong></span></span><br/></td>
    <td><span data-ttu-id="05fb3-499"><strong>補充指示</strong></span><span class="sxs-lookup"><span data-stu-id="05fb3-499"><strong>Supplemental instruction</strong></span></span><br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="05fb3-500">非預期的結果確認</span><span class="sxs-lookup"><span data-stu-id="05fb3-500">Unintended consequence confirmations</span></span> <br/></td>
    <td><span data-ttu-id="05fb3-501">請詢問一個問題，以判斷使用者是否想要繼續進行。</span><span class="sxs-lookup"><span data-stu-id="05fb3-501">Ask a single question to determine if the user wants to proceed.</span></span> <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="05fb3-502">All others</span><span class="sxs-lookup"><span data-stu-id="05fb3-502">All others</span></span> <br/></td>
    <td><span data-ttu-id="05fb3-503">說明使用者可能不想繼續的任何非明顯原因。</span><span class="sxs-lookup"><span data-stu-id="05fb3-503">Explain any non-obvious reasons why the user might not want to proceed.</span></span> <span data-ttu-id="05fb3-504">原因包括：</span><span class="sxs-lookup"><span data-stu-id="05fb3-504">Such reasons include:</span></span> <br/>
    <ul>
    <li><span data-ttu-id="05fb3-505">可能會遺失下列一或多項：</span><span class="sxs-lookup"><span data-stu-id="05fb3-505">Potential loss of one or more of the following:</span></span> <ul>
    <li><span data-ttu-id="05fb3-506">有價值的資產，例如資料遺失或財務損失。</span><span class="sxs-lookup"><span data-stu-id="05fb3-506">A valuable asset, such as data loss or financial loss.</span></span></li>
    <li><span data-ttu-id="05fb3-507">系統存取或完整性。</span><span class="sxs-lookup"><span data-stu-id="05fb3-507">System access or integrity.</span></span></li>
    <li><span data-ttu-id="05fb3-508">隱私權或對機密資訊的控制。</span><span class="sxs-lookup"><span data-stu-id="05fb3-508">Privacy or control over confidential information.</span></span></li>
    </ul></li>
    <li><span data-ttu-id="05fb3-509">無法復原的動作。</span><span class="sxs-lookup"><span data-stu-id="05fb3-509">Actions that are irreversible.</span></span></li>
    </ul></td>
    </tr>
    </tbody>
    </table>

    

     

-   <span data-ttu-id="05fb3-510">**請勿以稍微不同的用語重複主要指令。**</span><span class="sxs-lookup"><span data-stu-id="05fb3-510">**Don't repeat the main instruction with slightly different wording.**</span></span> <span data-ttu-id="05fb3-511">相反地，如果沒有其他要新增的指令，請省略補充指令。</span><span class="sxs-lookup"><span data-stu-id="05fb3-511">Instead, omit the supplemental instruction if there is not more to add.</span></span>
-   <span data-ttu-id="05fb3-512">**針對非預期的結果確認，請考慮使用詞彙，以確定不會** 在使用者忽略主要指示的情況下繼續進行。</span><span class="sxs-lookup"><span data-stu-id="05fb3-512">**For unintended consequence confirmations, consider using the term anyway to concisely indicate that there is a reason not to continue** in case the user overlooked the main instruction.</span></span> <span data-ttu-id="05fb3-513">如需詳細資訊，請參閱設計概念。</span><span class="sxs-lookup"><span data-stu-id="05fb3-513">See Design Concepts for more information.</span></span>
-   <span data-ttu-id="05fb3-514">使用完整句子、句子樣式的大小寫和結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="05fb3-514">Use complete sentences, sentence-style capitalization, and ending punctuation.</span></span>

## <a name="documentation"></a><span data-ttu-id="05fb3-515">文件</span><span class="sxs-lookup"><span data-stu-id="05fb3-515">Documentation</span></span>

<span data-ttu-id="05fb3-516">參考確認時：</span><span class="sxs-lookup"><span data-stu-id="05fb3-516">When referring to confirmations:</span></span>

-   <span data-ttu-id="05fb3-517">如果標題是確認 (（而不是方案名稱) ;），請依標題參閱確認的標題。否則，請使用其主要指示來參考它。</span><span class="sxs-lookup"><span data-stu-id="05fb3-517">Refer to a confirmation by its title if the title is specific to the confirmation (that is, not the program name); otherwise, refer to it by its main instruction.</span></span>
-   <span data-ttu-id="05fb3-518">如有必要，您可以將確認對話方塊參考為訊息。</span><span class="sxs-lookup"><span data-stu-id="05fb3-518">If necessary, you may refer to a confirmation dialog box as a message.</span></span>
-   <span data-ttu-id="05fb3-519">使用完全相符的文字，包括其大小寫。</span><span class="sxs-lookup"><span data-stu-id="05fb3-519">Use the exact text, including its capitalization.</span></span>
-   <span data-ttu-id="05fb3-520">可能的話，請使用粗體格式化文字。</span><span class="sxs-lookup"><span data-stu-id="05fb3-520">When possible, format the text using bold.</span></span> <span data-ttu-id="05fb3-521">否則，請只在必要時才將文字放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="05fb3-521">Otherwise, put the text in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="05fb3-522">範例：在 [ **複製** 檔案] 訊息中，按一下較新的檔案。</span><span class="sxs-lookup"><span data-stu-id="05fb3-522">Example: In the **Copy File** message, click the newer file.</span></span>

