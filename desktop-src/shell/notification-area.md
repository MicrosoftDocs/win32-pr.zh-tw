---
description: 通知區域是工作列的一部分，可提供通知和狀態的暫時來源。
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: 通知和通知區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318632"
---
# <a name="notifications-and-the-notification-area"></a><span data-ttu-id="d8731-103">通知和通知區域</span><span class="sxs-lookup"><span data-stu-id="d8731-103">Notifications and the Notification Area</span></span>

<span data-ttu-id="d8731-104">通知區域是工作列的一部分，可提供通知和狀態的暫時來源。</span><span class="sxs-lookup"><span data-stu-id="d8731-104">The notification area is a portion of the taskbar that provides a temporary source for notifications and status.</span></span> <span data-ttu-id="d8731-105">它也可以用來顯示桌上型電腦上沒有存在的系統和程式功能圖示，例如電池計量、音量控制和網路狀態。</span><span class="sxs-lookup"><span data-stu-id="d8731-105">It can also be used to display icons for system and program features that have no presence on the desktop, such as battery level, volume control, and network status.</span></span> <span data-ttu-id="d8731-106">過去已經知道通知區域是系統匣或狀態欄。</span><span class="sxs-lookup"><span data-stu-id="d8731-106">The notification area has been known historically as the system tray or status area.</span></span>

