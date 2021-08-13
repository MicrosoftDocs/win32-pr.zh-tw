---
description: 您可以在載入時間和執行時間動態連結中使用相同的 DLL。
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: 使用 Run-Time 動態連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c13cc66a34f0fd5938fcdada027b30223ebff0abe6e9ce459d60f93a6546f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119255978"
---
# <a name="using-run-time-dynamic-linking"></a>使用 Run-Time 動態連結

您可以在載入時間和執行時間動態連結中使用相同的 DLL。 下列範例會使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函數來取得 Myputs DLL 的控制碼 (請參閱 [建立簡單的 Dynamic-Link 程式庫](creating-a-simple-dynamic-link-library.md)) 。 如果 **LoadLibrary** 成功，則程式會在 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式中使用傳回的控制碼，以取得 DLL 的 myPuts 函式的位址。 呼叫 DLL 函式之後，程式會呼叫 [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) 函式來卸載 dll。

因為程式會使用執行時間動態連結，所以不需要將模組與 DLL 的匯入程式庫連結。

此範例說明執行時間與載入時間動態連結之間的重要差異。 如果 DLL 無法使用，則使用載入時間動態連結的應用程式必須直接終止。 不過，執行時間動態連結範例可以回應錯誤。


```C++
// A simple program that uses LoadLibrary and 
// GetProcAddress to access myPuts from Myputs.dll. 
 
#include <windows.h> 
#include <stdio.h> 
 
typedef int (__cdecl *MYPROC)(LPWSTR); 
 
int main( void ) 
{ 
    HINSTANCE hinstLib; 
    MYPROC ProcAdd; 
    BOOL fFreeResult, fRunTimeLinkSuccess = FALSE; 
 
    // Get a handle to the DLL module.
 
    hinstLib = LoadLibrary(TEXT("MyPuts.dll")); 
 
    // If the handle is valid, try to get the function address.
 
    if (hinstLib != NULL) 
    { 
        ProcAdd = (MYPROC) GetProcAddress(hinstLib, "myPuts"); 
 
        // If the function address is valid, call the function.
 
        if (NULL != ProcAdd) 
        {
            fRunTimeLinkSuccess = TRUE;
            (ProcAdd) (L"Message sent to the DLL function\n"); 
        }
        // Free the DLL module.
 
        fFreeResult = FreeLibrary(hinstLib); 
    } 

    // If unable to call the DLL function, use an alternative.
    if (! fRunTimeLinkSuccess) 
        printf("Message printed from executable\n"); 

    return 0;

}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[執行時間動態連結](run-time-dynamic-linking.md)
</dt> </dl>

 

 
