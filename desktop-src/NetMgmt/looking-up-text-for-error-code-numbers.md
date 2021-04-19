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
# <a name="looking-up-text-for-error-code-numbers"></a><span data-ttu-id="4d85f-104">查閱文字中的錯誤碼編號</span><span class="sxs-lookup"><span data-stu-id="4d85f-104">Looking Up Text for Error Code Numbers</span></span>

<span data-ttu-id="4d85f-105">有時必須顯示與網路相關功能所傳回錯誤碼相關的錯誤文字。</span><span class="sxs-lookup"><span data-stu-id="4d85f-105">It is sometimes necessary to display error text associated with error codes returned from networking-related functions.</span></span> <span data-ttu-id="4d85f-106">您可能需要使用系統提供的網路管理功能來執行這項工作。</span><span class="sxs-lookup"><span data-stu-id="4d85f-106">You may need to perform this task with the network management functions provided by the system.</span></span>

<span data-ttu-id="4d85f-107">這些訊息的錯誤文字可在名為 Netmsg.dll 的訊息資料表檔案中找到，該檔案位於% systemroot% \\ system32 中。</span><span class="sxs-lookup"><span data-stu-id="4d85f-107">The error text for these messages is found in the message table file named Netmsg.dll, which is found in %systemroot%\\system32.</span></span> <span data-ttu-id="4d85f-108">此檔案包含 NERR \_ base (2100) 到 MAX \_ NERR (NERR \_ base + 899) 範圍中的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="4d85f-108">This file contains error messages in the range NERR\_BASE (2100) through MAX\_NERR(NERR\_BASE+899).</span></span> <span data-ttu-id="4d85f-109">這些錯誤碼是在 SDK 標頭檔 lmerr 中定義。</span><span class="sxs-lookup"><span data-stu-id="4d85f-109">These error codes are defined in the SDK header file lmerr.h.</span></span>

<span data-ttu-id="4d85f-110">[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)和 [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa)函數可以載入 Netmsg.dll。</span><span class="sxs-lookup"><span data-stu-id="4d85f-110">The [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) functions can load Netmsg.dll.</span></span> <span data-ttu-id="4d85f-111">[**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage)函式會將錯誤碼對應至郵件內文（指定 Netmsg.dll 檔的模組控制碼）。</span><span class="sxs-lookup"><span data-stu-id="4d85f-111">The [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function maps an error code to message text, given a module handle to the Netmsg.dll file.</span></span>

<span data-ttu-id="4d85f-112">下列範例說明除了顯示與系統相關的錯誤碼相關的錯誤文字之外，如何顯示與網路管理功能相關聯的錯誤文字。</span><span class="sxs-lookup"><span data-stu-id="4d85f-112">The following sample illustrates how to display error text associated with network management functions, in addition to displaying error text associated with system-related error codes.</span></span> <span data-ttu-id="4d85f-113">如果提供的錯誤號碼在特定範圍內，就會載入 netmsg.dll 訊息模組，並使用 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 函式來查閱指定的錯誤號碼。</span><span class="sxs-lookup"><span data-stu-id="4d85f-113">If the supplied error number is in a specific range, the netmsg.dll message module is loaded and used to look up the specified error number with the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function.</span></span>


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



<span data-ttu-id="4d85f-114">編譯此程式之後，您可以將錯誤碼號碼插入作為引數，程式會顯示文字。</span><span class="sxs-lookup"><span data-stu-id="4d85f-114">After you compile this program, you can insert the error code number as an argument and the program will display the text.</span></span> <span data-ttu-id="4d85f-115">例如：</span><span class="sxs-lookup"><span data-stu-id="4d85f-115">For example:</span></span>

``` syntax
C:\> netmsg 2453
Could not find domain controller for this domain
```

 

 