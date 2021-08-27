---
title: 正在捕獲網路錯誤
description: WNet 函式會傳回錯誤碼，以與工作組 Windows 的相容性。 每個 WNet 函數也會設定由 GetLastError 傳回的錯誤碼值。
ms.assetid: 8188304a-8ab3-4c43-a6d6-2806043cc195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92f02a05ab93d50b9c448ae280e5de7ddbed1260cf1df8b8b3e56aa33aaeff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072018"
---
# <a name="retrieving-network-errors"></a>正在捕獲網路錯誤

WNet 函式會傳回錯誤碼，以與工作組 Windows 的相容性。 每個 WNet 函數也會設定由 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)傳回的錯誤碼值。

當其中一個 WNet 函式傳回錯誤 \_ 擴充 \_ 錯誤時，應用程式可以呼叫 [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora) 函式來取得錯誤的其他相關資訊。 這項資訊通常是網路提供者特有的。

下列範例說明 (NetErrorHandler) 的應用程式定義錯誤處理函式。 函數會採用三個引數：視窗控制碼、其中一個 WNet 函式所傳回的錯誤碼，以及產生錯誤的函式名稱。 如果錯誤碼為錯誤 \_ 擴充 \_ 錯誤，NetErrorHandler 會呼叫 **WNetGetLastError** 來取得延伸的錯誤資訊並列印資訊。 此範例會呼叫 [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) 函數來處理訊息。


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")
#pragma comment(lib, "user32.lib")

BOOL WINAPI NetErrorHandler(HWND hwnd, 
                            DWORD dwErrorCode, 
                            LPSTR lpszFunction) 
{ 
    DWORD dwWNetResult, dwLastError; 
    CHAR szError[256]; 
    CHAR szCaption[256]; 
    CHAR szDescription[256]; 
    CHAR szProvider[256]; 
 
    // The following code performs standard error-handling. 
 
    if (dwErrorCode != ERROR_EXTENDED_ERROR) 
    { 
        sprintf_s((LPSTR) szError, sizeof(szError), "%s failed; \nResult is %ld", 
            lpszFunction, dwErrorCode); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
 
    // The following code performs error-handling when the 
    //  ERROR_EXTENDED_ERROR return value indicates that the 
    //  WNetGetLastError function can retrieve additional information.
 
    else 
    { 
        dwWNetResult = WNetGetLastError(&dwLastError, // error code
            (LPSTR) szDescription,  // buffer for error description 
            sizeof(szDescription),  // size of error buffer
            (LPSTR) szProvider,     // buffer for provider name 
            sizeof(szProvider));    // size of name buffer
 
        //
        // Process errors.
        //
        if(dwWNetResult != NO_ERROR) { 
            sprintf_s((LPSTR) szError, sizeof(szError), 
                "WNetGetLastError failed; error %ld", dwWNetResult); 
            MessageBox(hwnd, (LPSTR) szError, "WNetGetLastError", MB_OK); 
            return FALSE; 
        } 
 
        //
        // Otherwise, print the additional error information.
        //
        sprintf_s((LPSTR) szError, sizeof(szError), 
            "%s failed with code %ld;\n%s", 
            (LPSTR) szProvider, dwLastError, (LPSTR) szDescription); 
        sprintf_s((LPSTR) szCaption, sizeof(szCaption), "%s error", lpszFunction); 
        MessageBox(hwnd, (LPSTR) szError, (LPSTR) szCaption, MB_OK); 
        return TRUE; 
    } 
}
```



 

 