---
description: 事件處理常式原型函式用於所有處理 Winlogon 通知事件的函式。
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: 事件處理常式函式原型回呼函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978334"
---
# <a name="event-handler-function-prototype-callback-function"></a>事件處理常式函式原型回呼函數

\[從 Windows Server 2008 和 Windows Vista 起，無法再使用事件處理常式原型函式。 \]

事件處理常式原型函式用於所有處理 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 通知事件的函式。 函式名稱（以預留位置 *事件 \_ 處理常式函式 \_ \_ 名稱* 表示）通常會反映函式處理的事件名稱。 例如，處理登入事件的函式可能會命名為： **WLEventLogon**。

## <a name="syntax"></a>語法


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInfo* \[在\]
</dt> <dd>

[**WLX \_ 通知 \_ 資訊**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info)結構的指標，其中包含事件的詳細資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個回呼函式不會傳回值。

## <a name="remarks"></a>備註

如果您的事件處理常式需要建立子進程，它應該呼叫 [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) 函數。 否則，就會在 Winlogon 桌面上建立新的進程，而不是使用者的桌面。

## <a name="examples"></a>範例

下列範例會示範如何執行 Winlogon 事件的事件處理常式。 為了簡單起見，系統只會顯示登入和登出事件處理常式的執行。 您可以用完全相同的方式來執行其餘事件的處理常式。


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows XP<br/>                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                       |



 

