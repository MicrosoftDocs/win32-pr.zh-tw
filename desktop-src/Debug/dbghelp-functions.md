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
# <a name="dbghelp-functions"></a><span data-ttu-id="19ba5-103">DbgHelp 函式</span><span class="sxs-lookup"><span data-stu-id="19ba5-103">DbgHelp Functions</span></span>

<span data-ttu-id="19ba5-104">以下是 DbgHelp 函數。</span><span class="sxs-lookup"><span data-stu-id="19ba5-104">The following are the DbgHelp functions.</span></span>

## <a name="general"></a><span data-ttu-id="19ba5-105">一般</span><span class="sxs-lookup"><span data-stu-id="19ba5-105">General</span></span>

<span data-ttu-id="19ba5-106">以下是一般 helper 函式：</span><span class="sxs-lookup"><span data-stu-id="19ba5-106">The following are general helper functions:</span></span>

<dl>

[<span data-ttu-id="19ba5-107">**EnumDirTree**</span><span class="sxs-lookup"><span data-stu-id="19ba5-107">**EnumDirTree**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumdirtree)  
[<span data-ttu-id="19ba5-108">**ImagehlpApiVersion**</span><span class="sxs-lookup"><span data-stu-id="19ba5-108">**ImagehlpApiVersion**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversion)  
[<span data-ttu-id="19ba5-109">**ImagehlpApiVersionEx**</span><span class="sxs-lookup"><span data-stu-id="19ba5-109">**ImagehlpApiVersionEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagehlpapiversionex)  
[<span data-ttu-id="19ba5-110">**MakeSureDirectoryPathExists**</span><span class="sxs-lookup"><span data-stu-id="19ba5-110">**MakeSureDirectoryPathExists**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-makesuredirectorypathexists)  
[<span data-ttu-id="19ba5-111">**SearchTreeForFile**</span><span class="sxs-lookup"><span data-stu-id="19ba5-111">**SearchTreeForFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-searchtreeforfile)  
</dl>

## <a name="debugger"></a><span data-ttu-id="19ba5-112">偵錯工具</span><span class="sxs-lookup"><span data-stu-id="19ba5-112">Debugger</span></span>

<span data-ttu-id="19ba5-113">偵錯工具服務函式是最適合偵錯工具或應用程式中的偵錯工具程式碼使用的函式。</span><span class="sxs-lookup"><span data-stu-id="19ba5-113">The debugging service functions are the functions most suited for use by a debugger or the debugging code in an application.</span></span> <span data-ttu-id="19ba5-114">這些函式可與符號處理常式函式搭配使用，以便更容易使用。</span><span class="sxs-lookup"><span data-stu-id="19ba5-114">These functions can be used in concert with the symbol handler functions for easier use.</span></span>

<dl>

