---
title: 查閱文字中的錯誤碼編號
description: 有時必須顯示與網路相關功能所傳回錯誤碼相關的錯誤文字。 您可能需要使用系統提供的網路管理功能來執行這項工作。
ms.assetid: 90ed87ca-7a08-4a66-b06a-e1bf668fb81a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0811c2b2da283a9cd5eb776cdb33a175c63491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967670"
---
# <a name="looking-up-text-for-error-code-numbers"></a>查閱文字中的錯誤碼編號

有時必須顯示與網路相關功能所傳回錯誤碼相關的錯誤文字。 您可能需要使用系統提供的網路管理功能來執行這項工作。

這些訊息的錯誤文字可在名為 Netmsg.dll 的訊息資料表檔案中找到，該檔案位於% systemroot% \\ system32 中。 此檔案包含 NERR \_ base (2100) 到 MAX \_ NERR (NERR \_ base + 899) 範圍中的錯誤訊息。 這些錯誤碼是在 SDK 標頭檔 lmerr 中定義。

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)和 [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa)函數可以載入 Netmsg.dll。 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage)函式會將錯誤碼對應至郵件內文（指定 Netmsg.dll 檔的模組控制碼）。

下列範例說明除了顯示與系統相關的錯誤碼相關的錯誤文字之外，如何顯示與網路管理功能相關聯的錯誤文字。 如果提供的錯誤號碼在特定範圍內，就會載入 netmsg.dll 訊息模組，並使用 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 函式來查閱指定的錯誤號碼。


```C++
#include <windows.h>
#include <stdio.h>

#include <lmerr.h>

void
DisplayErrorText(
    DWORD dwLastError
    );

#define RTN_OK 0
#define RTN_USAGE 1
#define RTN_ERROR 13

int
__cdecl
main(
    int argc,
    char *argv[]
    )
{
    if(argc != 2) {
        fprintf(stderr,"Usage: %s <error number>\n", argv[0]);
        return RTN_USAGE;
    }

    DisplayErrorText( atoi(argv[1]) );

    return RTN_OK;
}

void
DisplayErrorText(
    DWORD dwLastError
    )
{
    HMODULE hModule = NULL; // default to system source
    LPSTR MessageBuffer;
    DWORD dwBufferLength;

    DWORD dwFormatFlags = FORMAT_MESSAGE_ALLOCATE_BUFFER |
        FORMAT_MESSAGE_IGNORE_INSERTS |
        FORMAT_MESSAGE_FROM_SYSTEM ;

    //
    // If dwLastError is in the network range, 
    //  load the message source.
    //

    if(dwLastError >= NERR_BASE && dwLastError <= MAX_NERR) {
        hModule = LoadLibraryEx(
            TEXT("netmsg.dll"),
            NULL,
            LOAD_LIBRARY_AS_DATAFILE
            );

        if(hModule != NULL)
            dwFormatFlags |= FORMAT_MESSAGE_FROM_HMODULE;
    }

    //
    // Call FormatMessage() to allow for message 
    //  text to be acquired from the system 
    //  or from the supplied module handle.
    //

    if(dwBufferLength = FormatMessageA(
        dwFormatFlags,
        hModule, // module to get message from (NULL == system)
        dwLastError,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // default language
        (LPSTR) &MessageBuffer,
        0,
        NULL
        ))
    {
        DWORD dwBytesWritten;

        //
        // Output message string on stderr.
        //
        WriteFile(
            GetStdHandle(STD_ERROR_HANDLE),
            MessageBuffer,
            dwBufferLength,
            &dwBytesWritten,
            NULL
            );

        //
        // Free the buffer allocated by the system.
        //
        LocalFree(MessageBuffer);
    }

    //
    // If we loaded a message source, unload it.
    //
    if(hModule != NULL)
        FreeLibrary(hModule);
}
```



編譯此程式之後，您可以將錯誤碼號碼插入作為引數，程式會顯示文字。 例如：

``` syntax
C:\> netmsg 2453
Could not find domain controller for this domain
```

 

 