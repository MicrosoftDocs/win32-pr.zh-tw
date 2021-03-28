---
description: Windows XP 使用者帳戶可讓多個使用者同時登入，每個使用者都有自己的設定，以及各自執行自己的應用程式。
ms.assetid: bc404afc-f73e-404d-854d-faab5cf205a5
title: 具有快速使用者切換和遠端桌面的使用者帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc26471bcf56efce79fb5ccc91a78c24e43ae312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991607"
---
# <a name="user-accounts-with-fast-user-switching-and-remote-desktop"></a><span data-ttu-id="cdb3b-103">具有快速使用者切換和遠端桌面的使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="cdb3b-103">User Accounts with Fast User Switching and Remote Desktop</span></span>

<span data-ttu-id="cdb3b-104">Windows XP 使用者帳戶可讓多個使用者同時登入，每個使用者都有自己的設定，以及各自執行自己的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-104">Windows XP user accounts enable multiple users to be logged on simultaneously, each with his or her own settings and each running his or her own applications.</span></span> <span data-ttu-id="cdb3b-105">因為一個使用者不需要登出以允許存取另一位使用者，所以可以使用快速使用者切換功能輕鬆地存取每個使用者的桌面。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-105">Because one user does not have to log off to allow access to another user, each user's desktop is easily accessed using the fast user switching feature.</span></span> <span data-ttu-id="cdb3b-106">使用者帳戶也包含個人終端機伺服器功能或遠端桌面，可讓使用者從遠端系統存取其桌面帳戶。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-106">User accounts also include the Personal Terminal Server feature, or Remote Desktop, which enables users to access their desktop account from remote systems.</span></span>

<span data-ttu-id="cdb3b-107">討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-107">The following topics are discussed.</span></span>

