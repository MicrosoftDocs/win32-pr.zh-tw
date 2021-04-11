---
description: 下列程式碼示範如何從符號處理常式取得和報告有關搜尋和載入模組和對應符號檔的詳細資訊狀態資訊。
ms.assetid: 1dd8af0e-280b-4fc4-bf75-45c5c7517365
title: 取得通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bebaed2683f329fa267bdc926063d0b763190400
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191032"
---
# <a name="getting-notifications"></a><span data-ttu-id="5d758-103">取得通知</span><span class="sxs-lookup"><span data-stu-id="5d758-103">Getting Notifications</span></span>

<span data-ttu-id="5d758-104">下列程式碼示範如何從符號處理常式取得和報告有關搜尋和載入模組和對應符號檔的詳細資訊狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="5d758-104">The following code shows how to obtain and report verbose status information from the symbol handler about searching for and loading of modules and the corresponding symbol files.</span></span>

<span data-ttu-id="5d758-105">許多熟悉 WinDbg 偵錯工具的人，可能還記得一個稱為「！ sym 雜訊」的命令。</span><span class="sxs-lookup"><span data-stu-id="5d758-105">Many familiar with the WinDbg debugger may remember a command called "!sym noisy".</span></span> <span data-ttu-id="5d758-106">使用者會使用此命令來判斷 WinDbg 為何或無法載入符號檔。</span><span class="sxs-lookup"><span data-stu-id="5d758-106">This command is used by the user to determine why WinDbg is or is not able to load symbol files.</span></span> <span data-ttu-id="5d758-107">它會顯示符號處理常式嘗試的所有專案的詳細資訊清單。</span><span class="sxs-lookup"><span data-stu-id="5d758-107">It shows a verbose listing of everything the symbol handler tries.</span></span>

<span data-ttu-id="5d758-108">這份清單也可供任何開發用戶端至 DbgHelp 符號處理常式的人使用。</span><span class="sxs-lookup"><span data-stu-id="5d758-108">This same listing is also available to anyone developing a client to the DbgHelp symbol handler.</span></span>

<span data-ttu-id="5d758-109">首先，使用 **SYMOPT \_ DEBUG** 來呼叫 [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) 。</span><span class="sxs-lookup"><span data-stu-id="5d758-109">First, call [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) with **SYMOPT\_DEBUG**.</span></span> <span data-ttu-id="5d758-110">這會導致 DbgHelp 開啟 debug 通知。</span><span class="sxs-lookup"><span data-stu-id="5d758-110">This causes DbgHelp to turn on debug notifications.</span></span>

<span data-ttu-id="5d758-111">呼叫 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)之後，請使用 [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) 來註冊每當發生有趣的事件時，DbgHelp 將呼叫的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="5d758-111">After calling [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), use [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) to register a callback function that DbgHelp will call whenever an interesting event occurs.</span></span> <span data-ttu-id="5d758-112">在此範例中，回呼函式稱為 [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback)。</span><span class="sxs-lookup"><span data-stu-id="5d758-112">In this example, the callback function is called [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback).</span></span> <span data-ttu-id="5d758-113">符號回呼函式會傳遞給它們可根據類型處理的動作碼。</span><span class="sxs-lookup"><span data-stu-id="5d758-113">Symbol callback functions are passed an assortment of action codes that they can handle according to type.</span></span> <span data-ttu-id="5d758-114">在此範例中，我們只會處理 **CBA \_ 事件** 動作程式碼。</span><span class="sxs-lookup"><span data-stu-id="5d758-114">In this example, we are handling only the **CBA\_EVENT** action code.</span></span> <span data-ttu-id="5d758-115">此函式會傳遞包含載入符號之程式中所發生事件詳細資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="5d758-115">This function passes a string containing verbose information about an event that occurred in the process of loading a symbol.</span></span> <span data-ttu-id="5d758-116">此事件可能是嘗試將可執行映射中的資料讀取至符號檔成功位置的任何專案。</span><span class="sxs-lookup"><span data-stu-id="5d758-116">This event could be anything from an attempt to read the data within an executable image to the successful location of a symbol file.</span></span> <span data-ttu-id="5d758-117">**SymRegisterCallbackProc64** 會顯示該字串，並傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="5d758-117">**SymRegisterCallbackProc64** displays that string and returns **TRUE**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d758-118">請確定您未處理的每個動作程式碼都傳回 **FALSE** ，否則您可能會遇到未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="5d758-118">Make sure you return **FALSE** to every action code that you do not handle, otherwise you may experience undefined behavior.</span></span> <span data-ttu-id="5d758-119">如需所有動作碼及其含意的清單，請參閱 [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) 。</span><span class="sxs-lookup"><span data-stu-id="5d758-119">Refer to [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) for a list of all the action codes and their implications.</span></span>

 

<span data-ttu-id="5d758-120">現在已註冊回呼，現在可以藉由呼叫 [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)，載入命令列上指定的模組。</span><span class="sxs-lookup"><span data-stu-id="5d758-120">Now that the callback is registered, it is time to load the module specified on the command line by calling [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex).</span></span>

<span data-ttu-id="5d758-121">最後，在結束之前呼叫 [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) 。</span><span class="sxs-lookup"><span data-stu-id="5d758-121">Lastly, call [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) before exiting.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#ifdef UNICODE
 #define DBGHELP_TRANSLATE_TCHAR
