---
description: DbgHelp 程式庫會使用符號搜尋路徑來找出 ( .pdb 和 dbg 檔案) 的 debug 符號。 搜尋路徑可由一個或多個以分號分隔的路徑元素組成。
ms.assetid: 3527f589-285b-4cdf-b024-17920971a904
title: 符號路徑
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 977772e45c345e1e990dc038fccd852d17d279dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936202"
---
# <a name="symbol-paths"></a><span data-ttu-id="5d29f-104">符號路徑</span><span class="sxs-lookup"><span data-stu-id="5d29f-104">Symbol Paths</span></span>

<span data-ttu-id="5d29f-105">DbgHelp 程式庫會使用符號搜尋路徑來找出 ( .pdb 和 dbg 檔案) 的 debug 符號。</span><span class="sxs-lookup"><span data-stu-id="5d29f-105">The DbgHelp library uses the symbol search path to locate debug symbols (.pdb and .dbg files).</span></span> <span data-ttu-id="5d29f-106">搜尋路徑可由一個或多個以分號分隔的路徑元素組成。</span><span class="sxs-lookup"><span data-stu-id="5d29f-106">The search path can be made up of one or more path elements separated by semicolons.</span></span>

## <a name="specifying-search-paths"></a><span data-ttu-id="5d29f-107">指定搜尋路徑</span><span class="sxs-lookup"><span data-stu-id="5d29f-107">Specifying Search Paths</span></span>

<span data-ttu-id="5d29f-108">若要指定符號處理常式將在其中搜尋符號檔之磁碟目錄的位置，請呼叫 [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) 函式。</span><span class="sxs-lookup"><span data-stu-id="5d29f-108">To specify where the symbol handler will search disk directories for symbol files, call the [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) function.</span></span> <span data-ttu-id="5d29f-109">或者，您也可以在 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)函數的 *UserSearchPath* 參數中指定符號搜尋路徑。</span><span class="sxs-lookup"><span data-stu-id="5d29f-109">Alternatively, you can specify a symbol search path in the *UserSearchPath* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

<span data-ttu-id="5d29f-110">[**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)中的 *UserSearchPath* 參數和 [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)中的 *SearchPath* 參數會採用以 null 結束的字串指標，該字串會指定路徑或以分號分隔的路徑系列。</span><span class="sxs-lookup"><span data-stu-id="5d29f-110">The *UserSearchPath* parameter in [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) and the *SearchPath* parameter in [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) take a pointer to a null-terminated string that specifies a path, or series of paths separated by a semicolon.</span></span> <span data-ttu-id="5d29f-111">符號處理常式會使用這些路徑來搜尋符號檔。</span><span class="sxs-lookup"><span data-stu-id="5d29f-111">The symbol handler uses these paths to search for symbol files.</span></span> <span data-ttu-id="5d29f-112">如果這個參數是 **Null**，符號處理常式會搜尋包含要搜尋符號之模組的目錄。</span><span class="sxs-lookup"><span data-stu-id="5d29f-112">If this parameter is **NULL**, the symbol handler searches the directory that contains the module for which symbols are being searched.</span></span> <span data-ttu-id="5d29f-113">否則，如果將這個參數指定為非 **Null** 值，符號處理常式會先搜尋應用程式所設定的路徑，然後再搜尋模組目錄。</span><span class="sxs-lookup"><span data-stu-id="5d29f-113">Otherwise, if this parameter is specified as a non-**NULL** value, the symbol handler first searches the paths set by the application before searching the module directory.</span></span> <span data-ttu-id="5d29f-114">如果您設定 \_ nt \_ 符號 \_ 路徑或 \_ nt \_ ALT \_ 符號 \_ 路徑環境變數，符號處理常式會依下列順序搜尋符號檔：</span><span class="sxs-lookup"><span data-stu-id="5d29f-114">If you set the \_NT\_SYMBOL\_PATH or \_NT\_ALT\_SYMBOL\_PATH environment variable, the symbol handler searches for symbol files in the following order:</span></span>

