---
description: 關機事件追蹤器可讓使用者或應用程式記錄關閉或重新開機系統的原因。
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: 關機事件追蹤器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2deaebde736ed2e0ba72f38e8849cf815b167da68fdddbecb92e713083699b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664358"
---
# <a name="shutdown-event-tracker"></a>關機事件追蹤器

*關機事件追蹤* 器可讓使用者或應用程式記錄關閉或重新開機系統的原因。 當您從 [**開始**] 功能表選取 **關機**，或使用 [Shutdown.exe] 時，系統會提示使用者填寫資訊。 開發人員在呼叫 [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) 和 [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) 函式時，可能會包含原因代碼。 這項資訊會儲存在事件記錄檔中。

**Windows XP：** 從 Windows Server 2003 開始，預設會啟用這項功能，因此您必須在 Windows XP 上啟用此功能。 如需詳細資訊，請參閱系統或 TechNet 上所含之關機事件追蹤器的檔。

[**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)和 [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)函式已更新，可支援 *dwReason* 參數中的關機原因代碼。 使用 Reason 定義的值來建立關機原因代碼，或定義自訂的原因代碼。 關機原因代碼是由主要旗標、次要旗標和兩個選擇性旗標所組成。 如需詳細資訊，請參閱 [系統關機原因代碼](system-shutdown-reason-codes.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (TechNet) 關機事件追蹤器 ](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))
</dt> </dl>

 

 
