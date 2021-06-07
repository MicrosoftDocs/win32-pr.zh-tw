---
title: 控制台
description: 使用控制台專案來協助使用者設定系統層級的功能，並執行相關工作。 具有使用者介面的程式應該改為從其 UI 直接設定。
ms.assetid: 845325ef-9f1d-4aa7-a5b0-685fac74a9f8
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 3b0e6fdf4e0c916f80ae3c1783e4e9e5fee920a8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443309"
---
# <a name="control-panels"></a><span data-ttu-id="51077-104">控制台</span><span class="sxs-lookup"><span data-stu-id="51077-104">Control Panels</span></span>

> [!NOTE]
> <span data-ttu-id="51077-105">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="51077-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="51077-106">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="51077-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="51077-107">使用控制台專案來協助使用者設定系統層級的功能，並執行相關工作。</span><span class="sxs-lookup"><span data-stu-id="51077-107">Use control panel items to help users configure system-level features and perform related tasks.</span></span> <span data-ttu-id="51077-108">具有使用者介面的程式應該改為從其 UI 直接設定。</span><span class="sxs-lookup"><span data-stu-id="51077-108">Programs that have a user interface should be configured directly from their UI instead.</span></span>

<span data-ttu-id="51077-109">有了 Microsoft Windows 的主控台，使用者就可以設定系統層級的功能，並執行相關工作。</span><span class="sxs-lookup"><span data-stu-id="51077-109">With Control Panel in Microsoft Windows, users can configure system-level features and perform related tasks.</span></span> <span data-ttu-id="51077-110">系統層級功能設定的範例包括硬體和軟體設定、安全性、系統維護以及使用者帳戶管理。</span><span class="sxs-lookup"><span data-stu-id="51077-110">Examples of system-level feature configuration include hardware and software setup and configuration, security, system maintenance, and user account management.</span></span>

<span data-ttu-id="51077-111">主控台一詞指的是整個 Windows 主控台功能。</span><span class="sxs-lookup"><span data-stu-id="51077-111">The term Control Panel refers to the entire Windows Control Panel feature.</span></span> <span data-ttu-id="51077-112">個別的控制台稱為控制台專案。</span><span class="sxs-lookup"><span data-stu-id="51077-112">Individual control panels are referred to as control panel items.</span></span> <span data-ttu-id="51077-113">當您直接從 [控制台] 首頁或類別頁面存取 [控制台] 專案時，會將其視為最上層。</span><span class="sxs-lookup"><span data-stu-id="51077-113">A control panel item is considered top-level when it is directly accessible from the control panel home page or a category page.</span></span>

