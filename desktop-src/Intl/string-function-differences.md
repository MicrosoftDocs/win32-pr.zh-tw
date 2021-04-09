---
description: 本主題說明用來處理 Unicode 和字元集資訊的字串函數之間的差異。 這些函式都有 Unicode 和 Windows 字碼頁的實作為支援 Unicode 和 Windows 字碼頁參數。
ms.assetid: 52a15957-b44b-49ba-b915-e5c8e003a7e6
title: 字串函數差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c940aa8be1603f7958fb1993cc521ca7b1ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943848"
---
# <a name="string-function-differences"></a>字串函數差異

本主題說明用來處理 Unicode 和字元集資訊的字串函數之間的差異。 這些函式都有 [unicode](unicode.md) 和 [windows 字碼頁](code-pages.md) 的實作為支援 unicode 和 windows 字碼頁參數。

下列字串函數不需要特殊批註。 其 Unicode 和 Windows 字碼頁的執行方式均相同。

-   [**CharNext**](/windows/win32/api/winuser/nf-winuser-charnexta)
-   [**CharPrev**](/windows/win32/api/winuser/nf-winuser-charpreva)
-   [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata)、 [ **StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)
-   [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya)、 [ **StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa)
-   [**StrCbLength**](/windows/win32/api/strsafe/nf-strsafe-stringcblengtha)、 [ **StrCchLength**](/windows/win32/api/strsafe/nf-strsafe-stringcchlengtha)

其中一個字串長度函式所抓取的長度值一律以一般字元寬度為依據：適用于 Windows 字碼頁的8位、Unicode 的16位。 此值通常稱為「字元計數」。 因為使用 [雙位元組字元集](double-byte-character-sets.md) 的 Windows 字碼頁 (dbcs) 有一些全形字元實際上是以兩個連續的位元組來表示，所以此詞彙完全正確。 Unicode 中的 [代理](surrogates-and-supplementary-characters.md) 程式會發生類似的情況。

下列字串函式會區分目前線程的地區設定，這些函數衍生自使用者在主控台中選取的語言。 [**Lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)和 [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)函式不會像 ANSI namesakes 一樣執行位元組比較，例如 [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp)。 相反地，它們會根據地區設定的規則來比較字串。

-   [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
-   [**CharLowerBuff**](/windows/win32/api/winuser/nf-winuser-charlowerbuffa)
-   [**CharUpper**](/windows/win32/api/winuser/nf-winuser-charuppera)
-   [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
-   [**lstrcmp**](/windows/win32/api/winbase/nf-winbase-lstrcmpa)
-   [**lstrcmpi**](/windows/win32/api/winbase/nf-winbase-lstrcmpia)

下列函式會根據所使用的版本，在 OEM 字元集和目前的 Windows 字碼頁或 Unicode 之間進行轉換：

-   [**CharToOem**](/windows/win32/api/winuser/nf-winuser-chartooema)
-   [**CharToOemBuff**](/windows/win32/api/winuser/nf-winuser-chartooembuffa)
-   [**OemToCharBuff**](/windows/win32/api/winuser/nf-winuser-oemtocharbuffa)

列印函式（例如 [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa)）支援 Unicode，方法是在其格式規格中提供下列新的和變更的資料類型。 這些格式規格會影響函數解讀對應輸入參數的方式。



| 格式規格 | Windows 字碼頁版本的資料類型 | Unicode 版本的資料類型 |
|----------------------|-----------------------------------------|-------------------------------|
| c                    | CHAR                                    | WCHAR                         |
| C                    | WCHAR                                   | CHAR                          |
| hc、hC               | CHAR                                    | CHAR                          |
| hs、hS               | LPSTR                                   | LPSTR                         |
| lc、lC               | WCHAR                                   | WCHAR                         |
| ls、lS               | LPWSTR                                  | LPWSTR                        |
| s                    | LPSTR                                   | LPWSTR                        |
| S                    | LPWSTR                                  | LPSTR                         |



 

輸出文字的資料類型一律取決於函數的版本。 當輸入參數的資料類型和輸出文字的資料類型不一致時，print 函式會視需要執行從 Unicode 轉換成目前的 Windows 字碼頁，反之亦然。

若是列印函式的 Unicode 版本，格式字串是 Unicode，就像輸出文字一樣。

> [!Caution]  
> 不佳的緩衝區處理暗喻著在涉及緩衝區溢位的許多安全性問題中。 請參閱 [>strsafe.h 參考](../menurc/strsafe-ovw.md)。 >strsafe.h 中定義的函式會在程式碼中為適當的緩衝區處理提供額外的處理。 基於這個理由，它們的目的是要取代其內建的 C/c + + 對應專案，以及特定的 Microsoft Windows 實作為方案。 如需詳細資訊，請參閱 [安全性考慮：國際化功能](security-considerations--international-features.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows API 中的 Unicode](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