[<span data-ttu-id="19ba5-115">**EnumerateLoadedModules64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-115">**EnumerateLoadedModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodules)  
[<span data-ttu-id="19ba5-116">**EnumerateLoadedModulesEx**</span><span class="sxs-lookup"><span data-stu-id="19ba5-116">**EnumerateLoadedModulesEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-enumerateloadedmodulesex)  
[<span data-ttu-id="19ba5-117">**FindDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="19ba5-117">**FindDebugInfoFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofile)  
[<span data-ttu-id="19ba5-118">**FindDebugInfoFileEx**</span><span class="sxs-lookup"><span data-stu-id="19ba5-118">**FindDebugInfoFileEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-finddebuginfofileex)  
[<span data-ttu-id="19ba5-119">**FindExecutableImage**</span><span class="sxs-lookup"><span data-stu-id="19ba5-119">**FindExecutableImage**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimage)  
[<span data-ttu-id="19ba5-120">**FindExecutableImageEx**</span><span class="sxs-lookup"><span data-stu-id="19ba5-120">**FindExecutableImageEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-findexecutableimageex)  
[<span data-ttu-id="19ba5-121">**StackWalk64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-121">**StackWalk64**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-stackwalk)  
[<span data-ttu-id="19ba5-122">**SymSetParentWindow**</span><span class="sxs-lookup"><span data-stu-id="19ba5-122">**SymSetParentWindow**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetparentwindow)  
[<span data-ttu-id="19ba5-123">**UnDecorateSymbolName**</span><span class="sxs-lookup"><span data-stu-id="19ba5-123">**UnDecorateSymbolName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname)  
</dl>

## <a name="image-access"></a><span data-ttu-id="19ba5-124">影像存取</span><span class="sxs-lookup"><span data-stu-id="19ba5-124">Image Access</span></span>

<span data-ttu-id="19ba5-125">影像存取功能可存取可執行映射中的資料。</span><span class="sxs-lookup"><span data-stu-id="19ba5-125">The image access functions access the data in an executable image.</span></span> <span data-ttu-id="19ba5-126">這些函式可提供映射基底的高階存取，以及對影像資料最常見部分的非常特定存取。</span><span class="sxs-lookup"><span data-stu-id="19ba5-126">The functions provide high-level access to the base of images and very specific access to the most common parts of an image's data.</span></span>

<dl>

[<span data-ttu-id="19ba5-127">**GetTimestampForLoadedLibrary**</span><span class="sxs-lookup"><span data-stu-id="19ba5-127">**GetTimestampForLoadedLibrary**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-gettimestampforloadedlibrary)  
[<span data-ttu-id="19ba5-128">**ImageDirectoryEntryToData**</span><span class="sxs-lookup"><span data-stu-id="19ba5-128">**ImageDirectoryEntryToData**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodata)  
[<span data-ttu-id="19ba5-129">**ImageDirectoryEntryToDataEx**</span><span class="sxs-lookup"><span data-stu-id="19ba5-129">**ImageDirectoryEntryToDataEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagedirectoryentrytodataex)  
[<span data-ttu-id="19ba5-130">**ImageNtHeader**</span><span class="sxs-lookup"><span data-stu-id="19ba5-130">**ImageNtHeader**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagentheader)  
[<span data-ttu-id="19ba5-131">**ImageRvaToSection**</span><span class="sxs-lookup"><span data-stu-id="19ba5-131">**ImageRvaToSection**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatosection)  
[<span data-ttu-id="19ba5-132">**ImageRvaToVa**</span><span class="sxs-lookup"><span data-stu-id="19ba5-132">**ImageRvaToVa**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-imagervatova)  
</dl>

## <a name="symbol-handler"></a><span data-ttu-id="19ba5-133">符號處理常式</span><span class="sxs-lookup"><span data-stu-id="19ba5-133">Symbol Handler</span></span>

<span data-ttu-id="19ba5-134">[符號處理常式](symbol-handling.md)函式可讓應用程式輕鬆且可攜存取影像的符號調試資訊。</span><span class="sxs-lookup"><span data-stu-id="19ba5-134">The [symbol handler](symbol-handling.md) functions give applications easy and portable access to the symbolic debugging information of an image.</span></span> <span data-ttu-id="19ba5-135">這些函數應該專門用來確保存取符號資訊。</span><span class="sxs-lookup"><span data-stu-id="19ba5-135">These functions should be used exclusively to ensure access to symbolic information.</span></span> <span data-ttu-id="19ba5-136">這是必要的，因為這些函式會從符號格式隔離應用程式。</span><span class="sxs-lookup"><span data-stu-id="19ba5-136">This is necessary because these functions isolate the application from the symbol format.</span></span>

<dl>

[<span data-ttu-id="19ba5-137">**SymAddSourceStream**</span><span class="sxs-lookup"><span data-stu-id="19ba5-137">**SymAddSourceStream**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsourcestream)  
[<span data-ttu-id="19ba5-138">**SymAddSymbol**</span><span class="sxs-lookup"><span data-stu-id="19ba5-138">**SymAddSymbol**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symaddsymbol)  
[<span data-ttu-id="19ba5-139">**SymCleanup**</span><span class="sxs-lookup"><span data-stu-id="19ba5-139">**SymCleanup**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup)  
[<span data-ttu-id="19ba5-140">**SymDeleteSymbol**</span><span class="sxs-lookup"><span data-stu-id="19ba5-140">**SymDeleteSymbol**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symdeletesymbol)  
[<span data-ttu-id="19ba5-141">**SymEnumerateModules64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-141">**SymEnumerateModules64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules)  
[<span data-ttu-id="19ba5-142">**SymEnumLines**</span><span class="sxs-lookup"><span data-stu-id="19ba5-142">**SymEnumLines**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumlines)  
[<span data-ttu-id="19ba5-143">**SymEnumProcesses**</span><span class="sxs-lookup"><span data-stu-id="19ba5-143">**SymEnumProcesses**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumprocesses)  
[<span data-ttu-id="19ba5-144">**SymEnumSourceFiles**</span><span class="sxs-lookup"><span data-stu-id="19ba5-144">**SymEnumSourceFiles**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles)  
[<span data-ttu-id="19ba5-145">**SymEnumSourceLines**</span><span class="sxs-lookup"><span data-stu-id="19ba5-145">**SymEnumSourceLines**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcelines)  
[<span data-ttu-id="19ba5-146">**SymEnumSymbols**</span><span class="sxs-lookup"><span data-stu-id="19ba5-146">**SymEnumSymbols**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols)  
[<span data-ttu-id="19ba5-147">**SymEnumSymbolsForAddr**</span><span class="sxs-lookup"><span data-stu-id="19ba5-147">**SymEnumSymbolsForAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbolsforaddr)  
[<span data-ttu-id="19ba5-148">**SymEnumTypes**</span><span class="sxs-lookup"><span data-stu-id="19ba5-148">**SymEnumTypes**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypes)  
[<span data-ttu-id="19ba5-149">**SymEnumTypesByName**</span><span class="sxs-lookup"><span data-stu-id="19ba5-149">**SymEnumTypesByName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumtypesbyname)  
[<span data-ttu-id="19ba5-150">**SymFindDebugInfoFile**</span><span class="sxs-lookup"><span data-stu-id="19ba5-150">**SymFindDebugInfoFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfinddebuginfofile)  
[<span data-ttu-id="19ba5-151">**SymFindExecutableImage**</span><span class="sxs-lookup"><span data-stu-id="19ba5-151">**SymFindExecutableImage**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfindexecutableimage)  
[<span data-ttu-id="19ba5-152">**SymFindFileInPath**</span><span class="sxs-lookup"><span data-stu-id="19ba5-152">**SymFindFileInPath**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symfindfileinpath)  
[<span data-ttu-id="19ba5-153">**SymFromAddr**</span><span class="sxs-lookup"><span data-stu-id="19ba5-153">**SymFromAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr)  
[<span data-ttu-id="19ba5-154">**SymFromIndex**</span><span class="sxs-lookup"><span data-stu-id="19ba5-154">**SymFromIndex**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromindex)  
[<span data-ttu-id="19ba5-155">**SymFromName**</span><span class="sxs-lookup"><span data-stu-id="19ba5-155">**SymFromName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname)  
[<span data-ttu-id="19ba5-156">**SymFromToken**</span><span class="sxs-lookup"><span data-stu-id="19ba5-156">**SymFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromtoken)  
[<span data-ttu-id="19ba5-157">**SymFunctionTableAccess64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-157">**SymFunctionTableAccess64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symfunctiontableaccess)  
[<span data-ttu-id="19ba5-158">**SymGetFileLineOffsets64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-158">**SymGetFileLineOffsets64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetfilelineoffsets64)  
[<span data-ttu-id="19ba5-159">**SymGetHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="19ba5-159">**SymGetHomeDirectory**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgethomedirectory)  
[<span data-ttu-id="19ba5-160">**SymGetLineFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-160">**SymGetLineFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr)  
[<span data-ttu-id="19ba5-161">**SymGetLineFromName64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-161">**SymGetLineFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname)  
[<span data-ttu-id="19ba5-162">**SymGetLineNext64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-162">**SymGetLineNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinenext)  
[<span data-ttu-id="19ba5-163">**SymGetLinePrev64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-163">**SymGetLinePrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlineprev)  
[<span data-ttu-id="19ba5-164">**SymGetModuleBase64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-164">**SymGetModuleBase64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmodulebase)  
[<span data-ttu-id="19ba5-165">**SymGetModuleInfo64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-165">**SymGetModuleInfo64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetmoduleinfo)  
[<span data-ttu-id="19ba5-166">**SymGetOmaps**</span><span class="sxs-lookup"><span data-stu-id="19ba5-166">**SymGetOmaps**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetomaps)  
[<span data-ttu-id="19ba5-167">**SymGetOptions**</span><span class="sxs-lookup"><span data-stu-id="19ba5-167">**SymGetOptions**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetoptions)  
[<span data-ttu-id="19ba5-168">**SymGetScope**</span><span class="sxs-lookup"><span data-stu-id="19ba5-168">**SymGetScope**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetscope)  
[<span data-ttu-id="19ba5-169">**SymGetSearchPath**</span><span class="sxs-lookup"><span data-stu-id="19ba5-169">**SymGetSearchPath**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath)  
[<span data-ttu-id="19ba5-170">**SymGetSymbolFile**</span><span class="sxs-lookup"><span data-stu-id="19ba5-170">**SymGetSymbolFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymbolfile)  
[<span data-ttu-id="19ba5-171">**SymGetTypeFromName**</span><span class="sxs-lookup"><span data-stu-id="19ba5-171">**SymGetTypeFromName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypefromname)  
[<span data-ttu-id="19ba5-172">**SymGetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="19ba5-172">**SymGetTypeInfo**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfo)  
[<span data-ttu-id="19ba5-173">**SymGetTypeInfoEx**</span><span class="sxs-lookup"><span data-stu-id="19ba5-173">**SymGetTypeInfoEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgettypeinfoex)  
[<span data-ttu-id="19ba5-174">**SymInitialize**</span><span class="sxs-lookup"><span data-stu-id="19ba5-174">**SymInitialize**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)  
[<span data-ttu-id="19ba5-175">**SymLoadModule64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-175">**SymLoadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule)  
[<span data-ttu-id="19ba5-176">**SymLoadModuleEx**</span><span class="sxs-lookup"><span data-stu-id="19ba5-176">**SymLoadModuleEx**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex)  
[<span data-ttu-id="19ba5-177">**SymMatchFileName**</span><span class="sxs-lookup"><span data-stu-id="19ba5-177">**SymMatchFileName**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symmatchfilename)  
[<span data-ttu-id="19ba5-178">**SymMatchString**</span><span class="sxs-lookup"><span data-stu-id="19ba5-178">**SymMatchString**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symmatchstring)  
[<span data-ttu-id="19ba5-179">**SymNext**</span><span class="sxs-lookup"><span data-stu-id="19ba5-179">**SymNext**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symnext)  
[<span data-ttu-id="19ba5-180">**SymPrev**</span><span class="sxs-lookup"><span data-stu-id="19ba5-180">**SymPrev**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symprev)  
[<span data-ttu-id="19ba5-181">**SymRefreshModuleList**</span><span class="sxs-lookup"><span data-stu-id="19ba5-181">**SymRefreshModuleList**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist)  
[<span data-ttu-id="19ba5-182">**SymRegisterCallback64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-182">**SymRegisterCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback)  
[<span data-ttu-id="19ba5-183">**SymRegisterFunctionEntryCallback64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-183">**SymRegisterFunctionEntryCallback64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symregisterfunctionentrycallback)  
[<span data-ttu-id="19ba5-184">**SymSearch**</span><span class="sxs-lookup"><span data-stu-id="19ba5-184">**SymSearch**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsearch)  
[<span data-ttu-id="19ba5-185">**SymSetCoNtext**</span><span class="sxs-lookup"><span data-stu-id="19ba5-185">**SymSetContext**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetcontext)  
[<span data-ttu-id="19ba5-186">**SymSetHomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="19ba5-186">**SymSetHomeDirectory**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsethomedirectory)  
[<span data-ttu-id="19ba5-187">**SymSetOptions**</span><span class="sxs-lookup"><span data-stu-id="19ba5-187">**SymSetOptions**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions)  
[<span data-ttu-id="19ba5-188">**SymSetScopeFromAddr**</span><span class="sxs-lookup"><span data-stu-id="19ba5-188">**SymSetScopeFromAddr**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromaddr)  
[<span data-ttu-id="19ba5-189">**SymSetScopeFromIndex**</span><span class="sxs-lookup"><span data-stu-id="19ba5-189">**SymSetScopeFromIndex**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetscopefromindex)  
[<span data-ttu-id="19ba5-190">**SymSetSearchPath**</span><span class="sxs-lookup"><span data-stu-id="19ba5-190">**SymSetSearchPath**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)  
[<span data-ttu-id="19ba5-191">**SymUnDName64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-191">**SymUnDName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symundname)  
[<span data-ttu-id="19ba5-192">**SymUnloadModule64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-192">**SymUnloadModule64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule)  
</dl>

## <a name="symbol-server"></a><span data-ttu-id="19ba5-193">符號伺服器</span><span class="sxs-lookup"><span data-stu-id="19ba5-193">Symbol Server</span></span>

<span data-ttu-id="19ba5-194">[符號伺服器](symbol-servers-and-symbol-stores.md)可讓偵錯工具自動取得正確的符號檔，而不包含產品名稱、版本或組建編號。</span><span class="sxs-lookup"><span data-stu-id="19ba5-194">The [symbol server](symbol-servers-and-symbol-stores.md) enables debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="19ba5-195">下列函式會搭配符號伺服器使用。</span><span class="sxs-lookup"><span data-stu-id="19ba5-195">The following functions are used with the symbol server.</span></span>

<dl>

[<span data-ttu-id="19ba5-196">**SymSrvDeltaName**</span><span class="sxs-lookup"><span data-stu-id="19ba5-196">**SymSrvDeltaName**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvdeltaname)  
[<span data-ttu-id="19ba5-197">**SymSrvGetFileIndexes**</span><span class="sxs-lookup"><span data-stu-id="19ba5-197">**SymSrvGetFileIndexes**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexes)  
[<span data-ttu-id="19ba5-198">**SymSrvGetFileIndexInfo**</span><span class="sxs-lookup"><span data-stu-id="19ba5-198">**SymSrvGetFileIndexInfo**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symsrvgetfileindexinfo)  
[<span data-ttu-id="19ba5-199">**SymSrvGetFileIndexString**</span><span class="sxs-lookup"><span data-stu-id="19ba5-199">**SymSrvGetFileIndexString**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetfileindexstring)  
[<span data-ttu-id="19ba5-200">**SymSrvGetSupplement**</span><span class="sxs-lookup"><span data-stu-id="19ba5-200">**SymSrvGetSupplement**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvgetsupplement)  
[<span data-ttu-id="19ba5-201">**SymSrvIsStore**</span><span class="sxs-lookup"><span data-stu-id="19ba5-201">**SymSrvIsStore**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvisstore)  
[<span data-ttu-id="19ba5-202">**SymSrvStoreFile**</span><span class="sxs-lookup"><span data-stu-id="19ba5-202">**SymSrvStoreFile**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstorefile)  
[<span data-ttu-id="19ba5-203">**SymSrvStoreSupplement**</span><span class="sxs-lookup"><span data-stu-id="19ba5-203">**SymSrvStoreSupplement**</span></span>](/windows/desktop/api/DbgHelp/nf-dbghelp-symsrvstoresupplement)  
</dl>

## <a name="user-mode-minidump-files"></a><span data-ttu-id="19ba5-204">使用者模式小型傾印檔案</span><span class="sxs-lookup"><span data-stu-id="19ba5-204">User-mode Minidump Files</span></span>

<span data-ttu-id="19ba5-205">小型傾印函式提供一種方法，讓應用程式產生損毀傾印檔案，其中包含整個進程內容的實用子集;這就是所謂的 [小型](minidump-files.md)傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="19ba5-205">The minidump functions provide a way for applications to produce crashdump files that contain a useful subset of the entire process context; this is known as a [minidump file](minidump-files.md).</span></span> <span data-ttu-id="19ba5-206">下列函式可用於小型傾印檔案。</span><span class="sxs-lookup"><span data-stu-id="19ba5-206">The following functions are used with minidump files.</span></span>

<dl>

[<span data-ttu-id="19ba5-207">**MiniDumpCallback**</span><span class="sxs-lookup"><span data-stu-id="19ba5-207">**MiniDumpCallback**</span></span>](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[<span data-ttu-id="19ba5-208">**MiniDumpReadDumpStream**</span><span class="sxs-lookup"><span data-stu-id="19ba5-208">**MiniDumpReadDumpStream**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[<span data-ttu-id="19ba5-209">**MiniDumpWriteDump**</span><span class="sxs-lookup"><span data-stu-id="19ba5-209">**MiniDumpWriteDump**</span></span>](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

## <a name="source-server"></a><span data-ttu-id="19ba5-210">來源伺服器</span><span class="sxs-lookup"><span data-stu-id="19ba5-210">Source Server</span></span>

<span data-ttu-id="19ba5-211">[來源伺服器](source-server-and-source-indexing.md) 可讓用戶端取出用來建立應用程式的原始程式檔的確切版本。</span><span class="sxs-lookup"><span data-stu-id="19ba5-211">[Source server](source-server-and-source-indexing.md) enables a client to retrieve the exact version of the source files that were used to build an application.</span></span> <span data-ttu-id="19ba5-212">下列函式會搭配來源伺服器使用。</span><span class="sxs-lookup"><span data-stu-id="19ba5-212">The following functions are used with source server.</span></span>

-   [<span data-ttu-id="19ba5-213">**SymGetSourceFile**</span><span class="sxs-lookup"><span data-stu-id="19ba5-213">**SymGetSourceFile**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile)
-   [<span data-ttu-id="19ba5-214">**SymEnumSourceFileTokens**</span><span class="sxs-lookup"><span data-stu-id="19ba5-214">**SymEnumSourceFileTokens**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsourcefiletokens)
-   [<span data-ttu-id="19ba5-215">**SymEnumSourceFileTokensProc**</span><span class="sxs-lookup"><span data-stu-id="19ba5-215">**SymEnumSourceFileTokensProc**</span></span>](/windows/desktop/api/Dbghelp/nc-dbghelp-penumsourcefiletokenscallback)
-   [<span data-ttu-id="19ba5-216">**SymGetSourceFileFromToken**</span><span class="sxs-lookup"><span data-stu-id="19ba5-216">**SymGetSourceFileFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefilefromtoken)
-   [<span data-ttu-id="19ba5-217">**SymGetSourceFileToken**</span><span class="sxs-lookup"><span data-stu-id="19ba5-217">**SymGetSourceFileToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefiletoken)
-   [<span data-ttu-id="19ba5-218">**SymGetSourceVarFromToken**</span><span class="sxs-lookup"><span data-stu-id="19ba5-218">**SymGetSourceVarFromToken**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcevarfromtoken)

## <a name="obsolete-functions"></a><span data-ttu-id="19ba5-219">過時的函式</span><span class="sxs-lookup"><span data-stu-id="19ba5-219">Obsolete Functions</span></span>

<dl>

[<span data-ttu-id="19ba5-220">**MapDebugInformation**</span><span class="sxs-lookup"><span data-stu-id="19ba5-220">**MapDebugInformation**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-mapdebuginformation)  
[<span data-ttu-id="19ba5-221">**SymEnumerateSymbols64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-221">**SymEnumerateSymbols64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratesymbols)  
[<span data-ttu-id="19ba5-222">**SymGetSymFromAddr64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-222">**SymGetSymFromAddr64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromaddr)  
[<span data-ttu-id="19ba5-223">**SymGetSymFromName64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-223">**SymGetSymFromName64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymfromname)  
[<span data-ttu-id="19ba5-224">**SymGetSymNext64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-224">**SymGetSymNext64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymnext)  
[<span data-ttu-id="19ba5-225">**SymGetSymPrev64**</span><span class="sxs-lookup"><span data-stu-id="19ba5-225">**SymGetSymPrev64**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsymprev)  
[<span data-ttu-id="19ba5-226">**UnMapDebugInformation**</span><span class="sxs-lookup"><span data-stu-id="19ba5-226">**UnMapDebugInformation**</span></span>](/windows/desktop/api/Dbghelp/nf-dbghelp-unmapdebuginformation)  
</dl>

 

 



