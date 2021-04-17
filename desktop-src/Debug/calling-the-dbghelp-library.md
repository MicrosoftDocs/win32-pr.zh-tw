---
description: 雖然 DbgHelp.dll 隨附于所有版本的 Windows，但呼叫端應該考慮使用這個 DLL 的其中一個較新版本，如 Windows 封裝的偵錯工具中所找到。 如需 DbgHelp 散發的詳細資訊，請參閱 DbgHelp 版本。
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: 呼叫 DbgHelp 程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc06f6a0e28f163d80490647ee8f33754c249b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104467961"
---
# <a name="calling-the-dbghelp-library"></a><span data-ttu-id="b68bd-104">呼叫 DbgHelp 程式庫</span><span class="sxs-lookup"><span data-stu-id="b68bd-104">Calling the DbgHelp Library</span></span>

<span data-ttu-id="b68bd-105">雖然 DbgHelp.dll 隨附于所有版本的 Windows，但呼叫端應該考慮使用這個 DLL 的其中一個較新版本，如 Windows 封裝的 [偵錯工具](https://www.microsoft.com/?ref=go) 中所找到。</span><span class="sxs-lookup"><span data-stu-id="b68bd-105">Although DbgHelp.dll ships with all versions of Windows, callers should consider using one of the more recent versions of this DLL as found in the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package.</span></span> <span data-ttu-id="b68bd-106">如需 DbgHelp 散發的詳細資訊，請參閱 [DbgHelp 版本](dbghelp-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="b68bd-106">For details on distribution of DbgHelp, see [DbgHelp Versions](dbghelp-versions.md).</span></span>

<span data-ttu-id="b68bd-107">使用 DbgHelp 時，最佳策略是從應用程式目錄中的 Windows 封裝的 [調試](https://www.microsoft.com/?ref=go) 程式，在邏輯上與呼叫它的軟體相關的應用程式目錄中安裝程式庫複本。</span><span class="sxs-lookup"><span data-stu-id="b68bd-107">When using DbgHelp, the best strategy is to install a copy of the library from the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package in the application directory logically adjacent to the software that calls it.</span></span> <span data-ttu-id="b68bd-108">如果也需要符號伺服器和來源伺服器，則 SymSrv.dll 和 SrcSrv.dll 都必須安裝在與 DbgHelp.dll 相同的目錄中，因為 DbgHelp 只會在與它們共用相同目錄時，才會呼叫這些 Dll。</span><span class="sxs-lookup"><span data-stu-id="b68bd-108">If Symbol Server and Source Server are also needed, then both SymSrv.dll and SrcSrv.dll must be installed in the same directory as DbgHelp.dll, as DbgHelp will only call these DLLs if they share the same directory with it.</span></span> <span data-ttu-id="b68bd-109"> (請注意，DbgHelp 不會從標準搜尋路徑呼叫這兩個 Dll。 ) 這有助於防止使用不相符的 Dll;同樣地，它也能提高整體安全性。</span><span class="sxs-lookup"><span data-stu-id="b68bd-109">(Note that DbgHelp will not call these two DLLs from the standard search path.) This helps prevent the usage of mismatched DLLs; likewise, it also improves security overall.</span></span>

<span data-ttu-id="b68bd-110">下列程式碼會從 DbgHelp 來源解壓縮。</span><span class="sxs-lookup"><span data-stu-id="b68bd-110">The following code is extracted from the DbgHelp source.</span></span> <span data-ttu-id="b68bd-111">它會顯示 DbgHelp 如何只從 DbgHelp.dll 所在的相同目錄載入 SymSrv.dll 和 SrcSrv.dll 的版本。</span><span class="sxs-lookup"><span data-stu-id="b68bd-111">It shows how DbgHelp only loads versions of SymSrv.dll and SrcSrv.dll from the same directory that DbgHelp.dll resides in.</span></span>


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



<span data-ttu-id="b68bd-112">載入這兩個 Dll 之後，DbgHelp 會呼叫 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 來取得其所需的函數。</span><span class="sxs-lookup"><span data-stu-id="b68bd-112">After loading these two DLLs, DbgHelp calls [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain the functions it needs from them.</span></span>

<span data-ttu-id="b68bd-113">一般來說，呼叫 DbgHelp.dll 的程式碼會在與起始目前進程的應用程式相同的目錄中安裝 DbgHelp.dll，以確保載入的是正確的版本。</span><span class="sxs-lookup"><span data-stu-id="b68bd-113">Normally, code that calls DbgHelp.dll ensures that the correct version is loaded by installing DbgHelp.dll in the same directory as the application that initiated the current process.</span></span> <span data-ttu-id="b68bd-114">如果呼叫程式碼位於 DLL 中，而且無法存取或知道初始進程的位置，則 DbgHelp.dll 必須與呼叫 DLL 一起安裝，並使用類似 DbgHelp LoadDLL 的程式碼。</span><span class="sxs-lookup"><span data-stu-id="b68bd-114">If the calling code is in a DLL and does not have access to or knowledge of the location of the initial process, then DbgHelp.dll must be installed alongside the calling DLL and code similar to DbgHelp's LoadDLL should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b68bd-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b68bd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b68bd-116">DbgHelp 版本</span><span class="sxs-lookup"><span data-stu-id="b68bd-116">DbgHelp Versions</span></span>](dbghelp-versions.md)
</dt> <dt>

[<span data-ttu-id="b68bd-117">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="b68bd-117">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="b68bd-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="b68bd-118">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="b68bd-119">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="b68bd-119">**GetModuleFileName**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
