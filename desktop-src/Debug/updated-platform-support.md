---
description: 必要時，DbgHelp 程式庫已加寬，以支援32和64位的 Windows。
ms.assetid: 34ec8cd3-3260-441d-b55f-4ea21c736eb1
title: 更新的平臺支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a7b0b4f5e343c1dbfcbb0d9434a662553c93d67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510578"
---
# <a name="updated-platform-support"></a>更新的平臺支援

必要時，DbgHelp 程式庫已加寬，以支援32和64位的 Windows。 原始的函式和結構定義仍在 DbgHelp 中，但這些定義的更新版本也與64位的視窗相容。 如果您在程式碼中使用更新的函式，則可以針對 32-和64位 Windows 進行編譯。 您的程式碼也會更有效率，因為原始函式只會呼叫更新的函式來執行工作。

例如，DbgHelp 包含 **SymUnloadModule** (原始函式的定義) 和 **SymUnloadModule64** (更新函數) 。 這些定義幾乎完全相同，但會針對 *BaseOfDll* 參數使用不同的類型。  (**SymUnloadModule** 會使用 **DWORD** 類型，而 **SymUnloadModule64** 則會使用 **DWORD64** 類型。 ) 如果您撰寫程式碼來使用 **SymUnloadModule64**，則可以針對 32-和64位 Windows 進行編譯。 除了呼叫 **SymUnloadModule**，程式碼也會更有效率。

以下是已更新的函式清單：

<dl>

[**EnumerateLoadedModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[**StackWalk64**](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[**SymEnumerateSymbols64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[**SymFunctionTableAccess64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[**SymGetLineNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[**SymGetLinePrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[**SymGetModuleBase64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[**SymGetModuleInfo64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[**SymGetSymFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[**SymGetSymFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[**SymGetSymNext64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[**SymGetSymPrev64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[**SymRegisterFunctionEntryCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[**SymUnDName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

以下是已更新結構的清單：

<dl>

[**ADDRESS64**](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[**IMAGEHLP.DLL \_ 延後 \_ 符號 \_ LOAD64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[**IMAGEHLP.DLL \_ 重複的 \_ SYMBOL64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[**IMAGEHLP.DLL \_ LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[**IMAGEHLP.DLL \_ MODULE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[**IMAGEHLP.DLL \_ SYMBOL64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[**KDHELP64**](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[**STACKFRAME64**](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



