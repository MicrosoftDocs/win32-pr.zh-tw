---
title: 通知區域
description: 通知區域會提供通知和狀態。 設計完善的程式會適當地使用通知區域，而不會干擾或困擾。
ms.assetid: d30e293f-b424-4fe3-8191-1692c081245d
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 0293038dd155f12b96b22dd1c273a50f1c030ffa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103945578"
---
# <a name="notification-area"></a><span data-ttu-id="94af1-104">通知區域</span><span class="sxs-lookup"><span data-stu-id="94af1-104">Notification Area</span></span>

> [!NOTE]
> <span data-ttu-id="94af1-105">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="94af1-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="94af1-106">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="94af1-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="94af1-107">通知區域會提供通知和狀態。</span><span class="sxs-lookup"><span data-stu-id="94af1-107">The notification area provides notifications and status.</span></span> <span data-ttu-id="94af1-108">設計完善的程式會適當地使用通知區域，而不會干擾或困擾。</span><span class="sxs-lookup"><span data-stu-id="94af1-108">Well-designed programs use the notification area appropriately, without being annoying or distracting.</span></span>

<span data-ttu-id="94af1-109">通知區域是工作列的一部分，可提供通知和狀態的暫時來源。</span><span class="sxs-lookup"><span data-stu-id="94af1-109">The notification area is a portion of the taskbar that provides a temporary source for notifications and status.</span></span> <span data-ttu-id="94af1-110">它也可以用來顯示桌面上沒有任何狀態的系統和程式功能圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-110">It can also be used to display icons for system and program features that have no presence on the desktop.</span></span>

<span data-ttu-id="94af1-111">通知區域中的專案稱為通知區域圖示，如果已清楚地建立通知區域的內容，則只是圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-111">Items in the notification area are referred to as notification area icons, or simply icons if the context of the notification area is already clearly established.</span></span>

