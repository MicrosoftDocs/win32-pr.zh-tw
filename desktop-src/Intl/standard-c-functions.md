---
description: 標準 C 執行時間程式庫同時包含 Unicode UTF-16 (寬字元) 版本的字串函式，這些函式可搭配 Unicode 和位元組導向版本的字串函式使用，這些函式可搭配單一位元組字元集中的字元 (SBCSs) 。 Unicode 資料類型 WCHAR 與 ANSI C 中的資料類型 WCHAR \_ t 相容，並允許存取 Unicode 字串函數。 函數的 Unicode 版本會以字母 &\# 0034; wcs&\# 0034; (或有時 &\# 0034; \_wcs&\# 0034; ) 。 用於字碼頁的資料類型 CHAR 與 ANSI C 中的字元資料類型 char 相容，以允許存取字元字串函數。 函數位符版本的開頭是字母 &\# 0034; str&\# 0034;。 另外還有特殊版本的雙位元組字元集 (Dbcs) ，其開頭為字母 &\# 0034; \_mb&\# 0034;。
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: 標準 C 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6247b3707f96908ef16d887462ba06573fd8dd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852788"
---
# <a name="standard-c-functions"></a><span data-ttu-id="a670a-108">標準 C 函數</span><span class="sxs-lookup"><span data-stu-id="a670a-108">Standard C Functions</span></span>

