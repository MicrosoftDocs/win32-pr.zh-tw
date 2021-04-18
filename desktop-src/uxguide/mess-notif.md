---
title: " (設計基本概念) 的通知"
description: 通知會通知使用者與目前使用者活動不相關的事件，方法是在通知區域中的圖示上短暫顯示批註。
ms.assetid: dcac2fb7-e503-4ea3-a2c5-e3cb660c040a
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5de312b33a970245d2f6f410e55a891c286d9aa7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104565085"
---
# <a name="notifications-design-basics"></a><span data-ttu-id="ffcf5-103"> (設計基本概念) 的通知</span><span class="sxs-lookup"><span data-stu-id="ffcf5-103">Notifications (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="ffcf5-104">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-104">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="ffcf5-105">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-105">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="ffcf5-106">通知會通知使用者與目前使用者活動不相關的事件，方法是在通知區域中的圖示上短暫顯示批註。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-106">A notification informs users of events that are unrelated to the current user activity, by briefly displaying a balloon from an icon in the notification area.</span></span> <span data-ttu-id="ffcf5-107">通知可能是由使用者動作或重要的系統事件所造成，或可能提供 Microsoft Windows 或應用程式可能有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-107">The notification could result from a user action or significant system event, or could offer potentially useful information from Microsoft Windows or an application.</span></span>

<span data-ttu-id="ffcf5-108">通知中的資訊很 **有用且相關，但絕對不重要。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-108">The information in a notification is **useful and relevant, but never critical.**</span></span> <span data-ttu-id="ffcf5-109">因此，通知不需要立即的使用者動作，使用者可以自由地忽略它們。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-109">Consequently, notifications don't require immediate user action and users can freely ignore them.</span></span>

