---
description: 若要報告事件，您必須先在訊息文字檔中定義事件。 如需撰寫訊息文字檔的詳細資訊，請參閱訊息文字檔。 下圖顯示此範例中使用的訊息文字檔。
ms.assetid: ace31e17-a638-414f-8518-9b944118047b
title: 報告事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52c5fe2abba47adb3b1b7bdf7d5562da8e57eb26aa21fe8448871c940cf2c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015426"
---
# <a name="reporting-events"></a>報告事件

若要報告事件，您必須先在訊息文字檔中定義事件。 如需撰寫訊息文字檔的詳細資訊，請參閱 [訊息文字檔](message-text-files.md)。 下圖顯示此範例中使用的訊息文字檔。


```C++
; // MyEventProvider.mc 

; // This is the header section.


SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
               Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
               Warning=0x2:STATUS_SEVERITY_WARNING
               Error=0x3:STATUS_SEVERITY_ERROR
              )


FacilityNames=(System=0x0:FACILITY_SYSTEM
               Runtime=0x2:FACILITY_RUNTIME
               Stubs=0x3:FACILITY_STUBS
               Io=0x4:FACILITY_IO_ERROR_CODE
              )

LanguageNames=(English=0x409:MSG00409)


; // The following are the categories of events.

MessageIdTypedef=WORD

MessageId=0x1
SymbolicName=NETWORK_CATEGORY
Language=English
Network Events
.

MessageId=0x2
SymbolicName=DATABASE_CATEGORY
Language=English
Database Events
.

MessageId=0x3
SymbolicName=UI_CATEGORY
Language=English
UI Events
.


; // The following are the message definitions.

MessageIdTypedef=DWORD

MessageId=0x100
Severity=Error
Facility=Runtime
SymbolicName=MSG_INVALID_COMMAND
Language=English
The command is not valid.
.


MessageId=0x101
Severity=Error
Facility=System
SymbolicName=MSG_BAD_FILE_CONTENTS
Language=English
File %1 contains content that is not valid.
.

MessageId=0x102
Severity=Warning
Facility=System
SymbolicName=MSG_RETRIES
Language=English
There have been %1 retries with %2 success! Disconnect from
the server and try again later.
.

MessageId=0x103
Severity=Informational
Facility=System
SymbolicName=MSG_COMPUTE_CONVERSION
Language=English
%1 %%4096 = %2 %%4097. 
.


; // The following are the parameter strings */


MessageId=0x1000
Severity=Success
Facility=System
SymbolicName=QUARTS_UNITS
Language=English
quarts%0
.

MessageId=0x1001
Severity=Success
Facility=System
SymbolicName=GALLONS_UNITS
Language=English
gallons%0
.
```



若要編譯訊息文字檔，請使用下列命令：

**mc-U provider.mc**

若要編譯訊息編譯器產生的資源，請使用下列命令：

**rc 提供者 .rc**

若要建立包含訊息資料表字串資源的僅包含資源的 DLL，請使用下列命令 (您可以從 Visual Studio 命令提示字元執行命令) ：

**連結-dll-noentry 提供者 .res**

以下顯示編譯器為上述訊息文字檔所產生的標頭檔。 將標頭檔包含在您的專案中。


```C++
// MyEventProvider.mc 
// This is the header section.
// The following are categories of events.
//
//  Values are 32 bit values laid out as follows:
//
//   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
//   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
//  +---+-+-+-----------------------+-------------------------------+
//  |Sev|C|R|     Facility          |               Code            |
//  +---+-+-+-----------------------+-------------------------------+
//
//  where
//
//      Sev - is the severity code
//
//          00 - Success
//          01 - Informational
//          10 - Warning
//          11 - Error
//
//      C - is the Customer code flag
//
//      R - is a reserved bit
//
//      Facility - is the facility code
//
//      Code - is the facility's status code
//
//
// Define the facility codes
//
#define FACILITY_SYSTEM                  0x0
#define FACILITY_STUBS                   0x3
#define FACILITY_RUNTIME                 0x2
#define FACILITY_IO_ERROR_CODE           0x4


//
// Define the severity codes
//
#define STATUS_SEVERITY_WARNING          0x2
#define STATUS_SEVERITY_SUCCESS          0x0
#define STATUS_SEVERITY_INFORMATIONAL    0x1
#define STATUS_SEVERITY_ERROR            0x3


//
// MessageId: NETWORK_CATEGORY
//
// MessageText:
//
// Network Events
//
#define NETWORK_CATEGORY                 ((WORD)0x00000001L)

//
// MessageId: DATABASE_CATEGORY
//
// MessageText:
//
// Database Events
//
#define DATABASE_CATEGORY                ((WORD)0x00000002L)

//
// MessageId: UI_CATEGORY
//
// MessageText:
//
// UI Events
//
#define UI_CATEGORY                      ((WORD)0x00000003L)

 // The following are message definitions.
//
// MessageId: MSG_INVALID_COMMAND
//
// MessageText:
//
// The command is not valid.
//
#define MSG_INVALID_COMMAND              ((DWORD)0xC0020100L)

//
// MessageId: MSG_BAD_FILE_CONTENTS
//
// MessageText:
//
// File %1 contains content that is not valid.
//
#define MSG_BAD_FILE_CONTENTS            ((DWORD)0xC0000101L)

//
// MessageId: MSG_RETRIES
//
// MessageText:
//
// There have been %1 retries with %2 success! Disconnect from
// the server and try again later.
//
#define MSG_RETRIES                      ((DWORD)0x80000102L)

//
// MessageId: MSG_COMPUTE_CONVERSION
//
// MessageText:
//
// %1 %%4096 = %2 %%4097. 
//
#define MSG_COMPUTE_CONVERSION           ((DWORD)0x40000103L)

 // The following are the parameter strings */
//
// MessageId: QUARTS_UNITS
//
// MessageText:
//
// quarts%0
//
#define QUARTS_UNITS                     ((DWORD)0x00001000L)

//
// MessageId: GALLONS_UNITS
//
// MessageText:
//
// gallons%0
//
#define GALLONS_UNITS                    ((DWORD)0x00001001L)

```



