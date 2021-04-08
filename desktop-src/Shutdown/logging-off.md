---
description: ExitWindows 函式會將目前的使用者登出。 您也可以使用 EXW 登出旗標來呼叫 ExitWindowsEx 函數 \_ 。
ms.assetid: 906d92f1-7cbe-454e-9c71-34b4383aebab
title: 登出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0571c0522c494acd763d57dcae8d200125cd53d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103853116"
---
# <a name="logging-off"></a>登出

[**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)函式會將目前的使用者登出。 您也可以使用 EXW 登出旗標來呼叫 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 函數 \_ 。

根據預設，當應用程式使用 [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) 或 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 來登出時，系統會將 [**WM \_ QUERYENDSESSION**](wm-queryendsession.md) 訊息傳送至每個視窗。 應用程式在收到此訊息時，會傳回 **TRUE** 來同意終止。 如果任何應用程式在處理此訊息時傳回 **FALSE** ，就會取消登出作業。 如果您的應用程式會處理 **WM \_ QUERYENDSESSION** 訊息，您可以允許使用者取消登出作業，即使另一個應用程式或系統產生了端對端會話的要求也是一樣。 如需範例，請參閱 [如何登出目前的使用者](how-to-log-off-the-current-user.md)。

當應用程式針對 [**wm \_ QUERYENDSESSION**](wm-queryendsession.md)傳回 **TRUE** 時，無論其他應用程式如何回應 **wm \_ QUERYENDSESSION** 訊息，它都會收到 [**wm \_ ENDSESSION**](wm-endsession.md)訊息並將它終止。

若要強制所有應用程式終止，請使用 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)，並指定 EXW \_ force 旗標。 這可防止系統傳送 [**WM 的 \_ QUERYENDSESSION**](wm-queryendsession.md) 訊息。

系統也會在登出作業期間，將 CTRL \_ 登出 \_ 事件控制信號傳送至每個進程。 主控台應用程式可以註冊 [**HandlerRoutine**](/windows/console/handlerroutine) 來處理這些訊息。

如果呼叫 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 的進程在互動式使用者的登入會話中執行，登入會話中的所有處理常式都會終止。 如果呼叫 **ExitWindowsEx** 的進程在其他登入會話中，則只會發出通知;沒有進程終止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何登出目前的使用者](how-to-log-off-the-current-user.md)
</dt> </dl>

 

 
