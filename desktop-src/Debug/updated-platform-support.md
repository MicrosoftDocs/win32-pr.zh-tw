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
# <a name="updated-platform-support"></a><span data-ttu-id="52e89-103">更新的平臺支援</span><span class="sxs-lookup"><span data-stu-id="52e89-103">Updated Platform Support</span></span>

<span data-ttu-id="52e89-104">必要時，DbgHelp 程式庫已加寬，以支援32和64位的 Windows。</span><span class="sxs-lookup"><span data-stu-id="52e89-104">Where necessary, the DbgHelp library has been widened to support both 32- and 64-bit Windows.</span></span> <span data-ttu-id="52e89-105">原始的函式和結構定義仍在 DbgHelp 中，但這些定義的更新版本也與64位的視窗相容。</span><span class="sxs-lookup"><span data-stu-id="52e89-105">The original function and structure definitions are still in DbgHelp.h, but there are also updated versions of these definitions that are compatible with 64-bit Windows.</span></span> <span data-ttu-id="52e89-106">如果您在程式碼中使用更新的函式，則可以針對 32-和64位 Windows 進行編譯。</span><span class="sxs-lookup"><span data-stu-id="52e89-106">If you use the updated functions in your code, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="52e89-107">您的程式碼也會更有效率，因為原始函式只會呼叫更新的函式來執行工作。</span><span class="sxs-lookup"><span data-stu-id="52e89-107">Your code will also be more efficient, since the original functions simply call the updated functions to perform the work.</span></span>

<span data-ttu-id="52e89-108">例如，DbgHelp 包含 **SymUnloadModule** (原始函式的定義) 和 **SymUnloadModule64** (更新函數) 。</span><span class="sxs-lookup"><span data-stu-id="52e89-108">For example, DbgHelp.h contains definitions for **SymUnloadModule** (original function) and **SymUnloadModule64** (updated function).</span></span> <span data-ttu-id="52e89-109">這些定義幾乎完全相同，但會針對 *BaseOfDll* 參數使用不同的類型。</span><span class="sxs-lookup"><span data-stu-id="52e89-109">These definitions are nearly identical, but use different types for the *BaseOfDll* parameter.</span></span> <span data-ttu-id="52e89-110"> (**SymUnloadModule** 會使用 **DWORD** 類型，而 **SymUnloadModule64** 則會使用 **DWORD64** 類型。 ) 如果您撰寫程式碼來使用 **SymUnloadModule64**，則可以針對 32-和64位 Windows 進行編譯。</span><span class="sxs-lookup"><span data-stu-id="52e89-110">(**SymUnloadModule** uses the **DWORD** type, while **SymUnloadModule64** uses the **DWORD64** type.) If you write your code to use **SymUnloadModule64**, it can be compiled for both 32- and 64-bit Windows.</span></span> <span data-ttu-id="52e89-111">除了呼叫 **SymUnloadModule**，程式碼也會更有效率。</span><span class="sxs-lookup"><span data-stu-id="52e89-111">The code is also more efficient than if it were to call **SymUnloadModule**.</span></span>

<span data-ttu-id="52e89-112">以下是已更新的函式清單：</span><span class="sxs-lookup"><span data-stu-id="52e89-112">The following is a list of the updated functions:</span></span>

<dl>

[<span data-ttu-id="52e89-113">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="52e89-113">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="52e89-114">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="52e89-114">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="52e89-115">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="52e89-115">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="52e89-116">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="52e89-116">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="52e89-117">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="52e89-117">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="52e89-118">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="52e89-118">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="52e89-119">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="52e89-119">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="52e89-120">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="52e89-120">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="52e89-121">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="52e89-121">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="52e89-122">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="52e89-122">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="52e89-123">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="52e89-123">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="52e89-124">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="52e89-124">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="52e89-125">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="52e89-125">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="52e89-126">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="52e89-126">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="52e89-127">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="52e89-127">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="52e89-128">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="52e89-128">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="52e89-129">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="52e89-129">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="52e89-130">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="52e89-130">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="52e89-131">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="52e89-131">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="52e89-132">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="52e89-132">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

<span data-ttu-id="52e89-133">以下是已更新結構的清單：</span><span class="sxs-lookup"><span data-stu-id="52e89-133">The following is a list of the updated structures:</span></span>

<dl>

[<span data-ttu-id="52e89-134">**ADDRESS64**</span><span class="sxs-lookup"><span data-stu-id="52e89-134">**ADDRESS64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-address)  
[<span data-ttu-id="52e89-135">**IMAGEHLP.DLL \_ 延後 \_ 符號 \_ LOAD64**</span><span class="sxs-lookup"><span data-stu-id="52e89-135">**IMAGEHLP\_DEFERRED\_SYMBOL\_LOAD64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_deferred_symbol_load)  
[<span data-ttu-id="52e89-136">**IMAGEHLP.DLL \_ 重複的 \_ SYMBOL64**</span><span class="sxs-lookup"><span data-stu-id="52e89-136">**IMAGEHLP\_DUPLICATE\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_duplicate_symbol)  
[<span data-ttu-id="52e89-137">**IMAGEHLP.DLL \_ LINE64**</span><span class="sxs-lookup"><span data-stu-id="52e89-137">**IMAGEHLP\_LINE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line)  
[<span data-ttu-id="52e89-138">**IMAGEHLP.DLL \_ MODULE64**</span><span class="sxs-lookup"><span data-stu-id="52e89-138">**IMAGEHLP\_MODULE64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_module)  
[<span data-ttu-id="52e89-139">**IMAGEHLP.DLL \_ SYMBOL64**</span><span class="sxs-lookup"><span data-stu-id="52e89-139">**IMAGEHLP\_SYMBOL64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_symbol)  
[<span data-ttu-id="52e89-140">**KDHELP64**</span><span class="sxs-lookup"><span data-stu-id="52e89-140">**KDHELP64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-kdhelp)  
[<span data-ttu-id="52e89-141">**STACKFRAME64**</span><span class="sxs-lookup"><span data-stu-id="52e89-141">**STACKFRAME64**</span></span>](/windows/desktop/api/DbgHelp/ns-dbghelp-stackframe)  
</dl>

 

 



