---
description: 如果您在程式碼中使用泛型資料類型，則可以使用預處理器指示詞來定義 &0034，以針對 Unicode 進行編譯： \#UNICODE&\# 0034; 在 \# 標頭檔的 include 語句之前。
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: 使用泛型資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a61bed094506f0d31718b0b88fe519028ba1db785ebda3e00404a7aa3257e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535459"
---
# <a name="using-generic-data-types"></a>使用泛型資料類型

如果您在程式碼中使用泛型資料類型，則可以使用預處理器指示詞，在標頭檔的 **\# include** 語句之前定義 "unicode"，以編譯 [Unicode](unicode.md) 。 若要編譯[Windows (ANSI) 字碼頁](code-pages.md)的程式碼，請省略 "UNICODE" 定義。 新的 Windows 應用程式應該使用 Unicode 來避免不同字碼頁的不一致，並簡化當地語系化。

若要建立可編譯成使用 Unicode 字元和字串的原始程式碼，或是使用 Windows 字碼頁的字元和字串：

1.  針對文字所使用的所有字元和字串類型使用泛型資料類型，例如 TCHAR、LPTSTR 和 LPTCH。 如需泛型型別的詳細資訊，請參閱[Windows 資料類型的字串](windows-data-types-for-strings.md)。
2.  請確定非文字資料緩衝區或二進位位元組陣列的指標會以資料類型（例如 LPBYTE 或 LPWORD）進行編碼，而不是使用 LPTSTR 或 LPTCH 類型。
3.  適當地使用 LPVOID，將不定類型的指標明確宣告為 void 指標。
4.  將指標算術類型設為獨立。 如果已定義 UNICODE，則使用 TCHAR 大小的單位會產生2個位元組的變數，而如果未定義 UNICODE，則會產生1個位元組。 如果元素的大小為1或2個位元組，使用指標算術一律會傳回指標所指出的元素數目。 下列運算式一律會抓取專案數目，而不論是否已定義 UNICODE。

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    下列運算式會決定所使用的位元組數目。

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    不需要變更如下的語句，因為指標遞增指向下一個字元元素。

    ```C++
    chNext = *++lpText;
    ```

    

5.  使用宏取代常值字串和資訊清單字元常數。 變更運算式，如下所示。

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    在此運算式中使用 [**文字**](/windows/desktop/api/Winnt/nf-winnt-text) 宏，如下所示。

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    在定義 UNICODE 時， [**文字**](/windows/desktop/api/Winnt/nf-winnt-text) 宏會將字串評估為 L "string"，否則會是 "string"。 為了更容易管理，請將常值字串移至資源，特別是如果它們包含 ASCII 範圍以外的字元 (0x00 到 0x7F) 或在使用者介面公開。 為了針對不同國語言支援您應用程式的當地語系化，所有使用者介面字串都必須在可當地語系化的資源中，這點非常重要。

6.  使用 Windows 函數的泛型版本。 如需詳細資訊，請參閱 [函數原型的慣例](conventions-for-function-prototypes.md)。
7.  使用標準 C 程式庫字串函式的泛型版本，並記得定義 " \_ unicode" 和 "unicode"，如 [標準 c](standard-c-functions.md)函式中所述。
8.  如果您要調整原本針對 Windows 字碼頁所撰寫的應用程式，請記得將任何依賴255的程式碼變更為最大的字元值。

當您編譯如上面所述撰寫的程式碼時，編譯器可以從相同來源同時建立 Unicode 和 Windows 程式字碼頁版本。 根據 unicode 的定義，會解析泛型函式來產生相同的二進位檔案，就像您針對 unicode 或專門針對 Windows 字碼頁撰寫程式碼一樣。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Unicode 和字元集](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



