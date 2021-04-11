---
description: 大部分的字串作業都可以使用 Unicode 和 Windows 字碼頁的相同邏輯。
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: 適用於字串的 Windows 資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027574"
---
# <a name="windows-data-types-for-strings"></a>適用於字串的 Windows 資料類型

大部分的字串作業都可以使用 [Unicode](unicode.md) 和 [Windows 字碼頁](code-pages.md)的相同邏輯。 唯一的差別在於，基本的運算單位是16位的字元 (也稱為寬字元) 用於 Unicode，而8位字元則適用于 Windows 字碼頁。 Windows 標頭檔提供數種類型定義，可讓您輕鬆地建立可針對 Unicode 或 Windows 字碼頁編譯的來源。

Windows 支援三組字元和字串資料類型：一組可以針對 Unicode 或 Windows 字碼頁編譯的泛型型別定義，以及兩組特定的類型定義。 一組特定的型別定義適用于 Unicode，而另一組則是用來搭配 Windows 字碼頁使用。

使用泛型資料類型的應用程式只要在標頭檔的 **\# include** 語句之前定義 "unicode"，或在編譯期間定義 "unicode"，就可以針對 Unicode 編譯。 新的 Windows 應用程式應該使用 Unicode 來避免不同字碼頁的不一致，並簡化當地語系化。 它們應該以泛型資料類型撰寫，且應該定義 "UNICODE"，以便將這些類型編譯成 Unicode 類型。 在應用程式必須使用8位字元資料的幾個地方，它可以明確地使用 Windows 字碼頁的類型。

將泛型型別編譯成 Windows 字碼頁類型的能力，主要是為了支援繼承應用程式。 若要針對 Windows 字碼頁進行編譯，應用程式只會省略 UNICODE 定義。

下列範例顯示 Windows 標頭檔中用來定義三組資料類型的方法。 若要執行此程式，請參閱 Winnt 標頭檔。


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



類型定義中的字母 "T" （例如，TCHAR 或 LPTSTR）會指定可針對 Windows 字碼頁或 Unicode 編譯的泛型型別。 型別定義中的字母 "W" （例如，WCHAR 或 LPWSTR）會指定 Unicode 型別。 由於 Windows 字碼頁的格式較舊，因此它們具有簡單的型別定義，例如 CHAR 和 LPSTR。 如需 Windows 中資料類型的完整說明，請參閱 [Windows 資料類型](../winprog/windows-data-types.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows API 中的 Unicode](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
