---
description: 雖然 DbgHelp.dll 隨附 Windows 的所有版本，但是呼叫端應該考慮使用此 DLL 的其中一個較新版本，如 Windows 封裝的偵錯工具中所找到。 如需 DbgHelp 散發的詳細資訊，請參閱 DbgHelp 版本。
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: 呼叫 DbgHelp 程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d6a111da8b0874a0c66fa08840e1ea4edeabf539afab2e9decf0eb19372db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957157"
---
# <a name="calling-the-dbghelp-library"></a>呼叫 DbgHelp 程式庫

雖然 DbgHelp.dll 隨附 Windows 的所有版本，但是呼叫端應該考慮使用此 DLL 的其中一個較新版本，如 Windows 封裝的[偵錯工具](https://www.microsoft.com/?ref=go)中所找到。 如需 DbgHelp 散發的詳細資訊，請參閱 [DbgHelp 版本](dbghelp-versions.md)。

使用 DbgHelp 時，最佳策略是從應用程式目錄中的 Windows 套件的[調試](https://www.microsoft.com/?ref=go)程式，在邏輯上與呼叫它的軟體相關的應用程式目錄中安裝程式庫複本。 如果也需要符號伺服器和來源伺服器，則 SymSrv.dll 和 SrcSrv.dll 都必須安裝在與 DbgHelp.dll 相同的目錄中，因為 DbgHelp 只會在與它們共用相同目錄時，才會呼叫這些 Dll。  (請注意，DbgHelp 不會從標準搜尋路徑呼叫這兩個 Dll。 ) 這有助於防止使用不相符的 Dll;同樣地，它也能提高整體安全性。

下列程式碼會從 DbgHelp 來源解壓縮。 它會顯示 DbgHelp 如何只從 DbgHelp.dll 所在的相同目錄載入 SymSrv.dll 和 SrcSrv.dll 的版本。


```C++
HINSTANCE ghinst;

// For calculating the size of arrays for safe string functions.

#ifndef cch
 #define ccht(Array, EltType) (sizeof(Array) / sizeof(EltType))
 #define cch(Array) ccht(Array, (Array)[0])
#endif

//
// LoadLibrary() a DLL, using the same directory as dbghelp.dll.
//

HMODULE 
LoadDLL(
    __in PCWSTR filename
    )
{
    WCHAR drive[10] = L"";
    WCHAR dir[MAX_PATH + 1] = L"";
    WCHAR file[MAX_PATH + 1] = L"";
    WCHAR ext[MAX_PATH + 1] = L"";
    WCHAR path[MAX_PATH + 1] = L"";
    HMODULE hm;
    
    // Chop up 'filename' into its elements.
    
    _wsplitpath_s(filename, drive, cch(drive), dir, cch(dir), file, cch(file), ext, cch(ext));

    // If 'filename' contains no path information, then get the path to our module and 
    // use it to create a fully qualified path to the module we are loading.  Then load it.
    
    if (!*drive && !*dir) 
    {
        // ghinst is the HINSTANCE of this module, initialized in DllMain or WinMain
         
        if (GetModuleFileNameW(ghinst, path, MAX_PATH)) 
        {
            _wsplitpath_s(path, drive, cch(drive), dir, cch(dir), NULL, 0, NULL, 0);
            if (*drive || *dir) 
            {
                swprintf_s(path, cch(path), L"%s%s%s%s", drive, dir, file, ext);
                hm = LoadLibrary(path);
                if (hm)
                    return hm;
            }
        }
    }
    else
    {
        // If we wanted to, we could have LoadDLL also support directories being specified
        // in 'filename'.  We could pass the path here.  The result is if no path is specified,
        // the module path is used as above, otherwise the path in 'filename' is specified.
        // But the standard search logic of LoadLibrary is still avoided.
        
        /*
        hm = LoadLibrary(path);
        if (hm)
            return hm;
        */
    }
    
    return 0;
}
```



載入這兩個 Dll 之後，DbgHelp 會呼叫 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 來取得其所需的函數。

一般來說，呼叫 DbgHelp.dll 的程式碼會在與起始目前進程的應用程式相同的目錄中安裝 DbgHelp.dll，以確保載入的是正確的版本。 如果呼叫程式碼位於 DLL 中，而且無法存取或知道初始進程的位置，則 DbgHelp.dll 必須與呼叫 DLL 一起安裝，並使用類似 DbgHelp LoadDLL 的程式碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DbgHelp 版本](dbghelp-versions.md)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
