---
title: pragma 屬性
description: '\ Pragma midl \_ echo 指示詞會指示 midl 將指定的字串（不含引號）發出至產生的標頭檔。'
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- pragma 屬性 MIDL
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ca869acddf4b0a0a098707833e889efcfccc267a3abf1949921c550cf66c773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383496"
---
# <a name="pragma-attribute"></a>pragma 屬性

\# **Pragma midl \_ echo** 指示詞會指示 midl 將指定的字串（不含引號字元）發出至產生的標頭檔。

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a>參數

<dl> <dt>

*string* 
</dt> <dd>

指定插入產生的標頭檔中的字串。 插入過程中會移除引號。

</dd> <dt>

*權杖順序* 
</dt> <dd>

指定在產生的標頭檔中插入為 **\# pragma** 指示詞一部分的權杖順序，而不是由 MIDL 編譯器處理。

</dd> <dt>

*n* 
</dt> <dd>

指定目前的套件大小。 有效值為 1、2、4、8 和 16。

</dd> <dt>

*id* 
</dt> <dd>

指定使用者識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

出現在 IDL 檔案中的 c 語言前置處理指示詞是由 C 編譯器的預處理器所處理。 在 MIDL 編譯期間，可以使用 IDL 檔案中的 **\# 定義** 指示詞，但不能使用 C 編譯器。

例如，當預處理器遇到「定義 WINDOWS 4」指示詞時 \# ，預處理器會將 IDL 檔案中所有出現的 "WINDOWS" 取代為 "4"。 C 編譯時間不提供符號 "WINDOWS"。

若要允許 C 預處理器巨集定義傳遞 MIDL 編譯器至 C 編譯器，請使用 **\# pragma MIDL \_ echo** 或 [**cpp \_ 引號**](cpp-quote.md)指示詞。 這些指示詞會指示 MIDL 編譯器產生包含參數字串的標頭檔，並移除引號。 **\# Pragma midl \_ echo** 和 **cpp \_ 引號** 指示詞是相等的。

MIDL 編譯器會使用 **\# pragma pack** 指示詞來控制結構的封裝。 它會覆寫 [**/Zp**](-zp.md) 命令列參數。 Pack (*n*) 選項會將目前的套件大小設定為特定的值：1、2、4、8或16。 套件 (推送) 和套件 (pop) 選項具有下列特性：

-   編譯器會維護封裝堆疊。 封裝堆疊的元素包含套件大小和選擇性 *識別碼*。堆疊僅受限於堆疊頂端有目前套件大小的可用記憶體。
-   封裝 (推送) 會導致目前的套件大小推送至封裝堆疊。 堆疊受到可用記憶體的限制。
-   套件 (推入，*n*) 與套件 (推入) ，接著套件 (*n*) 相同。
-   套件 (推送， *識別碼*) 也會將 *識別碼* 和套件大小一起推送至封裝堆疊。
-   套件 (推送、 *識別碼*、 *n*) 與套件 (推送、 *識別碼*) ，然後再加上套件 (*n*) 相同。
-   Pack (pop) 會導致推出封裝堆疊。 不對稱的 pop 會導致警告，並將目前的套件大小設定為命令列值。
-   如果指定了 pack (pop、 *id*、 *n*) ，則會忽略 *n* 。

MIDL 編譯器會將 [**\\ cpp \_ 引號**](cpp-quote.md)和 **pragma** 指示詞中所指定的字串，以 idl 檔案中指定的順序，以及 idl 檔案中其他介面元件的相對順序，放在標頭檔中。 在所有匯 [**入**](import.md) 作業之後，字串通常應該會出現在 IDL 檔案的介面主體區段中。

MIDL 編譯器不會嘗試處理開頭不是前置詞 "MIDL" 的 **\# pragma** 指示詞 \_ 。 IDL 檔案中的其他 **\# pragma** 指示詞會傳遞至產生的標頭檔，而不會有任何變更。

## <a name="examples"></a>範例

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**cpp \_ 引號**](cpp-quote.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**進口**](import.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




