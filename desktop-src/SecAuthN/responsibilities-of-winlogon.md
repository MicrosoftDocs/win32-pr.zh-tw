---
description: 列出並說明 Winlogon 的責任。
ms.assetid: 5aef4164-11bd-4acc-b851-de982e35d2b5
title: Winlogon 的責任
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6561bea11c48eb474c0ff56c5c0aa5ebfa0c22d9d6689aa55a6a208bbbc683e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919026"
---
# <a name="responsibilities-of-winlogon"></a>Winlogon 的責任

[*Winlogon*](../secgloss/w-gly.md) 具有下列責任：

-   視窗站和桌上型電腦保護

    Winlogon 會設定視窗工作站和對應桌面的保護，以確保每一個都能正確存取。 一般而言，這表示本機系統將擁有這些物件的完整存取權，而且以互動方式登入的使用者將擁有視窗站物件的讀取權限，以及應用程式桌面物件的完整存取權。

-   標準 SAS 辨識

    Winlogon 在 User32 伺服器中有特殊的勾點，可讓它監視 CTRL + ALT + DEL [*安全的注意順序*](../secgloss/s-gly.md) (SAS) 事件。 Winlogon 會將此 SAS 事件資訊提供給 Gina 使用，以作為 SAS 或其 SAS 的一部分。 一般而言，Gina 應該自行監視 SASs;不過，任何具有標準 CTRL + ALT + DEL SAS 作為其辨識 SASs 的 [*GINA*](../secgloss/g-gly.md) ，都應該使用針對此用途所提供的 Winlogon 支援。

-   SAS 例行分派

    當 Winlogon 遇到 SAS 事件或 GINA 提供 SAS 給 Winlogon 時，Winlogon 會據以設定狀態、對 Winlogon 桌面的變更，以及呼叫 GINA 的其中一個 SAS 處理函式。

-   使用者設定檔載入

    當使用者登入時，其使用者設定檔會載入至登錄中。 如此一來，使用者的處理常式就可以使用特殊的登錄機碼 HKEY \_ 目前的 \_ 使用者。 Winlogon 會在成功登入之後，但在啟用新登入使用者的 shell 之前自動執行這項操作。

-   將安全性指派給使用者 shell

    當使用者登入時，GINA 會負責為該使用者建立一或多個初始進程。 Winlogon 會為 GINA 提供支援功能，以將新登入之使用者的安全性套用至這些處理常式。 不過，最好的方法是讓 GINA 呼叫 Windows 函式 [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)，並讓系統提供服務。

-   螢幕保護裝置控制項

    Winlogon 會監視鍵盤和滑鼠活動，以決定何時要啟動畫面保護。 啟用螢幕保護裝置之後，Winlogon 會繼續監視鍵盤和滑鼠活動，以判斷何時終止螢幕保護裝置。 如果螢幕保護裝置標示為安全，則 Winlogon 會將工作站視為鎖定。 當有滑鼠或鍵盤活動時，Winlogon 會叫用 GINA 的 [**WlxDisplayLockedNotice**](/windows/desktop/api/Winwlx/nf-winwlx-wlxdisplaylockednotice) 函式，而鎖定的工作站行為會繼續。 如果螢幕保護裝置不安全，任何鍵盤或滑鼠活動都會終止螢幕保護裝置，而不會通知 GINA。

-   多個網路提供者支援

    安裝在 Windows 系統上的多個網路可以包含在驗證程式和密碼更新作業中。 這項包含可讓其他網路在正常登入期間，使用 Winlogon 的安全桌面，同時收集識別和驗證資訊。 Gina 可供您明確支援這些額外網路提供者的 Winlogon 服務中所需的某些參數。

 

 