![<span data-ttu-id="ffcf5-110">標題中包含 [新增更新] 之氣球的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-110">screen shot of balloon with 'new updates' in title</span></span> ](images/mess-notif-image1.png)

<span data-ttu-id="ffcf5-111">一般通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-111">A typical notification.</span></span>

<span data-ttu-id="ffcf5-112">在 Windows Vista （含）以後版本中，系統會在9秒的固定期間內顯示通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-112">In Windows Vista and later, notifications are displayed for a fixed duration of 9 seconds.</span></span> <span data-ttu-id="ffcf5-113">當使用者處於非使用中狀態或螢幕保護裝置程式正在執行時，不會立即顯示通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-113">Notifications aren't displayed immediately when users are inactive or screen savers are running.</span></span> <span data-ttu-id="ffcf5-114">Windows 會在這段時間內自動將通知排入佇列，並在使用者繼續進行一般活動時顯示佇列的通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-114">Windows automatically queues notifications during these times, and displays the queued notifications when the user resumes regular activity.</span></span> <span data-ttu-id="ffcf5-115">因此，您不需要採取任何動作來處理這些特殊情況。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-115">Consequently, you don't have to do anything to handle these special circumstances.</span></span>

<span data-ttu-id="ffcf5-116">**開發人員：** 您可以使用 SHQueryUserNotificationState API 來判斷使用者何時處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-116">**Developers:** You can determine when the user is active using the SHQueryUserNotificationState API.</span></span>

<span data-ttu-id="ffcf5-117">**注意：**[通知區域](winenv-notification.md)、[工作列](winenv-taskbar.md)和 [氣球](ctrl-balloons.md)的相關指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-117">**Note:** Guidelines related to [notification area](winenv-notification.md), [taskbar](winenv-taskbar.md), and [balloons](ctrl-balloons.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="ffcf5-118">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="ffcf5-118">Is this the right user interface?</span></span>

<span data-ttu-id="ffcf5-119">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-119">To decide, consider these questions:</span></span>

-   <span data-ttu-id="ffcf5-120">**這項資訊是使用者與應用程式互動的直接結果嗎？**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-120">**Is the information the immediate, direct result of users' interaction with your application?**</span></span> <span data-ttu-id="ffcf5-121">若是如此，請使用 [對話方塊](win-dialog-box.md)、 [訊息方塊](glossary.md)、 [氣球](ctrl-balloons.md)或 [就地](glossary.md) UI，直接在您的應用程式中顯示此同步資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-121">If so, display this synchronous information directly within your application instead using a [dialog box](win-dialog-box.md), [message box](glossary.md), [balloon](ctrl-balloons.md), or [in place](glossary.md) UI.</span></span> <span data-ttu-id="ffcf5-122">通知僅適用于非同步資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-122">Notifications are for asynchronous information only.</span></span>

![<span data-ttu-id="ffcf5-123">windows 安全性警示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-123">screen shot of windows security alert</span></span> ](images/mess-notif-image2.png)

<span data-ttu-id="ffcf5-124">在此範例中，[Windows 防火牆例外狀況] 對話方塊會顯示為使用者互動的直接結果。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-124">In this example, the Windows Firewall exceptions dialog box is displayed as a direct result of user interaction.</span></span> <span data-ttu-id="ffcf5-125">在這裡不適合使用通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-125">A notification wouldn't be appropriate here.</span></span>

-   <span data-ttu-id="ffcf5-126">**只有當使用者主動使用您的應用程式時，才會有相關資訊？**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-126">**Is the information relevant only when users are actively using your application?**</span></span> <span data-ttu-id="ffcf5-127">如果是的話，請在您應用程式的 [狀態列](ctrl-status-bars.md) 或其他狀態區域中顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-127">If so, display the information in your application's [status bar](ctrl-status-bars.md) or other status area.</span></span>

![<span data-ttu-id="ffcf5-128">outlook 狀態列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-128">screen shot of outlook status bar</span></span> ](images/mess-notif-image3.png)

<span data-ttu-id="ffcf5-129">在此範例中，Outlook 會在其狀態列上顯示其連接和同步處理狀態。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-129">In this example, Outlook displays its connection and synchronization state on its status bar.</span></span>

-   <span data-ttu-id="ffcf5-130">**資訊是否快速變更、持續、即時的資訊？**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-130">**Is the information rapidly changing, continuous, real-time information?**</span></span> <span data-ttu-id="ffcf5-131">範例包括處理進度、股票報價和體育分數。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-131">Examples include processing progress, stock quotes, and sports scores.</span></span> <span data-ttu-id="ffcf5-132">若是如此，請不要使用通知，因為它們不適用於快速變更的資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-132">If so, don't use notifications because they aren't suitable for rapidly changing information.</span></span>
-   <span data-ttu-id="ffcf5-133">**此資訊是否有用且相關？使用者是否有可能變更其行為，或避免因為接收資訊而造成的不便？**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-133">**Is the information useful and relevant? Are users likely to change their behavior or avoid inconvenience as the result of receiving the information?**</span></span> <span data-ttu-id="ffcf5-134">如果不是，則不會顯示資訊，或將其放在狀態視窗或記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-134">If not, either don't display the information or put it in a status window or log file.</span></span>
-   <span data-ttu-id="ffcf5-135">**資訊很重要嗎？是否需要立即採取動作？**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-135">**Is the information critical? Is immediate action required?**</span></span> <span data-ttu-id="ffcf5-136">如果是的話，請使用需要注意的介面來顯示資訊，而且無法輕易地忽略，例如強制回應對話方塊或訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-136">If so, display the information using an interface that demands attention and cannot be easily ignored, such as a modal dialog box or message box.</span></span> <span data-ttu-id="ffcf5-137">如果程式未在使用中，您可以將 [程式的工作列按鈕閃爍](winenv-taskbar.md) 三次，並讓它反白顯示，直到程式處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-137">If the program isn't active, you can draw attention to the critical information by [flashing the program's taskbar button](winenv-taskbar.md) three times and leaving it highlighted until the program is active.</span></span>
-   <span data-ttu-id="ffcf5-138">**主要目標使用者是 IT 專業人員嗎？**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-138">**Are the primary target users IT professionals?**</span></span> <span data-ttu-id="ffcf5-139">若是如此，請使用替代的意見反應機制，例如 [記錄](glossary.md) 檔專案或電子郵件訊息。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-139">If so, use an alternative feedback mechanism such as [log file](glossary.md) entries or e-mail messages.</span></span> <span data-ttu-id="ffcf5-140">IT 專業人員強烈偏好記錄檔，以取得非重要的資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-140">IT professionals strongly prefer log files for non-critical information.</span></span> <span data-ttu-id="ffcf5-141">此外，通常會在遠端管理伺服器，且通常會在沒有任何使用者登入的情況下執行，讓通知失效。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-141">Furthermore, servers are often managed remotely and typically run without any users logged on, making notifications ineffective.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="ffcf5-142">設計概念</span><span class="sxs-lookup"><span data-stu-id="ffcf5-142">Design concepts</span></span>

<span data-ttu-id="ffcf5-143">提升良好使用者體驗的有效通知如下：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-143">Effective notifications that promote a good user experience are:</span></span>

-   <span data-ttu-id="ffcf5-144">**非同步。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-144">**Asynchronous.**</span></span> <span data-ttu-id="ffcf5-145">此事件不是使用者目前與 Microsoft Windows 或您的應用程式互動的直接結果。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-145">The event is not an immediate, direct result of users' current interaction with Microsoft Windows or your application.</span></span>
-   <span data-ttu-id="ffcf5-146">**有用。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-146">**Useful.**</span></span> <span data-ttu-id="ffcf5-147">使用者有機會執行工作，或將其行為變更為通知的結果。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-147">There is a reasonable chance that users will perform a task or change their behavior as the result of the notification.</span></span>
-   <span data-ttu-id="ffcf5-148">**相關。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-148">**Relevant.**</span></span> <span data-ttu-id="ffcf5-149">通知會顯示使用者在意且不知道的有用資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-149">The notification displays helpful information that users care about and don't already know.</span></span>
-   <span data-ttu-id="ffcf5-150">**不重要。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-150">**Not critical.**</span></span> <span data-ttu-id="ffcf5-151">通知不是強制回應，而且不需要使用者互動，因此使用者可以自由地忽略它們。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-151">Notifications aren't modal and don't require user interaction, so users can freely ignore them.</span></span>
-   <span data-ttu-id="ffcf5-152">**可行。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-152">**Actionable.**</span></span> <span data-ttu-id="ffcf5-153">針對那些建議執行動作的通知，請按一下通知來起始該動作。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-153">For those notifications that suggest performing an action, that action is initiated by clicking on the notification.</span></span> <span data-ttu-id="ffcf5-154">不過，此動作一律可以延後。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-154">However, the action can always be postponed.</span></span>
-   <span data-ttu-id="ffcf5-155">**適當地呈現。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-155">**Appropriately presented.**</span></span> <span data-ttu-id="ffcf5-156">通知的展示 (持續時間、頻率、文字、圖示和互動) 符合其情況。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-156">The notification's presentation (duration, frequency, text, icon, and interactivity) matches its circumstances.</span></span>
-   <span data-ttu-id="ffcf5-157">**不討厭！**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-157">**Not annoying!**</span></span> <span data-ttu-id="ffcf5-158">輕輕地通知事件使用者並 pestering 活動之間有一條細微的線。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-158">There is a fine line between gently informing users of an event and pestering them.</span></span>

<span data-ttu-id="ffcf5-159">可惜的是，有太多討厭、不當、無用、不相關的通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-159">Unfortunately, there are too many annoying, inappropriate, useless, irrelevant notifications out there.</span></span> <span data-ttu-id="ffcf5-160">請從太可惜的 Windows XP 廳考慮這些通知：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-160">Consider these notifications from the Windows XP Hall of Shame:</span></span>

![<span data-ttu-id="ffcf5-161">[導覽 windows xp] 通知的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-161">screen shot of 'tour windows xp' notification</span></span> ](images/mess-notif-image4.png)

![<span data-ttu-id="ffcf5-162">[未使用的圖示] 通知的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-162">screen shot of 'unused icons' notification</span></span> ](images/mess-notif-image5.png)

![<span data-ttu-id="ffcf5-163">[新增 .net passport] 通知的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-163">screen shot of 'add .net passport' notification</span></span> ](images/mess-notif-image6.png)

<span data-ttu-id="ffcf5-164">在這些範例中，Windows XP root\wmi 嘗試協助使用者進行初始設定。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-164">In these examples, Windows XP is ostensibly attempting to assist users with their initial configuration.</span></span> <span data-ttu-id="ffcf5-165">不過，這些通知會在很有用的時候出現太多，因此會比未經要求的功能公告來得多。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-165">However, these notifications pop up far too often and well after they are useful, so they are little more than unsolicited feature advertisements.</span></span>

## <a name="user-flow-must-be-maintained"></a><span data-ttu-id="ffcf5-166">必須維護使用者流程</span><span class="sxs-lookup"><span data-stu-id="ffcf5-166">User flow must be maintained</span></span>

<span data-ttu-id="ffcf5-167">**在理想的情況下，可以沉浸工作的使用者不會看到您的通知。相反地，只有在流程已中斷時，他們才會看到您的通知。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-167">**Ideally, users immersed in their work won't see your notifications at all. Rather, they'll see your notifications only when their flow is already broken.**</span></span>

<span data-ttu-id="ffcf5-168">在 Flow 中：最佳體驗的心理學，Mihaly Csikszentmihalyi 指出當使用者完全吸收活動時，使用者進入流程狀態，在這段期間內，他們會失去其時間的意義，並感受到絕佳的滿意度。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-168">In Flow: The Psychology of Optimal Experience, Mihaly Csikszentmihalyi says that users enter a flow state when they are fully absorbed in activity during which they lose their sense of time and have feelings of great satisfaction.</span></span>

<span data-ttu-id="ffcf5-169">**有效的通知可協助使用者藉由呈現有用的相關資訊，輕鬆地加以忽略，以協助使用者維護流程。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-169">**Effective notifications help users maintain their flow by presenting useful, relevant information that can easily be ignored.**</span></span> <span data-ttu-id="ffcf5-170">通知會以低金鑰的周邊方式呈現，而不需要互動。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-170">The notifications are presented in a low-key, peripheral way, and they don't require interaction.</span></span>

<span data-ttu-id="ffcf5-171">請勿假設如果通知是 [無模式](glossary.md) 的，則它們不會是討厭的中斷。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-171">Don't assume that if notifications are [modeless](glossary.md) a they can't be an annoying interruption.</span></span> <span data-ttu-id="ffcf5-172">通知不會要求使用者注意，但他們肯定會要求。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-172">Notifications don't demand users' attention, but they certainly request it.</span></span> <span data-ttu-id="ffcf5-173">您可以透過下列方式來中斷使用者流程：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-173">You can break users flow by:</span></span>

-   <span data-ttu-id="ffcf5-174">顯示使用者不在意的通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-174">Displaying notifications that users don't care about.</span></span>
-   <span data-ttu-id="ffcf5-175">太常顯示通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-175">Displaying a notification too often.</span></span>
-   <span data-ttu-id="ffcf5-176">當單一通知已足夠時，使用多個通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-176">Using several notifications when a single notification is sufficient.</span></span>
-   <span data-ttu-id="ffcf5-177">顯示通知時使用音效。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-177">Using sound when displaying a notification.</span></span>

<span data-ttu-id="ffcf5-178">在 Windows 7 中，使用者可以對通知進行終極控制。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-178">In Windows 7, users have ultimate control over notifications.</span></span> <span data-ttu-id="ffcf5-179">**如果使用者發現某個程式的通知太討厭，他們可以選擇隱藏該程式的所有通知。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-179">**If users find that a program's notifications are too annoying, they can choose to suppress all notifications from that program.**</span></span> <span data-ttu-id="ffcf5-180">請確定使用者不會在您的程式中提供有用的相關資訊，並遵循這些指導方針。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-180">Make sure users don't do this to your program by presenting useful, relevant information and following these guidelines.</span></span>

## <a name="notifications-must-be-ignorable"></a><span data-ttu-id="ffcf5-181">通知必須是可忽略的</span><span class="sxs-lookup"><span data-stu-id="ffcf5-181">Notifications must be ignorable</span></span>

<span data-ttu-id="ffcf5-182">**通知不需要立即的使用者動作，使用者可以自由地忽略它們。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-182">**Notifications don't require immediate user action and users can freely ignore them.**</span></span>

<span data-ttu-id="ffcf5-183">開發人員和設計人員通常會想要以使用者無法忽略的方式來呈現他們的通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-183">Developers and designers often want to present their notifications in a way that users can't ignore.</span></span> <span data-ttu-id="ffcf5-184">此目標會完全破壞通知的主要優點，因為這會中斷使用者的流程。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-184">This goal completely undermines the primary benefit of notifications because it would break users' flow.</span></span> <span data-ttu-id="ffcf5-185">如果您的通知會將使用者的注意力放在一起，或想要閱讀這些使用者，您的通知設計就會失敗。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-185">If users are distracted by your notifications or feel obligated to read them, your notification design has failed.</span></span>

<span data-ttu-id="ffcf5-186">**如果您擔心使用者忽略您的通知，請考慮下列事項：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-186">**If you are concerned that users are ignoring your notifications, consider the following:**</span></span>

-   <span data-ttu-id="ffcf5-187">如果您使用的是正確的通知，而不需要立即使用者動作，則讓使用者選擇忽略它們是由設計所設計。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-187">If you are using notifications correctly and they don't require immediate user action, then having users choose to ignore them is by design.</span></span> <span data-ttu-id="ffcf5-188">請勿變更此變更。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-188">Don't change this.</span></span>
-   <span data-ttu-id="ffcf5-189">如果事件需要立即使用者動作，請使用使用者無法忽略的替代使用者介面 (UI) 。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-189">If the event requires immediate user action, use an alternative user interface (UI) that users cannot ignore.</span></span> <span data-ttu-id="ffcf5-190">這是正確的使用者介面嗎？作為替代方案。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-190">See Is this the right user interface? for the alternatives.</span></span>

## <a name="use-progressive-escalation-where-applicable"></a><span data-ttu-id="ffcf5-191">在適用的情況下使用漸進式擴大</span><span class="sxs-lookup"><span data-stu-id="ffcf5-191">Use progressive escalation where applicable</span></span>

<span data-ttu-id="ffcf5-192">如果通知是用於使用者可以在一開始就安全地略過的事件，但必須最後解決此事件，則當情況變得很重要時，應使用替代的 UI。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-192">If a notification is used for an event that users can safely ignore at first, but that must addressed eventually, an alternative UI should be used when the situation becomes critical.</span></span> <span data-ttu-id="ffcf5-193">這項技術稱為漸進式擴大。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-193">This technique is known as progressive escalation.</span></span>

<span data-ttu-id="ffcf5-194">例如，Windows 電源管理系統一開始會透過變更其通知區域圖示來指出電力偏低。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-194">For example, the Windows power management system initially indicates a low battery by simply changing its notification area icon.</span></span>

![<span data-ttu-id="ffcf5-195">顯示電池狀態的六個圖示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-195">screen shot of six icons showing battery status</span></span> ](images/mess-notif-image7.png)

<span data-ttu-id="ffcf5-196">在這些範例中，Windows 電源管理會使用通知區域圖標來通知使用者，電池電力會逐漸降低。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-196">In these examples, Windows power management uses the notification area icon to notify users of progressively lower battery power.</span></span>

<span data-ttu-id="ffcf5-197">當電池電力變低時，Windows 會使用通知向使用者發出電力不足的警告。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-197">As the battery power becomes lower, Windows warns users of weak battery power using a notification.</span></span>

![電力偏低電源通知的螢幕擷取畫面](images/mess-notif-image8.png)

<span data-ttu-id="ffcf5-199">在此範例中，Windows 電源管理會使用通知來告訴使用者其電池電力是否弱。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-199">In this example, Windows power management uses a notification to tell users that their battery power is weak.</span></span>

<span data-ttu-id="ffcf5-200">當使用者仍有數個選項時，就會顯示此通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-200">This notification appears while users still have several options.</span></span> <span data-ttu-id="ffcf5-201">使用者可以插入、變更其電源選項、包裝其工作並關閉電腦，或忽略通知並繼續工作。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-201">Users can plug in, change their power options, wrap up their work and shut down the computer, or ignore the notification and continue working.</span></span> <span data-ttu-id="ffcf5-202">當電池電力繼續清空時，通知的文字和圖示會反映額外的緊急情況。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-202">As the battery power continues to drain, the notification's text and icon reflect the additional urgency.</span></span> <span data-ttu-id="ffcf5-203">不過，一旦電池電力變得較低，使用者就必須立即採取行動，Windows 電源管理會使用強制 [回應訊息框](glossary.md) 來通知使用者。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-203">However, once the battery power becomes so low that users must act immediately, Windows power management notifies users using a [modal](glossary.md) message box.</span></span>

![嚴重電力偏低警告的螢幕擷取畫面](images/mess-notif-image9.png)

<span data-ttu-id="ffcf5-205">在此範例中，Windows 電源管理會使用強制回應訊息框來通知使用者電力偏低的情況。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-205">In this example, Windows power management uses a modal message box to notify users of critically low battery power.</span></span>

<span data-ttu-id="ffcf5-206">**如果您只進行三件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-206">**If you do only three things...**</span></span>

1.  <span data-ttu-id="ffcf5-207">只有在您真的需要時，才使用通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-207">Use notifications only if you really need to.</span></span> <span data-ttu-id="ffcf5-208">當您顯示通知時，可能會中斷使用者或甚至討厭使用者。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-208">When you display a notification, you are potentially interrupting users or even annoying them.</span></span> <span data-ttu-id="ffcf5-209">請確定中斷的對齊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-209">Make sure that interruption is justified.</span></span>
2.  <span data-ttu-id="ffcf5-210">針對不需要立即使用者動作的非重大事件或情況，請使用通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-210">Use notifications for non-critical events or situations that don't require immediate user action.</span></span> <span data-ttu-id="ffcf5-211">對於需要立即執行使用者動作的重大事件或情況，請使用替代的 UI (例如) 的強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-211">For critical events or situations that require immediate user action, use an alternative UI (such as a modal dialog box).</span></span>
3.  <span data-ttu-id="ffcf5-212">如果您使用通知，請讓它成為良好的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-212">If you use notifications, make it a good user experience.</span></span> <span data-ttu-id="ffcf5-213">請勿嘗試強制使用者查看您的通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-213">Don't try to force users to see your notifications.</span></span> <span data-ttu-id="ffcf5-214">如果使用者可以沉浸他們的工作沒有看到您的通知，表示您的設計是不錯的。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-214">If users are so immersed in their work that they don't see your notifications, your design is good.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="ffcf5-215">使用模式</span><span class="sxs-lookup"><span data-stu-id="ffcf5-215">Usage patterns</span></span>

<span data-ttu-id="ffcf5-216">通知有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-216">Notifications have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffcf5-217"><strong>動作成功</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-217"><strong>Action success</strong></span></span><br/> <span data-ttu-id="ffcf5-218">當非同步使用者起始的動作順利完成時，通知使用者。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-218">Notifies users when an asynchronous, user initiated action completes successfully.</span></span> <br/></td>
<td><span data-ttu-id="ffcf5-219"><strong>正確：</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-219"><strong>Correct:</strong></span></span><br/> <img src="images/mess-notif-image10.png" alt="Screen shot of balloon showing successful updates " /><br/> <span data-ttu-id="ffcf5-220">在此範例中，Windows Update 會在電腦已成功更新時通知使用者。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-220">In this example, Windows Update notifies users when their computer has been updated successfully.</span></span><br/> <span data-ttu-id="ffcf5-221"><strong>不正確：</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-221"><strong>Incorrect:</strong></span></span><br/> <img src="images/mess-notif-image11.png" alt="Screen shot of balloon showing file check complete " /><br/> <span data-ttu-id="ffcf5-222">在此範例中，當資料檔案檢查完成時，Microsoft Outlook 會通知使用者。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-222">In this example, Microsoft Outlook notifies users when a data file check is complete.</span></span> <span data-ttu-id="ffcf5-223">使用者現在應該怎麼做？</span><span class="sxs-lookup"><span data-stu-id="ffcf5-223">What are users supposed to do now?</span></span> <span data-ttu-id="ffcf5-224">為什麼要警告使用者成功完成？</span><span class="sxs-lookup"><span data-stu-id="ffcf5-224">And why warn users about successful completion?</span></span><br/> <span data-ttu-id="ffcf5-225"><strong>顯示時機：</strong> 非同步工作完成時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-225"><strong>Show when:</strong> Upon completion of an asynchronous task.</span></span> <span data-ttu-id="ffcf5-226">只有在使用者可能等候完成或最近失敗之後，才通知使用者成功的動作。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-226">Notify users of successful actions only if they are likely to be waiting for completion, or after recent failures.</span></span><br/> <span data-ttu-id="ffcf5-227"><strong>示範如何：</strong> 使用即時選項，在使用者執行全螢幕應用程式或未主動使用其電腦時，不會將這些通知排入佇列。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-227"><strong>Show how:</strong> Use the real-time option so that these notifications aren't queued when users are running a full-screen application or aren't actively using their computer.</span></span><br/> <span data-ttu-id="ffcf5-228"><strong>顯示頻率：</strong> 一旦。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-228"><strong>Show how often:</strong> Once.</span></span><br/> <span data-ttu-id="ffcf5-229"><strong>干擾因素：</strong> 如果因為最近的失敗而不預期成功，則會在發生重大或高度異常的失敗之後成功，讓使用者需要額外的意見反應，或使用者等候完成;如果沒有，則為 high。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-229"><strong>Annoyance factor:</strong> Low if success isn't expected due to recent failures, success is after a critical or highly unusual failure so user needs additional feedback, or user is waiting for completion; high if not.</span></span><br/> <span data-ttu-id="ffcf5-230"><strong>替代方案：</strong> 在 &quot; &quot; 執行作業時，在通知區域中顯示圖示 (或變更現有的圖示) 來提供意見反應; 移除圖示 (或還原先前的圖示) 作業完成時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-230"><strong>Alternatives:</strong> Give feedback &quot;on demand&quot; by displaying an icon (or changing an existing icon) in the notification area while the operation is being performed; remove the icon (or restore the previous icon) when the operation is complete.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffcf5-231"><strong>動作失敗</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-231"><strong>Action failure</strong></span></span><br/> <span data-ttu-id="ffcf5-232">在非同步、使用者起始的動作失敗時通知使用者。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-232">Notifies users when an asynchronous, user initiated action fails.</span></span> <br/></td>
<td><span data-ttu-id="ffcf5-233"><strong>正確：</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-233"><strong>Correct:</strong></span></span><br/> <img src="images/mess-notif-image12.png" alt="Screen shot of notification of failure to install " /><br/> <span data-ttu-id="ffcf5-234">在此範例中，Windows 啟用會通知使用者失敗。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-234">In this example, Windows activation notifies users of failure.</span></span><br/> <span data-ttu-id="ffcf5-235"><strong>不正確：</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-235"><strong>Incorrect:</strong></span></span><br/> <img src="images/mess-notif-image13.png" alt="Screen shot of notification of failure to update " /><br/> <span data-ttu-id="ffcf5-236">在此範例中，Microsoft Outlook 用來通知使用者，他們不太可能在意這些錯誤。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-236">In this example, Microsoft Outlook used to notify users of a failure that they are unlikely to care about.</span></span><br/> <span data-ttu-id="ffcf5-237"><strong>顯示時機：</strong> 非同步工作失敗時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-237"><strong>Show when:</strong> Upon failure of an asynchronous task.</span></span><br/> <span data-ttu-id="ffcf5-238"><strong>顯示頻率：</strong> 一旦。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-238"><strong>Show how often:</strong> Once.</span></span><br/> <span data-ttu-id="ffcf5-239"><strong>干擾因素：</strong> 如果有用且相關，則為 Low;如果問題會立即自行解決或使用者不在意，則為高。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-239"><strong>Annoyance factor:</strong> Low if useful and relevant; high if the problem will immediately resolve itself or users otherwise don't care.</span></span><br/> <span data-ttu-id="ffcf5-240"><strong>替代方案：</strong> 如果使用者必須立即處理失敗，請使用強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-240"><strong>Alternatives:</strong> Use a modal dialog box if users must address the failure immediately.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffcf5-241"><strong>非重大系統事件</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-241"><strong>Non-critical system event</strong></span></span><br/> <span data-ttu-id="ffcf5-242">通知使用者很重要的系統事件或狀態，而且可以安全地忽略（至少暫時）。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-242">Notifies users of significant system events or status that can be safely ignored, at least temporarily.</span></span> <br/></td>
<td><img src="images/mess-notif-image8.png" alt="Screen shot of notification of low battery power " /><br/> <span data-ttu-id="ffcf5-243">在此範例中，Windows 會警告使用者電池電力偏低，但仍有足夠的時間來採取行動。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-243">In this example, Windows warns users of low battery power, but there is still plenty of time before they have take action.</span></span><br/> <span data-ttu-id="ffcf5-244"><strong>顯示時機：</strong> 當事件發生且使用者為作用中狀態，或條件持續存在時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-244"><strong>Show when:</strong> When an event occurs and the user is active, or a condition continues to exist.</span></span> <span data-ttu-id="ffcf5-245">如果發生問題，請在問題解決後立即移除目前顯示的通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-245">If resulting from a problem, remove currently displayed notifications immediately once the problem is resolved.</span></span> <span data-ttu-id="ffcf5-246">如同動作通知，只有在使用者可能等候事件或最近失敗之後，才通知使用者系統事件是否成功。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-246">As with action notifications, notify users of successful system events only if users are likely to be waiting for the event, or after recent failures.</span></span><br/> <span data-ttu-id="ffcf5-247"><strong>顯示頻率：</strong> 第一次發生事件時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-247"><strong>Show how often:</strong> Once when the event first occurs.</span></span> <span data-ttu-id="ffcf5-248">如果這是由使用者需要解決的問題所產生，請一天重新顯示一次。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-248">If this results from a problem that users need to solve, redisplay once a day.</span></span><br/> <span data-ttu-id="ffcf5-249"><strong>干擾因素：</strong> 低，只要通知未顯示太頻繁。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-249"><strong>Annoyance factor:</strong> Low, as long as the notification isn't displayed too often.</span></span><br/> <span data-ttu-id="ffcf5-250"><strong>替代方案：</strong> 如果使用者最終必須解決問題，請在解析變成強制性時，使用漸進式擴大以最後顯示模式對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-250"><strong>Alternatives:</strong> If users must eventually resolve a problem, use progressive escalation by ultimately displaying a modal dialog box when resolution becomes mandatory.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffcf5-251"><strong>選用的使用者工作</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-251"><strong>Optional user task</strong></span></span><br/> <span data-ttu-id="ffcf5-252">通知使用者其應該執行的非同步工作。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-252">Notifies users of asynchronous tasks they should perform.</span></span> <span data-ttu-id="ffcf5-253">無論是選擇性或必要，工作都可以安全地延後。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-253">Whether optional or required, the task can be safely postponed.</span></span> <br/></td>
<td><img src="images/mess-notif-image14.png" alt="Screen shot of notification of available updates " /><br/> <span data-ttu-id="ffcf5-254">在此範例中，Windows Update 會通知使用者有新的安全性更新。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-254">In this example, Windows Update is notifying users of a new security update.</span></span><br/> <span data-ttu-id="ffcf5-255"><strong>顯示時機：</strong> 當您決定執行工作的需求，且使用者為作用中狀態時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-255"><strong>Show when:</strong> When the need to perform a task is determined and the user is active.</span></span><br/> <span data-ttu-id="ffcf5-256"><strong>顯示頻率：</strong> 一天一次，最多三次。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-256"><strong>Show how often:</strong> Once a day for a maximum of three times.</span></span><br/> <span data-ttu-id="ffcf5-257"><strong>干擾因素：</strong> 低，只要使用者將工作視為重要，且通知未顯示太頻繁。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-257"><strong>Annoyance factor:</strong> Low, as long as users consider the task important and the notification isn't displayed too often.</span></span><br/> <span data-ttu-id="ffcf5-258"><strong>替代方案：</strong> 如果使用者最終必須執行此工作，請在工作變成強制執行時，使用漸進式擴大以最後顯示模式對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-258"><strong>Alternatives:</strong> If users must eventually perform the task, use progressive escalation by ultimately displaying a modal dialog box when the task becomes mandatory.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffcf5-259"><strong>僅供參考</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-259"><strong>FYI</strong></span></span><br/> <span data-ttu-id="ffcf5-260">通知使用者可能有用的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-260">Notifies users of potentially useful, relevant information.</span></span> <span data-ttu-id="ffcf5-261">如果使用者是選擇性的，且使用者加入宣告，您可以通知使用者有關臨界相關性的資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-261">You can notify users of information of marginal relevance if it is optional and users opt in.</span></span> <br/></td>
<td><span data-ttu-id="ffcf5-262"><strong>正確：</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-262"><strong>Correct:</strong></span></span><br/> <img src="images/mess-notif-image15.png" alt="Screen shot of notification of new e-mail message " /><br/> <span data-ttu-id="ffcf5-263">在此範例中，當收到新的電子郵件訊息時，就會通知使用者。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-263">In this example, users are notified when a new e-mail message is received.</span></span><br/> <span data-ttu-id="ffcf5-264"><strong>正確：</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-264"><strong>Correct:</strong></span></span><br/> <img src="images/mess-notif-image16.png" alt="Screen shot of notification of contact signed in " /><br/> <span data-ttu-id="ffcf5-265">在此範例中，當連絡人上線，而且他們選擇接收此選擇性資訊時，會通知使用者。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-265">In this example, users are notified when contacts come online and they chose to receive this optional information.</span></span><br/> <span data-ttu-id="ffcf5-266"><strong>不正確：</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-266"><strong>Incorrect:</strong></span></span><br/> <img src="images/mess-notif-image17.png" alt="Screen shot of notification for faster performance " /><br/> <span data-ttu-id="ffcf5-267">在此範例中，只有當使用者已安裝高速 USB 埠時，此資訊才會很有用。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-267">In this example, the information is useful only if the user already has high-speed USB ports installed.</span></span> <span data-ttu-id="ffcf5-268">否則，使用者不太可能做任何不同的結果。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-268">Otherwise, the user isn't likely to do anything different as the result of it.</span></span><br/> <span data-ttu-id="ffcf5-269"><strong>顯示時機：</strong> 當觸發事件發生時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-269"><strong>Show when:</strong> When the triggering event occurs.</span></span><br/> <span data-ttu-id="ffcf5-270"><strong>示範如何：</strong> 使用即時選項，在使用者執行全螢幕應用程式或未主動使用其電腦時，不會將這些通知排入佇列。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-270"><strong>Show how:</strong> Use the real-time option so that these notifications aren't queued when users are running a full-screen application or aren't actively using their computer.</span></span><br/> <span data-ttu-id="ffcf5-271"><strong>顯示頻率：</strong> 一旦。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-271"><strong>Show how often:</strong> Once.</span></span><br/> <span data-ttu-id="ffcf5-272"><strong>干擾因素：</strong> 中至高，視使用者對實用性和相關性的認知而定。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-272"><strong>Annoyance factor:</strong> Medium to high, depending upon users' perception of usefulness and relevance.</span></span> <span data-ttu-id="ffcf5-273">如果使用者感興趣的機率很低，則不建議使用。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-273">Not recommended if there is a low probability of user interest.</span></span><br/> <span data-ttu-id="ffcf5-274"><strong>替代方案：</strong> 不要通知使用者。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-274"><strong>Alternatives:</strong> Don't notify users.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffcf5-275"><strong>功能公告</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-275"><strong>Feature advertisement</strong></span></span><br/> <span data-ttu-id="ffcf5-276">通知使用者新安裝、未使用的系統或應用程式功能。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-276">Notifies users of newly installed, unused system or application features.</span></span><br/></td>
<td><span data-ttu-id="ffcf5-277"><strong>請勿使用功能公告的通知！</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-277"><strong>Don't use notifications for feature advertisements!</strong></span></span> <span data-ttu-id="ffcf5-278">相反地，請使用另一種方式來讓功能可供探索，例如：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-278">Instead, use another way to make the feature discoverable, such as:</span></span> <br/>
<ul>
<li><span data-ttu-id="ffcf5-279">設計在需要時更容易在內容中探索的功能。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-279">Design the feature to be easier to discover in contexts where it is needed.</span></span></li>
<li><span data-ttu-id="ffcf5-280">請勿做任何特殊的動作，讓使用者自行探索功能。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-280">Don't do anything special and let users discover the feature on their own.</span></span></li>
</ul><span data-ttu-id="ffcf5-281">
<strong>不正確：</strong></span><span class="sxs-lookup"><span data-stu-id="ffcf5-281">
<strong>Incorrect:</strong></span></span><br/> <img src="images/mess-notif-image4.png" alt="Screen shot of notification of new features " /><br/> <span data-ttu-id="ffcf5-282">請勿使用功能公告的通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-282">Don't use notifications for feature advertisements.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="ffcf5-283">指導方針</span><span class="sxs-lookup"><span data-stu-id="ffcf5-283">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="ffcf5-284">一般</span><span class="sxs-lookup"><span data-stu-id="ffcf5-284">General</span></span>

-   <span data-ttu-id="ffcf5-285">**選取以其使用方式為基礎的通知模式。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-285">**Select the notification pattern based on its usage.**</span></span> <span data-ttu-id="ffcf5-286">如需每個使用模式的說明，請參閱上一個表格。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-286">For a description of each usage pattern, see the previous table.</span></span>
-   <span data-ttu-id="ffcf5-287">**請勿在初始 Windows 體驗期間使用任何通知。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-287">**Don't use any notifications during the initial Windows experience.**</span></span> <span data-ttu-id="ffcf5-288">為了改善它的第一個經驗，Windows 7 會隱藏在前幾小時的使用量中顯示的所有通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-288">To improve its first experience, Windows 7 suppresses all notifications displayed during the first few hours of usage.</span></span> <span data-ttu-id="ffcf5-289">設計您的程式，假設使用者不會看到任何這類通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-289">Design your program assuming users won't see any such notifications.</span></span>

### <a name="what-to-notify"></a><span data-ttu-id="ffcf5-290">要通知的內容</span><span class="sxs-lookup"><span data-stu-id="ffcf5-290">What to notify</span></span>

-   <span data-ttu-id="ffcf5-291">**請勿通知成功的作業，但在下列情況除外：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-291">**Don't notify of successful operations, except in the following circumstances:**</span></span>
    -   <span data-ttu-id="ffcf5-292">**安全性。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-292">**Security.**</span></span> <span data-ttu-id="ffcf5-293">使用者將安全性作業視為最重要性，因此請通知使用者安全性作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-293">Users consider security operations to be of the highest importance, so notify users of successful security operations.</span></span>
    -   <span data-ttu-id="ffcf5-294">**最近的失敗。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-294">**Recent failure.**</span></span> <span data-ttu-id="ffcf5-295">如果使用者立即失敗，就不會成功授與使用者成功的作業，因此請在作業最近失敗時通知使用者成功。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-295">Users don't take successful operations for granted if they were failing immediately before, so notify users of success when the operation was recently failing.</span></span>
    -   <span data-ttu-id="ffcf5-296">**避免不便。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-296">**Prevent inconvenience.**</span></span> <span data-ttu-id="ffcf5-297">在這麼做時回報成功的作業，可能會避免給帶來不便的使用者。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-297">Report successful operations when doing so might avoid inconveniencing users.</span></span> <span data-ttu-id="ffcf5-298">因此，在執行成功的作業時通知使用者，例如，當作業的時間過長，或比預期更晚或更晚完成時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-298">Consequently, notify users when a successful operation is performed in an unexpected way, such as when an operation is lengthy or completes earlier or later than expected.</span></span>
-   <span data-ttu-id="ffcf5-299">**在其他情況下，則不會提供成功的意見反應，或提供意見反應「視需要」。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-299">**In other circumstances, either give no feedback for success or give feedback "on demand."**</span></span> <span data-ttu-id="ffcf5-300">假設使用者已成功執行授與的作業。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-300">Assume that users take successful operations for granted.</span></span> <span data-ttu-id="ffcf5-301">當作業執行時，您可以在通知區域中顯示圖示 (或變更現有的圖示) 來提供意見反應，並在作業完成時移除圖示 (或還原先前的圖示) 。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-301">You can give feedback on demand by displaying an icon (or changing an existing icon) in the notification area while the operation is being performed, and removing the icon (or restoring the previous icon) when the operation is complete.</span></span>
-   <span data-ttu-id="ffcf5-302">針對僅供參考模式， **如果使用者可以繼續正常運作，或不太可能執行與通知結果不同的動作，則不會提供通知。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-302">For the FYI pattern, **don't give a notification if users can continue to work normally or are unlikely to do anything different as the result of the notification.**</span></span>

    <span data-ttu-id="ffcf5-303">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-303">**Incorrect:**</span></span>

    ![<span data-ttu-id="ffcf5-304">通知的螢幕擷取畫面，以提供更快速的效能</span><span class="sxs-lookup"><span data-stu-id="ffcf5-304">screen shot of notification for faster performance</span></span> ](images/mess-notif-image17.png)

    <span data-ttu-id="ffcf5-305">在此範例中，只有當使用者已安裝埠時，資訊才有説明。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-305">In this example, the information is useful only if the user already has the ports installed.</span></span> <span data-ttu-id="ffcf5-306">否則，使用者不太可能做任何不同的結果。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-306">Otherwise, the user isn't likely to do anything different as the result of it.</span></span>

    -   <span data-ttu-id="ffcf5-307">例外狀況： **如果使用者是選擇性的，且使用者加入宣告，您可以通知使用者有疑問的相關性資訊。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-307">Exception: **You can notify users of information of questionable relevance if it is optional and users opt in.**</span></span>

        <span data-ttu-id="ffcf5-308">**正確：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-308">**Correct:**</span></span>

        ![<span data-ttu-id="ffcf5-309">已登入的連絡人通知螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-309">screen shot of notification of contact signed in</span></span> ](images/mess-notif-image16.png)

        <span data-ttu-id="ffcf5-310">在此範例中，當連絡人上線，而且他們選擇接收此選擇性資訊時，會通知使用者。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-310">In this example, users are notified when contacts come online and they chose to receive this optional information.</span></span>

-   <span data-ttu-id="ffcf5-311">針對非關鍵性的系統事件和僅供參考模式，請 **使用單一事件的完整通知。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-311">For the non-critical system event and FYI patterns, **use complete notifications for a single event.**</span></span> <span data-ttu-id="ffcf5-312">不要提供數個部分。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-312">Don't present several partial ones.</span></span>

    <span data-ttu-id="ffcf5-313">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-313">**Incorrect:**</span></span>

    ![<span data-ttu-id="ffcf5-314">「找到新硬體」通知的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-314">screen shot of 'found new hardware' notifications</span></span> ](images/mess-notif-image18.png)

    <span data-ttu-id="ffcf5-315">這些範例只會顯示 Windows XP 在使用者連接特定 USB 鍵盤時所顯示的八個通知中的四個，每個通知都會以累加方式呈現詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-315">These examples show just four of the eight notifications that were displayed by Windows XP when a user attaches a specific USB keyboard, each presenting incrementally more information.</span></span>

    <span data-ttu-id="ffcf5-316">**正確：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-316">**Correct:**</span></span>

    ![<span data-ttu-id="ffcf5-317">安裝狀態通知的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-317">screen shot of notifications of install status</span></span> ](images/mess-notif-image19.png)

    <span data-ttu-id="ffcf5-318">在此範例中，連接 USB 鍵盤會產生兩個完整的通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-318">In this example, attaching a USB keyboard results in two complete notifications.</span></span>

### <a name="when-to-notify"></a><span data-ttu-id="ffcf5-319">通知時機</span><span class="sxs-lookup"><span data-stu-id="ffcf5-319">When to notify</span></span>

-   <span data-ttu-id="ffcf5-320">**根據其設計模式顯示通知：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-320">**Display a notification based on its design pattern:**</span></span>



|                                      |                                                                                                                                                                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffcf5-321">**模式**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-321">**Pattern**</span></span><br/>               | <span data-ttu-id="ffcf5-322">**通知時機**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-322">**When to notify**</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="ffcf5-323">動作成功</span><span class="sxs-lookup"><span data-stu-id="ffcf5-323">Action success</span></span><br/>            | <span data-ttu-id="ffcf5-324">非同步工作完成時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-324">Upon completion of an asynchronous task.</span></span> <span data-ttu-id="ffcf5-325">只有在使用者可能等候完成或最近失敗之後，才通知使用者成功的動作。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-325">Notify users of successful actions only if they are likely to be waiting for completion, or after recent failures.</span></span><br/>                                             |
| <span data-ttu-id="ffcf5-326">動作失敗</span><span class="sxs-lookup"><span data-stu-id="ffcf5-326">Action failure</span></span><br/>            | <span data-ttu-id="ffcf5-327">非同步工作失敗時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-327">Upon failure of an asynchronous task.</span></span><br/>                                                                                                                                                                   |
| <span data-ttu-id="ffcf5-328">非重大系統事件</span><span class="sxs-lookup"><span data-stu-id="ffcf5-328">Non-critical system event</span></span><br/> | <span data-ttu-id="ffcf5-329">當事件發生且使用者為作用中狀態，或條件持續存在時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-329">When an event occurs and the user is active, or the condition continues to exist.</span></span> <span data-ttu-id="ffcf5-330">如果發生問題，請在問題解決後立即移除目前顯示的通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-330">If this results from a problem, remove the currently displayed notification immediately once the problem is resolved.</span></span><br/> |
| <span data-ttu-id="ffcf5-331">選用的使用者工作</span><span class="sxs-lookup"><span data-stu-id="ffcf5-331">Optional user task</span></span><br/>        | <span data-ttu-id="ffcf5-332">當您決定執行工作的需求，且使用者為作用中狀態時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-332">When the need to perform a task is determined and the user is active.</span></span><br/>                                                                                                                                   |
| <span data-ttu-id="ffcf5-333">僅供參考</span><span class="sxs-lookup"><span data-stu-id="ffcf5-333">FYI</span></span><br/>                       | <span data-ttu-id="ffcf5-334">當觸發事件發生時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-334">When the triggering event occurs.</span></span><br/>                                                                                                                                                                       |



 

-   <span data-ttu-id="ffcf5-335">針對動作失敗模式， **如果問題可能在幾秒鐘內自行修正，請將失敗通知延遲一段適當的時間。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-335">For the action failure pattern, **if the problem might correct itself within seconds, delay the failure notification for an appropriate amount of time.**</span></span> <span data-ttu-id="ffcf5-336">如果問題自行修正，請報告 nothing。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-336">If the problem corrects itself, report nothing.</span></span> <span data-ttu-id="ffcf5-337">只有在經過一段時間之後才通知，這會明顯失敗。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-337">Notify only after enough time has passed that the failure is noticeable.</span></span> <span data-ttu-id="ffcf5-338">如果您提前回報太早，最有可能的使用者不會注意到回報的問題，但是會注意到不必要的通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-338">If you report too early, most likely users won't notice the problem reported, but they will notice the unnecessary notification.</span></span>

<span data-ttu-id="ffcf5-339">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-339">**Incorrect:**</span></span>

![<span data-ttu-id="ffcf5-340">沒有網路連接通知的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-340">screen shot of no network connection notification</span></span> ](images/mess-notif-image20.png)

<span data-ttu-id="ffcf5-341">其後緊接著：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-341">When immediately followed by:</span></span>

![<span data-ttu-id="ffcf5-342">連接成功通知的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-342">screen shot of connection successful notification</span></span> ](images/mess-notif-image21.png)

<span data-ttu-id="ffcf5-343">在此範例中，在 Windows Vista 中，沒有無線連線的通知會提早出現，因為它通常會緊接在正常連線的通知中。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-343">In this example, in Windows Vista the notification of no wireless connectivity is premature because it is often immediately followed by a notification of good connectivity.</span></span>

-   <span data-ttu-id="ffcf5-344">針對「動作成功」和「僅供參考」模式，使用即時選項，讓當使用者執行全螢幕應用程式或未主動使用其電腦時 **，過時通知不會排入佇列** 。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-344">For the action success and FYI patterns, **use the real-time option so that stale notifications aren't queued** when users are running a full-screen application or aren't actively using their computer.</span></span>
-   <span data-ttu-id="ffcf5-345">針對非關鍵性的系統事件模式， **不會產生通知風暴的可能性，方法是將事件系結至已知事件（例如使用者登入）。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-345">For the non-critical system event pattern, **don't create the potential for notification storms by staggering events tied to well-known events such as user logon.**</span></span> <span data-ttu-id="ffcf5-346">相反地，請將事件系結至事件之後的某個時間週期。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-346">Instead, tie the event to some time period after the event.</span></span> <span data-ttu-id="ffcf5-347">例如，您可以在使用者登入後，提醒使用者註冊您的產品五分鐘。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-347">For example, you could remind users to register your product five minutes after user logon.</span></span>

### <a name="how-long-to-notify"></a><span data-ttu-id="ffcf5-348">通知的時間長度</span><span class="sxs-lookup"><span data-stu-id="ffcf5-348">How long to notify</span></span>

<span data-ttu-id="ffcf5-349">在 Windows Vista （含）以後版本中，系統會在9秒的固定期間內顯示通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-349">In Windows Vista and later, notifications are displayed for a fixed duration of 9 seconds.</span></span>

### <a name="how-often-to-notify"></a><span data-ttu-id="ffcf5-350">通知的頻率</span><span class="sxs-lookup"><span data-stu-id="ffcf5-350">How often to notify</span></span>

-   <span data-ttu-id="ffcf5-351">**顯示通知的次數取決於其設計模式：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-351">**The number of times to display a notification is based on its design pattern:**</span></span>



|                                      |                                                                                                                             |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffcf5-352">**模式**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-352">**Pattern**</span></span><br/>               | <span data-ttu-id="ffcf5-353">**通知的頻率**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-353">**How often to notify**</span></span><br/>                                                                                          |
| <span data-ttu-id="ffcf5-354">動作成功</span><span class="sxs-lookup"><span data-stu-id="ffcf5-354">Action success</span></span><br/>            | <span data-ttu-id="ffcf5-355">一次。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-355">Once.</span></span><br/>                                                                                                            |
| <span data-ttu-id="ffcf5-356">動作失敗</span><span class="sxs-lookup"><span data-stu-id="ffcf5-356">Action failure</span></span><br/>            | <span data-ttu-id="ffcf5-357">一次。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-357">Once.</span></span><br/>                                                                                                            |
| <span data-ttu-id="ffcf5-358">非重大系統事件</span><span class="sxs-lookup"><span data-stu-id="ffcf5-358">Non-critical system event</span></span><br/> | <span data-ttu-id="ffcf5-359">第一次發生事件時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-359">Once when the event first occurs.</span></span> <span data-ttu-id="ffcf5-360">如果這是由使用者需要解決的問題所產生，請一天重新顯示一次。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-360">If this results from a problem that users need to solve, redisplay once a day.</span></span><br/> |
| <span data-ttu-id="ffcf5-361">選用的使用者工作</span><span class="sxs-lookup"><span data-stu-id="ffcf5-361">Optional user task</span></span><br/>        | <span data-ttu-id="ffcf5-362">一天一次，最多三次。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-362">Once a day for a maximum of three times.</span></span><br/>                                                                         |
| <span data-ttu-id="ffcf5-363">僅供參考</span><span class="sxs-lookup"><span data-stu-id="ffcf5-363">FYI</span></span><br/>                       | <span data-ttu-id="ffcf5-364">一次。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-364">Once.</span></span><br/>                                                                                                            |



 

-   <span data-ttu-id="ffcf5-365">**若為選擇性的使用者工作，請不要嘗試持續顯示通知，以 pester 使用者進入提交。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-365">**For optional user tasks, don't try to pester users into submission by constantly displaying notifications.**</span></span> <span data-ttu-id="ffcf5-366">如果需要此工作，請立即顯示模式對話方塊，而不是使用通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-366">If the task is required, display a modal dialog box immediately instead of using notifications.</span></span>

### <a name="notification-escalation"></a><span data-ttu-id="ffcf5-367">通知擴大</span><span class="sxs-lookup"><span data-stu-id="ffcf5-367">Notification escalation</span></span>

-   <span data-ttu-id="ffcf5-368">**請勿假設使用者會看到您的通知。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-368">**Don't assume that users will see your notifications.**</span></span> <span data-ttu-id="ffcf5-369">使用者將不會看到它們的時機：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-369">Users won't see them when:</span></span>
    -   <span data-ttu-id="ffcf5-370">它們會在其工作中可以沉浸。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-370">They are immersed in their work.</span></span>
    -   <span data-ttu-id="ffcf5-371">他們不會注意到。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-371">They aren't paying attention.</span></span>
    -   <span data-ttu-id="ffcf5-372">它們不在電腦上。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-372">They are away from their computer.</span></span>
    -   <span data-ttu-id="ffcf5-373">它們正在執行全螢幕應用程式。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-373">They are running a full-screen application.</span></span>
    -   <span data-ttu-id="ffcf5-374">他們的系統管理員已關閉其電腦的所有通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-374">Their administrator has turned off all notifications for their computer.</span></span>
-   <span data-ttu-id="ffcf5-375">**如果使用者最終必須採取某種動作，請使用漸進式擴大** 來顯示使用者無法忽略的替代 UI。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-375">**If users must eventually take some kind of action, use progressive escalation** to display an alternative UI that users cannot ignore.</span></span>

### <a name="interaction"></a><span data-ttu-id="ffcf5-376">互動</span><span class="sxs-lookup"><span data-stu-id="ffcf5-376">Interaction</span></span>

-   <span data-ttu-id="ffcf5-377">**當下列情況時，請按一下通知：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-377">**Make notifications clickable when:**</span></span>
    -   <span data-ttu-id="ffcf5-378">**使用者應執行動作。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-378">**Users should perform an action.**</span></span> <span data-ttu-id="ffcf5-379">按一下通知應該會顯示一個視窗，讓使用者可以在其中執行動作。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-379">Clicking the notification should display a window in which users can perform the action.</span></span> <span data-ttu-id="ffcf5-380">這是動作失敗和選擇性使用者工作設計模式的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-380">This approach is preferred for the action failure and optional user task design patterns.</span></span>
    -   <span data-ttu-id="ffcf5-381">**使用者可能會想要查看詳細資訊。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-381">**Users may want to see more information.**</span></span> <span data-ttu-id="ffcf5-382">按一下通知應該會顯示一個視窗，讓使用者可以在其中查看其他資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-382">Clicking the notification should display a window in which users can view additional information.</span></span>
-   <span data-ttu-id="ffcf5-383">**當使用者按一下執行動作時，一律會顯示視窗。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-383">**Always display a window when users click to perform an action.**</span></span> <span data-ttu-id="ffcf5-384">按一下 [直接執行動作]。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-384">Don't have clicking perform an action directly.</span></span>
-   <span data-ttu-id="ffcf5-385">**按一下以顯示詳細資訊，應該一律顯示詳細資訊。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-385">**Clicking to show more information should always show more information.**</span></span> <span data-ttu-id="ffcf5-386">請勿只改寫已在通知中的資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-386">Don't just rephrase the information already in the notification.</span></span>

### <a name="icons"></a><span data-ttu-id="ffcf5-387">圖示</span><span class="sxs-lookup"><span data-stu-id="ffcf5-387">Icons</span></span>

-   <span data-ttu-id="ffcf5-388">**針對動作失敗模式，請使用標準錯誤圖示。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-388">**For the action failure pattern, use the standard error icon.**</span></span>
-   <span data-ttu-id="ffcf5-389">**若為非關鍵性的系統事件模式，請使用標準警告圖示。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-389">**For the non-critical system event patterns, use the standard warning icon.**</span></span>
-   <span data-ttu-id="ffcf5-390">**針對其他模式，請使用圖示來顯示** 與主旨相關的物件，例如安全性的防護罩或電力的電池。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-390">**For other patterns, use icons showing objects that relate to or suggest the subject**, such as a shield for security or a battery for power.</span></span>
-   <span data-ttu-id="ffcf5-391">**如果您的目標使用者將辨識這些圖示，且沒有更好的替代方案，請根據您的應用程式或公司商標使用這些圖示。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-391">**Use icons based on your application or company branding if your target users will recognize them and there is no better alternative.**</span></span>
-   <span data-ttu-id="ffcf5-392">針對漸進式擴大，請 **考慮在情況變得更緊急的情況下，使用具有逐漸 emphatic 外觀的圖示。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-392">For progressive escalation, **consider using icons with a progressively more emphatic appearance as the situation becomes more urgent.**</span></span>
-   <span data-ttu-id="ffcf5-393">**請勿使用標準資訊圖示。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-393">**Don't use the standard information icon.**</span></span> <span data-ttu-id="ffcf5-394">通知是資訊不需要說。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-394">That notifications are information goes without saying.</span></span>
-   <span data-ttu-id="ffcf5-395">**在下列情況中，請考慮使用大型圖示 (32x32 圖元) ：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-395">**Consider using large icons (32x32 pixels) when:**</span></span>
    -   <span data-ttu-id="ffcf5-396">使用者將快速理解此圖示，而不是文字。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-396">Users will quickly comprehend the icon rather than the text.</span></span>
    -   <span data-ttu-id="ffcf5-397">大型圖示比標準的16x16 圖元圖示更清楚且有效率地傳達其意義。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-397">The large icons convey their meaning more clearly and effectively than the standard 16x16 pixel icons.</span></span>
    -   <span data-ttu-id="ffcf5-398">圖示使用 [Aero 樣式](vis-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-398">The icon uses the [Aero-style](vis-icons.md).</span></span>

![<span data-ttu-id="ffcf5-399">[重要訊息] 通知的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-399">screen shot of 'important messages' notification</span></span> ](images/mess-notif-image22.png)

<span data-ttu-id="ffcf5-400">在此範例中，使用者可以快速理解通知的本質，並在大型圖示上一目了然。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-400">In this example, users can quickly comprehend the nature of the notification with a glance at the large icon.</span></span>

### <a name="notification-queuing"></a><span data-ttu-id="ffcf5-401">通知佇列</span><span class="sxs-lookup"><span data-stu-id="ffcf5-401">Notification queuing</span></span>

<span data-ttu-id="ffcf5-402">**注意：** 通知會在無法立即顯示時排入佇列，例如，當另一個通知顯示時、使用者正在執行全螢幕應用程式，或是使用者未主動使用該電腦時。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-402">**Note:** Notifications are queued whenever they cannot be displayed immediately, such as when another notification is being displayed, the user is running a full-screen application, or the user isn't actively using the computer.</span></span> <span data-ttu-id="ffcf5-403">即時通知會保留在佇列中，僅限60秒。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-403">Real-time notifications remain in the queue for only 60 seconds.</span></span>

-   <span data-ttu-id="ffcf5-404">**針對「動作成功」和「僅供參考」模式，請使用即時選項** ，讓通知未排入佇列的時間長度。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-404">**For the action success and FYI patterns, use the real-time option** so that the notification isn't queued for long.</span></span> <span data-ttu-id="ffcf5-405">只有當這些通知可以立即顯示時，才會有值。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-405">These notifications have value only when they can be displayed immediately.</span></span>
-   <span data-ttu-id="ffcf5-406">**當佇列通知不再相關時，請將其移除。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-406">**Remove queued notifications when they are no longer relevant.**</span></span>
-   <span data-ttu-id="ffcf5-407">**開發人員：** 若要這麼做，您可以 \_ 在 uFlags 中設定 n 資訊旗標，並將 szInfo 設為空字串。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-407">**Developers:** You can do this by setting the NIF\_INFO flag in uFlags and set szInfo to an empty string.</span></span> <span data-ttu-id="ffcf5-408">如果通知已不在佇列中，就不會有任何損害。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-408">There is no harm in doing this if the notification is no longer in the queue.</span></span>

### <a name="system-integration"></a><span data-ttu-id="ffcf5-409">系統整合</span><span class="sxs-lookup"><span data-stu-id="ffcf5-409">System integration</span></span>

-   <span data-ttu-id="ffcf5-410">如果您的應用程式在 [通知區域](winenv-notification.md) 中不一定會有圖示，則會在 **引發通知的非同步工作或事件期間暫時顯示圖示。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-410">If your application doesn't always have an icon in the [notification area](winenv-notification.md) when it's running, **display an icon temporarily during the asynchronous task or event that caused the notification.**</span></span>

## <a name="text"></a><span data-ttu-id="ffcf5-411">Text</span><span class="sxs-lookup"><span data-stu-id="ffcf5-411">Text</span></span>

### <a name="title-text"></a><span data-ttu-id="ffcf5-412">標題文字</span><span class="sxs-lookup"><span data-stu-id="ffcf5-412">Title text</span></span>

-   <span data-ttu-id="ffcf5-413">**使用標題文字，簡要地摘要說明您需要以清晰、簡潔、精確的特定語言傳達給使用者的最重要資訊。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-413">**Use title text that briefly summarizes the most important information you need to communicate to users in clear, plain, concise, specific language.**</span></span> <span data-ttu-id="ffcf5-414">使用者應該能夠快速且輕鬆地瞭解通知資訊的用途。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-414">Users should be able to understand the purpose of the notification information quickly and with minimal effort.</span></span>
-   <span data-ttu-id="ffcf5-415">**使用文字片段或完成句子，而不結束標點符號。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-415">**Use text fragments or complete sentences without ending punctuation.**</span></span>
-   <span data-ttu-id="ffcf5-416">**使用句型大寫。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-416">**Use sentence-style capitalization.**</span></span>
-   <span data-ttu-id="ffcf5-417">**使用英文)  (不超過48個字元來容納當地語系化。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-417">**Use no more than 48 characters (in English) to accommodate localization.**</span></span> <span data-ttu-id="ffcf5-418">標題的長度上限為63個字元，但翻譯英文文字時，您必須允許30% 的擴充。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-418">The title has a maximum length of 63 characters, but you must allow for 30 percent expansion when the English-language text is translated.</span></span>

### <a name="body-text"></a><span data-ttu-id="ffcf5-419">主體文字</span><span class="sxs-lookup"><span data-stu-id="ffcf5-419">Body text</span></span>

-   <span data-ttu-id="ffcf5-420">**使用提供描述 (的內文文字，而不重複標題中的資訊) 並選擇性地提供通知的特定詳細資料，並讓使用者知道有哪些動作可供使用。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-420">**Use body text that gives a description (without repeating the information in the title) and, optionally, that gives specific details about the notification, and also lets users know what action is available.**</span></span>
-   <span data-ttu-id="ffcf5-421">**使用結尾標點符號的完整句子。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-421">**Use complete sentences with ending punctuation.**</span></span>
-   <span data-ttu-id="ffcf5-422">**使用句型大寫。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-422">**Use sentence-style capitalization.**</span></span>
-   <span data-ttu-id="ffcf5-423">**使用英文)  (不超過200個字元來容納當地語系化。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-423">**Use no more than 200 characters (in English) to accommodate localization.**</span></span> <span data-ttu-id="ffcf5-424">本文的長度上限為255個字元，但翻譯英文文字時，您必須允許30% 的擴充。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-424">The body text has a maximum length of 255 characters, but you must allow for 30 percent expansion when the English-language text is translated.</span></span>
-   <span data-ttu-id="ffcf5-425">**在本文文字中包含基本資訊，例如特定的物件名稱。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-425">**Include essential information in the body text, such as specific object names.**</span></span> <span data-ttu-id="ffcf5-426"> (範例：使用者名稱、檔案名或 Url。 ) 使用者不應該開啟另一個視窗來尋找這類資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-426">(Examples: user names, file names, or URLs.) Users shouldn't have to open another window to find such information.</span></span>
-   <span data-ttu-id="ffcf5-427">**在物件名稱前後加上雙引號。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-427">**Put double quotation marks around object names.**</span></span>
    -   <span data-ttu-id="ffcf5-428">**例外狀況：** 請勿在下列情況使用引號：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-428">**Exception:** Don't use quotation marks when:</span></span>
        -   <span data-ttu-id="ffcf5-429">物件名稱一律使用 [標題樣式的大小寫](glossary.md)，例如使用使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-429">The object name always uses [title-style capitalization](glossary.md), such as with user names.</span></span>
        -   <span data-ttu-id="ffcf5-430">物件名稱會以冒號 (範例：印表機名稱：我的印表機) 。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-430">The object name is offset with a colon (example: Printer name: My printer).</span></span>
        -   <span data-ttu-id="ffcf5-431">您可以從內容輕鬆地判斷物件名稱。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-431">The object name can be easily determined from the context.</span></span>
-   <span data-ttu-id="ffcf5-432">**如果您必須將物件名稱截斷為固定大小上限以容納當地語系化，請使用省略號來指出截斷。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-432">**If you must truncate object names to a fixed maximum size to accommodate localization, use an ellipsis to indicate truncation.**</span></span>

    ![<span data-ttu-id="ffcf5-433">包含縮寫名稱之訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-433">screen shot of message containing shortened name</span></span> ](images/mess-notif-image23.png)

    <span data-ttu-id="ffcf5-434">在此範例中，物件名稱會使用省略號截斷。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-434">In this example, an object name is truncated using an ellipsis.</span></span>

-   <span data-ttu-id="ffcf5-435">**如果通知可採取動作，請使用下列措辭：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-435">**Use the following phrasing if the notification is actionable:**</span></span>
    -   <span data-ttu-id="ffcf5-436">如果使用者可以按一下通知來執行動作：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-436">If users can click the notification to perform an action:</span></span>

        <span data-ttu-id="ffcf5-437">< 重要資訊的簡短描述></span><span class="sxs-lookup"><span data-stu-id="ffcf5-437">< brief description of essential information></span></span>

        <optional details>

        <span data-ttu-id="ffcf5-438">按一下 [到] <do something> 。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-438">Click to <do something>.</span></span>

        ![<span data-ttu-id="ffcf5-439">訊息的螢幕擷取畫面： [按一下以查看進度]</span><span class="sxs-lookup"><span data-stu-id="ffcf5-439">screen shot of message: 'click to view progress'</span></span> ](images/mess-notif-image24.png)

        <span data-ttu-id="ffcf5-440">在此範例中，使用者可以按一下來執行動作。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-440">In this example, users can click to perform an action.</span></span>

    -   <span data-ttu-id="ffcf5-441">如果使用者可以按一下通知以查看詳細資訊：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-441">If users can click the notification to see more information:</span></span>

        <span data-ttu-id="ffcf5-442">< 重要資訊的簡短描述></span><span class="sxs-lookup"><span data-stu-id="ffcf5-442">< brief description of essential information></span></span>

        <optional details>

        <span data-ttu-id="ffcf5-443">按一下以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-443">Click for more information.</span></span>

        ![<span data-ttu-id="ffcf5-444">訊息的螢幕擷取畫面：按一下以取得詳細資訊</span><span class="sxs-lookup"><span data-stu-id="ffcf5-444">screen shot of message: click for more information</span></span> ](images/mess-notif-image25.png)

        <span data-ttu-id="ffcf5-445">在此範例中，使用者可以按一下以取得詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-445">In this example, users can click for more information.</span></span>

-   <span data-ttu-id="ffcf5-446">**不要說使用者「必須」在通知中執行動作。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-446">**Don't say that the user "must" perform an action in a notification.**</span></span> <span data-ttu-id="ffcf5-447">通知適用于使用者可自由忽略的非重要資訊。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-447">Notifications are for non-critical information that users can freely ignore.</span></span> <span data-ttu-id="ffcf5-448">如果使用者真的必須執行動作，請不要使用通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-448">If users really must perform an action, don't use notifications.</span></span>
-   <span data-ttu-id="ffcf5-449">**如果使用者應該執行動作，請將重要性設為 clear。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-449">**If users should perform an action, make the importance clear.**</span></span>
-   <span data-ttu-id="ffcf5-450">針對動作失敗和非關鍵性的系統事件模式， **以純語言描述問題。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-450">For the action failure and non-critical system event patterns, **describe problems in plain language.**</span></span>

    <span data-ttu-id="ffcf5-451">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-451">**Incorrect:**</span></span>

    ![<span data-ttu-id="ffcf5-452">冗長複雜訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-452">screen shot of lengthy, complex message</span></span> ](images/mess-notif-image26.png)

    <span data-ttu-id="ffcf5-453">在此範例中，問題的描述是使用過度技術性但 unspecific 的語言。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-453">In this example, the problem is described using overly technical, yet unspecific language.</span></span>

    <span data-ttu-id="ffcf5-454">**正確：**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-454">**Correct:**</span></span>

    ![<span data-ttu-id="ffcf5-455">清晰、簡潔訊息的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="ffcf5-455">screen shot of clear, concise message</span></span> ](images/mess-notif-image27.png)

    <span data-ttu-id="ffcf5-456">在此範例中，問題是以純文字來描述。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-456">In this example, the problem is described in plain language.</span></span>

-   <span data-ttu-id="ffcf5-457">**以與目標使用者相關的方式來描述事件。**</span><span class="sxs-lookup"><span data-stu-id="ffcf5-457">**Describe the event in a way that is relevant to the target users.**</span></span> <span data-ttu-id="ffcf5-458">如果有合理的機會讓使用者執行工作，或將其行為變更為通知的結果，則會有相關通知。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-458">A notification is relevant if there's a reasonable chance that users will perform a task or change their behavior as the result of the notification.</span></span> <span data-ttu-id="ffcf5-459">您通常可以藉由在使用者目標（而非技術問題）中描述通知，來達成此目的。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-459">You can often accomplish this by describing notifications in terms of user goals instead of technological issues.</span></span>

## <a name="documentation"></a><span data-ttu-id="ffcf5-460">文件</span><span class="sxs-lookup"><span data-stu-id="ffcf5-460">Documentation</span></span>

<span data-ttu-id="ffcf5-461">參考通知時：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-461">When referring to notifications:</span></span>

-   <span data-ttu-id="ffcf5-462">使用確切的標題文字，包括其大小寫。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-462">Use the exact title text, including its capitalization.</span></span>
-   <span data-ttu-id="ffcf5-463">請以通知的形式來參考元件，而不是以氣球或警示的形式來表示。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-463">Refer to the component as a notification, not as a balloon or an alert.</span></span>
-   <span data-ttu-id="ffcf5-464">若要描述使用者互動，請使用按一下。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-464">To describe user interaction, use click.</span></span>
-   <span data-ttu-id="ffcf5-465">可能的話，請使用粗體文字來格式化標題文字。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-465">When possible, format the title text using bold text.</span></span> <span data-ttu-id="ffcf5-466">否則，請只在必要時才將標題放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-466">Otherwise, put the title in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="ffcf5-467">範例：當 [ **重大更新已準備好要安裝** ] 通知出現時，請按一下通知以開始處理。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-467">Example: When the **Critical updates are ready to install** notification appears, click the notification to start the process.</span></span>

<span data-ttu-id="ffcf5-468">參考通知區域時：</span><span class="sxs-lookup"><span data-stu-id="ffcf5-468">When referring to the notification area:</span></span>

-   <span data-ttu-id="ffcf5-469">請將通知區域稱為通知區域，而不是系統匣。</span><span class="sxs-lookup"><span data-stu-id="ffcf5-469">Refer to the notification area as the notification area, not the system tray.</span></span>

 

