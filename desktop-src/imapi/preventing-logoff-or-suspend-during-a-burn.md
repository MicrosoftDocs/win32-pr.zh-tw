---
title: 在燒錄期間防止登出或暫停
description: 如果未在應用程式中進行適當的預防措施，使用者可能會在燒錄作業期間登出。 這會導致燒錄程式中斷，這可能會導致資料遺失，而且可能會導致無法使用光碟。
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5922fbe6dbc27303cee82e7ed745cbaaf2744781
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463024"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a>在燒錄期間防止登出或暫停

如果未在應用程式中進行適當的預防措施，使用者可能會在燒錄作業期間登出。 這會導致燒錄程式中斷，這可能會導致資料遺失，而且可能會導致無法使用光碟。

若要避免這個問題，應用程式應該處理在登出之前傳遞的 [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) 訊息。 如果應用程式在執行燒錄操作時收到此訊息，則會傳回 **FALSE** 以取消登出程式。 如果應用程式可讓使用者決定是否要繼續登出，則應該提供警告，指出使用者將會遺失資料。

燒錄程式期間的電源轉換也可能會在燒錄活動成功時產生潛在問題。 在燒錄程式中避免這些複雜性，需要應用程式知道何時即將進行電源轉換。 這是藉由讓應用程式處理 [**WM \_ POWERBROADCAST**](/windows/desktop/Power/wm-powerbroadcast) 訊息來完成。 針對 Windows XP 或 Windows Server 2003 開發的應用程式可能會傳回「 **廣播 \_ 查詢 \_ 拒絕** 」以回應 [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend)，以防止在燒錄過程中暫停。

由於 Windows Vista 和 Windows Server 2008 的電源管理模型有所變更，因此 [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) 事件不再傳遞給應用程式。 相反地，系統會傳遞 [**PBT \_ APMSUSPEND**](/windows/desktop/Power/pbt-apmsuspend) 事件，讓應用程式有兩秒鐘的時間來準備進行轉換。

由於這些變更的結果，建議應用程式呼叫 [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) 函式來防止系統閒置時間，這通常會導致轉換暫停。 請務必記得，使用適當的旗標來呼叫這個函式只會防止系統閒置，而非進行中的暫止。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 IMAPI.EXE](using-imapi.md)
</dt> <dt>

[**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 