![<span data-ttu-id="94af1-112">通知區域、時間和日期的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-112">screen shot of notification area, time, and date</span></span> ](images/winenv-notification-image1.png)

<span data-ttu-id="94af1-113">通知區域。</span><span class="sxs-lookup"><span data-stu-id="94af1-113">The notification area.</span></span>

<span data-ttu-id="94af1-114">若要讓使用者能夠在 Windows 7 中控制其桌面，預設不會顯示所有通知區域圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-114">To give users control of their desktop in Windows 7, not all notification area icons are displayed by default.</span></span> <span data-ttu-id="94af1-115">相反地，除非使用者將圖示升級為通知區域，否則圖示會顯示在通知區域溢位中。</span><span class="sxs-lookup"><span data-stu-id="94af1-115">Rather, icons are displayed in the notification area overflow unless promoted to the notification area by the user.</span></span>

![顯示通知區域和溢位的螢幕擷取畫面。](images/winenv-notification-image2.png)

<span data-ttu-id="94af1-117">通知區域溢位。</span><span class="sxs-lookup"><span data-stu-id="94af1-117">The notification area overflow.</span></span>

<span data-ttu-id="94af1-118">**注意：** 與 [工作列](winenv-taskbar.md)、通知和批註 [提示](mess-notif.md)相關的 [](ctrl-balloons.md)指導方針會顯示在不同的文章中。</span><span class="sxs-lookup"><span data-stu-id="94af1-118">**Note:** Guidelines related to the [taskbar](winenv-taskbar.md), [notifications](mess-notif.md) , and [balloons](ctrl-balloons.md) are presented in separate articles.</span></span>

## <a name="is-this-the-right-user-interface"></a><span data-ttu-id="94af1-119">這是正確的使用者介面嗎？</span><span class="sxs-lookup"><span data-stu-id="94af1-119">Is this the right user interface?</span></span>

<span data-ttu-id="94af1-120">若要決定使用時機，請考量下列問題：</span><span class="sxs-lookup"><span data-stu-id="94af1-120">To decide, consider these questions:</span></span>

-   <span data-ttu-id="94af1-121">**您的程式是否需要顯示通知？**</span><span class="sxs-lookup"><span data-stu-id="94af1-121">**Does your program need to display a notification?**</span></span> <span data-ttu-id="94af1-122">如果是，您必須使用通知區域圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-122">If so, you must use a notification area icon.</span></span>
-   <span data-ttu-id="94af1-123">**圖示是否會暫時顯示，以顯示狀態的變更？**</span><span class="sxs-lookup"><span data-stu-id="94af1-123">**Is the icon displayed temporarily to show a change of status?**</span></span> <span data-ttu-id="94af1-124">如果有的話，可能會有適當的通知區域圖示，視下列因素而定：</span><span class="sxs-lookup"><span data-stu-id="94af1-124">If so, a notification area icon may be appropriate, depending upon the following factors:</span></span>

    -   <span data-ttu-id="94af1-125">**狀態是否有用且相關？**</span><span class="sxs-lookup"><span data-stu-id="94af1-125">**Is the status useful and relevant?**</span></span> <span data-ttu-id="94af1-126">也就是說，使用者是否有可能監視圖示，並因為這項資訊的結果而變更其行為？</span><span class="sxs-lookup"><span data-stu-id="94af1-126">That is, are users likely to monitor the icon and change their behavior as a result of this information?</span></span> <span data-ttu-id="94af1-127">如果不是，則不會顯示狀態，也不會將它放入記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="94af1-127">If not, either don't display the status, or put it in a log file.</span></span>

        <span data-ttu-id="94af1-128">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="94af1-128">**Incorrect:**</span></span>

        ![<span data-ttu-id="94af1-129">具有磁片磁碟機圖示之通知區域的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-129">screen shot of notification area with drive icon</span></span> ](images/winenv-notification-image3.png)

        <span data-ttu-id="94af1-130">在此範例中，磁片磁碟機活動圖示並不適當，因為使用者不太可能會根據它來變更其行為。</span><span class="sxs-lookup"><span data-stu-id="94af1-130">In this example, the disk drive activity icon is inappropriate because users are unlikely to change their behavior based on it.</span></span>

    -   <span data-ttu-id="94af1-131">**狀態是否危急？是否需要立即採取動作？**</span><span class="sxs-lookup"><span data-stu-id="94af1-131">**Is the status critical? Is immediate action required?**</span></span> <span data-ttu-id="94af1-132">如果是的話，請以需要注意的方式來顯示資訊，而且無法輕易地忽略，例如 [對話方塊](win-dialog-box.md)。</span><span class="sxs-lookup"><span data-stu-id="94af1-132">If so, display the information in a way that demands attention and cannot be easily ignored, such as a [dialog box](win-dialog-box.md).</span></span>

    <span data-ttu-id="94af1-133">針對 Windows 7 設計的程式可以使用程式工作列按鈕上的重迭圖示來顯示狀態的變更，以及工作列按鈕的進度列，以顯示長時間執行之工作的進度。</span><span class="sxs-lookup"><span data-stu-id="94af1-133">Programs designed for Windows 7 can use overlay icons on the program's taskbar button to show change of status, as well as taskbar button progress bars to show progress of long-running tasks.</span></span>

-   <span data-ttu-id="94af1-134">**功能是否已經有「桌上型電腦目前狀態」？**</span><span class="sxs-lookup"><span data-stu-id="94af1-134">**Does the feature already have "desktop presence"?**</span></span> <span data-ttu-id="94af1-135">也就是說，執行時，功能是否會出現在桌面的視窗中 (可能會最小化) ？</span><span class="sxs-lookup"><span data-stu-id="94af1-135">That is, when run, does the feature appear in a window on the desktop (possibly minimized)?</span></span> <span data-ttu-id="94af1-136">如果是的話，請在程式的 [狀態列](ctrl-status-bars.md)、其他狀態區域，或是直接在工作列按鈕上，顯示 Windows 7 的狀態。</span><span class="sxs-lookup"><span data-stu-id="94af1-136">If so, display status in the program's [status bar](ctrl-status-bars.md), other status area, or, for Windows 7, directly on the taskbar button.</span></span> <span data-ttu-id="94af1-137">如果功能沒有桌上型電腦存在，您可以使用圖示進行程式存取，並顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="94af1-137">If the feature doesn't have desktop presence, you can use an icon for program access and to show status.</span></span>
-   <span data-ttu-id="94af1-138">**圖示主要是用來快速啟動程式或存取其功能或設定？**</span><span class="sxs-lookup"><span data-stu-id="94af1-138">**Is the icon primarily to launch a program or access its features or settings quickly?**</span></span> <span data-ttu-id="94af1-139">若是如此，請改用 [開始] 功能表來啟動程式。</span><span class="sxs-lookup"><span data-stu-id="94af1-139">If so, use the Start menu to launch programs instead.</span></span> <span data-ttu-id="94af1-140">通知區域不適用於快速程式或命令存取。</span><span class="sxs-lookup"><span data-stu-id="94af1-140">The notification area isn't intended for quick program or command access.</span></span>

    ![<span data-ttu-id="94af1-141">[快速啟動] 工具列的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-141">screen shot of quick launch toolbar</span></span> ](images/winenv-notification-image4.png)

    <span data-ttu-id="94af1-142">在此範例中，Windows Vista 會使用快速啟動來快速啟動 Windows 檔案總管和 Windows Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="94af1-142">In this example from Windows Vista, Quick Launch is used to launch Windows Explorer and Windows Internet Explorer quickly.</span></span>

    <span data-ttu-id="94af1-143">針對 Windows 7 的設計程式，使用者可以釘選工作列按鈕以進行快速程式存取。</span><span class="sxs-lookup"><span data-stu-id="94af1-143">For programs designed for Windows 7, users can pin taskbar buttons for quick program access.</span></span> <span data-ttu-id="94af1-144">程式可以使用捷徑清單或縮圖工具列，直接從程式的工具列按鈕存取常用的命令。</span><span class="sxs-lookup"><span data-stu-id="94af1-144">Programs can use a Jump List or thumbnail toolbar to access frequently used commands directly from a program's toolbar button.</span></span> <span data-ttu-id="94af1-145">在 Windows 7 中，預設不會顯示快速啟動區域。</span><span class="sxs-lookup"><span data-stu-id="94af1-145">The Quick Launch area isn't displayed by default in Windows 7.</span></span>

    ![<span data-ttu-id="94af1-146">具有圖示的工作列和跳躍清單螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-146">screen shot of taskbar and jump list with icons</span></span> ](images/winenv-notification-image5.png)

    <span data-ttu-id="94af1-147">在此範例中，會使用捷徑清單來存取快速命令。</span><span class="sxs-lookup"><span data-stu-id="94af1-147">In this example, a Jump List is used for quick command access.</span></span>

## <a name="design-concepts"></a><span data-ttu-id="94af1-148">設計概念</span><span class="sxs-lookup"><span data-stu-id="94af1-148">Design concepts</span></span>

### <a name="the-windows-desktop"></a><span data-ttu-id="94af1-149">Windows 桌面</span><span class="sxs-lookup"><span data-stu-id="94af1-149">The Windows desktop</span></span>

<span data-ttu-id="94af1-150">Windows 桌面具有下列程式存取點：</span><span class="sxs-lookup"><span data-stu-id="94af1-150">The Windows desktop has the following program access points:</span></span>

-   <span data-ttu-id="94af1-151">**工作區。**</span><span class="sxs-lookup"><span data-stu-id="94af1-151">**Work area.**</span></span> <span data-ttu-id="94af1-152">使用者可以執行其工作的螢幕區域，以及儲存程式、檔和其快捷方式。</span><span class="sxs-lookup"><span data-stu-id="94af1-152">The onscreen area where users can perform their work, as well as store programs, documents, and their shortcuts.</span></span> <span data-ttu-id="94af1-153">雖然在技術上，桌面包含工作列，但在大部分的情況下，它只會參考工作區域。</span><span class="sxs-lookup"><span data-stu-id="94af1-153">While technically the desktop includes the taskbar, in most contexts it refers just to the work area.</span></span>
-   <span data-ttu-id="94af1-154">**[開始] 按鈕。**</span><span class="sxs-lookup"><span data-stu-id="94af1-154">**Start button.**</span></span> <span data-ttu-id="94af1-155">所有程式和特殊 Windows 的存取點都將 (檔、圖片、音樂、遊戲、電腦主控台) 、使用「最近使用的」清單來快速存取最近使用的程式和檔。</span><span class="sxs-lookup"><span data-stu-id="94af1-155">The access point for all programs and special Windows places (Documents, Pictures, Music, Games, Computer, Control Panel), with "most recently used" lists for quick access to recently used programs and documents.</span></span>
-   <span data-ttu-id="94af1-156">**快速啟動。**</span><span class="sxs-lookup"><span data-stu-id="94af1-156">**Quick Launch.**</span></span> <span data-ttu-id="94af1-157">使用者選取之程式的直接存取點。</span><span class="sxs-lookup"><span data-stu-id="94af1-157">A direct access point for programs selected by the user.</span></span> <span data-ttu-id="94af1-158">快速啟動已從 Windows 7 移除。</span><span class="sxs-lookup"><span data-stu-id="94af1-158">Quick Launch was removed from Windows 7.</span></span>
-   <span data-ttu-id="94af1-159">**任務。**</span><span class="sxs-lookup"><span data-stu-id="94af1-159">**Taskbar.**</span></span> <span data-ttu-id="94af1-160">執行具有桌上型電腦狀態之程式的存取點。</span><span class="sxs-lookup"><span data-stu-id="94af1-160">The access point for running programs that have desktop presence.</span></span> <span data-ttu-id="94af1-161">雖然在技術上，工作列橫跨 [開始] 按鈕到通知區域的整個橫條，但是在大部分的內容中，工作列都指的是介於中間的區域，其中包含工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="94af1-161">While technically the taskbar spans the entire bar from the Start button to the notification area, in most contexts taskbar refers to the area in between, containing the taskbar buttons.</span></span> <span data-ttu-id="94af1-162">此區域有時稱為 taskband。</span><span class="sxs-lookup"><span data-stu-id="94af1-162">This area is sometimes referred to as the taskband.</span></span>
-   <span data-ttu-id="94af1-163">**Deskbands.不建議使用。**</span><span class="sxs-lookup"><span data-stu-id="94af1-163">**Deskbands. Not recommended.**</span></span>
-   <span data-ttu-id="94af1-164">**通知區域。**</span><span class="sxs-lookup"><span data-stu-id="94af1-164">**Notification area.**</span></span> <span data-ttu-id="94af1-165">通知和狀態的短期來源，以及不存在於桌面上的系統和程式相關功能的存取點。</span><span class="sxs-lookup"><span data-stu-id="94af1-165">A short-term source for notifications and status, as well as an access point for system- and program-related features that have no presence on the desktop.</span></span>

![<span data-ttu-id="94af1-166">識別桌面存取點的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-166">screen shot identifying desktop access points</span></span> ](images/winenv-notification-image6.png)

<span data-ttu-id="94af1-167">Windows 桌面存取點包含 [開始] 按鈕、工作列和通知區域。</span><span class="sxs-lookup"><span data-stu-id="94af1-167">The Windows desktop access points include the Start button, taskbar, and notification area.</span></span> <span data-ttu-id="94af1-168">請注意工作列按鈕的縮圖功能。</span><span class="sxs-lookup"><span data-stu-id="94af1-168">Note the thumbnail feature of the taskbar button.</span></span>

<span data-ttu-id="94af1-169">**桌面是受限的共用資源，是使用者進入 Windows 的進入點。**</span><span class="sxs-lookup"><span data-stu-id="94af1-169">**The desktop is a limited, shared resource that is the user's entry point to Windows.**</span></span> <span data-ttu-id="94af1-170">讓使用者保持控制。</span><span class="sxs-lookup"><span data-stu-id="94af1-170">Leave users in control.</span></span> <span data-ttu-id="94af1-171">您應以預期的方式使用桌面區域，否則應該將任何其他用途視為濫用。</span><span class="sxs-lookup"><span data-stu-id="94af1-171">You should use the desktop areas as intended any other usage should be considered an abuse.</span></span> <span data-ttu-id="94af1-172">例如，絕對不要將桌面區域視為推廣程式或其 [品牌](exper-branding.md)的方式。</span><span class="sxs-lookup"><span data-stu-id="94af1-172">For example, never view desktop areas as ways to promote your program or its [Brand](exper-branding.md).</span></span>

### <a name="using-the-notification-area-appropriately"></a><span data-ttu-id="94af1-173">適當地使用通知區域</span><span class="sxs-lookup"><span data-stu-id="94af1-173">Using the notification area appropriately</span></span>

<span data-ttu-id="94af1-174">通知區域最初是作為通知和狀態的暫時來源。</span><span class="sxs-lookup"><span data-stu-id="94af1-174">The notification area was originally intended as a temporary source for notifications and status.</span></span> <span data-ttu-id="94af1-175">它的效率與便利性鼓勵開發人員提供其他用途，例如啟動程式和執行命令。</span><span class="sxs-lookup"><span data-stu-id="94af1-175">Its efficiency and convenience has encouraged developers to give it other purposes, such as launching programs and executing commands.</span></span> <span data-ttu-id="94af1-176">可惜的是，這些新增專案讓通知區域變得太大和雜訊，並與其他桌面存取點混淆。</span><span class="sxs-lookup"><span data-stu-id="94af1-176">Unfortunately over time, these additions made the notification area too large and noisy, and confused its purpose with the other desktop access points.</span></span>

<span data-ttu-id="94af1-177">Windows XP 藉由使區域可折迭並隱藏未使用的圖示，來解決調整問題。</span><span class="sxs-lookup"><span data-stu-id="94af1-177">Windows XP addressed the scale problem by making the area collapsible and hiding the unused icons.</span></span> <span data-ttu-id="94af1-178">Windows Vista 藉由移除不必要、討厭的通知來解決干擾。</span><span class="sxs-lookup"><span data-stu-id="94af1-178">Windows Vista addressed the noise by removing unnecessary, annoying notifications.</span></span> <span data-ttu-id="94af1-179">Windows 7 更進一步的原因是，將通知的原始目的放在通知來源。</span><span class="sxs-lookup"><span data-stu-id="94af1-179">Windows 7 has gone a step further by focusing the notification on its original purpose of being a notification source.</span></span> <span data-ttu-id="94af1-180">**在 Windows 7 中，大部分的圖示都是隱藏的，但使用者可以手動升級至通知區域。為了讓使用者能夠掌控其桌面，您的程式無法自動執行這項升級。**</span><span class="sxs-lookup"><span data-stu-id="94af1-180">**Most icons are hidden by default in Windows 7, but can be promoted to the notification area manually, by the user. To keep users in control of their desktops, there is no way for your program to perform this promotion automatically.**</span></span> <span data-ttu-id="94af1-181">Windows 仍會暫時加以升級，以顯示隱藏圖示的通知。</span><span class="sxs-lookup"><span data-stu-id="94af1-181">Windows still displays notifications for hidden icons by promoting them temporarily.</span></span>

![<span data-ttu-id="94af1-182">通知區域和溢位的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-182">screen shot of notification area and overflow</span></span> ](images/winenv-notification-image7.png)

<span data-ttu-id="94af1-183">在 Windows 7 中，預設會隱藏大部分的通知區域圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-183">In Windows 7, most notification area icons are hidden by default.</span></span>

<span data-ttu-id="94af1-184">此外，Windows 7 也直接在工作列按鈕中支援許多功能。</span><span class="sxs-lookup"><span data-stu-id="94af1-184">In addition, Windows 7 supports many features directly in the taskbar buttons.</span></span> <span data-ttu-id="94af1-185">具體而言，您可以使用：</span><span class="sxs-lookup"><span data-stu-id="94af1-185">Specifically, you can use:</span></span>

-   <span data-ttu-id="94af1-186">跳躍清單和縮圖工具列可快速存取常用的命令。</span><span class="sxs-lookup"><span data-stu-id="94af1-186">Jump Lists and thumbnail toolbars to quickly access frequently used commands.</span></span>
-   <span data-ttu-id="94af1-187">覆迭圖示，以顯示執行中程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="94af1-187">Overlay icons to show status for running programs.</span></span>
-   <span data-ttu-id="94af1-188">用來顯示長時間執行之工作進度的工作列按鈕進度列。</span><span class="sxs-lookup"><span data-stu-id="94af1-188">Taskbar button progress bars to show progress for long-running tasks.</span></span>

<span data-ttu-id="94af1-189">簡單地說，如果您的程式有桌上型電腦存在，請充分利用 Windows 7 工作列按鈕功能來進行這些工作。</span><span class="sxs-lookup"><span data-stu-id="94af1-189">In short, if your program has desktop presence, take full advantage of the Windows 7 taskbar button features for these purposes.</span></span> <span data-ttu-id="94af1-190">**讓通知區域圖示專注于顯示通知和狀態。**</span><span class="sxs-lookup"><span data-stu-id="94af1-190">**Keep the notification area icons focused on displaying notifications and status.**</span></span>

### <a name="keeping-users-in-control"></a><span data-ttu-id="94af1-191">讓使用者保持掌控</span><span class="sxs-lookup"><span data-stu-id="94af1-191">Keeping users in control</span></span>

<span data-ttu-id="94af1-192">讓控制項保持在外，不會正確地使用通知區域。</span><span class="sxs-lookup"><span data-stu-id="94af1-192">Keeping users in control extends beyond using the notification area correctly.</span></span> <span data-ttu-id="94af1-193">視圖標的本質而定，您可能會想要讓使用者執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="94af1-193">Depending on the nature of your icon, you may want to let users do the following:</span></span>

-   <span data-ttu-id="94af1-194">**移除圖示。**</span><span class="sxs-lookup"><span data-stu-id="94af1-194">**Remove the icon.**</span></span> <span data-ttu-id="94af1-195">您的圖示可能會提供相關的有用狀態，但使用者可能不會想要看到它。</span><span class="sxs-lookup"><span data-stu-id="94af1-195">Your icon may provide relevant, useful status, but even so, users may not want to see it.</span></span> <span data-ttu-id="94af1-196">Windows 允許使用者隱藏圖示，但這項功能不容易找到。</span><span class="sxs-lookup"><span data-stu-id="94af1-196">Windows allows users to hide icons, but this feature isn't easily discoverable.</span></span> <span data-ttu-id="94af1-197">若要讓使用者保持控制，請在圖示內容功能表上的 [ **通知區域] 選項中提供顯示圖示** 。</span><span class="sxs-lookup"><span data-stu-id="94af1-197">To keep users in control, provide a **Display icon in notification area** option on the icon's context menu.</span></span> <span data-ttu-id="94af1-198">請注意，移除圖示不需要影響基礎程式、功能或流程。</span><span class="sxs-lookup"><span data-stu-id="94af1-198">Note that removing an icon doesn't have to affect the underlying program, feature, or process.</span></span>
-   <span data-ttu-id="94af1-199">**選取要顯示的通知類型。**</span><span class="sxs-lookup"><span data-stu-id="94af1-199">**Select types of notifications to display.**</span></span> <span data-ttu-id="94af1-200">您的通知必須有用且相關，但可能會有使用者不想看到的通知。</span><span class="sxs-lookup"><span data-stu-id="94af1-200">Your notification must be useful and relevant, but there may be notifications that users don't want to see.</span></span> <span data-ttu-id="94af1-201">這特別適用于僅供參考 [通知](mess-notif.md)。</span><span class="sxs-lookup"><span data-stu-id="94af1-201">This is especially true for FYI [notifications](mess-notif.md).</span></span> <span data-ttu-id="94af1-202">讓使用者選擇啟用較不重要的專案。</span><span class="sxs-lookup"><span data-stu-id="94af1-202">Let users choose to enable the less important ones.</span></span>
-   <span data-ttu-id="94af1-203">**暫止選用功能。**</span><span class="sxs-lookup"><span data-stu-id="94af1-203">**Suspend optional features.**</span></span> <span data-ttu-id="94af1-204">圖示可用來顯示功能的狀態，而不會顯示桌面。</span><span class="sxs-lookup"><span data-stu-id="94af1-204">Icons are used to display status for features without desktop presence.</span></span> <span data-ttu-id="94af1-205">這類功能通常會是長時間執行的選擇性背景工作，例如列印、編制索引、掃描或同步處理。</span><span class="sxs-lookup"><span data-stu-id="94af1-205">Such features tend to be long-running, optional background tasks, such as printing, indexing, scanning, or synchronizing.</span></span> <span data-ttu-id="94af1-206">使用者可能會想要暫停這類功能，以提高系統效能、降低耗電量，或是因為它們已離線。</span><span class="sxs-lookup"><span data-stu-id="94af1-206">Users may want to suspend such features to increase system performance, reduce power consumption, or because they are offline.</span></span>
-   <span data-ttu-id="94af1-207">**結束程式。**</span><span class="sxs-lookup"><span data-stu-id="94af1-207">**Quit the program.**</span></span> <span data-ttu-id="94af1-208">提供更適合的選項：</span><span class="sxs-lookup"><span data-stu-id="94af1-208">Provide the more suitable of these options:</span></span>
    -   <span data-ttu-id="94af1-209">**暫時退出程式。**</span><span class="sxs-lookup"><span data-stu-id="94af1-209">**Temporarily quit program.**</span></span> <span data-ttu-id="94af1-210">重新開機 Windows 時，會停止並重新啟動程式。</span><span class="sxs-lookup"><span data-stu-id="94af1-210">The program is stopped and restarted when Windows is restarted.</span></span> <span data-ttu-id="94af1-211">這種方法適用于重要的系統公用程式，例如安全性程式。</span><span class="sxs-lookup"><span data-stu-id="94af1-211">This approach is suitable for important system utilities such as security programs.</span></span>
    -   <span data-ttu-id="94af1-212">**永久終止程式。**</span><span class="sxs-lookup"><span data-stu-id="94af1-212">**Permanently quit program.**</span></span> <span data-ttu-id="94af1-213">重新開機 Windows 時，程式會停止且不會重新開機 (除非使用者選擇稍後重新開機) 。</span><span class="sxs-lookup"><span data-stu-id="94af1-213">The program is stopped and not restarted when Windows is restarted (unless the user chooses to restart later).</span></span> <span data-ttu-id="94af1-214">使用者不想再執行程式，或想要視需要執行程式，也許可以改善系統效能。</span><span class="sxs-lookup"><span data-stu-id="94af1-214">Either the user no longer wants to run the program, or wants to run the program on demand perhaps to improve system performance.</span></span>

<span data-ttu-id="94af1-215">雖然最好在圖示的內容功能表上提供大部分的設定，但程式的預設體驗應該適用于大部分的使用者。</span><span class="sxs-lookup"><span data-stu-id="94af1-215">Although it's a good idea to provide most of these settings on the icon's context menu, the program's default experience should be suitable for most users.</span></span> <span data-ttu-id="94af1-216">預設不會開啟任何專案，而且會預期使用者關閉功能。</span><span class="sxs-lookup"><span data-stu-id="94af1-216">Don't turn everything on by default and expect users to turn features off.</span></span> <span data-ttu-id="94af1-217">相反地，根據預設，將重要功能開啟，讓使用者能夠視需要啟用其他功能。</span><span class="sxs-lookup"><span data-stu-id="94af1-217">Rather, turn the important features on by default, and let users enable additional features as desired.</span></span>

<span data-ttu-id="94af1-218">**如果您只進行四件事 .。。**</span><span class="sxs-lookup"><span data-stu-id="94af1-218">**If you do only four things...**</span></span>

1.  <span data-ttu-id="94af1-219">請勿濫用通知區域。</span><span class="sxs-lookup"><span data-stu-id="94af1-219">Don't abuse the notification area.</span></span> <span data-ttu-id="94af1-220">您只能將它用於通知和狀態的來源，以及沒有桌上型電腦狀態的功能。</span><span class="sxs-lookup"><span data-stu-id="94af1-220">Use it only as a source for notifications and status, and for features without desktop presence.</span></span>
2.  <span data-ttu-id="94af1-221">讓使用者保持掌控。</span><span class="sxs-lookup"><span data-stu-id="94af1-221">Keep users in control.</span></span> <span data-ttu-id="94af1-222">提供適當的選項來控制圖示、其通知和基礎功能。</span><span class="sxs-lookup"><span data-stu-id="94af1-222">Provide appropriate options to control the icon, its notifications, and the underlying features.</span></span>
3.  <span data-ttu-id="94af1-223">提供適用于大部分使用者的預設體驗。</span><span class="sxs-lookup"><span data-stu-id="94af1-223">Present a default experience that is suitable for most users.</span></span> <span data-ttu-id="94af1-224">讓使用者能夠啟用所需的功能，而不是預期的功能。</span><span class="sxs-lookup"><span data-stu-id="94af1-224">Let users enable desired features rather than expect them to disable undesired ones.</span></span>
4.  <span data-ttu-id="94af1-225">充分利用 Windows 7 工作列按鈕功能來顯示狀態，並讓您的程式最常執行的工作更有效率。</span><span class="sxs-lookup"><span data-stu-id="94af1-225">Take full advantage of the Windows 7 taskbar button features to show status and make your program's most frequently performed tasks efficient.</span></span>

## <a name="usage-patterns"></a><span data-ttu-id="94af1-226">使用模式</span><span class="sxs-lookup"><span data-stu-id="94af1-226">Usage patterns</span></span>

<span data-ttu-id="94af1-227">通知區域圖示有數種使用模式：</span><span class="sxs-lookup"><span data-stu-id="94af1-227">Notification area icons have several usage patterns:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="94af1-228"><strong>系統狀態和存取</strong></span><span class="sxs-lookup"><span data-stu-id="94af1-228"><strong>System status and access</strong></span></span><br/> <span data-ttu-id="94af1-229">持續顯示，以顯示重要但非重大的系統狀態，以及提供對相關功能和設定的存取權。</span><span class="sxs-lookup"><span data-stu-id="94af1-229">Displayed continuously to show important but not critical system status, and to provide access to relevant features and settings.</span></span> <br/></td>
<td><span data-ttu-id="94af1-230">需要通知區域圖示的系統功能不會有持續性的桌面存在。</span><span class="sxs-lookup"><span data-stu-id="94af1-230">System features that need notification area icons have no persistent desktop presence.</span></span> <span data-ttu-id="94af1-231">也可以當做通知來源使用。</span><span class="sxs-lookup"><span data-stu-id="94af1-231">Can also be used as a notification source.</span></span> <br/> <img src="images/winenv-notification-image8.png" alt="Screenshot that shows a notification area and icons for system status." /><br/> <span data-ttu-id="94af1-232">在此範例中，電池、網路和磁片區圖示會在適用時持續顯示。</span><span class="sxs-lookup"><span data-stu-id="94af1-232">In this example, the battery, network, and volume icons are displayed continuously when applicable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94af1-233"><strong>背景工作狀態和存取權</strong></span><span class="sxs-lookup"><span data-stu-id="94af1-233"><strong>Background task status and access</strong></span></span><br/> <span data-ttu-id="94af1-234">在背景工作執行時顯示，以顯示狀態並提供功能和設定的存取權。</span><span class="sxs-lookup"><span data-stu-id="94af1-234">Displayed while a background task is running to show status and provide access to features and settings.</span></span> <br/></td>
<td><span data-ttu-id="94af1-235">背景進程如果沒有桌上型電腦，則需要通知區域圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-235">Background processes need notification area icons when they have no desktop presence.</span></span> <span data-ttu-id="94af1-236">也可以當做通知來源使用。</span><span class="sxs-lookup"><span data-stu-id="94af1-236">Can also be used as a notification source.</span></span> <br/> <img src="images/winenv-notification-image9.png" alt="Screenshot that shows notification area and icon for background task status." /><br/> <span data-ttu-id="94af1-237">在此範例中，[動作中心] 圖示可讓使用者檢查其狀態（即使沒有桌上型電腦）。</span><span class="sxs-lookup"><span data-stu-id="94af1-237">In this example, the Action Center icon allows users to check its status even when it has no desktop presence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="94af1-238"><strong>暫存事件狀態</strong></span><span class="sxs-lookup"><span data-stu-id="94af1-238"><strong>Temporary event status</strong></span></span><br/> <span data-ttu-id="94af1-239">具有桌上型電腦狀態的程式可以暫時顯示圖示，以顯示狀態的重要事件或變更。</span><span class="sxs-lookup"><span data-stu-id="94af1-239">Programs with desktop presence can display icons temporarily to show important events or changes in status.</span></span> <br/></td>
<td><img src="images/winenv-notification-image10.png" alt="Screenshot that shows notification area and icons for a temporary event status." /><br/> <span data-ttu-id="94af1-240">在此範例中，會暫時顯示用於列印和安裝更新的圖示，以顯示狀態中的重要事件或變更。</span><span class="sxs-lookup"><span data-stu-id="94af1-240">In this example, icons for printing and installing updates are displayed temporarily to show important events or changes in status.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94af1-241"><strong>暫時通知來源</strong></span><span class="sxs-lookup"><span data-stu-id="94af1-241"><strong>Temporary notification source</strong></span></span><br/> <span data-ttu-id="94af1-242">暫時顯示以顯示通知。</span><span class="sxs-lookup"><span data-stu-id="94af1-242">Displayed temporarily to show a notification.</span></span> <span data-ttu-id="94af1-243">在超時之後，或當基礎問題已解決或工作執行時移除。</span><span class="sxs-lookup"><span data-stu-id="94af1-243">Removed after a timeout, or when the underlying problem is addressed or task performed.</span></span> <br/></td>
<td><span data-ttu-id="94af1-244">單純的通知來源偏好暫存圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-244">Temporary icons are preferred for pure notification sources.</span></span> <span data-ttu-id="94af1-245">請勿顯示不提供實用、相關、動態狀態的圖示，因為功能可能需要在未來顯示通知。</span><span class="sxs-lookup"><span data-stu-id="94af1-245">Don't display an icon that doesn't provide useful, relevant, dynamic status just because a feature might need to display a notification in the future.</span></span> <br/> <img src="images/winenv-notification-image11.png" alt="Screen shot of notification area install message " /><br/> <span data-ttu-id="94af1-246">在此範例中，會顯示「隨插即用」圖示，並顯示新的硬體偵測到通知。</span><span class="sxs-lookup"><span data-stu-id="94af1-246">In this example, the plug-and-play icon is displayed while a new hardware detected notification is shown.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="94af1-247"><strong>最小化單一實例應用程式</strong></span><span class="sxs-lookup"><span data-stu-id="94af1-247"><strong>Minimized single-instance application</strong></span></span><br/> <span data-ttu-id="94af1-248">為了減少工作列雜亂，單一實例、長時間執行的應用程式可以改為最小化到通知區域的圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-248">To reduce taskbar clutter, a single-instance, long-running application can be minimized to a notification area icon instead.</span></span> <br/></td>
<td><img src="images/winenv-notification-image12.png" alt="Screen shot of notification area and icons " /><br/> <span data-ttu-id="94af1-249">在此範例中，從 Windows Vista 開始，Outlook 和 Windows Live Messenger 是單一實例的應用程式，最小化到通知區域圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-249">In this example from Windows Vista, Outlook and Windows Live Messenger are single-instance applications that minimize to notification area icons.</span></span><br/> <span data-ttu-id="94af1-250">只有在下列所有情況都適用時，才考慮使用此模式：</span><span class="sxs-lookup"><span data-stu-id="94af1-250">Consider using this pattern only if all of the following apply:</span></span> <br/>
<ul>
<li><span data-ttu-id="94af1-251">應用程式只能有單一實例。</span><span class="sxs-lookup"><span data-stu-id="94af1-251">The application can have only a single instance.</span></span></li>
<li><span data-ttu-id="94af1-252">應用程式會執行一段很長的時間。</span><span class="sxs-lookup"><span data-stu-id="94af1-252">The application is run for an extended period of time.</span></span></li>
<li><span data-ttu-id="94af1-253">圖示會顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="94af1-253">The icon shows status.</span></span></li>
<li><span data-ttu-id="94af1-254">圖示可以是通知來源。</span><span class="sxs-lookup"><span data-stu-id="94af1-254">The icon can be a notification source.</span></span></li>
<li><span data-ttu-id="94af1-255">這麼做是選擇性的，使用者必須 <a href="glossary.md">加入宣告</a>。</span><span class="sxs-lookup"><span data-stu-id="94af1-255">Doing so is optional and users must <a href="glossary.md">opt in</a>.</span></span></li>
</ul>
<span data-ttu-id="94af1-256">如果所有條件都適用，則將圖示降至最低會在需要只有一個時，才會有兩個存取點。</span><span class="sxs-lookup"><span data-stu-id="94af1-256">If all these conditions apply, minimizing to an icon eliminates having two access points when only one is necessary.</span></span> <br/> <span data-ttu-id="94af1-257"><strong>注意：</strong> Windows 7 不再建議使用此圖示模式。</span><span class="sxs-lookup"><span data-stu-id="94af1-257"><strong>Note:</strong> This icon pattern is no longer recommended for Windows 7.</span></span> <span data-ttu-id="94af1-258">如果您的程式有桌上型電腦存在，請改用一般工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="94af1-258">Use regular taskbar buttons instead if your program has desktop presence.</span></span><br/> <img src="images/winenv-notification-image13.png" alt="Screen shot of Outlook and Messenger taskbar icons " /><br/> <span data-ttu-id="94af1-259">在此範例中，Windows 7 的一般工作列按鈕幾乎沒有空間，而是從 Windows 7 工作列按鈕功能獲益，包括跳躍清單、重迭圖示，以及豐富的縮圖。</span><span class="sxs-lookup"><span data-stu-id="94af1-259">In this example from Windows 7, a regular taskbar button takes little space, but benefits from the Windows 7 taskbar button features, including Jump Lists, overlay icons, and rich thumbnails.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="guidelines"></a><span data-ttu-id="94af1-260">指導方針</span><span class="sxs-lookup"><span data-stu-id="94af1-260">Guidelines</span></span>

### <a name="general"></a><span data-ttu-id="94af1-261">一般</span><span class="sxs-lookup"><span data-stu-id="94af1-261">General</span></span>

-   <span data-ttu-id="94af1-262">**每個元件只提供一個通知區域圖示。**</span><span class="sxs-lookup"><span data-stu-id="94af1-262">**Provide only one notification area icon per component.**</span></span>
-   <span data-ttu-id="94af1-263">**使用具有16x16、20x20 和24x24 圖元版本的圖示。**</span><span class="sxs-lookup"><span data-stu-id="94af1-263">**Use an icon with 16x16, 20x20, and 24x24 pixel versions.**</span></span> <span data-ttu-id="94af1-264">較大的版本會在高 DPI 的顯示模式中使用。</span><span class="sxs-lookup"><span data-stu-id="94af1-264">The larger versions are used in high-dpi display modes.</span></span>

### <a name="when-to-show"></a><span data-ttu-id="94af1-265">顯示時機</span><span class="sxs-lookup"><span data-stu-id="94af1-265">When to show</span></span>

-   <span data-ttu-id="94af1-266">針對暫時通知來源模式：</span><span class="sxs-lookup"><span data-stu-id="94af1-266">For the temporary notification source pattern:</span></span>
    -   <span data-ttu-id="94af1-267">Windows 會在顯示通知時顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-267">Windows displays the icon when the notification is displayed.</span></span>
    -   <span data-ttu-id="94af1-268">根據其 [通知設計](mess-notif.md) 模式來移除圖示：</span><span class="sxs-lookup"><span data-stu-id="94af1-268">Remove the icon based on its [notification design](mess-notif.md) pattern:</span></span>



    | <span data-ttu-id="94af1-269">模式</span><span class="sxs-lookup"><span data-stu-id="94af1-269">Pattern</span></span>                                     | <span data-ttu-id="94af1-270">何時移除</span><span class="sxs-lookup"><span data-stu-id="94af1-270">When to remove</span></span>                                         |
    |--------------------------------------|------------------------------------------|
    | <span data-ttu-id="94af1-271">動作成功</span><span class="sxs-lookup"><span data-stu-id="94af1-271">Action success</span></span><br/>            | <span data-ttu-id="94af1-272">當通知被移除時。</span><span class="sxs-lookup"><span data-stu-id="94af1-272">When notification is removed.</span></span><br/> |
    | <span data-ttu-id="94af1-273">動作失敗</span><span class="sxs-lookup"><span data-stu-id="94af1-273">Action failure</span></span><br/>            | <span data-ttu-id="94af1-274">解決問題時。</span><span class="sxs-lookup"><span data-stu-id="94af1-274">When problem is resolved.</span></span><br/>     |
    | <span data-ttu-id="94af1-275">非重大系統事件</span><span class="sxs-lookup"><span data-stu-id="94af1-275">Non-critical system event</span></span><br/> | <span data-ttu-id="94af1-276">解決問題時。</span><span class="sxs-lookup"><span data-stu-id="94af1-276">When problem is resolved.</span></span><br/>     |
    | <span data-ttu-id="94af1-277">選用的使用者工作</span><span class="sxs-lookup"><span data-stu-id="94af1-277">Optional user task</span></span><br/>        | <span data-ttu-id="94af1-278">當工作完成時。</span><span class="sxs-lookup"><span data-stu-id="94af1-278">When task is done.</span></span><br/>            |
    | <span data-ttu-id="94af1-279">僅供參考</span><span class="sxs-lookup"><span data-stu-id="94af1-279">FYI</span></span><br/>                       | <span data-ttu-id="94af1-280">當通知被移除時。</span><span class="sxs-lookup"><span data-stu-id="94af1-280">When notification is removed.</span></span><br/> |



 

-   <span data-ttu-id="94af1-281">**針對暫存事件狀態模式，在事件發生時顯示圖示。**</span><span class="sxs-lookup"><span data-stu-id="94af1-281">**For the temporary event status pattern, display the icon while the event is happening.**</span></span>
-   <span data-ttu-id="94af1-282">若為所有其他模式，請在 **程式、功能或進程正在執行時顯示圖示** ，除非使用者已 **在 [通知區域** ] 選項中清除其顯示圖示，否則會顯示圖示 (如需詳細資訊，請參閱 [內容功能表](#context-menus)) 。</span><span class="sxs-lookup"><span data-stu-id="94af1-282">For all other patterns, **display the icon when the program, feature, or process is running and the icon is relevant** unless the user has cleared its **Display icon in notification area** option (for more information, see [Context menus](#context-menus)).</span></span> <span data-ttu-id="94af1-283">在 Windows 7 中，大部分的圖示都是隱藏的，但可以由使用者升級至通知區域。</span><span class="sxs-lookup"><span data-stu-id="94af1-283">Most icons are hidden by default in Windows 7, but can be promoted to the notification area by the user.</span></span>
-   <span data-ttu-id="94af1-284">**不要顯示系統管理員對標準使用者的圖示。**</span><span class="sxs-lookup"><span data-stu-id="94af1-284">**Don't display icons meant for administrators to standard users.**</span></span> <span data-ttu-id="94af1-285">記錄 Windows 事件記錄檔中的資訊。</span><span class="sxs-lookup"><span data-stu-id="94af1-285">Record the information in the Windows event log.</span></span>

### <a name="where-to-show"></a><span data-ttu-id="94af1-286">顯示位置</span><span class="sxs-lookup"><span data-stu-id="94af1-286">Where to show</span></span>

-   <span data-ttu-id="94af1-287">**從通知區域附近的通知區域圖示顯示啟動的視窗。**</span><span class="sxs-lookup"><span data-stu-id="94af1-287">**Display windows launched from notification area icons near the notification area.**</span></span>

![<span data-ttu-id="94af1-288">靠近通知區域的視窗圖表</span><span class="sxs-lookup"><span data-stu-id="94af1-288">figure of a window near the notification area</span></span> ](images/winenv-notification-image14.png)

<span data-ttu-id="94af1-289">從通知區域圖示啟動的 Windows 會顯示在通知區域附近。</span><span class="sxs-lookup"><span data-stu-id="94af1-289">Windows launched from notification area icons are displayed near the notification area.</span></span>

### <a name="icons"></a><span data-ttu-id="94af1-290">圖示</span><span class="sxs-lookup"><span data-stu-id="94af1-290">Icons</span></span>

-   <span data-ttu-id="94af1-291">**根據其設計模式選擇圖示：**</span><span class="sxs-lookup"><span data-stu-id="94af1-291">**Choose the icon based on its design pattern:**</span></span>

    | <span data-ttu-id="94af1-292">模式</span><span class="sxs-lookup"><span data-stu-id="94af1-292">Pattern</span></span>                                                 | <span data-ttu-id="94af1-293">圖示類型</span><span class="sxs-lookup"><span data-stu-id="94af1-293">Icon type</span></span>                                   |
    |--------------------------------------------------|------------------------------------|
    | <span data-ttu-id="94af1-294">系統狀態和存取</span><span class="sxs-lookup"><span data-stu-id="94af1-294">System status and access</span></span><br/>              | <span data-ttu-id="94af1-295">系統功能圖示</span><span class="sxs-lookup"><span data-stu-id="94af1-295">System feature icon</span></span><br/>     |
    | <span data-ttu-id="94af1-296">背景工作狀態和存取權</span><span class="sxs-lookup"><span data-stu-id="94af1-296">Background task status and access</span></span><br/>     | <span data-ttu-id="94af1-297">程式或功能圖示</span><span class="sxs-lookup"><span data-stu-id="94af1-297">Program or feature icon</span></span><br/> |
    | <span data-ttu-id="94af1-298">暫時通知來源</span><span class="sxs-lookup"><span data-stu-id="94af1-298">Temporary notification source</span></span><br/>         | <span data-ttu-id="94af1-299">程式或功能圖示</span><span class="sxs-lookup"><span data-stu-id="94af1-299">Program or feature icon</span></span><br/> |
    | <span data-ttu-id="94af1-300">暫存事件狀態</span><span class="sxs-lookup"><span data-stu-id="94af1-300">Temporary event status</span></span><br/>                | <span data-ttu-id="94af1-301">程式或功能圖示</span><span class="sxs-lookup"><span data-stu-id="94af1-301">Program or feature icon</span></span><br/> |
    | <span data-ttu-id="94af1-302">最小化單一實例應用程式</span><span class="sxs-lookup"><span data-stu-id="94af1-302">Minimized single-instance application</span></span><br/> | <span data-ttu-id="94af1-303">程式圖示</span><span class="sxs-lookup"><span data-stu-id="94af1-303">Program icon</span></span><br/>            |

    

     

    ![<span data-ttu-id="94af1-304">通知區域和 outlook 圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-304">screen shot of notification area and outlook icons</span></span> ](images/winenv-notification-image15.png)

    <span data-ttu-id="94af1-305">在此範例中，Outlook 會使用電子郵件功能圖示作為暫時通知來源，並使用其應用程式圖示來提供最小化的應用程式。</span><span class="sxs-lookup"><span data-stu-id="94af1-305">In this example, Outlook uses an e-mail feature icon for a temporary notification source and its application icon for the minimized application.</span></span>

-   <span data-ttu-id="94af1-306">**選擇容易辨識的圖示設計。**</span><span class="sxs-lookup"><span data-stu-id="94af1-306">**Choose an easily recognizable icon design.**</span></span> <span data-ttu-id="94af1-307">偏好在正方形或矩形圖示上具有唯一輪廓的圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-307">Prefer icons with unique outlines over square or rectangular shaped icons.</span></span> <span data-ttu-id="94af1-308">讓設計簡單易用的符號超過實際影像。</span><span class="sxs-lookup"><span data-stu-id="94af1-308">Keep the designs simple prefer symbols over realistic images.</span></span> <span data-ttu-id="94af1-309">也套用其他 [Aero 樣式的圖示指導方針](vis-icons.md) 。</span><span class="sxs-lookup"><span data-stu-id="94af1-309">Apply the other [Aero-style icon guidelines](vis-icons.md) as well.</span></span>
-   <span data-ttu-id="94af1-310">**使用圖示變化或覆迭來指出狀態或狀態變更。**</span><span class="sxs-lookup"><span data-stu-id="94af1-310">**Use icon variations or overlays to indicate status or status changes.**</span></span> <span data-ttu-id="94af1-311">使用圖示變化顯示數量或強度的變更。</span><span class="sxs-lookup"><span data-stu-id="94af1-311">Use icon variations to show changes in quantities or strengths.</span></span> <span data-ttu-id="94af1-312">針對其他類型的狀態，請使用下列標準重迭。</span><span class="sxs-lookup"><span data-stu-id="94af1-312">For other types of status, use the following standard overlays.</span></span> <span data-ttu-id="94af1-313">只使用單一重迭，並在右下角找出一致性。</span><span class="sxs-lookup"><span data-stu-id="94af1-313">Use only a single overlay, and locate it bottom-right for consistency.</span></span> 

    | <span data-ttu-id="94af1-314">重疊</span><span class="sxs-lookup"><span data-stu-id="94af1-314">Overlay</span></span>                                                                                                       | <span data-ttu-id="94af1-315">狀態</span><span class="sxs-lookup"><span data-stu-id="94af1-315">Status</span></span>                                 |
    |--------------------------------------------------------------------------------------------------------|----------------------------------|
    | ![<span data-ttu-id="94af1-316">小型警告圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-316">screen shot of small warning icon</span></span> ](images/winenv-notification-image16.png)<br/>               | <span data-ttu-id="94af1-317">警告</span><span class="sxs-lookup"><span data-stu-id="94af1-317">Warning</span></span><br/>               |
    | ![<span data-ttu-id="94af1-318">小錯誤圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-318">screen shot of small error icon</span></span> ](images/winenv-notification-image17.png)<br/>                 | <span data-ttu-id="94af1-319">錯誤</span><span class="sxs-lookup"><span data-stu-id="94af1-319">Error</span></span><br/>                 |
    | ![<span data-ttu-id="94af1-320">小型停用/中斷連線圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-320">screen shot of small disabled/disconnected icon</span></span> ](images/winenv-notification-image18.png)<br/> | <span data-ttu-id="94af1-321">已停用/已中斷連線</span><span class="sxs-lookup"><span data-stu-id="94af1-321">Disabled/Disconnected</span></span><br/> |
    | ![<span data-ttu-id="94af1-322">小型封鎖/離線圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-322">screen shot of small blocked/offline icon</span></span> ](images/winenv-notification-image19.png)<br/>       | <span data-ttu-id="94af1-323">封鎖/離線</span><span class="sxs-lookup"><span data-stu-id="94af1-323">Blocked/Offline</span></span><br/>       |

    

     

    ![<span data-ttu-id="94af1-324">通知區域和兩個圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-324">screen shot of notification area and two icons</span></span> ](images/winenv-notification-image20.png)

    <span data-ttu-id="94af1-325">在此範例中，無線和電池圖示會顯示數量或強度的變化。</span><span class="sxs-lookup"><span data-stu-id="94af1-325">In this example, the wireless and battery icons show changes in quantities or strengths.</span></span>

    ![<span data-ttu-id="94af1-326">通知區域和兩個重迭的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-326">screen shot of notification area and two overlays</span></span> ](images/winenv-notification-image21.png)

    <span data-ttu-id="94af1-327">在此範例中，會使用覆迭來顯示錯誤和警告狀態。</span><span class="sxs-lookup"><span data-stu-id="94af1-327">In this example, overlays are used to show error and warning states.</span></span>

-   <span data-ttu-id="94af1-328">**避免在基底圖示中大量純紅色、黃色和綠色。**</span><span class="sxs-lookup"><span data-stu-id="94af1-328">**Avoid swaths of pure red, yellow, and green in your base icons.**</span></span> <span data-ttu-id="94af1-329">為了避免混淆，請保留這些色彩以傳達狀態。</span><span class="sxs-lookup"><span data-stu-id="94af1-329">To avoid confusion, reserve these colors to communicate status.</span></span> <span data-ttu-id="94af1-330">如果您的 [商標](exper-branding.md) 使用這些色彩，請考慮為您的基底通知區域圖示使用靜音。</span><span class="sxs-lookup"><span data-stu-id="94af1-330">If your [branding](exper-branding.md) uses these colors, consider using muted tones for your base notification area icons.</span></span>
-   <span data-ttu-id="94af1-331">針對 [漸進式擴大](mess-notif.md)， **當情況變得更緊急時，請使用具有逐漸 emphatic 外觀的圖示。**</span><span class="sxs-lookup"><span data-stu-id="94af1-331">For [progressive escalation](mess-notif.md), **use icons with a progressively more emphatic appearance as the situation becomes more urgent.**</span></span>

    ![<span data-ttu-id="94af1-332">通知區域和五個圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-332">screen shot of notification area and five icons</span></span> ](images/winenv-notification-image22.png)

    <span data-ttu-id="94af1-333">在這些範例中，當緊急增加時，電池圖示的外觀會變得更 emphatic。</span><span class="sxs-lookup"><span data-stu-id="94af1-333">In these examples, the appearance of the battery icon becomes more emphatic as the urgency increases.</span></span>

-   <span data-ttu-id="94af1-334">**請勿變更太頻繁的狀態。**</span><span class="sxs-lookup"><span data-stu-id="94af1-334">**Don't change status too frequently.**</span></span> <span data-ttu-id="94af1-335">通知區域圖示不應該出現雜訊、不穩定或需要注意。</span><span class="sxs-lookup"><span data-stu-id="94af1-335">Notification area icons shouldn't appear noisy, unstable, or demand attention.</span></span> <span data-ttu-id="94af1-336">眼睛對周邊周邊領域的變化很敏感，因此狀態變更必須很微妙。</span><span class="sxs-lookup"><span data-stu-id="94af1-336">The eye is sensitive to changes in the peripheral field of vision, so status changes need to be subtle.</span></span>
    -   <span data-ttu-id="94af1-337">**請勿快速變更圖示。**</span><span class="sxs-lookup"><span data-stu-id="94af1-337">**Don't change the icon rapidly.**</span></span> <span data-ttu-id="94af1-338">如果基礎狀態快速變更，請讓圖示反映高階狀態。</span><span class="sxs-lookup"><span data-stu-id="94af1-338">If underlying status is changing rapidly, have the icon reflect high-level status.</span></span>

        <span data-ttu-id="94af1-339">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="94af1-339">**Incorrect:**</span></span>

        ![<span data-ttu-id="94af1-340">通知區域和數據機圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-340">screen shot of notification area and modem icon</span></span> ](images/winenv-notification-image23.png)

        <span data-ttu-id="94af1-341">在此範例中，數據機圖示會顯示 (硬體數據機) 的閃爍燈，但這些狀態變更對使用者而言並不重要。</span><span class="sxs-lookup"><span data-stu-id="94af1-341">In this example, the modem icon displays blinking lights (as a hardware modem does), but those state changes aren't significant to users.</span></span>

    -   <span data-ttu-id="94af1-342">**請勿使用長時間執行的動畫來顯示連續的活動。**</span><span class="sxs-lookup"><span data-stu-id="94af1-342">**Don't use long-running animations to show continuous activities.**</span></span> <span data-ttu-id="94af1-343">這類動畫是個干擾。</span><span class="sxs-lookup"><span data-stu-id="94af1-343">Such animations are a distraction.</span></span> <span data-ttu-id="94af1-344">通知區域中的圖示存在，足以指出連續活動。</span><span class="sxs-lookup"><span data-stu-id="94af1-344">An icon's presence in the notification area sufficiently indicates continuous activity.</span></span>
    -   <span data-ttu-id="94af1-345">**簡單、微妙的動畫可在重要的暫存、可轉移狀態變更期間顯示進度。**</span><span class="sxs-lookup"><span data-stu-id="94af1-345">**Brief, subtle animations are acceptable to show progress during important temporary, transitive status changes.**</span></span>

        ![<span data-ttu-id="94af1-346">通知區域和無線圖示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-346">screen shot of notification area and wireless icon</span></span> ](images/winenv-notification-image24.png)

        <span data-ttu-id="94af1-347">在此範例中，無線圖示會顯示活動指示器，以顯示工作正在進行中。</span><span class="sxs-lookup"><span data-stu-id="94af1-347">In this example, the Wireless icon displays an activity indicator to show that work is in progress.</span></span>

    -   <span data-ttu-id="94af1-348">**請勿將圖示閃爍。**</span><span class="sxs-lookup"><span data-stu-id="94af1-348">**Don't flash the icon.**</span></span> <span data-ttu-id="94af1-349">這麼做會造成太雜亂的事情。</span><span class="sxs-lookup"><span data-stu-id="94af1-349">Doing so is too distracting.</span></span> <span data-ttu-id="94af1-350">如果事件需要立即注意，請改用對話方塊。</span><span class="sxs-lookup"><span data-stu-id="94af1-350">If an event requires immediate attention, use a dialog box instead.</span></span> <span data-ttu-id="94af1-351">如果事件另需要注意，請使用通知。</span><span class="sxs-lookup"><span data-stu-id="94af1-351">If the event otherwise needs attention, use a notification.</span></span>

-   <span data-ttu-id="94af1-352">**不要停用通知區域圖示。**</span><span class="sxs-lookup"><span data-stu-id="94af1-352">**Don't disable notification area icons.**</span></span> <span data-ttu-id="94af1-353">如果目前未套用圖示，請將它移除。</span><span class="sxs-lookup"><span data-stu-id="94af1-353">If the icon doesn't currently apply, remove it.</span></span> <span data-ttu-id="94af1-354">不過，如果使用者可以從圖示啟用，您可以顯示已停用狀態重迭的已啟用圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-354">However, you can show an enabled icon with a disabled status overlay if users can enable from the icon.</span></span>

    ![<span data-ttu-id="94af1-355">通知區域和音量滑杆的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-355">screen shot of notification area and volume slider</span></span> ](images/winenv-notification-image25.png)

    <span data-ttu-id="94af1-356">在此範例中，使用者可以啟用圖示的音效輸出。</span><span class="sxs-lookup"><span data-stu-id="94af1-356">In this example, users can enable sound output from the icon.</span></span>

<span data-ttu-id="94af1-357">如需一般圖示指導方針和範例，請參閱 [圖示](vis-icons.md)。</span><span class="sxs-lookup"><span data-stu-id="94af1-357">For general icon guidelines and examples, see [Icons](vis-icons.md).</span></span>

### <a name="interaction"></a><span data-ttu-id="94af1-358">互動</span><span class="sxs-lookup"><span data-stu-id="94af1-358">Interaction</span></span>

<span data-ttu-id="94af1-359">**注意：** 下列 click 事件應該會出現在滑鼠上，而不是滑鼠向下。</span><span class="sxs-lookup"><span data-stu-id="94af1-359">**Note:** The following click events should occur on mouse up, not mouse down.</span></span>

<span data-ttu-id="94af1-360">**暫留**</span><span class="sxs-lookup"><span data-stu-id="94af1-360">**Hover**</span></span>

-   <span data-ttu-id="94af1-361">**顯示指出圖示代表內容的工具提示或提示。**</span><span class="sxs-lookup"><span data-stu-id="94af1-361">**Display a tooltip or infotip that indicates what the icon represents.**</span></span>

    ![<span data-ttu-id="94af1-362">通知區域和工具提示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-362">screen shot of notification area and tooltip</span></span> ](images/winenv-notification-image26.png)

    <span data-ttu-id="94af1-363">在此範例中，會使用工具提示來描述停留時的圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-363">In this example, a tooltip is used to describe the icon on hover.</span></span>

<span data-ttu-id="94af1-364">如需提示文字的指導方針，請參閱本文的「 [文字](#context-menus) 」一節。</span><span class="sxs-lookup"><span data-stu-id="94af1-364">For infotip text guidelines, see the [Text](#context-menus) section of this article.</span></span>

<span data-ttu-id="94af1-365">**按一下滑鼠左鍵**</span><span class="sxs-lookup"><span data-stu-id="94af1-365">**Left single-click**</span></span>

-   <span data-ttu-id="94af1-366">**顯示最可能想要看到的任何使用者**，可能是：</span><span class="sxs-lookup"><span data-stu-id="94af1-366">**Display whatever users most likely want to see**, which may be:</span></span>

    -   <span data-ttu-id="94af1-367">具有最實用設定和一般執行工作的飛出視窗、對話方塊或程式視窗。</span><span class="sxs-lookup"><span data-stu-id="94af1-367">A flyout window, dialog box, or program window with the most useful settings and commonly performed tasks.</span></span> <span data-ttu-id="94af1-368">如需展示指導方針，請參閱 [通知區域 flyouts](#notification-area-flyouts)。</span><span class="sxs-lookup"><span data-stu-id="94af1-368">For presentation guidelines, see [Notification area flyouts](#notification-area-flyouts).</span></span>

        ![<span data-ttu-id="94af1-369">通知區域和 flyouts 的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-369">screen shot of notification area and flyouts</span></span> ](images/winenv-notification-image27.png)

        <span data-ttu-id="94af1-370">在這些範例中，按一下滑鼠左鍵會顯示具有最有用設定的快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="94af1-370">In these examples, left clicking displays popup windows with the most useful settings.</span></span>

    -   <span data-ttu-id="94af1-371">狀態飛出視窗。</span><span class="sxs-lookup"><span data-stu-id="94af1-371">A status flyout.</span></span>

        ![<span data-ttu-id="94af1-372">通知區域和狀態飛出視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-372">screen shot of notification area and status flyout</span></span> ](images/winenv-notification-image28.png)

        <span data-ttu-id="94af1-373">在此範例中，按一下滑鼠左鍵會顯示狀態飛出視窗。</span><span class="sxs-lookup"><span data-stu-id="94af1-373">In this example, left clicking displays the status flyout.</span></span>

        -   <span data-ttu-id="94af1-374">相關的控制台專案。</span><span class="sxs-lookup"><span data-stu-id="94af1-374">The related control panel item.</span></span>
        -   <span data-ttu-id="94af1-375">內容功能表。</span><span class="sxs-lookup"><span data-stu-id="94af1-375">The context menu.</span></span>

    <span data-ttu-id="94af1-376">使用者只需要按一下滑鼠，就能顯示某個東西，因此不會顯示任何內容，讓通知區域的圖示沒有回應。</span><span class="sxs-lookup"><span data-stu-id="94af1-376">Users expect left single-clicks to display something, so not displaying anything makes a notification area icon appear unresponsive.</span></span>

-   <span data-ttu-id="94af1-377">**只有當其他選項不適用時，才會顯示內容功能表**，並以粗體顯示預設命令。</span><span class="sxs-lookup"><span data-stu-id="94af1-377">**Display a context menu only if the other choices don't apply**, with the default command in bold.</span></span> <span data-ttu-id="94af1-378">在此情況下，會顯示在按一下滑鼠右鍵時所顯示的相同內容功能表，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="94af1-378">In this case, display the same context menu that is shown on right-click to avoid confusion.</span></span>
-   <span data-ttu-id="94af1-379">**偏好在對話方塊中使用快顯視窗** ，以提供更輕量的感覺。</span><span class="sxs-lookup"><span data-stu-id="94af1-379">**Prefer using a popup window over a dialog box** for a more lightweight feel.</span></span> <span data-ttu-id="94af1-380">只顯示最常見的設定，並讓它們立即生效，以提供更簡單的互動。</span><span class="sxs-lookup"><span data-stu-id="94af1-380">Show only the most common settings and have them take immediate effect for a simpler interaction.</span></span> <span data-ttu-id="94af1-381">如果使用者按一下視窗外的任何位置，請關閉快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="94af1-381">Dismiss the popup window if the user clicks anywhere outside the window.</span></span>
-   <span data-ttu-id="94af1-382">**在相關聯的圖示附近顯示小型視窗。**</span><span class="sxs-lookup"><span data-stu-id="94af1-382">**Display small windows near the associated icon.**</span></span> <span data-ttu-id="94af1-383">不過，大型視窗（例如控制台專案）可以顯示在預設監視器的中央。</span><span class="sxs-lookup"><span data-stu-id="94af1-383">However, large windows such as control panel items can be displayed in the center of the default monitor.</span></span>

<span data-ttu-id="94af1-384">**按兩下滑鼠左鍵**</span><span class="sxs-lookup"><span data-stu-id="94af1-384">**Left double-click**</span></span>

-   <span data-ttu-id="94af1-385">**在內容功能表上執行預設命令。**</span><span class="sxs-lookup"><span data-stu-id="94af1-385">**Perform the default command on the context menu.**</span></span> <span data-ttu-id="94af1-386">一般而言，這會顯示與圖示相關聯的主要 UI，例如相關聯的 [控制台] 專案、[屬性工作表] 或 [程式] 視窗。</span><span class="sxs-lookup"><span data-stu-id="94af1-386">Typically, this displays the primary UI associated with the icon, such as the associated control panel item, property sheet, or program window.</span></span>
-   <span data-ttu-id="94af1-387">**如果沒有預設的命令，請執行與左側單鍵的相同動作。**</span><span class="sxs-lookup"><span data-stu-id="94af1-387">**If there is no default command, perform the same action as a left single-click.**</span></span>

<span data-ttu-id="94af1-388">**以滑鼠右鍵按一下**</span><span class="sxs-lookup"><span data-stu-id="94af1-388">**Right-click**</span></span>

-   <span data-ttu-id="94af1-389">**顯示內容功能表**，並以粗體顯示預設命令。</span><span class="sxs-lookup"><span data-stu-id="94af1-389">**Display the context menu**, with the default command in bold.</span></span>

### <a name="context-menus"></a><span data-ttu-id="94af1-390">操作功能表</span><span class="sxs-lookup"><span data-stu-id="94af1-390">Context menus</span></span>

-   <span data-ttu-id="94af1-391">**將內容功能表顯示在其相關聯的圖示旁邊**，但遠離工作列。</span><span class="sxs-lookup"><span data-stu-id="94af1-391">**Display the context menu near its associated icon**, but away from the taskbar.</span></span>
-   <span data-ttu-id="94af1-392">**內容功能表可能會** 依列出的順序，在適當的順序中包含下列專案 (確切的文字是以引號括住) ：</span><span class="sxs-lookup"><span data-stu-id="94af1-392">**The context menu may include the following items**, as appropriate, in the listed order (exact text is in quotes):</span></span>

<span data-ttu-id="94af1-393">主要命令</span><span class="sxs-lookup"><span data-stu-id="94af1-393">Primary commands</span></span>

<span data-ttu-id="94af1-394">開啟 (預設，先列出，以粗體顯示) </span><span class="sxs-lookup"><span data-stu-id="94af1-394">Open (default, list first, in bold)</span></span>

<span data-ttu-id="94af1-395">執行</span><span class="sxs-lookup"><span data-stu-id="94af1-395">Run</span></span>

<span data-ttu-id="94af1-396">次要命令</span><span class="sxs-lookup"><span data-stu-id="94af1-396">Secondary commands</span></span>

<span data-ttu-id="94af1-397">< 分隔符號></span><span class="sxs-lookup"><span data-stu-id="94af1-397">< separator></span></span>

<span data-ttu-id="94af1-398">暫停/繼續啟用/停用命令 (核取記號) </span><span class="sxs-lookup"><span data-stu-id="94af1-398">Suspend/resume enable/disable command (check mark)</span></span>

<span data-ttu-id="94af1-399">「最小化至通知區域」 (核取記號) </span><span class="sxs-lookup"><span data-stu-id="94af1-399">"Minimized to notification area" (check mark)</span></span>

<span data-ttu-id="94af1-400">加入宣告通知 (核取記號) </span><span class="sxs-lookup"><span data-stu-id="94af1-400">Opt in to notifications (check mark)</span></span>

<span data-ttu-id="94af1-401">「通知區域中顯示圖示」 (核取記號) </span><span class="sxs-lookup"><span data-stu-id="94af1-401">"Display icon in notification area" (check mark)</span></span>

<span data-ttu-id="94af1-402">< 分隔符號></span><span class="sxs-lookup"><span data-stu-id="94af1-402">< separator></span></span>

<span data-ttu-id="94af1-403">設置</span><span class="sxs-lookup"><span data-stu-id="94af1-403">"Options"</span></span>

<span data-ttu-id="94af1-404">"Exit"</span><span class="sxs-lookup"><span data-stu-id="94af1-404">"Exit"</span></span>

-   <span data-ttu-id="94af1-405">**移除，而不是停用任何未套用的內容功能表項目。**</span><span class="sxs-lookup"><span data-stu-id="94af1-405">**Remove rather than disable any context menu items that don't apply.**</span></span>
-   <span data-ttu-id="94af1-406">針對開啟、執行和暫停/繼續命令，請 **特別說明開啟、執行、暫停和繼續的內容。**</span><span class="sxs-lookup"><span data-stu-id="94af1-406">For Open, Run, and Suspend/Resume commands, **be specific about what is being opened, run, suspended, and resumed.**</span></span>

![顯示通知區域和命令的螢幕擷取畫面。](images/winenv-notification-image29.png)

<span data-ttu-id="94af1-408">在此範例中，Windows Defender 有特定的 Open 和 Run 命令。</span><span class="sxs-lookup"><span data-stu-id="94af1-408">In this example, Windows Defender has specific Open and Run commands.</span></span>

-   <span data-ttu-id="94af1-409">**使用暫停/繼續執行背景工作，啟用/停用其他所有專案。**</span><span class="sxs-lookup"><span data-stu-id="94af1-409">**Use Suspend/Resume running background tasks, Enable/Disable for everything else.**</span></span>
-   <span data-ttu-id="94af1-410">**使用核取記號來表示狀態。**</span><span class="sxs-lookup"><span data-stu-id="94af1-410">**Use check marks to indicate state.**</span></span> <span data-ttu-id="94af1-411">列出並啟用所有狀態，並將核取記號放置在目前狀態的旁邊。</span><span class="sxs-lookup"><span data-stu-id="94af1-411">List and enable all states and place the check mark next to the current state.</span></span> <span data-ttu-id="94af1-412">請勿停用選項或變更選項標籤來指出目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="94af1-412">Don't disable options or change option labels to indicate the current state.</span></span>

<span data-ttu-id="94af1-413">**正確：**</span><span class="sxs-lookup"><span data-stu-id="94af1-413">**Correct:**</span></span>

![<span data-ttu-id="94af1-414">具有核取記號的命令螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-414">screen shot of a command with check mark</span></span> ](images/winenv-notification-image29.png)

<span data-ttu-id="94af1-415">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="94af1-415">**Incorrect:**</span></span>

![<span data-ttu-id="94af1-416">沒有核取記號的命令螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-416">screen shot of a command without check mark</span></span> ](images/winenv-notification-image30.png)

<span data-ttu-id="94af1-417">在不正確的範例中，Windows Defender 應該使用核取記號來表示目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="94af1-417">In the incorrect example, Windows Defender should use a check mark to indicate the current state.</span></span>

-   <span data-ttu-id="94af1-418">**所有背景工作都必須有暫停/繼續命令。**</span><span class="sxs-lookup"><span data-stu-id="94af1-418">**All background tasks must have a Suspend/Resume command.**</span></span> <span data-ttu-id="94af1-419">選擇命令應該會暫時暫停工作。</span><span class="sxs-lookup"><span data-stu-id="94af1-419">Choosing the command should temporarily suspend the task.</span></span> <span data-ttu-id="94af1-420">使用者可能會想要暫時暫停背景工作，以提高系統效能或減少耗電量。</span><span class="sxs-lookup"><span data-stu-id="94af1-420">Users may want to temporarily suspend background tasks to increase system performance or reduce power consumption.</span></span> <span data-ttu-id="94af1-421">當使用者繼續或重新開機 Windows 時，會重新開機已暫停的背景工作。</span><span class="sxs-lookup"><span data-stu-id="94af1-421">Suspended background tasks are restarted when resumed by the user or when Windows is restarted.</span></span>
-   <span data-ttu-id="94af1-422">如果您的程式有某些使用者可能不想看到的通知，**可讓使用者加入宣告或退出不同的通知類型**。</span><span class="sxs-lookup"><span data-stu-id="94af1-422">**Allow users to opt into or out of different notification types** if your program has notifications that some users might not want to see.</span></span> <span data-ttu-id="94af1-423">[僅供參考](mess-notif.md)通知模式會要求使用者加入宣告，因此這些通知必須預設為停用。</span><span class="sxs-lookup"><span data-stu-id="94af1-423">The [FYI](mess-notif.md) notification pattern requires users to opt in, so these notifications must be disabled by default.</span></span>

![<span data-ttu-id="94af1-424">通知區域和命令的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-424">screen shot of notification area and commands</span></span> ](images/winenv-notification-image31.png)

<span data-ttu-id="94af1-425">在此範例中，Outlook 可讓使用者從圖示選擇收到的通知。</span><span class="sxs-lookup"><span data-stu-id="94af1-425">In this example, Outlook allows users to choose the notifications they receive from the icon.</span></span>

-   <span data-ttu-id="94af1-426">**清除 [在通知區域中顯示圖示] 選項會從通知區域移除圖示**，但不會影響基礎程式、功能或流程。</span><span class="sxs-lookup"><span data-stu-id="94af1-426">**Clearing the "Display icon in notification area" option removes the icon from the notification area**, but doesn't affect the underlying program, feature, or process.</span></span> <span data-ttu-id="94af1-427">使用者可以從程式的 [選項] 對話方塊中重新顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-427">Users can redisplay the icon from the program's Options dialog box.</span></span> <span data-ttu-id="94af1-428">重新開機 Windows 時，請勿自動重新顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-428">Don't automatically re-display the icon when Windows is restarted.</span></span>
-   <span data-ttu-id="94af1-429">**Exit 命令會結束目前 Windows 會話的程式，並移除圖示。**</span><span class="sxs-lookup"><span data-stu-id="94af1-429">**The Exit command quits the program for the current Windows session and removes the icon.**</span></span> <span data-ttu-id="94af1-430">如果無法關閉程式，則沒有結束命令。</span><span class="sxs-lookup"><span data-stu-id="94af1-430">Don't have an Exit command if program can't be shut down.</span></span> <span data-ttu-id="94af1-431">重新開機 Windows 時，會重新開機程式。</span><span class="sxs-lookup"><span data-stu-id="94af1-431">The program is restarted when Windows is restarted.</span></span> <span data-ttu-id="94af1-432">使用者可以從 [選項] 對話方塊中永久結束程式。</span><span class="sxs-lookup"><span data-stu-id="94af1-432">Users can permanently quit the program from the Options dialog box.</span></span>
-   <span data-ttu-id="94af1-433">**沒有 About 命令。**</span><span class="sxs-lookup"><span data-stu-id="94af1-433">**Don't have an About command.**</span></span> <span data-ttu-id="94af1-434">這類資訊應該透過圖示、其資訊提示和操作功能表來傳達。</span><span class="sxs-lookup"><span data-stu-id="94af1-434">Such information should be communicated by the icon, its infotip, and the context menu.</span></span> <span data-ttu-id="94af1-435">如果使用者想要詳細資訊，他們可以看到主要的 UI。</span><span class="sxs-lookup"><span data-stu-id="94af1-435">If users want more information, they can view the primary UI.</span></span>
    -   <span data-ttu-id="94af1-436">**例外狀況：** 如果沒有桌上型電腦的程式圖示，您可以提供 [關於] 命令。</span><span class="sxs-lookup"><span data-stu-id="94af1-436">**Exception:** You may provide an About command if the icon is for a program that doesn't have desktop presence.</span></span>

<span data-ttu-id="94af1-437">如需一般內容功能表的指導方針和範例，請參閱 [功能表](cmd-menus.md)。</span><span class="sxs-lookup"><span data-stu-id="94af1-437">For general context menu guidelines and examples, see [Menus](cmd-menus.md).</span></span>

### <a name="rich-tooltips"></a><span data-ttu-id="94af1-438">豐富的工具提示</span><span class="sxs-lookup"><span data-stu-id="94af1-438">Rich tooltips</span></span>

-   <span data-ttu-id="94af1-439">**請只使用豐富的工具提示，讓資訊更容易瞭解。**</span><span class="sxs-lookup"><span data-stu-id="94af1-439">**Use rich tooltips only to make the information easier to understand.**</span></span> <span data-ttu-id="94af1-440">請不要使用豐富的工具提示來裝飾功能。</span><span class="sxs-lookup"><span data-stu-id="94af1-440">Don't use rich tooltips just to decorate the feature.</span></span> <span data-ttu-id="94af1-441">如果您無法使用豐富的資訊來理解資訊，請改為使用一般工具提示。</span><span class="sxs-lookup"><span data-stu-id="94af1-441">If you can't use richness to make the information easier to understand, use a plain tooltip instead.</span></span>

    <span data-ttu-id="94af1-442">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="94af1-442">**Incorrect:**</span></span>

    ![<span data-ttu-id="94af1-443">通知區域和豐富工具提示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-443">screen shot of notification area and rich tooltip</span></span> ](images/winenv-notification-image32.png)

    <span data-ttu-id="94af1-444">**正確：**</span><span class="sxs-lookup"><span data-stu-id="94af1-444">**Correct:**</span></span>

    ![<span data-ttu-id="94af1-445">通知區域和一般工具提示的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-445">screen shot of notification area and plain tooltip</span></span> ](images/winenv-notification-image33.png)

    <span data-ttu-id="94af1-446">在不正確的範例中，行事曆圖示不會讓日期變得更容易瞭解。</span><span class="sxs-lookup"><span data-stu-id="94af1-446">In the incorrect example, the calendar icon doesn't make the date easier to understand.</span></span>

-   <span data-ttu-id="94af1-447">**使用簡潔的簡報。**</span><span class="sxs-lookup"><span data-stu-id="94af1-447">**Use a concise presentation.**</span></span> <span data-ttu-id="94af1-448">使用簡潔的文字，以及具有32x32 圖元圖示的精確版面配置。</span><span class="sxs-lookup"><span data-stu-id="94af1-448">Use concise text and a concise layout with a 32x32 pixel icon.</span></span> <span data-ttu-id="94af1-449">Spacious 工具提示的風險會受到干擾，尤其是不慎顯示時。</span><span class="sxs-lookup"><span data-stu-id="94af1-449">Spacious tooltips risk being distracting, especially when displayed unintentionally.</span></span>
-   <span data-ttu-id="94af1-450">**請勿將在豐富的工具提示中顯示為互動式的控制項或元素放在一起。**</span><span class="sxs-lookup"><span data-stu-id="94af1-450">**Don't put controls or elements that appear interactive in a rich tooltip.**</span></span> <span data-ttu-id="94af1-451">工具提示不是互動式的，因此不應該顯示為互動式。</span><span class="sxs-lookup"><span data-stu-id="94af1-451">Tooltips aren't interactive and therefore shouldn't appear interactive.</span></span> <span data-ttu-id="94af1-452">請勿使用藍色或加底線的文字。</span><span class="sxs-lookup"><span data-stu-id="94af1-452">Don't use blue or underlined text.</span></span>

    <span data-ttu-id="94af1-453">**正確：**</span><span class="sxs-lookup"><span data-stu-id="94af1-453">**Correct:**</span></span>

    ![<span data-ttu-id="94af1-454">具有黑色文字的豐富工具提示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-454">screen shot of rich tooltip with black text</span></span> ](images/winenv-notification-image34.png)

    <span data-ttu-id="94af1-455">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="94af1-455">**Incorrect:**</span></span>

    ![<span data-ttu-id="94af1-456">具有藍色文字的豐富工具提示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-456">screen shot of rich tooltip with blue text</span></span> ](images/winenv-notification-image35.png)

    <span data-ttu-id="94af1-457">在不正確的範例中，目前的電源計劃會顯示為連結，但無法按一下。</span><span class="sxs-lookup"><span data-stu-id="94af1-457">In the incorrect example, the current power plan appears to be a link, but it is impossible to click.</span></span>

### <a name="notification-area-flyouts"></a><span data-ttu-id="94af1-458">通知區域 flyouts</span><span class="sxs-lookup"><span data-stu-id="94af1-458">Notification area flyouts</span></span>

-   <span data-ttu-id="94af1-459">適當時，會顯示具有三個區段的通知區域 flyouts：</span><span class="sxs-lookup"><span data-stu-id="94af1-459">When appropriate, present notification area flyouts with three sections:</span></span>
    -   <span data-ttu-id="94af1-460">**總結。**</span><span class="sxs-lookup"><span data-stu-id="94af1-460">**Summary.**</span></span> <span data-ttu-id="94af1-461">顯示出現在圖示工具提示或資訊提示中的相同資訊，可能會有更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="94af1-461">Display the same information that is displayed in the icon's tooltip or infotip, possibly with more detail.</span></span> <span data-ttu-id="94af1-462">為求一致，請使用相同的文字和圖示，且通常相同的版面配置 (如果使用豐富的工具提示) 。</span><span class="sxs-lookup"><span data-stu-id="94af1-462">For consistency, use the same text and icons, and generally the same layout (if using a rich tooltip).</span></span> <span data-ttu-id="94af1-463">不同于提示，這項資訊可在使用觸控時存取。</span><span class="sxs-lookup"><span data-stu-id="94af1-463">Unlike the infotips, this information is accessible when using touch.</span></span>
    -   <span data-ttu-id="94af1-464">**一般工作。**</span><span class="sxs-lookup"><span data-stu-id="94af1-464">**Common tasks.**</span></span> <span data-ttu-id="94af1-465">直接在飛出視窗中顯示最常執行的工作。</span><span class="sxs-lookup"><span data-stu-id="94af1-465">Present the most commonly performed tasks directly in the flyout.</span></span>
    -   <span data-ttu-id="94af1-466">**相關連結。**</span><span class="sxs-lookup"><span data-stu-id="94af1-466">**Related links.**</span></span> <span data-ttu-id="94af1-467">請提供下列其中一種選擇性連結：</span><span class="sxs-lookup"><span data-stu-id="94af1-467">Provide at most one of each type of the following optional links:</span></span>
        -   <span data-ttu-id="94af1-468">主控台中最常執行之工作的連結。</span><span class="sxs-lookup"><span data-stu-id="94af1-468">A link to the most frequently performed task in Control Panel.</span></span> <span data-ttu-id="94af1-469">提供 [一般工作] 區段中是否有經常執行的工作無法顯示。</span><span class="sxs-lookup"><span data-stu-id="94af1-469">Provide if there is a frequently performed task that can't be presented in the common tasks section.</span></span>
        -   <span data-ttu-id="94af1-470">相關主控台專案的連結。</span><span class="sxs-lookup"><span data-stu-id="94af1-470">A link to the related Control Panel item.</span></span> <span data-ttu-id="94af1-471">此主控台專案應允許使用者執行無法在 [一般工作] 區段中執行的任何工作。</span><span class="sxs-lookup"><span data-stu-id="94af1-471">This Control Panel item should allow users to perform any tasks that can't be performed in the common tasks section.</span></span>
        -   <span data-ttu-id="94af1-472">特定相關說明主題的連結。</span><span class="sxs-lookup"><span data-stu-id="94af1-472">A link to a specific, relevant Help topic.</span></span> <span data-ttu-id="94af1-473">遵循標準說明 [連結的指導方針](winenv-help.md)。</span><span class="sxs-lookup"><span data-stu-id="94af1-473">Follow the standard [Help link guidelines](winenv-help.md).</span></span>

![<span data-ttu-id="94af1-474">通知區域和飛出視窗的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-474">screen shot of notification area and flyout</span></span> ](images/winenv-notification-image36.png)

<span data-ttu-id="94af1-475">此範例顯示使用建議簡報的通知區域飛出視窗。</span><span class="sxs-lookup"><span data-stu-id="94af1-475">This example shows a notification area flyout using the recommended presentation.</span></span>

### <a name="options-dialog-box"></a><span data-ttu-id="94af1-476">選項對話方塊</span><span class="sxs-lookup"><span data-stu-id="94af1-476">Options dialog box</span></span>

-   <span data-ttu-id="94af1-477">無法直接從內容功能表存取的選項，必須位於 [選項] 對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="94af1-477">Options not accessible directly from the context menu must be in the Options dialog box.</span></span> <span data-ttu-id="94af1-478">此對話方塊可能是功能的 [控制台]。</span><span class="sxs-lookup"><span data-stu-id="94af1-478">This dialog could be the feature's control panel.</span></span>
-   <span data-ttu-id="94af1-479">**[選項] 對話方塊可能會在適當的情況下包含下列專案** (確切的文字是以引號括住) ：</span><span class="sxs-lookup"><span data-stu-id="94af1-479">**The Options dialog box may include the following items** as appropriate (exact text is in quotes):</span></span>
    -   <span data-ttu-id="94af1-480">啟用 \[ 功能名稱 \] (核取方塊) </span><span class="sxs-lookup"><span data-stu-id="94af1-480">Enable \[feature name\] (check box)</span></span>
        -   <span data-ttu-id="94af1-481">清除此選項會永久結束程式。</span><span class="sxs-lookup"><span data-stu-id="94af1-481">Clearing this option permanently quits the program.</span></span> <span data-ttu-id="94af1-482">程式可以從其控制台專案重新開機。</span><span class="sxs-lookup"><span data-stu-id="94af1-482">Program can be restarted from its control panel item.</span></span> <span data-ttu-id="94af1-483">內容功能表中的 [結束] 命令只會針對目前的 Windows 會話結束程式。</span><span class="sxs-lookup"><span data-stu-id="94af1-483">The Exit command in the context menu quits the program only for the current Windows session.</span></span>
    -   <span data-ttu-id="94af1-484">「通知區域中顯示圖示」 (核取方塊) </span><span class="sxs-lookup"><span data-stu-id="94af1-484">"Display icon in notification area" (check box)</span></span>
        -   <span data-ttu-id="94af1-485">從通知區域移除圖示，並不會影響基礎功能。</span><span class="sxs-lookup"><span data-stu-id="94af1-485">Removing the icon from the notification area doesn't affect the underlying feature.</span></span>
        -   <span data-ttu-id="94af1-486">選取此選項可讓使用者還原圖示，當然無法從圖示本身完成。</span><span class="sxs-lookup"><span data-stu-id="94af1-486">Selecting this option allows user to restore the icon, which of course can't be done from the icon itself.</span></span>
-   <span data-ttu-id="94af1-487">停用很少使用或可能令人討厭或混亂的功能。</span><span class="sxs-lookup"><span data-stu-id="94af1-487">Disable features that are rarely used, or potentially annoying or distracting.</span></span> <span data-ttu-id="94af1-488">讓使用者 [加入宣告](glossary.md) 這類功能。</span><span class="sxs-lookup"><span data-stu-id="94af1-488">Let users [opt in](glossary.md) to such features.</span></span>

<span data-ttu-id="94af1-489">如需一般選項對話方塊的指導方針和範例，請參閱 [屬性視窗](win-property-win.md)。</span><span class="sxs-lookup"><span data-stu-id="94af1-489">For general Options dialog box guidelines and examples, see [Property Windows](win-property-win.md).</span></span>

### <a name="minimizing-programs-to-the-notification-area"></a><span data-ttu-id="94af1-490">將程式降至最低通知區域</span><span class="sxs-lookup"><span data-stu-id="94af1-490">Minimizing programs to the notification area</span></span>

<span data-ttu-id="94af1-491">**注意： Windows 7 不再建議將程式視窗最小化至通知區域。**</span><span class="sxs-lookup"><span data-stu-id="94af1-491">**Note: Minimizing program windows to the notification area is no longer recommended for Windows 7.**</span></span> <span data-ttu-id="94af1-492">請改用一般 [工作列](winenv-taskbar.md) 按鈕。</span><span class="sxs-lookup"><span data-stu-id="94af1-492">Use regular [taskbar](winenv-taskbar.md) buttons instead.</span></span> <span data-ttu-id="94af1-493">您的程式可能會支援這兩種機制來提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="94af1-493">Your program may support both mechanisms for backward compatibility.</span></span>

-   <span data-ttu-id="94af1-494">若要減少工作列雜亂，請考慮提供將程式最小化到通知區域的功能，只適用于下列所有專案：</span><span class="sxs-lookup"><span data-stu-id="94af1-494">To reduce taskbar clutter, consider providing the ability to minimize programs to the notification area only if all of the following apply:</span></span>
    -   <span data-ttu-id="94af1-495">程式只能有一個單一實例。</span><span class="sxs-lookup"><span data-stu-id="94af1-495">The program can have only a single instance.</span></span>
    -   <span data-ttu-id="94af1-496">此程式會執行一段很長的時間。</span><span class="sxs-lookup"><span data-stu-id="94af1-496">The program is run for an extended period of time.</span></span>
    -   <span data-ttu-id="94af1-497">圖示會顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="94af1-497">The icon shows status.</span></span>
    -   <span data-ttu-id="94af1-498">圖示可以是通知來源。</span><span class="sxs-lookup"><span data-stu-id="94af1-498">The icon can be a notification source.</span></span>
    -   <span data-ttu-id="94af1-499">這麼做是選擇性的，使用者必須 [加入宣告](glossary.md)。</span><span class="sxs-lookup"><span data-stu-id="94af1-499">Doing so is optional and users must [opt in](glossary.md).</span></span>
-   <span data-ttu-id="94af1-500">使用應用程式標題列上的 [最小化] 按鈕，而不是 [關閉] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="94af1-500">Use the Minimize button on the application's title bar, not the Close button.</span></span>

## <a name="text"></a><span data-ttu-id="94af1-501">Text</span><span class="sxs-lookup"><span data-stu-id="94af1-501">Text</span></span>

### <a name="infotips"></a><span data-ttu-id="94af1-502">提示</span><span class="sxs-lookup"><span data-stu-id="94af1-502">Infotips</span></span>

-   <span data-ttu-id="94af1-503">圖示提示應該具有下列其中一種格式 (其中公司名稱是選擇性的) ：</span><span class="sxs-lookup"><span data-stu-id="94af1-503">The icon infotip should have one of the following formats (where the company name is optional):</span></span>
    -   <span data-ttu-id="94af1-504"> (的公司名稱) 功能、程式或裝置名稱</span><span class="sxs-lookup"><span data-stu-id="94af1-504">(Company name) Feature, program, or device name</span></span>
    -   ![<span data-ttu-id="94af1-505">具有公司名稱的提示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-505">screen shot of infotip with company name</span></span> ](images/winenv-notification-image37.png)
    -   <span data-ttu-id="94af1-506"> (的公司名稱) 功能、程式或裝置名稱-狀態摘要</span><span class="sxs-lookup"><span data-stu-id="94af1-506">(Company name) Feature, program, or device name - Status summary</span></span>
    -   ![<span data-ttu-id="94af1-507">顯示狀態摘要的提示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-507">screen shot of infotip displaying status summary</span></span> ](images/winenv-notification-image38.png)
    -   <span data-ttu-id="94af1-508"> (的公司名稱) 功能、程式或裝置名稱的狀態語句。</span><span class="sxs-lookup"><span data-stu-id="94af1-508">(Company name) Feature, program, or device name status statement.</span></span>
    -   ![<span data-ttu-id="94af1-509">顯示狀態語句的顯示提示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-509">screen shot of infotip displaying status statement</span></span> ](images/winenv-notification-image39.png)
    -   <span data-ttu-id="94af1-510"> (的公司名稱) 功能、程式或裝置名稱</span><span class="sxs-lookup"><span data-stu-id="94af1-510">(Company name) Feature, program, or device name</span></span>
    -   <span data-ttu-id="94af1-511">不同行上每個專案的狀態清單</span><span class="sxs-lookup"><span data-stu-id="94af1-511">Status list with each item on a separate line</span></span>
    -   ![<span data-ttu-id="94af1-512">顯示狀態清單的顯示提示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-512">screen shot of infotip displaying status list</span></span> ](images/winenv-notification-image40.png)

<span data-ttu-id="94af1-513">提示表達：</span><span class="sxs-lookup"><span data-stu-id="94af1-513">Infotip phrasing:</span></span>

-   <span data-ttu-id="94af1-514">將焦點放在最有用的資訊。</span><span class="sxs-lookup"><span data-stu-id="94af1-514">Focus on the most useful information.</span></span> <span data-ttu-id="94af1-515">在左側按一下滑鼠右鍵時顯示其他資訊。</span><span class="sxs-lookup"><span data-stu-id="94af1-515">Display other information on left single-click.</span></span>
-   <span data-ttu-id="94af1-516">很簡潔。</span><span class="sxs-lookup"><span data-stu-id="94af1-516">Be concise.</span></span> <span data-ttu-id="94af1-517">使用句子片段或簡單語句。</span><span class="sxs-lookup"><span data-stu-id="94af1-517">Use sentence fragments or simple statements.</span></span>
-   <span data-ttu-id="94af1-518">除非提示片語為完整句子，否則請勿使用結尾標點符號。</span><span class="sxs-lookup"><span data-stu-id="94af1-518">Don't use ending punctuation unless tip is phrased as a complete sentence.</span></span>
-   <span data-ttu-id="94af1-519">省略不必要的字組。</span><span class="sxs-lookup"><span data-stu-id="94af1-519">Omit unnecessary words.</span></span> <span data-ttu-id="94af1-520">請勿包含軟體版本或其他無關的資訊。</span><span class="sxs-lookup"><span data-stu-id="94af1-520">Don't include the software version or other extraneous information.</span></span>

    <span data-ttu-id="94af1-521">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="94af1-521">**Incorrect:**</span></span>

    ![<span data-ttu-id="94af1-522">具有不必要資訊的資訊提示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-522">screen shot of infotip with unnecessary information</span></span> ](images/winenv-notification-image41.png)

    <span data-ttu-id="94af1-523">在此範例中，資訊提示有無關的資訊。</span><span class="sxs-lookup"><span data-stu-id="94af1-523">In this example, the infotip has extraneous information.</span></span>

-   <span data-ttu-id="94af1-524">請勿解釋如何與圖示互動。</span><span class="sxs-lookup"><span data-stu-id="94af1-524">Don't explain how to interact with the icon.</span></span>

    <span data-ttu-id="94af1-525">**不正確：**</span><span class="sxs-lookup"><span data-stu-id="94af1-525">**Incorrect:**</span></span>

    ![<span data-ttu-id="94af1-526">以滑鼠右鍵按一下指示的顯示提示螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="94af1-526">screen shot of infotip with right-click instructions</span></span> ](images/winenv-notification-image42.png)

    <span data-ttu-id="94af1-527">在此範例中，[無線網路連線] 圖示提供按滑鼠右鍵的指示。</span><span class="sxs-lookup"><span data-stu-id="94af1-527">In this example, the Wireless Network Connection icon gives right-click instructions.</span></span>

## <a name="documentation"></a><span data-ttu-id="94af1-528">文件</span><span class="sxs-lookup"><span data-stu-id="94af1-528">Documentation</span></span>

<span data-ttu-id="94af1-529">參考通知區域時：</span><span class="sxs-lookup"><span data-stu-id="94af1-529">When referring to the notification area:</span></span>

-   <span data-ttu-id="94af1-530">請將通知區域稱為通知區域，而不是系統匣。</span><span class="sxs-lookup"><span data-stu-id="94af1-530">Refer to the notification area as the notification area, not the system tray.</span></span>

<span data-ttu-id="94af1-531">參考通知區域圖示時：</span><span class="sxs-lookup"><span data-stu-id="94af1-531">When referring to a notification area icon:</span></span>

-   <span data-ttu-id="94af1-532">請使用其提示中提供的確切名稱來參考圖示，包括其大小寫，後面接著圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-532">Refer to the icon using the exact name given in its infotip, including its capitalization, followed by icon.</span></span>
-   <span data-ttu-id="94af1-533">第一個參考也請參閱通知區域。</span><span class="sxs-lookup"><span data-stu-id="94af1-533">For the first reference, also refer to the notification area.</span></span>
-   <span data-ttu-id="94af1-534">可能的話，請使用粗體格式化標題文字。</span><span class="sxs-lookup"><span data-stu-id="94af1-534">When possible, format the heading text using bold.</span></span> <span data-ttu-id="94af1-535">否則，請只在必要時才將標題放在引號中，以避免混淆。</span><span class="sxs-lookup"><span data-stu-id="94af1-535">Otherwise, put the heading in quotation marks only if required to prevent confusion.</span></span>

<span data-ttu-id="94af1-536">**範例：** 若要快速檢查網路狀態，請按一下通知區域中的 **網路** 圖示。</span><span class="sxs-lookup"><span data-stu-id="94af1-536">**Example:** To check the network status quickly, click the **Network** icon in the notification area.</span></span>

 