下列範例顯示如何使用 [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) 函式來寫入上述訊息文字檔中定義的事件。


```C++
#ifndef UNICODE
#define UNICODE
#endif
#include <windows.h>
#include <stdio.h>
#include "provider.h"

#pragma comment(lib, "advapi32.lib")

#define PROVIDER_NAME L"MyEventProvider"

// Hardcoded insert string for the event messages.
CONST LPWSTR pBadCommand = L"The command that was not valid";
CONST LPWSTR pFilename = L"c:\\folder\\file.ext";
CONST LPWSTR pNumberOfRetries = L"3";
CONST LPWSTR pSuccessfulRetries = L"0";
CONST LPWSTR pQuarts = L"8";
CONST LPWSTR pGallons = L"2";

void wmain(void)
{
    HANDLE hEventLog = NULL;
    LPWSTR pInsertStrings[2] = {NULL, NULL};
    DWORD dwEventDataSize = 0;

    // The source name (provider) must exist as a subkey of Application.
    hEventLog = RegisterEventSource(NULL, PROVIDER_NAME);
    if (NULL == hEventLog)
    {
        wprintf(L"RegisterEventSource failed with 0x%x.\n", GetLastError());
        goto cleanup;
    }

    // This event includes user-defined data as part of the event. The event message
    // does not use insert strings.
    dwEventDataSize = ((DWORD)wcslen(pBadCommand) + 1) * sizeof(WCHAR);
    if (!ReportEvent(hEventLog, EVENTLOG_ERROR_TYPE, UI_CATEGORY, MSG_INVALID_COMMAND, NULL, 0, dwEventDataSize, NULL, pBadCommand))
    {
        wprintf(L"ReportEvent failed with 0x%x for event 0x%x.\n", GetLastError(), MSG_INVALID_COMMAND);
        goto cleanup;
    }

    // This event uses insert strings.
    pInsertStrings[0] = pFilename;
    if (!ReportEvent(hEventLog, EVENTLOG_ERROR_TYPE, DATABASE_CATEGORY, MSG_BAD_FILE_CONTENTS, NULL, 1, 0, (LPCWSTR*)pInsertStrings, NULL))
    {
        wprintf(L"ReportEvent failed with 0x%x for event 0x%x.\n", GetLastError(), MSG_BAD_FILE_CONTENTS);
        goto cleanup;
    }

    // This event uses insert strings.
    pInsertStrings[0] = pNumberOfRetries;
    pInsertStrings[1] = pSuccessfulRetries;
    if (!ReportEvent(hEventLog, EVENTLOG_WARNING_TYPE, NETWORK_CATEGORY, MSG_RETRIES, NULL, 2, 0, (LPCWSTR*)pInsertStrings, NULL))
    {
        wprintf(L"ReportEvent failed with 0x%x for event 0x%x.\n", GetLastError(), MSG_RETRIES);
        goto cleanup;
    }

    // This event uses insert strings.
    pInsertStrings[0] = pQuarts;
    pInsertStrings[1] = pGallons;
    if (!ReportEvent(hEventLog, EVENTLOG_INFORMATION_TYPE, UI_CATEGORY, MSG_COMPUTE_CONVERSION, NULL, 2, 0, (LPCWSTR*)pInsertStrings, NULL))
    {
        wprintf(L"ReportEvent failed with 0x%x for event 0x%x.\n", GetLastError(), MSG_COMPUTE_CONVERSION);
        goto cleanup;
    }

    wprintf(L"All events successfully reported.\n");

cleanup:

    if (hEventLog)
        DeregisterEventSource(hEventLog);
}
```



執行此範例之前，請在登錄中註冊提供者。 如需登錄設定的詳細資訊，請參閱 [事件來源](event-sources.md)。 在下列機碼底下新增 "MyEventProvider" 作為登錄機碼：

**HKEY \_ 本機 \_ 電腦 \\ 系統 \\ CurrentControlSet \\ 服務 \\ eventlog \\ 應用程式**

以下顯示要為 "MyEventProvider" 登錄機碼設定的登錄值。

| 值名稱           | 類型       | [數值資料]           |
|----------------------|------------|----------------------|
| CategoryCount        | REG \_ DWORD | 0x00000003           |
| CategoryMessageFile  | REG \_ SZ    | *路徑* \\provider.dll |
| EventMessageFile     | REG \_ SZ    | *路徑* \\provider.dll |
| ParameterMessageFile | REG \_ SZ    | *路徑* \\provider.dll |
| TypesSupported       | REG \_ DWORD | 0x00000007           |



 

 

 



