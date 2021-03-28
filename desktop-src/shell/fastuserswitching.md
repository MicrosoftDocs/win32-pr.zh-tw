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
# <a name="user-accounts-with-fast-user-switching-and-remote-desktop"></a>具有快速使用者切換和遠端桌面的使用者帳戶

Windows XP 使用者帳戶可讓多個使用者同時登入，每個使用者都有自己的設定，以及各自執行自己的應用程式。 因為一個使用者不需要登出以允許存取另一位使用者，所以可以使用快速使用者切換功能輕鬆地存取每個使用者的桌面。 使用者帳戶也包含個人終端機伺服器功能或遠端桌面，可讓使用者從遠端系統存取其桌面帳戶。

討論下列主題。

-   [基礎結構使用需求](#infrastructure-usage-requirements)
-   [與現有應用程式的相容性](#compatibility-with-existing-applications)
-   [註冊會話切換通知](#registering-for-session-switching-notification)
-   [確保您的應用程式只有一個實例正在執行](#ensuring-only-one-instance-of-your-application-is-running)
-   [在所有會話中關閉您的應用程式](#shutting-down-your-application-across-all-sessions)
-   [與系統服務的互動](#interaction-with-system-services)
-   [遠端桌面和頻寬](#remote-desktop-and-bandwidth)

## <a name="infrastructure-usage-requirements"></a>基礎結構使用需求

繼承自 Windows 2000 的基礎結構支援使用者資料、使用者設定和電腦設定的狀態分離。 利用此基礎結構，必須具備下列各項，才能在 Windows XP 下成功執行您的應用程式。

-   預設為用於儲存使用者建立之資料的 **我的檔** 資料夾。
-   正確分類和儲存應用程式資料。
-   在「拒絕存取」訊息上正常降級。

暫存檔案、記憶體對應檔案和檔都應該儲存在使用者設定檔目錄的適當子目錄中。 使用 [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) 或 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 來判斷這些檔案的適當儲存位置。 將 [**CSIDL \_ APPDATA**](csidl.md) 旗標傳遞給這些函式會傳回檔案系統目錄的路徑，做為應用程式特定資料的通用存放庫。 使用旗標 [**CSIDL \_ 本機 \_ APPDATA**](csidl.md) 取代在使用者變更時應變更之資料的 **CSIDL \_ APPDATA** ，例如暫存檔案。

以上所列的需求是 Microsoft 認證計畫中的子集。 如需詳細資訊，請參閱的 **Windows 認證程式** 頁面 https://www.microsoft.com/windowsserver2003/partners/isvs/cfw.mspx 。

## <a name="compatibility-with-existing-applications"></a>與現有應用程式的相容性

快速使用者切換和個人終端機伺服器都使用終端機服務技術，因此與大部分舊版的 Microsoft Win32 應用程式相容。 如果應用程式是符合 Windows 2000 標誌的規範，執行基本設定檔區隔和電源管理功能時，該應用程式應該會在個別的 Windows XP 使用者帳戶下正確執行。

## <a name="registering-for-session-switching-notification"></a>註冊會話切換通知

一般情況下，應用程式不需要在桌面切換時收到通知。 不過，當應用程式執行時，必須通知的應用程式是目前的桌面，例如存取序列埠或其他共用資源的應用程式，可以註冊桌面交換器通知。 若要註冊通知，請使用 [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification) 函數。

一旦呼叫該函式，就會註冊具有控制碼 *hWnd* 的視窗，以透過其 **WndProc** 函數接收 [**WM \_ WTSSESSION \_ 變更**](../termserv/wm-wtssession-change.md)訊息。 會話識別碼是在 **lParam** 參數中傳送，而程式碼表示產生訊息的事件是以下列其中一個旗標在 **wParam** 中傳送。

-   WTS \_ 主控台 \_ 連接
-   WTS \_ 主控台 \_ 中斷連線
-   WTS \_ 遠端 \_ 連接
-   WTS \_ 遠端 \_ 中斷連線
-   WTS \_ 會話 \_ 登出
-   WTS \_ 會話 \_ 登入

應用程式可以使用此訊息來追蹤其狀態，以及釋放和取得主控台專屬的資源。 使用者桌面可以在遠端和主控台控制之間動態切換。 應用程式應該使用 [**WM \_ WTSSESSION \_ 變更**](../termserv/wm-wtssession-change.md) 訊息來與遠端或本機連接狀態進行同步處理。

當您的進程不再需要這些通知或正在終止時，它應該呼叫 [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification) 來取消註冊其通知。

> [!IMPORTANT]
> 傳遞至 [**WTSRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsregistersessionnotification)的 **hWnd** 值為參考計數，因此您必須對 [**WTSUnRegisterSessionNotification**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)發出相等的呼叫數目，以確保釋放所有已配置的資源。

 

## <a name="ensuring-only-one-instance-of-your-application-is-running"></a>確保您的應用程式只有一個實例正在執行

許多應用程式必須確定它們只有一個實例正在執行。 在 Windows XP 中有幾種方法可以這麼做。 其中包括下列各項：

-   使用 [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) 或 [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) 來搜尋您應用程式開啟的已知視窗。 如果該視窗已經開啟，您可以使用它來表示應用程式已經在執行。
-   當您的應用程式開啟時，建立 mutex 或信號物件，並在應用程式終止時關閉該物件。 全域物件命名空間會為每個桌面分隔，允許每個桌面有唯一的 mutex 和信號物件清單。

## <a name="shutting-down-your-application-across-all-sessions"></a>在所有會話中關閉您的應用程式

應用程式可能需要在所有會話中自行關閉。 例如，在兩個或多個會話中執行的應用程式，可能會從 web 下載新的檔案。 然後，它可能需要關閉它，並以更新的位重新開機。 當然，這必須在所有執行中的會話中完成。 您應該撰寫應用程式，以便在收到通知時完全結束。

## <a name="interaction-with-system-services"></a>與系統服務的互動

從程式設計的觀點來看，必須解決下列情況。

-   伺服器進程會從用戶端進程收到直接要求。

    在此情況下，可能會使用本機程序呼叫來傳輸訊息 (LPC) 或 (RPC) 的遠端程序呼叫。 有適用于 LPC 或 RPC 的 Api，可讓您抓取用戶端權杖。 一旦取得用戶端權杖，伺服器就可以在 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)的呼叫中使用它。 如此一來，如果用戶端使用者權杖有會話標記，就會在正確的視窗站上啟動處理常式。

    > [!Note]  
    > [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 不支援在此時間處理跨會話的繼承。

     

-   伺服器進程會收到通知，而且需要顯示 UI，但顯示不一定要在目前使用者的內容中。

    在此情況下，伺服器進程可以複製其主要進程權杖，並變更有問題的會話識別碼，以符合目前的會話識別碼。 您可以使用 [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid) 函數來取得目前的會話識別碼。

    > [!Note]  
    > 若要設定權杖會話識別碼，您需要 **SE \_ TCB \_ 許可權**。 您只會將這項服務做為在 NT 授權單位系統中執行的服務 \\ 。

     

## <a name="remote-desktop-and-bandwidth"></a>遠端桌面和頻寬

透過將遠端桌面功能新增至 Windows XP，應用程式應該避免使用比所需更多的頻寬，並避免在遠端連線到桌面時產生大量的螢幕繪圖和動畫效果。 若要判斷目前的會話是否為遠端，您可以使用 **SM \_ REMOTESESSION** 呼叫 [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) 。 不過請注意，此呼叫並不區分遠端與中斷連線。

 

 
