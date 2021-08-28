---
description: Winlogon 會執行兩個超時作業，一個用於安全對話方塊，另一個用於啟用和終止螢幕保護裝置。
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: 支援的對話方塊服務超時作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7715cafb426a59bd9773791788dd9914fff0c1fac4a5b820e9cc06416e966eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916447"
---
# <a name="supported-dialog-box-service-time-out-operations"></a>支援的對話方塊服務超時作業

[*Winlogon*](../secgloss/w-gly.md) 會執行兩個超時作業，一個用於安全對話方塊，另一個用於啟用和終止螢幕保護裝置。

在顯示安全的對話方塊時（例如登入或解除鎖定工作站），Winlogon 可以超時對話方塊，並將適當的結果碼傳回到對話方塊程式。 Winlogon 提供一組 [*GINA*](../secgloss/g-gly.md)的對話方塊支援功能。 GINA 必須使用這些函式，而不是其 Windows 的對應專案，以確保 GINA 和 Winlogon 維持適當的對話方塊控制。 若無法使用這些函式的 Winlogon 版本，可能會導致未經授權的使用者取得系統的存取權。

Winlogon 對話方塊服務是由下列支援功能所提供。



| Support 函數                                               | Description                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**WlxMessageBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | 類似于 Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox)函數。                         |
| [**WlxDialogBox**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | 類似于 Windows [**對話方塊**](/windows/win32/api/winuser/nf-winuser-dialogboxa)函數。                           |
| [**WlxDialogBoxIndirect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | 類似于 Windows [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta)函數。           |
| [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | 類似于 Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama)函數。                 |
| [**WlxDialogBoxIndirectParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | 類似于 Windows [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama)函數。 |



 

GINA Dll 也可以接收 \_ \_ 來自 WINLOGON 的 WLX WM SAS 訊息。 如果收到 (SAS) 的 [*安全注意順序*](../secgloss/s-gly.md) ，則會將這些訊息傳送至使用中的對話方塊。 如果 GINA 正在提示 [*智慧卡*](../secgloss/s-gly.md)的相符 PIN，而且卡片已從智慧卡 [*讀卡機*](../secgloss/r-gly.md)中移除，這就很有用。 \_當在對話方塊作業 \_ 期間發生 SAS 事件時，Winlogon 會使用 WLX DLG SAS 作為 EndDialog 結果碼。

您也可以透過這種方式來傳遞超時時間。 WLX 的 \_ WM \_ SAS 訊息會以 WLX \_ sas \_ 類型 \_ SCRNSVR \_ TIMEOUT 或 WLX \_ sas \_ 類型 timeout 傳送 \_ 。 對話方塊會以適當的結束代碼結束，讓 GINA 開發人員攔截超時通知。

您可以使用程式碼 WLX 使用者登出，來終止 GINA 對話方塊 \_ \_ \_ 。 這表示使用者已在執行對話方塊期間登出 (例如，從另一個執行緒) 呼叫 [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) 函數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[正在初始化 Winlogon](initializing-winlogon.md)
</dt> <dt>

[Winlogon 狀態](winlogon-states.md)
</dt> <dt>

[將訊息傳送至 GINA](sending-messages-to-the-gina.md)
</dt> <dt>

[Winlogon 支援函式](authentication-functions.md)
</dt> </dl>

 

 