<span data-ttu-id="a670a-109">標準 C 執行時間程式庫同時包含 Unicode UTF-16 (寬字元) 版本的字串函式，這些函式可搭配 [unicode](unicode.md) 和位元組導向版本的字串函式使用，這些函式可搭配 [單一位元組字元集](single-byte-character-sets.md) 中的字元 (SBCSs) 。</span><span class="sxs-lookup"><span data-stu-id="a670a-109">The standard C runtime libraries contain both Unicode UTF-16 (wide character) versions of string functions that can be used with [Unicode](unicode.md) and byte-oriented versions of string functions that can be used with characters from [single-byte character sets](single-byte-character-sets.md) (SBCSs).</span></span> <span data-ttu-id="a670a-110">Unicode 資料類型 WCHAR 與 ANSI C 中的資料類型 WCHAR \_ t 相容，並允許存取 Unicode 字串函數。</span><span class="sxs-lookup"><span data-stu-id="a670a-110">The Unicode data type WCHAR is compatible with the data type wchar\_t in ANSI C, and allows access to the Unicode string functions.</span></span> <span data-ttu-id="a670a-111">函式的 Unicode 版本以字母 "wcs" 為開頭 (或有時是 " \_ wcs" ) 。</span><span class="sxs-lookup"><span data-stu-id="a670a-111">The Unicode versions of the functions start with the letters "wcs" (or sometimes "\_wcs").</span></span> <span data-ttu-id="a670a-112">用於字碼頁的資料類型 CHAR 與 ANSI C 中的字元資料類型 char 相容，以允許存取字元字串函數。</span><span class="sxs-lookup"><span data-stu-id="a670a-112">The data type CHAR used for code pages is compatible with the character data type char in ANSI C, to allow access to the character string functions.</span></span> <span data-ttu-id="a670a-113">函式的字元版本以字母 "str" 開頭。</span><span class="sxs-lookup"><span data-stu-id="a670a-113">The character versions of the functions start with the letters "str".</span></span> <span data-ttu-id="a670a-114">另外還有特殊版本的 [雙位元組字元集](double-byte-character-sets.md) (dbcs 以字母 "mb" 開頭的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="a670a-114">There are also special versions for [double-byte character sets](double-byte-character-sets.md) (DBCSs) that start with the letters "\_mbs".</span></span>

<span data-ttu-id="a670a-115">標準 C 執行時間程式庫包含所有標準 C 字串函數的泛型函式。</span><span class="sxs-lookup"><span data-stu-id="a670a-115">The standard C runtime libraries include generic functions for all standard C string functions.</span></span> <span data-ttu-id="a670a-116">它們的開頭 \_ 是 "tcs"，而且會列在 Tchar .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="a670a-116">They start with "\_tcs" and are listed in the Tchar.h header file.</span></span> <span data-ttu-id="a670a-117">這些函數會使用一般 TCHAR 資料類型。</span><span class="sxs-lookup"><span data-stu-id="a670a-117">These functions use the generic TCHAR data type.</span></span>

<span data-ttu-id="a670a-118">應用程式必須加入下列幾行，才能使用泛型函式並針對 Unicode 進行編譯。</span><span class="sxs-lookup"><span data-stu-id="a670a-118">An application must add the following lines to use the generic functions and compile for Unicode.</span></span>


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



<span data-ttu-id="a670a-119">請注意，Tchar .h 和 Wchar .h 檔案都是必要的，而且 UNICODE 變數上的前置底線 \_ 也是必要的。</span><span class="sxs-lookup"><span data-stu-id="a670a-119">Note that both the Tchar.h and Wchar.h files are required, and that the leading underscore on the \_UNICODE variable is also required.</span></span> <span data-ttu-id="a670a-120">這是標準 C 程式庫特有的命名法。</span><span class="sxs-lookup"><span data-stu-id="a670a-120">This nomenclature is specific to the standard C library.</span></span> <span data-ttu-id="a670a-121">未以底線轉譯的「UNICODE」適用于 Microsoft Windows 執行時間。</span><span class="sxs-lookup"><span data-stu-id="a670a-121">"UNICODE" rendered without the underscore is for the Microsoft Windows runtimes.</span></span>

<span data-ttu-id="a670a-122">[Wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l)和[mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l)函式可以從標準 C 程式庫所支援的字元集轉換成 Unicode 和回來，但有一些限制。</span><span class="sxs-lookup"><span data-stu-id="a670a-122">The [wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l) and [mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l) functions can convert from the character set supported by the standard C library to Unicode and back, with some limitations.</span></span> <span data-ttu-id="a670a-123">如需將字串轉換成 Unicode 和從 Unicode 轉譯的詳細資訊，請參閱 [字串類型之間的轉譯](translation-between-string-types.md)。</span><span class="sxs-lookup"><span data-stu-id="a670a-123">For more information about translating strings to and from Unicode, see [Translation Between String Types](translation-between-string-types.md).</span></span>

<span data-ttu-id="a670a-124">Tchar 中定義的 [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) 函數支援與 >strsafe.h 相同的格式規格，例如 [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa)。</span><span class="sxs-lookup"><span data-stu-id="a670a-124">The [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function defined in Tchar.h supports the same format specifications as the Strsafe.h print functions, for example [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa).</span></span> <span data-ttu-id="a670a-125">同樣地，Tchar 會定義 [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) 函式，其中格式字串本身是 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="a670a-125">Similarly, Tchar.h defines a [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) function, in which the format string itself is a Unicode string.</span></span>

> [!Caution]  
> <span data-ttu-id="a670a-126">不佳的緩衝區處理暗喻著在涉及緩衝區溢位的許多安全性問題中。</span><span class="sxs-lookup"><span data-stu-id="a670a-126">Poor buffer handling is implicated in many security issues that involve buffer overruns.</span></span> <span data-ttu-id="a670a-127">請參閱 [>strsafe.h 參考](../menurc/strsafe-ovw.md)。</span><span class="sxs-lookup"><span data-stu-id="a670a-127">See [Strsafe.h Reference](../menurc/strsafe-ovw.md).</span></span> <span data-ttu-id="a670a-128">>strsafe.h 中定義的函式會在程式碼中為適當的緩衝區處理提供額外的處理。</span><span class="sxs-lookup"><span data-stu-id="a670a-128">The functions defined in Strsafe.h provide additional processing for proper buffer handling in your code.</span></span> <span data-ttu-id="a670a-129">它們的目的是要取代其內建的 C/c + + 對應專案，以及特定的 Microsoft Windows 實作為方案。</span><span class="sxs-lookup"><span data-stu-id="a670a-129">They are intended to replace their built-in C/C++ counterparts as well as specific Microsoft Windows implementations.</span></span> <span data-ttu-id="a670a-130">如需詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。</span><span class="sxs-lookup"><span data-stu-id="a670a-130">For more information, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a670a-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="a670a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a670a-132">Windows API 中的 Unicode</span><span class="sxs-lookup"><span data-stu-id="a670a-132">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
