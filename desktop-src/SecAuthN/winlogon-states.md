---
description: Winlogon 會維護 GINA 所使用的工作站狀態，以判斷需要哪些驗證動作。
ms.assetid: e04175c4-bb43-4f76-8ceb-50282a1ebed0
title: Winlogon 狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d2e4ec690d6bdda15fb8e350969b36e01d5c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556227"
---
# <a name="winlogon-states"></a>Winlogon 狀態

[*Winlogon*](../secgloss/w-gly.md) 會維護 [*GINA*](../secgloss/g-gly.md) 所使用的工作站狀態，以判斷需要哪些驗證動作。

在任何時間點，Winlogon 都處於下列三種狀態之一：

-   [已登出狀態](#logged-off-state)
-   [登入狀態](#logged-on-state)
-   [工作站鎖定狀態](#workstation-locked-state)

下圖顯示這三種狀態。

![winlogon 州](images/winlogonst.png)

## <a name="logged-off-state"></a>Logged-Off 狀態

當 Winlogon 處於已登出狀態時，系統會提示使用者識別自己並提供驗證資訊。 如果使用者提供正確的使用者帳戶資訊，且沒有任何限制，則使用者會登入，而 shell 程式 (例如 Windows 檔案總管) 會在應用程式桌面上執行。 Winlogon 變更為登入狀態。

## <a name="logged-on-state"></a>Logged-On 狀態

當 Winlogon 處於登入狀態時，使用者可以與 shell 互動、啟動其他應用程式，以及執行其工作。 從登入狀態中，使用者可以停止所有工作並登出，或鎖定工作站 (將所有工作保留) 。 如果使用者決定登出，則 Winlogon 將會終止與該 [*登入會話*](../secgloss/l-gly.md) 相關聯的所有進程，而且工作站將可供其他使用者使用。 相反地，如果使用者決定鎖定工作站，則 Winlogon 會變更為工作站鎖定狀態。

## <a name="workstation-locked-state"></a>Workstation-Locked 狀態

當 Winlogon 處於工作站鎖定狀態時，會顯示安全桌面，直到使用者解除鎖定工作站，方法是提供與原本登入的使用者相同的識別和驗證資訊，或在系統管理員強制登出之前。 如果工作站已解除鎖定，則會顯示應用程式桌面，而且可以繼續工作。 但是，如果系統管理員藉由提供系統管理員帳戶) 的識別和驗證資訊來解除鎖定工作站 (，已登入使用者的處理常式會終止，而 Winlogon 會變更為已登出狀態。

您可以在每個 Winlogon 狀態中執行許多不同的動作。 GINA DLL 可執行不屬於標準 Windows 作業系統的動作。 例如，高安全性系統可能會每隔10分鐘自動鎖定工作站，並強制使用者自行重新驗證。

如需建立桌上型電腦以及註冊 (SAS) 之 [*安全注意順序*](../secgloss/s-gly.md) 的相關資訊，請參閱 [初始化 Winlogon](initializing-winlogon.md)。 如需超時作業的相關資訊，請參閱 [支援的對話方塊服務超時作業](supported-dialog-box-service-time-out-operations.md)。 如需在顯示對話方塊時將訊息傳送至 GINA 的詳細資訊，請參閱將 [訊息傳送至 GINA](sending-messages-to-the-gina.md)。 如需支援函式的詳細資訊，請參閱 [Winlogon 支援功能](authentication-functions.md)。

 

 
