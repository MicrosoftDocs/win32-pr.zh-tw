---
description: MUI：系統設定應用程式範例
ms.assetid: 34cfd3a8-20b2-4a57-bc43-8da410cf9ae9
title: MUI：系統設定應用程式範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27871f3878c695b85b2131916185c62bc4a3dc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983354"
---
# <a name="mui-system-settings-application-sample"></a>MUI：系統設定應用程式範例

本主題所述的範例應用程式是簡單的 Hello MUI 應用程式，支援其使用者介面語言的系統設定。


```C++
// Vista and later enabled application, this application will not work on OS versions prior to Vista

#include <windows.h>
#include <wchar.h>
#include <strsafe.h>
#include "resource.h"

#define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
#define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)

int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
{
    UNREFERENCED_PARAMETER(hInstance);
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);
    UNREFERENCED_PARAMETER(nCmdShow);

    // The following code presents a hypothetical, yet common use pattern of MUI technology
    WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

    // 1. Basic application obtains access to the proper resource container 
    // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
    // LoadLibraryEx is the preferred alternative for resource modules as used below because it
    // provides increased security and performance over that of LoadLibrary
    HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
    if(!resContainer)
    {
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
        MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
        return 1; // exit
    }

    // 2. Application parses the resource container to find the appropriate item
    WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
    if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
    {
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
        MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
        FreeLibrary(resContainer);
        return 1; // exit
    }

    // 3. Application presents the discovered resource to the user via UI
    swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
    MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

    // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
    if(!FreeLibrary(resContainer))
    {
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
        MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
        return 1; // exit
    }

    return 0;
}
```



 

 