1. <span data-ttu-id="5d29f-115">\_NT \_ 符號 \_ 路徑環境變數。</span><span class="sxs-lookup"><span data-stu-id="5d29f-115">The \_NT\_SYMBOL\_PATH environment variable.</span></span>
2. <span data-ttu-id="5d29f-116">\_NT \_ ALT \_ 符號 \_ 路徑環境變數。</span><span class="sxs-lookup"><span data-stu-id="5d29f-116">The \_NT\_ALT\_SYMBOL\_PATH environment variable.</span></span>
3. <span data-ttu-id="5d29f-117">包含對應模組的目錄。</span><span class="sxs-lookup"><span data-stu-id="5d29f-117">The directory that contains the corresponding module.</span></span>

<span data-ttu-id="5d29f-118">若要取出搜尋路徑，請呼叫 [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) 函數。</span><span class="sxs-lookup"><span data-stu-id="5d29f-118">To retrieve the search paths, call the [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) function.</span></span>

<span data-ttu-id="5d29f-119">程式資料庫 ( .pdb) 檔的搜尋路徑與 debug ( 的路徑不同) 。</span><span class="sxs-lookup"><span data-stu-id="5d29f-119">The search path for program database (.pdb) files is different than the path for debug (.dbg) files.</span></span> <span data-ttu-id="5d29f-120">演算法是由符號庫的功能所決定。</span><span class="sxs-lookup"><span data-stu-id="5d29f-120">The algorithm is determined by the functionality of the symbol library.</span></span> <span data-ttu-id="5d29f-121">根據預設，Microsoft Visual C/c + + 會建立 Microsoft 格式符號，從影像中移除它們，然後將它們放在個別的 .pdb 檔案中。</span><span class="sxs-lookup"><span data-stu-id="5d29f-121">By default, Microsoft Visual C/C++ creates Microsoft format symbols, strips them from the image, and places them in a separate .pdb file.</span></span> <span data-ttu-id="5d29f-122">一般而言，.pdb 檔案將位於包含可執行檔映射的目錄中。</span><span class="sxs-lookup"><span data-stu-id="5d29f-122">Typically, the .pdb file will be located in the directory that contains the executable image.</span></span> <span data-ttu-id="5d29f-123">Visual C/c + + 會在可執行檔映射中內嵌 .pdb 檔案的絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="5d29f-123">Visual C/C++ embeds the absolute path to the .pdb file in the executable image.</span></span> <span data-ttu-id="5d29f-124">如果符號處理常式在該位置找不到 .pdb 檔案，或 .pdb 檔案已移至另一個目錄，則符號處理常式會使用針對 dbg 檔案所描述的搜尋路徑來尋找 .pdb 檔。</span><span class="sxs-lookup"><span data-stu-id="5d29f-124">If the symbol handler cannot find the .pdb file in that location or if the .pdb file was moved to another directory, the symbol handler will locate the .pdb file using the search path described for .dbg files.</span></span>

## <a name="path-element-types"></a><span data-ttu-id="5d29f-125">Path 元素類型</span><span class="sxs-lookup"><span data-stu-id="5d29f-125">Path Element Types</span></span>

<span data-ttu-id="5d29f-126">有三種類型的路徑元素。</span><span class="sxs-lookup"><span data-stu-id="5d29f-126">There are three types of path elements.</span></span>

### <a name="standard-path-element"></a><span data-ttu-id="5d29f-127">標準路徑元素</span><span class="sxs-lookup"><span data-stu-id="5d29f-127">Standard Path Element</span></span>

<span data-ttu-id="5d29f-128">搜尋 path 元素所指定之目錄的根目錄，以搜尋標準路徑元素。</span><span class="sxs-lookup"><span data-stu-id="5d29f-128">A standard path element is searched by looking in the root of the directory specified by the path element.</span></span> <span data-ttu-id="5d29f-129">符號處理常式也會在「符號」子目錄中尋找符合要尋找符號之模組的副檔名。</span><span class="sxs-lookup"><span data-stu-id="5d29f-129">The symbol handler also looks in a subdirectory of "symbols" that matches the file extension of the module that symbols are being looked for.</span></span> <span data-ttu-id="5d29f-130">這通常是 "dll"、"exe" 或 "sys"。</span><span class="sxs-lookup"><span data-stu-id="5d29f-130">This is typically "dll", "exe", or "sys".</span></span> <span data-ttu-id="5d29f-131">最後，它會在名為「符號」的子目錄中尋找具有與擴充功能相同名稱的目錄。</span><span class="sxs-lookup"><span data-stu-id="5d29f-131">Lastly, it looks in a subdirectory called "symbols" with a directory of the same name as the extension.</span></span> <span data-ttu-id="5d29f-132">例如，如果符號路徑元素是 "c： \\ mySymbols"，而搜尋符號的檔案是 "boo.dll"，則會搜尋下列目錄。</span><span class="sxs-lookup"><span data-stu-id="5d29f-132">For example, if the symbol path element is "c:\\mySymbols" and the file that symbols are being searched for is "boo.dll", then the following directories would be searched.</span></span>

