---
description: Winlogon 通知套件是一個 DLL，可匯出處理 Winlogon 事件的函式。 例如，當使用者登入系統時，Winlogon 會呼叫每個通知套件的登入事件處理常式函式，以提供事件的相關資訊。
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: 建立 Winlogon 通知套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c84d0290f7afeba7a427f5c50caf1638fd88bfdb4b52ee513a9b1c0506aed9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008866"
---
# <a name="creating-a-winlogon-notification-package"></a>建立 Winlogon 通知套件

[*Winlogon*](/windows/desktop/SecGloss/w-gly)通知套件是一個 DLL，可匯出處理 Winlogon 事件的函式。 例如，當使用者登入系統時，Winlogon 會呼叫每個通知套件的登入事件處理常式函式，以提供事件的相關資訊。

在通知套件中執行的事件處理常式函式的名稱會保留給開發人員;Winlogon 會檢查登錄來取得事件處理常式函式的名稱。 例如，一個通知套件可能會執行 logon 事件處理常式函式， `WLEventLogon` 而另一個則可能使用 `HandleLogonEvent` 。

您不需要針對每個 Winlogon 事件（僅適用于您的應用程式有用的事件）來執行和註冊事件處理常式。 每個事件處理常式函數都必須使用 [事件處理常式](event-handler-function-prototype.md)函式原型中所述的函式原型。 此原型具有單一參數： [**WLX \_ 通知 \_ 資訊**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) 結構，其中包含事件的詳細資料。

Winlogon 會忽略事件處理常式函數的輸出。 如果處理事件需要與 Winlogon 互動，請使用 [Winlogon 支援功能](authentication-functions.md)。

若要使用 Winlogon 通知套件，必須將 DLL 複製到% SystemRoot% \\ system32 資料夾，並且必須針對通知套件進行登錄更新。 如需登錄更新的詳細資訊，請參閱 [註冊 Winlogon 通知套件](registering-a-winlogon-notification-package.md)。

 

 
