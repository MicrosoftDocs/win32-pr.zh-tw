---
title: 汽球
description: 球形球是一個小型的快顯視窗，可通知使用者有非嚴重問題或控制項中的特殊狀況。
ms.assetid: 67092831-e573-4ad6-b1fc-baa1836031cb
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 348167594db2f7895e185d8d7761832ec5c0c1cb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104321400"
---
# <a name="balloons"></a><span data-ttu-id="eba9d-103">汽球</span><span class="sxs-lookup"><span data-stu-id="eba9d-103">Balloons</span></span>

> [!NOTE]
> <span data-ttu-id="eba9d-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="eba9d-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="eba9d-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="eba9d-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="eba9d-106">球形球是一個小型的快顯視窗，可通知使用者有非嚴重問題或控制項中的特殊狀況。</span><span class="sxs-lookup"><span data-stu-id="eba9d-106">A balloon is a small pop-up window that informs users of a non-critical problem or special condition in a control.</span></span>

![顯示表示 CAPS LOCK 已開啟之氣球的螢幕擷取畫面。](images/ctrl-balloons-image1.png)

<span data-ttu-id="eba9d-108">一般氣球。</span><span class="sxs-lookup"><span data-stu-id="eba9d-108">A typical balloon.</span></span>

<span data-ttu-id="eba9d-109">球標有圖示、標題和內文文字，全都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="eba9d-109">Balloons have an icon, a title, and body text, all of which are optional.</span></span> <span data-ttu-id="eba9d-110">不同于工具提示和提示，氣球也有可識別其來源的結尾。</span><span class="sxs-lookup"><span data-stu-id="eba9d-110">Unlike tooltips and infotips, balloons also have a tail that identifies their source.</span></span> <span data-ttu-id="eba9d-111">通常來源是一個控制項，如果是的話，就稱為「擁有者」 [控制項](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="eba9d-111">Usually the source is a control if so, it is referred to as the [owner control](glossary.md).</span></span>

<span data-ttu-id="eba9d-112">雖然批註提示會通知使用者非重大問題，但不會防止問題，雖然擁有者控制項可能也不會發生。</span><span class="sxs-lookup"><span data-stu-id="eba9d-112">While balloons inform users of non-critical problems, they don't prevent problems although the owner control might.</span></span> <span data-ttu-id="eba9d-113">當使用者嘗試認可動作時，擁有者使用者介面必須處理任何未處理的問題 (UI) 。</span><span class="sxs-lookup"><span data-stu-id="eba9d-113">Any unhandled problems must be handled by the owner user interface (UI) when users attempt to commit to the action.</span></span>

<span data-ttu-id="eba9d-114">氣球通常會與文字方塊一起使用，或使用文字方塊來變更值的控制項，例如下拉式方塊、清單視圖和樹狀檢視。</span><span class="sxs-lookup"><span data-stu-id="eba9d-114">Balloons are usually used with text boxes, or controls that use text boxes for changing values, such as combo boxes, list views, and tree views.</span></span> <span data-ttu-id="eba9d-115">其他種類的控制項都有充分的限制，不需要額外的意見反應氣球。</span><span class="sxs-lookup"><span data-stu-id="eba9d-115">Other kinds of controls are sufficiently well constrained, and don't need the additional feedback balloons afford.</span></span> <span data-ttu-id="eba9d-116">此外，如果其他類型的控制項有問題，通常會在多個控制項之間發生不一致的情況。</span><span class="sxs-lookup"><span data-stu-id="eba9d-116">Furthermore, if there is a problem with other types of controls, it often involves inconsistency between multiple controls a situation for which balloons aren't suitable.</span></span> <span data-ttu-id="eba9d-117">只有文字輸入控制項不受限制，而且是 [單一點錯誤](glossary.md)的常見來源。</span><span class="sxs-lookup"><span data-stu-id="eba9d-117">Only text-entry controls are both unconstrained and a common source of [single-point errors](glossary.md).</span></span>

<span data-ttu-id="eba9d-118">通知是由 [通知區域](winenv-notification.md) 圖示所顯示的特定批註類型。</span><span class="sxs-lookup"><span data-stu-id="eba9d-118">A notification is a specific type of balloon displayed by a [notification area](winenv-notification.md) icon.</span></span>

<span data-ttu-id="eba9d-119">**注意：**[通知](mess-notif.md)、[工具提示和提示](ctrl-tooltips-and-infotips.md)的相關指導方針，以及 [錯誤訊息](mess-error.md)會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="eba9d-119">**Note:** Guidelines related to [notifications](mess-notif.md), [tooltips and infotips](ctrl-tooltips-and-infotips.md), and [error messages](mess-error.md) are presented in separate articles.</span></span>

<span data-ttu-id="eba9d-120">**這是正確的控制項嗎？**</span><span class="sxs-lookup"><span data-stu-id="eba9d-120">**Is this the right control?**</span></span>

<span data-ttu-id="eba9d-121">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="eba9d-121">To decide, consider these questions:</span></span>

-   <span data-ttu-id="eba9d-122">**此資訊是否會描述問題或特殊條件？**</span><span class="sxs-lookup"><span data-stu-id="eba9d-122">**Does the information describe a problem or special condition?**</span></span> <span data-ttu-id="eba9d-123">如果不是，請使用其他控制項。</span><span class="sxs-lookup"><span data-stu-id="eba9d-123">If not, use another control.</span></span> <span data-ttu-id="eba9d-124">請勿使用球形球顯示控制項的補充資訊;請考慮改為使用 [靜態文字](glossary.md)、[提示](glossary.md)、 [漸進式洩漏](glossary.md)或提示。</span><span class="sxs-lookup"><span data-stu-id="eba9d-124">Don't use balloons to display supplemental information for a control; consider using [static text](glossary.md),[infotips](glossary.md), [progressive disclosure](glossary.md), or prompts instead.</span></span>
-   <span data-ttu-id="eba9d-125">在輸入或擁有者控制項失去輸入焦點時 **，是否可以立即偵測到問題或特殊條件**？</span><span class="sxs-lookup"><span data-stu-id="eba9d-125">**Can the problem or special condition be detected immediately** either on input or when the owner control loses input focus?</span></span> <span data-ttu-id="eba9d-126">如果沒有，請使用工作 [對話方塊](glossary.md) 或 [訊息方塊](glossary.md)中顯示的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="eba9d-126">If not, use an error message displayed in a [task dialog](glossary.md) or [message box](glossary.md).</span></span>
-   <span data-ttu-id="eba9d-127">**針對問題，問題是否嚴重？**</span><span class="sxs-lookup"><span data-stu-id="eba9d-127">**For problems, is the problem critical?**</span></span> <span data-ttu-id="eba9d-128">如果是的話，請使用工作對話方塊或訊息方塊中顯示的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="eba9d-128">If so, use an error message displayed in a task dialog or message box.</span></span> <span data-ttu-id="eba9d-129">這類錯誤訊息需要互動 (這適用于) 的重大錯誤，而球標則否。</span><span class="sxs-lookup"><span data-stu-id="eba9d-129">Such error messages require interaction (which is suitable for critical errors), whereas balloons don't.</span></span>
-   <span data-ttu-id="eba9d-130">**針對特殊條件，條件是否有效，但可能不是預期的？**</span><span class="sxs-lookup"><span data-stu-id="eba9d-130">**For special conditions, is the condition valid yet likely to be unintended?**</span></span> <span data-ttu-id="eba9d-131">如果是的話，則會有適當的球標。</span><span class="sxs-lookup"><span data-stu-id="eba9d-131">If so, balloons are appropriate.</span></span> <span data-ttu-id="eba9d-132">在條件不正確情況下，最好是先防止它們發生。</span><span class="sxs-lookup"><span data-stu-id="eba9d-132">For conditions not valid, it is better to prevent them in the first place.</span></span> <span data-ttu-id="eba9d-133">針對可能的情況，不需要採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="eba9d-133">For likely intended conditions, there is no need to do anything.</span></span>
-   <span data-ttu-id="eba9d-134">**問題或特殊條件可以明確表示嗎？**</span><span class="sxs-lookup"><span data-stu-id="eba9d-134">**Can the problem or special condition be expressed concisely?**</span></span> <span data-ttu-id="eba9d-135">如果不是，請使用其他控制項。</span><span class="sxs-lookup"><span data-stu-id="eba9d-135">If not, use another control.</span></span> <span data-ttu-id="eba9d-136">氣球不能有詳細說明或提供補充資訊。</span><span class="sxs-lookup"><span data-stu-id="eba9d-136">Balloons can't have detailed explanations or provide supplemental information.</span></span>
-   <span data-ttu-id="eba9d-137">**此資訊是否描述目前正在停留的控制項？**</span><span class="sxs-lookup"><span data-stu-id="eba9d-137">**Does the information describe the control currently being hovered over?**</span></span> <span data-ttu-id="eba9d-138">如果是的話，請改用秘訣，除非使用者可能需要與訊息互動。</span><span class="sxs-lookup"><span data-stu-id="eba9d-138">If so, use a tip instead, unless users may need to interact with the message.</span></span>
-   <span data-ttu-id="eba9d-139">**這是與使用者目前活動相關的資訊嗎？**</span><span class="sxs-lookup"><span data-stu-id="eba9d-139">**Is the information related to the user's current activity?**</span></span> <span data-ttu-id="eba9d-140">如果沒有，請考慮改為使用 [通知](mess-notif.md) 或 [對話方塊](win-dialog-box.md) 。</span><span class="sxs-lookup"><span data-stu-id="eba9d-140">If not, consider using a [notification](mess-notif.md) or [dialog box](win-dialog-box.md) instead.</span></span> <span data-ttu-id="eba9d-141">使用者可能會忽略目前活動以外的氣球，而且預設會在10秒後出現球的時間。</span><span class="sxs-lookup"><span data-stu-id="eba9d-141">Users are likely to overlook balloons outside the current activity, and, by default, balloons time out after 10 seconds.</span></span>
-   <span data-ttu-id="eba9d-142">**資訊來自單一的特定來源嗎？**</span><span class="sxs-lookup"><span data-stu-id="eba9d-142">**Does the information come from a single, specific source?**</span></span> <span data-ttu-id="eba9d-143">如果問題或條件有多個來源或沒有特定來源，請改用就地 [訊息](glossary.md) 或對話方塊。</span><span class="sxs-lookup"><span data-stu-id="eba9d-143">If a problem or condition has multiple sources or no specific source, use an [in-place message](glossary.md) or a dialog box instead.</span></span>

<span data-ttu-id="eba9d-144">**不正確：** ![氣球的螢幕擷取畫面：登入失敗](images/ctrl-balloons-image2.png)</span><span class="sxs-lookup"><span data-stu-id="eba9d-144">**Incorrect:** ![screen shot of a balloon: logon unsuccessful](images/ctrl-balloons-image2.png)</span></span>

<span data-ttu-id="eba9d-145">在此範例中，問題可能是使用者名稱或密碼，但以視覺化的方式回報問題，表示只有密碼是問題。</span><span class="sxs-lookup"><span data-stu-id="eba9d-145">In this example, the problem could be with the user name or the password, but reporting the problem with a balloon visually suggests that only the password is the problem.</span></span> <span data-ttu-id="eba9d-146">因此，輸入不正確使用者名稱的意見反應會造成誤導。</span><span class="sxs-lookup"><span data-stu-id="eba9d-146">Consequently, the feedback from entering an incorrect user name is misleading.</span></span>

<span data-ttu-id="eba9d-147">氣球是提示、對話方塊和就地訊息的替代方案。</span><span class="sxs-lookup"><span data-stu-id="eba9d-147">Balloons are an alternative to infotips, dialog boxes, and in-place messages.</span></span> <span data-ttu-id="eba9d-148">相對於工具提示和提示：</span><span class="sxs-lookup"><span data-stu-id="eba9d-148">In contrast to tooltips and infotips:</span></span>

-   <span data-ttu-id="eba9d-149">氣球可以獨立于目前的指標位置顯示，因此它們具有表示其來源的結尾。</span><span class="sxs-lookup"><span data-stu-id="eba9d-149">Balloons can be displayed independently of the current pointer location, so they have a tail that indicates their source.</span></span>
-   <span data-ttu-id="eba9d-150">球標有標題、內文文字和圖示。</span><span class="sxs-lookup"><span data-stu-id="eba9d-150">Balloons have a title, body text, and an icon.</span></span>
-   <span data-ttu-id="eba9d-151">氣球可以是互動式的，但無法按一下提示。</span><span class="sxs-lookup"><span data-stu-id="eba9d-151">Balloons can be interactive, whereas it is impossible to click on a tip.</span></span>

<span data-ttu-id="eba9d-152">相對於強制回應對話方塊：</span><span class="sxs-lookup"><span data-stu-id="eba9d-152">In contrast to modal dialog boxes:</span></span>

-   <span data-ttu-id="eba9d-153">球標不會竊取輸入焦點或需要互動。</span><span class="sxs-lookup"><span data-stu-id="eba9d-153">Balloons don't steal input focus or require interaction.</span></span>
-   <span data-ttu-id="eba9d-154">球形球識別單一特定的來源。</span><span class="sxs-lookup"><span data-stu-id="eba9d-154">Balloons identify a single, specific source.</span></span> <span data-ttu-id="eba9d-155">強制回應對話方塊可以有多個來源，或完全沒有特定來源。</span><span class="sxs-lookup"><span data-stu-id="eba9d-155">Modal dialogs can have multiple sources, or no specific source at all.</span></span>

<span data-ttu-id="eba9d-156">相對於就地訊息：</span><span class="sxs-lookup"><span data-stu-id="eba9d-156">In contrast to in-place messages:</span></span>

-   <span data-ttu-id="eba9d-157">球標更明顯。</span><span class="sxs-lookup"><span data-stu-id="eba9d-157">Balloons are more noticeable.</span></span>
-   <span data-ttu-id="eba9d-158">氣球不需要可用的螢幕空間或顯示就地訊息所需的動態配置。</span><span class="sxs-lookup"><span data-stu-id="eba9d-158">Balloons don't require available screen space or the dynamic layout that is required to display in-place messages.</span></span>
-   <span data-ttu-id="eba9d-159">批註會在超時後自動移除。</span><span class="sxs-lookup"><span data-stu-id="eba9d-159">Balloons remove themselves automatically after a timeout.</span></span>

<span data-ttu-id="eba9d-160">**使用模式**</span><span class="sxs-lookup"><span data-stu-id="eba9d-160">**Usage patterns**</span></span>

<span data-ttu-id="eba9d-161">球標具有下列使用模式：</span><span class="sxs-lookup"><span data-stu-id="eba9d-161">Balloons have these usage patterns:</span></span>



|                                                                                                                                                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eba9d-162">**輸入問題** 來自單一擁有者控制項（通常是文字方塊）的非關鍵使用者輸入問題。</span><span class="sxs-lookup"><span data-stu-id="eba9d-162">**Input problem** A non-critical user input problem coming from a single owner control, usually a text box.</span></span> <br/>                                               | <span data-ttu-id="eba9d-163">如果擁有者控制項有輸入焦點，則使用氣球來處理錯誤訊息並不會竊取輸入焦點，但仍會很明顯。</span><span class="sxs-lookup"><span data-stu-id="eba9d-163">using balloons for error messages doesn't steal input focus, yet is still very noticeable if the owner control has input focus.</span></span> <span data-ttu-id="eba9d-164">若要修正此問題，使用者可能必須變更或重新輸入輸入;但是，如果擁有者控制項忽略不正確的輸入，則使用者可能完全不需要進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="eba9d-164">to correct the problem, the user may have to change or reenter the input; but if the owner control ignores incorrect input, the user may not have to make any changes at all.</span></span> <span data-ttu-id="eba9d-165">因為此問題並不重要，所以不需要任何 [錯誤圖示](vis-std-icons.md) 。</span><span class="sxs-lookup"><span data-stu-id="eba9d-165">because the problem isn't critical, no [error icon](vis-std-icons.md) is necessary.</span></span> <br/> <span data-ttu-id="eba9d-166">![顯示表示不正確字元之氣球的螢幕擷取畫面。](images/ctrl-balloons-image3.png)</span><span class="sxs-lookup"><span data-stu-id="eba9d-166">![Screenshot that shows a balloon indicating an incorrect character.](images/ctrl-balloons-image3.png)</span></span><br/> <span data-ttu-id="eba9d-167">用來報告非關鍵性使用者輸入問題的氣球。</span><span class="sxs-lookup"><span data-stu-id="eba9d-167">A balloon used to report a non-critical user input problem.</span></span><br/>                                                                                                  |
| <span data-ttu-id="eba9d-168">**特殊條件** 擁有者控制項處於影響輸入的狀態。</span><span class="sxs-lookup"><span data-stu-id="eba9d-168">**Special condition** The owner control is in a state that affects input.</span></span> <span data-ttu-id="eba9d-169">此狀態可能是非預期的，使用者可能不會察覺到輸入受到影響。</span><span class="sxs-lookup"><span data-stu-id="eba9d-169">This state is likely unintended and the user may not realize input is affected.</span></span> <br/> | <span data-ttu-id="eba9d-170">使用球標來防止發生問題，方法是在使用者發生特殊狀況時立即發出警示 (例如，超過輸入大小上限，或錯誤) 設定 caps lock。</span><span class="sxs-lookup"><span data-stu-id="eba9d-170">use balloons to prevent frustration by alerting users of special conditions as soon as they happen (for example, exceeding maximum input size or setting caps lock on by mistake).</span></span> <span data-ttu-id="eba9d-171">請務必提供這類意見反應，而不需要竊取輸入焦點或強制互動，因為這些條件可能是故意的。</span><span class="sxs-lookup"><span data-stu-id="eba9d-171">it is important to give such feedback without stealing input focus or forcing interaction because these conditions might be intentional.</span></span> <span data-ttu-id="eba9d-172">這些球標對密碼和 pin 方塊來說特別重要，因為使用者會在其他情況下使用最短的意見反應。</span><span class="sxs-lookup"><span data-stu-id="eba9d-172">these balloons are especially important for password and pin boxes, where users are otherwise working with minimal feedback.</span></span> <span data-ttu-id="eba9d-173">這些球標有 [警告圖示](vis-std-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="eba9d-173">these balloons have a [warning icon](vis-std-icons.md).</span></span> <br/> <span data-ttu-id="eba9d-174">![顯示指出 CAPS LOCK 已開啟且輸入錯誤字元之氣球的螢幕擷取畫面。](images/ctrl-balloons-image4.png)</span><span class="sxs-lookup"><span data-stu-id="eba9d-174">![Screenshot that shows balloons indicating Caps Lock is on and an incorrect character is entered.](images/ctrl-balloons-image4.png)</span></span><br/> <span data-ttu-id="eba9d-175">用來報告特殊條件的氣球。</span><span class="sxs-lookup"><span data-stu-id="eba9d-175">A balloon used to report a special condition.</span></span><br/> |



 

<span data-ttu-id="eba9d-176">**指導方針**</span><span class="sxs-lookup"><span data-stu-id="eba9d-176">**Guidelines**</span></span>

<span data-ttu-id="eba9d-177">**顯示時機**</span><span class="sxs-lookup"><span data-stu-id="eba9d-177">**When to display**</span></span>

-   <span data-ttu-id="eba9d-178">**一旦偵測到問題或特殊狀況（即使重複）時，就會顯示氣球，而不會有明顯的延遲。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-178">**Display the balloon as soon as the problem or special condition is detected, even if repeatedly, without any noticeable delay.**</span></span>
    -   <span data-ttu-id="eba9d-179">針對涉及個別字元或最大輸入大小的問題，請在輸入時立即顯示批註提示。</span><span class="sxs-lookup"><span data-stu-id="eba9d-179">For problems involving individual characters or the maximum input size, display the balloon immediately on input.</span></span>
    -   <span data-ttu-id="eba9d-180">針對涉及輸入值的問題 (包括需要非空白值) ，當擁有者控制項失去輸入焦點時，會顯示氣球。</span><span class="sxs-lookup"><span data-stu-id="eba9d-180">For problems involving the input value (including requiring a non-blank value), display the balloon when the owner control loses input focus.</span></span> <span data-ttu-id="eba9d-181">否則，當使用者輸入可能有效的輸入時，顯示氣球可能會造成干擾和討厭。</span><span class="sxs-lookup"><span data-stu-id="eba9d-181">Otherwise, displaying balloons while users are entering potentially valid input can be distracting and annoying.</span></span>
-   <span data-ttu-id="eba9d-182">**一次只顯示一個氣球。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-182">**Display only one balloon at a time.**</span></span> <span data-ttu-id="eba9d-183">顯示多個球形球可能會很龐大。</span><span class="sxs-lookup"><span data-stu-id="eba9d-183">Displaying multiple balloons can be overwhelming.</span></span> <span data-ttu-id="eba9d-184">如果單一事件導致多個問題，可能會一次呈現所有問題，或只報告最重要的問題。</span><span class="sxs-lookup"><span data-stu-id="eba9d-184">If a single event results in multiple problems, either present all the problems at once or report only the most important problem.</span></span>

<span data-ttu-id="eba9d-185">**不正確：** ![指向一個方塊的兩個球的螢幕擷取畫面](images/ctrl-balloons-image5.png)</span><span class="sxs-lookup"><span data-stu-id="eba9d-185">**Incorrect:** ![screen shot of two balloons pointing to one box](images/ctrl-balloons-image5.png)</span></span>

<span data-ttu-id="eba9d-186">在此範例中，同時有兩個問題不正確地呈現。</span><span class="sxs-lookup"><span data-stu-id="eba9d-186">In this example, two problems are incorrectly presented at the same time.</span></span>

<span data-ttu-id="eba9d-187">**顯示的時間長度**</span><span class="sxs-lookup"><span data-stu-id="eba9d-187">**How long to display**</span></span>

-   <span data-ttu-id="eba9d-188">**移除氣球的時機：**</span><span class="sxs-lookup"><span data-stu-id="eba9d-188">**Remove a balloon when:**</span></span>
    -   <span data-ttu-id="eba9d-189">問題已解決或已移除特殊條件。</span><span class="sxs-lookup"><span data-stu-id="eba9d-189">The problem is resolved or special condition is removed.</span></span>
    -   <span data-ttu-id="eba9d-190">使用者輸入有效的資料 () 輸入問題。</span><span class="sxs-lookup"><span data-stu-id="eba9d-190">The user enters valid data (for input problems).</span></span>
    -   <span data-ttu-id="eba9d-191">球形球的時間。預設會在10秒後移除批註，但使用者可以藉由修改 SPI \_ MESSAGEDURATION 系統參數來變更。</span><span class="sxs-lookup"><span data-stu-id="eba9d-191">The balloon times out. By default balloons remove themselves after 10 seconds, although users can change this by modifying the SPI\_MESSAGEDURATION system parameter.</span></span>
-   <span data-ttu-id="eba9d-192">**如果在問題解決之前，使用者無法繼續，請移除超時時間。開發人員：** 在 Win32 中，您可以使用 TTM SETDELAYTIME 訊息來設定顯示時間 \_ 。</span><span class="sxs-lookup"><span data-stu-id="eba9d-192">**Remove the timeout if users can't continue until the problem is resolved.Developers:** In Win32, you can set the display time with the TTM\_SETDELAYTIME message.</span></span>

<span data-ttu-id="eba9d-193">**如何顯示**</span><span class="sxs-lookup"><span data-stu-id="eba9d-193">**How to display**</span></span>

-   <span data-ttu-id="eba9d-194">**將批註顯示在其擁有者控制項底下。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-194">**Display balloons below their owner control.**</span></span> <span data-ttu-id="eba9d-195">這麼做可讓使用者查看內容，包括擁有者控制項和其標籤。</span><span class="sxs-lookup"><span data-stu-id="eba9d-195">Doing so allows users to view the context, including the owner control and its label.</span></span> <span data-ttu-id="eba9d-196">Microsoft Windows 會自動調整球形球的位置，使其完全在螢幕上。</span><span class="sxs-lookup"><span data-stu-id="eba9d-196">Microsoft Windows automatically adjusts balloon positions so that they are completely on screen.</span></span> <span data-ttu-id="eba9d-197">預設行為是在其擁有者控制項上方顯示氣球，就像使用通知完成一樣。</span><span class="sxs-lookup"><span data-stu-id="eba9d-197">The default behavior is to display a balloon above its owner control, as done with notifications.</span></span>

<span data-ttu-id="eba9d-198">**正確：** ![顯示在控制項下方的氣球螢幕擷取畫面](images/ctrl-balloons-image6.png)</span><span class="sxs-lookup"><span data-stu-id="eba9d-198">**Correct:** ![screen shot of a balloon displayed below its control](images/ctrl-balloons-image6.png)</span></span>

<span data-ttu-id="eba9d-199">**不正確：** ![顯示在其控制項上方之氣球的螢幕擷取畫面](images/ctrl-balloons-image7.png)</span><span class="sxs-lookup"><span data-stu-id="eba9d-199">**Incorrect:** ![screen shot of a balloon displayed above its control](images/ctrl-balloons-image7.png)</span></span>

<span data-ttu-id="eba9d-200">在不正確的範例中，會將氣球滑雪顯示在其擁有者控制項上方。</span><span class="sxs-lookup"><span data-stu-id="eba9d-200">In the incorrect example, the balloon is awkwardly displayed above its owner control.</span></span>

<span data-ttu-id="eba9d-201">**密碼和 PIN 文字方塊**</span><span class="sxs-lookup"><span data-stu-id="eba9d-201">**Password and PIN text boxes**</span></span>

-   <span data-ttu-id="eba9d-202">**使用氣球來指出 Caps lock 已開啟，並** 使用下列範例中的文字：</span><span class="sxs-lookup"><span data-stu-id="eba9d-202">**Use a balloon to indicate that Caps Lock is on**, using the text in the following example:</span></span>

![指出 caps lock 開啟之氣球的螢幕擷取畫面](images/ctrl-balloons-image8.png)

<span data-ttu-id="eba9d-204">在此範例中，球標表示在 [釘選] 文字方塊中開啟 CAPS LOCK。</span><span class="sxs-lookup"><span data-stu-id="eba9d-204">In this example, a balloon indicates that Caps Lock is on in a PIN text box.</span></span>

-   <span data-ttu-id="eba9d-205">**使用氣球來指出使用者何時嘗試超過最大輸入大小。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-205">**Use a balloon to indicate when users attempt to exceed the maximum input size.**</span></span> <span data-ttu-id="eba9d-206">到達輸入大小上限比一般文字方塊的密碼和 PIN 文字方塊更不明顯。</span><span class="sxs-lookup"><span data-stu-id="eba9d-206">Reaching the maximum input size is much less obvious in password and PIN text boxes than ordinary text boxes.</span></span>

![表示 pin 碼限制之氣球的螢幕擷取畫面](images/ctrl-balloons-image9.png)

<span data-ttu-id="eba9d-208">在此範例中，氣球表示使用者嘗試超過輸入大小上限。</span><span class="sxs-lookup"><span data-stu-id="eba9d-208">In this example, a balloon indicates that the user is attempting to exceed the maximum input size.</span></span>

-   <span data-ttu-id="eba9d-209">**使用氣球來指出使用者輸入不正確的字元。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-209">**Use a balloon to indicate when users input incorrect characters.**</span></span> <span data-ttu-id="eba9d-210">不過，最好不要有這類限制，因為它們會降低密碼或 PIN 的安全性。</span><span class="sxs-lookup"><span data-stu-id="eba9d-210">However, it is better not to have such restrictions because they reduce the security of the password or PIN.</span></span> <span data-ttu-id="eba9d-211">為了避免資訊洩漏，氣球只會提及有關有效密碼或 Pin 的已記載事實。</span><span class="sxs-lookup"><span data-stu-id="eba9d-211">To prevent information disclosure, the balloon should mention only documented facts about valid passwords or PINs.</span></span>

![表示輸入不正確之氣球的螢幕擷取畫面](images/ctrl-balloons-image10.png)

<span data-ttu-id="eba9d-213">在此範例中，球標表示 PIN 需要數位。</span><span class="sxs-lookup"><span data-stu-id="eba9d-213">In this example, a balloon indicates that the PIN requires numbers.</span></span>

<span data-ttu-id="eba9d-214">**其他文字方塊**</span><span class="sxs-lookup"><span data-stu-id="eba9d-214">**Other text boxes**</span></span>

-   <span data-ttu-id="eba9d-215">**請考慮使用氣球來指出使用者何時嘗試超過重要、簡短的文字方塊的最大輸入大小（以初級使用者為目標）。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-215">**Consider using a balloon to indicate when users attempt to exceed the maximum input size for critical, short text boxes aimed at novice users.**</span></span> <span data-ttu-id="eba9d-216">範例包括使用者名稱和帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="eba9d-216">Examples include user names and account names.</span></span> <span data-ttu-id="eba9d-217">當使用者嘗試超過輸入上限時，文字方塊會發出嗶聲，但使用者可能不了解嗶聲的意義。</span><span class="sxs-lookup"><span data-stu-id="eba9d-217">Text boxes beep when users attempt to exceed the maximum input, but novice users might not understand the meaning of the beep.</span></span>

![指出字元限制之氣球的螢幕擷取畫面](images/ctrl-balloons-image11.png)

<span data-ttu-id="eba9d-219">在此範例中，氣球表示使用者嘗試超過輸入大小上限。</span><span class="sxs-lookup"><span data-stu-id="eba9d-219">In this example, a balloon indicates that the user attempted to exceed the maximum input size.</span></span>

<span data-ttu-id="eba9d-220">**互動**</span><span class="sxs-lookup"><span data-stu-id="eba9d-220">**Interaction**</span></span>

-   <span data-ttu-id="eba9d-221">**當使用者按一下球形框時，只要解除批註提示，而不顯示任何其他 UI 或有任何其他副作用。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-221">**When users click a balloon, just dismiss the balloon without displaying any other UI or having any other side effect.**</span></span> <span data-ttu-id="eba9d-222">與通知不同的是，球標不應有關閉按鈕。</span><span class="sxs-lookup"><span data-stu-id="eba9d-222">Unlike notifications, balloons shouldn't have close buttons.</span></span>

<span data-ttu-id="eba9d-223">**圖示**</span><span class="sxs-lookup"><span data-stu-id="eba9d-223">**Icons**</span></span>

-   <span data-ttu-id="eba9d-224">根據使用模式選擇圖示：</span><span class="sxs-lookup"><span data-stu-id="eba9d-224">Choose the icon based on the usage pattern:</span></span>



    |  <span data-ttu-id="eba9d-225">模式</span><span class="sxs-lookup"><span data-stu-id="eba9d-225">Pattern</span></span> |  <span data-ttu-id="eba9d-226">圖示</span><span class="sxs-lookup"><span data-stu-id="eba9d-226">Icon</span></span>                                                                                                                                                       |
    ------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="eba9d-227">輸入問題</span><span class="sxs-lookup"><span data-stu-id="eba9d-227">Input problem</span></span> | <span data-ttu-id="eba9d-228">無圖示。</span><span class="sxs-lookup"><span data-stu-id="eba9d-228">No icon.</span></span> <span data-ttu-id="eba9d-229">此處未使用 [錯誤圖示](vis-std-icons.md) ，與 [Windows 音調](text-style-tone.md) 指導方針一致。</span><span class="sxs-lookup"><span data-stu-id="eba9d-229">Not using an [error icon](vis-std-icons.md) here is consistent with the [Windows tone](text-style-tone.md) guidelines.</span></span> |
    | <span data-ttu-id="eba9d-230">特殊條件</span><span class="sxs-lookup"><span data-stu-id="eba9d-230">Special condition</span></span> | <span data-ttu-id="eba9d-231">標準16x16 圖元 [警告圖示](vis-std-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="eba9d-231">The standard 16x16 pixel [warning icon](vis-std-icons.md).</span></span>                                                                                  |

<span data-ttu-id="eba9d-232">**協助工具**</span><span class="sxs-lookup"><span data-stu-id="eba9d-232">**Accessibility**</span></span>

<span data-ttu-id="eba9d-233">正確使用時，氣球會增強存取範圍。</span><span class="sxs-lookup"><span data-stu-id="eba9d-233">When used properly, balloons enhance accessibility.</span></span> <span data-ttu-id="eba9d-234">可存取的球標：</span><span class="sxs-lookup"><span data-stu-id="eba9d-234">For balloons to be accessible:</span></span>

-   <span data-ttu-id="eba9d-235">只顯示與使用者目前活動相關的氣球。</span><span class="sxs-lookup"><span data-stu-id="eba9d-235">Only display balloons that relate to the user's current activity.</span></span>
-   <span data-ttu-id="eba9d-236">將氣球文字保持簡潔。</span><span class="sxs-lookup"><span data-stu-id="eba9d-236">Keep the balloon text concise.</span></span> <span data-ttu-id="eba9d-237">這樣做可讓視力較低的使用者更容易閱讀文字提示文字，並將螢幕讀取器讀取時的中斷降到最低。</span><span class="sxs-lookup"><span data-stu-id="eba9d-237">Doing so makes the balloon text easier to read for users with low vision, and minimizes the interruption when read by screen readers.</span></span>
-   <span data-ttu-id="eba9d-238">每當問題或條件重複時，重新顯示氣球。</span><span class="sxs-lookup"><span data-stu-id="eba9d-238">Redisplay the balloon whenever the problem or condition recurs.</span></span>

<span data-ttu-id="eba9d-239">**Text**</span><span class="sxs-lookup"><span data-stu-id="eba9d-239">**Text**</span></span>

<span data-ttu-id="eba9d-240">**標題文字**</span><span class="sxs-lookup"><span data-stu-id="eba9d-240">**Title text**</span></span>

-   <span data-ttu-id="eba9d-241">**使用標題文字，以簡潔的方式摘要輸入問題或特殊條件的明確、簡潔、明確的語言。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-241">**Use title text that briefly summarizes the input problem or special condition in clear, plain, concise, specific language.**</span></span> <span data-ttu-id="eba9d-242">使用者應該能夠快速且輕鬆地瞭解氣球的用途。</span><span class="sxs-lookup"><span data-stu-id="eba9d-242">Users should be able to understand the purpose of the balloon quickly and with minimal effort.</span></span>
-   <span data-ttu-id="eba9d-243">**使用文字片段或完成句子，而不結束標點符號。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-243">**Use text fragments or complete sentences without ending punctuation.**</span></span>
-   <span data-ttu-id="eba9d-244">**使用句型大寫。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-244">**Use sentence-style capitalization.**</span></span> <span data-ttu-id="eba9d-245">如需詳細資訊，請參閱 [詞彙](./glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="eba9d-245">For more info, see the [glossary](./glossary.md).</span></span>
-   <span data-ttu-id="eba9d-246">**使用英文)  (不超過48個字元來容納當地語系化。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-246">**Use no more than 48 characters (in English) to accommodate localization.**</span></span> <span data-ttu-id="eba9d-247">標題的長度上限為63個字元，而且必須至少要有30% 才能容納當地語系化。</span><span class="sxs-lookup"><span data-stu-id="eba9d-247">The title has a maximum length of 63 characters and must be able to expand by at least 30 percent to accommodate localization.</span></span>

<span data-ttu-id="eba9d-248">**主體文字**</span><span class="sxs-lookup"><span data-stu-id="eba9d-248">**Body text**</span></span>

-   <span data-ttu-id="eba9d-249">**使用內文文字的第一個句子，以與使用者清楚相關的方式來陳述問題或條件。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-249">**Use the first sentence of the body text to state the problem or condition in a way that is clearly relevant to the user.**</span></span> <span data-ttu-id="eba9d-250">請勿重複標題中的資訊。</span><span class="sxs-lookup"><span data-stu-id="eba9d-250">Don't repeat the information in the title.</span></span> <span data-ttu-id="eba9d-251">如果沒有其他要加入的專案，請省略此專案。</span><span class="sxs-lookup"><span data-stu-id="eba9d-251">Omit this if there is nothing more to add.</span></span>
-   <span data-ttu-id="eba9d-252">**使用第二個句子來陳述使用者可以執行哪些動作來解決問題或還原狀態。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-252">**Use the second sentence to state what the user can do to resolve the problem or revert the state.**</span></span> <span data-ttu-id="eba9d-253">根據 [樣式和語氣](./text-style-tone.md) 指導方針，在本聲明中不需要使用 word。</span><span class="sxs-lookup"><span data-stu-id="eba9d-253">In accordance with the [Style and Tone](./text-style-tone.md) guidelines, there's no need to use the word Please in this statement.</span></span> <span data-ttu-id="eba9d-254">將兩個分行符號放在第一個和第二個句子之間。</span><span class="sxs-lookup"><span data-stu-id="eba9d-254">Put two line breaks between the first and second sentences.</span></span>

![具有標題和主體文字之氣球的螢幕擷取畫面](images/ctrl-balloons-image12.png)

<span data-ttu-id="eba9d-256">此範例顯示標準的氣球文字配置。</span><span class="sxs-lookup"><span data-stu-id="eba9d-256">This example shows the standard balloon text layout.</span></span>

-   <span data-ttu-id="eba9d-257">**說明如何解決問題或還原狀態，即使該說明很明顯，** 但卻省略問題陳述與其解決方法之間的冗余。</span><span class="sxs-lookup"><span data-stu-id="eba9d-257">**Explain how to resolve the problem or revert the state even if that explanation is obvious,** but omit redundancy between the problem statement and its resolution.</span></span> <span data-ttu-id="eba9d-258">**異常：**</span><span class="sxs-lookup"><span data-stu-id="eba9d-258">**Exceptions:**</span></span>
    -   <span data-ttu-id="eba9d-259">如果無法精確表示，或沒有明顯的冗余，請省略解析度。</span><span class="sxs-lookup"><span data-stu-id="eba9d-259">Omit the resolution if it can't be expressed concisely or without significant redundancy.</span></span>
    -   <span data-ttu-id="eba9d-260">如果沒有使用者要執行的動作，例如當忽略不正確的字元時，請省略解析度。</span><span class="sxs-lookup"><span data-stu-id="eba9d-260">Omit the resolution if there is nothing for the user to do, such as when incorrect characters are ignored.</span></span>
-   <span data-ttu-id="eba9d-261">**使用結尾標點符號的完整句子。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-261">**Use complete sentences with ending punctuation.**</span></span>
-   <span data-ttu-id="eba9d-262">**使用句型大寫。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-262">**Use sentence-style capitalization.**</span></span>
-   <span data-ttu-id="eba9d-263">**使用英文)  (不超過200個字元來容納當地語系化。**</span><span class="sxs-lookup"><span data-stu-id="eba9d-263">**Use no more than 200 characters (in English) to accommodate localization.**</span></span> <span data-ttu-id="eba9d-264">本文文字的最大長度為255個字元，而且必須至少要有30% 才能容納當地語系化。</span><span class="sxs-lookup"><span data-stu-id="eba9d-264">The body text has a maximum length of 255 characters and must be able to expand by at least 30 percent to accommodate localization.</span></span>

<span data-ttu-id="eba9d-265">**文件集**</span><span class="sxs-lookup"><span data-stu-id="eba9d-265">**Documentation**</span></span>

<span data-ttu-id="eba9d-266">參考氣球時：</span><span class="sxs-lookup"><span data-stu-id="eba9d-266">When referring to balloons:</span></span>

-   <span data-ttu-id="eba9d-267">使用確切的標題文字，包括其大小寫。</span><span class="sxs-lookup"><span data-stu-id="eba9d-267">Use the exact title text, including its capitalization.</span></span>
-   <span data-ttu-id="eba9d-268">請將此元件稱為氣球，而不是通知或警示。</span><span class="sxs-lookup"><span data-stu-id="eba9d-268">Refer to the component as a balloon, not as a notification or an alert.</span></span>
-   <span data-ttu-id="eba9d-269">可能的話，請使用粗體文字來格式化標題文字。</span><span class="sxs-lookup"><span data-stu-id="eba9d-269">When possible, format the title text using bold text.</span></span> <span data-ttu-id="eba9d-270">否則，請只在必要時才將標題放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="eba9d-270">Otherwise, put the title in quotation marks only if required to prevent confusion.</span></span>