- <span data-ttu-id="5d29f-133">c： \\ mySymbols</span><span class="sxs-lookup"><span data-stu-id="5d29f-133">c:\\mySymbols</span></span>  
- <span data-ttu-id="5d29f-134">c： \\ mySymbols \\ dll</span><span class="sxs-lookup"><span data-stu-id="5d29f-134">c:\\mySymbols\\dll</span></span>  
- <span data-ttu-id="5d29f-135">c： \\ mySymbols \\ 符號 \\ dll</span><span class="sxs-lookup"><span data-stu-id="5d29f-135">c:\\mySymbols\\symbols\\dll</span></span>  

<span data-ttu-id="5d29f-136">符號處理常式會使用此邏輯來搜尋不符合準則的任何路徑元素，以做為 *符號伺服器* 或 *快* 取 (如下) 所述。</span><span class="sxs-lookup"><span data-stu-id="5d29f-136">The symbol handler uses this logic to search any path element that does not meet the criteria to be a *symbol server* or *cache* (described below).</span></span>

### <a name="symbol-server-path-element"></a><span data-ttu-id="5d29f-137">符號伺服器路徑元素</span><span class="sxs-lookup"><span data-stu-id="5d29f-137">Symbol Server Path Element</span></span>

<span data-ttu-id="5d29f-138">*符號伺服器* 路徑專案所使用的特殊技術，可以找出與有問題的模組完全相符的符號。</span><span class="sxs-lookup"><span data-stu-id="5d29f-138">A *symbol server* path element uses special technology that can locate a symbol that is an exact match for the module in question.</span></span> <span data-ttu-id="5d29f-139">如需詳細資訊，請參閱 [使用 SymSrv](using-symsrv.md) 。</span><span class="sxs-lookup"><span data-stu-id="5d29f-139">See [Using SymSrv](using-symsrv.md) for more details.</span></span>

<span data-ttu-id="5d29f-140">符號處理常式會將路徑元素視為符號伺服器（如果開頭為文字 "srv \* "）。</span><span class="sxs-lookup"><span data-stu-id="5d29f-140">The symbol handler treats a path element as a symbol server if it begins with the text, "srv\*".</span></span>

> [!Note]  
> <span data-ttu-id="5d29f-141">如果 \* 未指定 "srv" 文字，但實際的 path 元素是符號伺服器存放區，則符號處理常式將會如同指定了 "srv \* " 一樣。</span><span class="sxs-lookup"><span data-stu-id="5d29f-141">If the "srv\*" text is not specified but the actual path element is a symbol server store, then the symbol handler will act as if "srv\*" were specified.</span></span> <span data-ttu-id="5d29f-142">符號處理常式會搜尋指定路徑的根目錄中名為 "pingme.txt" 的檔案是否存在，以進行這項判斷。</span><span class="sxs-lookup"><span data-stu-id="5d29f-142">The symbol handler makes this determination by searching for the existence of a file called "pingme.txt" in the root directory of the specified path.</span></span>

 

### <a name="cache-path-element"></a><span data-ttu-id="5d29f-143">Cache Path 元素</span><span class="sxs-lookup"><span data-stu-id="5d29f-143">Cache Path Element</span></span>

<span data-ttu-id="5d29f-144">「快 *取路徑」* 元素是符號伺服器路徑元素的變化。</span><span class="sxs-lookup"><span data-stu-id="5d29f-144">A *cache* path element is a variation on a symbol server path element.</span></span>

