---
title: 處理 IDL 檔案中的定義
description: 此頁面描述為何以 \ 定義定義的符號會從 MIDL 編譯器產生的 H 檔案消失，以及可以完成的工作。 這項說明適用于 MIDL 所處理的任何檔案，例如 \ .idl、acf、.h 檔案。
ms.assetid: 148dabda-96cc-4f7c-abc7-4bf78ac166ea
keywords:
- MIDL 編譯器 MIDL，處理定義
- 定義 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c8a63423943d72326b16d53272f63d6efbe7d614661990560b00989be04cf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979699"
---
# <a name="dealing-with-defines-in-idl-files"></a>處理 \# IDL 檔案中的定義

此頁面描述使用 **\# 定義** 定義的符號為何會從 MIDL 編譯器產生的 H 檔案消失，以及可以完成的工作。 這項說明適用于 MIDL 所處理的任何檔案，例如 \* .idl、 \* . acf、 \* .h 檔案。

**\# 定義** 符號的消失是 MIDL 將預先處理的輸入檔委派給預處理器的結果。 根據預設，預處理器是組建環境中的 C/c + + 預處理器。 在前置處理之後，MIDL 接收的輸入資料流程只會有 \# 行預處理器指示詞。 尤其是，預處理器會展開輸入檔中的所有巨集定義，因此 MIDL 無法偵測到它們的存在。 因此，當 MIDL 將輸入檔中的型別定義複寫到產生的 H 檔案時， \# 就不會複寫定義。 因此， \# 如果稍後從產生的 H 檔案使用，請勿直接在 IDL 檔案中使用定義。

建議您採用下列四種解決方法：

-   使用 [**const**](const.md) 宣告規格。
-   使用匯入或包含在 IDL 檔案中的個別標頭檔，稍後包含在 C 原始程式碼中。
-   使用 IDL 檔案中的列舉常數。
-   使用 [**cpp \_ 引號**](cpp-quote.md)在產生的標頭檔中重現 **\# 定義**。

您可以使用 **IDL 常數宣告語法** 來重現資訊清單常數。 請注意，IDL 常數宣告中的 [**常數**](const.md) 與 c/c + + **const** 語義不同，只是導入 idl 編譯的命名常數。 例如：

``` syntax
const short ARRSIZE = 10
```

這個範例會指定 **ARRSIZE** 是值為10的常數。 您可以在 IDL 陣列宣告子中使用已命名的常數，以及 C 程式設計人員會使用資訊清單定義的其他位置。 此外，此語法會導致在標頭檔中產生下行：

``` syntax
#define ARRSIZE 10
```

處理 define 語句的另一種方式 **\#** ，是將它們封裝在個別的標頭檔中，放在專門用來定義語句的檔案， **\#** 或只包含型別定義的檔案中。 IDL 檔案和 C 原始程式檔都可以安全地同時包含預處理器指示詞的檔案。 雖然 MIDL 編譯器所產生的標頭檔中將無法使用指示詞，但 C 來來源程式可包含個別的標頭檔。 以類似的方式， **\#** 可以從 IDL 檔案匯入具有定義語句和一般類型定義的標頭檔。 這種方法 **\#** 會在 H 檔案中使用定義和 typedef 語句，讓 **\#** 定義符號不會直接在匯入 IDL 檔案中使用。 將標頭或 IDL 檔案匯入至另一個 IDL 檔案，可防止 typedef 語句複寫到 MIDL 所產生的 H 檔案 (這與 **\#** include 語句) 相反。 這種方法可讓原始的標頭檔在產生的 H 檔中安全地從 C 程式碼參考，而不會有重複定義的問題。

在 IDL 檔案中使用列舉常數也是有效的。 這些常數可以在 IDL 的常數運算式中使用，例如，在陣列宣告子中。 C 編譯器預處理器不會在 MIDL 編譯的早期階段中移除列舉常數，因此可在 MIDL 編譯器所產生的標頭檔中使用列舉常數。 以下列陳述式為例：

``` syntax
typedef enum midlworkaround { MAXSTRINGCOUNT = 300 };
```

C 預處理器不會在 MIDL 編譯期間移除此語句，而且 typedef 將會複寫至產生的 H 檔案。 常數 MAXSTRINGCOUNT 適用于 C 來來源程式，其中包括 MIDL 編譯器所產生的標頭檔。

最後，MIDL 的 [**cpp \_ 引號**](cpp-quote.md) 指示詞可以用來將任一字元串直接寫到產生的 H 檔案中。 例如，若要取得先前在此頁面上使用 **cpp \_ 引號** 的資訊清單常數，可以使用下列語句：

``` syntax
cpp_quote ("#define ARRSIZE 10")
```

此語句會導致在標頭檔中產生下行：

``` syntax
#define ARRSIZE 10
```

 

 




