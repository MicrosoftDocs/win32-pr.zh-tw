---
title: 桌上型電腦
description: 桌面具有邏輯顯示介面，且包含使用者介面物件，例如 windows、功能表和勾點;可以用來建立和管理 windows。
ms.assetid: c56cd63b-c260-40d0-9a62-1dee1eb18679
keywords:
- 桌面物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b763c05c3d45c701da0bdd606fa906dec3f8af07ce72d256b402e7df5d9319b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587348"
---
# <a name="desktops"></a>桌上型電腦

*桌面* 具有邏輯顯示介面，且包含使用者介面物件，例如 windows、功能表和勾點;可以用來建立和管理 windows。 每個桌面物件都是安全物件。 建立桌面時，它會與目前呼叫進程的 [視窗站](window-stations.md) 相關聯，並指派給呼叫的執行緒。

視窗訊息只能在相同桌面上的進程之間傳送。 此外，在特定桌上型電腦上執行之處理常式的攔截程式，只能接收在相同桌面上建立之 windows 的訊息。

您可以建立與互動式視窗工作站 Winsta0 相關聯的桌面，以顯示使用者介面並接收使用者輸入，但一次只能有一部桌上型電腦處於作用中狀態。 此作用中的桌面（也稱為 *輸入桌面*）是使用者目前看到的使用者，以及接收使用者輸入的桌面。 應用程式可以使用 [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) 函式來取得輸入桌面的控制碼。 具有必要存取權的應用程式可以使用 [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) 函數來指定不同的輸入桌面。

根據預設，互動式視窗工作站中有三個桌面：預設、螢幕保護裝置和 Winlogon。

當 Winlogon 以登入的使用者身分啟動初始進程時，就會建立預設桌面。 屆時，預設桌面會變成作用中狀態，並用來與使用者互動。

當安全的螢幕保護裝置啟動時，系統會自動切換到螢幕保護裝置程式桌面，以防止未經授權的使用者使用預設桌面上的進程。 不安全的螢幕保護裝置會在 Winsta0 預設上執行 \\ 。

當使用者登入時，Winlogon 桌面會處於作用中狀態。 當 shell 指出它已準備好顯示某個東西，或30秒後（以先發生者為准）時，系統會切換至預設桌面。 在使用者會話期間，當使用者按下 CTRL + ALT + DEL 鍵序列，或開啟 [使用者帳戶控制] (UAC) ] 對話方塊時，系統會切換至 Winlogon 桌面。

**Windows Server 2003 和 Windows XP/2000：** 不支援 UAC 對話方塊。

Winlogon 桌面的安全描述項允許存取一組非常受限制的帳戶，包括 [LocalSystem 帳戶](/windows/desktop/Services/localsystem-account)。 應用程式通常不會在其權杖中攜帶任何這些帳戶的 Sid，因此無法存取 Winlogon 桌面或在 Winlogon 桌面作用中時切換至不同的桌面。

如需詳細資訊，請參閱下列主題：

-   [視窗工作站和桌面建立](window-station-and-desktop-creation.md)
-   [與桌面的執行緒連接](thread-connection-to-a-desktop.md)
-   [桌面安全性與存取權限](desktop-security-and-access-rights.md)

 

 