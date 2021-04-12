---
description: 使用適用于家長監護的記錄 Api
ms.assetid: 6c38a634-53ba-4e76-83bf-1a3f36efb0bc
title: 使用適用于家長監護的記錄 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d1cedb9ff02856be6ea1ae2069d8635b980681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849516"
---
# <a name="using-logging-apis-for-parental-controls"></a>使用適用于家長監護的記錄 Api

### <a name="activity-reporting-logging"></a>活動報告 (記錄) 

WpcEvent 標頭檔包含每個預先定義之活動事件種類和自訂類型的欄位定義。 此範例程式碼示範使用 ETW 發佈 API 來記錄立即訊息交談邀請事件的步驟：


```C++
#include <windows.h>
#include <evntprov.h>
#include <wpcevent.h>

#pragma comment(lib, "advapi32.lib")

#define BYTELEN(x) ((wcslen(x) + 1) * sizeof(WCHAR))

void main()
{
    REGHANDLE hWpc = 0;

    // Register
    ULONG res = EventRegister(&WPCPROV, NULL, NULL, &hWpc);

    // Log an event
    PCWSTR pcszAppName = L"SuperIM";
    PCWSTR pcszAppVersion = L"7.0";
    PCWSTR pcszAccountName = L"Kate";
    PCWSTR pcszConvID = L"102";
    PCWSTR pcszRequestingIP = L"192.168.2.100";
    PCWSTR pcszSender = L"imperson@isp.com";
    const DWORD dwReason = WPCFLAG_ISBLOCKED_NOTBLOCKED;
    const DWORD dwRecipCount = 1;
    PCWSTR pcszRecipient = L"otherim@isp.com";

    EVENT_DATA_DESCRIPTOR eventData[WPC_ARGS_CONVERSATIONINITEVENT_CARGS];

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPNAME],
        (const PVOID)pcszAppName, (ULONG)BYTELEN(pcszAppName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_APPVERSION],
        (const PVOID)pcszAppVersion,(ULONG)BYTELEN(pcszAppVersion));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_ACCOUNTNAME], 
        (const PVOID)pcszAccountName, (ULONG)BYTELEN(pcszAccountName));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_CONVID], 
        (const PVOID)pcszConvID, (ULONG)BYTELEN(pcszConvID));

    EventDataDescCreate(
        &eventData[WPC_ARGS_CONVERSATIONINITEVENT_REQUESTINGIP], 
        (const PVOID)pcszRequestingIP, (ULONG)BYTELEN(pcszRequestingIP));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_SENDER],
        (const PVOID)pcszSender, (ULONG)BYTELEN(pcszSender));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_REASON],
        (const PVOID)&dwReason, sizeof(dwReason));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPCOUNT],
        (const PVOID)&dwRecipCount, sizeof(dwRecipCount));

    EventDataDescCreate(&eventData[WPC_ARGS_CONVERSATIONINITEVENT_RECIPIENT],
        (const PVOID)pcszRecipient, (ULONG)BYTELEN(pcszRecipient));


    ULONG lRet = EventWrite(hWpc, &WPCEVENT_IM_INVITATION, ARRAYSIZE(eventData), eventData);

    // Unregister
    EventUnregister(hWpc);
}
```



### <a name="custom-logging"></a>自訂記錄

若要讓應用程式擴充在預先定義的事件集合之外所記錄的事件，或一個自訂類型，您必須在應用程式資訊清單中定義該的提供者。 然後可以匯入 WPC 預設通道，然後記錄應用程式定義的事件。

### <a name="logging-rights"></a>記錄許可權

WPC 記錄通道是由 (ACL) 的 [*存取控制清單*](/windows/desktop/SecGloss/a-gly) 所控制，以提供僅限系統管理員的完整存取權。 非系統管理員帳戶可能會寫入至通道，但沒有讀取或刪除存取權。 通道的存取權是使用 ETW API。

### <a name="parental-controls-logging-provider-details"></a>家長監護記錄提供者詳細資料

WPC 提供者的名稱為 Microsoft.com/Windows/ParentalControls，GUID 為 {01090065-B467-4503-9B28-533766761087}。 預設的本機記錄通道是 Microsoft.com/Windows/ParentalControls/LocalEvents。

記錄檔會儲存在 Windows \\ System32 \\ Wpc \\ Logs 資料夾中。

### <a name="notification-of-impending-time-limits-logout"></a>即將登出的時間限制通知

家長監護系統會在15分鐘內引發警告事件，然後在根據時間限制登出受控制使用者之前的1分鐘內引發警告事件。 應用程式可以訂閱這些事件，尤其是在未顯示標準 Windows 通知的 DirectX 全螢幕模式中執行時。 提供的範例程式碼會顯示如何訂閱事件、註冊回呼函式，以及接收事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[家長監護擴充功能總覽](parental-controls-extensibility-features-overview.md)
</dt> <dt>

[**事件 \_ 資料 \_ 描述元**](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
</dt> <dt>

[**EventDataDescCreate**](/windows/desktop/api/evntprov/nf-evntprov-eventdatadesccreate)
</dt> <dt>

[**WPC 的 \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 
