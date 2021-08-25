---
description: 當許多系統函數失敗時，它們會設定最後一個錯誤碼。
ms.assetid: 4cc626ac-7574-44ce-8377-e0bdd8e74b7e
title: 正在抓取 Last-Error 程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853fb6991bab5ad761dacaf18a2ec086dbf8fc4176964888bd0ededc548fbeda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912448"
---
# <a name="retrieving-the-last-error-code"></a>正在抓取 Last-Error 程式碼

當許多系統函數失敗時，它們會設定最後一個錯誤碼。 如果您的應用程式需要更多有關錯誤的詳細資料，則可以使用 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數抓取最後一個錯誤碼，並使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式來顯示錯誤的描述。

下列範例包含一個錯誤處理函式，它會列印錯誤訊息並結束進程。 *LpszFunction* 參數是設定最後一個錯誤碼的函式名稱。


```C++
#include <windows.h>
#include <strsafe.h>

void ErrorExit(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code

    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    // Display the error message and exit the process

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR)lpMsgBuf) + lstrlen((LPCTSTR)lpszFunction) + 40) * sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR)lpDisplayBuf, TEXT("Error"), MB_OK); 

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
    ExitProcess(dw); 
}

void main()
{
    // Generate an error

    if(!GetProcessId(NULL))
        ErrorExit(TEXT("GetProcessId"));
}
```



 

 
