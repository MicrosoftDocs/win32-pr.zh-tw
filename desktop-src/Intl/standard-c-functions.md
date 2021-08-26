---
description: 標準 C 執行時間程式庫同時包含 Unicode UTF-16 (寬字元) 版本的字串函式，這些函式可搭配 Unicode 和位元組導向版本的字串函式使用，這些函式可搭配單一位元組字元集中的字元 (SBCSs) 。 Unicode 資料類型 WCHAR 與 ANSI C 中的資料類型 WCHAR \_ t 相容，並允許存取 Unicode 字串函數。 函數的 Unicode 版本會以字母 &\# 0034; wcs&\# 0034; (或有時 &\# 0034; \_wcs&\# 0034; ) 。 用於字碼頁的資料類型 CHAR 與 ANSI C 中的字元資料類型 char 相容，以允許存取字元字串函數。 函數位符版本的開頭是字母 &\# 0034; str&\# 0034;。 另外還有特殊版本的雙位元組字元集 (Dbcs) ，其開頭為字母 &\# 0034; \_mb&\# 0034;。
ms.assetid: a86626c1-7f90-4924-bfdd-384729bd0cc5
title: 標準 C 函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0e576dd8ad506d3d0f3379c161526dd7b9330542ca1cc575c95e3eda8e7dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130158"
---
# <a name="standard-c-functions"></a>標準 C 函數

標準 C 執行時間程式庫同時包含 Unicode UTF-16 (寬字元) 版本的字串函式，這些函式可搭配 [unicode](unicode.md) 和位元組導向版本的字串函式使用，這些函式可搭配 [單一位元組字元集](single-byte-character-sets.md) 中的字元 (SBCSs) 。 Unicode 資料類型 WCHAR 與 ANSI C 中的資料類型 WCHAR \_ t 相容，並允許存取 Unicode 字串函數。 函式的 Unicode 版本以字母 "wcs" 為開頭 (或有時是 " \_ wcs" ) 。 用於字碼頁的資料類型 CHAR 與 ANSI C 中的字元資料類型 char 相容，以允許存取字元字串函數。 函式的字元版本以字母 "str" 開頭。 另外還有特殊版本的 [雙位元組字元集](double-byte-character-sets.md) (dbcs 以字母 "mb" 開頭的) \_ 。

標準 C 執行時間程式庫包含所有標準 C 字串函數的泛型函式。 它們的開頭 \_ 是 "tcs"，而且會列在 Tchar .h 標頭檔中。 這些函數會使用一般 TCHAR 資料類型。

應用程式必須加入下列幾行，才能使用泛型函式並針對 Unicode 進行編譯。


```C++
#define _UNICODE

#include <tchar.h>
#include <wchar.h>
```



請注意，Tchar .h 和 Wchar .h 檔案都是必要的，而且 UNICODE 變數上的前置底線 \_ 也是必要的。 這是標準 C 程式庫特有的命名法。 「UNICODE」在沒有底線的情況下呈現，適用于 Microsoft Windows 執行時間。

[Wcstombs](/cpp/c-runtime-library/reference/wcstombs-wcstombs-l)和[mbstowcs](/cpp/c-runtime-library/reference/mbstowcs-s-mbstowcs-s-l)函式可以從標準 C 程式庫所支援的字元集轉換成 Unicode 和回來，但有一些限制。 如需將字串轉換成 Unicode 和從 Unicode 轉譯的詳細資訊，請參閱 [字串類型之間的轉譯](translation-between-string-types.md)。

Tchar 中定義的 [printf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) 函數支援與 >strsafe.h 相同的格式規格，例如 [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa)。 同樣地，Tchar 會定義 [wprintf](/cpp/c-runtime-library/reference/printf-printf-l-wprintf-wprintf-l) 函式，其中格式字串本身是 Unicode 字串。

> [!Caution]  
> 不佳的緩衝區處理暗喻著在涉及緩衝區溢位的許多安全性問題中。 請參閱 [>strsafe.h 參考](../menurc/strsafe-ovw.md)。 >strsafe.h 中定義的函式會在程式碼中為適當的緩衝區處理提供額外的處理。 它們的目的是要取代其內建的 c/c + + 對應專案，以及特定的 Microsoft Windows 的實作為方案。 如需詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows API 中的 Unicode](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