<span data-ttu-id="5d29f-145">此目錄的搜尋方式就像任何其他符號伺服器。</span><span class="sxs-lookup"><span data-stu-id="5d29f-145">This directory is searched like any other symbol server.</span></span> <span data-ttu-id="5d29f-146">但是，如果在這裡找不到符號，並且在符號路徑的鏈中找到較遠的路徑元素，則會將符號複製並儲存在此專案所指定的符號伺服器中。</span><span class="sxs-lookup"><span data-stu-id="5d29f-146">However, if the symbol is not found here and it is found in a path element farther down the chain of the symbol path, then the symbol will be copied and stored in the symbol server specified in this element.</span></span>

<span data-ttu-id="5d29f-147">符號處理常式會將路徑元素視為快取專案，如果其開頭為 "cache" 文字 \* 。</span><span class="sxs-lookup"><span data-stu-id="5d29f-147">The symbol handler treats a path element as a cache element if it begins with the text, "cache\*".</span></span> <span data-ttu-id="5d29f-148">若要在 "c： Mycache maxmemory-policy" 中指定快取 \\ ，請使用 "cache \* c： mycache maxmemory-policy" 的符號路徑元素 \\ 。</span><span class="sxs-lookup"><span data-stu-id="5d29f-148">To specify a cache in "c:\\myCache", use a symbol path element of "cache\*c:\\myCache".</span></span>

## <a name="example-search-path"></a><span data-ttu-id="5d29f-149">搜尋路徑範例</span><span class="sxs-lookup"><span data-stu-id="5d29f-149">Example Search Path</span></span>

<span data-ttu-id="5d29f-150">若要查看其運作方式，請設定此搜尋路徑。</span><span class="sxs-lookup"><span data-stu-id="5d29f-150">To see how this works, set this search path.</span></span>

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

<span data-ttu-id="5d29f-151">以下是使用上述搜尋路徑搜尋 ntdll.dll 時，符號處理常式的詳細資訊輸出清單。</span><span class="sxs-lookup"><span data-stu-id="5d29f-151">The following is a listing of the symbol handler's verbose output while searching for ntdll.pdb, using the above listed search path.</span></span>

```
DBGHELP: .\ntdll.pdb - file not found
DBGHELP: .\dll\ntdll.pdb - file not found
DBGHELP: .\symbols\dll\ntdll.pdb - file not found
SYMSRV: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb not found
SYMSRV: ntdll.pdb from \\symbols\symbols: 10497024 bytes - copied
DBGHELP: c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb already cached
DBGHELP: ntdll - private symbols & lines
c:\myCache\ntdll.pdb\0F7FCF88442F4B0E9FB51DC4A754D9DE2\ntdll.pdb
```

<span data-ttu-id="5d29f-152">輸出的前三行顯示符號處理常式，處理的第一個路徑元素 `.` 。</span><span class="sxs-lookup"><span data-stu-id="5d29f-152">The first three lines of output show the symbol handler processing the first path element of `.`.</span></span> <span data-ttu-id="5d29f-153">這是標準路徑元素。</span><span class="sxs-lookup"><span data-stu-id="5d29f-153">This is a standard path element.</span></span>

<span data-ttu-id="5d29f-154">第四行顯示符號處理常式，使用符號伺服器在的第二個 path 元素中尋找檔案， `cache*c:\myCache` 其為快取路徑元素。</span><span class="sxs-lookup"><span data-stu-id="5d29f-154">The fourth line shows the symbol handler using the symbol server to look for the file in the second path element of `cache*c:\myCache` which is a cache path element.</span></span>

<span data-ttu-id="5d29f-155">第五行顯示檔案是在的第三個 path 元素 `srv*\\symbols\symbols` （符號伺服器路徑元素）中找到。</span><span class="sxs-lookup"><span data-stu-id="5d29f-155">The fifth line shows the file is found in the third path element of `srv*\\symbols\symbols`, which is a symbol server path element.</span></span>

<span data-ttu-id="5d29f-156">第六行顯示將檔案複製到快取。</span><span class="sxs-lookup"><span data-stu-id="5d29f-156">The sixth line shows that the file is copied to the cache.</span></span>

<span data-ttu-id="5d29f-157">從快取中開啟檔案的最後兩行。</span><span class="sxs-lookup"><span data-stu-id="5d29f-157">The last two lines that the file is opened from the cache.</span></span>
