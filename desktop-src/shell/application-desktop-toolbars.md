---
description: 應用程式桌面工具列 (也稱為 appbar) 是類似于 Windows 工作列的視窗。
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: 使用應用程式桌面工具列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140ef94c1daeb571cd0d766dfbd4dc28b7991efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112353"
---
# <a name="using-application-desktop-toolbars"></a><span data-ttu-id="a0264-103">使用應用程式桌面工具列</span><span class="sxs-lookup"><span data-stu-id="a0264-103">Using Application Desktop Toolbars</span></span>

<span data-ttu-id="a0264-104">*應用程式桌面工具列* (也稱為 appbar) 是類似于 Windows 工作列的視窗。</span><span class="sxs-lookup"><span data-stu-id="a0264-104">An *application desktop toolbar* (also called an appbar) is a window that is similar to the Windows taskbar.</span></span> <span data-ttu-id="a0264-105">它會錨定到畫面邊緣，通常會包含可讓使用者快速存取其他應用程式和視窗的按鈕。</span><span class="sxs-lookup"><span data-stu-id="a0264-105">It is anchored to an edge of the screen, and it typically contains buttons that give the user quick access to other applications and windows.</span></span> <span data-ttu-id="a0264-106">系統會防止其他應用程式使用 appbar 所使用的桌面區域。</span><span class="sxs-lookup"><span data-stu-id="a0264-106">The system prevents other applications from using the desktop area used by an appbar.</span></span> <span data-ttu-id="a0264-107">在任何指定時間，桌面上都可以有任意數目的透過像 appbars。</span><span class="sxs-lookup"><span data-stu-id="a0264-107">Any number of appbars can exist on the desktop at any given time.</span></span>

