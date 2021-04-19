---
description: 下列範例是建立簡單 DLL Myputs.dll 所需的原始程式碼。
ms.assetid: 3b11a83b-9943-4b66-8d0d-4a236ad5ffb8
title: 建立簡單的 Dynamic-Link 程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572c25c87a3130739a55fcccfc9d8f9c6514d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983368"
---
# <a name="creating-a-simple-dynamic-link-library"></a><span data-ttu-id="13653-103">建立簡單的 Dynamic-Link 程式庫</span><span class="sxs-lookup"><span data-stu-id="13653-103">Creating a Simple Dynamic-Link Library</span></span>

<span data-ttu-id="13653-104">下列範例是建立簡單 DLL Myputs.dll 所需的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="13653-104">The following example is the source code needed to create a simple DLL, Myputs.dll.</span></span> <span data-ttu-id="13653-105">它會定義一個簡單的字串列印函式，稱為 myPuts。</span><span class="sxs-lookup"><span data-stu-id="13653-105">It defines a simple string-printing function called myPuts.</span></span> <span data-ttu-id="13653-106">Myputs DLL 並未定義進入點函式，因為它與 C 執行時間程式庫連結，而且沒有本身的初始化或清除功能可執行。</span><span class="sxs-lookup"><span data-stu-id="13653-106">The Myputs DLL does not define an entry-point function, because it is linked with the C run-time library and has no initialization or cleanup functions of its own to perform.</span></span>

<span data-ttu-id="13653-107">若要建立 DLL，請遵循開發工具隨附檔中的指示。</span><span class="sxs-lookup"><span data-stu-id="13653-107">To build the DLL, follow the directions in the documentation included with your development tools.</span></span>

<span data-ttu-id="13653-108">如需使用 myPuts 的範例，請參閱 [使用 Load-Time 動態連結](using-load-time-dynamic-linking.md) 或 [使用 Run-Time 動態連結](using-run-time-dynamic-linking.md)。</span><span class="sxs-lookup"><span data-stu-id="13653-108">For an example that uses myPuts, see [Using Load-Time Dynamic Linking](using-load-time-dynamic-linking.md) or [Using Run-Time Dynamic Linking](using-run-time-dynamic-linking.md).</span></span>


```C++
// The myPuts function writes a null-terminated string to
// the standard output device.
 
// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.
 
 
#include <windows.h>
 
#define EOF (-1)
 
#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif
 
__declspec(dllexport) int __cdecl myPuts(LPWSTR lpszMsg)
{
    DWORD cchWritten;
    HANDLE hConout;
    BOOL fRet;
 
    // Get a handle to the console output device.

    hConout = CreateFileW(L"CONOUT$",
                         GENERIC_WRITE,
                         FILE_SHARE_WRITE,
                         NULL,
                         OPEN_EXISTING,
                         FILE_ATTRIBUTE_NORMAL,
                         NULL);

    if (INVALID_HANDLE_VALUE == hConout)
        return EOF;
 
    // Write a null-terminated string to the console output device.
 
    while (*lpszMsg != L'\0')
    {
        fRet = WriteConsole(hConout, lpszMsg, 1, &cchWritten, NULL);
        if( (FALSE == fRet) || (1 != cchWritten) )
            return EOF;
        lpszMsg++;
    }
    return 1;
}
 
#ifdef __cplusplus
}
#endif
```



 

 



