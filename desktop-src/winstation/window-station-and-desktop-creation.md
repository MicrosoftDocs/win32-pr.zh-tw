---
title: 視窗工作站和桌面建立
description: 系統會自動建立互動式視窗工作站。
ms.assetid: 5b908cb6-3a72-4afc-aed0-8411e8d0888f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52a3cc85a3194bea6c8eaea00a7ce794901426e794c962e1b23713561f8fc744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030514"
---
# <a name="window-station-and-desktop-creation"></a>視窗工作站和桌面建立

系統會自動建立互動式視窗工作站。 當互動式使用者登入時，系統會將互動式視窗工作站與使用者登入會話產生關聯。 系統也會為互動式視窗工作站建立預設的輸入桌面 (Winsta0 \\ 預設) 。 由登入的使用者啟動的進程會與 Winsta0 \\ 預設桌面相關聯。

進程可以使用 [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) 函式來建立新的視窗工作站，並使用 **CreateDesktop** 或 [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) 函式來建立新的桌面。 可以建立的桌面數目受限於系統桌面堆積的大小。 如需詳細資訊，請參閱 [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)。

當非互動式進程（例如服務應用程式）嘗試連接到視窗工作站，而進程登入會話沒有任何視窗工作站時，系統會嘗試建立會話的視窗工作站和桌面。 所建立之視窗工作站的名稱是以登入會話識別碼為基礎，而桌面名為預設值，如下所述：

-   如果服務是在 LocalSystem 帳戶的安全性內容中執行，但是未包含服務 \_ 互動式 \_ 進程屬性，它會使用下列視窗站和 desktop： 3e7 $ \\ default。 此視窗站並非互動式，因此服務無法顯示使用者介面。 此外，服務所建立的進程也無法顯示使用者介面。
-   如果服務是在使用者帳戶的安全性內容中執行，則視窗工作站的名稱是以使用者 SID 服務-0x *Z1* - *Z2*$ 為基礎，其中 *Z1* 是登入 sid 的最高部分，而 *Z2* 是登入 sid 的低部分。 由於 SID 對登入會話而言是唯一的，因此在相同安全性內容中執行的兩個服務會接收唯一的視窗工作站。 這些視窗站並非互動式。

適用于 windows 工作站和桌面的任意存取控制清單 (DACL) 包含下列服務使用者帳戶的存取權限：

視窗站：

<dl> WINSTA \_ ACCESSCLIPBOARD  
WINSTA \_ ACCESSGLOBALATOMS  
WINSTA \_ CREATEDESKTOP  
WINSTA \_ EXITWINDOWS  
WINSTA \_ READATTRIBUTES  
\_需要標準許可權 \_  
</dl>

桌上型電腦：

<dl> 桌面 \_ CREATEMENU  
電腦 \_ CREATEWINDOW  
桌面 \_ 列舉  
桌面 \_ HOOKCONTROL  
桌面 \_ READOBJECTS  
桌面 \_ WRITEOBJECTS  
\_需要標準許可權 \_  
</dl>

 

 