<span data-ttu-id="a0264-108">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="a0264-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a0264-109">關於應用程式桌面工具列</span><span class="sxs-lookup"><span data-stu-id="a0264-109">About Application Desktop Toolbars</span></span>](#about-application-desktop-toolbars)
    -   [<span data-ttu-id="a0264-110">傳送訊息</span><span class="sxs-lookup"><span data-stu-id="a0264-110">Sending Messages</span></span>](#sending-messages)
    -   [<span data-ttu-id="a0264-111">註冊</span><span class="sxs-lookup"><span data-stu-id="a0264-111">Registration</span></span>](#registration)
    -   [<span data-ttu-id="a0264-112">Appbar 大小和位置</span><span class="sxs-lookup"><span data-stu-id="a0264-112">Appbar Size and Position</span></span>](#appbar-size-and-position)
    -   [<span data-ttu-id="a0264-113">自動隱藏應用程式桌面工具列</span><span class="sxs-lookup"><span data-stu-id="a0264-113">Autohide Application Desktop Toolbars</span></span>](#autohide-application-desktop-toolbars)
    -   [<span data-ttu-id="a0264-114">Appbar 通知訊息</span><span class="sxs-lookup"><span data-stu-id="a0264-114">Appbar Notification Messages</span></span>](#appbar-notification-messages)
-   [<span data-ttu-id="a0264-115">註冊應用程式桌面工具列</span><span class="sxs-lookup"><span data-stu-id="a0264-115">Registering an Application Desktop Toolbar</span></span>](#registering-an-application-desktop-toolbar)
-   [<span data-ttu-id="a0264-116">設定 Appbar 大小和位置</span><span class="sxs-lookup"><span data-stu-id="a0264-116">Setting the Appbar Size and Position</span></span>](#setting-the-appbar-size-and-position)
-   [<span data-ttu-id="a0264-117">處理 Appbar 通知訊息</span><span class="sxs-lookup"><span data-stu-id="a0264-117">Processing Appbar Notification Messages</span></span>](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a><span data-ttu-id="a0264-118">關於應用程式桌面工具列</span><span class="sxs-lookup"><span data-stu-id="a0264-118">About Application Desktop Toolbars</span></span>

<span data-ttu-id="a0264-119">Windows 提供的 API 可讓您利用系統提供的 appbar 服務。</span><span class="sxs-lookup"><span data-stu-id="a0264-119">Windows provides an API that lets you take advantage of appbar services provided by the system.</span></span> <span data-ttu-id="a0264-120">這些服務可協助確保應用程式定義的透過像 appbars 能以另一個和工作列順暢地運作。</span><span class="sxs-lookup"><span data-stu-id="a0264-120">The services help ensure that application-defined appbars operate smoothly with one another and with the taskbar.</span></span> <span data-ttu-id="a0264-121">系統會維護每個 appbar 的相關資訊，並傳送透過像 appbars 訊息，通知他們可能會影響其大小、位置和外觀的事件。</span><span class="sxs-lookup"><span data-stu-id="a0264-121">The system maintains information about each appbar and sends the appbars messages to notify them about events that can affect their size, position, and appearance.</span></span>

### <a name="sending-messages"></a><span data-ttu-id="a0264-122">傳送訊息</span><span class="sxs-lookup"><span data-stu-id="a0264-122">Sending Messages</span></span>

<span data-ttu-id="a0264-123">應用程式會使用一組特殊的訊息（稱為「appbar 訊息」）來新增或移除 appbar、設定 appbar 的大小和位置，以及取得工作列大小、位置和狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a0264-123">An application uses a special set of messages, called appbar messages, to add or remove an appbar, set an appbar's size and position, and retrieve information about the size, position, and state of the taskbar.</span></span> <span data-ttu-id="a0264-124">若要傳送 appbar 訊息，應用程式必須使用 [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="a0264-124">To send an appbar message, an application must use the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function.</span></span> <span data-ttu-id="a0264-125">函數的參數包含訊息識別碼，例如 [**ABM \_ NEW**](abm-new.md)，以及 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) 結構的位址。</span><span class="sxs-lookup"><span data-stu-id="a0264-125">The function's parameters include a message identifier, such as [**ABM\_NEW**](abm-new.md), and the address of an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="a0264-126">結構成員包含系統處理指定訊息所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="a0264-126">The structure members contain information that the system needs to process the given message.</span></span>

<span data-ttu-id="a0264-127">針對任何指定的 appbar 訊息，系統會使用 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) 結構的某些成員，並忽略其他成員。</span><span class="sxs-lookup"><span data-stu-id="a0264-127">For any given appbar message, the system uses some members of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure and ignores the others.</span></span> <span data-ttu-id="a0264-128">不過，系統一律會使用 **cbSize** 和 **hWnd** 成員，因此應用程式必須針對每個 appbar 訊息填滿這些成員。</span><span class="sxs-lookup"><span data-stu-id="a0264-128">However, the system always uses the **cbSize** and **hWnd** members, so an application must fill these members for every appbar message.</span></span> <span data-ttu-id="a0264-129">**CbSize** 成員會指定結構的大小，而 **hWnd** 成員是 appbar 視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a0264-129">The **cbSize** member specifies the size of the structure, and the **hWnd** member is the handle to the appbar's window.</span></span>

<span data-ttu-id="a0264-130">某些 appbar 訊息會要求系統的資訊。</span><span class="sxs-lookup"><span data-stu-id="a0264-130">Some appbar messages request information from the system.</span></span> <span data-ttu-id="a0264-131">處理這些訊息時，系統會將要求的資訊複製到 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) 結構中。</span><span class="sxs-lookup"><span data-stu-id="a0264-131">When processing these messages, the system copies the requested information into the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

### <a name="registration"></a><span data-ttu-id="a0264-132">註冊</span><span class="sxs-lookup"><span data-stu-id="a0264-132">Registration</span></span>

<span data-ttu-id="a0264-133">系統會保留透過像 appbars 的內部清單，並維護清單中每個橫條的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a0264-133">The system keeps an internal list of appbars and maintains information about each bar in the list.</span></span> <span data-ttu-id="a0264-134">系統會使用此資訊來管理透過像 appbars、為它們執行服務，並傳送通知訊息給他們。</span><span class="sxs-lookup"><span data-stu-id="a0264-134">The system uses the information to manage appbars, perform services for them, and send them notification messages.</span></span>

<span data-ttu-id="a0264-135">應用程式必須註冊 appbar (也就是將它新增至內部清單) ，然後才能從系統接收 appbar 服務。</span><span class="sxs-lookup"><span data-stu-id="a0264-135">An application must register an appbar (that is, add it to the internal list) before it can receive appbar services from the system.</span></span> <span data-ttu-id="a0264-136">若要註冊 appbar，應用程式會傳送 [**ABM 的 \_ 新**](abm-new.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-136">To register an appbar, an application sends the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="a0264-137">伴隨的 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) 結構包含 appbar 視窗的控制碼和應用程式定義的訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0264-137">The accompanying [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure includes the handle to the appbar's window and an application-defined message identifier.</span></span> <span data-ttu-id="a0264-138">系統會使用訊息識別碼，將通知訊息傳送至 appbar 視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="a0264-138">The system uses the message identifier to send notification messages to the window procedure of the appbar window.</span></span> <span data-ttu-id="a0264-139">如需詳細資訊，請參閱 Appbar 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-139">For more information, see Appbar Notification Messages.</span></span>

<span data-ttu-id="a0264-140">應用程式會藉由傳送 [**ABM \_ 移除**](abm-remove.md) 訊息來取消註冊 appbar。</span><span class="sxs-lookup"><span data-stu-id="a0264-140">An application unregisters an appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="a0264-141">取消註冊 appbar 會將它從系統的透過像 appbars 內部清單中移除。</span><span class="sxs-lookup"><span data-stu-id="a0264-141">Unregistering an appbar removes it from the system's internal list of appbars.</span></span> <span data-ttu-id="a0264-142">系統不會再將通知訊息傳送至 appbar，或防止其他應用程式使用 appbar 所使用的螢幕區域。</span><span class="sxs-lookup"><span data-stu-id="a0264-142">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span> <span data-ttu-id="a0264-143">應用程式應該一律在終結 appbar 之前傳送 **ABM \_ 移除** 。</span><span class="sxs-lookup"><span data-stu-id="a0264-143">An application should always send **ABM\_REMOVE** before destroying an appbar.</span></span>

### <a name="appbar-size-and-position"></a><span data-ttu-id="a0264-144">Appbar 大小和位置</span><span class="sxs-lookup"><span data-stu-id="a0264-144">Appbar Size and Position</span></span>

<span data-ttu-id="a0264-145">應用程式應該設定 appbar 的大小和位置，讓它不會干擾任何其他透過像 appbars 或工作列。</span><span class="sxs-lookup"><span data-stu-id="a0264-145">An application should set an appbar's size and position so that it does not interfere with any other appbars or the taskbar.</span></span> <span data-ttu-id="a0264-146">每個 appbar 都必須錨定到畫面的特定邊緣，而且可以將多個透過像 appbars 錨定至邊緣。</span><span class="sxs-lookup"><span data-stu-id="a0264-146">Every appbar must be anchored to a particular edge of the screen, and multiple appbars can be anchored to an edge.</span></span> <span data-ttu-id="a0264-147">但是，如果 appbar 錨定到與工作列相同的邊緣，系統就會確保工作列一律位於最外層的邊緣上。</span><span class="sxs-lookup"><span data-stu-id="a0264-147">However, if an appbar is anchored to the same edge as the taskbar, the system ensures that the taskbar is always on the outermost edge.</span></span>

<span data-ttu-id="a0264-148">若要設定 appbar 的大小和位置，應用程式會先傳送 [**ABM \_ QUERYPOS**](abm-querypos.md) 訊息，以針對 appbar 提出螢幕邊緣和周框矩形。</span><span class="sxs-lookup"><span data-stu-id="a0264-148">To set the size and position of an appbar, an application first proposes a screen edge and bounding rectangle for the appbar by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="a0264-149">系統會決定工作列或其他 appbar 是否使用建議的矩形內的任何部分的螢幕區域，視需要) 調整矩形 (，並將調整的矩形傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="a0264-149">The system determines whether any part of the screen area within the proposed rectangle is used by the taskbar or another appbar, adjusts the rectangle (if necessary), and returns the adjusted rectangle to the application.</span></span>

<span data-ttu-id="a0264-150">接下來，應用程式會傳送 [**ABM \_ SETPOS**](abm-setpos.md) 訊息，以設定 appbar 的新周框。</span><span class="sxs-lookup"><span data-stu-id="a0264-150">Next, the application sends the [**ABM\_SETPOS**](abm-setpos.md) message to set the new bounding rectangle for the appbar.</span></span> <span data-ttu-id="a0264-151">同樣地，系統可能會調整矩形，再將它傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="a0264-151">Again, the system may adjust the rectangle before returning it to the application.</span></span> <span data-ttu-id="a0264-152">基於這個理由，應用程式應該使用 **ABM \_ SETPOS** 所傳回的調整矩形來設定最終大小和位置。</span><span class="sxs-lookup"><span data-stu-id="a0264-152">For this reason, the application should use the adjusted rectangle returned by **ABM\_SETPOS** to set the final size and position.</span></span> <span data-ttu-id="a0264-153">應用程式可以使用 [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) 函式，將 appbar 移至位置。</span><span class="sxs-lookup"><span data-stu-id="a0264-153">The application can use the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="a0264-154">藉由使用兩個步驟的程式來設定大小和位置，系統可讓應用程式在移動作業期間提供中繼回饋給使用者。</span><span class="sxs-lookup"><span data-stu-id="a0264-154">By using a two-step process to set the size and position, the system enables the application to provide intermediate feedback to the user during the move operation.</span></span> <span data-ttu-id="a0264-155">例如，如果使用者拖曳 appbar，則應用程式可能會顯示陰影矩形，指出 appbar 實際移動之前的新位置。</span><span class="sxs-lookup"><span data-stu-id="a0264-155">For example, if the user drags an appbar, the application might display a shaded rectangle indicating the new position before the appbar actually moves.</span></span>

<span data-ttu-id="a0264-156">應用程式應該在註冊之後設定其 appbar 的大小和位置，並在 appbar 收到 [**ABN \_ POSCHANGED**](abn-poschanged.md) 通知訊息時設定它的位置。</span><span class="sxs-lookup"><span data-stu-id="a0264-156">An application should set the size and position of its appbar after registering it and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="a0264-157">每當在工作列的大小、位置或可見度狀態發生變更，以及在螢幕上的另一個 appbar 調整大小、新增或移除時，appbar 就會收到這則通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-157">An appbar receives this notification message whenever a change occurs in the taskbar's size, position, or visibility state and whenever another appbar on the same side of the screen is resized, added, or removed.</span></span>

<span data-ttu-id="a0264-158">每當 appbar 收到 WM \_ 啟動訊息時，它應該會傳送 [**ABM \_ 啟動**](abm-activate.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-158">Whenever an appbar receives the WM\_ACTIVATE message, it should send the [**ABM\_ACTIVATE**](abm-activate.md) message.</span></span> <span data-ttu-id="a0264-159">同樣地，當 appbar 收到 WM \_ WINDOWPOSCHANGED 訊息時，它必須呼叫 [**ABM \_ WINDOWPOSCHANGED**](abm-windowposchanged.md)。</span><span class="sxs-lookup"><span data-stu-id="a0264-159">Similarly, when an appbar receives a WM\_WINDOWPOSCHANGED message, it must call [**ABM\_WINDOWPOSCHANGED**](abm-windowposchanged.md).</span></span> <span data-ttu-id="a0264-160">傳送這些訊息可確保系統正確設定相同邊緣上任何自動隱藏透過像 appbars 的迭置順序。</span><span class="sxs-lookup"><span data-stu-id="a0264-160">Sending these messages ensures that the system properly sets the z-order of any autohide appbars on the same edge.</span></span>

### <a name="autohide-application-desktop-toolbars"></a><span data-ttu-id="a0264-161">自動隱藏應用程式桌面工具列</span><span class="sxs-lookup"><span data-stu-id="a0264-161">Autohide Application Desktop Toolbars</span></span>

<span data-ttu-id="a0264-162">自動隱藏 appbar 是一種一般隱藏的，但是當使用者將滑鼠游標移至與 appbar 相關聯的螢幕邊緣時，就會看到它。</span><span class="sxs-lookup"><span data-stu-id="a0264-162">An autohide appbar is one that is normally hidden but becomes visible when the user moves the mouse cursor to the screen edge with which the appbar is associated.</span></span> <span data-ttu-id="a0264-163">當使用者將滑鼠游標移出橫條的周框時，appbar 會再次隱藏本身。</span><span class="sxs-lookup"><span data-stu-id="a0264-163">The appbar hides itself again when the user moves the mouse cursor out of the bar's bounding rectangle.</span></span>

<span data-ttu-id="a0264-164">雖然系統在任何指定的時間都允許多個不同的透過像 appbars，但每個螢幕邊緣一次只允許一個自動隱藏 appbar，並以先服務為基礎。</span><span class="sxs-lookup"><span data-stu-id="a0264-164">Although the system allows a number of different appbars at any given time, it allows only one autohide appbar at a time for each screen edge on a first-come, first-served basis.</span></span> <span data-ttu-id="a0264-165">系統會自動將自動隱藏 appbar (的迭置順序維持在其 z 順序群組內，但僅) 。</span><span class="sxs-lookup"><span data-stu-id="a0264-165">The system automatically maintains the z-order of an autohide appbar (within its z-order group only).</span></span>

<span data-ttu-id="a0264-166">應用程式會使用 [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) 訊息來註冊或取消註冊自動隱藏 appbar。</span><span class="sxs-lookup"><span data-stu-id="a0264-166">An application uses the [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) message to register or unregister an autohide appbar.</span></span> <span data-ttu-id="a0264-167">訊息會指定 appbar 的邊緣，以及指定是否要註冊或取消註冊 appbar 的旗標。</span><span class="sxs-lookup"><span data-stu-id="a0264-167">The message specifies the edge for the appbar and a flag that specifies whether the appbar is to be registered or unregistered.</span></span> <span data-ttu-id="a0264-168">如果正在註冊自動隱藏 appbar，但其中一個已與指定的邊緣相關聯，則訊息會失敗。</span><span class="sxs-lookup"><span data-stu-id="a0264-168">The message fails if an autohide appbar is being registered but one is already associated with the specified edge.</span></span> <span data-ttu-id="a0264-169">應用程式可以藉由傳送 [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) 訊息，來取得與邊緣相關聯的自動隱藏 appbar 控制碼。</span><span class="sxs-lookup"><span data-stu-id="a0264-169">An application can retrieve the handle to the autohide appbar associated with an edge by sending the [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) message.</span></span>

<span data-ttu-id="a0264-170">自動隱藏 appbar 不需要註冊為一般 appbar;也就是說，它不需要藉由傳送 [**ABM 的 \_ 新**](abm-new.md) 訊息來註冊。</span><span class="sxs-lookup"><span data-stu-id="a0264-170">An autohide appbar does not need to register as a normal appbar; that is, it does not need to be registered by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="a0264-171">未由 **ABM \_ NEW** 註冊的 appbar 會與螢幕上相同邊緣上錨定的任何透過像 appbars 重迭。</span><span class="sxs-lookup"><span data-stu-id="a0264-171">An appbar that is not registered by **ABM\_NEW** overlaps any appbars anchored on the same edge of the screen.</span></span>

### <a name="appbar-notification-messages"></a><span data-ttu-id="a0264-172">Appbar 通知訊息</span><span class="sxs-lookup"><span data-stu-id="a0264-172">Appbar Notification Messages</span></span>

<span data-ttu-id="a0264-173">系統會傳送訊息，通知 appbar 可能會影響其位置和外觀的事件。</span><span class="sxs-lookup"><span data-stu-id="a0264-173">The system sends messages to notify an appbar about events that can affect its position and appearance.</span></span> <span data-ttu-id="a0264-174">訊息會在應用程式定義的訊息內容中傳送。</span><span class="sxs-lookup"><span data-stu-id="a0264-174">The messages are sent in the context of an application-defined message.</span></span> <span data-ttu-id="a0264-175">應用程式會在傳送 [**ABM 的 \_ 新**](abm-new.md) 訊息以註冊 appbar 時，指定訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a0264-175">The application specifies the identifier of the message when it sends the [**ABM\_NEW**](abm-new.md) message to register the appbar.</span></span> <span data-ttu-id="a0264-176">通知碼位於應用程式定義之訊息的 *wParam* 參數中。</span><span class="sxs-lookup"><span data-stu-id="a0264-176">The notification code is in the *wParam* parameter of the application-defined message.</span></span>

<span data-ttu-id="a0264-177">當您將另一個 appbar 新增至螢幕邊緣，或在螢幕上的另一個 appbar 調整大小或移除時，appbar 會在工作列的大小、位置或可見度狀態變更時收到 [**ABN \_ POSCHANGED**](abn-poschanged.md) 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-177">An appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message when the taskbar's size, position, or visibility state changes, when another appbar is added to the same edge of the screen, or when another appbar on the same edge of the screen is resized or removed.</span></span> <span data-ttu-id="a0264-178">Appbar 應該藉由傳送 [**ABM \_ QUERYPOS**](abm-querypos.md) 和 [**ABM \_ SETPOS**](abm-setpos.md) 訊息來回應這則通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-178">An appbar should respond to this notification message by sending [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="a0264-179">如果 appbar 的位置已變更，則應該呼叫 [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) 函式，將其本身移至新的位置。</span><span class="sxs-lookup"><span data-stu-id="a0264-179">If an appbar's position has changed, it should call the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

<span data-ttu-id="a0264-180">當工作列的自動隱藏或 alwayson 狀態變更時（也就是當使用者在工作列的屬性工作表上選取或清除 [**永遠開啟**] 或 [**自動隱藏**] 核取方塊時），系統就會傳送 [**ABN \_ STATECHANGE**](abn-statechange.md)通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-180">The system sends the [**ABN\_STATECHANGE**](abn-statechange.md) notification message whenever the taskbar's autohide or always-on-top state has changed—that is, when the user selects or clears the **Always on top** or **Auto hide** check box on the taskbar's property sheet.</span></span> <span data-ttu-id="a0264-181">Appbar 可以使用此通知訊息，將其狀態設定為符合工作列的狀態（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="a0264-181">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

<span data-ttu-id="a0264-182">當全螢幕應用程式啟動時，或當最後一個全螢幕應用程式關閉時，appbar 會收到 [**ABN \_ FULLSCREENAPP**](abn-fullscreenapp.md) 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-182">When a full-screen application is started or when the last full-screen application is closed, an appbar receives the [**ABN\_FULLSCREENAPP**](abn-fullscreenapp.md) notification message.</span></span> <span data-ttu-id="a0264-183">*LParam* 參數會指出全螢幕應用程式是否開啟或關閉。</span><span class="sxs-lookup"><span data-stu-id="a0264-183">The *lParam* parameter indicates whether the full-screen application is opening or closing.</span></span> <span data-ttu-id="a0264-184">如果開啟，appbar 必須放到迭置順序的底部。</span><span class="sxs-lookup"><span data-stu-id="a0264-184">If it is opening, the appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="a0264-185">當最後一個全螢幕應用程式關閉時，appbar 應該會還原其 z 順序位置。</span><span class="sxs-lookup"><span data-stu-id="a0264-185">The appbar should restore its z-order position when the last full-screen application has closed.</span></span>

<span data-ttu-id="a0264-186">當使用者從工作列的快捷方式功能表中選取串聯、水準磚或垂直磚命令時，appbar 會收到 [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-186">An appbar receives the [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) notification message when the user selects the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span> <span data-ttu-id="a0264-187">系統會在重新排列 windows (*lParam* 為 **TRUE**) 之前，以及在排列 Windows (*lParam* 為 **FALSE**) 之後，將訊息傳送兩次。</span><span class="sxs-lookup"><span data-stu-id="a0264-187">The system sends the message two times—before rearranging the windows (*lParam* is **TRUE**) and after arranging the windows (*lParam* is **FALSE**).</span></span>

<span data-ttu-id="a0264-188">Appbar 可以使用 [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) 訊息，將本身從 cascade 或磚作業中排除。</span><span class="sxs-lookup"><span data-stu-id="a0264-188">An appbar can use [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) messages to exclude itself from the cascade or tile operation.</span></span> <span data-ttu-id="a0264-189">若要排除本身，appbar 應該在 *lParam* 為 **TRUE** 時隱藏本身，並在 *lParam* 為 **FALSE** 時顯示本身。</span><span class="sxs-lookup"><span data-stu-id="a0264-189">To exclude itself, the appbar should hide itself when *lParam* is **TRUE** and show itself when *lParam* is **FALSE**.</span></span> <span data-ttu-id="a0264-190">如果 appbar 隱藏本身以回應此訊息，則不需要傳送 [**ABM \_ QUERYPOS**](abm-querypos.md) 和 [**ABM \_ SETPOS**](abm-setpos.md) 訊息來回應 cascade 或並排顯示的作業。</span><span class="sxs-lookup"><span data-stu-id="a0264-190">If an appbar hides itself in response to this message, it does not need to send the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages in response to the cascade or tile operation.</span></span>

## <a name="registering-an-application-desktop-toolbar"></a><span data-ttu-id="a0264-191">註冊應用程式桌面工具列</span><span class="sxs-lookup"><span data-stu-id="a0264-191">Registering an Application Desktop Toolbar</span></span>

<span data-ttu-id="a0264-192">應用程式必須藉由傳送 [**ABM 的 \_ 新**](abm-new.md) 訊息來註冊 appbar。</span><span class="sxs-lookup"><span data-stu-id="a0264-192">An application must register an appbar by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="a0264-193">註冊 appbar 會將它新增至系統的內部清單，並為系統提供訊息識別碼，以用來將通知訊息傳送至 appbar。</span><span class="sxs-lookup"><span data-stu-id="a0264-193">Registering an appbar adds it to the system's internal list and provides the system with a message identifier to use to send notification messages to the appbar.</span></span> <span data-ttu-id="a0264-194">在結束之前，應用程式必須藉由傳送 [**ABM \_ 移除**](abm-remove.md) 訊息來取消註冊 appbar。</span><span class="sxs-lookup"><span data-stu-id="a0264-194">Before exiting, an application must unregister the appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="a0264-195">取消註冊會從系統的內部清單中移除 appbar，並防止狀態列接收 appbar 通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-195">Unregistering removes the appbar from the system's internal list and prevents the bar from receiving appbar notification messages.</span></span>

<span data-ttu-id="a0264-196">下列範例中的函式會根據布林值旗標參數的值來註冊或取消註冊 appbar。</span><span class="sxs-lookup"><span data-stu-id="a0264-196">The function in the following example either registers or unregisters an appbar, depending on the value of a Boolean flag parameter.</span></span>


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a><span data-ttu-id="a0264-197">設定 Appbar 大小和位置</span><span class="sxs-lookup"><span data-stu-id="a0264-197">Setting the Appbar Size and Position</span></span>

<span data-ttu-id="a0264-198">應用程式應該在註冊 appbar 之後、使用者使用者移動或調整 appbar，以及每次 appbar 收到 [**ABN \_ POSCHANGED**](abn-poschanged.md) 通知訊息時，設定 appbar 的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="a0264-198">An application should set an appbar's size and position after registering the appbar, after the user user moves or sizes the appbar, and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="a0264-199">在設定 appbar 的大小和位置之前，應用程式會藉由傳送 [**ABM \_ QUERYPOS**](abm-querypos.md) 訊息，查詢系統是否有核准的周框。</span><span class="sxs-lookup"><span data-stu-id="a0264-199">Before setting the size and position of the appbar, the application queries the system for an approved bounding rectangle by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="a0264-200">系統會傳回不幹擾工作列或任何其他 appbar 的周框。</span><span class="sxs-lookup"><span data-stu-id="a0264-200">The system returns a bounding rectangle that does not interfere with the taskbar or any other appbar.</span></span> <span data-ttu-id="a0264-201">系統只會以矩形減法來調整矩形;這樣就不需要保留矩形的初始大小。</span><span class="sxs-lookup"><span data-stu-id="a0264-201">The system adjusts the rectangle purely by rectangle subtraction; it makes no effort to preserve the rectangle's initial size.</span></span> <span data-ttu-id="a0264-202">基於這個理由，appbar 應該會在傳送 **ABM \_ QUERYPOS** 之後，視需要重新調整矩形。</span><span class="sxs-lookup"><span data-stu-id="a0264-202">For this reason, the appbar should readjust the rectangle, as necessary, after sending **ABM\_QUERYPOS**.</span></span>

<span data-ttu-id="a0264-203">接下來，應用程式會使用 [**ABM \_ SETPOS**](abm-setpos.md) 訊息，將周框的矩形傳遞回系統。</span><span class="sxs-lookup"><span data-stu-id="a0264-203">Next, the application passes the bounding rectangle back to the system by using the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span> <span data-ttu-id="a0264-204">然後，它會呼叫 [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) 函式，將 appbar 移至位置。</span><span class="sxs-lookup"><span data-stu-id="a0264-204">Then it calls the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="a0264-205">下列範例顯示如何設定 appbar 的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="a0264-205">The following example shows how to set an appbar's size and position.</span></span>


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a><span data-ttu-id="a0264-206">處理 Appbar 通知訊息</span><span class="sxs-lookup"><span data-stu-id="a0264-206">Processing Appbar Notification Messages</span></span>

<span data-ttu-id="a0264-207">當全螢幕應用程式啟動 (或最後一個應用程式關閉) ，或是發生可能影響 appbar 大小和位置的事件時，appbar 會在工作列的狀態變更時收到通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-207">An appbar receives a notification message when the state of the taskbar changes, when a full-screen application starts (or the last one closes), or when an event occurs that can affect the appbar's size and position.</span></span> <span data-ttu-id="a0264-208">下列範例顯示如何處理各種通知訊息。</span><span class="sxs-lookup"><span data-stu-id="a0264-208">The following example shows how to process the various notification messages.</span></span>


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



<span data-ttu-id="a0264-209">下列函式會調整 appbar 的周框，然後呼叫上一節中所含的應用程式定義 AppBarQuerySetPos 函式 () 來據以設定橫條圖的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="a0264-209">The following function adjusts an appbar's bounding rectangle and then calls the application-defined AppBarQuerySetPos function (included in the previous section) to set the bar's size and position accordingly.</span></span>


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
