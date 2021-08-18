---
description: 一般來說，服務是設計來在沒有圖形化使用者介面的情況下自動執行的主控台應用程式 (GUI) 。
ms.assetid: 3d6e090a-00b1-47d8-a4fb-620f3db8ba9c
title: 互動式服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6b99eb41d26d6740a30a314654d92fdd4522f5597ea6e4cbb2a3d443de8120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889466"
---
# <a name="interactive-services"></a>互動式服務

一般來說，服務是設計來在沒有圖形化使用者介面的情況下自動執行的主控台應用程式 (GUI) 。 不過，某些服務可能需要與使用者偶爾進行互動。 本頁面會討論從服務與使用者互動的最佳方式。

> [!IMPORTANT]
> 在 Windows Vista 中，服務無法直接與使用者互動。 因此，不應在新的程式碼中使用標題為使用互動式服務的章節中所述的技術。

 

## <a name="interacting-with-a-user-from-a-service-indirectly"></a>間接與來自服務的使用者互動

您可以使用下列技術，從所有支援的 Windows 版本上的服務與使用者互動：

-   使用 [**WTSSendMessage**](/windows/desktop/api/wtsapi32/nf-wtsapi32-wtssendmessagea) 函數在使用者的會話中顯示對話方塊。
-   建立個別隱藏的 GUI 應用程式，並使用 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函式在互動式使用者的內容中執行應用程式。 設計 GUI 應用程式，透過一些處理序間通訊的方法與服務通訊， (IPC) ，例如具名管道。 服務會與 GUI 應用程式通訊，以告訴它何時顯示 GUI。 應用程式會將使用者互動的結果傳達給服務，讓服務可以採取適當的動作。 請注意，除非您 (ACL) 使用適當的存取控制清單，否則 IPC 可以透過網路公開您的服務介面。

    如果此服務在多使用者的系統上執行，請將應用程式新增至下列機碼，以便在每個會話中執行： **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ run**。 如果應用程式使用具名管道進行 IPC，伺服器可以根據會話識別碼為每個管道提供唯一的名稱，以區別多個使用者進程。

下列技術也適用于 Windows Server 2003 和 Windows XP：

-   藉由呼叫 [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) 函式與 **MB \_ 服務 \_ 通知** 來顯示訊息方塊。 這是顯示簡單狀態訊息的建議。 除非您是從不同的執行緒呼叫 MessageBox，否則請勿在服務初始化期間或從 [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)常式呼叫 **MessageBox** ，如此您就可以及時返回 SCM。

## <a name="using-an-interactive-service"></a>使用互動式服務

依預設，服務會使用非互動式 [視窗站](/windows/desktop/winstation/window-stations) ，而且無法與使用者互動。 不過， *互動式服務* 可以顯示使用者介面，並接收使用者輸入。

> [!Caution]  
> 在較高的安全性內容中執行的服務（例如 LocalSystem 帳戶），不應該在互動式桌面上建立視窗，因為在互動式桌面上執行的任何其他應用程式都可以與此視窗互動。 這會將服務公開給登入使用者執行的任何應用程式。 此外，以 LocalSystem 身分執行的服務不應藉由呼叫 [**OpenWindowStation**](/windows/desktop/api/winuser/nf-winuser-openwindowstationa) 或 [**GetThreadDesktop**](/windows/desktop/api/winuser/nf-winuser-getthreaddesktop) 函數來存取互動式桌面。

 

若要建立互動式服務，請在呼叫 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函式時執行下列動作：

1.  針對 *lpServiceStartName* 參數指定 Null，以在 [LocalSystem 帳戶](localsystem-account.md)內容中執行服務。
2.  指定 **服務 \_ 互動式 \_ 進程** 旗標。

若要判斷服務是否以互動式服務的形式執行，請呼叫 [**GetProcessWindowStation**](/windows/desktop/api/winuser/nf-winuser-getprocesswindowstation) 函式以抓取視窗工作站的控制碼，並使用 [**GetUserObjectInformation**](/windows/desktop/api/winuser/nf-winuser-getuserobjectinformationa) 函式來測試視窗工作站是否具有 **w2kmiguser.wsf \_ 可見** 的屬性。

不過請注意，下列登錄機碼包含值 **NoInteractiveServices**，可控制服務 \_ 互動式進程的效果 \_ ：

**HKEY \_ 本機 \_ 電腦 \\ SYSTEM \\ CurrentControlSet \\ Control \\ Windows**

**NoInteractiveServices** 值預設為1，表示不允許任何服務以互動方式執行，不論它是否有 **服務 \_ 互動式 \_ 進程**。 當 **NoInteractiveServices** 設為0時，會允許具有 **服務 \_ 互動式 \_ 進程** 的服務以互動方式執行。

**Windows 7、Windows server 2008 R2、Windows XP 和 Windows Server 2003：****NoInteractiveServices** 值的預設值為0，這表示具有 **服務 \_ 互動式 \_ 進程** 的服務允許以互動方式執行。 當 **NoInteractiveServices** 設定為非零值時，就不會在之後啟動任何服務，不論它是否有 **服務 \_ 互動式 \_ 進程**。

> [!IMPORTANT]
> 所有服務都會在終端機服務會話0中執行。 因此，如果互動式服務顯示使用者介面，只有連接到會話0的使用者才會看到它。 因為無法保證互動式使用者已連線到會話0，所以請勿將服務設定為在終端機服務或支援快速切換使用者的系統上以互動式服務的形式執行， (使用終端機服務) 來執行快速使用者切換。

 

 

 
