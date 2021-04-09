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
# <a name="symbol-paths"></a>符號路徑

DbgHelp 程式庫會使用符號搜尋路徑來找出 ( .pdb 和 dbg 檔案) 的 debug 符號。 搜尋路徑可由一個或多個以分號分隔的路徑元素組成。

## <a name="specifying-search-paths"></a>指定搜尋路徑

若要指定符號處理常式將在其中搜尋符號檔之磁碟目錄的位置，請呼叫 [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath) 函式。 或者，您也可以在 [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)函數的 *UserSearchPath* 參數中指定符號搜尋路徑。

[**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)中的 *UserSearchPath* 參數和 [**SymSetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetsearchpath)中的 *SearchPath* 參數會採用以 null 結束的字串指標，該字串會指定路徑或以分號分隔的路徑系列。 符號處理常式會使用這些路徑來搜尋符號檔。 如果這個參數是 **Null**，符號處理常式會搜尋包含要搜尋符號之模組的目錄。 否則，如果將這個參數指定為非 **Null** 值，符號處理常式會先搜尋應用程式所設定的路徑，然後再搜尋模組目錄。 如果您設定 \_ nt \_ 符號 \_ 路徑或 \_ nt \_ ALT \_ 符號 \_ 路徑環境變數，符號處理常式會依下列順序搜尋符號檔：

1. \_NT \_ 符號 \_ 路徑環境變數。
2. \_NT \_ ALT \_ 符號 \_ 路徑環境變數。
3. 包含對應模組的目錄。

若要取出搜尋路徑，請呼叫 [**SymGetSearchPath**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsearchpath) 函數。

程式資料庫 ( .pdb) 檔的搜尋路徑與 debug ( 的路徑不同) 。 演算法是由符號庫的功能所決定。 根據預設，Microsoft Visual C/c + + 會建立 Microsoft 格式符號，從影像中移除它們，然後將它們放在個別的 .pdb 檔案中。 一般而言，.pdb 檔案將位於包含可執行檔映射的目錄中。 Visual C/c + + 會在可執行檔映射中內嵌 .pdb 檔案的絕對路徑。 如果符號處理常式在該位置找不到 .pdb 檔案，或 .pdb 檔案已移至另一個目錄，則符號處理常式會使用針對 dbg 檔案所描述的搜尋路徑來尋找 .pdb 檔。

## <a name="path-element-types"></a>Path 元素類型

有三種類型的路徑元素。

### <a name="standard-path-element"></a>標準路徑元素

搜尋 path 元素所指定之目錄的根目錄，以搜尋標準路徑元素。 符號處理常式也會在「符號」子目錄中尋找符合要尋找符號之模組的副檔名。 這通常是 "dll"、"exe" 或 "sys"。 最後，它會在名為「符號」的子目錄中尋找具有與擴充功能相同名稱的目錄。 例如，如果符號路徑元素是 "c： \\ mySymbols"，而搜尋符號的檔案是 "boo.dll"，則會搜尋下列目錄。

- c： \\ mySymbols  
- c： \\ mySymbols \\ dll  
- c： \\ mySymbols \\ 符號 \\ dll  

符號處理常式會使用此邏輯來搜尋不符合準則的任何路徑元素，以做為 *符號伺服器* 或 *快* 取 (如下) 所述。

### <a name="symbol-server-path-element"></a>符號伺服器路徑元素

*符號伺服器* 路徑專案所使用的特殊技術，可以找出與有問題的模組完全相符的符號。 如需詳細資訊，請參閱 [使用 SymSrv](using-symsrv.md) 。

符號處理常式會將路徑元素視為符號伺服器（如果開頭為文字 "srv \* "）。

> [!Note]  
> 如果 \* 未指定 "srv" 文字，但實際的 path 元素是符號伺服器存放區，則符號處理常式將會如同指定了 "srv \* " 一樣。 符號處理常式會搜尋指定路徑的根目錄中名為 "pingme.txt" 的檔案是否存在，以進行這項判斷。

 

### <a name="cache-path-element"></a>Cache Path 元素

「快 *取路徑」* 元素是符號伺服器路徑元素的變化。

此目錄的搜尋方式就像任何其他符號伺服器。 但是，如果在這裡找不到符號，並且在符號路徑的鏈中找到較遠的路徑元素，則會將符號複製並儲存在此專案所指定的符號伺服器中。

符號處理常式會將路徑元素視為快取專案，如果其開頭為 "cache" 文字 \* 。 若要在 "c： Mycache maxmemory-policy" 中指定快取 \\ ，請使用 "cache \* c： mycache maxmemory-policy" 的符號路徑元素 \\ 。

## <a name="example-search-path"></a>搜尋路徑範例

若要查看其運作方式，請設定此搜尋路徑。

`cache*c:\myCache;srv*\\symbols\symbols`

<!-- 
See example from https://docs.microsoft.com/windows-hardware/drivers/debugger/symbol-path
cache*c:\MySymbols;srv*https://msdl.microsoft.com/download/symbols
-->

以下是使用上述搜尋路徑搜尋 ntdll.dll 時，符號處理常式的詳細資訊輸出清單。

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

輸出的前三行顯示符號處理常式，處理的第一個路徑元素 `.` 。 這是標準路徑元素。

第四行顯示符號處理常式，使用符號伺服器在的第二個 path 元素中尋找檔案， `cache*c:\myCache` 其為快取路徑元素。

第五行顯示檔案是在的第三個 path 元素 `srv*\\symbols\symbols` （符號伺服器路徑元素）中找到。

第六行顯示將檔案複製到快取。

從快取中開啟檔案的最後兩行。
