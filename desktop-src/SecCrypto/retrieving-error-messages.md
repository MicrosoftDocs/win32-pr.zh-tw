---
description: 當方法呼叫產生錯誤時，許多函數都會傳回錯誤碼。
ms.assetid: 9d60277a-5ee8-471e-bfcd-d104064030a8
title: 正在抓取錯誤訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d96ffb6627dac4f8612a80c68b1a227516ec645440c56dd7c58672cd8222c23a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900504"
---
# <a name="retrieving-error-messages"></a>正在抓取錯誤訊息

當方法呼叫產生錯誤時，許多函數都會傳回錯誤碼。 若為大部分的憑證服務介面和傳回錯誤碼的 API 專案，可以使用 **Null** 模組控制碼呼叫 [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)來取得錯誤訊息正文。 如果 **FormatMessage** 失敗，可能是因為備份 API 元素或資料庫相關的錯誤而產生的錯誤碼;使用對應至 Ntdsbmsg.dll 程式庫的模組控制碼來呼叫 **FormatMessage** 時，應該會取得錯誤訊息正文。 下列範例顯示如何在憑證服務應用程式中取得錯誤訊息正文。


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



 

 