-   [<span data-ttu-id="cdb3b-108">基礎結構使用需求</span><span class="sxs-lookup"><span data-stu-id="cdb3b-108">Infrastructure Usage Requirements</span></span>](#infrastructure-usage-requirements)
-   [<span data-ttu-id="cdb3b-109">與現有應用程式的相容性</span><span class="sxs-lookup"><span data-stu-id="cdb3b-109">Compatibility with Existing Applications</span></span>](#compatibility-with-existing-applications)
-   [<span data-ttu-id="cdb3b-110">註冊會話切換通知</span><span class="sxs-lookup"><span data-stu-id="cdb3b-110">Registering for Session Switching Notification</span></span>](#registering-for-session-switching-notification)
-   [<span data-ttu-id="cdb3b-111">確保您的應用程式只有一個實例正在執行</span><span class="sxs-lookup"><span data-stu-id="cdb3b-111">Ensuring Only One Instance of Your Application Is Running</span></span>](#ensuring-only-one-instance-of-your-application-is-running)
-   [<span data-ttu-id="cdb3b-112">在所有會話中關閉您的應用程式</span><span class="sxs-lookup"><span data-stu-id="cdb3b-112">Shutting Down Your Application Across All Sessions</span></span>](#shutting-down-your-application-across-all-sessions)
-   [<span data-ttu-id="cdb3b-113">與系統服務的互動</span><span class="sxs-lookup"><span data-stu-id="cdb3b-113">Interaction with System Services</span></span>](#interaction-with-system-services)
-   [<span data-ttu-id="cdb3b-114">遠端桌面和頻寬</span><span class="sxs-lookup"><span data-stu-id="cdb3b-114">Remote Desktop and Bandwidth</span></span>](#remote-desktop-and-bandwidth)

## <a name="infrastructure-usage-requirements"></a><span data-ttu-id="cdb3b-115">基礎結構使用需求</span><span class="sxs-lookup"><span data-stu-id="cdb3b-115">Infrastructure Usage Requirements</span></span>

<span data-ttu-id="cdb3b-116">繼承自 Windows 2000 的基礎結構支援使用者資料、使用者設定和電腦設定的狀態分離。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-116">Underlying infrastructure inherited from Windows 2000 supports state separation of user data, user settings, and computer settings.</span></span> <span data-ttu-id="cdb3b-117">利用此基礎結構，必須具備下列各項，才能在 Windows XP 下成功執行您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-117">Taking advantage of this infrastructure, the following are required to successfully run your application under Windows XP.</span></span>

-   <span data-ttu-id="cdb3b-118">預設為用於儲存使用者建立之資料的 **我的檔** 資料夾。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-118">Default to the **My Documents** folder for storage of user-created data.</span></span>
-   <span data-ttu-id="cdb3b-119">正確分類和儲存應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-119">Classify and store application data correctly.</span></span>
-   <span data-ttu-id="cdb3b-120">在「拒絕存取」訊息上正常降級。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-120">Degrade gracefully on "Access Denied" messages.</span></span>

<span data-ttu-id="cdb3b-121">暫存檔案、記憶體對應檔案和檔都應該儲存在使用者設定檔目錄的適當子目錄中。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-121">Temporary files, memory-mapped files, and documents should all be stored in the appropriate subdirectory of the user's profile directory.</span></span> <span data-ttu-id="cdb3b-122">使用 [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) 或 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 來判斷這些檔案的適當儲存位置。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-122">Use [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) or [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) to determine the appropriate storage location for these files.</span></span> <span data-ttu-id="cdb3b-123">將 [**CSIDL \_ APPDATA**](csidl.md) 旗標傳遞給這些函式會傳回檔案系統目錄的路徑，做為應用程式特定資料的通用存放庫。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-123">Passing the [**CSIDL\_APPDATA**](csidl.md) flag to these functions returns the path of a file system directory that serves as a common repository for application-specific data.</span></span> <span data-ttu-id="cdb3b-124">使用旗標 [**CSIDL \_ 本機 \_ APPDATA**](csidl.md) 取代在使用者變更時應變更之資料的 **CSIDL \_ APPDATA** ，例如暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-124">Use the flag [**CSIDL\_LOCAL\_APPDATA**](csidl.md) in place of **CSIDL\_APPDATA** for data that should change when the user changes, such as temporary files.</span></span>

<span data-ttu-id="cdb3b-125">以上所列的需求是 Microsoft 認證計畫中的子集。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-125">The requirements listed above are a subset of those in the Microsoft Certification program.</span></span> <span data-ttu-id="cdb3b-126">如需詳細資訊，請參閱的 **Windows 認證程式** 頁面 https://www.microsoft.com/windowsserver2003/partners/isvs/cfw.mspx 。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-126">For more information, see the **Certified for Windows Program** page at https://www.microsoft.com/windowsserver2003/partners/isvs/cfw.mspx.</span></span>

## <a name="compatibility-with-existing-applications"></a><span data-ttu-id="cdb3b-127">與現有應用程式的相容性</span><span class="sxs-lookup"><span data-stu-id="cdb3b-127">Compatibility with Existing Applications</span></span>

<span data-ttu-id="cdb3b-128">快速使用者切換和個人終端機伺服器都使用終端機服務技術，因此與大部分舊版的 Microsoft Win32 應用程式相容。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-128">Both fast user switching and Personal Terminal Server use Terminal Services technology and therefore are compatible with most earlier Microsoft Win32 applications.</span></span> <span data-ttu-id="cdb3b-129">如果應用程式是符合 Windows 2000 標誌的規範，執行基本設定檔區隔和電源管理功能時，該應用程式應該會在個別的 Windows XP 使用者帳戶下正確執行。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-129">If an application is Windows 2000 Logo compliant, implementing basic profile separation and power management features, that application should run properly under individual Windows XP user accounts.</span></span>

## <a name="registering-for-session-switching-notification"></a><span data-ttu-id="cdb3b-130">註冊會話切換通知</span><span class="sxs-lookup"><span data-stu-id="cdb3b-130">Registering for Session Switching Notification</span></span>

<span data-ttu-id="cdb3b-131">一般情況下，應用程式不需要在桌面切換時收到通知。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-131">Typically, an application does not need to be notified when a desktop switch occurs.</span></span> <span data-ttu-id="cdb3b-132">不過，當應用程式執行時，必須通知的應用程式是目前的桌面，例如存取序列埠或其他共用資源的應用程式，可以註冊桌面交換器通知。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-132">However, applications that must be notified when the account under which they are running is the current desktop, such as applications that access the serial port or other shared resources, can register for desktop switch notification.</span></span> <span data-ttu-id="cdb3b-133">若要註冊通知，請使用 [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) 函數。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-133">To register for a notification, use the [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) function.</span></span>

<span data-ttu-id="cdb3b-134">一旦呼叫該函式，就會註冊具有控制碼 *hWnd* 的視窗，以透過其 **WndProc** 函數接收 [**WM \_ WTSSESSION \_ 變更**](../termserv/wm-wtssession-change.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-134">Once that function has been called, the window with handle *hWnd* is registered to receive a [**WM\_WTSSESSION\_CHANGE**](../termserv/wm-wtssession-change.md) message through its **WndProc** function.</span></span> <span data-ttu-id="cdb3b-135">會話識別碼是在 **lParam** 參數中傳送，而程式碼表示產生訊息的事件是以下列其中一個旗標在 **wParam** 中傳送。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-135">The session ID is sent in the **lParam** parameter, and a code that indicates the event that generated the message is sent in **wParam** as one of the following flags.</span></span>

-   <span data-ttu-id="cdb3b-136">WTS \_ 主控台 \_ 連接</span><span class="sxs-lookup"><span data-stu-id="cdb3b-136">WTS\_CONSOLE\_CONNECT</span></span>
-   <span data-ttu-id="cdb3b-137">WTS \_ 主控台 \_ 中斷連線</span><span class="sxs-lookup"><span data-stu-id="cdb3b-137">WTS\_CONSOLE\_DISCONNECT</span></span>
-   <span data-ttu-id="cdb3b-138">WTS \_ 遠端 \_ 連接</span><span class="sxs-lookup"><span data-stu-id="cdb3b-138">WTS\_REMOTE\_CONNECT</span></span>
-   <span data-ttu-id="cdb3b-139">WTS \_ 遠端 \_ 中斷連線</span><span class="sxs-lookup"><span data-stu-id="cdb3b-139">WTS\_REMOTE\_DISCONNECT</span></span>
-   <span data-ttu-id="cdb3b-140">WTS \_ 會話 \_ 登出</span><span class="sxs-lookup"><span data-stu-id="cdb3b-140">WTS\_SESSION\_LOGOFF</span></span>
-   <span data-ttu-id="cdb3b-141">WTS \_ 會話 \_ 登入</span><span class="sxs-lookup"><span data-stu-id="cdb3b-141">WTS\_SESSION\_LOGON</span></span>

<span data-ttu-id="cdb3b-142">應用程式可以使用此訊息來追蹤其狀態，以及釋放和取得主控台專屬的資源。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-142">Applications can use this message to track their state, as well as to release and acquire console-specific resources.</span></span> <span data-ttu-id="cdb3b-143">使用者桌面可以在遠端和主控台控制之間動態切換。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-143">User desktops can be dynamically switched between remote and console control.</span></span> <span data-ttu-id="cdb3b-144">應用程式應該使用 [**WM \_ WTSSESSION \_ 變更**](../termserv/wm-wtssession-change.md) 訊息來與遠端或本機連接狀態進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-144">Applications should use the [**WM\_WTSSESSION\_CHANGE**](../termserv/wm-wtssession-change.md) message to synchronize with the remote or local connection state.</span></span>

<span data-ttu-id="cdb3b-145">當您的進程不再需要這些通知或正在終止時，它應該呼叫 [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) 來取消註冊其通知。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-145">When your process no longer requires these notifications or is terminating, it should call [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) to unregister its notification.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cdb3b-146">傳遞至 [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification)的 **hWnd** 值為參考計數，因此您必須對 [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)發出相等的呼叫數目，以確保釋放所有已配置的資源。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-146">The **hWnd** values passed to [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) are reference counted, so you must make an equal number of calls to [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) to ensure the release of all allocated resources.</span></span>

 

## <a name="ensuring-only-one-instance-of-your-application-is-running"></a><span data-ttu-id="cdb3b-147">確保您的應用程式只有一個實例正在執行</span><span class="sxs-lookup"><span data-stu-id="cdb3b-147">Ensuring Only One Instance of Your Application Is Running</span></span>

<span data-ttu-id="cdb3b-148">許多應用程式必須確定它們只有一個實例正在執行。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-148">Many applications must ensure that they have only one instance running.</span></span> <span data-ttu-id="cdb3b-149">在 Windows XP 中有幾種方法可以這麼做。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-149">There are several ways to do this in Windows XP.</span></span> <span data-ttu-id="cdb3b-150">其中包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="cdb3b-150">Among them are the following:</span></span>

-   <span data-ttu-id="cdb3b-151">使用 [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) 或 [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) 來搜尋您應用程式開啟的已知視窗。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-151">Use [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) or [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) to search for a known window that your application opens.</span></span> <span data-ttu-id="cdb3b-152">如果該視窗已經開啟，您可以使用它來表示應用程式已經在執行。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-152">If that window is already open, you can use that as an indication that the application is already running.</span></span>
-   <span data-ttu-id="cdb3b-153">當您的應用程式開啟時，建立 mutex 或信號物件，並在應用程式終止時關閉該物件。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-153">Create a mutex or semaphore object when your application is opened, and close that object when the application terminates.</span></span> <span data-ttu-id="cdb3b-154">全域物件命名空間會為每個桌面分隔，允許每個桌面有唯一的 mutex 和信號物件清單。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-154">The global object namespace is separated for each desktop, allowing a unique list of mutex and semaphore objects for each.</span></span>

## <a name="shutting-down-your-application-across-all-sessions"></a><span data-ttu-id="cdb3b-155">在所有會話中關閉您的應用程式</span><span class="sxs-lookup"><span data-stu-id="cdb3b-155">Shutting Down Your Application Across All Sessions</span></span>

<span data-ttu-id="cdb3b-156">應用程式可能需要在所有會話中自行關閉。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-156">An application might need to shut itself down across all sessions.</span></span> <span data-ttu-id="cdb3b-157">例如，在兩個或多個會話中執行的應用程式，可能會從 web 下載新的檔案。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-157">For example, an application running in two or more sessions simultaneously might download a new file from the web.</span></span> <span data-ttu-id="cdb3b-158">然後，它可能需要關閉它，並以更新的位重新開機。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-158">Then it might need to close itself and restart with the updated bits.</span></span> <span data-ttu-id="cdb3b-159">當然，這必須在所有執行中的會話中完成。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-159">This, of course, would need to be done in all running sessions.</span></span> <span data-ttu-id="cdb3b-160">您應該撰寫應用程式，以便在收到通知時完全結束。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-160">Your application should be written so that it exits cleanly when a notification is received.</span></span>

## <a name="interaction-with-system-services"></a><span data-ttu-id="cdb3b-161">與系統服務的互動</span><span class="sxs-lookup"><span data-stu-id="cdb3b-161">Interaction with System Services</span></span>

<span data-ttu-id="cdb3b-162">從程式設計的觀點來看，必須解決下列情況。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-162">From a programmatic standpoint, the following cases need to be addressed.</span></span>

-   <span data-ttu-id="cdb3b-163">伺服器進程會從用戶端進程收到直接要求。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-163">The server process receives a direct request from a client process.</span></span>

    <span data-ttu-id="cdb3b-164">在此情況下，可能會使用本機程序呼叫來傳輸訊息 (LPC) 或 (RPC) 的遠端程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-164">In this case, the message is probably transmitted using a local procedure call (LPC) or a remote procedure call (RPC).</span></span> <span data-ttu-id="cdb3b-165">有適用于 LPC 或 RPC 的 Api，可讓您抓取用戶端權杖。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-165">There are APIs for either LPC or RPC that enable retrieval of the client token.</span></span> <span data-ttu-id="cdb3b-166">一旦取得用戶端權杖，伺服器就可以在 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)的呼叫中使用它。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-166">Once the client token is obtained, the server can use it in a call to [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera).</span></span> <span data-ttu-id="cdb3b-167">如此一來，如果用戶端使用者權杖有會話標記，就會在正確的視窗站上啟動處理常式。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-167">This brings up the process on the correct window station, assuming that the client user token has a session tag, which it should.</span></span>

    > [!Note]  
    > <span data-ttu-id="cdb3b-168">[**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 不支援在此時間處理跨會話的繼承。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-168">[**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) does not support handle inheritance across sessions at this time.</span></span>

     

-   <span data-ttu-id="cdb3b-169">伺服器進程會收到通知，而且需要顯示 UI，但顯示不一定要在目前使用者的內容中。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-169">The server process receives a notification and needs to display the UI, but the display does not have to be in the current user's context.</span></span>

    <span data-ttu-id="cdb3b-170">在此情況下，伺服器進程可以複製其主要進程權杖，並變更有問題的會話識別碼，以符合目前的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-170">In this case, the server process can duplicate its primary process token and change the session identifier in question to match the current session identifier.</span></span> <span data-ttu-id="cdb3b-171">您可以使用 [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid) 函數來取得目前的會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-171">The current session identifier can be obtained by using the [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid) function.</span></span>

    > [!Note]  
    > <span data-ttu-id="cdb3b-172">若要設定權杖會話識別碼，您需要 **SE \_ TCB \_ 許可權**。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-172">To set the token session ID, you need the **SE\_TCB\_PRIVILEGE**.</span></span> <span data-ttu-id="cdb3b-173">您只會將這項服務做為在 NT 授權單位系統中執行的服務 \\ 。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-173">You will have this only as a service running in NT AUTHORITY\\SYSTEM.</span></span>

     

## <a name="remote-desktop-and-bandwidth"></a><span data-ttu-id="cdb3b-174">遠端桌面和頻寬</span><span class="sxs-lookup"><span data-stu-id="cdb3b-174">Remote Desktop and Bandwidth</span></span>

<span data-ttu-id="cdb3b-175">透過將遠端桌面功能新增至 Windows XP，應用程式應該避免使用比所需更多的頻寬，並避免在遠端連線到桌面時產生大量的螢幕繪圖和動畫效果。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-175">With the addition of the Remote Desktop feature to Windows XP, applications should make an effort not to use more bandwidth than needed, avoiding extensive screen drawings and animation effects if the desktop is connected remotely.</span></span> <span data-ttu-id="cdb3b-176">若要判斷目前的會話是否為遠端，您可以使用 **SM \_ REMOTESESSION** 呼叫 [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) 。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-176">To determine whether the current session is remote, you can call [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with **SM\_REMOTESESSION**.</span></span> <span data-ttu-id="cdb3b-177">不過請注意，此呼叫並不區分遠端與中斷連線。</span><span class="sxs-lookup"><span data-stu-id="cdb3b-177">Be aware, however, that this call does not distinguish between remote and disconnected.</span></span>

 

 
