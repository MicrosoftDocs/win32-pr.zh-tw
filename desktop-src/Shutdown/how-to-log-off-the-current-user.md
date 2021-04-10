---
description: 下列範例會使用 ExitWindows 函數來登出目前的使用者。
ms.assetid: 74be3505-c4bd-4ae2-aaed-700382839006
title: 如何登出目前的使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e59ce625ae7da8a2a4a901fbb1429ab0f9b638c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944217"
---
# <a name="how-to-log-off-the-current-user"></a>如何登出目前的使用者

下列範例會使用 [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) 函數來登出目前的使用者。

``` syntax
// Log off the current user. 

ExitWindows(0, 0);
```

下列範例會使用 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 函數來登出目前的使用者。

``` syntax
// Log off the current user. 

ExitWindowsEx(EWX_LOGOFF, 0);
```

應用程式會收到 [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) 訊息，並顯示對話方塊詢問是否確定要結束會話。 如果使用者按一下 [ **是]**，系統就會登出使用者。 如果使用者按一下 [ **否**]，就會取消登出。

``` syntax
// Process the message in the window procedure. 

case WM_QUERYENDSESSION:  
{ 
    int r; 
    r = MessageBox(NULL,(LPCWSTR)L"End the session?",(LPCWSTR)L"WM_QUERYENDSESSION",MB_YESNO);
 
    // Return TRUE to continue, FALSE to stop. 
 
    return r == IDYES; 
    break; 
}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[登出](logging-off.md)
</dt> </dl>

 

 



