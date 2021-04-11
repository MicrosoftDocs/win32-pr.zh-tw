---
description: 當許多系統函數失敗時，它們會設定最後一個錯誤碼。
ms.assetid: 4cc626ac-7574-44ce-8377-e0bdd8e74b7e
title: 正在抓取 Last-Error 程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28ba096fae2bd38bb8dc9c291a677aa6fa161d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025879"
---
# <a name="retrieving-the-last-error-code"></a><span data-ttu-id="e213c-103">正在抓取 Last-Error 程式碼</span><span class="sxs-lookup"><span data-stu-id="e213c-103">Retrieving the Last-Error Code</span></span>

<span data-ttu-id="e213c-104">當許多系統函數失敗時，它們會設定最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e213c-104">When many system functions fail, they set the last-error code.</span></span> <span data-ttu-id="e213c-105">如果您的應用程式需要更多有關錯誤的詳細資料，則可以使用 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數抓取最後一個錯誤碼，並使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函式來顯示錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="e213c-105">If your application needs more details about an error, it can retrieve the last-error code using the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function and display a description of the error using the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function.</span></span>

<span data-ttu-id="e213c-106">下列範例包含一個錯誤處理函式，它會列印錯誤訊息並結束進程。</span><span class="sxs-lookup"><span data-stu-id="e213c-106">The following example includes an error-handling function that prints the error message and terminates the process.</span></span> <span data-ttu-id="e213c-107">*LpszFunction* 參數是設定最後一個錯誤碼的函式名稱。</span><span class="sxs-lookup"><span data-stu-id="e213c-107">The *lpszFunction* parameter is the name of the function that set the last-error code.</span></span>


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



 

 
