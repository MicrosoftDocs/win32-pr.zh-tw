---
title: 處理字串
description: 處理字串
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1850d531a1cff713ec71a7e96399f029794545db9b695abe5b826ed63f0f080
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075198"
---
# <a name="working-with-strings"></a>處理字串

Windows 原本就支援 UI 元素、檔案名等等的 Unicode 字串。 Unicode 是慣用的字元編碼，因為它支援所有字元集和語言。 Windows 代表使用 utf-16 編碼的 Unicode 字元，其中每個字元會編碼為16位值。 UTF-16 字元稱為 *寬* 字元，用來區別8位的 ANSI 字元。 Visual C++ 編譯器支援內建資料類型 **wchar \_ t** 的寬字元。 標頭檔中的標頭檔也會定義下列 **typedef**。


```C++
typedef wchar_t WCHAR;
```



您會在 MSDN 範例程式碼中看到這兩個版本。 若要宣告寬字元常值或寬字元字串常值，請在常值前面加上 **L** 。


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



以下是您將會看到的一些其他字串相關 typedef：



| Typedef                   | 定義       |
|---------------------------|------------------|
| **CHAR**                  | `char`           |
| **PSTR** 或 **LPSTR**     | `char*`          |
| **PCSTR** 或 **LPCSTR**   | `const char*`    |
| **PWSTR** 或 **LPWSTR**   | `wchar_t*`       |
| **PCWSTR** 或 **LPCWSTR** | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a>Unicode 和 ANSI 函數

當 Microsoft 引進 Windows 的 Unicode 支援時，它會提供兩個平行的 api 集合來分階段減緩轉換，一個用於 ANSI 字串，另一個用於 Unicode 字串。 例如，有兩個函數可設定視窗標題列的文字：

-   **SetWindowTextA** 會採用 ANSI 字串。
-   **SetWindowTextW** 會採用 Unicode 字串。

就內部而言，ANSI 版本會將字串轉譯成 Unicode。 在定義預處理器符號或 ANSI 版本時，Windows 標頭也會定義可解析為 Unicode 版本的宏 `UNICODE` 。


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



在 MSDN 中，此函式會記錄在名稱 [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)底下，雖然這實際上是宏名稱，而不是實際的函式名稱。

新的應用程式應該一律呼叫 Unicode 版本。 許多世界語言都需要 Unicode。 如果您使用 ANSI 字串，就不可能將應用程式當地語系化。 ANSI 版本的效率也較低，因為作業系統必須在執行時間將 ANSI 字串轉換為 Unicode。 根據您的喜好設定，您可以明確地呼叫 Unicode 函式（例如 **SetWindowTextW**），或使用宏。 MSDN 上的範例程式碼通常會呼叫宏，但這兩種形式完全相等。 Windows 中的最新 api 只有 Unicode 版本，沒有對應的 ANSI 版本。

## <a name="tchars"></a>TCHARs

當應用程式需要同時支援 Windows NT 以及 Windows 95、Windows 98 和 Windows 時，請根據目標平臺，針對 ANSI 或 Unicode 字串編譯相同的程式碼，是很有用的。 至此，Windows SDK 提供宏將字串對應至 Unicode 或 ANSI （視平臺而定）。



| 巨集     | Unicode   | ANSI   |
|-----------|-----------|--------|
| TCHAR     | `wchar_t` | `char` |
| TEXT ( "x" )  | `L"x"`    | `"x"`  |



 

例如，下列程式碼：


```C++
SetWindowText(TEXT("My Application"));
```



解析成下列其中一項：


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



由於所有應用程式都應該使用 Unicode，因此 **TEXT** 和 **TCHAR** 宏目前較不實用。 不過，您可能會在較舊的程式碼和一些 MSDN 程式碼範例中看到它們。

Microsoft C 執行時間程式庫的標頭會定義一組類似的宏。 例如，如果未定義， **\_ tcslen** 會解析為 **strlen** `_UNICODE` ; 否則會解析為 **wcslen**，也就是寬字元版本的 **strlen**。


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



請小心：某些標頭會使用預處理器符號，其他標頭則會搭配 `UNICODE` `_UNICODE` 底線前置詞使用。 一律定義這兩個符號。 Visual C++ 在建立新專案時，預設會設定這些專案。

## <a name="next"></a>下一個

[什麼是視窗？](what-is-a-window-.md)

 

 