<span data-ttu-id="d8731-107">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="d8731-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="d8731-108">通知和通知區域指導方針</span><span class="sxs-lookup"><span data-stu-id="d8731-108">Notification and Notification Area Guidelines</span></span>](#notification-and-notification-area-guidelines)
-   [<span data-ttu-id="d8731-109">建立與顯示通知</span><span class="sxs-lookup"><span data-stu-id="d8731-109">Creating and Displaying a Notification</span></span>](#notifications-and-the-notification-area)
    -   [<span data-ttu-id="d8731-110">新增通知圖示</span><span class="sxs-lookup"><span data-stu-id="d8731-110">Add a Notification Icon</span></span>](#add-a-notification-icon)
    -   [<span data-ttu-id="d8731-111">定義 NOTIFYICONDATA 版本</span><span class="sxs-lookup"><span data-stu-id="d8731-111">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
    -   [<span data-ttu-id="d8731-112">定義通知的外觀和內容</span><span class="sxs-lookup"><span data-stu-id="d8731-112">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
    -   [<span data-ttu-id="d8731-113">檢查使用者狀態</span><span class="sxs-lookup"><span data-stu-id="d8731-113">Check the User Status</span></span>](#check-the-user-status)
    -   [<span data-ttu-id="d8731-114">顯示通知</span><span class="sxs-lookup"><span data-stu-id="d8731-114">Display the Notification</span></span>](#display-the-notification)
    -   [<span data-ttu-id="d8731-115">移除圖示</span><span class="sxs-lookup"><span data-stu-id="d8731-115">Removing an Icon</span></span>](#removing-an-icon)
-   [<span data-ttu-id="d8731-116">SDK 範例</span><span class="sxs-lookup"><span data-stu-id="d8731-116">SDK Sample</span></span>](#sdk-sample)
-   [<span data-ttu-id="d8731-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8731-117">Related topics</span></span>](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a><span data-ttu-id="d8731-118">通知和通知區域指導方針</span><span class="sxs-lookup"><span data-stu-id="d8731-118">Notification and Notification Area Guidelines</span></span>

<span data-ttu-id="d8731-119">請參閱 Windows 使用者經驗互動指導方針的 [通知](../uxguide/mess-notif.md) 和 [通知區域](../uxguide/winenv-notification.md) 章節，以取得使用通知和通知區域的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="d8731-119">See the [Notifications](../uxguide/mess-notif.md) and [Notification Area](../uxguide/winenv-notification.md) sections of the Windows User Experience Interaction Guidelines for best practices in the use of notifications and the notification area.</span></span> <span data-ttu-id="d8731-120">其目標是透過適當的通知使用來提供使用者權益，而不會干擾或困擾。</span><span class="sxs-lookup"><span data-stu-id="d8731-120">The goal is to provide user benefit through appropriate use of notifications, without being annoying or distracting.</span></span>

<span data-ttu-id="d8731-121">通知區域不適用於必須立即採取動作的重要資訊。</span><span class="sxs-lookup"><span data-stu-id="d8731-121">The notification area is not for critical information that must be acted on immediately.</span></span> <span data-ttu-id="d8731-122">它也不適合快速程式或命令存取。</span><span class="sxs-lookup"><span data-stu-id="d8731-122">It is also not intended for quick program or command access.</span></span> <span data-ttu-id="d8731-123">從 Windows 7，大部分的功能都是透過應用程式的工作列按鈕來完成。</span><span class="sxs-lookup"><span data-stu-id="d8731-123">As of Windows 7, much of that functionality is best accomplished through an application's taskbar button.</span></span>

<span data-ttu-id="d8731-124">Windows 7 可讓使用者從應用程式隱藏所有的通知（如果他們選擇的話），因此，您可以使用更好的通知設計和使用方式，讓您的應用程式繼續顯示。</span><span class="sxs-lookup"><span data-stu-id="d8731-124">Windows 7 allows a user to suppress all notifications from an application if they choose, so thoughtful notification design and use will incline the user to allow your application to continue to display them.</span></span> <span data-ttu-id="d8731-125">通知會中斷;請確定這是值得的。</span><span class="sxs-lookup"><span data-stu-id="d8731-125">Notifications are an interruption; ensure that they are worth it.</span></span>

<span data-ttu-id="d8731-126">Windows 7 引進了「安靜時間」的概念。</span><span class="sxs-lookup"><span data-stu-id="d8731-126">Windows 7 introduces the concept of "quiet time".</span></span> <span data-ttu-id="d8731-127">當新的使用者第一次登入其帳戶之後，或在作業系統升級或全新安裝之後第一次登入其帳戶時，會定義無訊息時間。</span><span class="sxs-lookup"><span data-stu-id="d8731-127">Quiet time is defined as the first hour after a new user logs into his or her account either for the first time or for the first time after an operating system upgrade or clean installation.</span></span> <span data-ttu-id="d8731-128">這段時間是為了讓使用者能夠探索並熟悉新環境，而不受通知干擾。</span><span class="sxs-lookup"><span data-stu-id="d8731-128">This time is set aside to allow the user to explore and familiarize themselves with the new environment without the distraction of notifications.</span></span> <span data-ttu-id="d8731-129">在這段期間內，不應該傳送或顯示大部分的通知。</span><span class="sxs-lookup"><span data-stu-id="d8731-129">During this time, most notifications should not be sent or shown.</span></span> <span data-ttu-id="d8731-130">例外狀況包括使用者預期會看到的意見反應，以回應使用者動作，例如，當使用者插入 USB 裝置或列印檔案時。</span><span class="sxs-lookup"><span data-stu-id="d8731-130">Exceptions include feedback that the user would expect to see in response to a user action, such as when he or she plugs in a USB device or prints a document.</span></span> <span data-ttu-id="d8731-131">本主題稍後會討論關於靜音時間的 API 細節。</span><span class="sxs-lookup"><span data-stu-id="d8731-131">API specifics of regarding quiet time are discussed later in this topic.</span></span>

## <a name="creating-and-displaying-a-notification"></a><span data-ttu-id="d8731-132">建立與顯示通知</span><span class="sxs-lookup"><span data-stu-id="d8731-132">Creating and Displaying a Notification</span></span>

<span data-ttu-id="d8731-133">本主題的其餘章節將概述在向使用者顯示應用程式的通知時，所要遵循的基本步驟。</span><span class="sxs-lookup"><span data-stu-id="d8731-133">The remaining sections in this topic outline the basic procedure to follow to display a notification from your application to the user.</span></span>

1.  [<span data-ttu-id="d8731-134">新增通知圖示</span><span class="sxs-lookup"><span data-stu-id="d8731-134">Add a Notification Icon</span></span>](#add-a-notification-icon)
2.  [<span data-ttu-id="d8731-135">定義 NOTIFYICONDATA 版本</span><span class="sxs-lookup"><span data-stu-id="d8731-135">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
3.  [<span data-ttu-id="d8731-136">定義通知的外觀和內容</span><span class="sxs-lookup"><span data-stu-id="d8731-136">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
4.  [<span data-ttu-id="d8731-137">檢查使用者狀態</span><span class="sxs-lookup"><span data-stu-id="d8731-137">Check the User Status</span></span>](#check-the-user-status)
5.  [<span data-ttu-id="d8731-138">顯示通知</span><span class="sxs-lookup"><span data-stu-id="d8731-138">Display the Notification</span></span>](#display-the-notification)
6.  [<span data-ttu-id="d8731-139">移除圖示</span><span class="sxs-lookup"><span data-stu-id="d8731-139">Removing an Icon</span></span>](#removing-an-icon)

### <a name="add-a-notification-icon"></a><span data-ttu-id="d8731-140">新增通知圖示</span><span class="sxs-lookup"><span data-stu-id="d8731-140">Add a Notification Icon</span></span>

<span data-ttu-id="d8731-141">若要顯示通知，您必須在通知區域中有一個圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-141">To display a notification, you must have an icon in the notification area.</span></span> <span data-ttu-id="d8731-142">在某些情況下（例如 Microsoft Communicator 或電池計量），該圖示將已存在。</span><span class="sxs-lookup"><span data-stu-id="d8731-142">In certain cases, such as Microsoft Communicator or battery level, that icon will already be present.</span></span> <span data-ttu-id="d8731-143">不過，在其他許多情況下，您只需在顯示通知所需的時間內，才將圖示新增至通知區域。</span><span class="sxs-lookup"><span data-stu-id="d8731-143">In many other cases, however, you will add an icon to the notification area only as long as is needed to show the notification.</span></span> <span data-ttu-id="d8731-144">無論是哪一種情況，都是使用 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 函式來完成。</span><span class="sxs-lookup"><span data-stu-id="d8731-144">In either case, this is accomplished using the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) function.</span></span> <span data-ttu-id="d8731-145">**Shell \_NotifyIcon** 可讓您新增、修改或刪除通知區域中的圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-145">**Shell\_NotifyIcon** allows you to add, modify, or delete an icon in the notification area.</span></span>

![包含三個圖示的通知區域](images/taskbar/notificationareaicons.png)

<span data-ttu-id="d8731-147">將圖示新增至 Windows 7 的通知區域時，預設會將它新增至通知區域的溢位區段。</span><span class="sxs-lookup"><span data-stu-id="d8731-147">When an icon is added to the notification area on Windows 7, it is added to the overflow section of the notification area by default.</span></span> <span data-ttu-id="d8731-148">此區域包含作用中，但不會顯示在通知區域中的通知區域圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-148">This area contains notification area icons that are active, but not visible in the notification area.</span></span> <span data-ttu-id="d8731-149">只有使用者可以將溢出的圖示升階到通知區域，不過在某些情況下，系統可以暫時將圖示升階到通知區域中，做為一分鐘) 的簡短預覽 (。</span><span class="sxs-lookup"><span data-stu-id="d8731-149">Only the user can promote an icon from the overflow to the notification area, although in certain circumstances the system can temporarily promote an icon into the notification area as a short preview (under one minute).</span></span>

> [!Note]  
> <span data-ttu-id="d8731-150">使用者應該要知道他們想要在其通知區域中看到的圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-150">The user should have the final say on which icons they want to see in their notification area.</span></span> <span data-ttu-id="d8731-151">在通知區域中安裝非暫時性的圖示之前，應該先要求使用者提供許可權。</span><span class="sxs-lookup"><span data-stu-id="d8731-151">Before installing a non-transient icon in the notification area, the user should be asked for permission.</span></span> <span data-ttu-id="d8731-152">您也應該提供選項 (一般，雖然它的快捷方式功能表) 從通知區域移除圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-152">They should also be given the option (normally though its shortcut menu) to remove the icon from the notification area.</span></span>

 

<span data-ttu-id="d8731-153">在 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)的呼叫中傳送的 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)結構包含指定通知區域圖示和通知本身的資訊。</span><span class="sxs-lookup"><span data-stu-id="d8731-153">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification itself.</span></span> <span data-ttu-id="d8731-154">以下是通知區域圖示本身特定的專案，可透過 **NOTIFYICONDATA** 設定。</span><span class="sxs-lookup"><span data-stu-id="d8731-154">The following are those items specific to the notification area icon itself that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="d8731-155">從中取得圖示的資源。</span><span class="sxs-lookup"><span data-stu-id="d8731-155">The resource from which the icon is taken.</span></span>
-   <span data-ttu-id="d8731-156">圖示的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8731-156">A unique identifier for the icon.</span></span>
-   <span data-ttu-id="d8731-157">圖示工具提示的樣式。</span><span class="sxs-lookup"><span data-stu-id="d8731-157">The style of the icon's tooltip.</span></span>
-   <span data-ttu-id="d8731-158">圖示的狀態 (隱藏、共用或在通知區域中) 。</span><span class="sxs-lookup"><span data-stu-id="d8731-158">The icon's state (hidden, shared, or both) in the notification area.</span></span>
-   <span data-ttu-id="d8731-159">與圖示相關聯之應用程式視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d8731-159">The handle of an application window associated with the icon.</span></span>
-   <span data-ttu-id="d8731-160">回呼訊息識別碼，可讓圖示與相關聯的應用程式視窗溝通出現在圖示周框矩形和氣球通知內的事件。</span><span class="sxs-lookup"><span data-stu-id="d8731-160">A callback message identifier that allows the icon to communicate events that occur within the icon's bounding rectangle and balloon notification with the associated application window.</span></span> <span data-ttu-id="d8731-161">您可以透過 [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)來取出圖示的周框。</span><span class="sxs-lookup"><span data-stu-id="d8731-161">The icon's bounding rectangle can be retrieved through [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span></span>

<span data-ttu-id="d8731-162">您可以透過兩種方式識別通知區域中的每個圖示：</span><span class="sxs-lookup"><span data-stu-id="d8731-162">Each icon in the notification area can be identified in two ways:</span></span>

-   <span data-ttu-id="d8731-163">在登錄中宣告圖示的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d8731-163">The GUID with which the icon is declared in the registry.</span></span> <span data-ttu-id="d8731-164">這是 Windows 7 和更新版本的慣用方法。</span><span class="sxs-lookup"><span data-stu-id="d8731-164">This is the preferred method on Windows 7 and later.</span></span>
-   <span data-ttu-id="d8731-165">與通知區域圖示相關聯的視窗控制碼，加上應用程式定義的圖示識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8731-165">The handle of a window associated with the notification area icon, plus an application-defined icon identifier.</span></span> <span data-ttu-id="d8731-166">這個方法是在 Windows Vista 及更早版本上使用。</span><span class="sxs-lookup"><span data-stu-id="d8731-166">This method is used on Windows Vista and earlier.</span></span>

<span data-ttu-id="d8731-167">通知區域中的圖示可以有工具提示。</span><span class="sxs-lookup"><span data-stu-id="d8731-167">Icons in the notification area can have a tooltip.</span></span> <span data-ttu-id="d8731-168">工具提示可以是標準工具提示 (慣用的) 或應用程式繪製的彈出 UI。</span><span class="sxs-lookup"><span data-stu-id="d8731-168">The tooltip can be either a standard tooltip (preferred) or an application-drawn, pop-up UI.</span></span> <span data-ttu-id="d8731-169">雖然不需要工具提示，但建議您這樣做。</span><span class="sxs-lookup"><span data-stu-id="d8731-169">While a tooltip is not required, it is recommended.</span></span>

<span data-ttu-id="d8731-170">通知區域圖示應為高 DPI 感知。</span><span class="sxs-lookup"><span data-stu-id="d8731-170">Notification area icons should be high-DPI aware.</span></span> <span data-ttu-id="d8731-171">應用程式應該在其資源檔中提供16x16 圖元圖示和32x32 圖示，然後使用 [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) 來確保正確載入正確的圖示，並適當地進行調整。</span><span class="sxs-lookup"><span data-stu-id="d8731-171">An application should provide both a 16x16 pixel icon and a 32x32 icon in its resource file, and then use [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) to ensure that the correct icon is loaded and scaled appropriately.</span></span>

<span data-ttu-id="d8731-172">負責通知區域圖標的應用程式應該處理滑鼠按一下圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-172">The application responsible for the notification area icon should handle a mouse click for that icon.</span></span> <span data-ttu-id="d8731-173">當使用者以滑鼠右鍵按一下圖示時，應該會顯示一般的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="d8731-173">When a user right-clicks the icon, it should bring up a normal shortcut menu.</span></span> <span data-ttu-id="d8731-174">不過，使用滑鼠左鍵按一下滑鼠左鍵的結果會與圖示的功能不同。</span><span class="sxs-lookup"><span data-stu-id="d8731-174">However, the result of a single click with the left mouse button will vary with the function of the icon.</span></span> <span data-ttu-id="d8731-175">它應該會顯示使用者預期會在最適合該內容的表單中看到的內容，也就是快顯視窗、對話方塊或程式視窗本身。</span><span class="sxs-lookup"><span data-stu-id="d8731-175">It should display what the user would expect to see in the form best suited to that content—a popup window, a dialog box or the program window itself.</span></span> <span data-ttu-id="d8731-176">例如，它可以顯示狀態圖示的狀態文字，或是音量控制項的滑杆。</span><span class="sxs-lookup"><span data-stu-id="d8731-176">For instance, it could show status text for a status icon, or a slider for the volume control.</span></span>

<span data-ttu-id="d8731-177">從按一下所產生的快顯視窗或對話方塊的位置，應該放在通知區域中按一下的座標附近。</span><span class="sxs-lookup"><span data-stu-id="d8731-177">The placement of a popup window or dialog box that results from the click should be placed near the coordinate of the click in the notification area.</span></span> <span data-ttu-id="d8731-178">使用 [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) 來判斷它的位置。</span><span class="sxs-lookup"><span data-stu-id="d8731-178">Use the [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) to determine its location.</span></span>

<span data-ttu-id="d8731-179">您可以將圖示新增至通知區域，而不會顯示通知，方法是只定義上述 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (圖示特定的成員) 和呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d8731-179">The icon can be added to the notification area without displaying a notification by defining only the icon-specific members of [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (discussed above) and calling [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) as shown here:</span></span>


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



<span data-ttu-id="d8731-180">您也可以將圖示新增至通知區域，並在一次呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)時顯示通知。</span><span class="sxs-lookup"><span data-stu-id="d8731-180">You can also add the icon to the notification area and display a notification all in one call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="d8731-181">若要這樣做，請繼續進行本主題中的指示。</span><span class="sxs-lookup"><span data-stu-id="d8731-181">To do so, continue with the instructions in this topic.</span></span>

### <a name="define-the-notifyicondata-version"></a><span data-ttu-id="d8731-182">定義 NOTIFYICONDATA 版本</span><span class="sxs-lookup"><span data-stu-id="d8731-182">Define the NOTIFYICONDATA Version</span></span>

<span data-ttu-id="d8731-183">隨著 Windows 的進展， [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) 結構已經擴充，以包含更多成員來定義更多功能。</span><span class="sxs-lookup"><span data-stu-id="d8731-183">As Windows has progressed, the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure has expanded to include more members to define more functionality.</span></span> <span data-ttu-id="d8731-184">常數用來宣告要搭配您的通知區域圖示使用的 **NOTIFYICONDATA** 版本，以允許回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="d8731-184">Constants are used to declare which version of **NOTIFYICONDATA** to use with your notification area icon, to allow for backward compatibility.</span></span> <span data-ttu-id="d8731-185">除非有令人信服的理由，否則強烈建議您使用 \_ \_ Windows Vista 中引進的 NOTIFYICON 第4版。</span><span class="sxs-lookup"><span data-stu-id="d8731-185">Unless there is a compelling reason to do otherwise, it is strongly recommended that you use the NOTIFYICON\_VERSION\_4 version, introduced in Windows Vista.</span></span> <span data-ttu-id="d8731-186">此版本提供完整的可用功能，包括慣用的功能，可透過已註冊的 GUID 來識別通知區域圖示、絕佳的回呼機制，以及更好的協助工具。</span><span class="sxs-lookup"><span data-stu-id="d8731-186">This version provides the full available functionality, including the preferred ability to identify the notification area icon though a registered GUID, a superior callback mechanism, and better accessibility.</span></span>

<span data-ttu-id="d8731-187">透過下列呼叫設定版本：</span><span class="sxs-lookup"><span data-stu-id="d8731-187">Set the version through the following calls:</span></span>


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



<span data-ttu-id="d8731-188">請注意，這個 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 呼叫不會顯示通知。</span><span class="sxs-lookup"><span data-stu-id="d8731-188">Note that this call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) does not display a notification.</span></span>

### <a name="define-the-notification-look-and-contents"></a><span data-ttu-id="d8731-189">定義通知的外觀和內容</span><span class="sxs-lookup"><span data-stu-id="d8731-189">Define the Notification Look and Contents</span></span>

<span data-ttu-id="d8731-190">通知是一種特殊類型的氣球工具提示控制項。</span><span class="sxs-lookup"><span data-stu-id="d8731-190">A notification is a special type of balloon tooltip control.</span></span> <span data-ttu-id="d8731-191">它包含標題、主體文字和圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-191">It contains a title, body text, and an icon.</span></span> <span data-ttu-id="d8731-192">就像視窗一樣，它的右上角有一個 [ **關閉** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="d8731-192">Like a window, it has a **Close** button in its upper right corner.</span></span> <span data-ttu-id="d8731-193">它也包含一個 [ **選項** ] 按鈕，可開啟主控台中的通知區域圖示專案，讓使用者可以顯示或隱藏圖示，或只顯示沒有圖示的通知。</span><span class="sxs-lookup"><span data-stu-id="d8731-193">It also contains a **Options** button that opens the Notification Area Icons item in the Control Panel, which allows the user to show or hide the icon or show only notifications without an icon.</span></span>

![通知氣球的螢幕擷取畫面，指出電池電力偏低](images/taskbar/notificationballoon.png)

<span data-ttu-id="d8731-195">在 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)的呼叫中傳送的 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)結構包含同時指定通知區域圖示和通知氣球本身的資訊。</span><span class="sxs-lookup"><span data-stu-id="d8731-195">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification balloon itself.</span></span> <span data-ttu-id="d8731-196">以下是可透過 **NOTIFYICONDATA** 設定的通知特定專案。</span><span class="sxs-lookup"><span data-stu-id="d8731-196">The following are those items specific to the notification that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="d8731-197">要在通知氣球中顯示的圖示，由通知類型指定。</span><span class="sxs-lookup"><span data-stu-id="d8731-197">An icon to display in the notification balloon, which is specified by the notification type.</span></span> <span data-ttu-id="d8731-198">您可以指定圖示的大小，也可以指定自訂圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-198">The size of the icon can be specified, as well as custom icons.</span></span>
-   <span data-ttu-id="d8731-199">通知標題。</span><span class="sxs-lookup"><span data-stu-id="d8731-199">A notification title.</span></span> <span data-ttu-id="d8731-200">在英文 (中，此標題的長度上限為48個字元，以容納當地語系化) 。</span><span class="sxs-lookup"><span data-stu-id="d8731-200">This title should be a maximum of 48 characters long in English (to accommodate localization).</span></span> <span data-ttu-id="d8731-201">標題是通知的第一行，而且會透過使用字型大小、色彩和權數來分開設定。</span><span class="sxs-lookup"><span data-stu-id="d8731-201">The title is the first line of the notification, and set apart through the use of font size, color, and weight.</span></span>
-   <span data-ttu-id="d8731-202">要在通知主體中使用的文字。</span><span class="sxs-lookup"><span data-stu-id="d8731-202">Text for use in the body of the notification.</span></span> <span data-ttu-id="d8731-203">此文字最多可有200個字元的英文 (，以配合當地語系化) 。</span><span class="sxs-lookup"><span data-stu-id="d8731-203">This text should be a maximum of 200 characters in English (to accommodate localization).</span></span>
-   <span data-ttu-id="d8731-204">如果通知無法立即顯示，是否應捨棄通知。</span><span class="sxs-lookup"><span data-stu-id="d8731-204">Whether the notification should be discarded if it cannot be displayed immediately.</span></span>
-   <span data-ttu-id="d8731-205">通知的超時時間。</span><span class="sxs-lookup"><span data-stu-id="d8731-205">A timeout for the notification.</span></span> <span data-ttu-id="d8731-206">在 Windows Vista 和更新版本的系統中，會忽略這項設定，以改用整個系統的協助工具超時設定。</span><span class="sxs-lookup"><span data-stu-id="d8731-206">This setting is ignored in Windows Vista and later systems in favor of a system-wide accessibility timeout setting.</span></span>
-   <span data-ttu-id="d8731-207">通知是否應遵守無訊息時間，請透過 [**NIIF 尊重無訊息 \_ \_ \_ 時間**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) 旗標來設定。</span><span class="sxs-lookup"><span data-stu-id="d8731-207">Whether the notification should respect quiet time, set through the [**NIIF\_RESPECT\_QUIET\_TIME**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) flag.</span></span>

> [!Note]  
> <span data-ttu-id="d8731-208">[**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)和 [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)介面是 [**Shell \_ NOTIFYICON**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)的元件物件模型 (COM) 包裝函式。</span><span class="sxs-lookup"><span data-stu-id="d8731-208">The [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) and [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) interfaces are Component Object Model (COM) wrappers for [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="d8731-209">不過，目前無法 \_ \_ 直接透過 **Shell \_ NOTIFYICON** 提供完整的 NOTIFYICON 第4版功能，包括使用 GUID 來識別通知區域圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-209">However, at this time, they do not provide the full NOTIFYICON\_VERSION\_4 functionality available through **Shell\_NotifyIcon** directly, including the use of a GUID to identify the notification area icon.</span></span>

 

### <a name="check-the-user-status"></a><span data-ttu-id="d8731-210">檢查使用者狀態</span><span class="sxs-lookup"><span data-stu-id="d8731-210">Check the User Status</span></span>

<span data-ttu-id="d8731-211">系統使用 [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) 函式來檢查使用者是否處於無訊息時間、離開電腦，或處於不間斷的狀態，例如展示模式。</span><span class="sxs-lookup"><span data-stu-id="d8731-211">The system uses the [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) function is used to check whether the user is in quiet time, away from the computer, or in an uninterruptable state such as Presentation mode.</span></span> <span data-ttu-id="d8731-212">系統是否會顯示您的通知取決於此狀態。</span><span class="sxs-lookup"><span data-stu-id="d8731-212">Whether the system displays your notification depends on this state.</span></span>

> [!Note]  
> <span data-ttu-id="d8731-213">如果您的應用程式使用未使用 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)、 [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)或 [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)的自訂通知方法，則應該一律明確地呼叫 [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) ，以判斷是否應該在該時間顯示通知 UI。</span><span class="sxs-lookup"><span data-stu-id="d8731-213">If your application is using a custom notification method that does not use [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification), or [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), it should always explicitly call [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) to determine whether it should display notification UI at that time.</span></span>

 

<span data-ttu-id="d8731-214">當使用者離開時傳送的通知已排入佇列以供顯示，但因為您無法得知使用者將會傳回的時間，或是在該時間之後是否仍然有效通知，您可能會考慮稍後再重新傳送通知。</span><span class="sxs-lookup"><span data-stu-id="d8731-214">Notifications sent when the user is away are queued for display, but because you cannot know when the user will return or whether the notification will still be valid at that time, you might consider resending the notification later.</span></span>

<span data-ttu-id="d8731-215">Unshown 時，會捨棄在無訊息期間傳送的通知。</span><span class="sxs-lookup"><span data-stu-id="d8731-215">Notifications sent during quiet time are discarded unshown.</span></span> <span data-ttu-id="d8731-216">設計指導方針會要求所有通知都可忽略。</span><span class="sxs-lookup"><span data-stu-id="d8731-216">Design guidelines ask that all notifications be ignorable.</span></span> <span data-ttu-id="d8731-217">它們應該不需要立即的使用者動作。</span><span class="sxs-lookup"><span data-stu-id="d8731-217">They should not require immediate user action.</span></span> <span data-ttu-id="d8731-218">因此，沒有任何通知應該覆寫無訊息時間。</span><span class="sxs-lookup"><span data-stu-id="d8731-218">Therefore, no notification is so important that it should override quiet time.</span></span>

### <a name="display-the-notification"></a><span data-ttu-id="d8731-219">顯示通知</span><span class="sxs-lookup"><span data-stu-id="d8731-219">Display the Notification</span></span>

<span data-ttu-id="d8731-220">設定 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) 版本並在 **NOTIFYICONDATA** 結構中定義通知之後，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 來顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-220">Once you have set the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) version and defined the notification in a **NOTIFYICONDATA** structure, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to display the icon.</span></span>

-   <span data-ttu-id="d8731-221">如果沒有通知區域圖示，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 來新增圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-221">If the notification area icon is not present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to add the icon.</span></span> <span data-ttu-id="d8731-222">針對暫時性和非暫時性的圖示進行這項作業。</span><span class="sxs-lookup"><span data-stu-id="d8731-222">Do this for both transient and non-transient icons.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   <span data-ttu-id="d8731-223">如果通知區域圖示已經存在，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) 來修改圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-223">If the notification area icon is already present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to modify the icon.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

<span data-ttu-id="d8731-224">下列程式碼顯示設定 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) 資料並透過 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)傳送它的範例。</span><span class="sxs-lookup"><span data-stu-id="d8731-224">The following code shows an example of setting [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) data and sending it through [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="d8731-225">請注意，此範例會透過 Windows 7) 中偏好的 GUID (來識別通知圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-225">Note that this example identifies the notification icon through a GUID (preferred in Windows 7).</span></span>


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a><span data-ttu-id="d8731-226">移除圖示</span><span class="sxs-lookup"><span data-stu-id="d8731-226">Removing an Icon</span></span>

<span data-ttu-id="d8731-227">若要移除圖示，例如，當您只是暫時新增圖示來廣播通知時，請呼叫 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)，如下所示。</span><span class="sxs-lookup"><span data-stu-id="d8731-227">To remove an icon—for instance, when you have only added the icon temporarily to broadcast a notification—call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)as shown here.</span></span> <span data-ttu-id="d8731-228">此呼叫只需要最基本的 [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) 結構來識別圖示。</span><span class="sxs-lookup"><span data-stu-id="d8731-228">Only a minimal [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure that identifies the icon is needed in this call.</span></span>


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> <span data-ttu-id="d8731-229">卸載應用程式時，它的通知區域圖示仍然可以在主控台的 [通知區域圖示] 頁面中，以選項的形式出現在最多七天。</span><span class="sxs-lookup"><span data-stu-id="d8731-229">When an application is uninstalled, its notification area icon can still appear to the user as an option in the Notification Area Icons page in the Control Panel for up to seven days.</span></span> <span data-ttu-id="d8731-230">不過，任何進行的變更都不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="d8731-230">However, any changes made there will have no effect.</span></span>

 

## <a name="sdk-sample"></a><span data-ttu-id="d8731-231">SDK 範例</span><span class="sxs-lookup"><span data-stu-id="d8731-231">SDK Sample</span></span>

<span data-ttu-id="d8731-232">如需使用 [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)的完整範例，請參閱 Windows 軟體開發套件 (SDK) 中的 [NotificationIcon 範例](samples-notificationicon.md)範例。</span><span class="sxs-lookup"><span data-stu-id="d8731-232">See the [NotificationIcon Sample](samples-notificationicon.md) sample in the Windows Software Development Kit (SDK) for a full example of the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8731-233">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8731-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8731-234">**Shell \_ NotifyIcon**</span><span class="sxs-lookup"><span data-stu-id="d8731-234">**Shell\_NotifyIcon**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[<span data-ttu-id="d8731-235">**Shell \_ NotifyIconGetRect**</span><span class="sxs-lookup"><span data-stu-id="d8731-235">**Shell\_NotifyIconGetRect**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[<span data-ttu-id="d8731-236">**NOTIFYICONDATA**</span><span class="sxs-lookup"><span data-stu-id="d8731-236">**NOTIFYICONDATA**</span></span>](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[<span data-ttu-id="d8731-237">**SHQueryUserNotificationState**</span><span class="sxs-lookup"><span data-stu-id="d8731-237">**SHQueryUserNotificationState**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[<span data-ttu-id="d8731-238">**IUserNotification**</span><span class="sxs-lookup"><span data-stu-id="d8731-238">**IUserNotification**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[<span data-ttu-id="d8731-239">**IUserNotification2**</span><span class="sxs-lookup"><span data-stu-id="d8731-239">**IUserNotification2**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[<span data-ttu-id="d8731-240">工作列</span><span class="sxs-lookup"><span data-stu-id="d8731-240">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="d8731-241">工作列擴充功能</span><span class="sxs-lookup"><span data-stu-id="d8731-241">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
