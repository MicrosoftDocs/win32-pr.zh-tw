---
description: 當方法呼叫產生錯誤時，許多函數都會傳回錯誤碼。
ms.assetid: 9d60277a-5ee8-471e-bfcd-d104064030a8
title: 正在抓取錯誤訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cefeab75e4419bc1e36785236962069a6913e84d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849238"
---
# <a name="retrieving-error-messages"></a><span data-ttu-id="e03bd-103">正在抓取錯誤訊息</span><span class="sxs-lookup"><span data-stu-id="e03bd-103">Retrieving Error Messages</span></span>

<span data-ttu-id="e03bd-104">當方法呼叫產生錯誤時，許多函數都會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e03bd-104">When a method call produces an error, many functions return an error code.</span></span> <span data-ttu-id="e03bd-105">若為大部分的憑證服務介面和傳回錯誤碼的 API 專案，可以使用 **Null** 模組控制碼呼叫 [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)來取得錯誤訊息正文。</span><span class="sxs-lookup"><span data-stu-id="e03bd-105">For most Certificate Services interfaces and API elements that return an error code, the error message text can be retrieved by calling [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) with a **NULL** module handle.</span></span> <span data-ttu-id="e03bd-106">如果 **FormatMessage** 失敗，可能是因為備份 API 元素或資料庫相關的錯誤而產生的錯誤碼;使用對應至 Ntdsbmsg.dll 程式庫的模組控制碼來呼叫 **FormatMessage** 時，應該會取得錯誤訊息正文。</span><span class="sxs-lookup"><span data-stu-id="e03bd-106">If **FormatMessage** does not succeed, the error code most likely resulted from a backup API element or database related error; calling **FormatMessage** with a module handle corresponding to the Ntdsbmsg.dll library should retrieve the error message text.</span></span> <span data-ttu-id="e03bd-107">下列範例顯示如何在憑證服務應用程式中取得錯誤訊息正文。</span><span class="sxs-lookup"><span data-stu-id="e03bd-107">The following example shows how to retrieve error message text in a Certificate Services application.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
// Display error message text, given an error code.
// Typically, the parameter passed to this function is retrieved
// from GetLastError().
void PrintCSBackupAPIErrorMessage(DWORD dwErr)
{

    WCHAR   wszMsgBuff[512];  // Buffer for text.

    DWORD   dwChars;  // Number of chars returned.

    // Try to get the message from the system errors.
    dwChars = FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM |
                             FORMAT_MESSAGE_IGNORE_INSERTS,
                             NULL,
                             dwErr,
                             0,
                             wszMsgBuff,
                             512,
                             NULL );

    if (0 == dwChars)
    {
        // The error code did not exist in the system errors.
        // Try Ntdsbmsg.dll for the error code.

        HINSTANCE hInst;

        // Load the library.
        hInst = LoadLibrary(L"Ntdsbmsg.dll");
        if ( NULL == hInst )
        {
            printf("cannot load Ntdsbmsg.dll\n");
            exit(1);  // Could 'return' instead of 'exit'.
        }

        // Try getting message text from ntdsbmsg.
        dwChars = FormatMessage( FORMAT_MESSAGE_FROM_HMODULE |
                                 FORMAT_MESSAGE_IGNORE_INSERTS,
                                 hInst,
                                 dwErr,
                                 0,
                                 wszMsgBuff,
                                 512,
                                 NULL );

        // Free the library.
        FreeLibrary( hInst );

    }

    // Display the error message, or generic text if not found.
    printf("Error value: %d Message: %ws\n",
            dwErr,
            dwChars ? wszMsgBuff : L"Error message not found." );

}
```



 

 