![<span data-ttu-id="51077-114">控制台語音分類的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-114">screen shot of control panel speech category</span></span> ](images/winenv-ctrl-panels-image1.png)

<span data-ttu-id="51077-115">一般的 [控制台] 專案。</span><span class="sxs-lookup"><span data-stu-id="51077-115">A typical control panel item.</span></span>

<span data-ttu-id="51077-116">[控制台] 首頁是所有控制台專案的主要進入點。</span><span class="sxs-lookup"><span data-stu-id="51077-116">The control panel home page is the main entry point for all control panel items.</span></span> <span data-ttu-id="51077-117">它會依類別目錄列出專案，以及最常見的工作。</span><span class="sxs-lookup"><span data-stu-id="51077-117">It lists the items by their category, along with the most common tasks.</span></span> <span data-ttu-id="51077-118">當使用者按一下 [開始] 功能表中的主控台時，就會顯示此畫面。</span><span class="sxs-lookup"><span data-stu-id="51077-118">It is displayed when users click Control Panel in the Start menu.</span></span>

<span data-ttu-id="51077-119">[控制台類別] 頁面會列出單一類別內的專案，以及最常見的工作。</span><span class="sxs-lookup"><span data-stu-id="51077-119">A control panel category page lists the items within a single category, along with the most common tasks.</span></span> <span data-ttu-id="51077-120">當使用者按一下首頁上的類別名稱時，就會顯示此頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-120">It is displayed when users click a category name on the home page.</span></span>

<span data-ttu-id="51077-121">控制台專案是使用工作 [流程](glossary.md) 或屬性工作表來執行。</span><span class="sxs-lookup"><span data-stu-id="51077-121">Control panel items are implemented using [task flows](glossary.md) or property sheets.</span></span> <span data-ttu-id="51077-122">針對 Windows Vista 和更新版本，工作流程是慣用的使用者介面， (UI) 。</span><span class="sxs-lookup"><span data-stu-id="51077-122">For Windows Vista and later, task flows are the preferred user interface (UI).</span></span>

<span data-ttu-id="51077-123">**開發人員：** 若要瞭解如何建立 [控制台] 專案，請參閱 [主控台專案](/previous-versions//bb776838(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="51077-123">**Developers:** To learn how to create control panel items, see [Control Panel Items](/previous-versions//bb776838(v=vs.85)).</span></span>

<span data-ttu-id="51077-124">**注意：** 與 [屬性工作表](win-property-win.md) 相關的指導方針會在個別的文章中顯示。</span><span class="sxs-lookup"><span data-stu-id="51077-124">**Note:** Guidelines related to [property sheets](win-property-win.md) are presented in a separate article.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="51077-125">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="51077-125">Is this the right user interface?</span></span>

<span data-ttu-id="51077-126">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="51077-126">To decide, consider these questions:</span></span>

-   <span data-ttu-id="51077-127">**設定系統層級功能的目的是什麼？**</span><span class="sxs-lookup"><span data-stu-id="51077-127">**Is the purpose to configure system-level features?**</span></span> <span data-ttu-id="51077-128">如果沒有，請使用另一個整合點。</span><span class="sxs-lookup"><span data-stu-id="51077-128">If not, use another integration point.</span></span> <span data-ttu-id="51077-129">您可以使用 [選項] 對話方塊，直接從 UI 設定您的應用程式功能，而不是使用主控台。</span><span class="sxs-lookup"><span data-stu-id="51077-129">Make your application features configurable directly from the UI using options dialog boxes, instead of using Control Panel.</span></span> <span data-ttu-id="51077-130">針對未用於安裝、設定或相關工作的公用程式 (例如疑難排解) ，請使用 [開始] 功能表作為整合點。</span><span class="sxs-lookup"><span data-stu-id="51077-130">For utilities that aren't used for setup, configuration, or related tasks (like troubleshooting), use the Start menu as the integration point.</span></span>
-   <span data-ttu-id="51077-131">**系統層級功能是否有它自己的 UI？**</span><span class="sxs-lookup"><span data-stu-id="51077-131">**Does the system-level feature have its own UI?**</span></span> <span data-ttu-id="51077-132">如果是這樣，則使用者應該前往該 UI 進行變更。</span><span class="sxs-lookup"><span data-stu-id="51077-132">If so, that UI is where users should go to make changes.</span></span> <span data-ttu-id="51077-133">例如，系統備份公用程式應從其程式選項中設定，而不是從主控台。</span><span class="sxs-lookup"><span data-stu-id="51077-133">For example, a system backup utility should be configured from its program options instead of from Control Panel.</span></span>
-   <span data-ttu-id="51077-134">**使用者是否需要經常變更設定？**</span><span class="sxs-lookup"><span data-stu-id="51077-134">**Will users need to change the configuration often?**</span></span> <span data-ttu-id="51077-135">如果有 (說，每週) 幾次，請考慮替代的解決方案，甚至是使用主控台。</span><span class="sxs-lookup"><span data-stu-id="51077-135">If so (say, several times a week), consider alternative solutions, perhaps in addition to using Control Panel.</span></span> <span data-ttu-id="51077-136">例如，您可以直接從通知區域中的圖示來設定 Windows 主要磁片區設定。</span><span class="sxs-lookup"><span data-stu-id="51077-136">For example, the Windows master volume setting can be configured directly from its icon in the notification area.</span></span> <span data-ttu-id="51077-137">某些設定可以自動設定。</span><span class="sxs-lookup"><span data-stu-id="51077-137">Some settings can be configured automatically.</span></span> <span data-ttu-id="51077-138">例如，在 Windows 檔案總管中，應用程式屬性的 [相容性] 索引標籤可讓應用程式在256色彩模式中執行，而不需要使用者手動變更影片模式。</span><span class="sxs-lookup"><span data-stu-id="51077-138">In Windows Explorer, for example, the Compatibility tab for application properties allows an application to be run in 256 color mode instead of requiring users to change the video mode manually.</span></span>
-   <span data-ttu-id="51077-139">**目標使用者是 IT 專業人員嗎？**</span><span class="sxs-lookup"><span data-stu-id="51077-139">**Are the target users IT professionals?**</span></span> <span data-ttu-id="51077-140">若是如此，請改用 [Microsoft Management Console 的 (mmc) ](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) 嵌入式管理單元，這是專為系統管理工作而設計的。</span><span class="sxs-lookup"><span data-stu-id="51077-140">If so, use a [Microsoft Management Console (MMC)](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) snap-in instead, which is designed specifically for system management tasks.</span></span> <span data-ttu-id="51077-141">在某些情況下，最好的解決方法是讓一般使用者都能使用 [控制台] 專案，並為 IT 專業人員提供 MMC 嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="51077-141">In some cases, the best solution is to have both a control panel item for general users and an MMC snap-in for IT professionals.</span></span>

    ![<span data-ttu-id="51077-142">[電腦管理] 視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-142">screen shot of computer management window</span></span> ](images/winenv-ctrl-panels-image2.png)

    <span data-ttu-id="51077-143">在此範例中，[本機使用者和群組] MMC 嵌入式管理單元提供以 IT 專業人員為目標的使用者管理。</span><span class="sxs-lookup"><span data-stu-id="51077-143">In this example, the Local Users and Groups MMC snap-in provides user management targeted at IT professionals.</span></span> <span data-ttu-id="51077-144">其他使用者更有可能使用主控台中的 [使用者帳戶] 專案。</span><span class="sxs-lookup"><span data-stu-id="51077-144">Other users are more likely to use the User Accounts item in Control Panel.</span></span>

-   <span data-ttu-id="51077-145">**這項功能是否只有在初始系統組態期間才會使用 OEM 功能？**</span><span class="sxs-lookup"><span data-stu-id="51077-145">**Is the feature an OEM feature used only during initial system configuration?**</span></span> <span data-ttu-id="51077-146">若是如此，請使用 Windows 歡迎中心作為整合點。</span><span class="sxs-lookup"><span data-stu-id="51077-146">If so, use the Windows Welcome Center as the integration point.</span></span>

<span data-ttu-id="51077-147">需要控制台專案，因為許多系統層級功能都沒有更明顯或直接的整合點。</span><span class="sxs-lookup"><span data-stu-id="51077-147">Control panel items are necessary because many system-level features don't have a more obvious or direct integration point.</span></span> <span data-ttu-id="51077-148">但主控台不應視為所有設定的「單一位置」。</span><span class="sxs-lookup"><span data-stu-id="51077-148">Yet Control Panel shouldn't be viewed as the "one place" for all configuration settings.</span></span> <span data-ttu-id="51077-149">**具有使用者介面的程式應該直接從其 UI 進行設定，而不是使用控制台專案。**</span><span class="sxs-lookup"><span data-stu-id="51077-149">**Programs that have a user interface should be configured directly from their UI instead of using control panel items.**</span></span>

<span data-ttu-id="51077-150">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-150">**Incorrect:**</span></span>

![<span data-ttu-id="51077-151">[控制台網際網路選項] 專案的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-151">screen shot of control panel internet options item</span></span> ](images/winenv-ctrl-panels-image3.png)

<span data-ttu-id="51077-152">在此範例中，Windows Internet Explorer 不應以主控台表示，因為它自己的 UI 是更好的整合點。</span><span class="sxs-lookup"><span data-stu-id="51077-152">In this example, Windows Internet Explorer shouldn't be represented in Control Panel, because its own UI is a better integration point.</span></span>

### <a name="create-a-new-control-panel-item-or-extend-an-existing-one"></a><span data-ttu-id="51077-153">建立新的控制台專案或擴充現有的控制台專案？</span><span class="sxs-lookup"><span data-stu-id="51077-153">Create a new control panel item or extend an existing one?</span></span>

<span data-ttu-id="51077-154">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="51077-154">To decide, consider these questions:</span></span>

-   <span data-ttu-id="51077-155">**這項功能可以用來表示可以插入現有、可擴充的控制台專案的工作嗎？**</span><span class="sxs-lookup"><span data-stu-id="51077-155">**Can the functionality be expressed as tasks that can plug into an existing, extensible control panel item?**</span></span> <span data-ttu-id="51077-156">下列控制台專案可延伸：藍牙裝置、顯示器、網際網路、鍵盤、滑鼠、網路、電源、系統、無線 (紅外線) 。</span><span class="sxs-lookup"><span data-stu-id="51077-156">The following control panel items are extensible: Bluetooth Devices, Display, Internet, Keyboard, Mouse, Network, Power, System, Wireless (infrared).</span></span>
-   <span data-ttu-id="51077-157">**[屬性] 和 [工作] 取代了現有可擴充控制台專案的功能嗎？**</span><span class="sxs-lookup"><span data-stu-id="51077-157">**Do the properties and tasks replace the features of the existing extensible control panel item?**</span></span> <span data-ttu-id="51077-158">若是如此，您應該擴充現有的 [控制台] 專案，因為這樣會產生更簡單的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="51077-158">If so, you should extend the existing control panel item because that results in a simpler user experience.</span></span> <span data-ttu-id="51077-159">如果沒有，請建立新的控制台專案。</span><span class="sxs-lookup"><span data-stu-id="51077-159">If not, create a new control panel item.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="51077-160">設計概念</span><span class="sxs-lookup"><span data-stu-id="51077-160">Design concepts</span></span>

<span data-ttu-id="51077-161">**主控台的概念是以真實世界比喻為基礎。**</span><span class="sxs-lookup"><span data-stu-id="51077-161">**The Control Panel concept is based on a real-world metaphor.**</span></span> <span data-ttu-id="51077-162">真實世界的控制台是控制項的集合， (旋鈕、切換、量測計，以及用來監視和控制裝置) 的顯示器。</span><span class="sxs-lookup"><span data-stu-id="51077-162">A real-world control panel is a collection of controls (knobs, switches, gauges, and displays) used to monitor and control a device.</span></span> <span data-ttu-id="51077-163">這類控制台的使用者通常需要訓練才能瞭解其使用方式。</span><span class="sxs-lookup"><span data-stu-id="51077-163">Users of such control panels often need training to understand how to use them.</span></span>

<span data-ttu-id="51077-164">不同于其真實世界的對應專案， **Windows 控制台設計已針對第一次使用者進行優化。**</span><span class="sxs-lookup"><span data-stu-id="51077-164">Unlike their real-world counterparts, **Windows control panel designs are optimized for first-time users.**</span></span> <span data-ttu-id="51077-165">使用者不會經常執行大部分的控制台工作，因此通常不會記得如何執行這些工作，而且每次都必須破解它們。</span><span class="sxs-lookup"><span data-stu-id="51077-165">Users don't perform most control panel tasks very often, so they usually don't remember how to do them and effectively have to relearn them every time.</span></span>

<span data-ttu-id="51077-166">設計實用且容易使用的控制台專案：</span><span class="sxs-lookup"><span data-stu-id="51077-166">To design a control panel item that is useful and easy to use:</span></span>

-   <span data-ttu-id="51077-167">請確定屬性是必要的。</span><span class="sxs-lookup"><span data-stu-id="51077-167">Make sure the properties are necessary.</span></span>
-   <span data-ttu-id="51077-168">以使用者目標為依據，而不是以技術呈現屬性。</span><span class="sxs-lookup"><span data-stu-id="51077-168">Present properties in terms of user goals instead of technology.</span></span>
-   <span data-ttu-id="51077-169">將屬性顯示在正確層級。</span><span class="sxs-lookup"><span data-stu-id="51077-169">Present properties at the right level.</span></span>
-   <span data-ttu-id="51077-170">特定工作的設計頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-170">Design pages for specific tasks.</span></span>
-   <span data-ttu-id="51077-171">標準使用者和受保護系統管理員的設計頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-171">Design pages for Standard users and Protected administrators.</span></span>

<span data-ttu-id="51077-172">當您設計和評估要包含在主控台中的專案時，請判斷使用者執行的一般工作，並確定有明確的路徑可以執行這些工作。</span><span class="sxs-lookup"><span data-stu-id="51077-172">When designing and evaluating items to include in Control Panel, determine the common tasks that users perform and make sure there is a clear path to perform those tasks.</span></span> <span data-ttu-id="51077-173">使用者通常會使用 [控制台] 專案來執行下列類型的工作：</span><span class="sxs-lookup"><span data-stu-id="51077-173">Users typically perform the following types of tasks with control panel items:</span></span>

-   <span data-ttu-id="51077-174">初始設定</span><span class="sxs-lookup"><span data-stu-id="51077-174">Initial configuration</span></span>
-   <span data-ttu-id="51077-175">大部分設定 (不頻繁的變更) </span><span class="sxs-lookup"><span data-stu-id="51077-175">Infrequent changes (for most settings)</span></span>
-   <span data-ttu-id="51077-176">頻繁的變更 (有幾個重要的設定) </span><span class="sxs-lookup"><span data-stu-id="51077-176">Frequent changes (for a few important settings)</span></span>
-   <span data-ttu-id="51077-177">將設定回復為初始或先前狀態</span><span class="sxs-lookup"><span data-stu-id="51077-177">Rolling back settings to an initial or previous state</span></span>
-   <span data-ttu-id="51077-178">疑難排解</span><span class="sxs-lookup"><span data-stu-id="51077-178">Troubleshooting</span></span>

<span data-ttu-id="51077-179">**如果您只做一件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="51077-179">**If you do only one thing...**</span></span>

<span data-ttu-id="51077-180">設計特定工作的控制台頁面，並以使用者目標而非技術呈現這些頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-180">Design control panel pages for specific tasks, and present them in terms of user goals instead of technology.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="51077-181">使用模式</span><span class="sxs-lookup"><span data-stu-id="51077-181">Usage patterns</span></span>

<span data-ttu-id="51077-182">您可以使用工作流程或屬性工作表，針對 [控制台] 專案。</span><span class="sxs-lookup"><span data-stu-id="51077-182">For control panel items, you can use a task flow or a property sheet.</span></span> <span data-ttu-id="51077-183">以下是其使用模式：</span><span class="sxs-lookup"><span data-stu-id="51077-183">Here are their usage patterns:</span></span>

### <a name="task-flow-patterns"></a><span data-ttu-id="51077-184">工作流程模式</span><span class="sxs-lookup"><span data-stu-id="51077-184">Task flow patterns</span></span>

<span data-ttu-id="51077-185">工作流程專案使用中樞頁面來呈現高階選項，以及用來執行實際設定的輪輻頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-185">Task flow items use a hub page to present the high-level choices, and spoke pages to perform the actual configuration.</span></span>

<span data-ttu-id="51077-186">**中樞頁面**</span><span class="sxs-lookup"><span data-stu-id="51077-186">**Hub pages**</span></span>

-   <span data-ttu-id="51077-187">以工作為基礎的中樞頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-187">Task-based hub pages.</span></span> <span data-ttu-id="51077-188">這些中樞頁面會顯示最常使用的工作。</span><span class="sxs-lookup"><span data-stu-id="51077-188">These hub pages present the most commonly used tasks.</span></span> <span data-ttu-id="51077-189">它們最適合用於一些常用或重要的工作，使用者需要更多指引和說明。</span><span class="sxs-lookup"><span data-stu-id="51077-189">They are best used for a few commonly used or important tasks where users need more guidance and explanation.</span></span> <span data-ttu-id="51077-190">中樞頁面沒有認可按鈕。</span><span class="sxs-lookup"><span data-stu-id="51077-190">Hub pages don't have commit buttons.</span></span> <span data-ttu-id="51077-191">混合式以工作為基礎的中樞頁面也有直接的一些屬性或命令。</span><span class="sxs-lookup"><span data-stu-id="51077-191">Hybrid task-based hub pages also have some properties or commands directly on them.</span></span> <span data-ttu-id="51077-192">當使用者最有可能使用主控台來存取這些屬性和命令時，強烈建議使用混合式中樞頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-192">Hybrid hub pages are strongly recommended when users are most likely to use Control Panel to access those properties and commands.</span></span>
-   <span data-ttu-id="51077-193">以物件為基礎的中樞頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-193">Object-based hub pages.</span></span> <span data-ttu-id="51077-194">這些中樞頁面會使用清單視圖控制項來顯示可用的物件。</span><span class="sxs-lookup"><span data-stu-id="51077-194">These hub pages present the available objects using a list view control.</span></span> <span data-ttu-id="51077-195">當可能有數個物件時，最好使用它們。</span><span class="sxs-lookup"><span data-stu-id="51077-195">They are best used when there could be several objects.</span></span> <span data-ttu-id="51077-196">中樞頁面沒有認可按鈕。</span><span class="sxs-lookup"><span data-stu-id="51077-196">Hub pages don't have commit buttons.</span></span>

<span data-ttu-id="51077-197">**輪輻頁面**</span><span class="sxs-lookup"><span data-stu-id="51077-197">**Spoke pages**</span></span>

-   <span data-ttu-id="51077-198">工作頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-198">Task pages.</span></span> <span data-ttu-id="51077-199">這些輪輻頁面會在工作中顯示工作或步驟，其中包含以工作為基礎的特定主要指令。</span><span class="sxs-lookup"><span data-stu-id="51077-199">These spoke pages present a task or a step in a task with a specific, task-based main instruction.</span></span> <span data-ttu-id="51077-200">它們最適合用於受益于其他指引和說明的工作。</span><span class="sxs-lookup"><span data-stu-id="51077-200">They are best used for tasks that benefit from additional guidance and explanation.</span></span>
-   <span data-ttu-id="51077-201">表單頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-201">Form pages.</span></span> <span data-ttu-id="51077-202">這些輪輻頁面會根據一般主要指示來呈現相關屬性和工作的集合。</span><span class="sxs-lookup"><span data-stu-id="51077-202">These spoke pages present a collection of related properties and tasks based on a general main instruction.</span></span> <span data-ttu-id="51077-203">它們最適合用於具有許多屬性的功能，並受益于直接的單一頁面呈現，例如 advanced properties。</span><span class="sxs-lookup"><span data-stu-id="51077-203">They are best used for features that have many properties and benefit from a direct, single-page presentation, such as advanced properties.</span></span>

### <a name="property-sheet-patterns"></a><span data-ttu-id="51077-204">屬性工作表模式</span><span class="sxs-lookup"><span data-stu-id="51077-204">Property sheet patterns</span></span>

-   <span data-ttu-id="51077-205">屬性工作表最適合用於具有許多設定（以 advanced users 為目標）的舊版專案。</span><span class="sxs-lookup"><span data-stu-id="51077-205">Property sheets are best used in legacy items with many settings targeted at advanced users.</span></span> <span data-ttu-id="51077-206">使用表單頁面模式的工作流程，新的專案可以達到相同的效果。</span><span class="sxs-lookup"><span data-stu-id="51077-206">New items can achieve the same effect with a task flow using the form page pattern.</span></span>

## <a name="guidelines"></a><span data-ttu-id="51077-207">指導方針</span><span class="sxs-lookup"><span data-stu-id="51077-207">Guidelines</span></span>

### <a name="property-sheet-control-panel-items"></a><span data-ttu-id="51077-208">屬性工作表的控制台專案</span><span class="sxs-lookup"><span data-stu-id="51077-208">Property sheet control panel items</span></span>

-   <span data-ttu-id="51077-209">**請勿將屬性工作表用於新的控制台專案。**</span><span class="sxs-lookup"><span data-stu-id="51077-209">**Don't use property sheets for new control panel items.**</span></span> <span data-ttu-id="51077-210">相反地，請使用工作流程來建立順暢的體驗，並充分利用 [控制台] 首頁的分類和搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="51077-210">Instead, use task flows to create a seamless experience and make full use of the categorization and search functionality of the control panel home page.</span></span>

### <a name="task-flow-control-panel-items"></a><span data-ttu-id="51077-211">[工作流程] 控制台專案</span><span class="sxs-lookup"><span data-stu-id="51077-211">Task flow control panel items</span></span>

<span data-ttu-id="51077-212">**一般**</span><span class="sxs-lookup"><span data-stu-id="51077-212">**General**</span></span>

-   <span data-ttu-id="51077-213">**將最重要的內容和控制項保持可見，而不需要滾動。**</span><span class="sxs-lookup"><span data-stu-id="51077-213">**Keep the most important content and controls visible without scrolling.**</span></span> <span data-ttu-id="51077-214">除非使用者有原因，否則使用者不會看到頁面內容。</span><span class="sxs-lookup"><span data-stu-id="51077-214">Users won't scroll to see page content unless they have a reason to.</span></span> <span data-ttu-id="51077-215">您可以將認可按鈕放在 [命令區域](glossary.md) 中，而不是在內容區域中，讓它們保持可見。</span><span class="sxs-lookup"><span data-stu-id="51077-215">You can make commit buttons always visible by placing them in a [command area](glossary.md) instead of the content area.</span></span> <span data-ttu-id="51077-216">請勿只分割頁面以避免滾動。</span><span class="sxs-lookup"><span data-stu-id="51077-216">Don't break up pages just to avoid scrolling.</span></span>
    -   <span data-ttu-id="51077-217">**您可以垂直捲動長頁，只要可以** 看到最重要的控制項而不需要滾動。</span><span class="sxs-lookup"><span data-stu-id="51077-217">**You can vertically scroll long pages,** as long as the most important controls are visible without scrolling.</span></span>
    -   <span data-ttu-id="51077-218">**請勿使用水準滾動。**</span><span class="sxs-lookup"><span data-stu-id="51077-218">**Don't use horizontal scrolling.**</span></span> <span data-ttu-id="51077-219">請改為重新設計頁面內容，並使用垂直捲動。</span><span class="sxs-lookup"><span data-stu-id="51077-219">Instead, redesign the page content and use vertical scrolling.</span></span> <span data-ttu-id="51077-220">頁面只有在變得很窄時，才會有水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="51077-220">Pages may have horizontal scrollbars only when made very narrow.</span></span>
-   <span data-ttu-id="51077-221">**在頁面之間流覽：**</span><span class="sxs-lookup"><span data-stu-id="51077-221">**To navigate between pages:**</span></span>
    -   <span data-ttu-id="51077-222">使用工作 [連結](glossary.md) 來啟動工作。</span><span class="sxs-lookup"><span data-stu-id="51077-222">Use [task links](glossary.md) to start a task.</span></span>
    -   <span data-ttu-id="51077-223">使用 [工作連結] 或 [下一步] 按鈕，流覽至多步驟工作中的下一個頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-223">Use task links or a Next button to navigate to the next page in a multi-step task.</span></span>
    -   <span data-ttu-id="51077-224">使用 [認可] 按鈕來完成工作。</span><span class="sxs-lookup"><span data-stu-id="51077-224">Use commit buttons to complete a task.</span></span>
    -   <span data-ttu-id="51077-225">使用功能表列中的 [上一頁] 按鈕，以返回先前看到的頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-225">Use the Back button in the menu bar to return to previously viewed pages.</span></span> <span data-ttu-id="51077-226">請勿將 [上一頁] 按鈕新增至命令區域。</span><span class="sxs-lookup"><span data-stu-id="51077-226">Do not add a Back button to the command area.</span></span>
    -   <span data-ttu-id="51077-227">使用網址列直接返回控制台的首頁。</span><span class="sxs-lookup"><span data-stu-id="51077-227">Use the Address bar to return directly to the control panel home page.</span></span>
    -   <span data-ttu-id="51077-228">使用工作窗格中的 [另請參閱連結]，流覽至其他控制台專案中的頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-228">Use See also links in the task pane to navigate to pages in other control panel items.</span></span> <span data-ttu-id="51077-229">否則，流覽應該會保留在單一控制台專案內。</span><span class="sxs-lookup"><span data-stu-id="51077-229">Otherwise, navigation should stay within a single control panel item.</span></span>
-   <span data-ttu-id="51077-230">**只將 [控制台] 首頁放在網址列中。**</span><span class="sxs-lookup"><span data-stu-id="51077-230">**Put only the control panel home page in the Address bar.**</span></span> <span data-ttu-id="51077-231">按一下該連結會返回 [控制台] 首頁，放棄任何進行中的工作而不進行 [確認](https://msdn.microsoft.com/library/windows/desktop/aa511273.aspx)。</span><span class="sxs-lookup"><span data-stu-id="51077-231">Clicking that link returns to the control panel home page, abandoning any work in progress without a [confirmation](https://msdn.microsoft.com/library/windows/desktop/aa511273.aspx).</span></span>
-   <span data-ttu-id="51077-232">**不要在 [控制台] 頁面上放置 [關閉命令] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-232">**Don't put a Close command button on control panel pages.**</span></span> <span data-ttu-id="51077-233">使用者可以使用標題列上的 [關閉] 按鈕，關閉 [控制台] 視窗。</span><span class="sxs-lookup"><span data-stu-id="51077-233">Users can close a control panel window using the Close button on the title bar.</span></span>

<span data-ttu-id="51077-234">**工作連結和按鈕**</span><span class="sxs-lookup"><span data-stu-id="51077-234">**Task links and buttons**</span></span>

-   <span data-ttu-id="51077-235">**當頁面有一組較小的固定選項時，請使用工作連結，而不是選項按鈕和 [下一步] 按鈕的組合。**</span><span class="sxs-lookup"><span data-stu-id="51077-235">**When a page has a small set of fixed options, use task links instead of a combination of radio buttons and a Next button.**</span></span> <span data-ttu-id="51077-236">如此一來，使用者只要按一下就可以選取回應。</span><span class="sxs-lookup"><span data-stu-id="51077-236">This allows users to select a response with a single click.</span></span>
-   <span data-ttu-id="51077-237">您可以在下列位置中放入工作連結和按鈕， (可探索) 的順序：</span><span class="sxs-lookup"><span data-stu-id="51077-237">You can put task links and buttons in the following places (in order of discoverability):</span></span>
    -   <span data-ttu-id="51077-238">只有) 的輪輻頁面上的命令按鈕 ([命令區](glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="51077-238">The [command area](glossary.md) (for command buttons on spoke pages only).</span></span>
    -   <span data-ttu-id="51077-239">[內容區域](glossary.md)：</span><span class="sxs-lookup"><span data-stu-id="51077-239">The [content area](glossary.md):</span></span>
        -   <span data-ttu-id="51077-240">命令按鈕</span><span class="sxs-lookup"><span data-stu-id="51077-240">Command buttons</span></span>
        -   <span data-ttu-id="51077-241">工作連結</span><span class="sxs-lookup"><span data-stu-id="51077-241">Task links</span></span>
        -   <span data-ttu-id="51077-242">其他連結</span><span class="sxs-lookup"><span data-stu-id="51077-242">Other links</span></span>
    -   <span data-ttu-id="51077-243">工作 [窗格](glossary.md) 中的連結只 (中樞頁面) 。</span><span class="sxs-lookup"><span data-stu-id="51077-243">Links in the [task pane](glossary.md) (hub pages only).</span></span>
-   <span data-ttu-id="51077-244">**將工作連結和按鈕的位置作為重要性，以及可搜尋性的需求。**</span><span class="sxs-lookup"><span data-stu-id="51077-244">**Base the location of task links and buttons on importance and need for discoverability.**</span></span>
    -   <span data-ttu-id="51077-245">**只將認可按鈕放在命令區域中。**</span><span class="sxs-lookup"><span data-stu-id="51077-245">**Put only commit buttons in the command area.**</span></span>
    -   <span data-ttu-id="51077-246">**將重要的工作放在內容區域中。**</span><span class="sxs-lookup"><span data-stu-id="51077-246">**Put essential tasks in the content area.**</span></span> <span data-ttu-id="51077-247">命令按鈕通常會繪製最多注意，因此請為使用者必須看到的命令保留它們。</span><span class="sxs-lookup"><span data-stu-id="51077-247">Command buttons tend to draw the most attention, so reserve them for commands users must see.</span></span> <span data-ttu-id="51077-248">工作連結也會強調，但小於命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="51077-248">Task links also draw attention, but less than command buttons.</span></span>
    -   <span data-ttu-id="51077-249">**保留工作窗格，以及次要 (不重要) 工作的純連結。**</span><span class="sxs-lookup"><span data-stu-id="51077-249">**Reserve the task pane and plain links for secondary (less important) tasks.**</span></span> <span data-ttu-id="51077-250">工作窗格是工作頁面中最不容易探索的區域，而純連結不像命令按鈕和工作連結一樣可見。</span><span class="sxs-lookup"><span data-stu-id="51077-250">The task pane is the least discoverable area of a task page, and plain links aren't as visible as command buttons and task links.</span></span>
-   <span data-ttu-id="51077-251">針對內容區域中顯示的工作連結：</span><span class="sxs-lookup"><span data-stu-id="51077-251">For task links presented in the content area:</span></span>
    -   <span data-ttu-id="51077-252">**如果有7個以上的連結，請將連結分組為類別。**</span><span class="sxs-lookup"><span data-stu-id="51077-252">**If there are more than seven links, group the links into categories.**</span></span> <span data-ttu-id="51077-253">為每個群組提供標題。</span><span class="sxs-lookup"><span data-stu-id="51077-253">Provide headings for each of the groups.</span></span>
    -   <span data-ttu-id="51077-254">**針對少於7個的連結，請在沒有標題的單一群組中顯示連結。**</span><span class="sxs-lookup"><span data-stu-id="51077-254">**For fewer than seven links, present the links in a single group without a heading.**</span></span>
-   <span data-ttu-id="51077-255">**以邏輯順序呈現工作連結和按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-255">**Present task links and buttons in a logical order.**</span></span> <span data-ttu-id="51077-256">垂直列出工作連結，以水準方式列出命令按鈕。</span><span class="sxs-lookup"><span data-stu-id="51077-256">List task links vertically, command buttons horizontally.</span></span>
-   <span data-ttu-id="51077-257">在類別中， **將命令分成相關的群組。**</span><span class="sxs-lookup"><span data-stu-id="51077-257">Within categories, **divide the commands into related groups.**</span></span> <span data-ttu-id="51077-258">先放置最常用的工作群組，然後在每個群組內，先放置最常使用的工作。</span><span class="sxs-lookup"><span data-stu-id="51077-258">Present the task groups by placing the most commonly used first, and within each group, place the most commonly used tasks first.</span></span> <span data-ttu-id="51077-259">**產生的順序大致上應該遵循使用的可能性，但也有邏輯流程。**</span><span class="sxs-lookup"><span data-stu-id="51077-259">**The resulting order should roughly follow the likelihood of use, but also have a logical flow.**</span></span>
    -   <span data-ttu-id="51077-260">**例外狀況：** 導致執行所有作業的工作連結應先放置。</span><span class="sxs-lookup"><span data-stu-id="51077-260">**Exception:** Task links that result in doing everything should be placed first.</span></span>
-   <span data-ttu-id="51077-261">如果有許多工具的連結，請使用24x24 圖元圖示和兩行文字 **，讓最重要的工作成為更顯著的外觀**。</span><span class="sxs-lookup"><span data-stu-id="51077-261">**If there are many task links, give the most important tasks a more prominent appearance** by using a 24x24 pixel icon and two lines of text.</span></span> <span data-ttu-id="51077-262">針對較不重要的工作，請使用16x16 圖元圖示或無圖示，以及單行連結文字。</span><span class="sxs-lookup"><span data-stu-id="51077-262">For less important tasks, use a 16x16 pixel icon, or no icon, and a single line of link text.</span></span>

    ![<span data-ttu-id="51077-263">具有大型和小圖示的專案螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-263">screen shot of items with large and small icons</span></span> ](images/winenv-ctrl-panels-image4.png)

    <span data-ttu-id="51077-264">在此範例中，重要的命令會獲得更顯著的外觀。</span><span class="sxs-lookup"><span data-stu-id="51077-264">In this example, important commands are given a more prominent appearance.</span></span>

-   <span data-ttu-id="51077-265">**在經常使用的命令和破壞性命令之間有清楚的實體分隔。**</span><span class="sxs-lookup"><span data-stu-id="51077-265">**Have clear physical separation between frequently used commands and destructive commands.**</span></span> <span data-ttu-id="51077-266">否則，使用者可能會不小心按一下破壞性命令。</span><span class="sxs-lookup"><span data-stu-id="51077-266">Otherwise, users might click destructive commands accidentally.</span></span> <span data-ttu-id="51077-267">您可能需要重新排列命令的順序，以將破壞性命令放在一起。</span><span class="sxs-lookup"><span data-stu-id="51077-267">You may need to reorder your commands somewhat to put destructive commands together.</span></span>
-   <span data-ttu-id="51077-268">**提供在頁面上直接復原命令的機制。**</span><span class="sxs-lookup"><span data-stu-id="51077-268">**Provide the mechanism to undo commands directly on the page.**</span></span> <span data-ttu-id="51077-269">使用者不需要在其他地方流覽以復原錯誤。</span><span class="sxs-lookup"><span data-stu-id="51077-269">Users shouldn't have to navigate somewhere else to undo a mistake.</span></span>
-   <span data-ttu-id="51077-270">**針對工作連結，請使用所有預設工作連結圖示或所有自訂圖示。**</span><span class="sxs-lookup"><span data-stu-id="51077-270">**For task links, use either all default task link icons or all custom icons.**</span></span> <span data-ttu-id="51077-271">請勿混用。</span><span class="sxs-lookup"><span data-stu-id="51077-271">Don't mix them.</span></span> <span data-ttu-id="51077-272">請考慮只在下列情況使用自訂圖示：</span><span class="sxs-lookup"><span data-stu-id="51077-272">Consider using custom icons only if:</span></span>
    -   <span data-ttu-id="51077-273">它們可協助使用者熟練工作。</span><span class="sxs-lookup"><span data-stu-id="51077-273">They aid users in comprehending the tasks.</span></span>
    -   <span data-ttu-id="51077-274">它們符合 [Aero 圖示標準](vis-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-274">They comply with the [Aero icon standards](vis-icons.md).</span></span>
    -   <span data-ttu-id="51077-275">它們具有不顯眼的外觀。</span><span class="sxs-lookup"><span data-stu-id="51077-275">They have an unobtrusive appearance.</span></span>

<span data-ttu-id="51077-276">**對話方塊**</span><span class="sxs-lookup"><span data-stu-id="51077-276">**Dialog boxes**</span></span>

<span data-ttu-id="51077-277">使用工作流程時，您通常會想要讓工作在單一視窗內從頁面流向頁面，但下列情況除外。</span><span class="sxs-lookup"><span data-stu-id="51077-277">When using task flows, you generally want a task to flow from page to page within a single window, but the following circumstances are exceptions.</span></span> <span data-ttu-id="51077-278">在下列情況下，請使用對話方塊：</span><span class="sxs-lookup"><span data-stu-id="51077-278">Use dialog boxes in the following circumstances:</span></span>

-   <span data-ttu-id="51077-279">以提示使用者輸入系統管理員的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="51077-279">To prompt users for an administrator user name and password.</span></span> <span data-ttu-id="51077-280">基於此目的，請一律使用 [認證管理員] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="51077-280">Always use the credential manager dialog box for this purpose.</span></span> <span data-ttu-id="51077-281"> ([應為強制](glossary.md)回應。 ) </span><span class="sxs-lookup"><span data-stu-id="51077-281">(Should be [modal](glossary.md).)</span></span>
-   <span data-ttu-id="51077-282">使用工作對話方塊或訊息方塊確認就地命令。</span><span class="sxs-lookup"><span data-stu-id="51077-282">To confirm an in-place command using a task dialog or message box.</span></span> <span data-ttu-id="51077-283"> (應為強制回應。 ) </span><span class="sxs-lookup"><span data-stu-id="51077-283">(Should be modal.)</span></span>
-   <span data-ttu-id="51077-284">取得就地命令的輸入，例如新的、新增、另存新檔、重新命名和列印命令。</span><span class="sxs-lookup"><span data-stu-id="51077-284">To get input for in-place commands, such as for New, Add, Save As, Rename, and Print commands.</span></span>

    ![<span data-ttu-id="51077-285">[刪除網路位置] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-285">screen shot of delete network locations dialog box</span></span> ](images/winenv-ctrl-panels-image5.png)

    <span data-ttu-id="51077-286">在此範例中，Delete 命令會在對話方塊中執行，而不是在不同的頁面上執行。</span><span class="sxs-lookup"><span data-stu-id="51077-286">In this example, the Delete command is performed in a dialog box instead of a separate page.</span></span>

-   <span data-ttu-id="51077-287">執行次要的獨立工作。</span><span class="sxs-lookup"><span data-stu-id="51077-287">To perform secondary, stand-alone tasks.</span></span> <span data-ttu-id="51077-288">使用非 [模式](glossary.md)的次要視窗可讓您獨立執行這類工作，並在主要工作流程之外執行。</span><span class="sxs-lookup"><span data-stu-id="51077-288">Using a [modeless](glossary.md), secondary window allows such tasks to be performed independently and outside the main task flow.</span></span>

### <a name="hub-pages"></a><span data-ttu-id="51077-289">中樞頁面</span><span class="sxs-lookup"><span data-stu-id="51077-289">Hub pages</span></span>

<span data-ttu-id="51077-290">**一般**</span><span class="sxs-lookup"><span data-stu-id="51077-290">**General**</span></span>

-   <span data-ttu-id="51077-291">在下列情況中使用以工作為基礎的中樞頁面：</span><span class="sxs-lookup"><span data-stu-id="51077-291">Use task-based hub pages when:</span></span>
    -   <span data-ttu-id="51077-292">**有少量的常用或重要工作。**</span><span class="sxs-lookup"><span data-stu-id="51077-292">**There are a small number of commonly used or important tasks.**</span></span>
    -   <span data-ttu-id="51077-293">設定 **包含一或兩個物件** (範例：監視器、鍵盤、滑鼠、遊戲控制器) 。</span><span class="sxs-lookup"><span data-stu-id="51077-293">**The configuration involves one or two objects** (examples: monitors, keyboard, mouse, game controllers).</span></span>
    -   <span data-ttu-id="51077-294">設定會 **套用整個系統的** (範例：日期和時間、安全性、電源選項) 。</span><span class="sxs-lookup"><span data-stu-id="51077-294">**The configuration applies system-wide** (examples: date and time, security, power options).</span></span>
-   <span data-ttu-id="51077-295">使用以物件為基礎的中樞頁面的時機：</span><span class="sxs-lookup"><span data-stu-id="51077-295">Use object-based hub pages when:</span></span>
    -   <span data-ttu-id="51077-296">設定 **可能涉及數個物件** (範例：使用者帳戶、網路連線、印表機) 。</span><span class="sxs-lookup"><span data-stu-id="51077-296">**The configuration could involve several objects** (examples: user accounts, network connections, printers).</span></span>
    -   <span data-ttu-id="51077-297">設定 **只會套用至選取的物件**。</span><span class="sxs-lookup"><span data-stu-id="51077-297">**The configuration applies only to the selected object**.</span></span>
-   <span data-ttu-id="51077-298">如果 [控制台] 專案具有包含所有相關工作和屬性的 **單一頁面，請勿使用 [中樞] 頁面**。</span><span class="sxs-lookup"><span data-stu-id="51077-298">**Don't use a hub page if the control panel item has a single page** that contains all the tasks and properties involved.</span></span>

<span data-ttu-id="51077-299">**物件清單**</span><span class="sxs-lookup"><span data-stu-id="51077-299">**Object lists**</span></span>

-   <span data-ttu-id="51077-300">**依邏輯順序列出專案。**</span><span class="sxs-lookup"><span data-stu-id="51077-300">**List items in a logical order.**</span></span> <span data-ttu-id="51077-301">依字母順序排序命名物件、依數位順序排序的數位和日期（以時間順序排列）。</span><span class="sxs-lookup"><span data-stu-id="51077-301">Sort named objects in alphabetical order, numbers in numeric order, and dates in chronological order.</span></span>
-   <span data-ttu-id="51077-302">如果是以物件為基礎的中樞，請 **在工作窗格中提供 [物件檢視] 命令（如果變更視圖的能力對工作很重要**）。</span><span class="sxs-lookup"><span data-stu-id="51077-302">For object-based hubs, **provide object view commands in the task pane if the ability to change the view is important to the tasks**.</span></span> <span data-ttu-id="51077-303">如果有許多物件，且預設的簡報在所有案例中都無法正常運作，則變更視圖的能力很重要。</span><span class="sxs-lookup"><span data-stu-id="51077-303">The ability to change views is important if there are many objects and the default presentation doesn't work well for all scenarios.</span></span> <span data-ttu-id="51077-304">即使沒有明確的命令透過清單視圖操作功能表，使用者也可以變更清單視圖，但較不容易找到。</span><span class="sxs-lookup"><span data-stu-id="51077-304">Users can change the list view even if there aren't explicit commands through the list view context menu, but it's less discoverable.</span></span>

<span data-ttu-id="51077-305">如需有關呈現物件清單的詳細指導方針，請參閱 [清單視圖](ctrl-list-views.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-305">For more guidelines about presenting object lists, see [List Views](ctrl-list-views.md).</span></span>

<span data-ttu-id="51077-306">**互動**</span><span class="sxs-lookup"><span data-stu-id="51077-306">**Interaction**</span></span>

-   <span data-ttu-id="51077-307">**不要在中樞頁面上放置認可按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-307">**Don't put commit buttons on hub pages.**</span></span> <span data-ttu-id="51077-308">中樞頁面基本上是啟動點。</span><span class="sxs-lookup"><span data-stu-id="51077-308">Hub pages are fundamentally launch points.</span></span> <span data-ttu-id="51077-309">使用者永遠不會「認可」中樞頁面，而不會使用它們來進行。</span><span class="sxs-lookup"><span data-stu-id="51077-309">Users never "commit" hub pages they are never done with them.</span></span> <span data-ttu-id="51077-310">中樞頁面上的 [認可] 按鈕讓任何從中樞啟動的工作變得令人困惑 (使用者會想要知道這些工作是否需要) 認可。</span><span class="sxs-lookup"><span data-stu-id="51077-310">And commit buttons on hub pages make any tasks initiated from a hub confusing (users will wonder if those tasks need to be committed).</span></span>
    -   <span data-ttu-id="51077-311">**例外狀況：** 如果變更設定需要提高 [許可權](glossary.md)，請提供具有 [安全性保護盾圖示](winenv-uac.md)的 [套用] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="51077-311">**Exception:** If changing a setting requires [elevation](glossary.md), provide an Apply button with a [security shield icon](winenv-uac.md).</span></span> <span data-ttu-id="51077-312">一旦套用變更之後，請停用 [認可] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="51077-312">Disable the commit button once changes have been applied.</span></span>
-   <span data-ttu-id="51077-313">**請考慮直接在中樞頁面上放置最有用的屬性。**</span><span class="sxs-lookup"><span data-stu-id="51077-313">**Consider putting the most useful properties directly on hub pages.**</span></span> <span data-ttu-id="51077-314">當使用者最有可能使用主控台來存取這些屬性時，強烈建議使用這類混合式中樞頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-314">Such hybrid hub pages are strongly recommended when users are most likely to use Control Panel to access those properties.</span></span>

    ![<span data-ttu-id="51077-315">電源選項中樞頁面的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-315">screen shot of power options hub page</span></span> ](images/winenv-ctrl-panels-image6.png)

    <span data-ttu-id="51077-316">在此範例中，電源選項控制台專案在中樞頁面上直接具有最有用的設定。</span><span class="sxs-lookup"><span data-stu-id="51077-316">In this example, the Power Options control panel item has the most useful settings directly on the hub page.</span></span>

-   <span data-ttu-id="51077-317">**針對混合式中樞頁面上的任何設定使用立即認可模型，以便立即進行變更。**</span><span class="sxs-lookup"><span data-stu-id="51077-317">**Use an immediate commit model for any settings on hybrid hub pages so that changes are made immediately.**</span></span> <span data-ttu-id="51077-318">同樣地，使用者永遠不會認可中樞頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-318">Again, users never commit a hub page.</span></span> <span data-ttu-id="51077-319">如果設定需要 [認可] 按鈕，請不要將它放在中樞頁面上。</span><span class="sxs-lookup"><span data-stu-id="51077-319">If a setting requires a commit button, don't put it on a hub page.</span></span>
-   <span data-ttu-id="51077-320">**請考慮直接在中樞頁面上放置簡單的「單一步驟」命令，而不是使用導覽連結。**</span><span class="sxs-lookup"><span data-stu-id="51077-320">**Consider putting simple, "one-step" commands directly on hub pages instead of using navigation links.**</span></span>
-   <span data-ttu-id="51077-321">**確認無法輕鬆復原其效果的就地命令。**</span><span class="sxs-lookup"><span data-stu-id="51077-321">**Confirm in-place commands whose effects cannot be easily undone.**</span></span> <span data-ttu-id="51077-322">使用工作 [對話方塊](win-dialog-box.md) 或 [訊息方塊](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-322">Use a [task dialog](win-dialog-box.md) or [message box](glossary.md).</span></span>

    ![<span data-ttu-id="51077-323">[確認刪除] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-323">screen shot of confirm delete dialog box</span></span> ](images/winenv-ctrl-panels-image7.png)

    <span data-ttu-id="51077-324">在此範例中，會使用對話方塊確認刪除命令。</span><span class="sxs-lookup"><span data-stu-id="51077-324">In this example, the Delete command is confirmed with a dialog box.</span></span>

-   <span data-ttu-id="51077-325">**如果是以工作為基礎的中樞頁面，請使用工作連結和圖示來識別每項工作。**</span><span class="sxs-lookup"><span data-stu-id="51077-325">**For task-based hub pages, identify each task with a task link and an icon.**</span></span> <span data-ttu-id="51077-326">您也可以為每個連結提供選擇性的描述。</span><span class="sxs-lookup"><span data-stu-id="51077-326">You can also provide an optional description for each link.</span></span> <span data-ttu-id="51077-327">不過，請試著讓工作連結一目了然，並只針對真正需要的連結提供選擇性描述。</span><span class="sxs-lookup"><span data-stu-id="51077-327">However, try to make the task links self-explanatory and provide optional descriptions only to links that really need them.</span></span>

    ![<span data-ttu-id="51077-328">[電腦效能中樞] 頁面的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-328">screen shot of computer performance hub page</span></span> ](images/winenv-ctrl-panels-image8.png)

    <span data-ttu-id="51077-329">在此範例中，每個工作都有一個工作連結和一個圖示。</span><span class="sxs-lookup"><span data-stu-id="51077-329">In this example, each task has a task link and an icon.</span></span>

-   <span data-ttu-id="51077-330">**如果是以物件為基礎的中樞頁面，請按一下 [選取物件]，然後按兩下 [選取物件] 並導覽至其預設頁面。**</span><span class="sxs-lookup"><span data-stu-id="51077-330">**For object-based hub pages, single-clicking selects objects, and double-clicking selects an object and navigates to its default page.**</span></span> <span data-ttu-id="51077-331">預設頁面通常是屬性頁或以工作為基礎的中樞頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-331">The default page is typically a property page or a task-based hub page.</span></span>
-   <span data-ttu-id="51077-332">**以物件為基礎的中樞頁面可能會針對選取的物件流覽至以工作為基礎的中樞。**</span><span class="sxs-lookup"><span data-stu-id="51077-332">**An object-based hub page may navigate to a task-based hub for the selected objects.**</span></span> <span data-ttu-id="51077-333">不過，您應該避免這類次要中樞，因為它們會讓 [控制台] 專案感覺太間接。</span><span class="sxs-lookup"><span data-stu-id="51077-333">However, such secondary hubs should be avoided because they make a control panel item feel too indirect.</span></span>

<span data-ttu-id="51077-334">**工作窗格**</span><span class="sxs-lookup"><span data-stu-id="51077-334">**Task panes**</span></span>

<span data-ttu-id="51077-335">使用工作窗格來呈現命令、流覽和相關控制台專案的連結。</span><span class="sxs-lookup"><span data-stu-id="51077-335">Use task panes to present links to commands, views, and related control panel items.</span></span>

-   <span data-ttu-id="51077-336">針對以工作為基礎的中樞中的工作窗格，以下列順序呈現連結：</span><span class="sxs-lookup"><span data-stu-id="51077-336">For task panes in task-based hubs, present links in the following order:</span></span>
    -   <span data-ttu-id="51077-337">**次要命令**。</span><span class="sxs-lookup"><span data-stu-id="51077-337">**Secondary commands**.</span></span> <span data-ttu-id="51077-338">只在內容區域中顯示主要工作。</span><span class="sxs-lookup"><span data-stu-id="51077-338">Present primary tasks only in the content area.</span></span> <span data-ttu-id="51077-339">使用工作窗格進行次要、選擇性的工作。</span><span class="sxs-lookup"><span data-stu-id="51077-339">Use the task pane for secondary, optional tasks.</span></span> <span data-ttu-id="51077-340">如果使用者必須在重要案例中探索，請考慮使用主要工作;次要（如果使用者可以接受的話）。</span><span class="sxs-lookup"><span data-stu-id="51077-340">Consider a task primary if users must discover it in important scenarios; secondary if it's acceptable for users not to discover it.</span></span>
    -   <span data-ttu-id="51077-341">另 **請參閱**。</span><span class="sxs-lookup"><span data-stu-id="51077-341">**See also**.</span></span> <span data-ttu-id="51077-342">流覽至相關控制台專案的選擇性連結。</span><span class="sxs-lookup"><span data-stu-id="51077-342">The optional links that navigate to related control panel items.</span></span>
-   <span data-ttu-id="51077-343">針對以物件為基礎的中樞中的工作窗格，以下列順序呈現連結：</span><span class="sxs-lookup"><span data-stu-id="51077-343">For task panes in object-based hubs, present links in the following order:</span></span>
    -   <span data-ttu-id="51077-344">**物件檢視**。</span><span class="sxs-lookup"><span data-stu-id="51077-344">**Object views**.</span></span> <span data-ttu-id="51077-345">選用的連結，可用來控制物件的呈現方式。</span><span class="sxs-lookup"><span data-stu-id="51077-345">The optional links used to control the presentation of the objects.</span></span>
    -   <span data-ttu-id="51077-346">已 **修正的命令**。</span><span class="sxs-lookup"><span data-stu-id="51077-346">**Fixed commands**.</span></span> <span data-ttu-id="51077-347">與目前選取的物件無關的命令。</span><span class="sxs-lookup"><span data-stu-id="51077-347">The commands that are independent of the currently selected objects.</span></span>
    -   <span data-ttu-id="51077-348">內容 **相關命令**。</span><span class="sxs-lookup"><span data-stu-id="51077-348">**Contextual commands**.</span></span> <span data-ttu-id="51077-349">這些命令相依于目前選取的物件，因此不一定會顯示。</span><span class="sxs-lookup"><span data-stu-id="51077-349">The commands that depend on the currently selected objects, and are therefore not always displayed.</span></span>
    -   <span data-ttu-id="51077-350">另 **請參閱**。</span><span class="sxs-lookup"><span data-stu-id="51077-350">**See also**.</span></span> <span data-ttu-id="51077-351">流覽至相關控制台專案的選擇性連結。</span><span class="sxs-lookup"><span data-stu-id="51077-351">The optional links that navigate to related control panel items.</span></span>
-   <span data-ttu-id="51077-352">**請勿在輪輻頁面中使用工作窗格。**</span><span class="sxs-lookup"><span data-stu-id="51077-352">**Don't use task panes in spoke pages.**</span></span> <span data-ttu-id="51077-353">不同于中樞頁面，輪輻頁面應著重于完成工作。</span><span class="sxs-lookup"><span data-stu-id="51077-353">Unlike hub pages, spoke pages should be focused on completing the task.</span></span> <span data-ttu-id="51077-354">您不想要鼓勵使用者在完成前離開。</span><span class="sxs-lookup"><span data-stu-id="51077-354">You don't want to encourage users to navigate away before completion.</span></span>

<span data-ttu-id="51077-355">**另請參閱連結**</span><span class="sxs-lookup"><span data-stu-id="51077-355">**See also links**</span></span>

-   <span data-ttu-id="51077-356">**提供 [工作] 窗格中的 [另請參閱] 連結，以協助使用者尋找相關的控制台專案，如果有錯誤，則為右邊的 [控制台] 專案。**</span><span class="sxs-lookup"><span data-stu-id="51077-356">**Provide See also links in the task pane to help users find related control panel items, or the right control panel item if they have the wrong one.**</span></span> <span data-ttu-id="51077-357">連結至使用者可能與您的控制台專案相關聯的專案。</span><span class="sxs-lookup"><span data-stu-id="51077-357">Link to items users are likely to associate with your control panel item.</span></span>

    ![<span data-ttu-id="51077-358">控制中心 [另請參閱] 連結的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-358">screen shot of action center 'see also' links</span></span> ](images/winenv-ctrl-panels-image9.png)

    <span data-ttu-id="51077-359">在此範例中，「動作中心控制台」專案會連結到相關的控制台專案。</span><span class="sxs-lookup"><span data-stu-id="51077-359">In this example, the Action Center control panel item links to related control panel items.</span></span>

-   <span data-ttu-id="51077-360">**如果是使用者更可能辨識的，則連結至特定的工作頁面。**</span><span class="sxs-lookup"><span data-stu-id="51077-360">**Link to a specific task page if that is what users are more likely to recognize.**</span></span> <span data-ttu-id="51077-361">否則，連結至整個 [控制台] 專案。</span><span class="sxs-lookup"><span data-stu-id="51077-361">Otherwise, link to the entire control panel item.</span></span> <span data-ttu-id="51077-362">使用 [控制台] 名稱，而不新增 [片語]、[控制台]。</span><span class="sxs-lookup"><span data-stu-id="51077-362">Use the control panel name without adding the phrase, control panel.</span></span>

### <a name="spoke-pages"></a><span data-ttu-id="51077-363">輪輻頁面</span><span class="sxs-lookup"><span data-stu-id="51077-363">Spoke pages</span></span>

<span data-ttu-id="51077-364">**一般**</span><span class="sxs-lookup"><span data-stu-id="51077-364">**General**</span></span>

-   <span data-ttu-id="51077-365">**在使用者需要更多指引和說明的情況下，使用工作頁面進行常用或重要的工作。**</span><span class="sxs-lookup"><span data-stu-id="51077-365">**Use task pages for commonly used or important tasks where users need more guidance and explanation.**</span></span>
-   <span data-ttu-id="51077-366">**將表單頁面用於具有許多設定的功能，並受益于直接的單一頁面呈現。**</span><span class="sxs-lookup"><span data-stu-id="51077-366">**Use form pages for features that have many settings and benefit from a direct, single-page presentation.**</span></span> <span data-ttu-id="51077-367">這類頁面的理想工作通常涉及一些簡單屬性的明顯變更。</span><span class="sxs-lookup"><span data-stu-id="51077-367">The ideal tasks for such pages typically involve obvious changes to a few simple properties.</span></span>
-   <span data-ttu-id="51077-368">**請勿在輪輻頁面中使用工作窗格。**</span><span class="sxs-lookup"><span data-stu-id="51077-368">**Don't use task panes in spoke pages.**</span></span>

<span data-ttu-id="51077-369">**互動**</span><span class="sxs-lookup"><span data-stu-id="51077-369">**Interaction**</span></span>

-   <span data-ttu-id="51077-370">**嘗試將主要工作限制在單一頁面上。**</span><span class="sxs-lookup"><span data-stu-id="51077-370">**Try to limit main tasks to a single page.**</span></span> <span data-ttu-id="51077-371">如果需要一個以上的頁面，您可以：</span><span class="sxs-lookup"><span data-stu-id="51077-371">If more than one page is required, you can:</span></span>
    -   <span data-ttu-id="51077-372">**使用中繼輪輻頁面進行其他或選擇性的步驟。**</span><span class="sxs-lookup"><span data-stu-id="51077-372">**Use intermediate spoke pages for additional or optional steps.**</span></span> <span data-ttu-id="51077-373">中繼輪輻頁面是由最終輪輻頁面所認可。</span><span class="sxs-lookup"><span data-stu-id="51077-373">Intermediate spoke pages are committed by the final spoke page.</span></span>
    -   <span data-ttu-id="51077-374">**針對獨立的輔助工作使用獨立的視窗。**</span><span class="sxs-lookup"><span data-stu-id="51077-374">**Use independent windows for independent auxiliary tasks.**</span></span> <span data-ttu-id="51077-375">獨立的視窗會自行認可，而獨立于主要工作。</span><span class="sxs-lookup"><span data-stu-id="51077-375">Independent windows are committed on their own, and independently of the main task.</span></span>

<span data-ttu-id="51077-376">這樣做會將主要工作的認可按鈕意義保持明確且明確。</span><span class="sxs-lookup"><span data-stu-id="51077-376">Doing so keeps the meaning of the commit buttons for the main task clear and unambiguous.</span></span> <span data-ttu-id="51077-377">使用者應該一律安心瞭解他們正在認可哪些內容。</span><span class="sxs-lookup"><span data-stu-id="51077-377">Users should always be confident in understanding what they are committing to.</span></span>

-   <span data-ttu-id="51077-378">**請勿使用工作流程中的 [另請參閱] 連結。**</span><span class="sxs-lookup"><span data-stu-id="51077-378">**Don't use See Also links within a task flow.**</span></span> <span data-ttu-id="51077-379">這些連結會連結到相關但不同的控制台專案。</span><span class="sxs-lookup"><span data-stu-id="51077-379">These link to related, but different, control panel items.</span></span> <span data-ttu-id="51077-380">雖然中樞頁面中可接受流覽至不同的專案，但它不在輪輻頁面中，因為這樣做會中斷工作。</span><span class="sxs-lookup"><span data-stu-id="51077-380">Although navigating to a different item is acceptable in hub pages, it is not in spoke pages, because doing so interrupts the task.</span></span>
-   <span data-ttu-id="51077-381">**請勿使用輪輻頁面來進行簡單的輸入或確認。**</span><span class="sxs-lookup"><span data-stu-id="51077-381">**Don't use spoke pages for simple input or confirmations.**</span></span> <span data-ttu-id="51077-382">請改用強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="51077-382">Use modal dialog boxes instead.</span></span>

<span data-ttu-id="51077-383">**(中繼輪輻頁面) 的互動**</span><span class="sxs-lookup"><span data-stu-id="51077-383">**Interaction (intermediate spoke pages)**</span></span>

-   <span data-ttu-id="51077-384">**使用 [工作連結] 或 [下一步] 按鈕流覽至下一個頁面。**</span><span class="sxs-lookup"><span data-stu-id="51077-384">**Use task links or a Next button to navigate to the next page.**</span></span> <span data-ttu-id="51077-385">繼續進行下一個步驟的方法應該一律很明顯。</span><span class="sxs-lookup"><span data-stu-id="51077-385">The way to proceed to the next step should always be obvious.</span></span>
-   <span data-ttu-id="51077-386">**您可以有選擇性工作步驟的導覽連結。**</span><span class="sxs-lookup"><span data-stu-id="51077-386">**You can have navigation links to optional task steps.**</span></span> <span data-ttu-id="51077-387">為了避免使用者認可工作時的混淆，這些額外的頁面應該是相同 [控制台] 專案內的中繼頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-387">To avoid confusion when users commit to the task, those extra pages should be intermediate pages within the same control panel item.</span></span> <span data-ttu-id="51077-388">他們不應該有認可按鈕，但應在認可主要工作時認可。</span><span class="sxs-lookup"><span data-stu-id="51077-388">They shouldn't have commit buttons, but should be committed when the main task is committed.</span></span>

<span data-ttu-id="51077-389">**(最終輪輻頁面) 的互動**</span><span class="sxs-lookup"><span data-stu-id="51077-389">**Interaction (final spoke pages)**</span></span>

-   <span data-ttu-id="51077-390">**使用 [認可] 按鈕來完成工作。**</span><span class="sxs-lookup"><span data-stu-id="51077-390">**Use commit buttons to complete a task.**</span></span> <span data-ttu-id="51077-391">針對輪輻頁面使用 [延遲的認可模型](glossary.md) ，如此一來，在明確認可的情況下才會進行變更 (如果使用者離開使用上一頁、Close 或 Address bar，變更就會) 放棄。</span><span class="sxs-lookup"><span data-stu-id="51077-391">Use a [delayed commit model](glossary.md) for spoke pages, so that changes aren't made until explicitly committed (if users navigate away using Back, Close, or the Address bar, changes are abandoned).</span></span> <span data-ttu-id="51077-392">認可按鈕是使用者即將完成工作的視覺線索。</span><span class="sxs-lookup"><span data-stu-id="51077-392">The commit buttons are a visual clue that the user is about to complete a task.</span></span> <span data-ttu-id="51077-393">請勿使用連結來進行此用途。</span><span class="sxs-lookup"><span data-stu-id="51077-393">Don't use links for this purpose.</span></span>
-   <span data-ttu-id="51077-394">**請勿確認認可按鈕 (包括取消) 。**</span><span class="sxs-lookup"><span data-stu-id="51077-394">**Don't confirm commit buttons (including Cancel).**</span></span> <span data-ttu-id="51077-395">這樣做可能會很麻煩。</span><span class="sxs-lookup"><span data-stu-id="51077-395">Doing so can be annoying.</span></span> <span data-ttu-id="51077-396">例外狀況：</span><span class="sxs-lookup"><span data-stu-id="51077-396">Exceptions:</span></span>
    -   <span data-ttu-id="51077-397">此動作會產生顯著的後果，如果不正確，則無法立即修復。</span><span class="sxs-lookup"><span data-stu-id="51077-397">The action has significant consequences and, if incorrect, not readily fixable.</span></span>
    -   <span data-ttu-id="51077-398">此動作可能會導致使用者的時間或工作大幅遺失。</span><span class="sxs-lookup"><span data-stu-id="51077-398">The action may result in a significant loss of the user's time or effort.</span></span>
    -   <span data-ttu-id="51077-399">動作與其他動作明顯不一致。</span><span class="sxs-lookup"><span data-stu-id="51077-399">The action is clearly inconsistent with other actions.</span></span>
-   <span data-ttu-id="51077-400">請勿使用 [上一步]、[關閉] 或 [網址] 列來 **確認使用者是否放棄變更**。</span><span class="sxs-lookup"><span data-stu-id="51077-400">**Don't confirm if users abandon changes** by navigating away using Back, Close, or the Address bar.</span></span> <span data-ttu-id="51077-401">不過，您可以確認可能的非預期流覽可能會導致使用者的時間或工作大幅遺失。</span><span class="sxs-lookup"><span data-stu-id="51077-401">However, you may confirm if a potentially unintended navigation may result in a significant loss of the user's time or effort.</span></span>
-   <span data-ttu-id="51077-402">**請勿使用命令或導覽連結** (包括 [另請參閱連結]) 。</span><span class="sxs-lookup"><span data-stu-id="51077-402">**Don't use command or navigation links** (including See also links).</span></span> <span data-ttu-id="51077-403">在最終輪輻頁面上，使用者應該明確地完成或取消工作。</span><span class="sxs-lookup"><span data-stu-id="51077-403">On final spoke pages, users should explicitly complete or cancel the task.</span></span> <span data-ttu-id="51077-404">不建議使用者在其他地方流覽，因為這樣做可能會隱含地取消工作。</span><span class="sxs-lookup"><span data-stu-id="51077-404">Users should not be encouraged to navigate somewhere else, because doing so would likely cancel the task implicitly.</span></span>
-   <span data-ttu-id="51077-405">**當使用者完成或取消工作時，應該會將其傳送回已啟動工作的中樞頁面。**</span><span class="sxs-lookup"><span data-stu-id="51077-405">**When users complete or cancel a task, they should be sent back to the hub page from which the task was launched.**</span></span> <span data-ttu-id="51077-406">如果沒有這類頁面，請改為關閉 [控制台] 視窗。</span><span class="sxs-lookup"><span data-stu-id="51077-406">If there is no such page, close the control panel window instead.</span></span> <span data-ttu-id="51077-407">請勿假設輪輻頁面一律會從另一個頁面啟動。</span><span class="sxs-lookup"><span data-stu-id="51077-407">Don't assume that spoke pages are always launched from another page.</span></span>
-   <span data-ttu-id="51077-408">當您將使用者回到從中啟動工作的頁面時，請 **從 Windows 檔案總管回堆疊中移除過時的**「已認可」頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-408">**Remove the stale "committed" pages from the Windows Explorer Back stack** when you return users back to the page that the task was launched from.</span></span> <span data-ttu-id="51077-409">當使用者按一下 [上一頁] 按鈕時，應該永遠不會看到他們已經認可的頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-409">Users should never see the pages that they have already committed to when clicking the Back button.</span></span> <span data-ttu-id="51077-410">使用者應該一律透過完全重做工作來進行其他變更，而不是按一下 [上一步] 來修改過時的頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-410">Users should always make additional changes by completely redoing the task instead of clicking Back to modify stale pages.</span></span>
    -   <span data-ttu-id="51077-411">**開發人員：** 您可以使用 ITravelLog：： FindTravelEntry () 和 ITravelLogEx：:D eleteEntry () Api 來移除這些過時的頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-411">**Developers:** You can remove these stale pages using the ITravelLog::FindTravelEntry() and ITravelLogEx::DeleteEntry() APIs.</span></span>

<span data-ttu-id="51077-412">**認可按鈕**</span><span class="sxs-lookup"><span data-stu-id="51077-412">**Commit buttons**</span></span>

<span data-ttu-id="51077-413">**注意：** 取消按鈕會被視為認可按鈕。</span><span class="sxs-lookup"><span data-stu-id="51077-413">**Note:** Cancel buttons are considered to be commit buttons.</span></span>

-   <span data-ttu-id="51077-414">**使用對主要指示的特定回應來確認工作，而不是一般標籤（例如 [確定]）。**</span><span class="sxs-lookup"><span data-stu-id="51077-414">**Confirm tasks using commit buttons that are specific responses to the main instruction, instead of generic labels such as OK.**</span></span> <span data-ttu-id="51077-415">認可按鈕上的標籤應該有意義。</span><span class="sxs-lookup"><span data-stu-id="51077-415">The labels on commit buttons should make sense on their own.</span></span> <span data-ttu-id="51077-416">請避免使用 [確定]，因為它不是主要指示的特定回應，因此更容易誤解。</span><span class="sxs-lookup"><span data-stu-id="51077-416">Avoid using OK because it isn't a specific response to the main instruction, and therefore easier to misunderstand.</span></span> <span data-ttu-id="51077-417">此外，[確定] 通常會搭配強制回應對話方塊使用，並不正確地表示關閉 [控制台] 專案視窗。</span><span class="sxs-lookup"><span data-stu-id="51077-417">Furthermore, OK is typically used with modal dialog boxes and incorrectly implies closing the control panel item window.</span></span>
    -   <span data-ttu-id="51077-418">**異常：**</span><span class="sxs-lookup"><span data-stu-id="51077-418">**Exceptions:**</span></span>
        -   <span data-ttu-id="51077-419">針對沒有設定的頁面，請使用 [確定]。</span><span class="sxs-lookup"><span data-stu-id="51077-419">Use OK for pages that don't have settings.</span></span>
        -   <span data-ttu-id="51077-420">當特定回應仍為一般（例如 [儲存]、[選取] 或 [選擇]）時，請使用 [確定]，就像變更特定設定或設定集合一樣。</span><span class="sxs-lookup"><span data-stu-id="51077-420">Use OK when the specific response is still generic, such as Save, Select, or Choose, as when changing a specific setting or a collection of settings.</span></span>
        -   <span data-ttu-id="51077-421">如果頁面有回應主要指示的選項按鈕，請使用 [確定]。</span><span class="sxs-lookup"><span data-stu-id="51077-421">Use OK if the page has radio buttons that are responses to the main instruction.</span></span> <span data-ttu-id="51077-422">若要維護延遲的認可模型，您無法使用最終輪輻頁面上的工作連結。</span><span class="sxs-lookup"><span data-stu-id="51077-422">To maintain the delayed commit model, you can't use task links on a final spoke page.</span></span>

            ![<span data-ttu-id="51077-423">具有 [確定] 按鈕之 web 限制的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-423">screen shot of web restrictions with ok button</span></span> ](images/winenv-ctrl-panels-image10.png)

            <span data-ttu-id="51077-424">在此範例中，選項按鈕（而非認可按鈕）會回應主要指令。</span><span class="sxs-lookup"><span data-stu-id="51077-424">In this example, the radio buttons, not the commit buttons, are responses to the main instruction.</span></span>
-   <span data-ttu-id="51077-425">**提供 [取消] 按鈕，讓使用者明確放棄變更。**</span><span class="sxs-lookup"><span data-stu-id="51077-425">**Provide a Cancel button to let users explicitly abandon changes.**</span></span> <span data-ttu-id="51077-426">雖然使用者可以藉由不確認其變更而隱含地放棄工作，但是提供 [取消] 按鈕可讓他們更有信心地進行工作。</span><span class="sxs-lookup"><span data-stu-id="51077-426">While users can implicitly abandon a task by not confirming their changes, providing a Cancel button allows them to do so with greater confidence.</span></span>
    -   <span data-ttu-id="51077-427">**例外狀況：** 請勿為使用者無法進行變更的工作提供 [取消] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="51077-427">**Exception:** Don't provide a Cancel button for tasks where users can't make changes.</span></span> <span data-ttu-id="51077-428">在此情況下，[確定] 按鈕的效果與 [取消] 相同。</span><span class="sxs-lookup"><span data-stu-id="51077-428">The OK button has the same effect as Cancel in this case.</span></span>
-   <span data-ttu-id="51077-429">**請勿使用 [關閉]、[完成] 或 [完成] 認可按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-429">**Don't use Close, Done, or Finish commit buttons.**</span></span> <span data-ttu-id="51077-430">這些按鈕通常會搭配強制回應對話方塊使用，並不正確地表示關閉 [控制台專案] 視窗。</span><span class="sxs-lookup"><span data-stu-id="51077-430">These buttons are typically used with modal dialog boxes and incorrectly imply closing the control panel item window.</span></span> <span data-ttu-id="51077-431">使用者可以使用標題列上的 [關閉] 按鈕來關閉視窗。</span><span class="sxs-lookup"><span data-stu-id="51077-431">Users can close the window using the Close button on the title bar.</span></span> <span data-ttu-id="51077-432">此外，[完成] 和 [完成] 會誤導，因為使用者會回到從中啟動工作的頁面，因此它們並不是真的完成。</span><span class="sxs-lookup"><span data-stu-id="51077-432">Also, Done and Finish are misleading because users are returned to the page where the task was launched from, so they aren't really done.</span></span>
-   <span data-ttu-id="51077-433">**不要停用認可按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-433">**Don't disable commit buttons.**</span></span> <span data-ttu-id="51077-434">否則使用者必須推算認可按鈕停用的原因。</span><span class="sxs-lookup"><span data-stu-id="51077-434">Otherwise users have to deduce why the commit buttons are disabled.</span></span> <span data-ttu-id="51077-435">最好讓認可按鈕保持啟用狀態，並在發生問題時提供實用的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="51077-435">It's better to leave commit buttons enabled, and give a helpful error message whenever there is a problem.</span></span>
-   <span data-ttu-id="51077-436">**請確定頁面上顯示的認可按鈕沒有滾動。**</span><span class="sxs-lookup"><span data-stu-id="51077-436">**Make sure the commit buttons appear on the page without scrolling.**</span></span> <span data-ttu-id="51077-437">如果頁面很長，您可以將 [認可] 按鈕放在 [命令區域](glossary.md)中，而不是在內容區域中，藉此顯示這些按鈕。</span><span class="sxs-lookup"><span data-stu-id="51077-437">If the page is long, you can make commit buttons always visible by placing them in a [command area](glossary.md), instead of in the content area.</span></span>

    ![<span data-ttu-id="51077-438">[自動播放] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-438">screen shot of autoplay dialog box</span></span> ](images/winenv-ctrl-panels-image11.png)

    <span data-ttu-id="51077-439">在此範例中，內容區域大小未系結，因此認可按鈕會置於命令區域中。</span><span class="sxs-lookup"><span data-stu-id="51077-439">In this example, content area size is unbounded, so the commit buttons are placed in the command area.</span></span>

-   <span data-ttu-id="51077-440">將認可按鈕靠右對齊，並使用此順序 (從左至右) ：正面的認可按鈕、取消及套用。</span><span class="sxs-lookup"><span data-stu-id="51077-440">Right-align the commit buttons and use this order (from left to right): positive commit buttons, Cancel, and Apply.</span></span>

<span data-ttu-id="51077-441">**預覽按鈕**</span><span class="sxs-lookup"><span data-stu-id="51077-441">**Preview buttons**</span></span>

-   <span data-ttu-id="51077-442">請確定 **[預覽] 按鈕表示立即套用暫止的變更，但如果使用者離開頁面而未認可變更，則還原目前的設定。**</span><span class="sxs-lookup"><span data-stu-id="51077-442">Make sure **the Preview button means to apply the pending changes now but restore the current settings if users navigate away from the page without committing to the changes.**</span></span>
-   <span data-ttu-id="51077-443">**您可以使用任何輪輻頁面上的 [預覽] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-443">**You can use Preview buttons on any spoke page.**</span></span> <span data-ttu-id="51077-444">因為中樞頁面使用 [立即認可模型](glossary.md)，所以不需要預覽按鈕。</span><span class="sxs-lookup"><span data-stu-id="51077-444">Hub pages don't need Preview buttons because they use an [immediate commit model](glossary.md).</span></span>
-   <span data-ttu-id="51077-445">**請考慮使用 [控制台] 頁面的 [預覽] 按鈕，而不是 [套用] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-445">**Consider using a Preview button instead of an Apply button for control panel pages.**</span></span> <span data-ttu-id="51077-446">預覽按鈕可讓使用者更容易瞭解，並且可用於任何輪輻頁面上。</span><span class="sxs-lookup"><span data-stu-id="51077-446">Preview buttons are easier for users to understand and can be used on any spoke page.</span></span>
-   <span data-ttu-id="51077-447">**只有當頁面的設定 (至少一個具有使用者可以看到之效果的) 時，才提供 [預覽] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-447">**Provide a Preview button only if the page has settings (at least one) with effects that users can see.**</span></span> <span data-ttu-id="51077-448">使用者應該能夠預覽變更、評估變更，然後根據該評估進行進一步的變更。</span><span class="sxs-lookup"><span data-stu-id="51077-448">Users should be able to preview a change, evaluate the change, and make further changes based on that evaluation.</span></span>
-   <span data-ttu-id="51077-449">**一律啟用 [預覽] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-449">**Always enable the Preview button.**</span></span>

<span data-ttu-id="51077-450">**即時預覽**</span><span class="sxs-lookup"><span data-stu-id="51077-450">**Live previews**</span></span>

<span data-ttu-id="51077-451">當您可以立即看到輪輻頁面上變更的影響時，[控制台] 專案會有即時預覽。</span><span class="sxs-lookup"><span data-stu-id="51077-451">A control panel item has live preview when the effect of changes on a spoke page can be seen immediately.</span></span>

-   <span data-ttu-id="51077-452">**當下列情況時，請考慮使用顯示設定的即時預覽：**</span><span class="sxs-lookup"><span data-stu-id="51077-452">**Consider using live preview for display settings when:**</span></span>
    -   <span data-ttu-id="51077-453">效果很明顯，通常是因為它會套用到整個監視器。</span><span class="sxs-lookup"><span data-stu-id="51077-453">The effect is obvious, typically because it applies to the entire monitor.</span></span>
    -   <span data-ttu-id="51077-454">可以套用效果，而不會有明顯的延遲。</span><span class="sxs-lookup"><span data-stu-id="51077-454">The effect can be applied without significant delay.</span></span>
    -   <span data-ttu-id="51077-455">效果很安全，而且可以輕鬆地復原。</span><span class="sxs-lookup"><span data-stu-id="51077-455">The effect is safe and can be undone easily.</span></span>

        ![<span data-ttu-id="51077-456">[變更色彩設定] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-456">screen shot of change color settings dialog box</span></span> ](images/winenv-ctrl-panels-image12.png)

        <span data-ttu-id="51077-457">在此範例中，會立即看到 Windows 色彩和外觀設定的效果。</span><span class="sxs-lookup"><span data-stu-id="51077-457">In this example, the effect of the Windows Color and Appearance settings is seen immediately.</span></span> <span data-ttu-id="51077-458">這麼做可讓使用者以極短的時間進行變更。</span><span class="sxs-lookup"><span data-stu-id="51077-458">Doing so allows users to make changes with minimal effort.</span></span>

-   <span data-ttu-id="51077-459">**使用 [儲存變更] 和 [取消] 作為 [認可] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-459">**Use Save changes and Cancel for the commit buttons.**</span></span> <span data-ttu-id="51077-460">[儲存變更] 會保留目前的設定，而 [取消] 則會還原成原始設定。</span><span class="sxs-lookup"><span data-stu-id="51077-460">"Save changes" keeps the current settings, whereas Cancel reverts to the original settings.</span></span> <span data-ttu-id="51077-461">使用 [儲存變更]，而不是 [確定]，讓您清楚知道任何預覽的變更尚未套用。</span><span class="sxs-lookup"><span data-stu-id="51077-461">"Save changes" is used instead of OK to make it clear that any previewed changes haven't been applied yet.</span></span>
-   <span data-ttu-id="51077-462">**不要提供 [套用] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-462">**Don't provide an Apply button.**</span></span> <span data-ttu-id="51077-463">Live preview 會套用不必要的應用。</span><span class="sxs-lookup"><span data-stu-id="51077-463">The live preview makes Apply unnecessary.</span></span>
-   <span data-ttu-id="51077-464">如果使用者使用 [上一頁]、[關閉] 或 [網址] 列離開，請 **還原任何變更**。</span><span class="sxs-lookup"><span data-stu-id="51077-464">**Restore any changes if users navigate away** using Back, Close, or the Address bar.</span></span> <span data-ttu-id="51077-465">若要保留變更，使用者必須明確地認可這些變更。</span><span class="sxs-lookup"><span data-stu-id="51077-465">To preserve changes, users must commit them explicitly.</span></span>

<span data-ttu-id="51077-466">**套用按鈕**</span><span class="sxs-lookup"><span data-stu-id="51077-466">**Apply buttons**</span></span>

-   <span data-ttu-id="51077-467">請確定 **[套用] 按鈕表示套用工作啟動後 (所做的暫止變更，或上次套用) ，但仍留在目前的頁面上。**</span><span class="sxs-lookup"><span data-stu-id="51077-467">Make sure **the Apply button means apply the pending changes (made since the task was started or the last Apply), but remain on the current page.**</span></span> <span data-ttu-id="51077-468">這麼做可讓使用者在繼續進行其他工作之前，先評估變更。</span><span class="sxs-lookup"><span data-stu-id="51077-468">Doing so allows users to evaluate the changes before moving on to other tasks.</span></span>
-   <span data-ttu-id="51077-469">**只在最終輪輻頁面上使用 [套用] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-469">**Use Apply buttons only on final spoke pages.**</span></span> <span data-ttu-id="51077-470">[套用] 按鈕不應該用於中繼輪輻頁面，以維護立即認可模型。</span><span class="sxs-lookup"><span data-stu-id="51077-470">Apply buttons should not be used on intermediate spoke pages to maintain an immediate commit model.</span></span>
    -   <span data-ttu-id="51077-471">**例外狀況：** 如果變更設定需要提高 [許可權](glossary.md)，您可以使用混合式中樞頁面上的 [套用] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="51077-471">**Exception:** You can use Apply buttons on a hybrid hub page if changing a setting requires [elevation](glossary.md).</span></span> <span data-ttu-id="51077-472">如需詳細資訊，請參閱 [中樞頁面互動](#hub-pages)。</span><span class="sxs-lookup"><span data-stu-id="51077-472">For more details, see [hub page interaction](#hub-pages).</span></span>
-   <span data-ttu-id="51077-473">**只有當頁面的設定 (至少一個) 具有使用者可透過有意義的方式評估的效果時，才提供 [套用] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="51077-473">**Provide an Apply button only if the page has settings (at least one) with effects that users can evaluate in a meaningful way.**</span></span> <span data-ttu-id="51077-474">一般情況下，[套用] 按鈕會在設定進行可見變更時使用。</span><span class="sxs-lookup"><span data-stu-id="51077-474">Typically, Apply buttons are used when settings make visible changes.</span></span> <span data-ttu-id="51077-475">使用者應該能夠套用變更、評估變更，然後根據該評估進行進一步的變更。</span><span class="sxs-lookup"><span data-stu-id="51077-475">Users should be able to apply a change, evaluate the change, and make further changes based on that evaluation.</span></span>
-   <span data-ttu-id="51077-476">**只有在有暫止的變更時，才啟用 [套用] 按鈕;** 否則，請將它停用。</span><span class="sxs-lookup"><span data-stu-id="51077-476">**Enable the Apply button only when there are pending changes;** otherwise, disable it.</span></span>
-   <span data-ttu-id="51077-477">**指派 "A" 作為存取金鑰。**</span><span class="sxs-lookup"><span data-stu-id="51077-477">**Assign "A" as the access key.**</span></span>

### <a name="control-panel-integration"></a><span data-ttu-id="51077-478">控制台整合</span><span class="sxs-lookup"><span data-stu-id="51077-478">Control panel integration</span></span>

<span data-ttu-id="51077-479">若要整合您的控制台專案與 Windows，您可以：</span><span class="sxs-lookup"><span data-stu-id="51077-479">To integrate your control panel item with Windows, you can:</span></span>

-   <span data-ttu-id="51077-480">**註冊您的控制台專案 (包括其名稱、描述和圖示)**，讓 Windows 知道它。</span><span class="sxs-lookup"><span data-stu-id="51077-480">**Register your control panel item (including its name, description, and icon)**, so that Windows is aware of it.</span></span>
-   <span data-ttu-id="51077-481">如果您的控制台專案是最上層 (請參閱以下) ：</span><span class="sxs-lookup"><span data-stu-id="51077-481">If your control panel item is top level (see below):</span></span>
    -   <span data-ttu-id="51077-482">將它與適當的 **類別頁面** 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="51077-482">Associate it with the appropriate **category page**.</span></span>
    -   <span data-ttu-id="51077-483">**提供工作連結 (包括其名稱、描述、關鍵字及命令列)** 來指出主要工作，並允許使用者直接流覽至工作。</span><span class="sxs-lookup"><span data-stu-id="51077-483">**Provide task links (including their name, description, keywords, and command line)** to indicate primary tasks and allow users to navigate directly to the tasks.</span></span>
-   <span data-ttu-id="51077-484">**提供搜尋字詞** ，以協助使用者使用主控台搜尋功能來尋找您的工作連結。</span><span class="sxs-lookup"><span data-stu-id="51077-484">**Provide search terms** to help users find your task links using the Control Panel search feature.</span></span>

    <span data-ttu-id="51077-485">請注意，您只能為個別的控制台專案提供此資訊，您無法針對您延伸的現有控制台專案新增或變更此資訊。</span><span class="sxs-lookup"><span data-stu-id="51077-485">Note that you can provide this information only for individual control panel items you can't add or change this information for existing control panel items that you extend.</span></span>

<span data-ttu-id="51077-486">**類別頁面**</span><span class="sxs-lookup"><span data-stu-id="51077-486">**Category pages**</span></span>

-   <span data-ttu-id="51077-487">**只有在下列情況時，才將 [控制台] 專案新增至 [類別] 頁面：**</span><span class="sxs-lookup"><span data-stu-id="51077-487">**Add your control panel item to a category page only if:**</span></span>

    -   <span data-ttu-id="51077-488">大部分的使用者都需要它。</span><span class="sxs-lookup"><span data-stu-id="51077-488">Most users need it.</span></span> <span data-ttu-id="51077-489">範例：網路和共用中心</span><span class="sxs-lookup"><span data-stu-id="51077-489">Example: Network and Sharing Center</span></span>
    -   <span data-ttu-id="51077-490">使用的次數很多。</span><span class="sxs-lookup"><span data-stu-id="51077-490">It is used many times.</span></span> <span data-ttu-id="51077-491">範例：系統</span><span class="sxs-lookup"><span data-stu-id="51077-491">Example: System</span></span>
    -   <span data-ttu-id="51077-492">它提供的重要功能不會在其他地方公開。</span><span class="sxs-lookup"><span data-stu-id="51077-492">It provides important functionality that isn't exposed elsewhere.</span></span> <span data-ttu-id="51077-493">範例：印表機</span><span class="sxs-lookup"><span data-stu-id="51077-493">Example: Printers</span></span>

    <span data-ttu-id="51077-494">符合這些準則的控制台專案稱為最上層。</span><span class="sxs-lookup"><span data-stu-id="51077-494">Control panel items that meet these criteria are referred to as top level.</span></span>

-   <span data-ttu-id="51077-495">**如果有下列情況，請不要將您的控制台專案加入至類別頁面：**</span><span class="sxs-lookup"><span data-stu-id="51077-495">**Don't add your control panel item to a category page if:**</span></span>

    -   <span data-ttu-id="51077-496">它很少使用或用於一次性設定。</span><span class="sxs-lookup"><span data-stu-id="51077-496">It is rarely used or used for one-time setup.</span></span> <span data-ttu-id="51077-497">範例：歡迎中心</span><span class="sxs-lookup"><span data-stu-id="51077-497">Example: Welcome Center</span></span>
    -   <span data-ttu-id="51077-498">其目標物件為 advanced users 或 IT 專業人員。</span><span class="sxs-lookup"><span data-stu-id="51077-498">It is targeted at advanced users or IT professionals.</span></span> <span data-ttu-id="51077-499">範例：色彩管理</span><span class="sxs-lookup"><span data-stu-id="51077-499">Example: Color Management</span></span>
    -   <span data-ttu-id="51077-500">不適用於目前的硬體或軟體設定。</span><span class="sxs-lookup"><span data-stu-id="51077-500">It doesn't apply to the current hardware or software configuration.</span></span> <span data-ttu-id="51077-501">範例： Windows SideShow (目前的硬體) 不支援的情況。</span><span class="sxs-lookup"><span data-stu-id="51077-501">Example: Windows SideShow (if not supported by current hardware).</span></span>

    <span data-ttu-id="51077-502">從類別頁面移除這類的 [控制台] 專案，可讓您更輕鬆地尋找最上層專案。</span><span class="sxs-lookup"><span data-stu-id="51077-502">Removing such control panel items from the category pages makes the top-level items easier to find.</span></span> <span data-ttu-id="51077-503">由於這些控制台專案的使用方式，可以透過搜尋或內容進入點充分探索。</span><span class="sxs-lookup"><span data-stu-id="51077-503">Given their usage, these control panel items are sufficiently discoverable through search or contextual entry points.</span></span>

-   <span data-ttu-id="51077-504">**將最上層的 [控制台] 專案與使用者最有可能尋找的類別建立關聯。**</span><span class="sxs-lookup"><span data-stu-id="51077-504">**Associate your top-level control panel item with the category under which users are most likely to look for it.**</span></span> <span data-ttu-id="51077-505">此決定應以使用者測試為基礎。</span><span class="sxs-lookup"><span data-stu-id="51077-505">This decision should be based on user testing.</span></span>
-   <span data-ttu-id="51077-506">**請考慮將最上層的控制台專案與第二個最可能的類別建立關聯。**</span><span class="sxs-lookup"><span data-stu-id="51077-506">**Consider associating your top-level control panel item with the second most likely category as well.**</span></span> <span data-ttu-id="51077-507">如果使用者可能會在多個位置中尋找其主要工作，您應該將 [控制台] 專案與兩個類別建立關聯。</span><span class="sxs-lookup"><span data-stu-id="51077-507">You should associate a control panel item with two categories if users are likely to look for its main tasks in more than one place.</span></span>
-   <span data-ttu-id="51077-508">**請勿將您的 [控制台] 專案與兩個以上的類別建立關聯。**</span><span class="sxs-lookup"><span data-stu-id="51077-508">**Don't associate your control panel item with more than two categories.**</span></span> <span data-ttu-id="51077-509">如果 [控制台] 專案出現在數個類別中，則分類的值為破壞。</span><span class="sxs-lookup"><span data-stu-id="51077-509">The value of the categorization is undermined if control panel items appear in several categories.</span></span>

<span data-ttu-id="51077-510">**工作連結**</span><span class="sxs-lookup"><span data-stu-id="51077-510">**Task links**</span></span>

-   <span data-ttu-id="51077-511">**將您的 [控制台] 專案與其主要工作產生關聯。**</span><span class="sxs-lookup"><span data-stu-id="51077-511">**Associate your control panel item with its primary tasks.**</span></span> <span data-ttu-id="51077-512">您最多可以在 [類別目錄] 頁面上顯示五個工作，但會使用其他工作來進行控制台搜尋作業。</span><span class="sxs-lookup"><span data-stu-id="51077-512">You can display up to five tasks on a Category page, but additional tasks are used for control panel searching.</span></span> <span data-ttu-id="51077-513">使用與工作連結相同的片語，可能會移除一些文字，讓工作連結更簡潔。</span><span class="sxs-lookup"><span data-stu-id="51077-513">Use the same phrasing as you do for task links, possibly removing some words to make the task links more succinct.</span></span>
-   <span data-ttu-id="51077-514">**偏好讓工作連結出現在 [控制台] 專案中的不同位置。**</span><span class="sxs-lookup"><span data-stu-id="51077-514">**Prefer to have task links lead to different places in your control panel item.**</span></span> <span data-ttu-id="51077-515">有多個相同位置的連結可能會造成混淆。</span><span class="sxs-lookup"><span data-stu-id="51077-515">Having multiple links to the same place can be confusing.</span></span>

<span data-ttu-id="51077-516">**搜尋詞彙**</span><span class="sxs-lookup"><span data-stu-id="51077-516">**Search terms**</span></span>

-   <span data-ttu-id="51077-517">**註冊您的控制台專案的搜尋詞彙，使用者最有可能用來描述它。**</span><span class="sxs-lookup"><span data-stu-id="51077-517">**Register search terms for your control panel item that users are most likely to use to describe it.**</span></span> <span data-ttu-id="51077-518">這些搜尋詞彙應包括：</span><span class="sxs-lookup"><span data-stu-id="51077-518">These search terms should include:</span></span>

    -   <span data-ttu-id="51077-519">已設定的功能或物件。</span><span class="sxs-lookup"><span data-stu-id="51077-519">The features or objects configured.</span></span>
    -   <span data-ttu-id="51077-520">主要工作。</span><span class="sxs-lookup"><span data-stu-id="51077-520">The primary tasks.</span></span>

    <span data-ttu-id="51077-521">這些搜尋詞彙應以使用者測試為基礎。</span><span class="sxs-lookup"><span data-stu-id="51077-521">These search terms should be based on user testing.</span></span>

-   <span data-ttu-id="51077-522">**也包含這些搜尋詞彙的一般同義字。**</span><span class="sxs-lookup"><span data-stu-id="51077-522">**Also include common synonyms for these search terms.**</span></span> <span data-ttu-id="51077-523">例如，「監視」和「顯示」是同義字，因此應該包含這兩個字。</span><span class="sxs-lookup"><span data-stu-id="51077-523">For example, monitor and display are synonyms, so both words should be included.</span></span>
-   <span data-ttu-id="51077-524">**包含替代的拼寫或斷詞。**</span><span class="sxs-lookup"><span data-stu-id="51077-524">**Include alternative spellings or word breaks.**</span></span> <span data-ttu-id="51077-525">例如，使用者可能會搜尋網站和網站。</span><span class="sxs-lookup"><span data-stu-id="51077-525">For example, users might search for either web site and website.</span></span> <span data-ttu-id="51077-526">也請考慮提供常見的拼寫錯誤。</span><span class="sxs-lookup"><span data-stu-id="51077-526">Consider providing common misspellings as well.</span></span>
-   <span data-ttu-id="51077-527">**請考慮單數與複數名詞形式。**</span><span class="sxs-lookup"><span data-stu-id="51077-527">**Consider singular vs. plural noun forms.**</span></span> <span data-ttu-id="51077-528">[控制台] 搜尋功能不會自動搜尋這兩種表單;提供使用者可能搜尋的表單。</span><span class="sxs-lookup"><span data-stu-id="51077-528">The control panel search feature doesn't automatically search for both forms; supply the forms for which users are likely to search.</span></span>
-   <span data-ttu-id="51077-529">**使用簡單的現在時動詞動詞。**</span><span class="sxs-lookup"><span data-stu-id="51077-529">**Use simple present tense verbs.**</span></span> <span data-ttu-id="51077-530">如果您將 [連線] 註冊為搜尋字詞，搜尋功能將不會自動尋找連接、連接和連線。</span><span class="sxs-lookup"><span data-stu-id="51077-530">If you register connect as a search term, the search feature won't automatically look for connects, connecting, and connected.</span></span>
-   <span data-ttu-id="51077-531">**不要擔心大小寫。**</span><span class="sxs-lookup"><span data-stu-id="51077-531">**Don't worry about case.**</span></span> <span data-ttu-id="51077-532">搜尋功能不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="51077-532">The search feature is not case-sensitive.</span></span>

### <a name="standard-users-and-protected-administrators"></a><span data-ttu-id="51077-533">標準使用者和受保護的系統管理員</span><span class="sxs-lookup"><span data-stu-id="51077-533">Standard users and Protected administrators</span></span>

<span data-ttu-id="51077-534">**許多設定都需要系統管理員許可權才能變更。**</span><span class="sxs-lookup"><span data-stu-id="51077-534">**Many settings require administrator privileges to change.**</span></span> <span data-ttu-id="51077-535">如果進程需要系統管理員許可權，則 Windows Vista 和更新版本需要 [標準使用者](glossary.md) 和 [受保護](glossary.md) 的系統管理員明確地提升其許可權。</span><span class="sxs-lookup"><span data-stu-id="51077-535">If a process requires administrator privileges, Windows Vista and later requires [Standard users](glossary.md) and [Protected administrators](glossary.md) to elevate their privileges explicitly.</span></span> <span data-ttu-id="51077-536">這樣做有助於防止惡意程式碼以系統管理員許可權執行。</span><span class="sxs-lookup"><span data-stu-id="51077-536">Doing so helps prevent malicious code from running with administrator privileges.</span></span>

<span data-ttu-id="51077-537">如需詳細資訊和範例，請參閱 [使用者帳戶控制](winenv-uac.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-537">For more information and examples, see [User Account Control](winenv-uac.md).</span></span>

### <a name="schemes-and-themes"></a><span data-ttu-id="51077-538">配置和主題</span><span class="sxs-lookup"><span data-stu-id="51077-538">Schemes and themes</span></span>

<span data-ttu-id="51077-539">配置是視覺設定的命名集合。</span><span class="sxs-lookup"><span data-stu-id="51077-539">A scheme is a named collection of visual settings.</span></span> <span data-ttu-id="51077-540">主題是跨系統設定的命名集合。</span><span class="sxs-lookup"><span data-stu-id="51077-540">A theme is a named collection of settings across the system.</span></span> <span data-ttu-id="51077-541">配置和主題的範例包括顯示、滑鼠、電話和數據機、電源選項，以及音效和音訊選項。</span><span class="sxs-lookup"><span data-stu-id="51077-541">Examples of schemes and themes include Display, Mouse, Phone and Modem, Power Options, and Sound and Audio Options.</span></span>

-   <span data-ttu-id="51077-542">**允許使用者在下列情況建立配置：**</span><span class="sxs-lookup"><span data-stu-id="51077-542">**Allow users to create schemes when:**</span></span>

    -   <span data-ttu-id="51077-543">**使用者很可能會變更設定。**</span><span class="sxs-lookup"><span data-stu-id="51077-543">**Users are likely to change the settings.**</span></span>
    -   <span data-ttu-id="51077-544">**使用者最有可能將設定變更為集合。**</span><span class="sxs-lookup"><span data-stu-id="51077-544">**Users are most likely to change settings as a collection.**</span></span>

    <span data-ttu-id="51077-545">當使用者位於不同的環境（例如 (國家/地區、時區) 的不同實體位置）時，配置會很有用;在不同的情況下使用其電腦 (電池、停駐/取消插接) ;或者，將電腦用於不同的功能 (簡報、影片播放) 。</span><span class="sxs-lookup"><span data-stu-id="51077-545">Schemes are useful when users are in a different environment, such as a different physical location (country/region, time zone); using their computer in a different situation (on batteries, docked/undocked); or using their computer for a different function (presentations, video playback).</span></span>

-   <span data-ttu-id="51077-546">**至少提供一個預設配置。**</span><span class="sxs-lookup"><span data-stu-id="51077-546">**Provide at least one default scheme.**</span></span> <span data-ttu-id="51077-547">在大多數情況下，預設配置應妥善命名並套用至大部分的使用者。</span><span class="sxs-lookup"><span data-stu-id="51077-547">The default scheme should be well named and apply to most users in most circumstances.</span></span> <span data-ttu-id="51077-548">使用者不應該建立自己的配置。</span><span class="sxs-lookup"><span data-stu-id="51077-548">Users shouldn't have to create a scheme of their own.</span></span>
-   <span data-ttu-id="51077-549">**提供預覽** 或其他機制，讓使用者可以查看配置內的設定。</span><span class="sxs-lookup"><span data-stu-id="51077-549">**Provide a preview** or other mechanism so that users can see the settings within the scheme.</span></span>

    ![<span data-ttu-id="51077-550">[個人化] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-550">screen shot of personalization dialog box</span></span> ](images/winenv-ctrl-panels-image13.png)

    <span data-ttu-id="51077-551">在此範例中，[個人化] 控制台專案會顯示桌面和外觀設定的預覽。</span><span class="sxs-lookup"><span data-stu-id="51077-551">In this example, the Personalization control panel item shows a preview of the desktop and appearance settings.</span></span>

-   <span data-ttu-id="51077-552">**提供 [另存新檔] 和 [刪除] 命令。**</span><span class="sxs-lookup"><span data-stu-id="51077-552">**Provide Save As and Delete commands.**</span></span> <span data-ttu-id="51077-553">重新命名命令不是必要的，使用者可以藉由儲存所需的名稱並刪除原始配置來重新命名配置。</span><span class="sxs-lookup"><span data-stu-id="51077-553">A rename command isn't necessary users can rename schemes by saving under the desired name and deleting the original scheme.</span></span>
-   <span data-ttu-id="51077-554">如果無法在沒有配置的情況下套用設定，則 **不允許使用者刪除所有配置。**</span><span class="sxs-lookup"><span data-stu-id="51077-554">If the settings can't be applied without a scheme, **don't allow users to delete all the schemes.**</span></span> <span data-ttu-id="51077-555">使用者不應該建立自己的配置。</span><span class="sxs-lookup"><span data-stu-id="51077-555">Users shouldn't have to create a scheme of their own.</span></span>
-   <span data-ttu-id="51077-556">如果配置不是完全獨立的 (例如，電源配置相依于目前的膝上型電腦模式) ，請 **確定有一個簡單的方法可變更套用到所有配置的設定。**</span><span class="sxs-lookup"><span data-stu-id="51077-556">If the schemes are not completely independent (for example, power schemes depend upon the current laptop mode of operation), **make sure there is an easy way to change settings that apply across all schemes.**</span></span> <span data-ttu-id="51077-557">例如，使用電源配置時，請確定使用者可以設定在單一位置中關閉可攜式電腦的蓋時所發生的情況。</span><span class="sxs-lookup"><span data-stu-id="51077-557">For example with power schemes, make sure that users can set what happens when a portable computer's lid is closed in a single location.</span></span>

### <a name="miscellaneous"></a><span data-ttu-id="51077-558">其他</span><span class="sxs-lookup"><span data-stu-id="51077-558">Miscellaneous</span></span>

-   <span data-ttu-id="51077-559">**使用主控台擴充功能來取代或擴充現有的 Windows 功能。**</span><span class="sxs-lookup"><span data-stu-id="51077-559">**Use Control Panel extensions for features that replace or extend existing Windows functionality.**</span></span> <span data-ttu-id="51077-560">下列控制台專案可延伸：藍牙裝置、顯示器、網際網路、鍵盤、滑鼠、網路、電源、系統、無線 (紅外線) 。</span><span class="sxs-lookup"><span data-stu-id="51077-560">The following control panel items are extensible: Bluetooth Devices, Display, Internet, Keyboard, Mouse, Network, Power, System, Wireless (infrared).</span></span>

### <a name="default-values"></a><span data-ttu-id="51077-561">預設值</span><span class="sxs-lookup"><span data-stu-id="51077-561">Default values</span></span>

-   <span data-ttu-id="51077-562">**[控制台] 專案內的設定必須反映功能的目前狀態。**</span><span class="sxs-lookup"><span data-stu-id="51077-562">**The settings within a control panel item must reflect the current state of the feature.**</span></span> <span data-ttu-id="51077-563">否則會產生誤導，可能會導致不想要的結果。</span><span class="sxs-lookup"><span data-stu-id="51077-563">Doing otherwise would be misleading and possibly lead to undesired results.</span></span> <span data-ttu-id="51077-564">例如，如果設定反映出建議，而不是目前的狀態，則使用者可能會按一下 [取消]，而不是進行變更，以為不需要任何變更。</span><span class="sxs-lookup"><span data-stu-id="51077-564">For example, if settings reflect the recommendations but not the current state, users might click Cancel instead of making changes, thinking that no changes are needed.</span></span>
-   <span data-ttu-id="51077-565">**選擇最安全的 (，以防止資料遺失或系統存取) 和最安全的初始狀態。**</span><span class="sxs-lookup"><span data-stu-id="51077-565">**Choose the safest (to prevent loss of data or system access) and most secure initial state.**</span></span> <span data-ttu-id="51077-566">假設大部分的使用者不會變更設定。</span><span class="sxs-lookup"><span data-stu-id="51077-566">Assume that most users won't change the settings.</span></span>
-   <span data-ttu-id="51077-567">**如果安全性和安全性不是因素，請選擇最有可能或方便的初始狀態。**</span><span class="sxs-lookup"><span data-stu-id="51077-567">**If safety and security aren't factors, choose the initial state that is most likely or convenient.**</span></span>

## <a name="text"></a><span data-ttu-id="51077-568">Text</span><span class="sxs-lookup"><span data-stu-id="51077-568">Text</span></span>

### <a name="item-names"></a><span data-ttu-id="51077-569">專案名稱</span><span class="sxs-lookup"><span data-stu-id="51077-569">Item names</span></span>

-   <span data-ttu-id="51077-570">**選擇明確通訊的描述性名稱，並區分 [控制台] 專案的用途。**</span><span class="sxs-lookup"><span data-stu-id="51077-570">**Choose a descriptive name that clearly communicates and differentiates what the control panel item does.**</span></span> <span data-ttu-id="51077-571">大部分的名稱會描述要設定的 Windows 功能或物件，並顯示在 [控制台] 首頁的 [傳統] 視圖中。</span><span class="sxs-lookup"><span data-stu-id="51077-571">Most names describe the Windows feature or object being configured, and are displayed in the Classic View of the control panel home page.</span></span>
-   <span data-ttu-id="51077-572">**請勿在名稱中包含單字「設定」、「選項」、「屬性」或「設定」。**</span><span class="sxs-lookup"><span data-stu-id="51077-572">**Don't include the words "Settings," "Options," "Properties," or "Configuration" in the name.**</span></span> <span data-ttu-id="51077-573">這是隱含的，而不是讓使用者能夠更輕鬆地進行掃描。</span><span class="sxs-lookup"><span data-stu-id="51077-573">This is implied, and leaving it off makes it easier for users to scan.</span></span>

    <span data-ttu-id="51077-574">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-574">**Incorrect:**</span></span>

    <span data-ttu-id="51077-575">協助工具選項</span><span class="sxs-lookup"><span data-stu-id="51077-575">Accessibility Options</span></span>

    <span data-ttu-id="51077-576">數據機設定</span><span class="sxs-lookup"><span data-stu-id="51077-576">Modem Settings</span></span>

    <span data-ttu-id="51077-577">電源選項</span><span class="sxs-lookup"><span data-stu-id="51077-577">Power Options</span></span>

    <span data-ttu-id="51077-578">地區及語言選項</span><span class="sxs-lookup"><span data-stu-id="51077-578">Regional and Language Options</span></span>

    <span data-ttu-id="51077-579">**正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-579">**Correct:**</span></span>

    <span data-ttu-id="51077-580">協助工具選項</span><span class="sxs-lookup"><span data-stu-id="51077-580">Accessibility</span></span>

    <span data-ttu-id="51077-581">數據機</span><span class="sxs-lookup"><span data-stu-id="51077-581">Modem</span></span>

    <span data-ttu-id="51077-582">電源</span><span class="sxs-lookup"><span data-stu-id="51077-582">Power</span></span>

    <span data-ttu-id="51077-583">地區格式和語言</span><span class="sxs-lookup"><span data-stu-id="51077-583">Regional Formats and Languages</span></span>

    <span data-ttu-id="51077-584">在正確的範例中，會移除不必要的字組。</span><span class="sxs-lookup"><span data-stu-id="51077-584">In the correct examples, unnecessary words are removed.</span></span>

-   <span data-ttu-id="51077-585">**如果 [控制台] 專案設定了相關的功能，只會列出識別該專案所需的功能，並列出最可能先辨識或使用的功能。**</span><span class="sxs-lookup"><span data-stu-id="51077-585">**If the control panel item configures related features, list only those features required to identify the item, and list the features the most likely to be recognized or used first.**</span></span>

    <span data-ttu-id="51077-586">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-586">**Incorrect:**</span></span>

    <span data-ttu-id="51077-587">資料夾選項</span><span class="sxs-lookup"><span data-stu-id="51077-587">Folder Options</span></span>

    <span data-ttu-id="51077-588">電話和數據機選項</span><span class="sxs-lookup"><span data-stu-id="51077-588">Phone and Modem Options</span></span>

    <span data-ttu-id="51077-589">**正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-589">**Correct:**</span></span>

    <span data-ttu-id="51077-590">檔案和資料夾</span><span class="sxs-lookup"><span data-stu-id="51077-590">Files and Folders</span></span>

    <span data-ttu-id="51077-591">數據機</span><span class="sxs-lookup"><span data-stu-id="51077-591">Modem</span></span>

    <span data-ttu-id="51077-592">在正確的範例中，主要的 [控制台] 專案功能會獲得強調。</span><span class="sxs-lookup"><span data-stu-id="51077-592">In the correct examples, the primary control panel item features are given emphasis.</span></span>

-   <span data-ttu-id="51077-593">使用 [標題樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-593">Use [title-style capitalization](glossary.md).</span></span>

### <a name="page-titles"></a><span data-ttu-id="51077-594">頁面標題</span><span class="sxs-lookup"><span data-stu-id="51077-594">Page titles</span></span>

<span data-ttu-id="51077-595">**注意：** 如同所有 Explorer 視窗，[控制台] 頁面標題會顯示在 [網址](glossary.md)列上，但不會顯示在標題列上。</span><span class="sxs-lookup"><span data-stu-id="51077-595">**Note:** As with all Explorer windows, control panel page titles are displayed on the [address bar](glossary.md), but not the title bar.</span></span>

-   <span data-ttu-id="51077-596">**若為中樞頁面，請使用 [控制台] 專案名稱。**</span><span class="sxs-lookup"><span data-stu-id="51077-596">**For hub pages, use the control panel item name.**</span></span>
-   <span data-ttu-id="51077-597">**針對輪輻頁面，請使用頁面的簡短摘要。**</span><span class="sxs-lookup"><span data-stu-id="51077-597">**For spoke pages, use a concise summary of the page's purpose.**</span></span> <span data-ttu-id="51077-598">如果它很簡潔，請使用頁面的主要指示;否則，請使用主要指令的精確重述。</span><span class="sxs-lookup"><span data-stu-id="51077-598">Use the page's main instruction if it is concise; otherwise use a concise restatement of the main instruction.</span></span>

    ![<span data-ttu-id="51077-599">[電源選項] 對話方塊的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="51077-599">screen shot of power options dialog box</span></span> ](images/winenv-ctrl-panels-image6.png)

    <span data-ttu-id="51077-600">在此範例中，電源選項用於頁面標題，而不是主要指令。</span><span class="sxs-lookup"><span data-stu-id="51077-600">In this example, Power Options is used for the page title instead of the main instruction.</span></span>

-   <span data-ttu-id="51077-601">使用標題樣式的大小寫。</span><span class="sxs-lookup"><span data-stu-id="51077-601">Use title-style capitalization.</span></span>

### <a name="task-link-text"></a><span data-ttu-id="51077-602">工作連結文字</span><span class="sxs-lookup"><span data-stu-id="51077-602">Task link text</span></span>

<span data-ttu-id="51077-603">下列指導方針適用于工作頁面的連結，例如類別頁面工作連結及另請參閱連結。</span><span class="sxs-lookup"><span data-stu-id="51077-603">The following guidelines apply to links to task pages, such as Category page task links and See also links.</span></span>

-   <span data-ttu-id="51077-604">**選擇清楚傳達和區分工作的精確工作名稱。**</span><span class="sxs-lookup"><span data-stu-id="51077-604">**Choose concise task names that clearly communicate and differentiate the task.**</span></span> <span data-ttu-id="51077-605">使用者不應該需要找出工作真正的意義，或與其他工作有何不同。</span><span class="sxs-lookup"><span data-stu-id="51077-605">Users shouldn't have to figure out what the task really means or how it differs from other tasks.</span></span>

    <span data-ttu-id="51077-606">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-606">**Incorrect:**</span></span>

    <span data-ttu-id="51077-607">調整顯示設定</span><span class="sxs-lookup"><span data-stu-id="51077-607">Adjust display settings</span></span>

    <span data-ttu-id="51077-608">**正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-608">**Correct:**</span></span>

    <span data-ttu-id="51077-609">螢幕解析度</span><span class="sxs-lookup"><span data-stu-id="51077-609">Screen resolution</span></span>

    <span data-ttu-id="51077-610">在正確的範例中，文字表達的精確度更高。</span><span class="sxs-lookup"><span data-stu-id="51077-610">In the correct example, the wording conveys more precision.</span></span>

-   <span data-ttu-id="51077-611">**在工作連結與它們所指向的頁面之間保留類似的語言。**</span><span class="sxs-lookup"><span data-stu-id="51077-611">**Retain similar language between task links and the pages they point to.**</span></span> <span data-ttu-id="51077-612">連結所顯示的頁面應該不會讓使用者感到驚訝。</span><span class="sxs-lookup"><span data-stu-id="51077-612">Users shouldn't be surprised by the page that is displayed by a link.</span></span>
-   <span data-ttu-id="51077-613">**針對工作頁面，請將主要指示、認可按鈕和工作連結設計為一組相關的文字。**</span><span class="sxs-lookup"><span data-stu-id="51077-613">**For task pages, design the main instruction, commit buttons, and task links as a related set of text.**</span></span>
    

    | <span data-ttu-id="51077-614">範例</span><span class="sxs-lookup"><span data-stu-id="51077-614">Example</span></span>                             |    <span data-ttu-id="51077-615">指令</span><span class="sxs-lookup"><span data-stu-id="51077-615">Instruction</span></span>                                                   |
    |------------------------------|-------------------------------------------------------|
    | <span data-ttu-id="51077-616">工作連結：</span><span class="sxs-lookup"><span data-stu-id="51077-616">Task link:</span></span><br/>        | <span data-ttu-id="51077-617">連接到無線網路</span><span class="sxs-lookup"><span data-stu-id="51077-617">Connect to a wireless network</span></span><br/>              |
    | <span data-ttu-id="51077-618">主要指示：</span><span class="sxs-lookup"><span data-stu-id="51077-618">Main instruction:</span></span><br/> | <span data-ttu-id="51077-619">選擇要連接的網路</span><span class="sxs-lookup"><span data-stu-id="51077-619">Choose a network to connect to</span></span><br/>             |
    | <span data-ttu-id="51077-620">認可按鈕：</span><span class="sxs-lookup"><span data-stu-id="51077-620">Commit button:</span></span><br/>    | <span data-ttu-id="51077-621">連線</span><span class="sxs-lookup"><span data-stu-id="51077-621">Connect</span></span><br/>                                    |
    | <span data-ttu-id="51077-622">工作連結：</span><span class="sxs-lookup"><span data-stu-id="51077-622">Task link:</span></span><br/>        | <span data-ttu-id="51077-623">設定家長監護控制項</span><span class="sxs-lookup"><span data-stu-id="51077-623">Set up parental controls</span></span><br/>                   |
    | <span data-ttu-id="51077-624">主要指示：</span><span class="sxs-lookup"><span data-stu-id="51077-624">Main instruction:</span></span><br/> | <span data-ttu-id="51077-625">選擇使用者並設定家長監護控制項</span><span class="sxs-lookup"><span data-stu-id="51077-625">Choose a user and set up parental controls</span></span><br/> |
    | <span data-ttu-id="51077-626">認可按鈕：</span><span class="sxs-lookup"><span data-stu-id="51077-626">Commit button:</span></span><br/>    | <span data-ttu-id="51077-627">套用家長監護</span><span class="sxs-lookup"><span data-stu-id="51077-627">Apply parental control</span></span><br/>                     |
    | <span data-ttu-id="51077-628">工作連結：</span><span class="sxs-lookup"><span data-stu-id="51077-628">Task link:</span></span><br/>        | <span data-ttu-id="51077-629">解決同步衝突</span><span class="sxs-lookup"><span data-stu-id="51077-629">Resolve your sync conflicts</span></span><br/>                |
    | <span data-ttu-id="51077-630">主要指示：</span><span class="sxs-lookup"><span data-stu-id="51077-630">Main instruction:</span></span><br/> | <span data-ttu-id="51077-631">您要如何解決這種衝突？</span><span class="sxs-lookup"><span data-stu-id="51077-631">How do you want to resolve this conflict?</span></span><br/>  |
    | <span data-ttu-id="51077-632">認可按鈕：</span><span class="sxs-lookup"><span data-stu-id="51077-632">Commit button:</span></span><br/>    | <span data-ttu-id="51077-633">解決</span><span class="sxs-lookup"><span data-stu-id="51077-633">Resolve</span></span><br/>                                    |

    

     

    <span data-ttu-id="51077-634">這些範例顯示工作連結文字、主要指令和認可按鈕文字的關聯性。</span><span class="sxs-lookup"><span data-stu-id="51077-634">These examples show the relationship of the task link text, main instruction, and commit button text.</span></span>

-   <span data-ttu-id="51077-635">雖然工作通常是以動詞開頭，但 **如果它是泛型、設定相關的動詞，而不能協助傳達工作，請考慮省略類別頁面上的動詞命令。**</span><span class="sxs-lookup"><span data-stu-id="51077-635">While tasks often start with verbs, **consider omitting the verb on Category pages if it is a generic, configuration-related verb that doesn't help communicate the task.**</span></span>

    <span data-ttu-id="51077-636">**特定且有用的動詞：**</span><span class="sxs-lookup"><span data-stu-id="51077-636">**Specific, helpful verbs:**</span></span>

    <span data-ttu-id="51077-637">加</span><span class="sxs-lookup"><span data-stu-id="51077-637">Add</span></span>

    <span data-ttu-id="51077-638">勾選</span><span class="sxs-lookup"><span data-stu-id="51077-638">Check</span></span>

    <span data-ttu-id="51077-639">連線</span><span class="sxs-lookup"><span data-stu-id="51077-639">Connect</span></span>

    <span data-ttu-id="51077-640">複製</span><span class="sxs-lookup"><span data-stu-id="51077-640">Copy</span></span>

    <span data-ttu-id="51077-641">建立</span><span class="sxs-lookup"><span data-stu-id="51077-641">Create</span></span>

    <span data-ttu-id="51077-642">刪除</span><span class="sxs-lookup"><span data-stu-id="51077-642">Delete</span></span>

    <span data-ttu-id="51077-643">中斷連線</span><span class="sxs-lookup"><span data-stu-id="51077-643">Disconnect</span></span>

    <span data-ttu-id="51077-644">安裝</span><span class="sxs-lookup"><span data-stu-id="51077-644">Install</span></span>

    <span data-ttu-id="51077-645">移除</span><span class="sxs-lookup"><span data-stu-id="51077-645">Remove</span></span>

    <span data-ttu-id="51077-646">設定</span><span class="sxs-lookup"><span data-stu-id="51077-646">Set up</span></span>

    <span data-ttu-id="51077-647">開始</span><span class="sxs-lookup"><span data-stu-id="51077-647">Start</span></span>

    <span data-ttu-id="51077-648">Stop</span><span class="sxs-lookup"><span data-stu-id="51077-648">Stop</span></span>

    <span data-ttu-id="51077-649">疑難排解</span><span class="sxs-lookup"><span data-stu-id="51077-649">Troubleshoot</span></span>

    <span data-ttu-id="51077-650">**泛型、無用動詞：**</span><span class="sxs-lookup"><span data-stu-id="51077-650">**Generic, unhelpful verbs:**</span></span>

    <span data-ttu-id="51077-651">Adjust</span><span class="sxs-lookup"><span data-stu-id="51077-651">Adjust</span></span>

    <span data-ttu-id="51077-652">變更</span><span class="sxs-lookup"><span data-stu-id="51077-652">Change</span></span>

    <span data-ttu-id="51077-653">Choose</span><span class="sxs-lookup"><span data-stu-id="51077-653">Choose</span></span>

    <span data-ttu-id="51077-654">設定</span><span class="sxs-lookup"><span data-stu-id="51077-654">Configure</span></span>

    <span data-ttu-id="51077-655">編輯</span><span class="sxs-lookup"><span data-stu-id="51077-655">Edit</span></span>

    <span data-ttu-id="51077-656">管理</span><span class="sxs-lookup"><span data-stu-id="51077-656">Manage</span></span>

    <span data-ttu-id="51077-657">開啟</span><span class="sxs-lookup"><span data-stu-id="51077-657">Open</span></span>

    <span data-ttu-id="51077-658">挑選</span><span class="sxs-lookup"><span data-stu-id="51077-658">Pick</span></span>

    <span data-ttu-id="51077-659">集合</span><span class="sxs-lookup"><span data-stu-id="51077-659">Set</span></span>

    <span data-ttu-id="51077-660">選取</span><span class="sxs-lookup"><span data-stu-id="51077-660">Select</span></span>

    <span data-ttu-id="51077-661">顯示</span><span class="sxs-lookup"><span data-stu-id="51077-661">Show</span></span>

    <span data-ttu-id="51077-662">檢視</span><span class="sxs-lookup"><span data-stu-id="51077-662">View</span></span>

-   <span data-ttu-id="51077-663">**如果工作設定數個相關的功能，只會列出代表該集合的功能。**</span><span class="sxs-lookup"><span data-stu-id="51077-663">**If the task configures several related features, list only the features that are representative of the set.**</span></span> <span data-ttu-id="51077-664">省略可以立即推斷的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="51077-664">Omit details that can be readily inferred.</span></span>

    <span data-ttu-id="51077-665">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-665">**Incorrect:**</span></span>

    <span data-ttu-id="51077-666">喇叭音量、靜音、音量圖示</span><span class="sxs-lookup"><span data-stu-id="51077-666">Speaker volume, mute, volume icon</span></span>

    <span data-ttu-id="51077-667">喇叭、麥克風、MIDI 和音效方案</span><span class="sxs-lookup"><span data-stu-id="51077-667">Speakers, microphones, MIDI, and sound schemes</span></span>

    <span data-ttu-id="51077-668">**正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-668">**Correct:**</span></span>

    <span data-ttu-id="51077-669">喇叭音量</span><span class="sxs-lookup"><span data-stu-id="51077-669">Speaker volume</span></span>

    <span data-ttu-id="51077-670">喇叭和麥克風</span><span class="sxs-lookup"><span data-stu-id="51077-670">Speakers and microphones</span></span>

    <span data-ttu-id="51077-671">在正確的範例中，工作連結中只會提供代表性的功能。</span><span class="sxs-lookup"><span data-stu-id="51077-671">In the correct examples, only the representative features are given in the task link.</span></span>

-   <span data-ttu-id="51077-672">**只有當目標使用者這麼做時，才應該將工作以技術為依據。**</span><span class="sxs-lookup"><span data-stu-id="51077-672">**You should phrase tasks in terms of technology only if target users would do so as well.**</span></span>

    <span data-ttu-id="51077-673">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-673">**Incorrect:**</span></span>

    <span data-ttu-id="51077-674">Connectoids</span><span class="sxs-lookup"><span data-stu-id="51077-674">Connectoids</span></span>

    <span data-ttu-id="51077-675">圖元深度</span><span class="sxs-lookup"><span data-stu-id="51077-675">Pixel depth</span></span>

    <span data-ttu-id="51077-676">DPI</span><span class="sxs-lookup"><span data-stu-id="51077-676">dpi</span></span>

    <span data-ttu-id="51077-677">**正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-677">**Correct:**</span></span>

    <span data-ttu-id="51077-678">印表機</span><span class="sxs-lookup"><span data-stu-id="51077-678">Printers</span></span>

    <span data-ttu-id="51077-679">掃描器</span><span class="sxs-lookup"><span data-stu-id="51077-679">Scanners</span></span>

    <span data-ttu-id="51077-680">滑鼠</span><span class="sxs-lookup"><span data-stu-id="51077-680">Mouse</span></span>

    <span data-ttu-id="51077-681">正確的範例是以技術為基礎的目標使用者可能會使用的詞彙，而不正確的範例則不正確。</span><span class="sxs-lookup"><span data-stu-id="51077-681">The correct examples are technology-based terms that target users are likely to use, whereas the incorrect examples are not.</span></span>

-   <span data-ttu-id="51077-682">只有在系統可以支援一個以上時，才使用複數名詞。</span><span class="sxs-lookup"><span data-stu-id="51077-682">Use plural nouns only if the system can support more than one.</span></span>
-   <span data-ttu-id="51077-683">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-683">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="51077-684">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="51077-684">Don't use ending punctuation.</span></span>

### <a name="main-instructions"></a><span data-ttu-id="51077-685">主要指示</span><span class="sxs-lookup"><span data-stu-id="51077-685">Main instructions</span></span>

-   <span data-ttu-id="51077-686">**在 [中樞] 頁面上，使用主要指示，透過 [控制台] 專案來說明使用者的目標。**</span><span class="sxs-lookup"><span data-stu-id="51077-686">**For the hub page, use the main instruction to explain the user's objective with the control panel item.**</span></span> <span data-ttu-id="51077-687">主要指示應可協助使用者判斷他們是否已選取正確的控制台專案。</span><span class="sxs-lookup"><span data-stu-id="51077-687">The main instruction should help users determine if they have selected the right control panel item.</span></span> <span data-ttu-id="51077-688">請記住，使用者可能已在錯誤中選取您的 [控制台] 專案，而且實際上正在尋找屬於其他 [控制台] 專案的設定。</span><span class="sxs-lookup"><span data-stu-id="51077-688">Keep in mind that users might have selected your control panel item in error and are actually looking for settings that are part of another control panel item.</span></span>

    <span data-ttu-id="51077-689">**範例：**</span><span class="sxs-lookup"><span data-stu-id="51077-689">**Examples:**</span></span>

    <span data-ttu-id="51077-690">保持電腦的安全和最新狀態</span><span class="sxs-lookup"><span data-stu-id="51077-690">Keep your computer secure and up-to-date</span></span>

    <span data-ttu-id="51077-691">優化您的電腦，以便更輕鬆地查看、聆聽及控制</span><span class="sxs-lookup"><span data-stu-id="51077-691">Optimize your computer so it's easier to see, hear, and control</span></span>

-   <span data-ttu-id="51077-692">**針對輪輻頁面，請使用主要指示來說明頁面上要執行的動作。**</span><span class="sxs-lookup"><span data-stu-id="51077-692">**For spoke pages, use the main instruction to explain what to do on the page.**</span></span> <span data-ttu-id="51077-693">指令應該是特定的語句、命令式方向或問題。</span><span class="sxs-lookup"><span data-stu-id="51077-693">The instruction should be a specific statement, imperative direction, or question.</span></span> <span data-ttu-id="51077-694">良好的指示會以頁面傳達使用者的目標，而不是單純專注于操作它的機制。</span><span class="sxs-lookup"><span data-stu-id="51077-694">Good instructions communicate the user's objective with the page rather than focusing purely on the mechanics of manipulating it.</span></span>

    <span data-ttu-id="51077-695">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-695">**Incorrect:**</span></span>

    <span data-ttu-id="51077-696">挑選通知工作</span><span class="sxs-lookup"><span data-stu-id="51077-696">Pick a notification task</span></span>

    <span data-ttu-id="51077-697">**正確：**</span><span class="sxs-lookup"><span data-stu-id="51077-697">**Correct:**</span></span>

    <span data-ttu-id="51077-698">指出如何處理連入資訊</span><span class="sxs-lookup"><span data-stu-id="51077-698">Indicate how to handle incoming information</span></span>

    <span data-ttu-id="51077-699">正確的版本會更妥善地傳達頁面所達到的目標。</span><span class="sxs-lookup"><span data-stu-id="51077-699">The correct version better communicates the goal achieved by the page.</span></span>

-   <span data-ttu-id="51077-700">**盡可能使用特定動詞。**</span><span class="sxs-lookup"><span data-stu-id="51077-700">**Use specific verbs whenever possible.**</span></span> <span data-ttu-id="51077-701">特定動詞對使用者來說更有意義，而不是泛型。</span><span class="sxs-lookup"><span data-stu-id="51077-701">Specific verbs are more meaningful to users than generic ones.</span></span>
-   <span data-ttu-id="51077-702">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-702">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="51077-703">**如果指令是語句，則不包含最後句號。**</span><span class="sxs-lookup"><span data-stu-id="51077-703">**Don't include final periods if the instruction is a statement.**</span></span> <span data-ttu-id="51077-704">如果指令是問題，請包含最後一個問號。</span><span class="sxs-lookup"><span data-stu-id="51077-704">If the instruction is a question, include a final question mark.</span></span>

### <a name="supplemental-instructions"></a><span data-ttu-id="51077-705">補充指示</span><span class="sxs-lookup"><span data-stu-id="51077-705">Supplemental instructions</span></span>

-   <span data-ttu-id="51077-706">**針對 [中樞] 頁面，請使用選擇性的補充指示，進一步說明 [控制台] 專案的用途。**</span><span class="sxs-lookup"><span data-stu-id="51077-706">**For the hub page, use the optional supplemental instruction to further explain the purpose of the control panel item.**</span></span>
-   <span data-ttu-id="51077-707">**若為輪輻頁面，請使用選擇性補充指示來呈現有助於瞭解或使用頁面的其他資訊。**</span><span class="sxs-lookup"><span data-stu-id="51077-707">**For spoke pages, use the optional supplemental instruction to present additional information helpful to understanding or using the page.**</span></span> <span data-ttu-id="51077-708">您可以提供更詳細的資訊並定義術語。</span><span class="sxs-lookup"><span data-stu-id="51077-708">You can provide more detailed information and define terminology.</span></span>
-   <span data-ttu-id="51077-709">使用完整句子和 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-709">Use complete sentences and [sentence-style capitalization](glossary.md).</span></span>

### <a name="page-text"></a><span data-ttu-id="51077-710">頁面文字</span><span class="sxs-lookup"><span data-stu-id="51077-710">Page text</span></span>

-   <span data-ttu-id="51077-711">**請勿重新聲明內容區域中的主要指示。**</span><span class="sxs-lookup"><span data-stu-id="51077-711">**Don't restate the main instruction in the content area.**</span></span>
-   <span data-ttu-id="51077-712">**使用 "page" 一詞來參考頁面本身。**</span><span class="sxs-lookup"><span data-stu-id="51077-712">**Use the word "page" to refer to the page itself.**</span></span>
-   <span data-ttu-id="51077-713">**使用第二個人 (您的) ，告訴使用者要** 在主要指示和內容區域中執行的動作。</span><span class="sxs-lookup"><span data-stu-id="51077-713">**Use the second person (you, your) to tell users what to do** in the main instruction and content area.</span></span> <span data-ttu-id="51077-714">通常會隱含第二個人。</span><span class="sxs-lookup"><span data-stu-id="51077-714">Often the second person is implied.</span></span>

    <span data-ttu-id="51077-715">**範例︰**</span><span class="sxs-lookup"><span data-stu-id="51077-715">**Example:**</span></span>

    <span data-ttu-id="51077-716">選擇您要列印的圖片。</span><span class="sxs-lookup"><span data-stu-id="51077-716">Choose the pictures you want to print.</span></span>

-   <span data-ttu-id="51077-717">**使用第一個人 (我，我的) 讓使用者知道要** 在內容區域中執行的動作，以回應主要指示。</span><span class="sxs-lookup"><span data-stu-id="51077-717">**Use the first person (I, me, my) to let users tell the control panel item what to do** in the content area that responds to the main instruction.</span></span>

    <span data-ttu-id="51077-718">**範例︰**</span><span class="sxs-lookup"><span data-stu-id="51077-718">**Example:**</span></span>

    <span data-ttu-id="51077-719">列印相機上的相片。</span><span class="sxs-lookup"><span data-stu-id="51077-719">Print the photos on my camera.</span></span>

### <a name="task-links"></a><span data-ttu-id="51077-720">工作連結</span><span class="sxs-lookup"><span data-stu-id="51077-720">Task links</span></span>

-   <span data-ttu-id="51077-721">**選擇清楚的連結文字，以明確地傳達和區分工作連結的用途。**</span><span class="sxs-lookup"><span data-stu-id="51077-721">**Choose concise link text that clearly communicates and differentiates what the task link does.**</span></span> <span data-ttu-id="51077-722">它應該是一目了然的，且對應至主要指令。</span><span class="sxs-lookup"><span data-stu-id="51077-722">It should be self-explanatory and correspond to the main instruction.</span></span> <span data-ttu-id="51077-723">使用者不應該需要找出連結真正的意義，或與其他連結有何不同。</span><span class="sxs-lookup"><span data-stu-id="51077-723">Users shouldn't have to figure out what the link really means or how it differs from other links.</span></span>
-   <span data-ttu-id="51077-724">**一律使用動詞啟動工作連結。**</span><span class="sxs-lookup"><span data-stu-id="51077-724">**Always start task links with a verb.**</span></span>
-   <span data-ttu-id="51077-725">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-725">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="51077-726">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="51077-726">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="51077-727">**如果工作連結需要進一步說明，請使用完整的句子和結束標點符號，在個別的文字控制項中提供說明** 。</span><span class="sxs-lookup"><span data-stu-id="51077-727">**If the task link requires further explanation, provide the explanation in a separate text control** using complete sentences and ending punctuation.</span></span> <span data-ttu-id="51077-728">不過，只有在需要時才新增這類說明，因為另一個工作連結需要一個。</span><span class="sxs-lookup"><span data-stu-id="51077-728">However, add such explanations only when needed don't add explanations to all task links because another task link needs one.</span></span>

<span data-ttu-id="51077-729">如需詳細資訊和範例，請參閱 [連結](ctrl-command-links.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-729">For more information and examples, see [Links](ctrl-command-links.md).</span></span>

### <a name="commit-buttons"></a><span data-ttu-id="51077-730">認可按鈕</span><span class="sxs-lookup"><span data-stu-id="51077-730">Commit buttons</span></span>

-   <span data-ttu-id="51077-731">**使用對自身有意義的特定認可按鈕標籤，並符合主要指令。**</span><span class="sxs-lookup"><span data-stu-id="51077-731">**Use specific commit button labels that make sense on their own and match the main instruction.**</span></span> <span data-ttu-id="51077-732">在理想的情況下，使用者不需要讀取任何其他人來瞭解標籤。</span><span class="sxs-lookup"><span data-stu-id="51077-732">Ideally users shouldn't have to read anything else to understand the label.</span></span> <span data-ttu-id="51077-733">使用者比靜態文字更可能讀取命令按鈕標籤。</span><span class="sxs-lookup"><span data-stu-id="51077-733">Users are far more likely to read command button labels than static text.</span></span>
-   <span data-ttu-id="51077-734">**一律使用動詞來啟動認可按鈕標籤。**</span><span class="sxs-lookup"><span data-stu-id="51077-734">**Always start commit button labels with a verb.**</span></span>
-   <span data-ttu-id="51077-735">**請勿使用 [關閉]、[完成] 或 [完成]。**</span><span class="sxs-lookup"><span data-stu-id="51077-735">**Don't use Close, Done, or Finish.**</span></span> <span data-ttu-id="51077-736">這些按鈕標籤更適合其他類型的視窗。</span><span class="sxs-lookup"><span data-stu-id="51077-736">These button labels are better suited for other types of windows.</span></span>
-   <span data-ttu-id="51077-737">使用 [句子樣式的大小寫](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-737">Use [sentence-style capitalization](glossary.md).</span></span>
-   <span data-ttu-id="51077-738">請勿使用結束標點符號。</span><span class="sxs-lookup"><span data-stu-id="51077-738">Don't use ending punctuation.</span></span>
-   <span data-ttu-id="51077-739">指派唯一的 [存取金鑰](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="51077-739">Assign a unique [access key](glossary.md).</span></span>
    -   <span data-ttu-id="51077-740">**例外狀況：** 請勿將存取金鑰指派給 [取消] 按鈕，因為 Esc 是其存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="51077-740">**Exception:** Don't assign access keys to Cancel buttons, because Esc is its access key.</span></span> <span data-ttu-id="51077-741">這麼做可讓您更輕鬆地指派其他存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="51077-741">Doing so makes the other access keys easier to assign.</span></span>

## <a name="documentation"></a><span data-ttu-id="51077-742">文件</span><span class="sxs-lookup"><span data-stu-id="51077-742">Documentation</span></span>

<span data-ttu-id="51077-743">參考 [控制台] 首頁或類別頁面時：</span><span class="sxs-lookup"><span data-stu-id="51077-743">When referring to the control panel home page or category pages:</span></span>

-   <span data-ttu-id="51077-744">在使用者檔中，請參閱主控台，使用標題樣式的大小寫，並省略前面的明確文章。</span><span class="sxs-lookup"><span data-stu-id="51077-744">In user documentation, refer to Control Panel, using title-style capitalization and omitting a preceding definite article the.</span></span>

    <span data-ttu-id="51077-745">**範例︰**</span><span class="sxs-lookup"><span data-stu-id="51077-745">**Example:**</span></span>

    <span data-ttu-id="51077-746">在主控台中，開啟 [ **安全性中心**]。</span><span class="sxs-lookup"><span data-stu-id="51077-746">In Control Panel, open **Security Center**.</span></span>

-   <span data-ttu-id="51077-747">在程式設計和其他技術檔中，請參閱 [控制台] 首頁和 [控制台類別] 頁面，而不將任何單字變成大寫。</span><span class="sxs-lookup"><span data-stu-id="51077-747">In programming and other technical documentation, refer to control panel home page and control panel category page, without capitalizing any of the words.</span></span> <span data-ttu-id="51077-748">上述的明確文章是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="51077-748">A preceding definite article is optional.</span></span>

<span data-ttu-id="51077-749">針對 [控制台] 專案：</span><span class="sxs-lookup"><span data-stu-id="51077-749">For control panel items:</span></span>

-   <span data-ttu-id="51077-750">參考個別的控制台專案時，請 \[ 在使用者檔中使用「主控台中的控制台專案名稱」 \] 或一般「主控台專案」。</span><span class="sxs-lookup"><span data-stu-id="51077-750">When referring to an individual control panel item, use "\[control panel item name\] in Control Panel" or generally "Control Panel item" in user documentation.</span></span> <span data-ttu-id="51077-751">請勿使用小程式、程式或控制台來參考個別的控制台專案。</span><span class="sxs-lookup"><span data-stu-id="51077-751">Don't use applet, program, or control panel to refer to individual control panel items.</span></span>
-   <span data-ttu-id="51077-752">參考控制台專案的 [中樞] 頁面時，請使用 [主要 \[ 控制台專案名稱 \] ] 頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-752">When referring to a control panel item's hub page, use "main \[control panel item name\] page."</span></span>
-   <span data-ttu-id="51077-753">可能的話，請使用粗體文字來格式化 [控制台] 名稱。</span><span class="sxs-lookup"><span data-stu-id="51077-753">When possible, format the control panel name using bold text.</span></span> <span data-ttu-id="51077-754">否則，請只在必要時才將名稱放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="51077-754">Otherwise, put the name in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="51077-755">範例：</span><span class="sxs-lookup"><span data-stu-id="51077-755">Examples:</span></span>

-   <span data-ttu-id="51077-756">在主控台中，開啟 [ **家長** 監護]。</span><span class="sxs-lookup"><span data-stu-id="51077-756">In Control Panel, open **Parental Controls**.</span></span>
-   <span data-ttu-id="51077-757">回到主要的 [ **家長** 監護] 頁面。</span><span class="sxs-lookup"><span data-stu-id="51077-757">Return to the main **Parental Controls** page.</span></span>

