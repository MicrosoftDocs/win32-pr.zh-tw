---
title: 型別定義、結構宣告和匯入
description: 型別定義、結構宣告和匯入可以出現在介面主體之外。
ms.assetid: 5d9011ab-bfc4-41f6-bd69-953660191652
keywords:
- 介面 MIDL、類型定義
- 介面 MIDL、結構聲明
- 介面 MIDL、imports
- 類型定義 MIDL
- 結構聲明 MIDL
- 匯入 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca1f80bca0a5d03ea0e935b05f973a6370c4180c9ce5c0fe7dea5d8f5c9c7de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829218"
---
# <a name="type-definitions-construct-declarations-and-imports"></a>型別定義、結構宣告和匯入

型別定義、結構宣告和匯入可以出現在介面主體之外。 所有來自主要 IDL 檔案的定義都會出現在產生的標頭檔中，而主要 IDL 檔案中所有介面的所有程式都會產生存根常式。 這可讓支援多個介面的應用程式將 IDL 檔案合併成單一合併的 IDL 檔。

因此，編譯檔案需要較少的時間，而且也允許 MIDL 減少產生的存根中的冗余。 這可以透過共用基底介面和衍生介面的通用程式碼的能力，大幅改善 [**物件**](object.md) 介面。 若是非 **物件** 介面，程式名稱在所有介面中都必須是唯一的。 針對 **物件** 介面，程式名稱只需要在介面內是唯一的。 請注意，當您使用 [**/osf**](-osf.md) 參數時，不允許使用多個介面。

## <a name="declarative-constructs"></a>宣告式結構

IDL 檔案中宣告式結構的語法類似于 C 的語法。 MIDL 支援所有的 Microsoft C/c + + 宣告式結構，但以下除外：

-   較舊的樣式宣告子，允許在沒有類型規範的情況下指定宣告子，例如：

    ``` syntax
    x (y) 
    short x (y)
    ```

-   具有初始化運算式 (MIDL 的宣告只接受符合 MIDL [**const**](const.md) 語法) 的宣告。

[**Import**](import.md)關鍵字會指定要匯入的一或多個 IDL 檔案的名稱。 匯入指示詞類似 C [**include**](include.md) 指示詞，但只有資料類型會 assimilated 到匯入的 IDL 檔案中。

## <a name="constant-declaration"></a>常數宣告

常數宣告會指定 [**布林值**](boolean.md)、整數、字元、寬字元、字串和 **void \** _ 常數。 如需詳細資訊，請參閱 [_ *const* *](const.md)。

## <a name="general-declaration"></a>一般宣告

一般宣告類似于 C [**typedef**](typedef.md) 語句加上 IDL 型別屬性。 除了在 [**/osf**](-osf.md) 模式中，MIDL 編譯器也會允許變數定義形式的隱含宣告。

## <a name="function-declaration"></a>函式宣告

函式宣告子是一般宣告的特殊案例。 您可以使用 IDL 屬性來指定函式傳回類型和每個參數的行為。

## <a name="examples"></a>範例

``` syntax
[ 
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(3.1), 
    pointer_default(unique) 
] 
interface IdlGrammarExample 
{ 
    import "windows.idl", "other.idl"; 
    const wchar_t * NAME = L"Example Program"; 
    typedef char * PCHAR; 
 
    HRESULT DictCheckSpelling( 
        [in, string] PCHAR   word,     // word to look up 
        [out]        short * isPresent // 0 if not present 
    ); 
}
```

 

 




