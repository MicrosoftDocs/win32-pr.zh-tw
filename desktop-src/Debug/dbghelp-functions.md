---
description: 以下是 DbgHelp 函數。
ms.assetid: 7b28f70b-2d97-4cc2-8064-dfb806f9cffa
title: DbgHelp 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db65e46fe407b26b1a6ec9ae3cb8d5d7301d5821
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510679"
---
# <a name="dbghelp-functions"></a>DbgHelp 函式

以下是 DbgHelp 函數。

## <a name="general"></a>一般

以下是一般 helper 函式：

<dl>

[**EnumDirTree**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumdirtree)  
[**ImagehlpApiVersion**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversion)  
[**ImagehlpApiVersionEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversionex)  
[**MakeSureDirectoryPathExists**](/windows/desktop/api/Dbghelp/nf-dbghelp-makesuredirectorypathexists)  
[**SearchTreeForFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-searchtreeforfile)  
</dl>

## <a name="debugger"></a>偵錯工具

偵錯工具服務函式是最適合偵錯工具或應用程式中的偵錯工具程式碼使用的函式。 這些函式可與符號處理常式函式搭配使用，以便更容易使用。

<dl>

[**EnumerateLoadedModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[**EnumerateLoadedModulesEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodulesex)  
[**FindDebugInfoFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofile)  
[**FindDebugInfoFileEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofileex)  
[**FindExecutableImage**](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimage)  
[**FindExecutableImageEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimageex)  
[**StackWalk64**](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[**SymSetParentWindow**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetparentwindow)  
[**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)  
</dl>

## <a name="image-access"></a>影像存取

影像存取功能可存取可執行映射中的資料。 這些函式可提供映射基底的高階存取，以及對影像資料最常見部分的非常特定存取。

<dl>

[**GetTimestampForLoadedLibrary**](/windows/desktop/api/Dbghelp/nf-dbghelp-gettimestampforloadedlibrary)  
[**ImageDirectoryEntryToData**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodata)  
[**ImageDirectoryEntryToDataEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodataex)  
[**ImageNtHeader**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagentheader)  
[**ImageRvaToSection**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatosection)  
[**ImageRvaToVa**](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatova)  
</dl>

## <a name="symbol-handler"></a>符號處理常式

[符號處理常式](symbol-handling.md)函式可讓應用程式輕鬆且可攜存取影像的符號調試資訊。 這些函數應該專門用來確保存取符號資訊。 這是必要的，因為這些函式會從符號格式隔離應用程式。

<dl>

[**SymAddSourceStream**](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsourcestream)  
[**SymAddSymbol**](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsymbol)  
[**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)  
[**SymDeleteSymbol**](/windows/desktop/api/Dbghelp/nf-dbghelp-symdeletesymbol)  
[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[**SymEnumLines**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumlines)  
[**SymEnumProcesses**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumprocesses)  
[**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles)  
[**SymEnumSourceLines**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcelines)  
[**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)  
[**SymEnumSymbolsForAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbolsforaddr)  
[**SymEnumTypes**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypes)  
[**SymEnumTypesByName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypesbyname)  
[**SymFindDebugInfoFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfinddebuginfofile)  
[**SymFindExecutableImage**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfindexecutableimage)  
[**SymFindFileInPath**](/windows/desktop/api/DbgHelp/nf-dbghelp-symfindfileinpath)  
[**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr)  
[**SymFromIndex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromindex)  
[**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname)  
[**SymFromToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromtoken)  
[**SymFunctionTableAccess64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[**SymGetFileLineOffsets64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetfilelineoffsets64)  
[**SymGetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgethomedirectory)  
[**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[**SymGetLineNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[**SymGetLinePrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[**SymGetModuleBase64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[**SymGetModuleInfo64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[**SymGetOmaps**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetomaps)  
[**SymGetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetoptions)  
[**SymGetScope**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetscope)  
[**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)  
[**SymGetSymbolFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymbolfile)  
[**SymGetTypeFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypefromname)  
[**SymGetTypeInfo**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfo)  
[**SymGetTypeInfoEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfoex)  
[**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  
[**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)  
[**SymMatchFileName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symmatchfilename)  
[**SymMatchString**](/windows/desktop/api/DbgHelp/nf-dbghelp-symmatchstring)  
[**SymNext**](/windows/desktop/api/DbgHelp/nf-dbghelp-symnext)  
[**SymPrev**](/windows/desktop/api/DbgHelp/nf-dbghelp-symprev)  
[**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)  
[**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[**SymRegisterFunctionEntryCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[**SymSearch**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsearch)  
[**SymSetCoNtext**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext)  
[**SymSetHomeDirectory**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)  
[**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)  
[**SymSetScopeFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromaddr)  
[**SymSetScopeFromIndex**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromindex)  
[**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)  
[**SymUnDName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

## <a name="symbol-server"></a>符號伺服器

[符號伺服器](symbol-servers-and-symbol-stores.md)可讓偵錯工具自動取得正確的符號檔，而不包含產品名稱、版本或組建編號。 下列函式會搭配符號伺服器使用。

<dl>

[**SymSrvDeltaName**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvdeltaname)  
[**SymSrvGetFileIndexes**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexes)  
[**SymSrvGetFileIndexInfo**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsrvgetfileindexinfo)  
[**SymSrvGetFileIndexString**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexstring)  
[**SymSrvGetSupplement**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetsupplement)  
[**SymSrvIsStore**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvisstore)  
[**SymSrvStoreFile**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstorefile)  
[**SymSrvStoreSupplement**](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstoresupplement)  
</dl>

## <a name="user-mode-minidump-files"></a>使用者模式小型傾印檔案

小型傾印函式提供一種方法，讓應用程式產生損毀傾印檔案，其中包含整個進程內容的實用子集;這就是所謂的 [小型](minidump-files.md)傾印檔案。 下列函式可用於小型傾印檔案。

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

## <a name="source-server"></a>來源伺服器

[來源伺服器](source-server-and-source-indexing.md) 可讓用戶端取出用來建立應用程式的原始程式檔的確切版本。 下列函式會搭配來源伺服器使用。

-   [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)
-   [**SymEnumSourceFileTokens**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsourcefiletokens)
-   [**SymEnumSourceFileTokensProc**](/windows/desktop/api/Dbghelp/nc-dbghelp-penumsourcefiletokenscallback)
-   [**SymGetSourceFileFromToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefilefromtoken)
-   [**SymGetSourceFileToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefiletoken)
-   [**SymGetSourceVarFromToken**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcevarfromtoken)

## <a name="obsolete-functions"></a>過時的函式

<dl>

[**MapDebugInformation**](/windows/desktop/api/Dbghelp/nf-dbghelp-mapdebuginformation)  
[**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[**SymGetSymNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[**SymGetSymPrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[**UnMapDebugInformation**](/windows/desktop/api/Dbghelp/nf-dbghelp-unmapdebuginformation)  
</dl>

 

 