#endif
#include <dbghelp.h>

// Here is an implementation of a Symbol Callback function.

BOOL 
CALLBACK 
SymRegisterCallbackProc64(
    __in HANDLE hProcess,
    __in ULONG ActionCode,
    __in_opt ULONG64 CallbackData,
    __in_opt ULONG64 UserContext
    )
{
    UNREFERENCED_PARAMETER(hProcess);
    UNREFERENCED_PARAMETER(UserContext);
    
    PIMAGEHLP_CBA_EVENT evt;

    // If SYMOPT_DEBUG is set, then the symbol handler will pass
    // verbose information on its attempt to load symbols.
    // This information be delivered as text strings.
    
    switch (ActionCode)
    {
    case CBA_EVENT:
        evt = (PIMAGEHLP_CBA_EVENT)CallbackData;
        _tprintf(_T("%s"), (PTSTR)evt->desc);
        break;

    // CBA_DEBUG_INFO is the old ActionCode for symbol spew.
    // It still works, but we use CBA_EVENT in this example.
#if 0
    case CBA_DEBUG_INFO:
        _tprintf(_T("%s"), (PTSTR)CallbackData);
        break;
#endif

    default:
        // Return false to any ActionCode we don't handle
        // or we could generate some undesirable behavior.
        return FALSE;
    }

    return TRUE;
}

// Main code.

int __cdecl
#ifdef UNICODE
_tmain(
#else
main(
#endif
    __in int argc,
    __in_ecount(argc) PCTSTR argv[]
    )
{
    BOOL status;
    int rc = -1;
    HANDLE hProcess;
    DWORD64 module;
    
    if (argc < 2)
    {
        _tprintf(_T("You must specify an executable image to load.\n"));
        return rc;
    }

    // If we want to se debug spew, we need to set this option.
        
    SymSetOptions(SYMOPT_DEBUG);
    
    // We are not debugging an actual process, so lets use a placeholder
    // value of 1 for hProcess just to ID these calls from any other
    // series we may want to load.  For this simple case, anything will do.
    
    hProcess = (HANDLE)1;
    
    // Initialize the symbol handler.  No symbol path.  
    // Just let dbghelp use _NT_SYMBOL_PATH
    
    status = SymInitialize(hProcess, NULL, false);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymInitialize.\n"), GetLastError());
        return rc;
    }
     
    // Now register our callback.
    
    status = SymRegisterCallback64(hProcess, SymRegisterCallbackProc64, NULL);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymRegisterCallback64.\n"), GetLastError());
        goto cleanup;
    }
    
    // Go ahead and load a module for testing.
    
    module = SymLoadModuleEx(hProcess,  // our unique id
                             NULL,      // no open file handle to image
                             argv[1],   // name of image to load
                             NULL,      // no module name - dbghelp will get it
                             0,         // no base address - dbghelp will get it
                             0,         // no module size - dbghelp will get it
                             NULL,      // no special MODLOAD_DATA structure
                             0);        // flags
    if (!module)
    {
        _tprintf(_T("Error 0x%x calling SymLoadModuleEx.\n"), GetLastError());
        goto cleanup;
    }
    rc = 0;
    
cleanup:
    SymCleanup(hProcess);
    
    return rc;    
}
```



<span data-ttu-id="5d758-122">將 **Null** 指定為 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) 的第二個參數，表示符號處理常式應該使用預設搜尋路徑來尋找符號檔。</span><span class="sxs-lookup"><span data-stu-id="5d758-122">Specifying **NULL** as the second parameter of [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indicates that the symbol handler should use the default search path to locate symbol files.</span></span> <span data-ttu-id="5d758-123">如需有關符號處理常式如何尋找符號檔或應用程式如何指定符號搜尋路徑的詳細資訊，請參閱 [符號路徑](symbol-paths.md)。</span><span class="sxs-lookup"><span data-stu-id="5d758-123">For detailed information on how the symbol handler locates symbol files or how an application can specify a symbol search path, see [Symbol Paths](symbol-paths.md).</span></span>

<span data-ttu-id="5d758-124">執行此程式會顯示如何處理符號路徑。</span><span class="sxs-lookup"><span data-stu-id="5d758-124">Running this program shows how the symbol path is processed.</span></span> <span data-ttu-id="5d758-125">當 DbgHelp 查看符號路徑來尋找符號檔時，它會重複呼叫 [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) ，進而顯示 DbgHelp 傳遞的下列字串。</span><span class="sxs-lookup"><span data-stu-id="5d758-125">As DbgHelp looks through the symbol path to find the symbol file, it repeatedly calls [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) which, in turn, displays the following strings being passed by DbgHelp.</span></span>

``` syntax
d:\load.exe c:\home\dbghelp.dll
DBGHELP: No header for c:\home\dbghelp.dll.  Searching for image on disk
DBGHELP: c:\home\dbghelp.dll - OK
DBGHELP: .\dbghelp.pdb - file not found
DBGHELP: .\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\symbols\dll\dbghelp.pdb - file not found
DBGHELP: d:\nt.binaries.amd64chk\symbols.pri\dbg\dbghelp.pdb - file not found
DBGHELP: dbghelp - private symbols & lines
         dbghelp.pdb
```

 

 



